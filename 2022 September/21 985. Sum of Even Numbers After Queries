class Solution {
public:
    vector<int> sumEvenAfterQueries(vector<int>& nums, vector<vector<int>>& queries) {
        int n=nums.size();
        vector<int >ans;
        int sum=0;
        for(auto x:nums){
            if(x%2==0)sum+=x;
        }
        for(auto x:queries){
            int val=x[0];
            int idx=x[1];
            if(nums[idx]%2==0)sum-=nums[idx];
            nums[idx]+=val;
            if(nums[idx]%2==0)sum+=nums[idx];
            ans.push_back(sum);
        }
        return ans;
    }
};
