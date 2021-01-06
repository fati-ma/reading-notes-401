# Readings: Implementation: Stacks and Queues
## Read: 10 - Stacks & Queues
### Hello this is ***Fatima*** :smile:, welcome to my blog where I will share with you the notes I take during reading from the resources provided each class. :closed_book: :pencil2:
### You can visit my GitHub repo for the readings notes from [here](https://github.com/fati-ma/reading-notes-401) or this webpage markdown file using this [link](https://github.com/fati-ma/reading-notes-401/blob/main/read-10.md).


# Stack

A stack is a data structure that consists of `Nodes`. Each `Node` references the next Node in the stack, but does not reference its previous.

### Methods:

1. `Push` - Nodes or items that are put into the stack are pushed
2. `Pop` - Nodes or items that are removed from the stack are popped. When you attempt to pop an empty stack an exception will be raised.
3. `Top` - This is the top of the stack.
4. `Peek` - When you peek you will view the value of the top Node in the stack. When you attempt to peek an empty stack an exception will be raised.
5. `IsEmpty` - returns true when stack is empty otherwise returns false.


### Concepts

**FILO**
First In Last Out

This means that the first item added in the stack will be the last item popped out of the stack.


**LIFO**
Last In First Out

This means that the last item added to the stack will be the first item popped out of the stack.


### Visualization

![stack](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-10/resources/images/stack1.PNG)


### Push

![](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-10/resources/images/pushStack1.PNG)

![](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-10/resources/images/pushStack2.PNG)

![](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-10/resources/images/pushStack3.PNG)


### Pop

![](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-10/resources/images/popStack1.PNG)

![](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-10/resources/images/popStack2.PNG)

![](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-10/resources/images/popStack3.PNG)

![](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-10/resources/images/popStack4.PNG)



# Queue

### Methods:

1. `Enqueue` - Nodes or items that are added to the queue.
2. `Dequeue` - Nodes or items that are removed from the queue. If called when the queue is empty an exception will be raised.
3. `Front` - This is the front/first Node of the queue.
4. `Rear` - This is the rear/last Node of the queue.
5. `Peek` - When you peek you will view the value of the front Node in the queue. If called when the queue is empty an exception will be raised.
6. `IsEmpty` - returns true when queue is empty otherwise returns false.


### Concepts

**FIFO**
First In First Out

This means that the first item in the queue will be the first item out of the queue.

**LILO**
Last In Last Out

This means that the last item in the queue will be the last item out of the queue.


### Visualization

![](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-10/resources/images/Queue.PNG)


### Enqueue

![](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-10/resources/images/Enqueue1.PNG)

![](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-10/resources/images/Enqueue2.PNG)

![](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-10/resources/images/Enqueue3.PNG)


### Dequeue

![](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-10/resources/images/Dequeue1.PNG)

![](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-10/resources/images/Dequeue2.PNG)

![](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-10/resources/images/Dequeue3.PNG)




