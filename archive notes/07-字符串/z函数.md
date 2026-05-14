# Z 函数
对于长度为n的字符串s, z函数是一个长度为n的数组。$z[i]$ 表示从下标i开始的，为s前缀的最长子串的长度。特殊的 $z[0] = 0$;

* "aaaaa" -  $[0, 4, 3, 2, 1]$ 
* "aaabaab" -  $[0, 2, 1, 0, 2, 1, 0]$ 
* "abacaba" -  $[0, 0, 1, 0, 3, 0, 1]$ 

## 朴素算法 $O(n^2)$
```cpp
vector<int> z_function_trivial(const string &s) {
    int n = s.size();
    vector<int> z(n);
    for (int i = 1; i < n; i++) {
        while (i + z[i] < n && s[z[i]] == s[i + z[i]])
            z[i]++;
    }

    return z[i];
}
```

# 优化算法
```cpp
vector<int> z_function(const string &s) {
    int n = s.size();
    vector<int> z(n);
    int l = 0, r = 0;
    for (int i = 1; i < n; i++) {
        if (i < r) {
            z[i] = min(r - i, z[i - l]);
        }
        while (i + z[i] < n && s[z[i]] == s[i + z[i]]) {
            z[i]++;
        }
        if (i + z[i] > r) {
            l = i;
            r = i + z[i];
        }
    }
    // z[0] = n;
    return z;
}
```
https://codeforces.com/problemset/problem/432/D
