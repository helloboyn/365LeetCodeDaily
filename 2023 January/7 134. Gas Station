class Solution:
    def canCompleteCircuit(self, gas: List[int], cost: List[int]) -> int:
        rem=0
        st=0
        t_gas=0
        for p in range(len(gas)):
            dif=gas[p]-cost[p]
            t_gas+=dif
            rem+=dif
            if rem<0:
                st=p+1
                rem=0
        else: return st if abs(t_gas)==t_gas else -1
