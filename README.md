# Binary Search Tree Assignment

## Overview
For this assignment you will be implementing the Binary Search Tree ADT and a number of associated functions. This project is based on the content of chapters 9 and 10 in the Java Software Structures book.

### Table of Contents
**[Files to complete](#files-to-complete)**<br>
**[Support Code API](#support-code-api)**<br>
**[Part One: Import Project](#part-one-import-project)**<br>
**[Part Two: Implement the BinaryTreeNode Interface](#part-two-implement-the-binarytreenode-interface)**<br>
**[Part Three: Implement the BinaryTreeUtility Interface](#part-three-implement-the-binarytreeutility-interface)**<br>
**[Part Four: Implement the BinarySearchTree Interface](#part-four-implement-the-binarysearchtree-interface)**<br>
**[Part Five: Commit Project and Submit Pull Request](#part-five-commit-project-and-submit-pull-request)**


## Files to complete
You are expected to write an implementation for each of the interfaces listed in the `Configuration` class: `BinaryTreeNode`, `BinaryTreeUtility`, and `BinarySearchTree`. Update the methods in `Configuration.java` as these implementation are completed.

### Test files
In the test folder, you are provided with several JUnit test cases that will help you keep on track while completing this assignment. It will help you to run the tests often and use them as a checklist of things to do next. Please do not modify my test cases, but you may add your own JUnit classes to fill out the test suite.

### Support Code API
The Support Code’s comments have been generated into a nicely formatted API that can be found here:

https://jd12.github.io/binary-search-tree/

You may benefit from spending some time reading over the Javadoc for each of the interfaces and classes provided.


## Part One: Import Project 
When you clone / download your project from GitHub Classroom, you will want to ensure that your project should have no errors and contain the following root items:

**src** - The source folder where all code you are submitting must go. You can change anything you want in this folder, you can add new files, etc...<br>
**test** - The test folder where all the public unit tests are available<br>
**support** - This folder contains support code for you to use. Be very careful if you choose to change files in this folder.<br>
**JUnit 5** - A library that is used to run the test programs<br>
**JRE System Library** - This is what allows java to run<br>

If you are missing any of the above or errors are present in the project, seek help immediately, so you can get started.


## Part Two: Implement the BinaryTreeNode Interface
A `BinaryTreeNode` represents a node in a binary tree. It stores data of generic type `T` and may have a right and a left child, each a reference to another `BinaryTreeNode`.  The `BinaryTreeNode` interface includes standard getters and setters for a `BinaryTreeNode`’s right and left children as well as its data.

## Part Three: Implement the BinaryTreeUtility Interface
The `BinaryTreeUtility` interface provides basic functions for working with a binary tree.

**Depth** -- The depth of the tree is the maximum level of any leaf node in the tree.  Recall that the level of a node begins at zero for the root of a tree with no children.  A child of the root is at level 1.

**Balance** -- The balance of a tree measures how close it is to a full or complete tree.  You will implement the method `isBalanced(BinaryTreeNode<T> root, int tolerance)` which determines whether the maximum difference in the depth of any two children is no larger than the given tolerance value.

**Testing the BST property** -- Recall that a BST is a binary tree that also satisfies a special sorting property: if all elements in left subtree of any node X are less than or equal to node X and all nodes in the right subtree of X are greater than X.  You will write a function `isBST(root)` which returns true if `root` is the root of a valid binary search tree.  Your function need not explicitly test basic requirements of the binary tree (e.g. that there is a unique path from the root to every node in the tree).  Testing the BST property has a nice recursive solution, but it requires some thought.

**Iterators** -- You will also provide three methods `getPreOrderIterator(BinaryTreeNode<T> root)`, `getInOrderIterator(BinaryTreeNode<T> root)`, `getPostOrderIterator(BinaryTreeNode<T> root)`, each returning an iterator that follows the stated traversal over a binary tree. A `PreOrderIterator` class has been provided as an example to get started.

**Feeling ambitious?**<br>
See if you can make a Level-Order iterator!


## Part Four: Implement the BinarySearchTree Interface
Next you will implement methods underlying the BST structure.  

**Transformers** -- Add and remove are the main transformers of a BST.  These must add or remove elements while maintaining the BST property.

**Observers** -- You will implement an `isEmpty()` method and a `size()` method.  In addition, you will implement  the `getMinimum()` and `getMaximum()` functions, which return the smallest and largest values stored in the BST.  

**Iterator** -- This function returns an iterator that supports in-order access to the nodes of the BST.  Recall that an in-order traversal of a BST results in a sorted order due to the BST property.  

**Bonus** The method returning an iterator should complete in O(1) time, so it should not compute the entire sequential order ahead of time.

If you choose to implement an iterator method that returns in O(1) time, you will receive extra credit. This means you should not compute the traversal in its entirety when creating and returning the iterator.  Instead, the iterator should be initialized and returned as a result of the function call, with the next element in the traversal computed with each call to `next()`.


## Part Five: Commit Project and Submit Pull Request
When you have finished your solution and are ready to submit, make your final commit and push everything up to GitHub.
