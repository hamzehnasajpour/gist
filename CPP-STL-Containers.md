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

## Container adaptors
### stack
### queue
### pritority_queue

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
