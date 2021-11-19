# Post-Order-Traversal

```
import java.util.ArrayDeque;
import java.util.Queue;
import java.util.Stack;

class TreeNode{
    TreeNode left, right;
    int data;
    public TreeNode(int data){
        this.data = data;
    }
}



public class BinaryTree {
    public static void postOrder(TreeNode node) {
        
        if(node == null)
            return;
        Stack<TreeNode> nodeStack = new Stack<>();
        TreeNode curr = node;
        TreeNode prev = null;
        while(curr != null || nodeStack.size() > 0)
        {
            if(curr != null)
            {
                nodeStack.push(curr);
                curr = curr.left;
            }
            else{
                curr = nodeStack.peek();
                if(curr.right == null || curr.right == prev){
                    nodeStack.pop();
                    System.out.println(curr.data);
                    
                    prev = curr;
                    curr = null;
                }
                else{
                    curr = curr.right;
                }
            }
        }
        
    }
    
    public static void main(String[] args) {
        TreeNode root = new TreeNode(10);
        root.left = new TreeNode(23);
        root.right = new TreeNode(15);
        root.right.left = new TreeNode(17);
        root.right.right = new TreeNode(18);
        levelOrder(root);
    }
}

```
