class Solution:
    def maxIceCream(self, costs: List[int], coins: int) -> int:
        cn=0
        for i in sorted(costs):
            if i<=coins:
                cn+=1
                coins-=i
        return cn
