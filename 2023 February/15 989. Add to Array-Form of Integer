class Solution:
    def addToArrayForm(self, num: List[int], k: int) -> List[int]:
        ans = []
        n = len(num)
        carry = 0
        i = n - 1
        while k > 0 or i >= 0 or carry > 0:
            sum = carry
            if k > 0:
                remainder = k % 10
                sum += remainder
                k //= 10
            if i >= 0:
                sum += num[i]
                i -= 1
            carry = sum // 10
            ans.insert(0, sum % 10)
        return ans
