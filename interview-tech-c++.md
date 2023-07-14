#### C++ advantages:
* OOP
  - Polymorphism
  - Inheritence 
  - Encapsulation
  - Abstraction
  - Object & Class
* Performance

---
#### Data Types
* Primary: `integer`, `char`, `bool`, `float`, `double`, `void`
* Derived: `function`, `array`, `pointer`, `reference`
* User Defined: `class`, `stuct`, `union`, `enum`, `typedef`

---

#### Call by value vs call by reference
by value: copy, call with copying, change scope, memory
---

#### Tokens
* keywords
* identifiers
* constants
* strings
* symbols
* operators
---

#### `struct` vs `class`
* `staruct`
   - all members are public
   - doesnot support inheritance
   - value in memory
   - stack
* `class`
   - private, public and protected
   - inheritance
   - reference
   - heap
---
#### reference vs pointer
* reference
    - cannot reassign
    - cannot be null
    - access to member with `.`
    - access easily like a variable
* pointer
    - reassign
    - null
    - `->`
    - `*`
---
#### `heap` vs `stack`
* heap: RAM, bigger size, memory allocation
* stack:    , small size, quicker, all other variables
---
#### `array` vs `list`
* array: fixed location, fixed size, static, less memory
* list: dynamic, more memory
---
#### `new` vs `malloc`
* new: call ctor, faster, return the exact data type
* malloc: ,slower, `void *`
---
#### `virtual` vs `pure virtual`
`pure virtual` does not have an implementation, is it for abstract class, `runtime polymorphism`
---
#### `class` vs `object`
class is an instance of object
---
#### polymorphism
* Compile time
    - function overloading
    - operator overloading
* runtime 
    - function overriding
    - virtual function
---
### constructors
* Default constructior
* Parametrized constructor
* Copy constructor
```cpp
Sample(Sample &t){id=t.id};
```
---
### Operation permitted to pointer
* incr/decr
* add/sub
* compare
---
### Friend class & Friend function
* Friend class: access to all member/functions in private, public and protected
* Friend function: it cannot be called by an object
---
### Scope resolution order `::`
* access a global var when there is a local var with the same name
* define the functions outside the class
* multiple inheirtance
* for namespace
---
### Access modifiers
* private
* protected
* public
---
### STL
* Algorithms
Binary, lower,upper bount
min/max
reverse/rotate
sort/scope
* Containers
    - sequence: array,vectore, deque, list
    - adaptors: stack, queue, priority_queue
    - associative: unordered set, map, multiset, multimap
    - unordered_associate: unordered set, unordered map, unordered multiset, unordered multimap
---
### abstract class
has at least one pure virtual function.
---
### volatile
* prevent the compiler from performing optimization
* mmap, signal handlers, ...
---
### namespace
organsin and categorizing the codes
---
### shallow copy vs deep copy
* shallow: duplicates as little as possible, faster
* deep: copy everything, slower
---
### void pointer
pointer to any data type
---