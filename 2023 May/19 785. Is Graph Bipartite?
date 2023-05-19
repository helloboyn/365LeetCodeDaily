from typing import List
from collections import deque

class Solution:
    def isBipartite(self, gr: List[List[int]]) -> bool:
        n = len(gr)
        colour = [0] * n

        for node in range(n):
            if colour[node] != 0:
                continue

            q = deque()
            q.append(node)
            colour[node] = 1

            while q:
                cur = q.popleft()

                for ne in gr[cur]:
                    if colour[ne] == 0:
                        colour[ne] = -colour[cur]
                        q.append(ne)
                    elif colour[ne] != -colour[cur]:
                        return False

        return True
