# Leetcode

class Solution(object):
    def twoSum(self, nums, target):
        """
        :type nums: List[int]
        :type target: int
        :rtype: List[int]
        """
        d = {}
        n = len(nums)
        
        i = 0
        for number in nums:
            d[number] = i
            i = i+1
            
        for j in range(n):
            rest = target - nums[j]
            if rest in d :
                key = d.get(rest)
                if key != j:
                    break
        
        return [j, key]
