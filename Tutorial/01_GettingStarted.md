# Getting Started

This page will instruct the reader on how to start writing C++ programs. The reader will be instructed on how to install and use C++ compilers and a basic "Hello World" program will be shown. This page assumes the reader is familiar with using a computer and is able to install and use programs without much assistance.

## Installing a Compiler

In order to start writing C++ code, there is a specific type of software that must be installed on the reader's computer, known as a _compiler_. A C++ _compiler_ is a program that converts C++ code into machine code, which can then be executed directly by the CPU. The concept of compiling might be unfamiliar for readers who are familiar with high-level programming languages, of which does not require or even have compilers. Converting the code to machine code before execution rather than converting it on the fly is one of the ways C++ achieves better efficiency than interpreted languages like Python or JavaScript.

### Windows

On Windows, the recommended compiler to use is the Visual C++ compiler developed by Microsoft. As of writing, it is currently proprietary and can only run on Windows. However, unlike any other compilers on this list, Visual C++ comes in a package along with an IDE. Because of this, the Visual C++ compiler is a rather large download and can take up a significant amount of disk space. If the reader is currently low on disk space or is actively concerned about disk usage, an alternative would be to use the open-sourced GCC compiler with MSYS2 instead. Microsoft Visual C++ can be downloaded and installed from [here](https://visualstudio.microsoft.com/), while MSYS2 can be found [here](https://www.msys2.org/), with instructions on how to set up GCC.

### macOS

Apple currently recommends using XCode for all C++ development on macOS, but XCode takes up a significant amount of disk space and most of it's features are not relevant to C++. Therefore, it is recommended to install the command line tools instead.

To install the GCC compiler for C++ on macOS, simply open a terminal window and run the `g++` command, which will open a dialog window with a button that one could use to install the command line tools.

### Linux

Most Linux distributions provides packages for the GCC compiler. On most Debian-based systems, the package can be installed through `apt` or `apt-get` and is often called `g++`. The author is unaware of the situation on other Linux distributions, though it should be similar.

## Using the Compiler

Both Microsoft and Apple have created 