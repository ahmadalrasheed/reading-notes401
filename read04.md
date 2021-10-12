## Classes and Objects

***Objects are an encapsulation of variables and functions into a single entity. Objects get their variables and functions from classes. Classes are essentially a template to create your objects.***

>class MyClass:
    variable = "blah"
    def function(self):
        print("This is a message inside the class.")

### Accessing Object Variables

>class MyClass:
    variable = "blah"
    def function(self):
        print("This is a message inside the class.")
myobjectx = MyClass()
myobjectx.variable


## Thinking Recursively in Python

### Recursive Functions in Python

***Now that we have some intuition about recursion, let’s introduce the formal definition of a recursive function. A recursive function is a function defined in terms of itself via self-referential expressions.***

***This means that the function will continue to call itself and repeat its behavior until some condition is met to return a result. All recursive functions share a common structure made up of two parts: base case and recursive case.***

***To demonstrate this structure, let’s write a recursive function for calculating n!:***

* Decompose the original problem into simpler instances of the same problem. This is the recursive case:

>n! = n x (n−1) x (n−2) x (n−3) ⋅⋅⋅⋅ x 3 x 2 x 1
n! = n x (n−1)!

* As the large problem is broken down into successively less complex ones, those subproblems must eventually become so simple that they can be solved without further subdivision. This is the base case:

>n! = n x (n−1)! 
n! = n x (n−1) x (n−2)!
n! = n x (n−1) x (n−2) x (n−3)!
⋅
⋅
n! = n x (n−1) x (n−2) x (n−3) ⋅⋅⋅⋅ x 3!
n! = n x (n−1) x (n−2) x (n−3) ⋅⋅⋅⋅ x 3 x 2!
n! = n x (n−1) x (n−2) x (n−3) ⋅⋅⋅⋅ x 3 x 2 x 1!


**Example:Recursive function for calculating n! implemented in Python:**

>def factorial_recursive(n):
    # Base case: 1! = 1
    if n == 1:
        return 1
    # Recursive case: n! = n * (n-1)!
    else:
        return n * factorial_recursive(n-1)
        factorial_recursive(5)
