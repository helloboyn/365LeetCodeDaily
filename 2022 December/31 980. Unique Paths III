class Solution {
public:
    int dx[4]={-1,0,1,0};
    int dy[4]={0,1,0,-1};
   int f(int i,int j,vector<vector<int>> &grid,int &c,int cnt)
   {
       if(i<0 or j<0 or i>=grid.size() or j>=grid[0].size() or grid[i][j]==-1)
           return 0;
       if(grid[i][j]==2)
       {
           cnt-=1;//-1 since we have also included start cell
           return (cnt==c)?1:0;//if all empty cells visited then returning 1 else 0
       }
       grid[i][j]=-1;
       int sum=0;
       sum=f(i+1,j,grid,c,cnt+1)+f(i,j+1,grid,c,cnt+1)+f(i-1,j,grid,c,cnt+1)+f(i,j-1,grid,c,cnt+1);
       grid[i][j]=0;
       return sum;
   }
    int uniquePathsIII(vector<vector<int>>& grid) {
        int m=grid.size();
        int n=grid[0].size();
        vector<pair<int,int>> s;
        int c=0;//for counting no of empty cells
        for(int i=0;i<m;i++)
        {
            for(int j=0;j<n;j++)
            {
                if(grid[i][j]==1)
                    s.push_back({i,j});//for storing starting indexes
                if(grid[i][j]==0)
                    c++;
            }
        }
       return f(s[0].first,s[0].second,grid,c,0); 
    }
};
