# Definition for a binary tree node.
# class TreeNode:
#     def __init__(self, val=0, left=None, right=None):
#         self.val = val
#         self.left = left
#         self.right = right
class Solution:
    def isSymmetric(self, root: TreeNode | None) -> bool:
        def are_mirrors(root1: TreeNode | None, root2: TreeNode | None) -> bool:
            return (
                root1.val == root2.val and 
                are_mirrors(root1.left, root2.right) and
                are_mirrors(root1.right, root2.left)
            ) if root1 and root2 else root1 == root2 == None
        
        return root and are_mirrors(root.left, root.right)
