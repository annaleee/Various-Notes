# C++ Basics

[toc]

## Const Qualifier

### Property

* Cannot be modified later on
* Must be initialized when it is defined

### Const Reference

* const reference can be initialized to an rvalue
* Practical use:
  * pass struct/class as the function argument
  * Function call with consts or expression is not available for non-const reference but is available for const reference

### Const Pointers

```C++
const T *p;// the object pointed by p cannot be changed
T *const p;// the pointer cannot be changed
const T * const p;// neither can be changed
```

## Recursion Function Call Mechanism

### Call Stacks

* Add the storage of new function on the top of the stack (LIFO)

## IO

* Print something: `cout<<`

* Read input: `cin>>foo`

* Read blanks/ tabs: `getline(cin,str)`

* Read single character: `cin.get(ch)`

* File stream:

  * ```C++
    #include <fstream>
    ifstream iFile;//declare an input file stream
    ofstream oFile;//declare an output file stream
    iFile.open("xxx.txt");
    iFile>> str;
    getline(iFile,str);
    iFile.close();
    oFile<<bar;
    
    ```

* string stream
  * `#include<sstream>`
  * Declare an input string stream object: `istringstream iStream`
  * Declare an output string stream object: `ostringstream oStream`
  * read the string: `iStream.str(a_string)`
  * output the string: `a_string = oStream.str()`

## Testing

* assert function

  * `#include<cassert>`

  * if the argument is true, `assert()` does nothing

  * if the argument is false, `assert()` causes your program to stop, printing an error message to the `cerr` stream

  * example:

  * ```C++
    #include<cassert>
    int smaller = min(a, b);
    assert(smaller <= a && smaller <= b);
    ```

## Inheritance

* Protected: can be seen by all memebers of this class and any derived classes

# Data Structure

## Linked List

### Implementation

* ```C++
  struct node{
    node *next;
    int value;
  }
  class IntList{
    	node *first;
    public:
    	bool isEmpty();
    	//returns true if list is empty, false otherwise
    	void insert(int v);
    	//inserts v into the front of the list
    	//Time-complexity: 
    	int remove();
    	// if list is empty, throw listIsEmpty, otherwise, remove and return the first element of the list
    	IntList();
    	IntList(const IntList& l);
    	~IntList();
    	IntList &operator=(const IntList &l);
    }
  ```

## Stack

* LIFO

### Implementation

* `size()`: number of elements
* `isEmpty()`: checks if stack has no elements
* `push(Object o)`: add object o to the top of stack
* `pop()`: remove the top object if stack is not empty, throw stack Empty otherwise
* `Object &top()`: return a reference to the top element

### Stack using Arrays

* `size()`: return size
* `isEmpty()`: return `size==0`
* `push(Object o)`: add object to the end of the array and increment size, allocate more space if necessary
* `pop()`: decrement size(), if `size==0`, throw stackEmpty
* `Object &top()`: return a reference to `Array[size - 1]`
* Advantages:
  * Time-efficient
* disadvantages:
  * Not memory-efficient

### Stack using Linked List

* `size()`: `LinkedList::size()`
* `isEmpty()`: `LinkedList::isEmpty()`
* `push(Object o)`: `LinkedList::insertFirst(Object o)`
* `pop()`: `LinkedList::removeFirst()`
* `Object &top()`: return a reference to object stored in the first node
* Advantages:
  * Memory-efficient
* disadvantages:
  * Not time-efficient

### Queue

* FIFO

### Implementation

* `size()`: number of elements in the queue
* `isEmpty()`: check if queue has no elements
* `enqueue(Object o)`: add object o to the rear of the queue
* `dequeue()`: remove the front object of the queue if not empty; otherwise, throw queueEmpty
* `Object &front()`: return a reference to the front element of the queue
* `Object & rear()`: return a reference to the rear element of the queue

### Queue using Linked Lists

### Queue using Arrays

* `enqueue(Object o)`: O(1)
* `dequeue()`: O(n)
* To solve the problem, we could use a circular arrays to implement the queue
* `front = (front + 1) % MAXSIZE`
* `rear = (rear + 1) % MAXSIZE`
* 