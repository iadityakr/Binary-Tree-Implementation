# Binary-Tree-Implementation

Today's Code
=======================================================

class TreeNode{
    TreeNode left, right;
    int data;
    public TreeNode(int data){
        this.data = data;
    }
}

public class BinaryTree {
    public static void main(String[] args) {
        TreeNode root = new TreeNode(10);
        root.left = new TreeNode(20);
        root.right = new TreeNode(30);
    }
}
