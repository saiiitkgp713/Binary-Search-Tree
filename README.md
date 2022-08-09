# Binary-Search-Tree
Python Implementation for Binary Search Tree.

Binary Search Tree is a Tree like data structure which consists of collection of objects linked to each other. All the values to the left of an object are less than the current value of the object and values right to it are greater. Its expression is similar to heaps(which is an array), but is completely different. A heap is a complete binary Tree where values in the lower level are filled from left to right without any none values between them which is not the case with BST where values are filled w.r.t their importance.

Total impementation consists of a class 'Tree' with 11 methods inside it.
_init_ method is used to create an object of the tree which have properties like 'value', 'left' & 'right'
where left and right separately point to two different objects of Tree which are considered to be child of the orginal object(which is considerd as parent).

'isempty' is the method which checks whether the value of an object is None or not.
'isleaf' is the method which checks whether an object is leaf or or not.
An object is considered to be leaf, if its both left and right pointers points to empty objects

'makeempty' is used to remove the value of the object(it has to be leaf) and make it None. This method is generally used when we are deleting a value from the Tree.
'copyright' is used when a deleting value is not of an object which is leaf. The value of the object is removed and value of its rightchild(provided the left child is empty) is copied to it and consequently its grandchildren(children of its right child) are promoted as its own children.

'find' is a method which search for a value in the entire tree and returns boolean value depending upon the situation. if value is in the Tree, it returns True or it will return false. 
'insert' is mehtod which inserts a value into the already existing tree.
'maxval' and 'minval' are methods which are used to find the max value and min values in a given tree.

'delete' is used to delete a value from the Tree which uses the methods like 'makeempty' and 'copyright' to achieve it.
'inorder' is a method which return a sorted list of all the values in the Tree in Ascending order.

In general the operations like insert, delete, finding max value or min value etc., in BST have a time complexity of O(logn) which is far better when compared to the heaps. In heaps the insertion is Linear-O(n), deletion and sorting takes O(nlogn). But the Time complexity of BST, O(logn) can be possible only if the Tree is balanced(if the left and right subtrees of the root differ by maximum 1). 
There is a possibility that tree is not balanced and is skewed to either right or left(means all the values are either to left of the root or to the right).
To modify this one can Improve the existing BST algorithm and the modified version is generally reffered to as AVL Tree(self Balancing Tree).
