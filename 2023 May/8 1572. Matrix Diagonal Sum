class Solution:
    def diagonalSum(self, mat: List[List[int]]) -> int:
        su=0
        n = len(mat)
        for i in range(n):
            su+=mat[i][i]
            su+=mat[i][n-1-i]
        if n%2==1:
            su-=mat[n//2][n//2]
        return su
