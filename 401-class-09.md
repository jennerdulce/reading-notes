# Stacks and Queues

## Stacks: LIFO

- liner data structure
- inserted and deleted from one side of the list known as the `top`
- Useful when order of actions is important
- ensures that a sytem does not move onto a new action before completing those before
- common uses: reversing, callstack
- insertion: `.push()`
- deletion: `.pop()`
- **recursion**

## Queues: FIFO

- liner data structure
- can only insert from rear
- deleted from the front
- insertion: `.enqueue()`
- deletion: `.dequeue()`
- maintains 2 pointers: `front` and `rear`
- **sequential processing**

## References

- https://levelup.gitconnected.com/the-stack-data-structure-what-is-it-and-how-is-it-used-in-javascript-23562fb8a590?gi=c4d654d0614f#:~:text=Stack%20data%20structures%20are%20useful,will%20reverse%20whatever%20is%20input.

- https://www.geeksforgeeks.org/difference-between-stack-and-queue-data-structures/
