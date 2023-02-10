class Solution:
    def maxDistance(self, grid: List[List[int]]) -> int:
        n = len(grid)
        q = collections.deque()
        for i in range(n):
            for j in range(n):
                if grid[i][j] == 1: q.append((i, j))
        if not q or len(q) == n * n: return -1
        res = -1
        dirs = [(0, 1), (0, -1), (1, 0), (-1, 0)]
        while q:
            size = len(q)
            res += 1
            while size:
                size -= 1
                x, y = q.popleft()
                for dx, dy in dirs:
                    i, j = x + dx, y + dy
                    if 0 <= i < n and 0 <= j < n and grid[i][j] == 0:
                        grid[i][j] = 1
                        q.append((i, j))
        return res
