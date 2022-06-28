## Basic Concepts

Before writing your first program in C++, you first need to familiarize yourself with some basic concepts in C++. This is because your first program is going to utilise a lot of C++ concepts, which is going to look very confusing if you don't understand them first.

### Types

In C++, there are things known as data-types. Data-types are exactly what they sounds like: types of data. There are a lot of different data-types in C++, but for now, you only need to know the following types.

Name | Description | Example
-- | -- | --
`int` | A signed integer (number with no decimal points) | `5`
`double` | A number with a decimal point | `6.7`
`string` | Text | `"Hello, this is a string of text!"`

You will be using data types a lot in C++, as you will see.

### Variables

When working in C++, you will encounter the need to hold data in the computer's memory. That is where variables comes in. Variables are specific chunks of the computer's memory that you can use to hold data. To create variables, the following syntax is used:

```c++
type name = initial_value
```
Here is a basic breakdown:
- `type` is the name of the data-type of the data that you're going to hold in the variable.
- `name` is the name of the variable. It can pratically be anything you want, with a few rules that I will eventually list below.
- `initial_value` is the value that you would like to assi

As stated above, there are a few rules to what you can name variables. They are:

- It must not begin with a number.
- It must not have spaces in it.
- You cannot use a C++ keyword.

Other than that, there really aren't any rules to naming variables in C++.

### Example Program

With what we now learned, you can make your first program with basic functions:

```c++
#include <iostream>
int main(){
    string hello = "Hello, World!";
    std::cout << hello;
    // Prints: Hello, World!
    return 0;
}
```
The `#include <iostream>` is used to import a file called iostream into the current program. iostream manages the input and output streams of the current program. You will learn more about this later.

`int main(){}` is always necessary for the main function. This is where all your code is going to be ran.

`string hello = "Hello, World!";` is the declaration of the variable, with a string type. This variable contains the string "Hello, World!"

`std::cout <<` stands for Standard Character Output, which is the method for printing logs to the console. It is the equivalent of `print()` in Python and `console.log()` in JavaScript. In this case, it tells the program to output the value of the string hello to the console.

Finally, `return 0;` is necessary to tell the program that the code executed successfully, with no problems. If it doesn't hit the `return 0;` it will throw an error.

### Functions

In C++, code are organized into structures known as _functions_. A function is essentially a block of code that can be executed by either another function or a different program altogether. Unlike in some other languages such as Python or JavaScript, you cannot put _statements_ (You'll learn about them later) outside of functions.

// Note: this tutorial is not finished, as shown by the incomplete nature of this page. Check back here later.