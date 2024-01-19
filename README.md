## Site Link- https://im-archit.github.io/crossUpdate/


It looks like there might be a confusion in your question. In C++, the correct namespace for the vector class is std. It's not stdc. The correct usage is std::vector.

The std::vector is a dynamic array in C++ that provides functionalities similar to arrays but with additional features, such as dynamic resizing, bounds-checking, and various utility functions. It is part of the C++ Standard Template Library (STL).

Here's a brief explanation:

std::vector: It's a template class, meaning you can create vectors of different types (e.g., std::vector<int>, std::vector<double>).

Example:

cpp
Copy code
#include <vector>
#include <iostream>

int main() {
    // Creating a vector of integers
    std::vector<int> myVector = {1, 2, 3, 4, 5};

    // Accessing elements
    std::cout << "First element: " << myVector[0] << std::endl;

    // Iterating through the vector
    for (int i : myVector) {
        std::cout << i << " ";
    }

    return 0;
}
So, it's std::vector and not stdc::vector. If you meant something else, please clarify your question.

User
how can we do dynamic resizing, bounds checking and other features tell with example 
and also tell other features of c++ STL with examples separately
ChatGPT
Sure, I'll provide examples for dynamic resizing, bounds checking, and other features of std::vector in C++.

Dynamic Resizing:
std::vector automatically handles dynamic resizing when the number of elements exceeds the current capacity. It doubles the capacity whenever resizing is needed.

Example:

cpp
Copy code
#include <iostream>
#include <vector>

int main() {
    std::vector<int> myVector;

    for (int i = 1; i <= 10; ++i) {
        myVector.push_back(i);  // Automatically resizes when needed
    }

    std::cout << "Size: " << myVector.size() << ", Capacity: " << myVector.capacity() << std::endl;

    return 0;
}
Bounds Checking:
Unlike C-style arrays, std::vector performs bounds checking when accessing elements using at() method. It throws an std::out_of_range exception if the index is out of bounds.

Example:

cpp
Copy code
#include <iostream>
#include <vector>

int main() {
    std::vector<int> myVector = {1, 2, 3, 4, 5};

    try {
        std::cout << "Element at index 2: " << myVector.at(2) << std::endl;
        std::cout << "Element at index 10: " << myVector.at(10) << std::endl;  // Out of bounds, throws exception
    } catch (const std::out_of_range& e) {
        std::cerr << "Out of Range error: " << e.what() << std::endl;
    }

    return 0;
}
Other Features of C++ STL:
C++ Standard Template Library (STL) provides various other containers and algorithms. Here are some examples:

std::list (Doubly Linked List):

cpp
Copy code
#include <iostream>
#include <list>

int main() {
    std::list<int> myList = {1, 2, 3, 4, 5};

    myList.push_back(6);
    myList.push_front(0);

    for (int i : myList) {
        std::cout << i << " ";
    }

    return 0;
}
std::map (Associative Container):

cpp
Copy code
#include <iostream>
#include <map>

int main() {
    std::map<std::string, int> myMap;

    myMap["One"] = 1;
    myMap["Two"] = 2;
    myMap["Three"] = 3;

    std::cout << "Value of Two: " << myMap["Two"] << std::endl;

    return 0;
}
std::algorithm (Algorithms):

cpp
Copy code
#include <iostream>
#include <vector>
#include <algorithm>

int main() {
    std::vector<int> myVector = {3, 1, 4, 1, 5, 9, 2, 6};

    std::sort(myVector.begin(), myVector.end());

    for (int i : myVector) {
        std::cout << i << " ";
    }

    return 0;
}
These are just a few examples, and C++ STL provides many more containers and algorithms for various purposes.
