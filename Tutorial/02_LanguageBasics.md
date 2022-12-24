# Language Basics

Now that you have compiled and ran your first C++ program, it's time to learn about some basics of the C++ programming language. To avoid boring you with just plain theory and all that, we're gonna break down the Hello World program that you ran earlier, line by line so that you have a basic understanding of how it works.

Please note that this section is written under the assumption that you are familiar with basic programming concepts such as variables, functions, etc, because we won't be discussing those concepts in this section but rather how they are implemented in C++.

## `#include <iostream>

The first line of the program says this.

```cpp
#include <iostream>
```

Header files are a rather complicated topic, so we won't be going into too much detail right now, but what this does is it _includes_ the header file `iostream` so that the compiler are aware of it's contents, which includes functions and symbols for, well, I/O. We need to make the compiler aware of these _symbols_ in order to use them, and we need the I/O symbols because, well, we want to output "Hello, World!" to the terminal.

The next line looks a bit weird.
```cpp
auto main() -> int
{
```

This is how you create a _function_ in C++. As stated, earlier, I assume that you already know what functions are, but basically they are a block of code that can be executed, or _called_, by other code. In C++, you need at least one function, the `main` function, because how it works is that you write code in the main function, and when you run the program, the operating system calls the `main` function. It's a lot more complicated than that, but that's the general idea.

Let's take a look at the syntax. In C++, there are two different syntaxes for functions: the legacy syntax and the modern syntax. I personally prefer the modern syntax more since it more closely resembles other programming languages, but if you look at some legacy C++ codebases or some other C++ or C++-related tutorials, you might encounter these function syntaxes.

```cpp
int main()
{
```

The two function syntaxes are practically equivalent (until we start talking about using `decltype`s as return types but that's for a future chapter), so simply choose the one that you prefer. The rest of the tutorial will use the modern syntax because it's my personal preference.

Anyways, let's break this down, word by word.

```cpp
auto main() -> int
```

- The `auto` keyword is used to declare a function. Actually, the `auto` keyword is used to declare quite a lot of things in C++. Why `auto`? It's because of a bit of history in the development of C++ that we won't get too deep into for now.
- `main` declares the name of the function. C++, like many other languages, is case-sensitive, so it has to be `main`, all lowercase.
- The `()` is where you place function parameters. The `main` function _can_ take in parameters, but we don't need them right now so we'll just leave them out.
- The `-> int` specifies that the main function returns an integer (or an `int`). In C++, functions can return values back to the caller (like in many other languages). In this case, the return value of the `main` function is the _exit code_ of the program. The exit code is used to indicate the operating system whether the program has crashed or not. If the program exits successfully, the exit code must be `0`. Anything else can be used to indicate an error.

The next character is a lonely `{`.

```cpp
{
```

This indicates the beginning of the body of the main function, which contains all of the code.

Anyways, now that we are now at the part of the program that actually prints out `Hello World!`!

```cpp
std::cout << "Hello, World!\n";
```

For people coming from other languages, this might look a bit weird, and it is quite complicated, so we'll break it down.

- `std` is a _namespace_. For now, don't worry about what namespaces are. They are just a way that you can group symbols (like functions and variables) into 