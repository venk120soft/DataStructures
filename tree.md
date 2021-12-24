If you feel new to subject Just go throw [video first](https://www.tutorialspoint.com/data_structures_algorithms/tree_data_structure.htm) if you already familiar just have a look at below notes

# Tree
Tree represents the nodes connected by edges. We can connect the nodes in many ways. 
If we form the tree, based on following some certain rules we endup creatng different type of data structures like Binary search tree, Max Heap, Min Heap, AVL tree, spanning tree

Binary tree has Parent Node, Left Child, Right Child

![Binary Tree](./images/binary_tree.jpg)

### Important Terms

Following are the important terms with respect to tree.

Path − Path refers to the sequence of nodes along the edges of a tree.

Root − The node at the top of the tree is called root. There is only one root per tree and one path from the root node to any node.

Parent − Any node except the root node has one edge upward to a node called parent.

Child − The node below a given node connected by its edge downward is called its child node.

Leaf − The node which does not have any child node is called the leaf node.

Subtree − Subtree represents the descendants of a node.

Visiting − Visiting refers to checking the value of a node when control is on the node.

Traversing − Traversing means passing through nodes in a specific order.

Levels − Level of a node represents the generation of a node. If the root node is at level 0, then its next child node is at level 1, its grandchild is at level 2, and so on.

keys − Key represents a value of a node based on which a search operation is to be carried out for a node.

### Full Binary Tree vs Complete Binary Tree
From the above image we can say that it is full binary tree with the height of 3 (level o, 1, 2) and complete binary tree with the height of 4 (level 0, 1, 2, 3)

All Binary search trees are complete binary trees

## Binary search Tree
- The left subtree of a node contains only nodes with keys lesser than the node’s key.
- The right subtree of a node contains only nodes with keys greater than the node’s key.
- The left and right subtree each must also be a binary search tree.
- There must be no duplicate nodes.
