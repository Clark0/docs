# 最短路算法

## Floyd
多源最短路

```cpp
vector<vector<int>> dist;

void floyd(int n, vector<int> &edges) {
    dist.resize(n, vector<int>(n, 0x3f3f3f));
    for (auto &e : edges) {
        int x = e[0], y = e[1], w = e[2];
        dist[x][y] = dist[y][x] = w;
    }

    for (int i = 0; i < n; i++)
        dist[i][i] = 0;

    for (int k = 0; k < n; k++) {
        for (int i = 0; i < n; i++) {
            for (int j = 0; j < n; j++) {
                dist[i][j] = min(dist[i][j], dist[i][k] + dist[k][j]);
            }
        }
    }
}
```

https://leetcode.cn/problems/find-the-city-with-the-smallest-number-of-neighbors-at-a-threshold-distance/


# Dij
单源最短路


