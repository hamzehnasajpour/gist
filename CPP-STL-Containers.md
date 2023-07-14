## Standard Containers
A container is a holder object to stores a collection of other objects. 

## Sequence containers:
### * array
```cpp
#include <array>

std::array<int, 5> ar = {5,4,3,2,1};
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

### * vector
```cpp
#include <vector>
std::vector<int> v;
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


### * deque
Double Ended Queue: Exact like `vector`, but with efficient insertion and deletion of elements also at the beginning of the sequence, and not only at its end. So all funcations are shared here with `vector`.

```cpp
#include <deque>
std::deque<int> gquiz;
```
link: https://www.geeksforgeeks.org/deque-cpp-stl/

### * forward_list
It differs from the list by the fact that the forward list keeps track of the location of only the next element while the list keeps track of both the next and previous elements. Forward List is preferred over the list when only forward traversal is required.

```cpp
#include <forward_list>
std::forward_list<int> flist1;
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


### * list
Lists are sequence containers that allow non-contiguous memory allocation. As compared to the vector, the list has slow traversal, but once a position has been found, insertion and deletion are quick (constant time). Normally, when we say a List, we talk about a doubly linked list. For implementing a singly linked list, we use a forward_list.

```cpp
#include <list>
std::list<int> gqlist{12,45,8,6};
```

link: https://www.geeksforgeeks.org/list-cpp-stl/

## Container adaptors
### * stack
Stacks are a type of container adaptor, specifically designed to operate in a LIFO context (last-in first-out), where elements are inserted and extracted only from one end of the container.

```cpp
#include <stack>
std::stack<int> stack;
```
* `empty()`: Returns whether the stack is empty – Time Complexity : O(1) 
* `size()` : Returns the size of the stack – Time Complexity : O(1) 
* `top()` : Returns a reference to the top most element of the stack – Time Complexity : O(1) 
* `push(g)` : Adds the element ‘g’ at the top of the stack – Time Complexity : O(1) 
* `pop()` : Deletes the most recent entered element of the stack – Time Complexity : O(1) 


link: https://www.geeksforgeeks.org/stack-in-cpp-stl/

### * queue
Queues are a type of container adaptors that operate in a first in first out (FIFO) type of arrangement. Elements are inserted at the back (end) and are deleted from the front.

```cpp
#include <queue>
std::queue<int> q;
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

### * pritority_queue
A C++ priority queue is a type of container adapter, specifically designed such that the first element of the queue is either the greatest or the smallest of all elements in the queue, and elements are in non-increasing or non-decreasing order (hence we can see that each element of the queue has a priority {fixed order}).

```cpp
#include <queue>
std::priority_queue<int> q;
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
### * set
Sets are a type of associative container in which each element has to be unique because the value of the element identifies it. The values are stored in a specific sorted order i.e. either ascending or descending.

```cpp
#include <set>
std::set<char> a;
```
* `begin()`, `end()`, `cbegin()` and `cend()` : itterators
* `rbegin()`, `rend()`, `crbegin()` and `crend()` : reverse itterators
* `empty` :	Test whether container is empty (public member function)
* `size` : Return container size (public member function)
* `max_size`: Return maximum size (public member function)
* `insert`: Insert element (public member function)
* `erase` : Erase elements (public member function)
* `swap` : Swap content (public member function)
* `clear` : Clear content (public member function)
* `emplace` : Construct and insert element (public member function)
* `emplace_hint` : Construct and insert element with hint (public member function)

link: https://www.geeksforgeeks.org/set-in-cpp-stl/

### * multiset
Multisets are a type of associative containers similar to the set, with the exception that multiple elements can have the same values.

```cpp
#include <set>
std::multiset<char> a;
```

* `begin()` – Returns an iterator to the first element in the multiset –>  O(1)
* `end()` – Returns an iterator to the theoretical element that follows the last element in the multiset –> O(1)
* `size()` – Returns the number of elements in the multiset –> O(1)
* `max_size()` – Returns the maximum number of elements that the multiset can hold –> O(1)
* `empty()` – Returns whether the multiset is empty –> O(1)
* `insert (x)` – Inserts the element x in the multiset –> O(log n)
* `clear ()` – Removes all the elements from the multiset –> O(n)
* `erase(x)` – Removes all the occurrences of x –> O(log n)

link: https://www.geeksforgeeks.org/multiset-in-cpp-stl/

### * map
Maps are associative containers that store elements in a mapped fashion. Each element has a key value and a mapped value. No two mapped values can have the same key values.

```cpp
#include <map>
std::map<std::string, int> map;
```
* `begin()` – Returns an iterator to the first element in the map.
* `end()` – Returns an iterator to the theoretical element that follows the last element in the map.
* `size()` – Returns the number of elements in the map.
* `max_size()` – Returns the maximum number of elements that the map can hold.
* `empty()` – Returns whether the map is empty.
* `pair_insert(keyvalue, mapvalue)` – Adds a new element to the map.
* `erase(iterator position)` – Removes the element at the position pointed by the iterator.
* `erase(const g)` – Removes the key-value ‘g’ from the map.
* `clear()` – Removes all the elements from the map.

link: https://www.geeksforgeeks.org/map-associative-containers-the-c-standard-template-library-stl/

### * multimap
Multimap is similar to a map with the addition that multiple elements can have the same keys. Also, it is NOT required that the key-value and mapped value pair have to be unique in this case. One important thing to note about multimap is that multimap keeps all the keys in sorted order always. These properties of multimap make it very much useful in competitive programming.

```cpp
#include <map>
std::multimap<int, int> gquiz1; // empty multimap container
```

link: https://www.geeksforgeeks.org/multimap-associative-containers-the-c-standard-template-library-stl/

## Unordered associative containers:
### * unordered_set
Unordered sets are containers that store unique elements in no particular order, and which allow for fast retrieval of individual elements based on their value.

link: https://www.geeksforgeeks.org/unordered_set-in-cpp-stl/

### * unordered_multiset
Unordered multisets are containers that store elements in no particular order, allowing fast retrieval of individual elements based on their value, much like unordered_set containers, but allowing different elements to have equivalent values.

link: https://www.geeksforgeeks.org/cpp-unordered_multiset/

### * unordered_map
Unordered maps are associative containers that store elements formed by the combination of a key value and a mapped value, and which allows for fast retrieval of individual elements based on their keys.

link: https://www.geeksforgeeks.org/unordered_map-in-cpp-stl/

### * unordered_multimap
Unordered multimaps are associative containers that store elements formed by the combination of a key value and a mapped value, much like unordered_map containers, but allowing different elements to have equivalent keys.

link: https://www.geeksforgeeks.org/unordered_multimap-and-its-application/

---

https://cplusplus.com/reference/stl/