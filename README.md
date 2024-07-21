class Solution {
    public List<Integer> inorderTraversal(TreeNode root) {
        List<Integer> list = new ArrayList<>();
        inorderTraversal(root, list);
        return list;
    }

    void inorderTraversal(TreeNode node, List<Integer> list) {
        if (node == null) {
            return;
        }

        inorderTraversal(node.left, list); // Traverse the left subtree
        list.add(node.val); // Visit the root node
        inorderTraversal(node.right, list); // Traverse the right subtree
    }
}
