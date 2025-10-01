# What is Python??
Python is a programming language that combines features of both procedural languages, like C, and object-oriented languages, like Java. 
This blend allows for flexible programming styles.

# History of Python:
Python was developed by Guido Van Rossum in the year 1991 at the Center for Mathematics and Computer Science, managed by the Dutch Government.
Van Rossum was working on a project to develop system utilities in C, where he had to interact with the Bourne shell available in UNIX. He felt the necessity of creating a language that would fill the gap between C and the shell. This has led to the creation of Python.
Van Rossum picked the name Python for the new language from the TV show Monty Python’s Flying Circus. Python’s first working version was ready by early 1990, released it for the public on February 20, 1991. The logo of Python shows two intertwined snakes 

# Features Of Python:
## Simplicity and Readability:
Python's syntax is simple and clear, making it easy to read and understand, similar to reading English sentences.

## Open Source:
Python is free to download and use from www.python.org. Its source code is open, allowing for modification and use in various projects.

## High-Level Language:
It uses English words in its code, making it user-friendly and easy to learn, unlike low-level languages that use machine code.

## Dynamically Typed:
You don't need to declare variable data types explicitly. The type is determined at runtime based on the value assigned. A variable can be assigned an object of one type and later reassigned to an object of a different type.

## Platform Independent and Portable:
Python code is compiled into an intermediate "byte code" which can run on any operating system and hardware using the Python Virtual Machine (PVM). This makes Python highly portable, as a program written once can run on any system with a PVM.

## Object-Oriented and Procedural:
Python supports both procedural programming (using functions and procedures) and object-oriented programming (using classes and objects), giving programmers flexibility.

## Interpreted:
The PVM executes Python's bytecode by interpreting it into machine code line by line.

## Extensible and Embeddable:
You can integrate code from other languages like C, C++, or Java into Python programs. You can also embed Python programs within C or C++ code.

## Huge Standard Library: 
Python comes with a large collection of pre-developed modules and packages, sometimes referred to as "batteries included," which can be used to perform a wide range of tasks easily.
'''
argparse is a package that represents a command-line parsing library 
botois Amazon Web Services library 
CherryPy is an object-oriented HTTP framework 
Cryptography offers cryptographic techniques for programmers 
Fiona reads and writes big data files  
Jellyfish is a library for doing approximate and phonetic matching of strings 
mysql-connector-python is a driver written in Python to connect to a MySQL database 
numpy is a package for processing arrays of single or multidimensional type 
Pandas is a package for powerful data structures for data analysis, time series, and statistics 
Matplotlib is a package for drawing electronic circuits and 2D graphs.  
Pillow is a Python imaging library 
PyQuery represents a jQuery-like library for Python 
scipy is a scientific library to do scientific and engineering calculations 
Sphinx is the Python documentation generator 
Sympy is a package for a Computer algebra system (CAS) in Python 
w3lib is a library of web-related functions 
Whoosh contains a fast and pure Python full-text indexing, search, and spell checking library
''' 

## Database Connectivity:
Python provides interfaces to connect its programs to major databases like Oracle and MySQL.

# Execution of a Python program:
When you run a Python program, it goes through a two-step process: compilation and interpretation.
1. Compilation
A program's code, known as the source code, is first compiled by a Python compiler. The compiler translates the source code into an intermediate code called byte code.
This bytecode is a set of instructions that are platform-independent, meaning they can run on any operating system and hardware. This is what allows Python to be a portable language.
2. Interpretation
The byte code is then executed by the Python Virtual Machine (PVM).
Inside the PVM, an interpreter converts the byte code instructions into machine code that the computer's processor can understand and execute.
The PVM first identifies the computer's processor and operating system to generate the correct machine code, and then the processor runs the code to produce the final output.
While the compiler runs the entire program at once, the interpreter runs the program line by line, making this part of the process slower.

# Execution using command line:
When you execute a Python program from the command line using 
python x.py, you are instructing the Python interpreter to run the file named x.py. This single command handles both the compilation and interpretation of your code. 

# Viewing the Bytecode of a Python program:
You can view Python's bytecode by using the built-in dis module, which acts as a disassembler. This module takes your compiled code and breaks it down into human-readable instructions.

Using the dis Module
To view the bytecode of a function or a module, you can use the dis.dis() function. Here's a simple step-by-step example:

1) Create a Python file, for example, first.py, with the following code:
### Python program to add two numbers
a = b = 10 
print("Sum=", a + b)

2) Open your command line or terminal.
3) Run the dis module on your file using the -m flag:
((C:\>python -m dis first.py))

2  0 LOAD_CONST 0 (10)
   3 DUP_TOP
   4 STORE_NAME 0 (a)
   7 STORE_NAME 1 (b)

3  10 LOAD_NAME 2 (print)
   13 LOAD_CONST 1 ('Sum=')
   16 LOAD_NAME 0 (a)
   19 LOAD_NAME 1 (b)
   22 BINARY_ADD
   23 CALL_FUNCTION 2 (2 positional, 0 keyword pair)
   26 POP_TOP
   27 LOAD_CONST 2 (None)
   30 RETURN_VALUE

# Flavours of Python
Python has several "flavors," or different implementations, each designed to integrate with other programming languages or frameworks. These flavors allow Python code to run on various platforms and interact with different ecosystems.

Common Python Implementations
## CPython:
This is the standard, most widely used Python interpreter. It's written in C and is the version you get when you download Python from python.org. CPython compiles Python code into bytecode and runs it on a PVM built in C. It allows for the execution of C and C++ functions and programs within Python.

## Jython: 
Formerly known as JPython, this implementation is designed to run on the Java platform. The Jython compiler translates Python programs into Java bytecode, which is then executed by the Java Virtual Machine (JVM). This enables the use of both Python and Java libraries.

## IronPython: 
This version is implemented in C# and is specifically for the .NET framework. It compiles Python code into Intermediate Language (IL) that runs on the Common Language Runtime (CLR). IronPython allows developers to use both .NET and Python libraries in their programs.

## PyPy:
This is an implementation of Python written in a subset of Python itself called RPython. A key feature of PyPy is its 

## Just-In-Time (JIT) compiler:
which significantly improves the execution speed of Python programs compared to CPython.

## AnacondaPython: 
This is a specialized distribution of Python that includes a collection of packages for data science, scientific computing, and predictive analytics.

## StacklessPython:
This version of Python focuses on concurrency by using "tasklets," which are small, independent tasks that can communicate via channels.

## RubyPython:
This implementation acts as a bridge between the Ruby and Python interpreters, embedding a Python interpreter inside Ruby applications. 

# Python Virtaul Machine(PVM):
The Python Virtual Machine (PVM) is a crucial component of Python's runtime environment, responsible for executing Python code. It's an abstract layer that sits between Python's bytecode and the underlying hardware, ensuring a consistent environment for running programs across different platforms. The PVM's main function is to translate bytecode into machine code that the computer's processor can execute.

How the PVM Works
The PVM is essentially a loop that continuously interprets and executes bytecode instructions one by one. The process looks like this:

Bytecode Generation: First, your Python source code is compiled into platform-independent bytecode.

Execution Loop: The PVM fetches each bytecode instruction, decodes it, and then executes it sequentially.

Machine Code Translation: The PVM's interpreter handles the conversion of these bytecode instructions into machine code, which is then sent to the computer's processor.

Memory Management: The PVM also manages memory allocation and garbage collection to handle the objects created and used during program execution.

The most common PVM is CPython, which is implemented in C. This architecture is a key reason for Python's portability, as the same bytecode can run on any system with a compatible PVM.

# Frozen binaries in Python:
Frozen binaries in Python refer to single executable files that contain a Python program, the Python Virtual Machine (PVM), and all the necessary libraries to run the program. This allows the end-user to execute the program directly, without needing to install Python or any of its dependencies on their system first.

# Memory Management System in Python:
Python's memory management system handles memory allocation and deallocation automatically, freeing programmers from manual tasks like malloc() or free() in C or C++. 
The system uses a heap to store all objects—such as numbers, strings, lists, and functions—created during a program's runtime. The size of this heap can dynamically increase or decrease based on the program's needs
This process involves several layers:
## Operating System Layer:
The operating system allocates the main memory (RAM) for the program.
## Raw Memory Allocator:
A raw memory allocator sits on top of the OS layer to oversee if enough memory is available on the heap for new objects.
## Object-Specific Allocators:
On top of the raw memory allocator, multiple object-specific allocators apply different memory management policies depending on the type of object being created. For example, the way an integer is stored is different from how a string is stored.

# Garbage Collection
Python's memory management also includes an automatic garbage collector, which is a module named gc. The garbage collector's primary function is to deallocate memory for objects that are no longer in use.
## Reference Counting: 
The simplest way the garbage collector works is by maintaining a reference count for each object. When an object's reference count drops to zero, the collector understands that the object is no longer being used by the program and free up its memory.
## Cycle Detection: 
The garbage collector can also detect "reference cycles," where a group of objects reference each other but are no longer accessible by the program. To prevent these objects from lingering in memory, the garbage collector uses a specific algorithm to find and remove them.
## Generational Collection: 
The garbage collector categorizes objects into three generations. New objects are in generation 0, and if they survive a garbage collection cycle, they are promoted to the next generation. This approach prioritizes collecting newer, short-lived objects over older, more stable ones.

In Python's memory management system, the threshold number is a key value used to determine when the automatic garbage collector should run
### Note:
When more and more objects are created, and if the system runs out of memory, then the automatic garbage collector will not run. Instead, the Python program will throw an exception (runtime error). When the programmer is sure that his program does not contain any reference cycles, then the automatic garbage collector is best suitable.

I can't directly generate or provide images, but I can describe how you can create a visually appealing comparison table or chart for C, C++, Java, and Python. Here's a textual representation of what the comparison might look like, which you can use to design your image:

Comparison Table: C vs C++ vs Java vs Python
Feature
C
C++
Java
Python

Type
Procedural, Middle-level
Object-Oriented, Middle-level
Object-Oriented, High-level
High-level, Interpreted

Speed
Fast (Low-level access)
Fast (Supports OOP)
Moderate (Runs on JVM)
Slower (Interpreted)

Ease of Learning
Moderate (Manual memory management)
Moderate (Complex syntax)
Easy (Simpler syntax, JVM-based)
Very Easy (Beginner-friendly syntax)

Memory Management
Manual (Pointers)
Manual & Automatic (Smart pointers)
Automatic (Garbage Collection)
Automatic (Garbage Collection)

Use Cases
OS, Embedded Systems, Drivers
Game Dev, GUI, System Software
Web Apps, Mobile Apps, Enterprise
AI, ML, Data Science, Web Dev

Platform Dependency
Platform-dependent
Platform-dependent
Platform-independent (via JVM)
Platform-independent

Community Support
Strong
Strong
Very Strong
Very Strong

# Installation of Python on Windows:
(https://www.youtube.com/watch?v=ddGTXBhaGWA)
Download the Installer: Go to the official Python downloads page for Windows and download the latest stable version of Python 3. The website will usually recommend the appropriate 64-bit or 32-bit installer for your system.

1) Run the Installer: Double-click the downloaded .exe file to run the installer.

2) Crucial Step - Add to PATH: On the first screen of the installer, it is very important to check the box that says "Add python.exe to PATH". This step allows you to run Python from the Command Prompt or PowerShell, making it easier to use.

3) Install Now: Select "Install Now" to proceed with the default installation. This will install Python, pip (the package installer), IDLE (Python's Integrated Development and Learning Environment), and other useful tools.


4) Complete Installation: The installer will show a progress bar and then a "Setup was successful" message.

5) Verify the Installation: Open the Command Prompt or PowerShell and type python --version. Press Enter. If the installation was successful, you will see the version number of Python you just installed.

## Installing various packages in Python:
pip install (numpy/pandas/xlrd/seaborn/matplotlib)
## Verfying various packages in Python:
pip list
help('modules')

# Execution of Python program:
You can execute a Python program in three main ways:
## 1. Python's Command Line Window:
This is an interactive mode where you type Python code one line at a time. The Python Virtual Machine (PVM) executes each line as soon as you press Enter.

## 2. Python's IDLE Graphics Window
This is also an interactive mode, but it provides a graphical user interface (GUI). You can type and run code line by line, similar to the command line window. IDLE also allows you to write and save multi-line programs in a separate editor window.

## 3. Directly from the System Prompt
This is a non-interactive mode where you run a complete program file at once. After writing your code in a text editor and saving it with a .py extension, you open your system's command prompt, navigate to the file's directory, and execute it using the python command.

# Command line commands:
#### To Change Directory:
C:\>f: 
F:\>cd py 
F:\PY> 
#### Display contents of directory:
F:\PY>dir 
#### Create Directory:
To create a new directory, use the mkdir command followed by the desired name. For example, mkdir new_folder creates a folder named "new_folder".
#### Remove Directory: 
To delete an empty directory, use rmdir (on Windows) or rm -r (on macOS/Linux). Be cautious with this command as it permanently deletes files
#### To execute a text file in Python:
F:\PY>python first.py 
#### To close the cmd:
F:\PY>exit  
# Getting Help in Python:
Python Programming
Custom Gem
You can get help in Python through several built-in mechanisms and online resources.

1. The help() function
Python's built-in help() function provides a quick way to access documentation for modules, keywords, or topics directly from the interpreter.

To enter help mode: Simply type help() at the Python prompt (>>>help(numpy)) and press Enter. The interpreter will enter a help utility where you can type the name of a module, keyword, or topic to get more information. To exit this mode, type quit.

For specific help: You can also get help on a particular object directly from the interpreter by typing help('object_name') or help(object_name). For example, help('print') will show you the documentation for the print() function.

2. The dir() function
The dir() function returns a list of all the names (attributes, methods, etc.) in the current scope or for a given object. It can be useful for exploring modules or classes and discovering what functions are available.

3. Online Documentation
Python has comprehensive official documentation available online at docs.python.org. This resource includes tutorials, a language reference, and a standard library reference, offering extensive information on all Python features. You can access this directly from IDLE by navigating to Help > Python Docs.
