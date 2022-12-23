# Getting Started

Since you are reading this tutorial, I am assuming that you have a basic idea of what C++ is and what it's intended to be used for, so I'm not going to bore you with a bunch of theory and just jump right into the fun stuff. Because of this, 

## Installing a compiler

Computers can only understand a single language, and that is machine code. Therefore, any program that is written in human-readable code has to be converted into machine code in order to be executed. In C++, this process is known as _compilation_, and is performed by a program known as a _compiler_. Therefore, in order to run C++ code on your computer, you first need to install a C++ compiler.

There are many different compilers to use, depending on what operating system you are running on, but this tutorial will simply use the recommended compiler for each operating system.

### Windows

On Windows, the recommmended compiler is the Microsoft Visual C++ compiler. It is part of Microsoft's Visual Studio development suite, which includes the Visual Studio IDE, but can be installed all on it's own as well. Visual Studio is a very powerful IDE and definitely should be considered by any C++ developer, but for the sake of platform consistency this tutorial will not be using Visual Studio. Plus, the overhead of running an full-featured IDE may be too heavy for some readers.

To install the Microsoft Visual C++ compiler, head to [this link](https://visualstudio.microsoft.com/downloads/#tools-for-visual-studio-2022-family) and download the Build Tools for Visual Studio. After that, follow the onscreen instructions to install the Desktop Development with C/C++ workload. Then, you will have successfully installed Microsoft's Visual C++ compiler.

### Linux

On Linux, the recommended compiler is `g++`. Installing it should be rather straightforward, as most distributions provides a package that contains it (if you're using Linux, you should definitely know how to install packages). On Ubuntu (and maybe Debian?) based systems, the package name is `g++`.

You may also prefer the `clang++` compiler instead, but in the scope of this tutorial, the two compilers are practically equivalent and can interop bidirectionally (at least on Linux-based systems) so there isn't much of a point. But, if you still prefer `clang++`, you can use it as well, though the remainder of this section will use `g++`.

### macOS

On macOS, the recommended compiler is `clang++`. There are several methods to install `clang++` on macOS, but from my understanding if you just run the command `clang++` in a terminal, the operating system will prompt you to install the compiler. You can also use Homebrew if you want but [carpetmaker3162](https://github.com/carpetmaker3162) reports that it doesn't always work all of the time. Plus, I don't really have much experience developing on macOS in general which is the main reason why I placed this section at the bottom, so I'm probably not the right person to take advice from in regards to C++ development on macOS.

## Hello, World!

Alright, now that you have installed a compiler on our system, it is time for you to write your first program! Start by opening a text editor and writing the following code.

```cpp
// Make the compiler aware of the symbols defined in the 'iostream' header file
// .
#include <iostream>

// Define the main function, which returns an int. The return value of the main
// function in C++ is the exit code of the program, which can indicate either
// a successful exit or a crash.
auto main() -> int
{
    // Print out the text "Hello, World!" to the console.
    std::cout << "Hello, World!\n";
    
    // Returns the exit code 0 to the operating system. An exit code of 0 indi-
    // cates that the program has exited successfully.
    return 0;
}
```

We will break this down and explain it later on, but for now, don't worry too much about how it works.

Save your code somewhere where you will remember. C++ code files (known as _source files_) are often saved with a `.cpp` extension. Some people uses `.cxx` as well. Honestly, it doesn't really matter what file extension you use for your C++ source files but I tend to prefer the `.cpp` extension.

For the remainder of this tutorial, I will assume that you have saved the code file under the name `helloworld.cpp`.

### Compiling and Running Your Program

Now that you have written your first program, it is time to compile and run it. Please note that this is the only time I will walk you through compiling and running a C++ program, as the process is pretty much the same for much of the rest of the tutorial.

**Windows**

On Windows, you first need to open a developer console. The easiest way to do is by going to the start menu and searching for "Developer Powershell for VS 2022". This will open up a developer shell with all the required commands registered.

Next, navigate to the directory in which you have saved the `.cpp` file. Once you are there, run the following command.

```powershell
cl /W4 /std:c++20 /EHsc helloworld.cpp
```

Here's a basic breakdown of the command.
- `cl` is the name of the command.
- `/W4` tells the compiler to increase the warning level. This is so that compiler can catch common mistakes during compile time and warn you about it.
- `/std:c++20` tells the compiler that we want to compile under the C++20 standard, which is the latest stable standard of C++. The compiler might already be set to compile under C++20 by the time you are reading this but this isn't the case so far.
- `/EHsc` is added to ensure that exceptions works correctly. If you don't care much about exceptions don't worry too much about this one for now.
- `helloworld.cpp` is the name of the source file that you would like to compile.

Please note that if you have saved your `.cpp` file as anything other than `helloworld.cpp`, replace `helloworld.cpp` with the filename that you have saved it as.

Anyways, this will create a file called `helloworld.exe` in the same directory. This is the file that contains the compiled program. To run it, simply type `./helloworld` and hit enter.

If you did everything correctly, you should get the following output.

```
Hello, World!
```

**Linux and macOS**

On Linux (or macOS), simply open up a shell and navigate to the directory in which you have saved your source file.

On Linux, run the following command. On macOS, run the same command, but replace `g++` in the beginning with `clang++`.

```bash
g++ -std=c++20 -Wall -pedantic -o helloworld helloworld.cpp
```

Here's a basic breakdown of the command.
- `g++` is the name of the command. If you are using `clang++`, this is obviously, well, `clang++`.
- `std=c++20` tells the compiler that we want to compile under C++20. `g++` still doesn't do that by default.
- `-Wall` increases the warning level so that the compiler can warn us about common mistakes during the compilation process.
- `-pedantic` tells `g++` to warn about any non-standard C++ code. There are few cases in which `g++` will be able to compile code that are considered illegal in the C++ standard. For the sake of consistency with other platforms, we've decided to disable such behaviour.
- `-o helloworld` tells the compiler to write the compiled result of the program to a file named `helloworld`.
- `helloworld.cpp` is the name of the source file that the compiler needs to compile.

If this command produces no output, it indicates succcess and should produce a file called `helloworld` in the current working directory. To run it, simply run `./helloworld`.

Congratulations, you have written and compiled your first C++ program! Go to the next section to learn more about the C++ language itself.
