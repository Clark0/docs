---
title: 位运算题单
aliases: [位运算（基础/性质/拆位/试填/恒等式/思维）, 灵神位运算题单]
tags:
  - leetcode
  - bitwise
  - algorithm
  - study-plan
source: 灵茶山艾府 题单
author: 灵茶山艾府 (Endlesscheng)
original: https://leetcode.cn/circle/discuss/dHn9Vk
last_update: 2025-10-06 00:30:25
---

# 位运算（基础/性质/拆位/试填/恒等式/思维）

来源：https://leetcode.cn/circle/discuss/dHn9Vk
更新：2025-10-06 00:30:25

> 说明：本文件是本地刷题依据版，保留章节层级、可勾选题目、原题链接和难度分；大段题解讲解以原题单为准。

> 推荐先阅读：[从集合论到位运算，常见位运算技巧分类总结！](https://leetcode.cn/circle/discuss/CaOJ45/)

## 一、基础题

> **用位运算代替数组操作**：

- [ ] [3370. 仅含置位位的最小整数](https://leetcode.cn/problems/smallest-number-with-all-set-bits/) 1199
- [ ] [3226. 使两个整数相等的位更改次数](https://leetcode.cn/problems/number-of-bit-changes-to-make-two-integers-equal/) 1247
- [ ] [1356. 根据数字二进制下 1 的数目排序](https://leetcode.cn/problems/sort-integers-by-the-number-of-1-bits/) 1258
- [ ] [461. 汉明距离](https://leetcode.cn/problems/hamming-distance/)
- [ ] [2220. 转换数字的最少位翻转次数](https://leetcode.cn/problems/minimum-bit-flips-to-convert-number/) 1282
- [ ] [1342. 将数字变成 0 的操作次数](https://leetcode.cn/problems/number-of-steps-to-reduce-a-number-to-zero/) 1164
- [ ] [476. 数字的补数](https://leetcode.cn/problems/number-complement/)
- [ ] [1009. 十进制整数的反码](https://leetcode.cn/problems/complement-of-base-10-integer/) 1235
- [ ] [868. 二进制间距](https://leetcode.cn/problems/binary-gap/) 1307
- [ ] [2917. 找出数组中的 K-or 值](https://leetcode.cn/problems/find-the-k-or-of-an-array/) 1389
- [ ] [693. 交替位二进制数](https://leetcode.cn/problems/binary-number-with-alternating-bits/)
- [ ] [2657. 找到两个数组的前缀公共数组](https://leetcode.cn/problems/find-the-prefix-common-array-of-two-arrays/) 1304
- [ ] [面试题 05.01. 插入](https://leetcode.cn/problems/insert-into-bits-lcci/)
- [ ] [231. 2 的幂](https://leetcode.cn/problems/power-of-two/)
- [ ] [342. 4 的幂](https://leetcode.cn/problems/power-of-four/)
- [ ] [191. 位 1 的个数](https://leetcode.cn/problems/number-of-1-bits/)
- [ ] [338. 比特位计数](https://leetcode.cn/problems/counting-bits/)
- [ ] [2595. 奇偶位数](https://leetcode.cn/problems/number-of-even-and-odd-bits/) 1207
- [ ] [2154. 将找到的值乘以 2](https://leetcode.cn/problems/keep-multiplying-found-values-by-two/) 1236
- [ ] [3211. 生成不含相邻零的二进制字符串](https://leetcode.cn/problems/generate-binary-strings-without-adjacent-zeros/) 1353
- [ ] [3690. 拆分合并数组](https://leetcode.cn/problems/split-and-merge-array-transformation/) 1982

## 二、异或（XOR）的性质

> 本质是模 $2$ 剩余系的加法。
> 另见 [数据结构题单](/lc-rating/v0/list/data_structure) 中的「**§6.4 0-1 字典树（异或字典树）**」。

- [ ] [1486. 数组异或操作](https://leetcode.cn/problems/xor-operation-in-an-array/) 1181
- [ ] [1720. 解码异或后的数组](https://leetcode.cn/problems/decode-xored-array/) 1284
- [ ] [2433. 找出前缀异或的原始数组](https://leetcode.cn/problems/find-the-original-array-of-prefix-xor/) 1367
- [x] [1310. 子数组异或查询](https://leetcode.cn/problems/xor-queries-of-a-subarray/) 1460
- [ ] [2683. 相邻值的按位异或](https://leetcode.cn/problems/neighboring-bitwise-xor/) 1518
- [ ] [1829. 每个查询的最大异或值](https://leetcode.cn/problems/maximum-xor-for-each-query/) 1523
- [ ] [2997. 使数组异或和等于 K 的最少操作次数](https://leetcode.cn/problems/minimum-number-of-operations-to-make-array-xor-equal-to-k/) 1525
- [ ] [1442. 形成两个异或相等数组的三元组数目](https://leetcode.cn/problems/count-triplets-that-can-form-two-arrays-of-equal-xor/) 1525
- [ ] [2429. 最小异或](https://leetcode.cn/problems/minimize-xor/) 1532
- [ ] [2527. 查询数组异或美丽值](https://leetcode.cn/problems/find-xor-beauty-of-array/) 1550
- [ ] [2317. 操作后的最大异或和](https://leetcode.cn/problems/maximum-xor-after-operations/) 1679
- [ ] [2588. 统计美丽子数组数目](https://leetcode.cn/problems/count-the-number-of-beautiful-subarrays/) 1697
- [ ] [2564. 子字符串异或查询](https://leetcode.cn/problems/substring-xor-queries/) 1959
- [ ] [1734. 解码异或后的排列](https://leetcode.cn/problems/decode-xored-permutation/) 2024
- [ ] [2857. 统计距离为 k 的点对](https://leetcode.cn/problems/count-pairs-of-points-with-distance-k/) 2082
- [ ] [1803. 统计异或值在范围内的数对有多少](https://leetcode.cn/problems/count-pairs-with-xor-in-a-range/) 2479
- [ ] [3215. 用偶数异或设置位计数三元组 II](https://leetcode.cn/problems/count-triplets-with-even-xor-set-bits-ii/)（会员题）

## 三、与或（AND/OR）的性质

> $\text{AND}$ 的数越多，结果越小。
> $\text{OR}$ 的数越多，结果越大。

- [ ] [2980. 检查按位或是否存在尾随零](https://leetcode.cn/problems/check-if-bitwise-or-has-trailing-zeros/) 1234
- [ ] [1318. 或运算的最小翻转次数](https://leetcode.cn/problems/minimum-flips-to-make-a-or-b-equal-to-c/) 1383
- [ ] [2419. 按位与最大的最长子数组](https://leetcode.cn/problems/longest-subarray-with-maximum-bitwise-and/) 1496
- [ ] [2871. 将数组分割成最多数目的子数组](https://leetcode.cn/problems/split-array-into-maximum-number-of-subarrays/) 1750
- [ ] [2401. 最长优雅子数组](https://leetcode.cn/problems/longest-nice-subarray/) 1750
- [ ] [2680. 最大或值](https://leetcode.cn/problems/maximum-or/) 1912
- [ ] [3133. 数组最后一个元素的最小值](https://leetcode.cn/problems/minimum-array-end/) 1935
- [ ] [3108. 带权图里旅途的最小代价](https://leetcode.cn/problems/minimum-cost-walk-in-weighted-graph/) 2109
- [ ] [3117. 划分数组得到最小的值之和](https://leetcode.cn/problems/minimum-sum-of-values-by-dividing-array/) 2735
- [ ] [3125. 使得按位与结果为 0 的最大数字](https://leetcode.cn/problems/maximum-number-that-makes-result-of-bitwise-and-zero/)（会员题）

### AND/OR LogTrick

> [LogTrick 入门教程](https://zhuanlan.zhihu.com/p/1933215367158830792)，包含原地写法，以及额外维护一个列表的写法。
> 如果你不熟悉原地去重算法，可以看 [26. 删除有序数组中的重复项](https://leetcode.cn/problems/remove-duplicates-from-sorted-array/)，[我的题解](https://leetcode.cn/problems/remove-duplicates-from-sorted-array/solutions/2807162/gen-zhao-wo-guo-yi-bian-shi-li-2ni-jiu-m-rvyk/)。
> 模板：
> ```py [sol-Python3]

## 对于每个右端点 i，计算所有子数组的或值，打印这些或值的分布范围（子数组左端点范围）

## 对于左端点在 [left, right]，右端点为 i 的子数组，OR 值都是 or_val

> def logTrick(nums: List[int]) -> None:
> or_left = []  # (子数组或值，最小左端点)
> for i, x in enumerate(nums):
> for p in or_left:
> p[0] |= x  # **根据题目修改**
> or_left.append([x, i])
> idx = 1
> for j in range(1, len(or_left)):
> if or_left[j][0] != or_left[j - 1][0]:
> or_left[idx] = or_left[j]
> idx += 1
> del or_left[idx:]
> print(i, x)
> for k, (or_val, left) in enumerate(or_left):
> right = or_left[k + 1][1] - 1 if k  orLeft = new ArrayList<>(); // (子数组或值，最小左端点)
> for (int i = 0; i & nums) {
> vector> or_left; // (子数组或值，最小左端点)
> for (int i = 0; i  nums = {4, 2, 1, 5};
> logTrick(nums);
> return 0;
> }
> go [sol-Go]
> // 对于每个右端点 i，计算所有子数组的或值，打印这些或值的分布范围（子数组左端点范围）
> // 时间复杂度 O(nlogU)，其中 U = max(nums)
> func logTrick(nums []int) {
> type pair struc...

- [ ] [3171. 找到按位或最接近 K 的子数组](https://leetcode.cn/problems/find-subarray-with-bitwise-or-closest-to-k/) 2163
- [ ] [1521. 找到最接近目标值的函数值](https://leetcode.cn/problems/find-a-value-of-a-mysterious-function-closest-to-target/) 2384
- [ ] [3097. 或值至少为 K 的最短子数组 II](https://leetcode.cn/problems/shortest-subarray-with-or-at-least-k-ii/) 1891
- [ ] [2411. 按位或最大的最小子数组长度](https://leetcode.cn/problems/smallest-subarrays-with-maximum-bitwise-or/) 1938
- [ ] [3209. 子数组按位与值为 K 的数目](https://leetcode.cn/problems/number-of-subarrays-with-and-value-of-k/) 2050
- [ ] [898. 子数组按位或操作](https://leetcode.cn/problems/bitwise-ors-of-subarrays/) 2133

### GCD LogTrick

- [ ] [2447. 最大公因数等于 K 的子数组数目](https://leetcode.cn/problems/number-of-subarrays-with-gcd-equal-to-k/) 1603
- [ ] [2654. 使数组所有元素变成 1 的最少操作次数](https://leetcode.cn/problems/minimum-number-of-operations-to-make-all-array-elements-equal-to-1/) 1929
- [ ] [3605. 数组的最小稳定性因子](https://leetcode.cn/problems/minimum-stability-factor-of-array/) 2410
- [ ] [3574. 最大子数组 GCD 分数](https://leetcode.cn/problems/maximize-subarray-gcd-score/) 2258
- [ ] [2941. 子数组的最大 GCD-Sum](https://leetcode.cn/problems/maximum-gcd-sum-of-a-subarray/)（会员题）

### 四、拆位 / 贡献法

> **十进制拆位**

- [ ] [477. 汉明距离总和](https://leetcode.cn/problems/total-hamming-distance/)
- [ ] [1863. 找出所有子集的异或总和再求和](https://leetcode.cn/problems/sum-of-all-subset-xor-totals/) 1372
- [ ] [2425. 所有数对的异或和](https://leetcode.cn/problems/bitwise-xor-of-all-pairings/) 1622
- [ ] [2275. 按位与结果大于零的最长组合](https://leetcode.cn/problems/largest-combination-with-bitwise-and-greater-than-zero/) 1642
- [ ] [1835. 所有数对按位与结果的异或和](https://leetcode.cn/problems/find-xor-sum-of-all-pairs-bitwise-and/) 1825
- [ ] [3688. 偶数的按位或运算](https://leetcode.cn/problems/bitwise-or-of-even-numbers-in-an-array/) 1205
- [ ] [2505. 所有子序列和的按位或](https://leetcode.cn/problems/bitwise-or-of-all-subsequence-sums/)（会员题）
- [ ] [3153. 所有数对中数位不同之和](https://leetcode.cn/problems/sum-of-digit-differences-of-all-pairs/) 1645

### 五、试填法

- [ ] [421. 数组中两个数的最大异或值](https://leetcode.cn/problems/maximum-xor-of-two-numbers-in-an-array/)
- [ ] [2935. 找出强数对的最大异或值 II](https://leetcode.cn/problems/maximum-strong-pair-xor-ii/) 2349
- [ ] [3007. 价值和小于等于 K 的最大数字](https://leetcode.cn/problems/maximum-number-that-sum-of-the-prices-is-less-than-or-equal-to-k/) 2258
- [ ] [3145. 大数组元素的乘积](https://leetcode.cn/problems/find-products-of-elements-of-big-array/) 2859
- [ ] [3022. 给定操作次数内使剩余元素的或值最小](https://leetcode.cn/problems/minimize-or-of-remaining-elements-using-operations/) 2918
- [ ] [3287. 求出数组中最大序列值](https://leetcode.cn/problems/find-the-maximum-sequence-value-of-array/) 2545
- [ ] [3344. 最大尺寸数组](https://leetcode.cn/problems/maximum-sized-array/)（会员题）

### 六、恒等式

- [ ] [1835. 所有数对按位与结果的异或和](https://leetcode.cn/problems/find-xor-sum-of-all-pairs-bitwise-and/) 1825
- [ ] [2354. 优质数对的数目](https://leetcode.cn/problems/number-of-excellent-pairs/) 2076

### 由于每个位的基至多一个，所以每个位只需考虑异或一个基，若能变大，则异或之

> [讲解](https://www.bilibili.com/video/BV1pm8vzAEXx/)
> 模板（最大异或和）：

- [ ] [3681. 子序列最大 XOR 值](https://leetcode.cn/problems/maximum-xor-of-subsequences/) 2027
- [ ] [3630. 划分数组得到最大异或运算和与运算之和](https://leetcode.cn/problems/partition-array-for-maximum-xor-and-and/) 2744

### 八、思维题

> 贪心、脑筋急转弯等。

- [ ] [2546. 执行逐位运算使字符串相等](https://leetcode.cn/problems/apply-bitwise-operations-to-make-strings-equal/) 1605
- [ ] [1558. 得到目标数组的最少函数调用次数](https://leetcode.cn/problems/minimum-numbers-of-function-calls-to-make-target-array/) 1637
- [ ] [2571. 将整数减少到零需要的最少操作数](https://leetcode.cn/problems/minimum-operations-to-reduce-an-integer-to-0/) 1649
- [ ] [3315. 构造最小位运算数组 II](https://leetcode.cn/problems/construct-the-minimum-bitwise-array-ii/) 1715
- [ ] [2568. 最小无法得到的或值](https://leetcode.cn/problems/minimum-impossible-or/) 1754
- [ ] [3644. 排序排列](https://leetcode.cn/problems/maximum-k-to-sort-a-permutation/) 1775
- [ ] [2509. 查询树中环的长度](https://leetcode.cn/problems/cycle-length-queries-in-a-tree/) 1948
- [ ] [2939. 最大异或乘积](https://leetcode.cn/problems/maximum-xor-product/) 2128
- [ ] [2749. 得到整数零需要执行的最少操作数](https://leetcode.cn/problems/minimum-operations-to-make-the-integer-zero/) 2132
- [ ] [2835. 使子序列的和等于目标的最少操作次数](https://leetcode.cn/problems/minimum-operations-to-form-subsequence-with-target-sum/) 2207
- [ ] [2897. 对数组执行操作使平方和最大](https://leetcode.cn/problems/apply-operations-on-array-to-maximize-sum-of-squares/) 2301
- [ ] [810. 黑板异或游戏](https://leetcode.cn/problems/chalkboard-xor-game/) 2341
- [ ] [3064. 使用按位查询猜测数字 I](https://leetcode.cn/problems/guess-the-number-using-bitwise-questions-i/)（会员题）
- [ ] [3094. 使用按位查询猜测数字 II](https://leetcode.cn/problems/guess-the-number-using-bitwise-questions-ii/)（会员题）

### 九、其他

- [ ] [136. 只出现一次的数字](https://leetcode.cn/problems/single-number/)
- [ ] [260. 只出现一次的数字 III](https://leetcode.cn/problems/single-number-iii/)
- [ ] [2965. 找出缺失和重复的数字](https://leetcode.cn/problems/find-missing-and-repeated-values/) 1245
- [ ] [137. 只出现一次的数字 II](https://leetcode.cn/problems/single-number-ii/)
- [ ] [645. 错误的集合](https://leetcode.cn/problems/set-mismatch/)
- [ ] [190. 颠倒二进制位](https://leetcode.cn/problems/reverse-bits/)
- [ ] [371. 两整数之和](https://leetcode.cn/problems/sum-of-two-integers/)
- [ ] [201. 数字范围按位与](https://leetcode.cn/problems/bitwise-and-of-numbers-range/)
- [ ] [2438. 二的幂数组中查询范围内的乘积](https://leetcode.cn/problems/range-product-queries-of-powers/) 1610
- [ ] [1680. 连接连续二进制数字](https://leetcode.cn/problems/concatenation-of-consecutive-binary-numbers/) 1630
- [ ] [1261. 在受污染的二叉树中查找元素](https://leetcode.cn/problems/find-elements-in-a-contaminated-binary-tree/) 1440
- [ ] [89. 格雷编码](https://leetcode.cn/problems/gray-code/)
- [ ] [1238. 循环码排列](https://leetcode.cn/problems/circular-permutation-in-binary-representation/) 1775
- [ ] [982. 按位与为零的三元组](https://leetcode.cn/problems/triples-with-bitwise-and-equal-to-zero/) 2085
- [ ] [3307. 找出第 K 个字符 II](https://leetcode.cn/problems/find-the-k-th-character-in-string-game-ii/) 2232
- [ ] [1611. 使整数变为 0 的最少操作次数](https://leetcode.cn/problems/minimum-one-bit-operations-to-make-integers-zero/) 2345
- [ ] [3514. 不同 XOR 三元组的数目 II](https://leetcode.cn/problems/number-of-unique-xor-triplets-ii/) 1884
- [ ] [LCP 81. 与非的谜题](https://leetcode.cn/problems/ryfUiz/)
- [ ] [751. IP 到 CIDR](https://leetcode.cn/problems/ip-to-cidr/) 2025（会员题）
- [ ] [3595. 一次或两次](https://leetcode.cn/problems/once-twice/)（会员题）
- [ ] [3141. 最大汉明距离](https://leetcode.cn/problems/maximum-hamming-distances/)（会员题）

### 算法题单
