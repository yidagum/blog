剑指
Offer
53 - I.在排序数组中查找数字
I
统计一个数字在排序数组中出现的次数。



示例
1:

输入: nums = [5, 7, 7, 8, 8, 10], target = 8
输出: 2
示例
2:

输入: nums = [5, 7, 7, 8, 8, 10], target = 6
输出: 0

限制：

0 <= 数组长度 <= 50000

"""
class Solution:
    def search(self, nums: List[int], target: int) -> int:
        count  = 0
        for i in nums:
            if i == target:
                count += 1
        return count

**二分查找右边界，右边界 互减：
class Solution:
    def search(self, nums: [int], target: int) -> int:
        def helper(tar):
            i, j = 0, len(nums) - 1
            while i <= j:
                m = (i + j) // 2
                if nums[m] <= tar: i = m + 1
                else: j = m - 1
            return i
        return helper(target) - helper(target - 1)





"""


