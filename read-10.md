# Read class 09 
- Stacks & Queues

## What is a Stack

Terminology
* Push - Nodes or items that are put into the stack are pushed
* Pop - Nodes or items that are removed from the stack are popped. When you attempt to pop an empty stack an exception will be raised.
* Top - This is the top of the stack.
* Peek - When you peek you will view the value of the top Node in the stack. When you attempt to peek an empty stack an exception will be raised.
* IsEmpty - returns true when stack is empty otherwise returns false.

## Stack concepts

* FILO First in Last out - first item added in the stack will be the last item popped out of the stack.
* LIFO Last in first out - last item added to the stack will be the first item popped out of the stack.

- Stack Visualization
![stack](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-10/resources/images/stack1.PNG)

- Pushing a Node onto a stack will always be an O(1) operation. This is because it takes the same amount of time no matter how many Nodes (n) you have in the stack

- When adding a Node, you push it into the stack by assigning it as the new top, with its next property equal to the original top.

* PUSH O(1)
- First, you should have the Node that you want to add. Here is an example of a Node that we want to add to the stack.
- Next, you need to assign the next property of Node 5 to reference the same Node that top is referencing: Node 4
- Technically at this point, your new Node is added to your stack, but there is no indication that it is the first Node in the stack. To make this happen, you have to re-assign our reference top to the newly added Node, Node 5.

* POP o(1)
- The first step of removing Node 5 from the stack is to create a reference named temp that points to the same Node that top points to.
- Once you have created the new reference type, you now need to re-assign top to the value that the next property is referencing. In our visual, we can see that the next property is pointing to Node 4. We will re-assign top to be Node 4.
- We can now remove Node 5 safely without it affecting the rest of the stack. Before we do that though you may want to make sure that you clear out the next property in your current temp reference. This will ensure that no further references to Node 4 are floating around the heap. This will allow our garbage collector to cleanly and safely dispose of the Nodes correctly.
- Finally, we return the value of the temp Node that was just popped off.

* Peek O(1)
```

ALGORITHM peek()
// INPUT <-- none
// OUTPUT <-- value of top Node in stack
// EXCEPTION if stack is empty

   return top.value
```

* IsEmpty O(1)
```
ALGORITHM isEmpty()
// INPUT <-- none
// OUTPUT <-- boolean

return top = NULL
```

## What is a Queue
Terminology
* Enqueue - Nodes or items that are added to the queue.
* Dequeue - Nodes or items that are removed from the queue. If called when the queue is empty an exception will be raised.
* Front - This is the front/first Node of the queue.
* Rear - This is the rear/last Node of the queue.
* Peek - When you peek you will view the value of the front Node in the queue. If called when the queue is empty an exception will be raise
* IsEmpty - returns true when queue is empty otherwise returns false.

Queue Visualization
!(queue)[https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-10/resources/images/Queue.PNG]

* Enqueue O(1)
- First, we should change the next property of Node 4 to point to the Node we are adding. In our case with the visual below, we will be re-assigning Node 4’s .next to Node 5. The only way we have access to Node 4 is through our reference rear. Following the rules of reference types, this means that we must change rear.next to Node 5.
- After we have set the next property, we can re-assign the rear reference to point to Node 5. By doing this, it allows us to keep a reference of where the rear is, and we can continue to enqueue Nodes into the queue as needed.

* Dequeue O(1)
- The first thing you want to do is create a temporary reference type named temp and have it point to the same Node that front is pointing too. This means that temp will point to Node 1.
- Next, you want to re-assign front to the next value that the Node front is referencing. In our visual, this would be Node 2.
- Now that we have moved front to the second Node in line, we can next re-assign the next property on the temp Node to null. We do this because we want to make sure that all the proper Nodes clear any unnecessary references for the garbage collector to come in later and clean up.
- Finally, we return the value of the temp Node that was just removed.
