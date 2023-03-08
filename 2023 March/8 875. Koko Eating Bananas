class Solution:
    def minEatingSpeed(self, piles: List[int], h: int) -> int:
        # Define the search space
        left = 1
        right = max(piles)

        # Define a function to check if it's possible to eat all bananas in h hours
        def can_eat_all_bananas(speed):
            time = 0
            for pile in piles:
                time += (pile + speed - 1) // speed
            return time <= h

        # Binary search for the minimum speed
        while left < right:
            mid = (left + right) // 2
            if can_eat_all_bananas(mid):
                right = mid
            else:
                left = mid + 1

        return left
