## Standard Containers
A container is a holder object to stores a collection of other objects. 

### Sequence containers:
#### array
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

#### vector
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

#### deque
#### forward_list
#### list

### Container adaptors
#### stack
#### queue
#### pritority_queue

### Associative containers:
#### set
#### multiset
#### map
#### multimap

### Unordered associative containers:
#### unordered_set
#### unordered_multiset
#### unordered_map
#### unordered_multimap
