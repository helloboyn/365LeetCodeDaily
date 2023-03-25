class Solution:
    def countPairs(self, n: int, edges: List[List[int]]) -> int:
        def dfs(node):
            if visited[node]:
                return 0
            visited[node] = True
            res = 1
            for nbr in graph[node]:
                res += dfs(nbr)
            return res
        graph = {}
        for i in range(n):
            graph[i] = []
        for edge in edges:
            graph[edge[0]].append(edge[1])
            graph[edge[1]].append(edge[0])
            
        visited = [False for _ in range(n)]
        components = []
        for node in range(n):
            if visited[node] == False:
                components.append(dfs(node))   
        
        ans = n * (n - 1) // 2
        for k in components:
            ans -= k * (k - 1) // 2
        
        return ans
