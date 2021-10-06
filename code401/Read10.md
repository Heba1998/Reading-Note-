# ***Stacks and Queues***

## ***What is a Stack***



*A stack is a data structure that consists of `Nodes`. Each Node references the next Node in the stack, but does not reference its previous.*

```
In the stacks only two operations are allowed: push the item into the stack, and pop the item out of the stack. A stack is a limited access data structure - elements can be added and removed from the stack only at the top. push adds an item to the top of the stack, pop removes the item from the top. A helpful analogy is to think of a stack of books; you can remove only the top book, also you can add a new book on the top.
```
![IMG](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-10/resources/images/stack1.PNG)


* ***Common terminology for a stack is***

    * **Push**

       *means to put an item into the stack*
       *Pushing a Node onto a stack will always be an `O(1)` operation. This is because it takes the same amount of time no matter how many Nodes `(n)` you have in the stack.*

       *When adding a Node, you push it into the stack by assigning it as the new top, with its next property equal to the original top.*

    * **Pop**

        *means to remove an item from the stack.*
        *When conducting a pop, the top Node will be re-assigned to the Node that lives below and the top Node is returned to the user.*


    * **Top** 

        *top function returns the topmost element of the stack.*


    * **Peek** 

        *means to view the value of the top node of the stack.*
        *When conducting a peek, you will only be inspecting the top Node of the stack.*

    
    * **IsEmpty** 
    
        *checking if the stack is empty return true else return false.*


* ***The concepts of Stacks:*** 
    * FILO `First In Last Out`

    *This means that the first item added in the stack will be the last item popped out of the stack.*

    * LIFO `Last In First Out`

    *This means that the last item added to the stack will be the first item popped out of the stack.*


## ***What is a Queue***

```
An excellent example of a queue is a line of students. New additions to a line made to the back of the queue, while removal (or serving) happens in the front. In the queue only two operations are allowed enqueue and dequeue. Enqueue means to insert an item into the back of the queue, dequeue means removing the front item. 
```


![IMG](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-10/resources/images/Queue.PNG)


* ***Common terminology for a queue is***

    * **Enqueue**

       *Nodes or items that are added to the queue.*
       *This is done with an `O(1)` operation in time because it does not matter how many other items live in the queue (n); it takes the same amount of time to perform the operation.*

    * **Dequeue**

        *Nodes or items that are removed from the queue. If called when the queue is empty an exception will be raised.*
        *This is done with an `O(1)` operation in time because it doesn’t matter how many other items are in the queue, you are always just removing the front Node of the queue.*


    * **Front** 

        *This is the front/first Node of the queue.*


    * **Peek** 

        *When you peek you will view the value of the front Node in the queue. If called when the queue is empty an exception will be raised.*
        *When conducting a peek, you will only be inspecting the front Node of the queue.*

    
    * **IsEmpty** 
    
        *checking if the stack is empty return true else return false.*


    * **Rear** 
    
        *This is the rear/last Node of the queue.*



* ***The concepts of Queues :*** 
    * FIFO `First In First Out`

    *This means that the first item in the queue will be the first item out of the queue.*

    * LILO `Last In Last Out`

    *This means that the last item in the queue will be the last item out of the queue.*


