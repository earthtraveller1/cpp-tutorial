# Data

Data manipulation is essential to almost any task in programming, whether it be serving web pages to a client or rendering graphics on a screen. Because of this, most languages includes functionalities for operating with data as fundamental components of the language, and C++ is no exception. This page will introduce the reader to basic C++ features for data storage, management, and manipulation.

## Stacks and Heaps

Like many other programming languages, C++ has a concept of both a _stack_ and a _heap_. All data are allocated on the stack by default unless otherwise stated. There are several ways to allocate data on the heap, but such methods are quite advanced and won't be introduced in this page.

### Stack

The stack is organized similarly to a physical stack in the way that they are both *first in, last out*. This means that data allocated on the stack are deallocated in the reverse order in which they are allocated in. Unlike on the heap, data allocated on the stack do not need any form of explicit deallocation, as they will be automatically deallocated when they reach the end of their *scope*.

Because C++ is a statically typed language, the type *and* size of all stack-allocated data must be known at compile time. 