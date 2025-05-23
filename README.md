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

## Supported Features

- ✅ Custom singly linked list implementation
- ✅ Iterator support (compatible with range-based for loops and STL algorithms)
- ✅ Comparison operators:
    - `==`, `!=`, `<`, `>`, `<=`, `>=`
    - Implemented using `std::equal` and `std::lexicographical_compare`
- ✅ Swap operations:
    - Member method `swap`
    - Overload of template `std::swap`
- ✅ `std::initializer_list` constructor:
    - Enables list creation like: `List l = {1, 2, 3};`
- ✅ Copy constructor and copy assignment:
    - Copy assignment provides **strong exception safety**
    - If an exception occurs during assignment, the original list remains unchanged
- ✅ List modification methods:
    - `PopFront`: removes the first element (noexcept)
    - `InsertAfter`: inserts an element after the given iterator (strong exception safety)
    - `EraseAfter`: removes the element after the given iterator (noexcept)
- ✅ Special iterators:
    - `before_begin()` and `cbefore_begin()` return iterators to the fictitious position before the list’s first element
    - These iterators are used with `InsertAfter` and `EraseAfter` at the beginning of the list

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


