# 数位dp

https://leetcode.com/problems/number-of-digit-one/

```cpp
int countDigitOne(int num) {
    string s = to_string(num);
    int n = s.size();
    const int digit = 1;
    vector<vector<int>> dp(n, vector<int>(n, -1));

    function<int(int, int, bool, bool)> dfs = [&](int i, int cnt, bool lim, bool lead) {
        if (i >= n)
            return cnt;

        if (!lim && !lead && dp[i][cnt] != -1)
            return dp[i][cnt];

        int up = lim ? s[i] - '0' : 9;
        int res = 0;

        /// leading zeros
        if (lead)
            res += dfs(i + 1, cnt, lim && 0 == up, true);

        for (int v = 1; v <= up; v++) {
            res += dfs(i + 1, cnt + (v == digit), lim && v == up, false);
        }

        if (!lim && !lead)
            dp[i][cnt] = res;

        return res;
    };

    return dfs(0, 0, true, true);
}
```