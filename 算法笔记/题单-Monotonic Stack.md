---
title: 单调栈题单
aliases: [单调栈（矩形面积/贡献法/最小字典序）, 灵神单调栈题单]
tags:
  - leetcode
  - monotonic-stack
  - algorithm
  - study-plan
source: 灵茶山艾府 题单
author: 灵茶山艾府 (Endlesscheng)
original: https://leetcode.cn/circle/discuss/9oZFK9
last_update: 2025-08-05 01:28:01
---

# 单调栈（矩形面积/贡献法/最小字典序）

来源：https://leetcode.cn/circle/discuss/9oZFK9
更新：2025-08-05 01:28:01

> 说明：本文件是本地刷题依据版，保留章节层级、可勾选题目、原题链接和难度分；大段题解讲解以原题单为准。

> > 他向远方望去，无法看到高山背后的矮山，只看到一座座更高的山峰。
> 推荐先做做 [数据结构题单](/lc-rating/v0/list/data_structure) 中的「枚举右，维护左」以及第三章「栈」的基础题目后，再来刷本题单。

## 一、单调栈

### right[i] 是 nums[i] 右侧最近的严格大于 nums[i] 的数的下标，若不存在则为 n

> 原理讲解：[单调栈【基础算法精讲 26】](https://www.bilibili.com/video/BV1VN411J7S7/)
> 模板：

- [ ] [739. 每日温度](https://leetcode.cn/problems/daily-temperatures/)
- [ ] [1475. 商品折扣后的最终价格](https://leetcode.cn/problems/final-prices-with-a-special-discount-in-a-shop/) 1212
- [ ] [496. 下一个更大元素 I](https://leetcode.cn/problems/next-greater-element-i/)
- [ ] [503. 下一个更大元素 II](https://leetcode.cn/problems/next-greater-element-ii/)
- [ ] [901. 股票价格跨度](https://leetcode.cn/problems/online-stock-span/) 1709
- [ ] [853. 车队](https://leetcode.cn/problems/car-fleet/) 1678

### §1.2 进阶（选做）

> **思维扩展**：

- [ ] [1019. 链表中的下一个更大节点](https://leetcode.cn/problems/next-greater-node-in-linked-list/) 1571
- [ ] [768. 最多能完成排序的块 II](https://leetcode.cn/problems/max-chunks-to-make-sorted-ii/) 1788
- [ ] [654. 最大二叉树](https://leetcode.cn/problems/maximum-binary-tree/)
- [ ] [456. 132 模式](https://leetcode.cn/problems/132-pattern/)
- [ ] [3113. 边界元素是最大值的子数组数目](https://leetcode.cn/problems/find-the-number-of-subarrays-where-boundary-elements-are-maximum/) 2046
- [ ] [2866. 美丽塔 II](https://leetcode.cn/problems/beautiful-towers-ii/) 2072
- [ ] [1944. 队列中可以看到的人数](https://leetcode.cn/problems/number-of-visible-people-in-a-queue/) 2105
- [ ] [2454. 下一个更大元素 IV](https://leetcode.cn/problems/next-greater-element-iv/) 2175
- [ ] [1130. 叶值的最小代价生成树](https://leetcode.cn/problems/minimum-cost-tree-from-leaf-values/) 1919
- [ ] [2289. 使数组按非递减顺序排列](https://leetcode.cn/problems/steps-to-make-array-non-decreasing/) 2482
- [ ] [1776. 车队 II](https://leetcode.cn/problems/car-fleet-ii/) 2531
- [ ] [2736. 最大和查询](https://leetcode.cn/problems/maximum-sum-queries/) 2533
- [ ] [3420. 统计 K 次操作以内得到非递减子数组的数目](https://leetcode.cn/problems/count-non-decreasing-subarrays-after-k-operations/) 2855
- [ ] [3221. 最大数组跳跃得分 II](https://leetcode.cn/problems/maximum-array-hopping-score-ii/)（会员题）
- [ ] [1966. 未排序数组中的可被二分搜索的数](https://leetcode.cn/problems/binary-searchable-numbers-in-an-unsorted-array/)（会员题）
- [ ] [2832. 每个元素为最大值的最大范围](https://leetcode.cn/problems/maximal-range-that-each-element-is-maximum-in-it/)（会员题）
- [ ] [2282. 在一个网格中可以看到的人数](https://leetcode.cn/problems/number-of-people-that-can-be-seen-in-a-grid/)（会员题）
- [ ] [3555. 排序每个滑动窗口中最小的子数组](https://leetcode.cn/problems/smallest-subarray-to-sort-in-every-sliding-window/)（会员题）
- [ ] [962. 最大宽度坡](https://leetcode.cn/problems/maximum-width-ramp/) 1608
- [ ] [3542. 将所有元素变为 0 的最少操作次数](https://leetcode.cn/problems/minimum-operations-to-convert-all-elements-to-zero/) 1890
- [x] [1124. 表现良好的最长时间段](https://leetcode.cn/problems/longest-well-performing-interval/) 1908

## 二、矩形

- [ ] [84. 柱状图中最大的矩形](https://leetcode.cn/problems/largest-rectangle-in-histogram/)
- [ ] [1793. 好子数组的最大分数](https://leetcode.cn/problems/maximum-score-of-a-good-subarray/) 1946
- [ ] [85. 最大矩形](https://leetcode.cn/problems/maximal-rectangle/)
- [ ] [221. 最大正方形](https://leetcode.cn/problems/maximal-square/)
- [ ] [42. 接雨水](https://leetcode.cn/problems/trapping-rain-water/)
- [ ] [1504. 统计全 1 子矩形](https://leetcode.cn/problems/count-submatrices-with-all-ones/) 1845
- [ ] [1277. 统计全为 1 的正方形子矩阵](https://leetcode.cn/problems/count-square-submatrices-with-all-ones/) 1613
- [ ] [755. 倒水](https://leetcode.cn/problems/pour-water/) 1832（会员题）

## 三、贡献法

> **思维扩展**：

- [ ] [907. 子数组的最小值之和](https://leetcode.cn/problems/sum-of-subarray-minimums/) 1976
- [ ] [2104. 子数组范围和（最大值-最小值）](https://leetcode.cn/problems/sum-of-subarray-ranges/) 1504
- [ ] [1856. 子数组最小乘积的最大值](https://leetcode.cn/problems/maximum-subarray-min-product/) 2051
- [ ] [2818. 操作使得分最大](https://leetcode.cn/problems/apply-operations-to-maximize-score/) 2397
- [ ] [2281. 巫师的总力量和（最小值×和）](https://leetcode.cn/problems/sum-of-total-strength-of-wizards/) 2621
- [ ] [3430. 最多 K 个元素的子数组的最值之和](https://leetcode.cn/problems/maximum-and-minimum-sums-of-at-most-size-k-subarrays/) 2645
- [ ] [3359. 查找最大元素不超过 K 的有序子矩阵](https://leetcode.cn/problems/find-sorted-submatrices-with-maximum-element-at-most-k/)（会员题）
- [ ] [2334. 元素值大于变化阈值的子数组](https://leetcode.cn/problems/subarray-with-elements-greater-than-varying-threshold/) 2381
- [ ] [2962. 统计最大元素出现至少 K 次的子数组·我的题解](https://leetcode.cn/problems/count-subarrays-where-max-element-appears-at-least-k-times/solutions/2560940/hua-dong-chuang-kou-fu-ti-dan-pythonjava-xvwg/) 1701

## 四、最小字典序

- [ ] [402. 移掉 K 位数字](https://leetcode.cn/problems/remove-k-digits/)
- [ ] [1673. 找出最具竞争力的子序列](https://leetcode.cn/problems/find-the-most-competitive-subsequence/) 1802
- [ ] [316. 去除重复字母](https://leetcode.cn/problems/remove-duplicate-letters/)
- [ ] [316 扩展：重复个数不超过 limit](https://leetcode.cn/contest/tianchi2022/problems/ev2bru/)
- [ ] [1081. 不同字符的最小子序列](https://leetcode.cn/problems/smallest-subsequence-of-distinct-characters/) 2185
- [ ] [321. 拼接最大数](https://leetcode.cn/problems/create-maximum-number/)
- [ ] [2030. 含特定字母的最小子序列](https://leetcode.cn/problems/smallest-k-length-subsequence-with-occurrences-of-a-letter/) 2562

## 算法题单
