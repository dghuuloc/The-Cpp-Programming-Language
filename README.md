# <p align="center">The Cpp Programming Language</p>
---

## Introduction
C++ is a general purpose programming language which was first developed in the 1980s. The language was designed by Bjarne Stroustrup under with the name “C with classes”.

## Hello World in C++
```cpp
#include <iostream>
using namespace std;

int main() {
	cout << "Hello, World!" << endl;
	return 0;
}
```
or
```cpp
#include <iostream>

int main() {
	std::cout << "Hello, World!" << std::endl;
	return 0;
}
```

### Understanding a C++ Program
The first line tells the computer to use the `#include <iostream>` header file for this specific program. A header file is a separate file with prewritten C++ code.

here are many other header files which are required for a specific program to run properly. Some of them are `math`, `vector`, and `string`. Header files are generally represented by a `.h` extension (you don’t need to add `.h` when including C++ standard library files)

The `iostream` stands for "input-output stream". The `iostream` file contains code for allowing the computer to take input and generate an output like the `std::cout` and `std::endl`, using the C++ language.

The second line, `using namespace std;`, tells the computer to use the standard namespace which includes features of standard C++.

You could write this program without this line, but you’d have to use `std::cout` instead of `cout` and `std::endl` instead of `endl` on line 4. But the second line makes the code more readable and our lives as programmers easier.

C++ starts the execution of a program from the global `main()` function, which is declared with `int main()`. This `main()` function will be called by the OS when you execute your program and every executable C++ program must have a `main()` function. During execution, the computer starts running the code from every line from the opening curly brace, `{`, to the closing curly brace, `}`.

The word `int` in the function declaration simply means this function returns an integer. Returning `0` at the end of a program means it ran successfully. A non zero return value usually indicates some kind of failure, but that topic is out of the scope of this article.

>[!NOTE]
> Note: Every function starts with `{` and ends with `}`

`cout` stands for "character output", and is an object to display output on the screen.

`cout` is followed by `<<`, which is an insertion operator. Insertion operators send data to the stream operators that come before them.

Next is the phrase `Hello, World!` surrounded by double quotes (`"`). Anything between double quotes is a string. This is a simple string with standard characters, but certain special characters have a different syntax for print statements.

So the insertion operator, `<<`, passes the string `"Hello, World!"` to the `cout` object. You can chain multiple things to output in a single `std::cout` call as follows:
```cpp
#include <iostream>

int main() {
	std::cout << "Hello, World!" << " " << "C++ is awesome!" << std::endl;
	return 0;
}
```
If you compile and run this program, you'll get the following output:

```
Hello, World! C++ is awesome!
```

Moreover, if you look at the end of the line, there's another insertion operator and `endl`. The `endl` is a reserved word in the C++ language, and stand for "end line". In C++, you can use the `endl` object to end the current line, flush the stream, and go to the next line in the output.

Finally, the line ends with a semicolon, `;`.

The `"Hello, World!"` and the `endl` are passed to `cout` with insertion operators, and the line ends with a semicolon.

The `return 0;` safely terminates the current function, `main()`. And since there's no function after `main()`, the entire program is terminated.

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

## Compiling and Running C++ Programs
Once you've done that, you should be able to write and compile C++ programs on your computer. To do so, create a file `hello-world.cpp` anywhere in your computer.

Now if you're using GCC, open a terminal window in the same directory where the `hello-world.cpp` file exists and execute the following command:

```
g++ -o hello-world hello-world.cpp
```
This command will compile the `hello-world.cpp` into the file indicated in the `-o` option. You should see a new binary file named `hello-world` in the same folder. Execute the file from the terminal as follows:

```
./hello-world
# Hello, World!
```

## Data Types and Arrays
### Data Types
C++ has seven fundamental data types. They are as follows:

| DATA TYPES   | MEANING 		 | TYPICAL BIT WIDTH			| TYPICAL RANGE 	|  
|--------------|:------------------------|:---------------------|:---------------------|
| `char`       | Character         	 | 1 bytes 		| -128 to 127 or 0 to 255 |
| `unsigned char`       | Character         	 | 1 bytes 		| 0 to 255 |
| `signed char`       | Character         	 | 1 bytes 		| -128 to 127 |
| `int`        | Integer          	 | 2 bytes or 4 bytes   | -2147483648 to 2147483647 |
| `unsigned int`        | Integer          	 | 2 bytes or 4 bytes   | 0 to 4294967295 |
| `signed int`        | Integer          	 | 2 bytes or 4 bytes   | -2147483648 to 2147483647 |
| `short int`        | Integer          	 | 2 bytes   | -32768 to 32767 |
| `unsigned short int`        | Integer          	 | 2 bytes   | 0 to 65535 |
| `signed short int`        | Integer          	 | 2 bytes   | -32768 to 32767 |
| `long int`        | Integer          	 | 4 bytes   | -2147483648 to 2147483647 |
| `unsigned long int`        | Integer          	 | 4 bytes   | 0 to 4294967295 |
| `signed long int`        | Integer          	 | 4 bytes   | -2147483648 to 2147483647 |
| `float`      | Floating Point          | 4 bytes 		| +/-3.4e +/-38 (~7 digits) |
| `double`     | Double Floating Point   | 8 bytes 		| +/-1.7e +/-308 (~15 digits) |
| `wchar_t`     | Wide Character          | 2 bytes or 4 bytes  | 1 wide character		 |
| `bool`       | Boolean          	 | 1 bytes 		| |
| `void`       | Empty          	 | 0 bytes 		| |

There are modifiers such as `short`, `long`, `signed`, and `unsigned`.

To declare a variable of a certain data type, you can do something like this:

```cpp
#include <iostream>
using namespace std;

int main() {
	int number = 25;
	cout << "The number is " << number << endl;
	return 0;
}
```

### Array
There are also arrays which are capable of storing multiple values of the same type. So if you want to declare an array of type `int`, you can do so as follows:

```cpp
#include <iostream>
using namespace std;

int main() {
	int numbers[] = {2, 4, 5, 9, 4};
	cout << "The number is " << numbers[0] << endl;
	return 0;
}
```
You can access any element from the array following the `arrayName[index]` syntax. Array indexes are zero-based so to access the number one element.

You can also create strings using arrays of `char` type as follows:

```cpp
#include <iostream>
using namespace std;

int main() {
	char name[] = "Farhan";
	cout << "My name is " << name << endl;
	return 0;
}
```
## C++ String




## References
- [How to Learn the C++ Programming Language](https://www.freecodecamp.org/news/how-to-learn-the-c-programming-language/)




