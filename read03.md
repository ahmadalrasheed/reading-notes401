## Reading and Writing Files in Python
![tdd](https://cdn.techbeamers.com/wp-content/uploads/2019/10/Read-Write-File-in-Python-Explained-with-Examples.png)
### What Is a File?

***Before we can go into how to work with files in Python, it’s important to understand what exactly a file is and how modern operating systems handle some of their aspects***

***At its core, a file is a contiguous set of bytes used to store data. This data is organized in a specific format and can be anything as simple as a text file or as complicated as a program executable. In the end, these byte files are then translated into binary 1 and 0 for easier processing by the computer.***

#### Files components

* Header: metadata about the contents of the file (file name, size, type, and so on)
* Data: contents of the file as written by the creator or editor
* End of file (EOF): special character that indicates the end of the file

### Opening and Closing a File in Python

***When you want to work with a file, the first thing to do is to open it. This is done by invoking the open() built-in function. open() has a single required argument that is the path to the file. open() has a single return, the file object:***

>file = open('dog_breeds.txt')

After you open a file, the next thing to learn is how to close it.

**Example:**

>reader = open('dog_breeds.txt')
try:
    # Further file processing goes here
finally:
    reader.close()

## Python Exceptions

***A Python program terminates as soon as it encounters an error. In Python, an error can be a syntax error or an exception. In this article, you will see what an exception is and how it differs from a syntax error. After that, you will learn about raising exceptions and making assertions. Then, you’ll finish with a demonstration of the try and except block.***

### Exceptions versus Syntax Errors

***Syntax errors occur when the parser detects an incorrect statement. Observe the following example:***

>print( 0 / 0 ))
  File "<stdin>", line 1
    print( 0 / 0 ))       ^
SyntaxError: invalid syntax


***The arrow indicates where the parser ran into the syntax error. In this example, there was one bracket too many. Remove it and run your code again:***

>print( 0 / 0)
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
ZeroDivisionError: integer division or modulo by zero

***This time, you ran into an exception error. This type of error occurs whenever syntactically correct Python code results in an error. The last line of the message indicated what type of exception error you ran into.***