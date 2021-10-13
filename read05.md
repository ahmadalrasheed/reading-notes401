## Big O: Analysis of Algorithm Efficiency

![biog](https://slideplayer.com/slide/4035807/13/images/2/Algorithm+Efficiency+and+Big-O.jpg)

***Big O’s role in algorithm efficiency is to describe the Worst Case of efficiency an algorithm can have in performing it’s job. It specifically looks at the factors mentioned above, which we often refer to as Space and Time. In order to analyze these limiting factors, we should consider 4 Key Areas for analysis:***


* Input Size
* Units of Measurement
* Orders of Growth
* Best Case, Worst Case, and Average Case




## Linked Lists

### What is a Linked List

***A Linked List is a sequence of Nodes that are connected/linked to each other. The most defining feature of a Linked List is that each Node references the next Node in the link.***

***There are two types of Linked List - Singly and Doubly. We will be implementing a Singly Linked List in this implementation.***

### Terminology:

* Linked List - A data structure that contains nodes that links/points to the next node in the list.

* Singly - `Singly` refers to the number of references the node has. A Singly linked list means that there is only one reference, and the reference points to the `Next` node in a linked list.

* Doubly - Doubly refers to there being two (double) references within the node. A `Doubly` linked list means that there is a reference to both the `Next `and `Previous` node.

* Node - Nodes are the individual items/links that live in a linked list. Each node contains the data for each link.

* Next - Each node contains a property called `Next`. This property contains the reference to the next node.

* Head - The `Head` is a reference of type `Node` to the first node in a linked list.

* Current - The `Current` is a reference of type `Node` to the node that is currently being looked at. When traversing, you create a new `Current `variable at the `Head` to guarantee you are starting from the beginning of the linked list.

### What does it look like

![linkedlist](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-05/resources/images/LinkedList1.PNG)


## Difference between Linked list and Array



**the follwing picture describes the difference between the linked lists and arrays**:
![difference](https://miro.medium.com/max/875/1*cUehR5S18XSoVLaPNfNzlA.jpeg)