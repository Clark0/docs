# 背包

## 01背包

> N件物品，装入容量V的背包，每个物品使用一次，i件物品体积为w, 价值为v, 求最大价值？

定义 $f(i, j)$ 为使用前i件物品, 且体积不超过j的最大价值, 对于物品 i 有选或不选两种策略。
不选 i, $f(i, j) = f(i - 1, j)$, 选i $f(i, j) = f(i - 1, j - w[i]) + v[i]$

$f(i, j) = max\{f(i - 1, j), f(i - 1, j - w[i]) + v[i]\}$

```cpp
int n, m;
int v[N], w[M];
int dp[N];
void knapsack()
{
    memset(dp, 0, sizeof dp);
    for (int i = 1; i <= n; i++)
    {
        for (int j = m; j >= w[i]; j--)
            dp[j] = max(dp[j], dp[j - w[i]] + v[i]);
    }
    cout << dp[m];
}
```