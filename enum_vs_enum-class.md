
### enum vs enum class in C++

#### Enum
##### Example 1

```cpp
enum BG_COLOR{ RED, GREEN, BLUE};
enum FG_COLOR{ RED, GREEN, BLUE};

int main () {
    // your code
    return 0;
}
```

Compile error for conflicts. :)

```bash
$ gcc example1.cpp -o example
example1.cpp:2:16: error: ‘RED’ conflicts with a previous declaration
    2 | enum FG_COLOR{ RED, GREEN, BLUE};
      |                ^~~
example1.cpp:1:16: note: previous declaration ‘BG_COLOR RED’
    1 | enum BG_COLOR{ RED, GREEN, BLUE};
      |                ^~~
example1.cpp:2:21: error: ‘GREEN’ conflicts with a previous declaration
    2 | enum FG_COLOR{ RED, GREEN, BLUE};
      |                     ^~~~~
example1.cpp:1:21: note: previous declaration ‘BG_COLOR GREEN’
    1 | enum BG_COLOR{ RED, GREEN, BLUE};
      |                     ^~~~~
example1.cpp:2:28: error: ‘BLUE’ conflicts with a previous declaration
    2 | enum FG_COLOR{ RED, GREEN, BLUE};
      |                            ^~~~
example1.cpp:1:28: note: previous declaration ‘BG_COLOR BLUE’
    1 | enum BG_COLOR{ RED, GREEN, BLUE};
      |                            ^~~~
```

##### Example 2

```cpp
enum BG_COLOR { RED, GREEN, BLUE};
enum ANIMALS  { DOG, CAT};

int main () {
    // ....  
    int color = BG_COLOR::RED;
    color = 50; // !!! Maybe you expect it's an enum value, but it's not. Since 50 is not valid at all.
    // ....      
    color = ANIMALS::DOG; // !!! You fill the color variable with invalid enum value
    return 0;
}
```

It will be compiled without any issue but you have compiled a series of bug instead of a reliable code. :)
* First bug: You fill the `color` with `50`. It's not a valid `BG_COLOR`.
* Second bug: You fill the `color` with `ANIMALS` enum values. 


#### Enum Class

##### Example1

```cpp
enum class BG_COLOR{ RED, GREEN, BLUE};
enum class FG_COLOR{ RED, GREEN, BLUE};
 
int main () {
    // your code
    return 0;
}
```
It will be compiled without any name conflict, since you are using the `enum class`.

##### Example2
```cpp
enum class BG_COLOR { RED, GREEN, BLUE};
enum class ANIMALS  { DOG, CAT};
 
int main () {
    // ....
    int color = BG_COLOR::RED;
    color = 50;  
    // ....
    color = ANIMALS::DOG; 
    return 0;
}
```

Compile Error:
```bash
$ gcc example2.cpp -o example2
example2.cpp: In function ‘int main()’:
example2.cpp:6:27: error: cannot convert ‘BG_COLOR’ to ‘int’ in initialization
    6 |     int color = BG_COLOR::RED;
      |                 ~~~~~~~~~~^~~
      |                           |
      |                           BG_COLOR
example2.cpp:9:22: error: cannot convert ‘ANIMALS’ to ‘int’ in assignment
    9 |     color = ANIMALS::DOG; // !!! You fill the color variable with invalid enum value
      |             ~~~~~~~~~^~~
      |                      |
      |                      ANIMALS
```


#### Conclusion
Using Enum Class is more safe.
