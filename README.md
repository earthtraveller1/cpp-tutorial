# Introduction

Hello, and welcome to this C++ tutorial! This tutorial will help you learn the C++ programming language. Of course, the best way to learn C++ is by writing C++ programs and gaining experience, which you are probably going to do after going through this tutorial. I would also suggest that you work through the examples listed in this tutorial, as one of the best ways to learn anything is by doing it!

## What is C++?

In short, C++ is a general-purposed compiled programming language. _General-purposed_ means that the language isn't specialized and can be used for pretty much anything. _Compiled_ means that the program that you write in C++ is converted to machine code, which is stored in a file, before it is ran.

C++ is a very powerful and versatile language, and is used in a majority of desktop applications, embedded devices, and servers. Most other programming languages have their foundations built by either C (a subset of C++ (kind of)) or C++. C++ pretty much forms the very fundamentals of modern computing, whether you like it or not.

The areas in which C++ is used the most are either to create interpreters for other programming languages or to create software that demands either high performance or direct, low-level access to hardware components. One of the most common applications of C++ is in game engines, as game engines demands very high performance and requires access to the graphics card to render frames. Desktop applications are also often written in C++, as they often have to integrate well with the rest of the system, which is often written also in C++.

C++ is currently a very popular language and definitely worth learning. However, C++ can indeed be hard to learn for some people (like Anthony Huang and Neng Li from the Li Institution), which is why C++ programmers are sometimes considered "programming masters".

## Basic Concepts

Before writing your first program in C++, you first need to familiarize yourself with some basic concepts in C++. This is because your first program is going to utilise a lot of C++ concepts, which is going to look very confusing if you don't understand them first.

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
Here is a basic breakdown:
- `type` is the name of the data-type of the data that you're going to hold in the variable.
- `name` is the name of the variable. It can pratically be anything you want, with a few rules that I will eventually list below.
- `initial_value` is the value that you would like to assi

As stated above, there are a few rules to what you can name variables. They are:

- It must not begin with a number.
- It must not have spaces in it.
- You cannot use a C++ keyword.

Other than that, there really aren't any rules to naming variables in C++.

### Functions

In C++, code are organized into structures known as _functions_. A function is essentially a block of code that can be executed by either another function or a different program altogether. Unlike in some other languages such as Python or JavaScript, you cannot put _statements_ (You'll learn about them later) outside of functions.

// Note: this tutorial is not finished, as shown by the incomplete nature of this page. Check back here later.