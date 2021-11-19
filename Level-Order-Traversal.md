# Level-Order-Traversal

```
import java.util.ArrayDeque;
import java.util.Queue;


class TreeNode{
    TreeNode left, right;
    int data;
    public TreeNode(int data){
        this.data = data;
    }
}



public class BinaryTree {
    
    public static void levelOrder(TreeNode node){
        
        if(node == null)
            return;
        
        Queue<TreeNode> q = new ArrayDeque<>();
        q.add(node);
        
        while(q.size() > 0){
            int count = q.size();
            for(int i=0; i < count; i++){
                node = q.remove();
                System.out.print(node.data+" ");
                
                if(node.left != null)
                    q.add(node.left);
                if(node.right != null)
                    q.add(node.right);
                
            }
            System.out.println();
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
