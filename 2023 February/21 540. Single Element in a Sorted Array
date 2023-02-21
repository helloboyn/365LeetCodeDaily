class Solution:
    def singleNonDuplicate(self, nums: List[int]) -> int:
        l, r = 0, len(nums) // 2
        ans = -1
        while l <= r:
            mid = (l + r) // 2
            idx = mid * 2
            if idx + 1 >= len(nums) or nums[idx] != nums[idx + 1]:
                r = mid - 1
                ans = nums[idx]
            else:
                l = mid + 1
        return ans
