# ST表
## RMQ问题
Range Minimum query问题，对于一个数列$A[1..n]$, 给出查询$RMQ(l, r)$, 返回区间$[l, r]$内的最小值的下标。
通常来说数列A是固定的(static)，RMQ查询是未提前得知的(on-line)。

## ST表
ST表基于倍增思想。例如，对于一个整数 $13 = (1101)_2 = 8 + 4 + 1$ 可以被划分为若干个 $2^i$ 的数之和。同理对于区间
$[2, 14] = [2, 9] \bigcup [10, 13] \bigcup [14, 14]$ 也可以被划分成若干个长度为 $2^i$ 的区间。ST表预处理这些长度
为 $2^i$ 的区间的最小值。

## 预处理
使用数组 $st[i][j]$ 存储区间 $[j, j + 2^i - 1]$ 的最小值。区间长度为 $2^i$。最大区间长度为MAXN, 所以要有$K >= log_2(MAX_N)$,
K一般可以取到20。
```
const int K = 20;
int st[K + 1][MAXN];
```

区间 $[j, j + 2^i-1]$ 刚好可以划分成两段长度为 $2^{i-1}$ 的区间: $[j, j + 2^{i-1} - 1]$ 以及 $[j + 2^{i-1}, j + 2^i-1]$。
因此可以使用动态规划来处理。时间复杂度为$O(NlogN)$


```cpp
// 边界条件长度为1的区间
std::copy(array.begin(), array.end(), st[0]);

for (int i = 1; i <= K; i++)
    for (int j = 0; j + (1 << i) <= n; j++)
        st[i][j] = min(st[i - 1][j], st[i - 1][j + (1 << (i - 1))]);
```

## 查询
对于 $RMQ(l, r)$ 查询, 可以把查询划分成两个长度为 $2^i$ 的区间 $[L, L + 2^i - 1]$ 以及 $[R - 2^i + 1, R]$, 显然需要满足
$L + 2^i - 1 <= R$ && $R-2^i + 1 >= L$。因此可以取到 $i = log_2(R - L + 1)$。这两个区间可能相交，且并集为 $[L, R]$

对于如何计算 $log_2(x)$
```cpp
// 预处理
int lg[MAXN + 1];
lg[1] = 0;
for (int i = 2; i <= MAXN; i++)
    lg[i] = lg[i / 2] + 1;

// gcc
std::__lg(x);
```

```cpp
int query(int l, int r)
{
    int i = __lg(r - l + 1);
    return max(st[i][l], st[i][r - (1 << i) + 1]);
}
```

# 例题
[ST模版](https://www.luogu.com.cn/problem/P3865)

# 参考
https://cp-algorithms.com/data_structures/sparse-table.html#practice-problems
