class Solution:
    def minDeletionSize(self, strs: List[str]) -> int:
        return sum(col != sorted(col) for col in map(list, zip(*strs)))
