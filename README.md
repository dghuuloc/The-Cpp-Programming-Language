#<p align="center">The Cpp Programming Language</p>
---

## Introduction
C++ is a general purpose programming language which was first developed in the 1980s. The language was designed by Bjarne Stroustrup under with the name “C with classes”.

## Hello World in C++
```cpp
#include<iostream>
using namespace std;

int main() {
	count << "Hello, World!" << endl;
	return 0;
}
```
or
```cpp
#include<iostream>

int main() {
	std::count << "Hello, World!" << std::endl;
	return 0;
}
```

The first line tells the computer to use the `iostream` header file for this specific program. A header file is a separate file with prewritten C++ code.

here are many other header files which are required for a specific program to run properly. Some of them are `math`, `vector`, and `string`. Header files are generally represented by a `.h` extension (you don’t need to add `.h` when including C++ standard library files)

`iostream` stands for "input-output stream". The `iostream` file contains code for allowing the computer to take input and generate an output, using the C++ language.

The second line, `using namespace std;`, tells the computer to use the standard namespace which includes features of standard C++.

You could write this program without this line, but you’d have to use `std::cout` instead of `cout` and `std::endl` instead of `endl` on line 4. But the second line makes the code more readable and our lives as programmers easier.
