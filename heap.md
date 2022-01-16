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
Apples are arranged in the Market one top of other which

Time complexity for Insertion and Deletion is from O(1) to O(log n) and the Height of the Tree is 2^(h+1). For creating the Heap time complexity is O(n logn)

**Max-Heap:** In a Max-Heap the key present at the root node must be greatest among the keys present at all of it’s children. The same property must be recursively true for all sub-trees in that Binary Tree.

- Heap is a complete Binary tree satisfying the conditions that
  1. Every node is having the element **Greater than or equal to** all its descendants(child nodes)
  2. Duplicates are Allowed, so we can have them in descendants
  3. There is no preference to arrang the left and right nodes like leftNode > rightNode or leftNode < rightNode it can be in any order
  ### Insert element into Heap
  1. We should always insert the element at end of the Binary tree
  2. Adjust the element by comparing with parent node and push to the top in heirarchy until the parent node is **Greater than or equal** to the element
  3. At the end of insertion Heap should always be complete binary tree
  ### Delete element from Heap
  1. **Only root element can/should/must and only be deleted**. There is no other choice to delete any other elemen except root element
  2. Once you delete the root element, replace the root element with the last element in Binary tree
  3. Then Adjust the root element by comparing with descendents
  4. First compare Left and right children of root element and get the greater element value 
  5. Now, compare the greater element with the root element, if root element is greater, then we will be good
  6. If not, we should swap the great element with the root element
  7. Do this comparison, down the line in heirarchy with its descendants until we place the element in right position 
  ### Heap Sort
  1. If we maintain the deleted element within the same at the end of array like wise for all the elements we endup getting the sorted Array
  ### Create Heap
  1. With the given Array, start inserting the element into heap one by one By comparing the parent node at each time down the line in heierarchy
  2. Time complexity is O(nlogn)
  ## Create the Heap using Heapify method
  1. Time complexity is O(n)
  2. Heapify is the process of adjusting the descendents of a node by keeping the parent node is always greater than or equal to parent node from leaft node to root node
  3. In a given array of elements, will start looking at the end of element
  4. At the last level, does not have the descendents hence we can simply skip
  5. Just Before the last level, will start looking at the end of element and compare the child nodes and bring the greater element to top
  6. Likewise adjust all the elements from bottom to top until all the elements are right in order
  ## Priority Queue: 
  This is not FIFO(First in first out), But the elements will have priority and they are inserted and deleted based on the priority.
  1. Heap is best data structure to Implement the Priority Queue
  2. We can insert and delete the elements with O(log n) time completxity 
  3. If we have small number Higher Priority then Create Min Heap
  4. If we have larger number Higher Priority then Create Max Heap

- **Min-Heap:** In a Min-Heap the key present at the root node must be minimum among the keys present at all of it’s children. The same property must be recursively true for all sub-trees in that Binary Tree.

  All the opearions will be same but the proirity will be Minimum numnber [For Image](https://www.geeksforgeeks.org/heap-data-structure/)

