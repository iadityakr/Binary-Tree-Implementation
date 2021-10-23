# Pre OrderTraversal-BinaryTree

# Recursive-Code

```
public static void preOrderRecursive(TreeNode root){
        // base condition
        if(root == null) return;
        
        System.out.println(root.data);
        preOrderRecursive(root.left);
        preOrderRecursive(root.right);
    }
 ```
 
 # Iterative-Code
 
 ```
 public static void preOrderIterative(TreeNode root){
        if(root == null) return;
        
        Stack<TreeNode> s = new Stack<>();
        s.push(root);
        while(s.empty() == false){
            TreeNode curr = s.pop();
            System.out.println(curr.data);
            if(curr.right != null)
                s.push(curr.right);
            if(curr.left != null)
                s.push(curr.left);
        }
        
    }
 ```
 
 # Whole code
 
 ```
 import java.util.Stack;

class TreeNode{
    TreeNode left, right;
    int data;
    public TreeNode(int data){
        this.data = data;
    }
}



public class BinaryTree {
    
    public static void preOrderRecursive(TreeNode root){
        // base condition
        if(root == null) return;
        
        System.out.println(root.data);
        preOrderRecursive(root.left);
        preOrderRecursive(root.right);
    }
    
    public static void preOrderIterative(TreeNode root){
        if(root == null) return;
        
        Stack<TreeNode> s = new Stack<>();
        s.push(root);
        while(s.empty() == false){
            TreeNode curr = s.pop();
            System.out.println(curr.data);
            if(curr.right != null)
                s.push(curr.right);
            if(curr.left != null)
                s.push(curr.left);
        }
        
    }
    
    public static void main(String[] args) {
        TreeNode root = new TreeNode(10);
        root.left = new TreeNode(20);
        root.right = new TreeNode(30);
        root.right.left = new TreeNode(40);
        root.right.right = new TreeNode(50);
//        preOrderRecursive(root);
        preOrderIterative(root);
    }
}
 ```
