class Solution:
    def invertTree(self, root: Optional[TreeNode]) -> Optional[TreeNode]:
        return TreeNode(root.val, self.invertTree(root.right), self.invertTree(root.left)) if root else None
