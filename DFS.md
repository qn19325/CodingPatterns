## Depth First Search

### Recursion Example
Task - Invert a binary tree \
  Input - root = [4,2,7,1,3,6,9] \
  Output - root = [4,7,3,9,6,3,1]
 ```
 class TreeNode:
     def __init__(self, val=0, left=None, right=None):
      self.val = val
      self.left = left
      self.right = right
class Solution:
    def invertTree(self, root: Optional[TreeNode]) -> Optional[TreeNode]:
      if not root:
        return None
        
      temp = root.left
      root.left = root.right
      root.right = temp
      
      self.invertTree(root.left)
      self.invertTree(root.right)
      
      return root
```
      
