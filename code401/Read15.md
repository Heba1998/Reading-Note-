# Trees

![img](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-15/resources/images/BinaryTree1.PNG)

*A tree is a non linier data structure that is like a list but that uses nodes starting at a root then then point to more than one "next" node.*


* ***Common Terminology***


    * `Node` - A Tree node is a component which may contain it’s own values, and references to other nodes
    * `Root` - The root is the node at the beginning of the tree
    * `K` - A number that specifies the maximum number of children any node may have in a k-ary tree. In a binary tree, k = 2.
    * `Left` - A reference to one child node, in a binary tree
    * `Right` - A reference to the other child node, in a binary tree
    * `Edge` - The edge in a tree is the link between a parent and child node
    * `Leaf` - A leaf is a node that does not have any children
    * `Height` - The height of a tree is the number of edges from the root to the furthest leaf


* ***Traversals***

*Traversing a tree allows us to search for a node, print out the contents of a tree, and much more.*
* There are two categories of traversals when it comes to trees:
    *  Depth First

         Depth first traversal is where we prioritize going through the depth (height) of the tree first. the Three methods for depth first traversal:
        * Pre-order: root >> left >> right
        * In-order: left >> root >> right
        * Post-order: left >> right >> root

   
    * Breadth First

        Breadth first traversal iterates through the tree by going through each level of the tree node-by-node.

        ```java

        ALGORITHM breadthFirs(root)
        // INPUT  <-- root node
        // OUTPUT <-- front node of queue to console

        Queue breadth <-- new Queue()
             breadth.enqueue(root)

        while breadth.peek()
         node front = breadth.dequeue()
         OUTPUT <-- front.value

            if front.left is not NULL
      breadth.enqueue(front.left)

        if front.right is not NULL
      breadth.enqueue(front.right)

        ```



* ***Binary Tree Vs K-ary Trees***

*Trees can have any number of children per node, but Binary Trees restrict the number of children to two (hence our left and right children).*

*`K-ary` Trees If Nodes are able have more than 2 child nodes, we call the tree that contains them a K-ary Tree. In this type of tree we use K to refer to the maximum number of children that each Node is able to have.*


* ***Adding a node***

*It does not matter where to add new node in tree.*

*It will go down to the children and start adding from left to right.*

*If I want to add the new node to a specific place, I have to get the parent first, then add the new value.*


* ***Big O***

*The Big O time complexity for inserting a new node is O(n). Searching for a specific node will also be O(n). Because of the lack of organizational structure in a Binary Tree, the worst case for most operations will involve traversing the entire tree. If we assume that a tree has n nodes, then in the worst case we will have to look at n items, hence the O(n) complexity.*

*The Big O space complexity for a node insertion using breadth first insertion will be O(w), where w is the largest width of the tree.*

*A “perfect” binary tree is one where every non-leaf node has exactly two children. The maximum width for a perfect binary tree, is 2^(h-1), where h is the height of the tree. Height can be calculated as log n, where n is the number of nodes.*