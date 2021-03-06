# CSCI-3901-A2
Software Development Concepts- List Hierarchy

---------

This program lets you search and add values in the list. The lists
are added into multiple levels based on the Coin Object that provides
random number.

This program uses several implementations to create a hierarchy between
the levels which mimics the binary binary tree.

	-	The list contains only string values.
	-	The constructor accepts a Coin Object for getting a random number.
	-	The Lower List must be in a sorted order.

Each of these cases have their own implementation using linked lists to 
create a links between the nodes in all levels.

Files and external data
-----------------------

  - SkipUI.java  -- main for the program that prompts the user for the commands to add and search
  - ListHierarchy.java -- class that helps to add and search in the list across levels
  -	Node.java	-- Class that helps to create a node to store each value
  -	SentinelNodeList.java	-- Class that stores all the head and tail nodes in a linked list
  -	Coin.java	-- Interface that has flip method to be implemented
  -	ArrayCoin.java -- Class that implements Coin having a flip method implemented
  - RandomCoin.java -- Class that implements Coin having a flip method implemented

Data structures and their relations to each other
-------------------------------------------------

The program uses add or search method that takes string value and are stored in 
linked lists which is collection of all nodes.

	data Nodes - Each string value is stored in a node pointing to respective left
		   right, top, bottom nodes to create a linked List.

	hierarchy levels - All head and tail nodes in all levels are linked to one another
			using nodes and are maintained as a stack.

All elements are added in these head and tail nodes in sorted manner and these levels are
maintained by stack of linked lists.

Key algorithms and design elements
----------------------------------

The program uses add and goToNextlevel as the main methods to add the
elements across all levels.

Given a string to add in the list, checks the list is empty or not
and adds between the head and tail nodes and these nodes will act as a 
sentinel nodes and stored in a stack.

After adding to the list, it will check with the random variable of the object 
that is passed to the constructor. If it gets 1 it will be added to the next level
using another set of linked list and added into the stack and this will call random
variable recursively until it reaches the top level.

The program uses search method to find the element at any level starting from the top
node unti it reaches the specific element which uses a while method by traversing between
the head and tail nodes.

Assumptions and Limitations
---------------------------
	- no string to store will be more than 15 characters.
	- do not use any data structures of the Collection framework.
