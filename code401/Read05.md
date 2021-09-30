# ***Linked Lists***

![IMG](https://miro.medium.com/max/700/1*Jy5tjwrMdtpGl2ceq4f94A.jpeg)

* *What is a Linked List*

```
A Linked List is a sequence of Nodes that are connected/linked to each other. The most defining feature of a Linked List is that each Node references the next Node in the link.
```

* *There are two types of Linked List*

```
1- Singly: means that there is only one reference, and the reference points to the Next node in a linked list.

2- Doubly: means that there is a reference to both the Next and Previous node.
```

## ***The difference between the array and linked lists***

![IMG](https://miro.medium.com/max/700/1*cUehR5S18XSoVLaPNfNzlA.jpeg)

* **Memory management**

```
- The biggest differentiator between arrays and linked lists is the way that they use memory in our machines.
When an array is created , it needs a certain amount of memory(all in one place ). On the other hand, when a linked list is born, it doesn’t need bytes of memory all in one place. One byte could live somewhere, while the next byte could be stored in another place in memory altogether!
```

![IMG](https://miro.medium.com/max/700/1*G43FVT5xJ1n1QDKVNZUxXQ.jpeg)



## ***Big O Notation***

![IMG](https://miro.medium.com/max/500/1*FC0XX0-9Vx7yCS0dTS2Zrw.jpeg)

```
Big O Notation is a method of evaluating an algorithm's performance . It's a means of expressing how long a function, operation, or algorithm takes to perform based on the number of elements we provide to it . An O(1) function runs in constant time, which means that no matter how huge our input is, our algorithm will always require the same amount of time and memory to run.

    - Best case O(1): If we want to add a node with an O(1) efficiency, we have to replace the current Head of the linked list with the new node, without losing the reference to the next node in the list.

    - Worse case  O(n): Adding a node to the middle of a linked list is a bit different than adding to the beginning. This is because we are working with more nodes and must re-allocate to make room for the new node.
```