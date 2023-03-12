class Solution:
    def mergeKLists(self, lists: List[Optional[ListNode]]) -> Optional[ListNode]:
        v=[]
        for i in lists:
            x=i
            while x:
                v+=[x.val]
                x=x.next
        v=sorted(v,reverse=True)
        ans=None
        for i in v:
            ans=ListNode(i,ans)
        return ans
