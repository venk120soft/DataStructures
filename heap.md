# Heap 
[for Better video explanation](https://www.youtube.com/watch?v=HqPJF2L5h9U)

Heap is a data structure of type Trees. [Learn more about trees](./tree.md)

Array representation of Bindary tree will be done by using below Formulas, so that we can easily find any element in the heap  and If the leaf is empty Array should leave that as empty space

Ex: 

| Operation                    | Formula           | Example           |
| -----------------------------|:-----------------:| -----------------:|
| If a Node is at Index        | i                 | 5                 |
| If a left child is at Index  | 2 * i             | 2 * 5 = 10        |
| If a right child is at Index | 2 * i + 1         | 2 * 5 +1 = 10+1   |
| If a parent is at Index      | (mod of i/2)      |  mod of 2.5 = 2   |

## Consider below to Implement Max Heap
Time complexity for Insertion is from O(1) to O(log n) and the Height of the Tree is 2^(h+1)
- **Max-Heap:** In a Max-Heap the key present at the root node must be greatest among the keys present at all of it’s children. The same property must be recursively true for all sub-trees in that Binary Tree.
- Heap is a complete Binary tree satisfying the conditions that
  1. Every node is having the element greater than or equal to all its descendants(child nodes)
  2. Duplicates are Allowed, so we can have them in descendants
  3. There is no preference to arrang the left and right nodes like leftNode > rightNode or leftNode < rightNode it can be in any order
  4. We should always insert the element at end of the Binary tree
  5. Adjust the element by comparing with parent node and push to the top in heirarchy until the parent node is **greater than or equal** to the element
  
- **Min-Heap:** In a Min-Heap the key present at the root node must be minimum among the keys present at all of it’s children. The same property must be recursively true for all sub-trees in that Binary Tree.
  1. Every node is having the element **Less than or equal to** all descendants(child nodes)
  2. Duplicates are Allowed, so we can have them in descendants
  3. There is no preference to arrang the left and right nodes like leftNode > rightNode or leftNode < rightNode it can be in any order
  4. We should always insert the element at end of the Binary tree
  5. Adjust the element by comparing with parent node and push to the top in heirarchy until the parent node is **Less than or equal** to the element
https://www.geeksforgeeks.org/heap-data-structure/
 
- Heap should always be complete binary tree
- Parent node should always be greater than left node and greater than equal to the right node
- Left node should always be less than to the right node
- Insertion of new node should always start with adding end of the binary tree
- 
- Deletion of 
