# Stack and Queues

- ## Review, Research, and Discussion

### What's the difference between Stack and Queue?

| Stack | Queue |
| ----- | ----- |
| The stack is based on LIFO(Last In First Out) principle | The queue is based on FIFO(First In First Out) principle |
| Insertion Operation is called Push Operation | Insertion Operation is called Enqueue Operation |
| Deletion Operation is called Pop Operation | Deletion Operation is called Dequeue Operation |
| Push and Pop Operation takes place from one end of the stack | Enqueue and Dequeue Operation takes place from a different end of the queue |
| The most accessible element is called Top and the least accessible is called the Bottom of the stack | The insertion end is called Rear End and the deletion end is called the Front End |
| Simple Implementation | Complex implementation in comparison to stack |
| Only one pointer is used for performing operations | Two pointers are used to perform operations |
| Empty condition is checked using Top==-1 | Empty condition is checked using Front==-1 or Front==Rear+1 |
| Full condition is checked using Top==Max-1 | Full condition is checked using Rear==Max-1 |
| There are no variants available for stack | There are three types of variants i.e circular queue, double-ended queue and priority queue |
| Can be considered as a vertical collection visual | Can be considered as a horizontal collection  visual |
| Used to solve the recursive type problems | Used to solve the problem having sequential processing |

### What is Stacks and how to use it?

Stack : a linear data structure that follows the specific order to perform the operations. Follows the LIFO (Last In First Out) principle, which means the element that is inserted last will be the first element to come out of the stack. we insert the element from one end with push operation and delete the element from the same end using pop operation. The end of the stack used to perform all the operations is called the top of the stack. </br>

### What is Queue?

Queue : a linear data structure in which we can insert the element from one side of the list and delete the element from the other side of the list. The end of the list from where the elements are inserted is called the rear end and the end from where the elements are deleted is called the front end. Therefore, the queue data structure follows the FIFO(First In First Out) principle, which means the element inserted first from the rear end will be the first element to be deleted from the front end. The insertion technique in the queue data structure is called enqueue operation and the deletion technique in the queue data structure is called dequeue operation. </br>

- ## Discussion

### Which 3 things had you heard about previously and now have better clarity on?

- HTTP requests
- Stack over flow
- Web Tokens

### Which 3 things are you hoping to learn more about in the upcoming lecture/demo?

- Stack
- Queue
- How to implement them using JS

### What are you most excited about trying to implement or see how it works?

- Stack

#### for more info please visit

- [Stack vs Queue | 12 Difference Between Stack and Queue](https://favtutor.com/blogs/stack-vs-queue)
- [Implementing Stack and Queue in JS](https://medium.com/globant/implementing-stack-and-queue-in-js-600c81a92120)
- [Stacks and Queues + tips for efficient implementation](https://blog.sessionstack.com/how-javascript-works-stacks-and-queues-tips-for-efficient-implementation-8072a130380b)
