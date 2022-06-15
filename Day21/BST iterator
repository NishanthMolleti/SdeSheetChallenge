#include<bits/stdc++.h>
class BSTiterator
{
    public:
      stack<TreeNode<int>*> order;
    BSTiterator(TreeNode<int>*root)
    {
        // write your code here
        inorder(root);
    }
    
    void inorder(TreeNode<int>* root){
    while(root != NULL){
        order.push(root);
        root = root->left;
    }    
    }

    int next()
    {
        // write your code here
         TreeNode<int>* topi = order.top();
        order.pop();
        inorder(topi->right);
        return topi->data;
    }

    bool hasNext()
    {
        // write your code here
         return !order.empty();
    }
};
