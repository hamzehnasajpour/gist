## Standard Containers
A container is a holder object to stores a collection of other objects. 

## Sequence containers:
### array
```cpp
#include <array>

array<int, 5> ar = {5,4,3,2,1};
```
* `[]` : `array[2]`
* `front()` and `back()` : first and last element
* `swap()` : swap contents of two arrays
* `empty()` : check the array is empty or not
* `at()` : access to elements
* `fill()` : fill all index with value
* `size()` and `max_size()`: maximum number of indexes
* `size_of()` : total size of array
* `begin()`, `end()`, `cbegin()` and `cend()`

link: https://www.geeksforgeeks.org/stdarray-in-cpp/

### vector
```cpp
#include <vector>
vector<int> v;
```

* `begin()`, `end()`, `cbegin()` and `cend()` : itterators
* `rbegin()`, `rend()`, `crbegin()` and `crend()` : reverse itterators
* `size()`
* `max_size()`: maximum elements which vector can hold
* `capacity()` : the size of the storage space currently allocated to the vector expressed as number of elements.
* `resize(n)`
* `empty()` : check is empty or not
* `shrink_to_fit()` : Reduces the capacity of the container to fit its size and destroys all elements beyond the capacity. (it affects on `capacity()`)
* `reserve()` : Requests that the vector capacity be at least enough to contain n elements.
* `[]` and `at()`
* `front()` and `back()`: first and last elements
* `data()` : returns a direct pointer to the memory array used internally to store
* `assign(n,value)`
* `push_back()` and `pop_back()`
* `insert(n,value)`
* `erase()`
* `swap()`
* `clear()`: remove all the elements
* `emplace(n,value)`: like `insert` ????

link: https://www.geeksforgeeks.org/vector-in-cpp-stl/


### deque
Double Ended Queue: Exact like `vector`, but with efficient insertion and deletion of elements also at the beginning of the sequence, and not only at its end. So all funcations are shared here with `vector`.

```cpp
#include <deque>
deque<int> gquiz;
```
link: https://www.geeksforgeeks.org/deque-cpp-stl/

### forward_list
It differs from the list by the fact that the forward list keeps track of the location of only the next element while the list keeps track of both the next and previous elements. Forward List is preferred over the list when only forward traversal is required.

```cpp
#include <forward_list>
forward_list<int> flist1;
```

* `assign()`: assign values to the forward list.
* `push_front()` and `emplace_front()`
* `pop_front()`
* `insert_after()`
* `emplace_after()`
* `erase_after()`
* `remove(value)`: Removes all occurrences of `value`
* `remove_if(condition)`: `flist.remove_if([](int x) { return x > 20; });`
* `clear()`
* `splice_after()`: This function transfers elements from one forward list to other.  

link: https://www.geeksforgeeks.org/forward-list-c-set-1-introduction-important-functions/


### list
Lists are sequence containers that allow non-contiguous memory allocation. As compared to the vector, the list has slow traversal, but once a position has been found, insertion and deletion are quick (constant time). Normally, when we say a List, we talk about a doubly linked list. For implementing a singly linked list, we use a forward_list.

```cpp
#include <list>
list<int> gqlist{12,45,8,6};
```

link: https://www.geeksforgeeks.org/list-cpp-stl/

## Container adaptors
### stack
Stacks are a type of container adaptor, specifically designed to operate in a LIFO context (last-in first-out), where elements are inserted and extracted only from one end of the container.

```cpp
#include <stack>
stack<int> stack;
```
* `empty()`: Returns whether the stack is empty – Time Complexity : O(1) 
* `size()` : Returns the size of the stack – Time Complexity : O(1) 
* `top()` : Returns a reference to the top most element of the stack – Time Complexity : O(1) 
* `push(g)` : Adds the element ‘g’ at the top of the stack – Time Complexity : O(1) 
* `pop()` : Deletes the most recent entered element of the stack – Time Complexity : O(1) 


link: https://www.geeksforgeeks.org/stack-in-cpp-stl/

### queue
Queues are a type of container adaptors that operate in a first in first out (FIFO) type of arrangement. Elements are inserted at the back (end) and are deleted from the front.

```cpp
#include <queue>
queue<int> q;
```

* `empty` :	Test whether container is empty (public member function)
* `size` :	Return size (public member function)
* `front` :	Access next element (public member function)
* `back` :	Access last element (public member function)
* `push` :	Insert element (public member function)
* `emplace` :	Construct and insert element (public member function)
* `pop` :	Remove next element (public member function)
* `swap` : contents (public member function)


link: https://www.geeksforgeeks.org/queue-cpp-stl/

### pritority_queue
A C++ priority queue is a type of container adapter, specifically designed such that the first element of the queue is either the greatest or the smallest of all elements in the queue, and elements are in non-increasing or non-decreasing order (hence we can see that each element of the queue has a priority {fixed order}).

```cpp
#include <queue>
priority_queue<int> q;
```

* `empty` :	Test whether container is empty (public member function)
* `size` : Return size (public member function)
* `top` : Access top element (public member function)
* `push` : Insert element (public member function)
* `emplace` : Construct and insert element (public member function)
* `pop` : Remove top element (public member function)
* `swap` : Swap contents (public member function)

link: https://www.geeksforgeeks.org/priority-queue-in-cpp-stl/

## Associative containers:
### set
### multiset
### map
### multimap

## Unordered associative containers:
### unordered_set
### unordered_multiset
### unordered_map
### unordered_multimap


---

https://cplusplus.com/reference/stl/