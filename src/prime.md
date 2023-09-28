# 素数筛

# 试除法

朴素判断x是否为素数

```cpp
bool is_prime(int x) {
    if (x < 2)
        return false;
    for (int i = 2; (LL) i * i <= x; i++) {
        if (x % i == 0)
            return false;
    }
    return true;
}
```



## 埃氏筛

时间复杂度`O(nloglogn)`, np代表不是素数，遍历1 - n,找到一个!np[i]的素数，然后删掉这个素数的倍数。

```cpp
const int MAXN = 1e6 + 10;
bool prime[MAXN];

void init(int n) {
    memset(prime, 1, sizeof prime);
    prime[0] = prime[1] = false;

    for (int i = 2; i * i <= n; i++) {
        if (prime[i]) {
            for (int j = i * i; j <= n; j += i) {
                prime[j] = false;
            }
        }
    }
}
```

# 欧拉筛

```cpp
const int MAXN = 1e6 + 10;
bool is_prime[MAXN];
vector<int> primes;

void init(int n) {
    memset(is_prime, 1, sizeof is_prime);
    is_prime[0] = is_prime[1] = false;

    for (int i = 2; i <= n; i++) {
        if (is_prime[i])
            primes.push_back(i);

        for (int p : primes) {
            if (p * i > n)
                break;
            is_prime[p * i] = false;
            if (i % p == 0)
                break;
        }
    }
}
```