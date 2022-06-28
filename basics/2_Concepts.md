## Basic Concepts

Before writing your first program in C++, you first need to familiarize yourself with some basic concepts in C++. This is because your first program is going to utilise a lot of C++ concepts, which is going to look very confusing if you don't understand them first.

Now, if you've already done some form of programming before, most of these concepts shouldn't appear alien to you. However, C++ implements certain programming concepts differently than other programming languages does, so this chapter is still worth learning.

And yes, this chapter might be a little boring since it's mainly just theory rather than actual programming, but I promise we'll get to hands-on programming in the next chapter.

### Types

In C++, there are things known as data-types. Data-types are exactly what they sounds like: types of data. There are a lot of different data-types in C++, but for now, you only need to know the following types.

Name | Description | Example
-- | -- | --
`int` | A signed integer (number with no decimal points) | `5`
`double` | A number with a decimal point | `6.7`
`std::string` | Text | `"Hello, this is a string of text!"`

You will be using data types a lot in C++, as you will see.

### Variables

When working in C++, you will encounter the need to hold data in the computer's memory. That is where variables comes in. Variables are specific chunks of the computer's memory that you can use to hold data. To create variables, the following syntax is used:

```c++
type name = initial_value
```
(Yes, this an example of a _statement_, which you will learn in the next section).

Here is a basic breakdown:
- `type` is the name of the data-type of the data that you're going to hold in the variable.
- `name` is the name of the variable. It can pratically be anything you want, with a few rules that I will eventually list below.
- `initial_value` is the value that you would like to assign to the variable when it was first created. Although you _can_ create variables with no initial value, you shouldn't for safety reasons.

As stated above, there are a few rules to what you can name variables. They are:

- It must not begin with a number.
- It must not have spaces in it.
- You cannot use a C++ keyword.

Other than that, there really aren't any rules to naming variables in C++.

To use a variable, simply reference it by name. For example, to add the variable `a` to `b` and assign the result to `c`, do:
```c++
c = a + b
```

### Statements

_Statements_ are really simple: they're just lines of code that does something. What do I mean by doing something? Well, by doing something, I mean _performing a task_. To show you what I mean, here's an example of a statement:

```c++
a = b + c;
```

This statement basically _assigns_ the variable `a` to the sum of the variables `b` and `c`.

Like most other programming languages, C++ runs statements from top to bottom. The statement at the top would run first, and then the next one directly below it, and so on.

Statements are pretty simple, but can also be very complex. Right now, the only rule that you need to know about statements is that **they must end with a semicolon**. If you create a statement that does not end with a semicolon, C++ will get confused and throw a bunch of errors.

### Scopes

A _scope_, sometimes referred to as a _code block_, is simple: a group of statements. Here's an example of a scope:
```c++
{
    statement_1;
    statement_2;
    statement_3;
    statement_4;
    // ...
}
```

You can also declare scopes inside scopes, and so on.

```c++
{
    // ...
    {
        {
            // ..
        }
    }
}
```

As you can see, scopes are a way to group your code. But you might be wondering, why do we even use scopes if they're just for grouping? This is because variables have a special behaviour when you create them in a scope.

Let's say that you create an integer called `neng` in this scope:

```c++
{
    int neng = 5;
    // ...
}
```

Now, here's a question for you: when do you think `neng` would be deleted from memory? Well, `neng` would be deleted _at the end of the scope_. This means that you cannot access variables inside a scope from outside the scope, since the variables would be deleted by the time the scope ends.

### Functions

In C++, code are organized into structures known as _functions_. A function is essentially a block of code that can be executed by either another function or a different program altogether. Unlike in some other languages such as Python or JavaScript, you cannot put most statements outside of functions, with the exception of variable creation statements (shown in the variables section above). Because of this, if your program is going to do more than just declaring a few variables, you will have at least one function.

Here is the syntax for a function:
```c++
return_type function_name(argument_type_1 argument_1, argument_type_2 argument_2, ...)
{
    statement_1;
    statement_2;
    // ...
}
```

This one is quite complex, so let's break it down a little.

- The return type of the function is the type of data that the function is going to return to the code that called the function. If the function does not return anything, the return type would be `void`.
- The function name is the name of the function. It's subjected to the same naming rule as variables are.
- _Arguments_ are basically variables that you can pass to the function when calling it. If your function isn't going to have any arguments, simply leave the argument list blank, like this:
```c++
return_type function_name()
{
    // ...
}
```

Now, you might've noticed the `{` and the `}`. Those are what marks the beginning and end of the function's _body_. The function's body is essentially the group of statements that is going run when the function is called. And yes, function bodies are indeed scopes and variables therefore behaves similarily in a function body as in a scope.

Calling a function is very simple. Here's the syntax:
```c++
function_name(argument_1, argument_2, ...);
```

If the function does not have any arguments, it's even simpler.
```c++
function_name();
```

And finally, to store the return value of the function in a variable, simply do this:
```c++
a = function_name();
```

If you've done programming in other languages before, these syntax should look familiar. 

### Your First Program!

Now, that you've gotten all the basic concepts of C++ (and programming in general), it's time I reveal your first program.

```c++
#include <iostream>

int main()
{
    std::string hello = "Hello, World!\n";
    std::cout << hello;
    
    return 0;
}
```

I'm pretty sure that you understand most of the concepts shown in this program, but we'll break it down line by line for you anyways.

Don't worry about what `#include <iostream>` does for now. Just remember that it's something that you need to put at the top of your program if you want to output anything to the terminal.

`int main()` declares the beginning of the _main function_. Remember how I said that your program needs at least one function for it to do anything? Well, that function is called the main function. It is the function that your operating system calls when you run your program. It **has to be called `main` and it has to return an `int`**, or else your operating system won't be able to find it (though typically C++ will tell you when the main function is missing, and it's usually not happy about it).

> Now, some C++ compilers does support the main function returning `void`, but most doesn't and it's not standard C++, so don't use it.

`{` begins the body of the main function. 

`std::string hello = "Hello, World!\n"` creates a variable (of type `std::string`) named `hello` and assigns the value `"Hello, World!\n"` to it. By the way, if you're wondering what the `\n` thing at the end is, it's something called a _newline character_, which is just fancy programming speak for "put everything after this in a new line".

`std::cout << hello` might look weird if you're used to Python or JavaScript or other languages where the method for outputtting stuff to the terminal is vastly different, but for now just keep in mind that to output stuff to the terminal, you use `std::cout <<` and follow it with whatever you want to print. In this case, we wanted to output the content of the variable `hello` to the terminal.

`return 0;` does exactly what it looks like: it returns the value `0` to the caller. Remember that `main` returns an `int`. If you're wondering why, it's because operating systems have a concept of an _exit code_, which is basically a code that the program returns to the operating system to tell it if it exited successfully or if the program crashed. `0` indicates a successful termination, and anything else indicates a crash. Some operating systems (like Microsoft Windows, for example) ignores the exit code, but others (like most Linux distros and macOS) will show a dialog or a notification or any indicators of the program crashing if the program returns a non-zero value.

And finally, `}` ends the body of the main function and deletes the variable `hello`.

In the next chapter, I'll show you how to install the tools required to do C++ programming on your computer and we'll get into actually compiling and running the program!

[Next Page] (incomplete)