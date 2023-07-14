#### C++ advantages:
* OOP
  - Polymorphism
    overloading and overriding
  - Inheritence 
    - defining a base class --> deriving a class from it
    - we have all that behaviour methods and variables
    - we can override
  - Encapsulation
    - hiding all vars and just implement some method to acess and modify
    - data protection
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
organsinng and categorizing the codes

---

### shallow copy vs deep copy
* shallow: duplicates as little as possible, faster
* deep: copy everything, slower

---

### void pointer
pointer to any data type

---

### smart pointers
* memory management/ leakage
* more efficient + additional feature
* destroy out of the scope
    - auto_ptr
    - unique_ptr
    - shared_ptr
    - weak_ptr

---

### `lvalue`
something refers to a memory location

---

* `decltype(n) a = 20;`
* `auto` vs `decltype`:
`auto` works on type, `decltype` works on expressions
* `typedef` creates an alias that can be used anywhere in place of a type
* `const` is a variable, readonly, used by pointer and by reference
* `explicit`: making the `ctor` or the conversions expliciti to avoid typecast by compiler

---

### design patterns
reusablity, proven solution, refactor, codesize

* Creational
* Structural
* Behavioural

- `singleton`
- `factory`: define an interface to decide which object to instansiate.
- `observer`: linking an object(`subject`) to dependents(`observers`) any of the ovserver change, subject in notified
- `adapter`: is a wrapper that converts one kind of interface to another
