https://leetcode.com/problems/rotate-array/


class Solution:
    def rotate(self, nums: List[int], k: int) -> None:
        """
        Do not return anything, modify nums in-place instead.
        """
        k=k%len(nums)
        def swap(l,r):
            while l<r:
                nums[l],nums[r] = nums[r],nums[l]
                l += 1
                r -= 1
        
        swap(0,len(nums)-1)
        swap(0,k-1)
        swap(k,len(nums)-1)