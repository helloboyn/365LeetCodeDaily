class Solution:
    def helper(self, piles, dp, suffixSum, i, M):
        if i == len(piles):
            return 0
        if i + 2 * M >= len(piles):
            return suffixSum[i]

        if dp[i][M] != 0:
            return dp[i][M]

        result = 0
        for x in range(1, 2 * M + 1):
            result = max(result, suffixSum[i] - self.helper(piles, dp, suffixSum, i + x, max(M, x)))

        dp[i][M] = result
        return result

    def stoneGameII(self, piles):
        if not piles:
            return 0
        dp = [[0] * len(piles) for _ in range(len(piles))]

        suffixSum = [0] * len(piles)
        suffixSum[-1] = piles[-1]
        for i in range(len(piles) - 2, -1, -1):
            suffixSum[i] = piles[i] + suffixSum[i + 1]

        return self.helper(piles, dp, suffixSum, 0, 1)
