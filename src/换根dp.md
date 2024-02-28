# 换根DP

给定一棵n个节点无向树（n个节点，n-1条无向边的连通图），要求选出一个节点，使得该节点做为根节点时，所有节点的深度和最大。
某个节点的深度被定义为 该节点与根节点的距离。

朴素算法，对每个节点dfs来计算深度和。

https://www.luogu.com.cn/problem/P3478


```cpp
void solve() {
    int n; cin >> n;
    vector<vector<int>> g(n + 1);

    for (int i = 0; i < n - 1; i++) {
        int x, y;
        cin >> x >> y;
        g[x].push_back(y);
        g[y].push_back(x);
    }

    vector<int> siz(n + 1);
    vector<int> ans(n + 1);

    function<void(int, int, int)> dfs = [&] (int x, int fa, int d) {
        siz[x] = 1;
        ans[1] += d;
        for (int y : g[x]) {
            if (y != fa) {
                dfs(y, x, d + 1);
                siz[x] += siz[y];
            }
        }
    };

    dfs(1, 0, 0);

    function<void(int, int)> reroot = [&](int x, int fa) {
        for (int y : g[x]) {
            if (y != fa) {
                ans[y] = ans[x] + siz[1] - 2 * siz[y];
                reroot(y, x);
            }
        }
    };

    reroot(1, 0);

    int p = max_element(ans.begin() + 1, ans.end()) - ans.begin();
    cout << p << '\n';
}
```