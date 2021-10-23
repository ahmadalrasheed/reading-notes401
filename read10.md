## Stacks and Queues


### What is a Stack


***A stack is a data structure that consists of Nodes. Each Node references the next Node in the stack, but does not reference its previous.***


### terminolgy 


* Push - Nodes or items that are put into the stack are pushed
* Pop - Nodes or items that are removed from the stack are popped. When you attempt to pop an empty stack an exception will be raised.
* Top - This is the top of the stack.
* Peek - When you peek you will view the value of the top Node in the stack. When you attempt to peek an empty stack an exception will be raised.
* IsEmpty - returns true when stack is empty otherwise returns false.



**Stacks Follow two important concepts which are :**

1. **FILO**
2. **LIFO**

#### FILO(First In Last Out)

***This means that the first item added in the stack will be the last item popped out of the stack.***



#### LIFO(Last In First Out)

***This means that the last item added to the stack will be the first item popped out of the stack.***

### Stack Visualization


![photo](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-10/resources/images/stack1.PNG)


#### Push O(1)
***its the process of adding new value to the Stack and it always must be  with O(1) complexity.***

***we can push any node we want by changing the top poitner of the stack from its current place into the new inserted node.***

#### Pop O(1)
***Popping a Node off a stack is the action of removing a Node from the top.***

***it can be done bu defining a  new pointer and make it the top place of the stack(because when poping values it will always be from the top), and then we can move the top pointer to the next value , and make the new pointer points to `NoNe`***

#### Peek

***Its a method for inspecting the top value of the Stack***


#### is_empty
***Its a method for checking if the stack is empty or not***













### What is a Queue



### terminolgy 
* Enqueue - Nodes or items that are added to the queue.
* Dequeue - Nodes or items that are removed from the queue. If called when the queue is empty an exception will be raised.
* Front - This is the front/first Node of the queue.
* Rear - This is the rear/last Node of the queue.
* Peek - When you peek you will view the value of the front Node in the queue. If called when the queue is empty * an exception will be raised.
* IsEmpty - returns true when queue is empty otherwise returns false.



**Queue Follow two important concepts which are :**

1. **FIFO**
2. **LILO**


#### FIFO(First In First Out)

This means that the first item in the queue will be the first item out of the queue.




#### LILO(Last In Last Out)

This means that the last item in the queue will be the last item out of the queue.


### Stack Visualization

this is how que look like:
![](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-10/resources/images/Queue.PNG)


#### Enqueue

its the process of adding a value to a queue, it can be done by defining two pointers `front` and `rear` and make them point to the first node , then we will move the rear pointer to every new node that we will add.

#### Dequeue

its the process of removing a value from a queue, it can be done by just by moving the front pointer from the value that we will delete (because always in queues we will delete from the `front` pointer postion ) and then we will make the node that we want to delete refer to  `None`.

#### Peek
Its a method for inspecting the top value of the Stack

#### is_empty


Its a method for checking if the stack is empty or not

