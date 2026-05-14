# 题单（原文结构全量整理）

来源：https://leetcode.cn/discuss/post/3583665/fen-xiang-gun-ti-dan-chang-yong-shu-ju-j-bvmv/

说明：原贴中部分题目会在多个章节重复出现（按“方法/数据结构”交叉归类），这里保留原分组结构。

## 零、常用枚举技巧

### §0.1 枚举右，维护左

笔记：
- 常见套路：枚举右端点/右侧变量，把多变量约束转成“在左侧维护信息并查询”的单变量问题。
- 常用数据结构：哈希表（计数/最近位置/前缀状态等）。

#### §0.1.1 基础
- [ ] [1. 两数之和](https://leetcode.com/problems/two-sum/)
- [ ] [1512. 好数对的数目](https://leetcode.com/problems/number-of-good-pairs/) 1161
- [ ] [2441. 与对应负数同时存在的最大正整数](https://leetcode.com/problems/largest-positive-integer-that-exists-with-its-negative/) 1168
- [ ] [121. 买卖股票的最佳时机](https://leetcode.com/problems/best-time-to-buy-and-sell-stock/)
- [ ] [2016. 增量元素之间的最大差值](https://leetcode.com/problems/maximum-difference-between-increasing-elements/) 1246
- [ ] [624. 数组列表中的最大距离](https://leetcode.com/problems/maximum-distance-in-arrays/)
- [ ] [2342. 数位和相等数对的最大和](https://leetcode.com/problems/max-sum-of-a-pair-with-equal-sum-of-digits/) 1309
- [ ] [1128. 等价多米诺骨牌对的数量](https://leetcode.com/problems/number-of-equivalent-domino-pairs/description/) 1333
- [ ] [1679. K 和数对的最大数目](https://leetcode.com/problems/max-number-of-k-sum-pairs/)
- [ ] [面试题 16.24. 数对和](https://leetcode.com/problems/pairs-with-sum-lcci/)
- [ ] [219. 存在重复元素 II](https://leetcode.com/problems/contains-duplicate-ii/)
- [ ] [2260. 必须拿起的最小连续卡牌数](https://leetcode.com/problems/minimum-consecutive-cards-to-pick-up/) 1365
- [ ] [2001. 可互换矩形的组数](https://leetcode.com/problems/number-of-pairs-of-interchangeable-rectangles/) 1436
- [ ] [2815. 数组中的最大数对和](https://leetcode.com/problems/max-pair-sum-in-an-array/)
- [ ] [3623. 统计梯形的数目 I](https://leetcode.com/problems/count-number-of-trapezoids-i/) 1580
- [ ] [2364. 统计坏数对的数目](https://leetcode.com/problems/count-number-of-bad-pairs/) 1622
- [ ] [3805. 统计凯撒加密对数目](https://leetcode.com/problems/count-caesar-cipher-pairs/) 1624
- [ ] [3371. 识别数组中的最大异常值](https://leetcode.com/problems/identify-the-largest-outlier-in-an-array/) 1644
- [ ] [3761. 镜像对之间最小绝对距离](https://leetcode.com/problems/minimum-absolute-distance-between-mirror-pairs/) 1669
- [ ] [1014. 最佳观光组合](https://leetcode.com/problems/best-sightseeing-pair/) 1730
- [ ] [1814. 统计一个数组中好对子的数目](https://leetcode.com/problems/count-nice-pairs-in-an-array/)
- [ ] [3584. 子序列首尾元素的最大乘积](https://leetcode.com/problems/maximum-product-of-first-and-last-elements-of-a-subsequence/) 1763
- [ ] [2905. 找出满足差值条件的下标 II](https://leetcode.com/problems/find-indices-with-index-and-value-difference-ii/)
- [ ] [3837. 相等元素的延迟计数](https://leetcode.com/problems/delayed-count-of-equal-elements/)

#### §0.1.2 进阶
- [ ] [1010. 总持续时间可被 60 整除的歌曲](https://leetcode.com/problems/pairs-of-songs-with-total-durations-divisible-by-60/)
- [ ] [3185. 构成整天的下标对数目 II](https://leetcode.com/problems/count-pairs-that-form-a-complete-day-ii/)
- [ ] [2748. 美丽下标对的数目](https://leetcode.com/problems/number-of-beautiful-pairs/)
- [ ] [2506. 统计相似字符串对的数目](https://leetcode.com/problems/count-pairs-of-similar-strings/)
- [ ] [2874. 有序三元组中的最大值 II](https://leetcode.com/problems/maximum-value-of-an-ordered-triplet-ii/) 1583
- [ ] [1497. 检查数组对是否可以被 k 整除](https://leetcode.com/problems/check-if-array-pairs-are-divisible-by-k/) 1787
- [ ] [1031. 两个无重叠子数组的最大和](https://leetcode.com/problems/maximum-sum-of-two-non-overlapping-subarrays/) 2000
- [ ] [2555. 两个线段获得的最多奖品](https://leetcode.com/problems/maximize-win-from-two-segments/)
- [ ] [1995. 统计特殊四元组](https://leetcode.com/problems/count-special-quadruplets/)
- [ ] [3404. 统计特殊子序列的数目](https://leetcode.com/problems/count-special-subsequences/) 2445
- [ ] [3267. 统计近似相等数对 II](https://leetcode.com/problems/count-almost-equal-pairs-ii/)
- [ ] [3480. 删除一个冲突对后最大子数组数目](https://leetcode.com/problems/maximize-subarrays-after-removing-one-conflicting-pair/)
- [ ] [1214. 查找两棵二叉搜索树之和](https://leetcode.com/problems/two-sum-bsts/)
- [ ] [2964. 可被整除的三元组数量](https://leetcode.com/problems/number-of-divisible-triplet-sums/)

#### 思维扩展
- [ ] [454. 四数相加 II](https://leetcode.com/problems/4sum-ii/)
- [ ] [220. 存在重复元素 III](https://leetcode.com/problems/contains-duplicate-iii/)
- [ ] [3027. 人员站位的方案数 II](https://leetcode.com/problems/find-the-number-of-ways-to-place-people-ii/)
- [ ] [3548. 等和矩阵分割 II](https://leetcode.com/problems/equal-sum-grid-partition-ii/) 2245
- [ ] [3713. 最长的平衡子串 I](https://leetcode.com/problems/longest-balanced-substring-i/)

### §0.2 枚举中间

笔记：
- 对于 `i < j < k`（或三/四元组）这类位置约束，枚举中间变量 `j` 往往能把左右两侧拆开独立统计，再合并。
- [ ] [2909. 元素和最小的山形三元组 II](https://leetcode.com/problems/minimum-sum-of-mountain-triplets-ii/)
- [ ] [3583. 统计特殊三元组](https://leetcode.com/problems/count-special-triplets/) 1510
- [ ] [1930. 长度为 3 的不同回文子序列](https://leetcode.com/problems/unique-length-3-palindromic-subsequences/) 1533
- [ ] [3128. 直角三角形](https://leetcode.com/problems/right-triangles/) 1541
- [ ] [2874. 有序三元组中的最大值 II](https://leetcode.com/problems/maximum-value-of-an-ordered-triplet-ii/) 1583
- [ ] [447. 回旋镖的数量](https://leetcode.com/problems/number-of-boomerangs/)
- [ ] [456. 132 模式](https://leetcode.com/problems/132-pattern/)
- [ ] [3067. 在带权树网络中统计可连接服务器对数目](https://leetcode.com/problems/count-pairs-of-connectable-servers-in-a-weighted-tree-network/) 1909
- [ ] [1534. 统计好三元组](https://leetcode.com/problems/count-good-triplets/)
- [ ] [3455. 最短匹配子字符串](https://leetcode.com/problems/shortest-matching-substring/)
- [ ] [2242. 节点序列的最大得分](https://leetcode.com/problems/maximum-score-of-a-node-sequence/) 2304
- [ ] [2867. 统计树中的合法路径数目](https://leetcode.com/problems/count-valid-paths-in-a-tree/)
- [ ] [2552. 统计上升四元组](https://leetcode.com/problems/count-increasing-quadruplets/) 2433
- [ ] [3257. 放三个车的价值之和最大 II](https://leetcode.com/problems/maximum-value-sum-by-placing-three-rooks-ii/) 2553
- [ ] [3073. 最大递增三元组](https://leetcode.com/problems/maximum-increasing-triplet-value/)

### §0.3 遍历对角线

笔记：
- 适用于矩阵按对角线方向遍历/分组处理的题型。
- 原帖还提到：与“前后缀分解”相关的内容可参考其对应专题题单。
- [ ] [3446. 按对角线进行矩阵排序](https://leetcode.com/problems/sort-matrix-by-diagonals/) 1373
- [ ] [2711. 对角线上不同值的数量差](https://leetcode.com/problems/difference-of-number-of-distinct-values-on-diagonals/) 1429
- [ ] [1329. 将矩阵按对角线排序](https://leetcode.com/problems/sort-the-matrix-diagonally/) 1548
- [ ] [498. 对角线遍历](https://leetcode.com/problems/diagonal-traverse/)
- [ ] [面试题 17.23. 最大黑方阵](https://leetcode.com/problems/max-black-square-lcci/)
- [ ] [562. 矩阵中最长的连续1线段](https://leetcode.com/problems/longest-line-of-consecutive-one-in-matrix/)

## 一、前缀和

### §1.1 基础

```cpp
vector<int> nums;

// 前缀和
vector<long long> pre(nums.size() + 1);
std::partial_sum(nums.begin(), nums.end(), pre.begin() + 1);

// 推荐用左闭右开区间：子数组 `[left, right)` 的和等于 `pre[right] - pre[left]`，避免频繁 `+1/-1`
// sum of subarray [left, right)
pre[right] - pre[left];
```

- [ ] [303. 区域和检索 - 数组不可变](https://leetcode.com/problems/range-sum-query-immutable/)
- [ ] [3427. 变长子数组求和](https://leetcode.com/problems/sum-of-variable-length-subarrays/)
- [ ] [2559. 统计范围内的元音字符串数](https://leetcode.com/problems/count-vowel-strings-in-ranges/) 1435
- [ ] [1310. 子数组异或查询](https://leetcode.com/problems/xor-queries-of-a-subarray/) 1460
- [ ] [3152. 特殊数组 II](https://leetcode.com/problems/special-array-ii/) 1523
- [ ] [1749. 任意子数组和的绝对值的最大值](https://leetcode.com/problems/maximum-absolute-sum-of-any-subarray/) 1542
- [ ] [53. 最大子数组和](https://leetcode.com/problems/maximum-subarray/)
- [ ] [3652. 按策略买卖股票的最佳时机](https://leetcode.com/problems/best-time-to-buy-and-sell-stock-using-strategy/) 1557
- [ ] [3361. 两个字符串的切换距离](https://leetcode.com/problems/shift-distance-between-two-strings/)
- [ ] [3511. 构造正数组](https://leetcode.com/problems/make-a-positive-array/)
- [ ] [3540. 访问所有房屋的最短时间](https://leetcode.com/problems/minimum-time-to-visit-all-houses/)

#### 思维扩展
- [ ] [1523. 在区间范围内统计奇数数目](https://leetcode.com/problems/count-odd-numbers-in-an-interval-range/)
- [ ] [848. 字母移位](https://leetcode.com/problems/shifting-letters/) 1353

### §1.2 前缀和与哈希表

- 这类题经常和“枚举右，维护左”配合：一边推进右端点，一边用哈希表维护前缀信息来计数/找最值。
```cpp
// 统计左端点的个数
unordered_map<long long, int> cnt;
cnt[0] = -1;
for (int x : nums) {
	pre += x;
}

// 统计左端点的下标
unordered_map<long long, int> seen;
cnt[0] = -1;
for (int x : nums) {
	pre += x;
}
```

- [x] [560. 和为 K 的子数组](https://leetcode.com/problems/subarray-sum-equals-k/)
- [x] [930. 和相同的二元子数组](https://leetcode.com/problems/binary-subarrays-with-sum/) 1592
- [x] [1524. 和为奇数的子数组数目](https://leetcode.com/problems/number-of-sub-arrays-with-odd-sum/) 1611
- [x] [974. 和可被 K 整除的子数组](https://leetcode.com/problems/subarray-sums-divisible-by-k/) 1676
- [x] [523. 连续的子数组和](https://leetcode.com/problems/continuous-subarray-sum/)
- [x] [2588. 统计美丽子数组数目](https://leetcode.com/problems/count-the-number-of-beautiful-subarrays/) 1697
- [x] [525. 连续数组](https://leetcode.com/problems/contiguous-array/)
- [ ] [面试题 17.05. 字母与数字](https://leetcode.com/problems/find-longest-subarray-lcci/)
- [ ] [3755. 最大平衡异或子数组的长度](https://leetcode.com/problems/find-maximum-balanced-xor-subarray-length/)
- [ ] [3026. 最大好子数组和](https://leetcode.com/problems/maximum-good-subarray-sum/) 1817
- [x] [1477. 找两个和为目标值且不重叠的子数组](https://leetcode.com/problems/find-two-non-overlapping-sub-arrays-each-with-target-sum/)
- [x] [1546. 和为目标值且不重叠的非空子数组的最大数目](https://leetcode.com/problems/maximum-number-of-non-overlapping-subarrays-with-sum-equals-target/)
- [ ] [1124. 表现良好的最长时间段](https://leetcode.com/problems/longest-well-performing-interval/) 1908
- [ ] [3728. 边界与内部和相等的稳定子数组](https://leetcode.com/problems/stable-subarrays-with-equal-boundary-and-interior-sum/) 1909
- [ ] [3381. 长度可被 K 整除的子数组的最大元素和](https://leetcode.com/problems/maximum-subarray-sum-with-length-divisible-by-k/) 1943
- [ ] [2488. 统计中位数为 K 的子数组](https://leetcode.com/problems/count-subarrays-with-median-k/) 1999
- [ ] [1590. 使数组和能被 P 整除](https://leetcode.com/problems/make-sum-divisible-by-p/) 2039
- [ ] [2845. 统计趣味子数组的数目](https://leetcode.com/problems/count-of-interesting-subarrays/) 2073
- [ ] [3739. 统计主要元素子数组数目 II](https://leetcode.com/problems/count-subarrays-with-majority-element-ii/) 2090
- [ ] [1074. 元素和为目标值的子矩阵数量](https://leetcode.com/problems/number-of-submatrices-that-sum-to-target/) 2189
- [ ] [1442. 形成两个异或相等数组的三元组数目](https://leetcode.com/problems/count-triplets-that-can-form-two-arrays-of-equal-xor/)
- [ ] [3714. 最长的平衡子串 II](https://leetcode.com/problems/longest-balanced-substring-ii/)
- [ ] [2025. 分割数组的最多方案数](https://leetcode.com/problems/maximum-number-of-ways-to-partition-an-array/) 2218
- [ ] [3729. 统计有序数组中可被 K 整除的子数组数量](https://leetcode.com/problems/count-distinct-subarrays-divisible-by-k-in-sorted-array/) 2248
- [ ] [2949. 统计美丽子字符串 II](https://leetcode.com/problems/count-beautiful-substrings-ii/) 2445
- [ ] [325. 和等于 k 的最长子数组长度](https://leetcode.com/problems/maximum-size-subarray-sum-equals-k/)
- [ ] [548. 将数组分割成和相等的子数组](https://leetcode.com/problems/split-array-with-equal-sum/)
- [ ] [1983. 范围和相等的最宽索引对](https://leetcode.com/problems/widest-pair-of-indices-with-equal-range-sum/)
- [ ] [2489. 固定比率的子字符串数](https://leetcode.com/problems/number-of-substrings-with-fixed-ratio/)
- [ ] [2031. 1 比 0 多的子数组个数](https://leetcode.com/problems/count-subarrays-with-more-ones-than-zeros/)
- [ ] [2950. 可整除子串的数量](https://leetcode.com/problems/number-of-divisible-substrings/)

#### 前缀和与有序集合
- [ ] [3364. 最小正和子数组](https://leetcode.com/problems/minimum-positive-sum-subarray/)
- [ ] [363. 矩形区域不超过 K 的最大数值和](https://leetcode.com/problems/max-sum-of-rectangle-no-larger-than-k/)
- [ ] [3739. 统计主要元素子数组数目 II](https://leetcode.com/problems/count-subarrays-with-majority-element-ii/) 2090
- [ ] [2031. 1 比 0 多的子数组个数](https://leetcode.com/problems/count-subarrays-with-more-ones-than-zeros/)

#### 思维扩展
- [ ] [437. 路径总和 III](https://leetcode.com/problems/path-sum-iii/)

### §1.3 距离和
- [ ] [1685. 有序数组中差绝对值之和](https://leetcode.com/problems/sum-of-absolute-differences-in-a-sorted-array/) 1496
- [ ] [2615. 等值距离和](https://leetcode.com/problems/sum-of-distances/) 1793
- [ ] [2602. 使数组元素全部相等的最少操作次数](https://leetcode.com/problems/minimum-operations-to-make-all-array-elements-equal/) 1903
- [ ] [2968. 执行操作使频率分数最大](https://leetcode.com/problems/apply-operations-to-maximize-frequency-score/) 2444
- [ ] [1703. 得到连续 K 个 1 的最少相邻交换次数](https://leetcode.com/problems/minimum-adjacent-swaps-for-k-consecutive-ones/) 2467
- [ ] [3086. 拾起 K 个 1 需要的最少行动次数](https://leetcode.com/problems/minimum-moves-to-pick-k-ones/) 2673
- [ ] [3422. 将子数组元素变为相等所需的最小操作数](https://leetcode.com/problems/minimum-operations-to-make-subarray-elements-equal/)

### §1.4 状态压缩前缀和

笔记：
- 用位运算把“前缀状态”压成一个整数（比如某些字符出现奇偶性），再用哈希表统计同状态/目标状态。
- 做之前建议先过一遍常见位运算技巧（掩码、lowbit、试填等）。
- [ ] [1177. 构建回文串检测](https://leetcode.com/problems/can-make-palindrome-from-substring/) 1848
- [ ] [1371. 每个元音包含偶数次的最长子字符串](https://leetcode.com/problems/find-the-longest-substring-containing-vowels-in-even-counts/)
- [ ] [1542. 找出最长的超赞子字符串](https://leetcode.com/problems/find-the-longest-awesome-substring/)
- [ ] [1915. 最美子字符串的数目](https://leetcode.com/problems/number-of-wonderful-substrings/) 2235
- [ ] [2791. 树中可以形成回文的路径数](https://leetcode.com/problems/count-paths-that-can-form-a-palindrome-in-a-tree/) 2677

### §1.5 进阶
- [ ] [2389. 和有限的最长子序列](https://leetcode.com/problems/longest-subsequence-with-limited-sum/)
- [ ] [3709. 设计考试分数记录器](https://leetcode.com/problems/design-exam-scores-tracker/) 1648
- [ ] [1895. 最大的幻方](https://leetcode.com/problems/largest-magic-square/) 1781
- [ ] [2055. 蜡烛之间的盘子](https://leetcode.com/problems/plates-between-candles/) 1819
- [ ] [1744. 你能在你最喜欢的那天吃到你最喜欢的糖果吗？](https://leetcode.com/problems/can-you-eat-your-favorite-candy-on-your-favorite-day/)
- [ ] [1878. 矩阵中最大的三个菱形和](https://leetcode.com/problems/get-biggest-three-rhombus-sums-in-a-grid/) 1898
- [ ] [3756. 连接非零数字并乘以其数字和 II](https://leetcode.com/problems/concatenate-non-zero-digits-and-multiply-by-sum-ii/) 1968
- [ ] [1031. 两个无重叠子数组的最大和](https://leetcode.com/problems/maximum-sum-of-two-non-overlapping-subarrays/) 2000
- [ ] [2245. 转角路径的乘积中最多能有几个尾随零](https://leetcode.com/problems/maximum-trailing-zeros-in-a-cornered-path/) 2037
- [ ] [1712. 将数组分成三个子数组的方案数](https://leetcode.com/problems/ways-to-split-array-into-three-subarrays/) 2079
- [ ] [1862. 向下取整数对和](https://leetcode.com/problems/sum-of-floored-pairs/) 2170
- [ ] [3748. 统计稳定子数组的数目](https://leetcode.com/problems/count-stable-subarrays/) 2209
- [ ] [2281. 巫师的总力量和](https://leetcode.com/problems/sum-of-total-strength-of-wizards/) 2621
- [ ] [3445. 奇偶频次间的最大差值 II](https://leetcode.com/problems/maximum-difference-between-even-and-odd-frequency-ii/) 2694
- [ ] [2983. 回文串重新排列查询](https://leetcode.com/problems/palindrome-rearrangement-queries/) 2780
- [ ] [2955. 同端子串的数量](https://leetcode.com/problems/number-of-same-end-substrings/)
- [ ] [1788. 最大化花园的美观度](https://leetcode.com/problems/maximize-the-beauty-of-the-garden/)
- [ ] [2819. 购买巧克力后的最小相对损失](https://leetcode.com/problems/minimum-relative-loss-after-buying-chocolates/)

#### 思维扩展
- [ ] [2300. 咒语和药水的成功对数](https://leetcode.com/problems/successful-pairs-of-spells-and-potions/)
- [ ] [1534. 统计好三元组](https://leetcode.com/problems/count-good-triplets/)

### §1.6 二维前缀和

笔记：
- 常用做法：前缀和数组多开一圈 0 边界，矩形查询用容斥。
- 典型递推：`s[i+1][j+1] = s[i+1][j] + s[i][j+1] - s[i][j] + a[i][j]`。
- [ ] [304. 二维区域和检索 - 矩阵不可变](https://leetcode.com/problems/range-sum-query-2d-immutable/)
- [ ] [1314. 矩阵区域和](https://leetcode.com/problems/matrix-block-sum/)
- [ ] [3070. 元素和小于等于 k 的子矩阵的数目](https://leetcode.com/problems/count-submatrices-with-top-left-element-and-sum-less-than-k/)
- [ ] [1738. 找出第 K 大的异或坐标值](https://leetcode.com/problems/find-kth-largest-xor-coordinate-value/) 1671
- [ ] [3212. 统计 X 和 Y 频数相等的子矩阵数量](https://leetcode.com/problems/count-submatrices-with-equal-frequency-of-x-and-y/)
- [ ] [1292. 元素和小于等于阈值的正方形的最大边长](https://leetcode.com/problems/maximum-side-length-of-a-square-with-sum-less-than-or-equal-to-threshold/) 1735
- [ ] [3148. 矩阵中的最大得分](https://leetcode.com/problems/maximum-difference-score-in-a-grid/)

## 二、差分

### §2.1 一维差分

#### §2.1.1 基础
- [ ] [2848. 与车相交的点](https://leetcode.com/problems/points-that-intersect-with-cars/) 1230
- [ ] [1893. 检查是否区域内所有整数都被覆盖](https://leetcode.com/problems/check-if-all-the-integers-in-a-range-are-covered/) 1307
- [ ] [1854. 人口最多的年份](https://leetcode.com/problems/maximum-population-year/) 1370
- [ ] [面试题 16.10. 生存人数](https://leetcode.com/problems/living-people-lcci/)
- [ ] [2960. 统计已测试设备](https://leetcode.com/problems/count-tested-devices-after-test-operations/)
- [x] [1094. 拼车](https://leetcode.com/problems/car-pooling/) 1441
- [x] [1109. 航班预订统计](https://leetcode.com/problems/corporate-flight-bookings/) 1570
- [x] [3355. 零数组变换 I](https://leetcode.com/problems/zero-array-transformation-i/) 1591
- [ ] [370. 区间加法](https://leetcode.com/problems/range-addition/)

#### §2.1.2 进阶
- [ ] [3453. 分割正方形 I](https://leetcode.com/problems/separate-squares-i/) 1735
- [x] [2381. 字母移位 II](https://leetcode.com/problems/shifting-letters-ii/) 1793
- [x] [995. K 连续位的最小翻转次数](https://leetcode.com/problems/minimum-number-of-k-consecutive-bit-flips/) 1835
- [ ] [1589. 所有排列中的最大和](https://leetcode.com/problems/maximum-sum-obtained-of-any-permutation/)
- [ ] [1526. 形成目标数组的子数组最少增加次数](https://leetcode.com/problems/minimum-number-of-increments-on-subarrays-to-form-a-target-array/) 1872
- [ ] [3356. 零数组变换 II](https://leetcode.com/problems/zero-array-transformation-ii/) 1913
- [ ] [1943. 描述绘画结果](https://leetcode.com/problems/describe-the-painting/) 1969
- [ ] [3224. 使差值相等的最少数组改动次数](https://leetcode.com/problems/minimum-array-changes-to-make-differences-equal/) 1996
- [ ] [2327. 知道秘密的人数](https://leetcode.com/problems/number-of-people-aware-of-a-secret/)
- [ ] [2251. 花期内花的数目](https://leetcode.com/problems/number-of-flowers-in-full-bloom/)
- [ ] [2772. 使数组中的所有元素都等于零](https://leetcode.com/problems/apply-operations-to-make-all-array-elements-equal-to-zero/) 2029
- [ ] [3229. 使数组等于目标数组所需的最少操作次数](https://leetcode.com/problems/minimum-operations-to-make-array-equal-to-target/) 2067
- [ ] [3529. 统计水平子串和垂直子串重叠格子的数目](https://leetcode.com/problems/count-cells-in-overlapping-horizontal-and-vertical-substrings/) 2105
- [ ] [798. 得分最高的最小轮调](https://leetcode.com/problems/smallest-rotation-with-highest-score/) 2130
- [ ] [3347. 执行操作后元素的最高频率 II](https://leetcode.com/problems/maximum-frequency-of-an-element-after-performing-operations-ii/) 2156
- [ ] [2528. 最大化城市的最小电量](https://leetcode.com/problems/maximize-the-minimum-powered-city/)
- [ ] [1674. 使数组互补的最少操作次数](https://leetcode.com/problems/minimum-moves-to-make-array-complementary/) 2333
- [ ] [3362. 零数组变换 III](https://leetcode.com/problems/zero-array-transformation-iii/) 2424
- [ ] [3655. 区间乘法查询后的异或 II](https://leetcode.com/problems/xor-after-range-multiplication-queries-ii/) 2454
- [ ] [3017. 按距离统计房屋对数目 II](https://leetcode.com/problems/count-the-number-of-houses-at-a-certain-distance-ii/)
- [ ] [2021. 街上最亮的位置](https://leetcode.com/problems/brightest-position-on-street/)
- [ ] [2015. 每段建筑物的平均高度](https://leetcode.com/problems/average-height-of-buildings-in-each-segment/)
- [ ] [2237. 计算街道上满足所需亮度的位置数量](https://leetcode.com/problems/count-positions-on-street-with-required-brightness/)
- [ ] [3009. 折线图上的最大交点数量](https://leetcode.com/problems/maximum-number-of-intersections-on-the-chart/)
- [ ] [3279. 活塞占据的最大总面积](https://leetcode.com/problems/maximum-total-area-occupied-by-pistons/)

#### 思维扩展
- [ ] [56. 合并区间](https://leetcode.com/problems/merge-intervals/)
- [ ] [57. 插入区间](https://leetcode.com/problems/insert-interval/)
- [ ] [732. 我的日程安排表 III](https://leetcode.com/problems/my-calendar-iii/)
- [ ] [2406. 将区间分为最少组数](https://leetcode.com/problems/divide-intervals-into-minimum-number-of-groups/) 1713
- [ ] [253. 会议室 II](https://leetcode.com/problems/meeting-rooms-ii/)
- [ ] [759. 员工空闲时间](https://leetcode.com/problems/employee-free-time/)

### §2.2 二维差分

笔记：
- 一维差分可自然推广到二维：对矩形区域做增量更新，用四个角做“打标记”，最后再还原。
- [ ] [2536. 子矩阵元素加 1](https://leetcode.com/problems/increment-submatrices-by-one/) 1583
- [ ] [850. 矩形面积 II](https://leetcode.com/problems/rectangle-area-ii/)
- [ ] [2132. 用邮票贴满网格图](https://leetcode.com/problems/stamping-the-grid/)
- [ ] [LCP 74. 最强祝福力场](https://leetcode.com/problems/xepqZ5/)

## 三、栈

### §3.1 基础
- [ ] [1441. 用栈操作构建数组](https://leetcode.com/problems/build-an-array-with-stack-operations/)
- [ ] [844. 比较含退格的字符串](https://leetcode.com/problems/backspace-string-compare/) 1228
- [ ] [682. 棒球比赛](https://leetcode.com/problems/baseball-game/)
- [ ] [2390. 从字符串中移除星号](https://leetcode.com/problems/removing-stars-from-a-string/)
- [ ] [1472. 设计浏览器历史记录](https://leetcode.com/problems/design-browser-history/) 1454
- [ ] [946. 验证栈序列](https://leetcode.com/problems/validate-stack-sequences/) 1462
- [ ] [3412. 计算字符串的镜像分数](https://leetcode.com/problems/find-mirror-score-of-a-string/) 1578
- [ ] [71. 简化路径](https://leetcode.com/problems/simplify-path/)

### §3.2 进阶
- [ ] [3170. 删除星号以后字典序最小的字符串](https://leetcode.com/problems/lexicographically-minimum-string-after-removing-stars/) 1772
- [ ] [155. 最小栈](https://leetcode.com/problems/min-stack/)
- [ ] [1381. 设计一个支持增量操作的栈](https://leetcode.com/problems/design-a-stack-with-increment-operation/)
- [ ] [636. 函数的独占时间](https://leetcode.com/problems/exclusive-time-of-functions/)
- [ ] [2434. 使用机器人打印字典序最小的字符串](https://leetcode.com/problems/using-a-robot-to-print-the-lexicographically-smallest-string/) 1953
- [ ] [895. 最大频率栈](https://leetcode.com/problems/maximum-frequency-stack/)
- [ ] [1172. 餐盘栈](https://leetcode.com/problems/dinner-plate-stacks/)
- [ ] [2589. 完成所有任务的最少时间](https://leetcode.com/problems/minimum-time-to-complete-all-tasks/)
- [ ] [2524. 子数组的最大频率分数](https://leetcode.com/problems/maximum-frequency-score-of-a-subarray/)
- [ ] [716. 最大栈](https://leetcode.com/problems/max-stack/)

### §3.3 邻项消除
- [ ] [2696. 删除子串后的字符串最小长度](https://leetcode.com/problems/minimum-string-length-after-removing-substrings/) 1282
- [ ] [1047. 删除字符串中的所有相邻重复项](https://leetcode.com/problems/remove-all-adjacent-duplicates-in-string/) 1286
- [ ] [1544. 整理字符串](https://leetcode.com/problems/make-the-string-great/) 1344
- [ ] [3561. 移除相邻字符](https://leetcode.com/problems/resulting-string-after-adjacent-removals/) 1397
- [ ] [1003. 检查替换后的词是否有效](https://leetcode.com/problems/check-if-word-is-valid-after-substitutions/)
- [ ] [3834. 合并相邻且相等的元素](https://leetcode.com/problems/merge-adjacent-equal-elements/) 1429
- [ ] [2216. 美化数组的最少删除数](https://leetcode.com/problems/minimum-deletions-to-make-array-beautiful/) 1510
- [ ] [1209. 删除字符串中的所有相邻重复项 II](https://leetcode.com/problems/remove-all-adjacent-duplicates-in-string-ii/) 1542
- [ ] [3703. 移除K-平衡子字符串](https://leetcode.com/problems/remove-k-balanced-substrings/)
- [ ] [1717. 删除子字符串的最大得分](https://leetcode.com/problems/maximum-score-from-removing-substrings/) 1868
- [ ] [2197. 替换数组中的非互质数](https://leetcode.com/problems/replace-non-coprime-numbers-in-array/) 2057
- [ ] [735. 小行星碰撞](https://leetcode.com/problems/asteroid-collision/)
- [ ] [2751. 机器人碰撞](https://leetcode.com/problems/robot-collisions/) 2092

### §3.4 合法括号字符串（RBS）
- [ ] [20. 有效的括号](https://leetcode.com/problems/valid-parentheses/)
- [ ] [921. 使括号有效的最少添加](https://leetcode.com/problems/minimum-add-to-make-parentheses-valid/) 1242
- [ ] [1021. 删除最外层的括号](https://leetcode.com/problems/remove-outermost-parentheses/) 1311
- [ ] [1614. 括号的最大嵌套深度](https://leetcode.com/problems/maximum-nesting-depth-of-the-parentheses/)
- [ ] [1190. 反转每对括号间的子串](https://leetcode.com/problems/reverse-substrings-between-each-pair-of-parentheses/) 1486
- [ ] [856. 括号的分数](https://leetcode.com/problems/score-of-parentheses/) 1563
- [ ] [1249. 移除无效的括号](https://leetcode.com/problems/minimum-remove-to-make-valid-parentheses/) 1657
- [ ] [1963. 使字符串平衡的最小交换次数](https://leetcode.com/problems/minimum-number-of-swaps-to-make-the-string-balanced/)
- [ ] [678. 有效的括号字符串](https://leetcode.com/problems/valid-parenthesis-string/) 1700
- [ ] [1111. 有效括号的嵌套深度](https://leetcode.com/problems/maximum-nesting-depth-of-two-valid-parentheses-strings/)
- [ ] [1541. 平衡括号字符串的最少插入次数](https://leetcode.com/problems/minimum-insertions-to-balance-a-parentheses-string/) 1759
- [ ] [2116. 判断一个括号字符串是否有效](https://leetcode.com/problems/check-if-a-parentheses-string-can-be-valid/) 2038
- [ ] [32. 最长有效括号](https://leetcode.com/problems/longest-valid-parentheses/)

### §3.5 表达式解析
- [ ] [1006. 笨阶乘](https://leetcode.com/problems/clumsy-factorial/) 1408
- [ ] [150. 逆波兰表达式求值](https://leetcode.com/problems/evaluate-reverse-polish-notation/)
- [ ] [394. 字符串解码](https://leetcode.com/problems/decode-string/)
- [ ] [8. 字符串转换整数 (atoi)](https://leetcode.com/problems/string-to-integer-atoi/)
- [ ] [224. 基本计算器](https://leetcode.com/problems/basic-calculator/)
- [ ] [227. 基本计算器 II](https://leetcode.com/problems/basic-calculator-ii/)
- [ ] [726. 原子的数量](https://leetcode.com/problems/number-of-atoms/)
- [ ] [1106. 解析布尔表达式](https://leetcode.com/problems/parsing-a-boolean-expression/) 1880
- [ ] [591. 标签验证器](https://leetcode.com/problems/tag-validator/)
- [ ] [736. Lisp 语法解析](https://leetcode.com/problems/parse-lisp-expression/)
- [ ] [1096. 花括号展开 II](https://leetcode.com/problems/brace-expansion-ii/) 2349
- [ ] [1896. 反转表达式值的最少操作次数](https://leetcode.com/problems/minimum-cost-to-change-the-final-value-of-expression/) 2532
- [ ] [65. 有效数字](https://leetcode.com/problems/valid-number/)
- [ ] [770. 基本计算器 IV](https://leetcode.com/problems/basic-calculator-iv/)
- [ ] [439. 三元表达式解析器](https://leetcode.com/problems/ternary-expression-parser/)
- [ ] [3749. 计算有效表达式](https://leetcode.com/problems/evaluate-valid-expressions/)
- [ ] [772. 基本计算器 III](https://leetcode.com/problems/basic-calculator-iii/)
- [ ] [1087. 花括号展开](https://leetcode.com/problems/brace-expansion/)
- [ ] [1597. 根据中缀表达式构造二叉表达式树](https://leetcode.com/problems/build-binary-expression-tree-from-infix-expression/)
- [ ] [1628. 设计带解析函数的表达式树](https://leetcode.com/problems/design-an-expression-tree-with-evaluate-function/)

### §3.6 对顶栈
- [ ] [2296. 设计一个文本编辑器](https://leetcode.com/problems/design-a-text-editor/) 1912

## 四、队列

笔记：
- 队列更常用于 BFS；栈更常用于 DFS（且 DFS 很多时候不需要手写栈）。

### §4.1 基础
- [ ] [933. 最近的请求次数](https://leetcode.com/problems/number-of-recent-calls/)
- [ ] [3829. 设计共享出行系统](https://leetcode.com/problems/design-ride-sharing-system/) 1594
- [ ] [950. 按递增顺序显示卡牌](https://leetcode.com/problems/reveal-cards-in-increasing-order/) 1686
- [ ] [649. Dota2 参议院](https://leetcode.com/problems/dota2-senate/)
- [ ] [346. 数据流中的移动平均值](https://leetcode.com/problems/moving-average-from-data-stream/)
- [ ] [362. 敲击计数器](https://leetcode.com/problems/design-hit-counter/)
- [ ] [3851. 不违反限制的最大请求数](https://leetcode.com/problems/maximum-requests-without-violating-the-limit/)
- [ ] [379. 电话目录管理系统](https://leetcode.com/problems/design-phone-directory/)
- [ ] [1429. 第一个唯一数字](https://leetcode.com/problems/first-unique-number/)
- [ ] [2534. 通过门的时间](https://leetcode.com/problems/time-taken-to-cross-the-door/)

### §4.2 设计
- [ ] [1670. 设计前中后队列](https://leetcode.com/problems/design-front-middle-back-queue/) 1610
- [ ] [3508. 设计路由器](https://leetcode.com/problems/implement-router/) 1851
- [ ] [225. 用队列实现栈](https://leetcode.com/problems/implement-stack-using-queues/)
- [ ] [232. 用栈实现队列](https://leetcode.com/problems/implement-queue-using-stacks/)
- [ ] [622. 设计循环队列](https://leetcode.com/problems/design-circular-queue/)
- [ ] [641. 设计循环双端队列](https://leetcode.com/problems/design-circular-deque/)

### §4.3 双端队列
- [ ] [2810. 故障键盘](https://leetcode.com/problems/faulty-keyboard/)
- [ ] [2071. 你可以安排的最多任务数目](https://leetcode.com/problems/maximum-number-of-tasks-you-can-assign/)

### §4.4 单调队列

笔记：
- 可理解为：滑动窗口 + 单调栈。
- 通常每步先弹出过期队首；是否先入队取决于“更新答案”是否需要当前元素。

示例模板（滑动窗口最大值）：
```py
while q and nums[q[-1]] <= x: q.pop()
q.append(i)
if q[0] < left: q.popleft()
ans[left] = nums[q[0]]
```
- [ ] [239. 滑动窗口最大值](https://leetcode.com/problems/sliding-window-maximum/)
- [ ] [LCR 184. 设计自助结算系统](https://leetcode.com/problems/dui-lie-de-zui-da-zhi-lcof/)
- [ ] [1438. 绝对差不超过限制的最长连续子数组](https://leetcode.com/problems/longest-continuous-subarray-with-absolute-diff-less-than-or-equal-to-limit/) 1672
- [ ] [2762. 不间断子数组](https://leetcode.com/problems/continuous-subarrays/)
- [ ] [3835. 开销小于等于 K 的子数组数目](https://leetcode.com/problems/count-subarrays-with-cost-less-than-or-equal-to-k/) 1759
- [ ] [2398. 预算内的最多机器人数目](https://leetcode.com/problems/maximum-number-of-robots-within-budget/)
- [ ] [3589. 计数质数间隔平衡子数组](https://leetcode.com/problems/count-prime-gap-balanced-subarrays/)
- [ ] [862. 和至少为 K 的最短子数组](https://leetcode.com/problems/shortest-subarray-with-sum-at-least-k/)
- [ ] [1499. 满足不等式的最大值](https://leetcode.com/problems/max-value-of-equation/) 2456

## 五、堆（优先队列）

### §5.1 基础
- [ ] [1046. 最后一块石头的重量](https://leetcode.com/problems/last-stone-weight/) 1173
- [ ] [3264. K 次乘运算后的最终数组 I](https://leetcode.com/problems/final-array-state-after-k-multiplication-operations-i/) 1178
- [ ] [2558. 从数量最多的堆取走礼物](https://leetcode.com/problems/take-gifts-from-the-richest-pile/)
- [ ] [2336. 无限集中的最小数字](https://leetcode.com/problems/smallest-number-in-infinite-set/) 1375
- [ ] [2530. 执行 K 次操作后的最大分数](https://leetcode.com/problems/maximal-score-after-applying-k-operations/)
- [ ] [3066. 超过阈值的最少操作数 II](https://leetcode.com/problems/minimum-operations-to-exceed-threshold-value-ii/)
- [ ] [1962. 移除石子使总数最小](https://leetcode.com/problems/remove-stones-to-minimize-the-total/) 1419
- [ ] [703. 数据流中的第 K 大元素](https://leetcode.com/problems/kth-largest-element-in-a-stream/)
- [ ] [3275. 第 K 近障碍物查询](https://leetcode.com/problems/k-th-nearest-obstacle-queries/) 1420
- [ ] [1845. 座位预约管理系统](https://leetcode.com/problems/seat-reservation-manager/) 1429
- [ ] [2208. 将数组和减半的最少操作次数](https://leetcode.com/problems/minimum-operations-to-halve-array-sum/) 1550
- [ ] [2233. K 次增加后的最大乘积](https://leetcode.com/problems/maximum-product-after-k-increments/) 1686
- [ ] [3296. 移山所需的最少秒数](https://leetcode.com/problems/minimum-number-of-seconds-to-make-mountain-height-zero/) 1695
- [ ] [1942. 最小未被占据椅子的编号](https://leetcode.com/problems/the-number-of-the-smallest-unoccupied-chair/) 1695
- [ ] [1801. 积压订单中的订单总数](https://leetcode.com/problems/number-of-orders-in-the-backlog/) 1711
- [ ] [2406. 将区间分为最少组数](https://leetcode.com/problems/divide-intervals-into-minimum-number-of-groups/) 1713
- [ ] [3478. 选出和最大的 K 个元素](https://leetcode.com/problems/choose-k-elements-with-maximum-sum/) 1753
- [ ] [2462. 雇佣 K 位工人的总代价](https://leetcode.com/problems/total-cost-to-hire-k-workers/) 1764
- [ ] [1834. 单线程 CPU](https://leetcode.com/problems/single-threaded-cpu/)
- [ ] [1792. 最大平均通过率](https://leetcode.com/problems/maximum-average-pass-ratio/) 1818
- [ ] [1167. 连接木棍的最低费用](https://leetcode.com/problems/minimum-cost-to-connect-sticks/)
- [ ] [253. 会议室 II](https://leetcode.com/problems/meeting-rooms-ii/)

### §5.2 进阶
- [ ] [23. 合并 K 个升序链表](https://leetcode.com/problems/merge-k-sorted-lists/)
- [ ] [2931. 购买物品的最大开销](https://leetcode.com/problems/maximum-spending-after-buying-items/) 1822
- [ ] [3781. 二进制交换后的最大分数](https://leetcode.com/problems/maximum-score-after-binary-swaps/) 1823
- [ ] [502. IPO](https://leetcode.com/problems/ipo/)
- [ ] [1705. 吃苹果的最大数目](https://leetcode.com/problems/maximum-number-of-eaten-apples/) 1930
- [ ] [778. 水位上升的泳池中游泳](https://leetcode.com/problems/swim-in-rising-water/)
- [ ] [1631. 最小体力消耗路径](https://leetcode.com/problems/path-with-minimum-effort/) 1948
- [ ] [1882. 使用服务器处理任务](https://leetcode.com/problems/process-tasks-using-servers/) 1979
- [ ] [1354. 多次求和构造目标数组](https://leetcode.com/problems/construct-target-array-with-multiple-sums/) 2015
- [ ] [1353. 最多可以参加的会议数目](https://leetcode.com/problems/maximum-number-of-events-that-can-be-attended/) 2016
- [ ] [1235. 规划兼职工作](https://leetcode.com/problems/maximum-profit-in-job-scheduling/)
- [ ] [632. 最小区间](https://leetcode.com/problems/smallest-range-covering-elements-from-k-lists/)
- [ ] [2542. 最大子序列的分数](https://leetcode.com/problems/maximum-subsequence-score/)
- [ ] [1383. 最大的团队表现值](https://leetcode.com/problems/maximum-performance-of-a-team/)
- [ ] [2402. 会议室 III](https://leetcode.com/problems/meeting-rooms-iii/) 2093
- [ ] [2503. 矩阵查询可获得的最大分数](https://leetcode.com/problems/maximum-number-of-points-from-grid-queries/) 2196
- [ ] [2163. 删除元素后和的最小差值](https://leetcode.com/problems/minimum-difference-in-sums-after-removal-of-elements/) 2225
- [ ] [857. 雇佣 K 名工人的最低成本](https://leetcode.com/problems/minimum-cost-to-hire-k-workers/)
- [ ] [1606. 找到处理最多请求的服务器](https://leetcode.com/problems/find-servers-that-handled-most-number-of-requests/)
- [ ] [1851. 包含每个查询的最小区间](https://leetcode.com/problems/minimum-interval-to-include-each-query/)
- [ ] [407. 接雨水 II](https://leetcode.com/problems/trapping-rain-water-ii/)
- [ ] [2940. 找到 Alice 和 Bob 可以相遇的建筑](https://leetcode.com/problems/find-building-where-alice-and-bob-can-meet/) 2327
- [ ] [3399. 字符相同的最短子字符串 II](https://leetcode.com/problems/smallest-substring-with-identical-characters-ii/)
- [ ] [2589. 完成所有任务的最少时间](https://leetcode.com/problems/minimum-time-to-complete-all-tasks/)
- [ ] [3266. K 次乘运算后的最终数组 II](https://leetcode.com/problems/final-array-state-after-k-multiplication-operations-ii/) 2509
- [ ] [1675. 数组的最小偏移量](https://leetcode.com/problems/minimize-deviation-in-array/) 2533
- [ ] [2617. 网格图中最少访问的格子数](https://leetcode.com/problems/minimum-number-of-visited-cells-in-a-grid/)
- [ ] [2532. 过桥的时间](https://leetcode.com/problems/time-to-cross-a-bridge/) 2589
- [ ] [LCP 33. 蓄水](https://leetcode.com/problems/o8SXZn/)
- [ ] [1500. 设计文件分享系统](https://leetcode.com/problems/design-a-file-sharing-system/)
- [ ] [1199. 建造街区的最短时间](https://leetcode.com/problems/minimum-time-to-build-blocks/)
- [ ] [3506. 查找消除细菌菌株所需时间](https://leetcode.com/problems/find-time-required-to-eliminate-bacterial-strains/)

#### 有序集合
- [ ] [1348. 推文计数](https://leetcode.com/problems/tweet-counts-per-frequency/)
- [ ] [855. 考场就座](https://leetcode.com/problems/exam-room/)
- [ ] [1912. 设计电影租借系统](https://leetcode.com/problems/design-movie-rental-system/)

### §5.3 第 K 小/大
- [ ] [264. 丑数 II](https://leetcode.com/problems/ugly-number-ii/)
- [ ] [378. 有序矩阵中第 K 小的元素](https://leetcode.com/problems/kth-smallest-element-in-a-sorted-matrix/)
- [ ] [23. 合并 K 个升序链表](https://leetcode.com/problems/merge-k-sorted-lists/)
- [ ] [373. 查找和最小的 K 对数字](https://leetcode.com/problems/find-k-pairs-with-smallest-sums/)
- [ ] [1439. 有序矩阵中的第 k 个最小数组和](https://leetcode.com/problems/find-the-kth-smallest-sum-of-a-matrix-with-sorted-rows/) 2134
- [ ] [786. 第 K 个最小的质数分数](https://leetcode.com/problems/k-th-smallest-prime-fraction/) 2169
- [ ] [3691. 最大子数组总值 II](https://leetcode.com/problems/maximum-total-subarray-value-ii/) 2469
- [ ] [2386. 找出数组的第 K 大和](https://leetcode.com/problems/find-the-k-sum-of-an-array/) 2648

### §5.4 重排元素
- [ ] [984. 不含 AAA 或 BBB 的字符串](https://leetcode.com/problems/string-without-aaa-or-bbb/) 1474
- [ ] [767. 重构字符串](https://leetcode.com/problems/reorganize-string/) 1681
- [ ] [1054. 距离相等的条形码](https://leetcode.com/problems/distant-barcodes/)
- [ ] [1405. 最长快乐字符串](https://leetcode.com/problems/longest-happy-string/) 1821
- [ ] [3081. 替换字符串中的问号使分数最小](https://leetcode.com/problems/replace-question-marks-in-string-to-minimize-its-value/) 1905
- [ ] [621. 任务调度器](https://leetcode.com/problems/task-scheduler/)
- [ ] [358. K 距离间隔重排字符串](https://leetcode.com/problems/rearrange-string-k-distance-apart/)

### §5.5 反悔堆
- [ ] [LCP 30. 魔塔游戏](https://leetcode.com/problems/p0NxJO/)
- [ ] [1642. 可以到达的最远建筑](https://leetcode.com/problems/furthest-building-you-can-reach/) 1962
- [ ] [630. 课程表 III](https://leetcode.com/problems/course-schedule-iii/)
- [ ] [871. 最低加油次数](https://leetcode.com/problems/minimum-number-of-refueling-stops/) 2074
- [ ] [3362. 零数组变换 III](https://leetcode.com/problems/zero-array-transformation-iii/) 2424
- [ ] [2813. 子序列最大优雅度](https://leetcode.com/problems/maximum-elegance-of-a-k-length-subsequence/) 2582
- [ ] [3049. 标记所有下标的最早秒数 II](https://leetcode.com/problems/earliest-second-to-mark-indices-ii/) 3111
- [ ] [3711. 不出现负余额的最大交易额](https://leetcode.com/problems/maximum-transactions-without-negative-balance/)
- [ ] [2599. 使前缀和数组非负](https://leetcode.com/problems/make-the-prefix-sum-non-negative/)

### §5.6 懒删除堆

笔记：
- 目标：支持“删除堆中任意元素”，用计数表记录待删次数，访问堆顶前循环清理。
- 最大堆可用取反或自定义比较实现。

清理堆顶示意：
```cpp

```
- [ ] [2349. 设计数字容器系统](https://leetcode.com/problems/design-a-number-container-system/) 1540
- [ ] [3607. 电网维护](https://leetcode.com/problems/power-grid-maintenance/)
- [ ] [2353. 设计食物评分系统](https://leetcode.com/problems/design-food-rating-system/)
- [ ] [3092. 最高频率的 ID](https://leetcode.com/problems/most-frequent-ids/) 1793
- [ ] [3408. 设计任务管理器](https://leetcode.com/problems/design-task-manager/) 1807
- [ ] [2034. 股票价格波动](https://leetcode.com/problems/stock-price-fluctuation/) 1832
- [ ] [3815. 设计拍卖系统](https://leetcode.com/problems/design-auction-system/)
- [ ] [1172. 餐盘栈](https://leetcode.com/problems/dinner-plate-stacks/)
- [ ] [218. 天际线问题](https://leetcode.com/problems/the-skyline-problem/)
- [ ] [3510. 移除最小数对使数组有序 II](https://leetcode.com/problems/minimum-pair-removal-to-sort-array-ii/)
- [ ] [3672. 子数组中加权众数的总和](https://leetcode.com/problems/sum-of-weighted-modes-in-subarrays/)
- [ ] [3391. 设计一个高效的层跟踪三维二进制矩阵](https://leetcode.com/problems/design-a-3d-binary-matrix-with-efficient-layer-tracking/)
- [ ] [716. 最大栈](https://leetcode.com/problems/max-stack/)

### §5.7 对顶堆（滑动窗口第 K 小/大）

笔记：
- 常用两个堆维护“左半/右半”以支持中位数或第 K 小/大；部分题需要结合懒删除。
- 有些题也可用有序集合/权值树状数组等替代实现。
- [x] [2102. 序列顺序查询](https://leetcode.com/problems/sequentially-ordinal-rank-tracker/) 2159
- [x] [295. 数据流的中位数](https://leetcode.com/problems/find-median-from-data-stream/)
- [ ] [480. 滑动窗口中位数](https://leetcode.com/problems/sliding-window-median/)
- [ ] [2653. 滑动子数组的美丽值](https://leetcode.com/problems/sliding-subarray-beauty/)
- [ ] [1825. 求出 MK 平均值](https://leetcode.com/problems/finding-mk-average/)
- [ ] [3505. 使 K 个子数组内元素相等的最少操作数](https://leetcode.com/problems/minimum-operations-to-make-elements-within-k-subarrays-equal/)
- [ ] [3013. 将数组分成最小总代价的子数组 II](https://leetcode.com/problems/divide-an-array-into-subarrays-with-minimum-cost-ii/) 2540
- [ ] [3321. 计算子数组的 x-sum II](https://leetcode.com/problems/find-x-sum-of-all-k-long-subarrays-ii/)
- [ ] [LCP 24. 数字游戏](https://leetcode.com/problems/5TxKeK/)
- [ ] [3369. 设计数组统计跟踪器](https://leetcode.com/problems/design-an-array-statistics-tracker/)
- [ ] [3422. 将子数组元素变为相等所需的最小操作数](https://leetcode.com/problems/minimum-operations-to-make-subarray-elements-equal/)

## 六、字典树（Trie）

### §6.1 基础
- [ ] [208. 实现 Trie (前缀树)](https://leetcode.com/problems/implement-trie-prefix-tree/)
- [ ] [3597. 分割字符串](https://leetcode.com/problems/partition-string/)
- [ ] [648. 单词替换](https://leetcode.com/problems/replace-words/)
- [ ] [720. 词典中最长的单词](https://leetcode.com/problems/longest-word-in-dictionary/)
- [ ] [2416. 字符串的前缀分数和](https://leetcode.com/problems/sum-of-prefix-scores-of-strings/) 1725
- [ ] [677. 键值映射](https://leetcode.com/problems/map-sum-pairs/)
- [ ] [1268. 搜索推荐系统](https://leetcode.com/problems/search-suggestions-system/)
- [ ] [1233. 删除子文件夹](https://leetcode.com/problems/remove-sub-folders-from-the-filesystem/)
- [ ] [820. 单词的压缩编码](https://leetcode.com/problems/short-encoding-of-words/)
- [ ] [2261. 含最多 K 个可整除元素的子数组](https://leetcode.com/problems/k-divisible-elements-subarrays/)
- [ ] [1804. 实现 Trie （前缀树） II](https://leetcode.com/problems/implement-trie-ii-prefix-tree/)
- [ ] [2168. 每个数字的频率都相同的独特子字符串的数量](https://leetcode.com/problems/unique-substrings-with-equal-digit-frequency/)

### §6.2 进阶
- [ ] [211. 添加与搜索单词 - 数据结构设计](https://leetcode.com/problems/design-add-and-search-words-data-structure/)
- [ ] [676. 实现一个魔法字典](https://leetcode.com/problems/implement-magic-dictionary/)
- [ ] [212. 单词搜索 II](https://leetcode.com/problems/word-search-ii/)
- [ ] [3093. 最长公共后缀查询](https://leetcode.com/problems/longest-common-suffix-queries/) 2118
- [ ] [745. 前缀和后缀搜索](https://leetcode.com/problems/prefix-and-suffix-search/)
- [ ] [3045. 统计前后缀下标对 II](https://leetcode.com/problems/count-prefix-and-suffix-pairs-ii/)
- [ ] [336. 回文对](https://leetcode.com/problems/palindrome-pairs/)
- [ ] [1948. 删除系统中的重复文件夹](https://leetcode.com/problems/delete-duplicate-folders-in-system/) 2534
- [ ] [425. 单词方块](https://leetcode.com/problems/word-squares/)
- [ ] [527. 单词缩写](https://leetcode.com/problems/word-abbreviation/)
- [ ] [588. 设计内存文件系统](https://leetcode.com/problems/design-in-memory-file-system/)
- [ ] [616. 给字符串添加加粗标签](https://leetcode.com/problems/add-bold-tag-in-string/)
- [ ] [758. 字符串中的加粗单词](https://leetcode.com/problems/bold-words-in-string/)
- [ ] [642. 设计搜索自动补全系统](https://leetcode.com/problems/design-search-autocomplete-system/)
- [ ] [1065. 字符串的索引对](https://leetcode.com/problems/index-pairs-of-a-string/)
- [ ] [1166. 设计文件系统](https://leetcode.com/problems/design-file-system/)
- [ ] [1858. 包含所有前缀的最长单词](https://leetcode.com/problems/longest-word-with-all-prefixes/)

#### 思维扩展
- [ ] [440. 字典序的第K小数字](https://leetcode.com/problems/k-th-smallest-in-lexicographical-order/)

### §6.3 字典树优化 DP
- [ ] [139. 单词拆分](https://leetcode.com/problems/word-break/)
- [ ] [140. 单词拆分 II](https://leetcode.com/problems/word-break-ii/)
- [ ] [面试题 17.13. 恢复空格](https://leetcode.com/problems/re-space-lcci/)
- [ ] [472. 连接词](https://leetcode.com/problems/concatenated-words/)
- [ ] [2977. 转换字符串的最小成本 II](https://leetcode.com/problems/minimum-cost-to-convert-string-ii/)

### §6.4 0-1 字典树（异或字典树）

笔记：
- 主要用于异或相关题；部分题也能用“试填法”思路解决。
- [ ] [421. 数组中两个数的最大异或值](https://leetcode.com/problems/maximum-xor-of-two-numbers-in-an-array/)
- [ ] [2935. 找出强数对的最大异或值 II](https://leetcode.com/problems/maximum-strong-pair-xor-ii/)
- [ ] [3845. 最大子数组异或值](https://leetcode.com/problems/maximum-subarray-xor-with-bounded-range/)
- [ ] [1707. 与数组中元素的最大异或值](https://leetcode.com/problems/maximum-xor-with-an-element-from-array/)
- [ ] [1803. 统计异或值在范围内的数对有多少](https://leetcode.com/problems/count-pairs-with-xor-in-a-range/) 2479
- [ ] [1938. 查询最大基因差](https://leetcode.com/problems/maximum-genetic-difference-query/)
- [ ] [3632. 异或至少为 K 的子数组数目](https://leetcode.com/problems/subarrays-with-xor-at-least-k/)
- [ ] [2479. 两个不重叠子树的最大异或值](https://leetcode.com/problems/maximum-xor-of-two-non-overlapping-subtrees/)

## 七、并查集

笔记：
- 常见模板元素：`fa`（父节点/代表元）、`size`（集合大小）、`cc`（连通块数）。
- `find` 做路径压缩，`merge` 合并并更新 `size/cc`。

### §7.1 基础
- [ ] [684. 冗余连接](https://leetcode.com/problems/redundant-connection/)
- [ ] [3493. 属性图](https://leetcode.com/problems/properties-graph/) 1565
- [ ] [990. 等式方程的可满足性](https://leetcode.com/problems/satisfiability-of-equality-equations/) 1638
- [ ] [721. 账户合并](https://leetcode.com/problems/accounts-merge/)
- [ ] [3532. 针对图的路径存在性查询 I](https://leetcode.com/problems/path-existence-queries-in-a-graph-i/)
- [ ] [737. 句子相似性 II](https://leetcode.com/problems/sentence-similarity-ii/)
- [ ] [1101. 彼此熟识的最早时间](https://leetcode.com/problems/the-earliest-moment-when-everyone-become-friends/)
- [ ] [1258. 近义词句子](https://leetcode.com/problems/synonymous-sentences/)

### §7.2 进阶
- [ ] [3551. 数位和排序需要的最小交换次数](https://leetcode.com/problems/minimum-swaps-to-sort-by-digit-sum/) 1507
- [ ] [2471. 逐层排序二叉树所需的最少操作数目](https://leetcode.com/problems/minimum-number-of-operations-to-sort-a-binary-tree-by-level/) 1635
- [ ] [1202. 交换字符串中的元素](https://leetcode.com/problems/smallest-string-with-swaps/)
- [ ] [1061. 按字典序排列最小的等效字符串](https://leetcode.com/problems/lexicographically-smallest-equivalent-string/)
- [ ] [1722. 执行交换操作后的最小汉明距离](https://leetcode.com/problems/minimize-hamming-distance-after-swap-operations/) 1892
- [ ] [3608. 包含 K 个连通分量需要的最小时间](https://leetcode.com/problems/minimum-time-for-k-connected-components/) 1893
- [ ] [3613. 最小化连通分量的最大成本](https://leetcode.com/problems/minimize-maximum-component-cost/)
- [ ] [778. 水位上升的泳池中游泳](https://leetcode.com/problems/swim-in-rising-water/)
- [ ] [3695. 交换元素后的最大交替和](https://leetcode.com/problems/maximize-alternating-sum-using-swaps/)
- [ ] [765. 情侣牵手](https://leetcode.com/problems/couples-holding-hands/)
- [ ] [2092. 找出知晓秘密的所有专家](https://leetcode.com/problems/find-all-people-with-secret/) 2004
- [ ] [839. 相似字符串组](https://leetcode.com/problems/similar-string-groups/) 2054
- [ ] [685. 冗余连接 II](https://leetcode.com/problems/redundant-connection-ii/)
- [ ] [1970. 你能穿过矩阵的最后一天](https://leetcode.com/problems/last-day-where-you-can-still-cross/) 2124
- [ ] [2076. 处理含限制条件的好友请求](https://leetcode.com/problems/process-restricted-friend-requests/) 2131
- [ ] [1579. 保证图可完全遍历](https://leetcode.com/problems/remove-max-number-of-edges-to-keep-graph-fully-traversable/)
- [ ] [959. 由斜杠划分区域](https://leetcode.com/problems/regions-cut-by-slashes/) 2136
- [ ] [2812. 找出最安全路径](https://leetcode.com/problems/find-the-safest-path-in-a-grid/) 2154
- [ ] [2503. 矩阵查询可获得的最大分数](https://leetcode.com/problems/maximum-number-of-points-from-grid-queries/) 2196
- [ ] [3600. 升级后最大生成树稳定性](https://leetcode.com/problems/maximize-spanning-tree-stability-with-upgrades/)
- [ ] [2867. 统计树中的合法路径数目](https://leetcode.com/problems/count-valid-paths-in-a-tree/)
- [ ] [2421. 好路径的数目](https://leetcode.com/problems/number-of-good-paths/)
- [ ] [2157. 字符串分组](https://leetcode.com/problems/groups-of-strings/) 2499
- [ ] [803. 打砖块](https://leetcode.com/problems/bricks-falling-when-hit/)
- [ ] [3235. 判断矩形的两个角落是否可达](https://leetcode.com/problems/check-if-the-rectangle-corner-is-reachable/)
- [ ] [LCP 71. 集水器](https://leetcode.com/problems/kskhHQ/)
- [ ] [2459. 通过移动项目到空白区域来排序数组](https://leetcode.com/problems/sort-array-by-moving-items-to-empty-space/)

### §7.3 中介并查集

笔记：
- 为避免两两连边导致的 `O(n^2)`，引入“中介点”让元素连到中介上，边数通常可降到近 `O(n)`。
- [ ] [947. 移除最多的同行或同列石头](https://leetcode.com/problems/most-stones-removed-with-same-row-or-column/) 2035
- [ ] [3873. 添加一个点后可激活的最大点数](https://leetcode.com/problems/maximum-points-activated-with-one-addition/)
- [ ] [2709. 最大公约数遍历](https://leetcode.com/problems/greatest-common-divisor-traversal/)
- [ ] [1627. 带阈值的图连通性](https://leetcode.com/problems/graph-connectivity-with-threshold/) 2221
- [ ] [952. 按公因数计算最大组件大小](https://leetcode.com/problems/largest-component-size-by-common-factor/) 2272
- [ ] [1998. 数组的最大公因数排序](https://leetcode.com/problems/gcd-sort-of-an-array/) 2429
- [ ] [1632. 矩阵转换后的排名](https://leetcode.com/problems/rank-transform-of-a-matrix/) 2530
- [ ] [3378. 统计最小公倍数图中的连通块数目](https://leetcode.com/problems/count-connected-components-in-lcm-graph/)
- [ ] [2371. 最小化网格中的最大值](https://leetcode.com/problems/minimize-maximum-value-in-a-grid/)

### §7.4 数组上的并查集
- [ ] [1562. 查找大小为 M 的最新分组](https://leetcode.com/problems/find-latest-group-of-size-m/)
- [ ] [1488. 避免洪水泛滥](https://leetcode.com/problems/avoid-flood-in-the-city/) 1974
- [ ] [1353. 最多可以参加的会议数目](https://leetcode.com/problems/maximum-number-of-events-that-can-be-attended/) 2016
- [ ] [2382. 删除操作后的最大子段和](https://leetcode.com/problems/maximum-segment-sum-after-removals/) 2136
- [ ] [2334. 元素值大于变化阈值的子数组](https://leetcode.com/problems/subarray-with-elements-greater-than-varying-threshold/) 2381
- [ ] [3666. 使二进制字符串全为 1 的最少操作次数](https://leetcode.com/problems/minimum-operations-to-equalize-binary-string/)
- [ ] [2612. 最少翻转操作数](https://leetcode.com/problems/minimum-reverse-operations/)

### §7.5 区间并查集
- [ ] [3244. 新增道路查询后的最短距离 II](https://leetcode.com/problems/shortest-distance-after-road-addition-queries-ii/)
- [ ] [1851. 包含每个查询的最小区间](https://leetcode.com/problems/minimum-interval-to-include-each-query/)
- [ ] [LCP 52. 二叉搜索树染色](https://leetcode.com/problems/QO5KpG/)
- [ ] [2158. 每天绘制新区域的数量](https://leetcode.com/problems/amount-of-new-area-painted-each-day/)

### §7.6 带权并查集（边权并查集）

笔记：
- 维护 `dis[x]` 表示 `x` 到代表元的距离/权值；路径压缩时要同步累加距离。
- 合并时根据约束（如 `to - from = value`）推导两棵树根之间的相对距离。
- [ ] [399. 除法求值](https://leetcode.com/problems/evaluate-division/)
- [ ] [3710. 最大划分因子](https://leetcode.com/problems/maximum-partition-factor/) 2135
- [ ] [2307. 检查方程中的矛盾之处](https://leetcode.com/problems/check-for-contradictions-in-equations/)
- [ ] [CF1850H. H](https://codeforces.com/problemset/problem/1850/H)

## 八、树状数组和线段树

笔记：
- 一般来说：能用树状数组（Fenwick）做的，线段树也能做；但树状数组实现更短更简单。

### §8.1 树状数组

笔记：
- 典型操作都是 `O(log n)`；常见 lowbit 迭代：
```txt
i += i & -i
i &= i - 1
```
- [ ] [307. 区域和检索 - 数组可修改](https://leetcode.com/problems/range-sum-query-mutable/)
- [ ] [3072. 将元素分配到两个数组中 II](https://leetcode.com/problems/distribute-elements-into-two-arrays-ii/) 2053
- [ ] [3624. 位计数深度为 K 的整数数目 II](https://leetcode.com/problems/number-of-integers-with-popcount-depth-equal-to-k-ii/) 2086
- [ ] [3187. 数组中的峰值](https://leetcode.com/problems/peaks-in-array/) 2154
- [ ] [3777. 使子字符串变交替的最少删除次数](https://leetcode.com/problems/minimum-deletions-to-make-alternating-substring/) 2202
- [ ] [1649. 通过指令创建有序数组](https://leetcode.com/problems/create-sorted-array-through-instructions/) 2208
- [ ] [1626. 无矛盾的最佳球队](https://leetcode.com/problems/best-team-with-no-conflicts/)
- [ ] [1409. 查询带键的排列](https://leetcode.com/problems/queries-on-a-permutation-with-key/)
- [ ] [2250. 统计包含每个点的矩形数目](https://leetcode.com/problems/count-number-of-rectangles-containing-each-point/)
- [ ] [2179. 统计数组中好三元组数目](https://leetcode.com/problems/count-good-triplets-in-an-array/)
- [ ] [1395. 统计作战单位数](https://leetcode.com/problems/count-number-of-teams/)
- [ ] [2659. 将数组清空](https://leetcode.com/problems/make-array-empty/) 2282
- [ ] [2653. 滑动子数组的美丽值](https://leetcode.com/problems/sliding-subarray-beauty/)
- [ ] [3515. 带权树中的最短路径](https://leetcode.com/problems/shortest-path-in-a-weighted-tree/)
- [ ] [LCP 05. 发 LeetCoin](https://leetcode.com/problems/coin-bonus/)
- [ ] [1505. 最多 K 次交换相邻数位后得到的最小整数](https://leetcode.com/problems/minimum-possible-integer-after-at-most-k-adjacent-swaps-on-digits/) 2337
- [ ] [3841. 查询树上回文路径](https://leetcode.com/problems/palindromic-path-queries-in-a-tree/)
- [ ] [2926. 平衡子序列的最大和](https://leetcode.com/problems/maximum-balanced-subsequence-sum/) 2448
- [ ] [2736. 最大和查询](https://leetcode.com/problems/maximum-sum-queries/)
- [ ] [3671. 子序列美丽值求和](https://leetcode.com/problems/sum-of-beautiful-subsequences/) 2647
- [ ] [3382. 用点构造面积最大的矩形 II](https://leetcode.com/problems/maximum-area-rectangle-with-point-constraints-ii/)
- [ ] [3590. 第 K 小的路径异或和](https://leetcode.com/problems/kth-smallest-path-xor-sum/) 2646
- [ ] [3245. 交替组 III](https://leetcode.com/problems/alternating-groups-iii/) 3112
- [ ] [3027. 人员站位的方案数 II](https://leetcode.com/problems/find-the-number-of-ways-to-place-people-ii/)
- [ ] [1756. 设计最近使用（MRU）队列](https://leetcode.com/problems/design-most-recently-used-queue/)
- [ ] [60. 排列序列](https://leetcode.com/problems/permutation-sequence/)
- [ ] [3109. 查找排列的下标](https://leetcode.com/problems/find-the-index-of-permutation/)
- [ ] [2519. 统计 K-Big 索引的数量](https://leetcode.com/problems/count-the-number-of-k-big-indices/)
- [ ] [2613. 美数对](https://leetcode.com/problems/beautiful-pairs/)
- [ ] [2921. 价格递增的最大利润三元组 II](https://leetcode.com/problems/maximum-profitable-triplets-with-increasing-prices-ii/)
- [ ] [308. 二维区域和检索 - 可变](https://leetcode.com/problems/range-sum-query-2d-mutable/)

### §8.2 逆序对
- [ ] [LCR 170. 交易逆序对的总数](https://leetcode.com/problems/shu-zu-zhong-de-ni-xu-dui-lcof/)
- [ ] [315. 计算右侧小于当前元素的个数](https://leetcode.com/problems/count-of-smaller-numbers-after-self/)
- [ ] [493. 翻转对](https://leetcode.com/problems/reverse-pairs/)
- [ ] [327. 区间和的个数](https://leetcode.com/problems/count-of-range-sum/)
- [ ] [2426. 满足不等式的数对数目](https://leetcode.com/problems/number-of-pairs-satisfying-inequality/)
- [ ] [3768. 固定长度子数组中的最小逆序对数目](https://leetcode.com/problems/minimum-inversion-count-in-subarrays-of-fixed-length/)
- [ ] [1850. 邻位交换的最小次数](https://leetcode.com/problems/minimum-adjacent-swaps-to-reach-the-kth-smallest-number/)
- [ ] [2193. 得到回文串的最少操作次数](https://leetcode.com/problems/minimum-number-of-moves-to-make-palindrome/)
- [ ] [1885. 统计数对](https://leetcode.com/problems/count-pairs-in-two-arrays/)

### §8.3 线段树（无区间更新）

笔记：
- 思路：把任意查询区间拆成 `O(log n)` 个节点区间，合并节点维护的信息得到答案。
- 单点更新/区间查询通常都是 `O(log n)`。
- [ ] [3479. 水果成篮 III](https://leetcode.com/problems/fruits-into-baskets-iii/) 2178
- [ ] [2940. 找到 Alice 和 Bob 可以相遇的建筑](https://leetcode.com/problems/find-building-where-alice-and-bob-can-meet/) 2327
- [ ] [2286. 以组为单位订音乐会的门票](https://leetcode.com/problems/booking-concert-tickets-in-groups/) 2470
- [ ] [3161. 物块放置查询](https://leetcode.com/problems/block-placement-queries/) 2513
- [ ] [2213. 由单个字符重复的最长子字符串](https://leetcode.com/problems/longest-substring-of-one-repeating-character/) 2629
- [ ] [3777. 使子字符串变交替的最少删除次数](https://leetcode.com/problems/minimum-deletions-to-make-alternating-substring/) 2202
- [ ] [3525. 求出数组的 X 值 II](https://leetcode.com/problems/find-x-value-of-array-ii/) 2645
- [ ] [3165. 不包含相邻元素的子序列的最大和](https://leetcode.com/problems/maximum-sum-of-subsequence-with-non-adjacent-elements/) 2697
- [ ] [3410. 删除所有值为某个元素后的最大子数组和](https://leetcode.com/problems/maximize-subarray-sum-after-removing-all-occurrences-of-one-element/)
- [ ] [3501. 操作后最大活跃区段数 II](https://leetcode.com/problems/maximize-active-section-with-trade-ii/)
- [ ] [LCP 81. 与非的谜题](https://leetcode.com/problems/ryfUiz/)

#### 思维扩展
- [ ] [1157. 子数组中占绝大多数的元素](https://leetcode.com/problems/online-majority-element-in-subarray/)
- [ ] [2407. 最长递增子序列 II](https://leetcode.com/problems/longest-increasing-subsequence-ii/) 2280

### §8.4 Lazy 线段树（有区间更新）

笔记：
- 懒标记核心：更新时先不下传，等后续访问到子节点时再传播，从而保持对数复杂度。
- [ ] [2569. 更新数组后处理求和查询](https://leetcode.com/problems/handling-sum-queries-after-update/) 2398
- [ ] [1622. 奇妙序列](https://leetcode.com/problems/fancy-sequence/)
- [ ] [2502. 设计内存分配器](https://leetcode.com/problems/design-memory-allocator/)
- [ ] [2589. 完成所有任务的最少时间](https://leetcode.com/problems/minimum-time-to-complete-all-tasks/)
- [ ] [2547. 拆分数组的最小代价](https://leetcode.com/problems/minimum-cost-to-split-an-array/)
- [ ] [850. 矩形面积 II](https://leetcode.com/problems/rectangle-area-ii/)
- [ ] [3454. 分割正方形 II](https://leetcode.com/problems/separate-squares-ii/) 2671
- [ ] [3569. 分割数组后不同质数的最大数目](https://leetcode.com/problems/maximize-count-of-distinct-primes-after-split/)
- [ ] [3721. 最长平衡子数组 II](https://leetcode.com/problems/longest-balanced-subarray-ii/) 2724
- [ ] [2916. 子数组不同元素数目的平方和 II](https://leetcode.com/problems/subarrays-distinct-element-sum-of-squares-ii/)
- [ ] [LCP 52. 二叉搜索树染色](https://leetcode.com/problems/QO5KpG/)

### §8.5 动态开点线段树
- [ ] [699. 掉落的方块](https://leetcode.com/problems/falling-squares/)
- [ ] [715. Range 模块](https://leetcode.com/problems/range-module/)
- [ ] [729. 我的日程安排表 I](https://leetcode.com/problems/my-calendar-i/)
- [ ] [731. 我的日程安排表 II](https://leetcode.com/problems/my-calendar-ii/)
- [ ] [732. 我的日程安排表 III](https://leetcode.com/problems/my-calendar-iii/)
- [ ] [2276. 统计区间中的整数数目](https://leetcode.com/problems/count-integers-in-intervals/)
- [ ] [2770. 达到末尾下标所需的最大跳跃次数](https://leetcode.com/problems/maximum-number-of-jumps-to-reach-the-last-index/)
- [ ] [3590. 第 K 小的路径异或和](https://leetcode.com/problems/kth-smallest-path-xor-sum/) 2646

### §8.6 可持久化线段树
- [ ] [3762. 使数组元素相等的最小操作次数](https://leetcode.com/problems/minimum-operations-to-equalize-subarrays/) 2497

### §8.7 ST 表（Sparse Table）

笔记：
- 适合静态 RMQ（区间最值等）：预处理 `O(n log n)`，查询 `O(1)`，不支持修改。
- [ ] [3691. 最大子数组总值 II](https://leetcode.com/problems/maximum-total-subarray-value-ii/) 2469
- [ ] [3501. 操作后最大活跃区段数 II](https://leetcode.com/problems/maximize-active-section-with-trade-ii/)

## 九、伸展树（Splay 树）
- [ ] [2296. 设计一个文本编辑器](https://leetcode.com/problems/design-a-text-editor/) 1912
- [ ] [3526. 范围异或查询与子数组反转](https://leetcode.com/problems/range-xor-queries-with-subarray-reversals/)

## 十、根号算法

### §10.1 根号分解（Sqrt Decomposition）
- [ ] [3655. 区间乘法查询后的异或 II](https://leetcode.com/problems/xor-after-range-multiplication-queries-ii/) 2454
- [ ] [LCP 16. 游乐园的游览计划](https://leetcode.com/problems/you-le-yuan-de-you-lan-ji-hua/)
- [ ] [1714. 数组中特殊等间距元素的和](https://leetcode.com/problems/sum-of-special-evenly-spaced-elements-in-array/)
- [ ] [3400. 右移后的最大匹配索引数](https://leetcode.com/problems/maximum-number-of-matching-indices-after-right-shifts/)

### §10.2 莫队算法
- [ ] [3636. 查询超过阈值频率最高元素](https://leetcode.com/problems/threshold-majority-queries/)
- [ ] [3590. 第 K 小的路径异或和](https://leetcode.com/problems/kth-smallest-path-xor-sum/) 2646

### §10.3 其他
- [ ] [3234. 统计 1 显著的字符串的数量](https://leetcode.com/problems/count-the-number-of-substrings-with-dominant-ones/)

## 专题：离线算法

笔记：
- 通过调整回答查询的顺序（而不是按输入顺序逐个处理），让问题更容易处理。
- [ ] [2343. 裁剪数字后查询第 K 小的数字](https://leetcode.com/problems/query-kth-smallest-trimmed-number/) 1652
- [ ] [3607. 电网维护](https://leetcode.com/problems/power-grid-maintenance/)
- [ ] [2070. 每一个查询的最大美丽值](https://leetcode.com/problems/most-beautiful-item-for-each-query/) 1724
- [ ] [1847. 最近的房间](https://leetcode.com/problems/closest-room/) 2082
- [ ] [2503. 矩阵查询可获得的最大分数](https://leetcode.com/problems/maximum-number-of-points-from-grid-queries/) 2196
- [ ] [1851. 包含每个查询的最小区间](https://leetcode.com/problems/minimum-interval-to-include-each-query/)
- [ ] [1697. 检查边长度限制的路径是否存在](https://leetcode.com/problems/checking-existence-of-edge-length-limited-paths/)
- [ ] [2940. 找到 Alice 和 Bob 可以相遇的建筑](https://leetcode.com/problems/find-building-where-alice-and-bob-can-meet/) 2327
- [ ] [2747. 统计没有收到请求的服务器数目](https://leetcode.com/problems/count-zero-request-servers/)
- [ ] [1938. 查询最大基因差](https://leetcode.com/problems/maximum-genetic-difference-query/)
- [ ] [2736. 最大和查询](https://leetcode.com/problems/maximum-sum-queries/)
- [ ] [3590. 第 K 小的路径异或和](https://leetcode.com/problems/kth-smallest-path-xor-sum/) 2646
- [ ] [3382. 用点构造面积最大的矩形 II](https://leetcode.com/problems/maximum-area-rectangle-with-point-constraints-ii/)

## 编程能力强化训练

笔记：
- 收集“思路大概有，但实现细节多/偏工程”的题目，其中一部分属于模拟实现。

### Part A
- [ ] [12. 整数转罗马数字](https://leetcode.com/problems/integer-to-roman/)
- [ ] [13. 罗马数字转整数](https://leetcode.com/problems/roman-to-integer/)
- [ ] [273. 整数转换英文表示](https://leetcode.com/problems/integer-to-english-words/)
- [ ] [68. 文本左右对齐](https://leetcode.com/problems/text-justification/)
- [ ] [420. 强密码检验器](https://leetcode.com/problems/strong-password-checker/)
- [ ] [8. 字符串转换整数 (atoi)](https://leetcode.com/problems/string-to-integer-atoi/)
- [ ] [65. 有效数字](https://leetcode.com/problems/valid-number/)

### Part B
- [ ] [146. LRU 缓存](https://leetcode.com/problems/lru-cache/)
- [ ] [460. LFU 缓存](https://leetcode.com/problems/lfu-cache/)
- [ ] [432. 全 O(1) 的数据结构](https://leetcode.com/problems/all-oone-data-structure/)
- [ ] [1206. 设计跳表](https://leetcode.com/problems/design-skiplist/)

### Part C
- [ ] [3197. 包含所有 1 的最小矩形面积 II](https://leetcode.com/problems/find-the-minimum-area-to-cover-all-ones-ii/)
- [ ] [2532. 过桥的时间](https://leetcode.com/problems/time-to-cross-a-bridge/) 2589
- [ ] [2056. 棋盘上有效移动组合的数目](https://leetcode.com/problems/number-of-valid-move-combinations-on-chessboard/)
- [ ] [LCP 48. 无限棋局](https://leetcode.com/problems/fsa7oZ/)
- [ ] [LCP 21. 追逐游戏](https://leetcode.com/problems/Za25hA/)
- [ ] [LCP 58. 积木拼接](https://leetcode.com/problems/De4qBB/)
- [ ] [LCP 13. 寻宝](https://leetcode.com/problems/xun-bao/)
- [ ] [LCP 69. Hello LeetCode!](https://leetcode.com/problems/rMeRt2/)
- [ ] [LCP 76. 魔法棋盘](https://leetcode.com/problems/1ybDKD/)
- [ ] [LCP 82. 万灵之树](https://leetcode.com/problems/cnHoX6/)

## 关联题单
- 链表、树与回溯：https://leetcode.com/circle/discuss/K0n2gO/
- 字符串题单：https://leetcode.com/circle/discuss/SJFwQI/

## 算法题单
- 01：https://leetcode.com/circle/discuss/0viNMK/
- 02：https://leetcode.com/circle/discuss/SqopEo/
- 03：https://leetcode.com/circle/discuss/9oZFK9/
- 04：https://leetcode.com/circle/discuss/YiXPXW/
- 05：https://leetcode.com/circle/discuss/dHn9Vk/
- 06：https://leetcode.com/circle/discuss/01LUak/
- 07：https://leetcode.com/circle/discuss/tXLS3i/
- 08：https://leetcode.com/circle/discuss/mOr1u6/
- 09：https://leetcode.com/circle/discuss/IYT3ss/
- 10：https://leetcode.com/circle/discuss/g6KTKL/
- 11：https://leetcode.com/circle/discuss/K0n2gO/
- 12：https://leetcode.com/circle/discuss/SJFwQI/

## 其他链接
- 题解精选：https://github.com/EndlessCheng/codeforces-go/blob/master/leetcode/SOLUTIONS.md
