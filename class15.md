# class13 Reading Notes:Trees
![Trees](https://www.researchgate.net/profile/Roslan-Hasni-2/publication/327046577/figure/fig2/AS:664838208499712@1535521189790/An-edge-irregular-labeling-of-complete-binary-tree-2-4-T.png)

- Node - A Tree node :
  contain it’s own values, and references to other nodes
- Root - The root is the node at the beginning of the tree.
- K - A maximum number of children
- Left - A :one child
- Right - A :another child.
- Edge :link between parent and child.
- Leaf:Node dosnt have any children
- Height :Number of edges from reeo to furthest leaf

### Traversals:

![Traversals](http://www.cse.unsw.edu.au/~billw/Justsearch1.gif)
- Used for to search for a node, print out the contents of a tree.
- Categories of Traversals:
    * Depth First
    * Breadth First

##### Depth 

- Methods:
   1. Pre-order: root >> left >> right
   2. In-order: left >> root >> right
   3. Post-order: left >> right >> root

#### Breadth First:

* Breadth first traversal iterates through the tree by going through each level of the tree node-by-node.

* Its first traversal uses a queue insted of stack.


#### Binary Tree Vs K-ary Trees:
- Binary Trees restrict the number of children to two.

-  K-ary Trees:Node can have more than two child


#### Big O:
- Time Complixity :O(n)
- Space Complixity :O(w)

- A “perfect” binary tree Where non-leaf have 2 children

- Maximum width for Aperfect binary tree is 2^(h-1) where h is Height of tree


#### Binary Search Trees:
![Binary Search Trees](https://miro.medium.com/max/1194/1*ziYvZzrttFYMXkkV9u66jw.png)

- Its an Organized Tree that have values similar to it on Left else on the Right.

Complixity: O(n)
