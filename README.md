# OGUN-3MTT-COMMUNITY-CHALLENGE
# DAY 1
# TASK IS LEETCODE TWO SUM at https://leetcode.com/problems/two-sum/description/

# SOLUTION IS 





class Solution(object):
    def twoSum(self, nums, target):
        d = {}
        
        # First, add all numbers and their indices to the dictionary
        for i in range(0, len(nums)):
            d[nums[i]] = i

        # Then, iterate over the list again to find the complement
        for i in range(0, len(nums)):
            x = target - nums[i]
            
            # Check if complement exists and that it's not the same index
            if x in d and i != d[x]:
                return [i, d[x]]
        
        return None  # Return None if no pair is found


