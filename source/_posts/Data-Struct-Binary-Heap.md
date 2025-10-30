\---

title: 'Data Struct: Binary Heap'

date: 2025-10-30 15:21:01

tags:

\---

## Binary Heap & Binary Search Tree

```C++
// BST
struct bst{
    bst* left;
    bst* right;
    int value;
    int cnt;
}
void del();
void new_tree();
void query();
void push(int value, bst* tree){
    if(value==tree.value){
        tree->cnt++;
        return;
    }
    if(value>tree.value){
        if(tree->right!=nullptr){
            push(value, tree->right);
        }else{
            tree->right=new_tree(value);
        }
    }else{
        if(tree->left!=nullptr){
            push(value, tree->left);
        }else{
            tree->left=new_tree(value);
        }
    }
}
```

```c++
// BH
vector<int> heap;

```

