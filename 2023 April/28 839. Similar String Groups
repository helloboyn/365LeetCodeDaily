class Solution:
    def numSimilarGroups(self, strs: List[str]) -> int:
        groups = 0
        n = len(strs)
        vis = [False] * n
        for i in range(n):
            if vis[i]: continue
            groups += 1
            self.dfs(i, strs, vis)
        return groups

    def dfs(self, i: int, strs: List[str], vis: List[bool]) -> None:
        vis[i] = True
        for j in range(len(strs)):
            if vis[j]: continue
            if self.is_similar(strs[i], strs[j]):
                self.dfs(j, strs, vis)

    def is_similar(self, a: str, b: str) -> bool:
        count = 0
        for i in range(len(a)):
            if a[i] != b[i]: count += 1
        return count == 2 or count == 0
