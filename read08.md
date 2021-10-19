## List Comprehensions in Python
![](https://www.freecodecamp.org/news/content/images/2021/07/list-comprehension-1.png)
### Syntax

>`my_new_list = [ expression for item in list ]`

Components of it:

* expression we’d like to carry out. expression inside the square brackets.

* Second is the object that the expression will work on

* iterable list of objects to build our new list from

**Example 1: Creating a list with list comprehensions**


>`digits = [x for x in range(10)]`
`print(digits)`

Output:

>`[0, 1, 2, 3, 4, 5, 6, 7, 8, 9]`


### Notes about Lists Comprehensions

* List comprehension methods are an elegant way to create and manage lists. 
* In Python, list comprehensions are a more compact way of creating lists. 
* More flexible than for loops, list comprehension is usually faster than other methods.


### Multiplying Parts of a List
instead of doing this by using loops we can do it by list Comprehensions in a very easy way

**Example 3: Multiplication with list comprehensions**

>`multiples_of_three = [ x*3 for x in range(10) ]`
`print(multiples_of_three)`

**Output:**

>`[0, 3, 6, 9, 12, 15, 18, 21, 24, 27]`


### Lower/Upper case converter using Python

Using list comprehension to loop through a string in Python, it’s possible to convert strings from lower case to upper case, and vice versa. 

**Example 6: Changing a letter’s case**

>`lower_case = [ letter.lower() for letter in ['A','B','C'] ]`
`upper_case = [ letter.upper() for letter in ['a','b','c'] ]`
`print(lower_case, upper_case)`



**Output:**
['a', 'b', 'c'] ['A', 'B', 'C']

### Difference between For loops and list comprehension

>`squares = []`
`for x in range(10):`
    `# raise x to the power of 2`
    `squares.append(x**2)`
`print(squares)`


**Output:**
[0, 1, 4, 9, 16, 25, 36, 49, 64, 81]


**We can do this easly in the list comprehensions ,Example:**

>`squares = [x**2 for x in range(10)]`
`print(squares)`
