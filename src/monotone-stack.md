# 单调栈

O(n)复杂度寻找左边或者右边第一个比它大小的元素。

从右向左，栈中记录下一个最大值的[候选项]
```cpp
vector<int> nextGreater(vector<int> & nums) {
    int n = nums.size();
    vector<int> ans(n, -1);
    stack<int> st;
    for (int i = n - 1; i >= 0; i--) {
        while (!st.empty() && nums[i] >= nums[st.top()])
            st.pop();

        if (!st.empty()) ans[i] = st.top();
        st.push(i);
    }
    return ans;
}
```

从左往右，栈中记录还没算出[下一个最大元素]的数的下表
```cpp
vector<int> nextGreater(vector<int> &nums) {
    int n = nums.size();
    vector<int> ans(n, -1);
    stack<int> st;

    for (int i = 0; i < n; i++) {
        while (!st.empty() && nums[st.top()] < nums[i]) {
            ans[st.top()] = i;
            st.pop();
        }

        st.push(i);
    }
    return ans;
}
```