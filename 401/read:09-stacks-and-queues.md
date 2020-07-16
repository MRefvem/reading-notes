# Read:09 - Stacks & Queues

## Article: Codefellows - Stacks and Queues

## What is a Stack?
A stack is a data structure that consists of Nodes. Each Node references the next Node in the stack, but does not reference its previous.

Common terminology for a stack includes:
- Push - Nodes or items that are put into the stack are pushed
- Pop - Nodes or items that are removed from the stack are popped. When you attempt to pop an empty stack an exception will be raised.
- Top - this is the top of the stack
- Peek - When you peed you will view the value of the top Node in the stack. When you attempt to peed an empty stack an exception will be raised
- IsEmpty - returns true when stack is empty otherwise returns false

Stacks use the following concepts:

### FILO
Fist in Last out
This means that the first term added will be the last out
### LIFO
Last in First out
This means that the last item added will be the first out

### Push O(1)
Pushing a Node onto a stack will always be an 0(1) operation. This is because it takes the same amount of time no matter how many Nodes(n) you have in your stack.
When adding to a Node, you push it into the stack by assigning it as the new top, with its next property equal to the original top.

Pseudocode:
ALOGORITHM push(value)
// INPUT <-- value to add, wrapped in Node internally
// OUTPUT <-- none
   node = new Node(value)
   node.next <-- Top
   top <-- Node

### Pop O(1)
Popping a Node off a stack is the action of removing a Node from the top. When conducting a pop, the top Node will be re-assigned to the Node that lives below and the top Node is returned to the user.
Typically, you would check isEmpty before conducting a pop. This will ensure that an exception is not raised. Alternately, you can wrap the call in a try/catch block.
You need to remove the top Node through reassignment otherwise it'll affect the rest of the stack.

Pseudocode:
ALGORITHM pop()
// INPUT <-- No input
// OUTPUT <-- value of top Node in stack
// EXCEPTION if stack is empty

   Node temp <-- top
   top <-- top.next
   temp.next <-- null
   return temp.value

### Peek O(1)
When conducting a peek, you will only be inspecting the top Node of the stack. Typically you would check isEmpty before conducting a peek. This ensures that an exception is not raised.

Pseudocode:
ALGORITHM peek()
// INPUT <-- none
// OUTPUT <-- value of top Node in stack
// EXCEPTION if stack is empty

   return top.value

### IsEmpty O(1)
Pseudocode:
ALGORITHM isEmpty()
// INPUT <-- none
// OUTPUT <-- boolean

return top = NULL

## What is a Queue?

Common terminology for a Queue is:

- Enqueue - Nodes or items that are added to the queue.
- Dequeue - Nodes or items that are removed from the queue. If called when the queue is empty and exception will be raised.
- Front - This is the first Node of the queue
- Read - This is the last Node of the queue
- Peek, you view the value of the front Node
- IsEmpty

Follows these concepts:

### FIFO
First in First out
This means that the first item in the queue will be the first out
### LILO
Last in Last out
This means that the last item in the queue will be the last out

### Enqueue O(1)

Pseudocode:
ALGORITHM enqueue(value)
// INPUT <-- value to add to queue (will be wrapped in Node internally)
// OUTPUT <-- none
   node = new Node(value)
   rear.next <-- node
   rear <-- node

### Dequeue O(1)

Pseudocode:
ALGORITHM dequeue()
// INPUT <-- none
// OUTPUT <-- value of the removed Node
// EXCEPTION if queue is empty

   Node temp <-- front
   front <-- front.next
   temp.next <-- null

   return temp.value

### Peek O(1)

Pseudocode:
ALGORITHM peek()
// INPUT <-- none
// OUTPUT <-- value of the front Node in Queue
// EXCEPTION if Queue is empty

   return front.value

### IsEmpty O(1)

Pseudocode:
ALGORITHM isEmpty()
// INPUT <-- none
// OUTPUT <-- boolean

return front = NULL