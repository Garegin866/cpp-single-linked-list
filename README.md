# SingleLinkedList

A simple implementation of a **singly linked list** in modern C++ with forward iterators, exception safety, and unit tests.  
This project is written from scratch for learning and practicing custom container development.

## Features

- Templated `SingleLinkedList` class  
- Support for custom data types  
- Forward iterator (`BasicIterator`) supporting both `Iterator` and `ConstIterator`  
- Basic operations:
  - `PushFront` — insert at the beginning  
  - `Clear` — remove all elements  
  - `GetSize`, `IsEmpty`  
  - Iteration with range-based for loops  
- Fully tested with custom test cases  
- Exception safety is considered for copy operations  

## Example Usage

```cpp
SingleLinkedList<int> list;
list.PushFront(1);
list.PushFront(2);

for (int value : list) {
    std::cout << value << " ";
}
// Output: 2 1

```

## Build & Run

```bash
g++ -std=c++20 -Wall -Wextra -pedantic main.cpp -o list
./list
```

## Tests

Includes several tests covering:

- Empty list behavior
- Element insertion and clearing
- Object lifetime tracking via spies
- Exception safety during copying
- Iterator operations (*, ->, ++, comparisons)

## License

This project is open-source and available under the MIT License.


