# KMP
https://www.luogu.com.cn/problem/P3375

给定两个字符串a, b, 求b在a中第一次出现的位置。
下标从0开始

```cpp
int kmp(const string &a, const string &b) {
    vector<int> ne;

    auto getNext = [&] {
        ne.resize(b.size() + 1);
        int j = 0;
        ne[0] = 0;
        for (int i = 1; i < b.size(); i++) {
            while (j > 0 && b[i] != b[j])
                j = ne[j - 1];

            if (b[i] == b[j]) j++;
            ne[i] = j;
        }
    };
    getNext();

    int i = 0, j = 0;
    int ans = -1;
    for (int i = 0; i < a.size(); i++) {
        while(j > 0 && b[j] != a[i])
            j = ne[j - 1];
        if (b[j] == a[i]) ++j;
        if (j == b.size()) {
            ans = i - b.size() + 1;
            // cnt++;
            break;
        }
    }
    return ans;
}
```

给定两个字符串a, b，并输出b在a中出现的次数。
改成cnt++，删掉break即可。