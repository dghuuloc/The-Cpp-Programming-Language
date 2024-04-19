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

C++ starts the execution of a program from the global `main()` function, which is declared with int `main()`. During execution, the computer starts running the code from every line from the opening curly brace, {, to the closing curly brace, }.

>[!NOTE]
> Note: Every function starts with `{` and ends with `}`

`cout` stands for "character output", and is an object to display output on the screen.

`cout` is followed by `<<`, which is an insertion operator. Insertion operators send data to the stream operators that come before them.

Next is the phrase `Hello, World!` surrounded by double quotes (`"`). Anything between double quotes is a string. This is a simple string with standard characters, but certain special characters have a different syntax for print statements.

So the insertion operator, `<<`, passes the string `"Hello, World!"` to the `cout` object.

But if you look at the end of the line, there's another insertion operator and `endl`.

`endl` is a reserved word in the C++ language, and stand for "end line". In C++, you can use the `endl` object to end the current line, flush the stream, and go to the next line in the output.

Finally, the line ends with a semicolon, `;`.

`"Hello, World!"` and the `endl` are passed to `cout` with insertion operators, and the line ends with a semicolon.

`return 0;` safely terminates the current function, `main()`. And since there's no function after `main()`, the entire program is terminated.

the `main()` function ends with a closing curly brace, `}`. If you don't end a function with a closing curly brace, you'll run into an execution error.

### Review
```cpp
#include <iostream>				// Header file
using namespace std;				// Standard namespace declaration

int main()					// The main() function
{						// Opening curly braces
	cout << "Hello, World!" << endl;	// Output "Hello, World!" to the console and end the line
	return 0;				// Terminate the main() function
}						// Closing curly braces
```



