# Getting Started

This page will instruct the reader on how to start writing C++ programs. The reader will be instructed on how to install and use C++ compilers and a basic "Hello World" program will be shown. This page assumes the reader is familiar with using a computer and is able to install and use programs without much assistance.

## Installing a Compiler

In order to start writing C++ code, there is a specific type of software that must be installed on the reader's computer, known as a _compiler_. A C++ _compiler_ is a program that converts C++ code into machine code, which can then be executed directly by the CPU. The concept of compiling might be unfamiliar for readers who are familiar with high-level programming languages, of which does not require or even have compilers. Converting the code to machine code before execution rather than converting it on the fly is one of the ways C++ achieves better efficiency than interpreted languages like Python or JavaScript.

### Windows

On Windows, the recommended compiler to use is the Visual C++ compiler developed by Microsoft. As of writing, it is currently proprietary and can only run on Windows. However, unlike any other compilers on this list, Visual C++ comes in a package along with an IDE. Because of this, the Visual C++ compiler is a rather large download and can take up a significant amount of disk space. 

If the reader is currently low on disk space or is actively concerned about disk usage, an alternative would be to use the open-sourced GCC compiler with MSYS2 instead. 

Microsoft Visual C++ can be downloaded and installed from [here](https://visualstudio.microsoft.com/), while MSYS2 can be found [here](https://www.msys2.org/), with instructions on how to set up GCC.

### macOS

Apple currently recommends using XCode for all C++ development on macOS, but XCode takes up a significant amount of disk space and most of it's features are not relevant to C++. Therefore, it is recommended to install the command line tools instead.

To install the GCC compiler for C++ on macOS, simply open a terminal window and run the `g++` command, which will open a dialog window with a button that one could use to install the command line tools.

### Linux

Most Linux distributions provides packages for the GCC compiler. On most Debian-based systems, the package can be installed through `apt` or `apt-get` and is often called `g++`. The author is unaware of the situation on other Linux distributions, though it should be similar.

## Compiler Usage

This section will inform the reader on the basic usage of the GCC compiler and Microsoft's Visual Studio IDE. Please note that this section will simply discuss the compiler features needed to compile the listings in this tutorial. For a more comprehensive list of the compilers' features, feel free the consult their documentation.

### GCC

Some readers might wanted to check the version of GCC that they are using. To do so, run

```bash
g++ --version
```

`g++` is the C++ compiler for GCC. There is also the `gcc` command which can be used to compile C programs, but that is outside the scope of this tutorial.

To write and compile a program with GCC, first write out the program in a plain text editor and save it with an `.cpp` extension. The `.cpp` extension is not strictly necessary, but it is a common practice used by many C++ developers and will be important when working with certain _build systems_ (like CMake) later on. 

Assuming the program is saved as `hello-world.cpp`, it can be compiled with GCC by running

```bash
g++ hello-world.cpp
```

This will produce an executable file called `a.exe` (`a.out` on macOS and Linux-based systems) in the directory in which the command was ran. 

It is possible to change the name of the produced executable by using the `-o` option.

```bash
g++ hello-world.cpp -o hello-world
```

This command will produce an executable named `hello-world`. It should be noted that on Windows-based systems an `.exe` extension will be automatically added.

By default, `g++` will show very few (if any) compiler warnings, but they can (and should be) enabled by using the `-Wall` option.

```bash
g++ -Wall hello-world.cpp -o hello-world
```

The `g++` command has many more options and parameters that the reader can explore with, but this is all that is needed to compile most of the basic C++ programs shown in this tutorial.

### Microsoft Visual Studio

In Visual Studio, programs are organized into _projects_, each of which contains all of the code files of the program in question.

Creating a project in Visual Studio is relatively straightforward, and as a result, this tutorial will not guide the reader through the process. Please note that almost all of the code listed in this tutorial should be compiled in the form of Console Apps.

To compile a progam in Visual Studio, make sure the project is open and simply press Ctrl+B, but this is unnecessary as Visual Studio usually automatically compiles the program.

To run a program in Visual Studio, press Ctrl+F5.

## Hello World Program

It is a tradition for most computer science students to write a program that outputs the text "Hello World!" in some ways when learning an new language. This tutorial will follow that tradition.

### GCC

To start, open a plain text editor and type in the following text.

```cpp
#include <iostream>

int main()
{
    std::cout << "Hello World!\n";
    return 0;
}
```

Save the file as `hello-world.cpp`.

Next, open a terminal in the directory in which the file is saved in and compile the program using the following command.

```bash
g++ -Wall hello-world.cpp -o helloworld
```

This will produce an executable file called `hello-world` (`hello-world.exe` on Windows-based systems) in the current directory, which can be executed by running the following command. Please note that appending an `.exe` extension might be necessary on some Windows-based systems for it to work.

```bash
./hello-world
```

Which should produce the following output.

```
Hello World!
```

### Microsoft Visual Studio

Start by creating a new Console App project and give it the name "HelloWorld". Upon project creation, the "Hello World" program should be created automatically by the IDE. To run the program, simply press Ctrl+F5, and a console window should appear with the text "Hello World" in it.

Currently, as of right now, it is likely that the reader has little to no understanding of the Hello World program, but most of the concepts within it will soon be explained in futures chapters.

[Next Page](02_Data.md)