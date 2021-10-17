## Python Scope & the LEGB Rule

### Modifying the Behavior of a Python Scope

### The global Statement and Why we use global ?


***You already know that when you try to assign a value to a global name inside a function, you create a new local name in the function scope. To modify this behavior, you can use a global statement. With this statement, you can define a list of names that are going to be treated as global names.***

***The statement consists of the global keyword followed by one or more names separated by commas. You can also use multiple global statements with a name (or a list of names). All the names that you list in a global statement will be mapped to the global or module scope in which you define them.***

**Here’s an example where you try to update a global variable from within a function:**


>>>> `counter = 0  # A global name`
>>> `def update_counter():`
...    ` counter = counter + 1  # Fail trying to` `update counter`

***When you try to assign counter inside update_counter(), Python assumes that counter is local to update_counter() and raises an UnboundLocalError because you’re trying to access a name that isn’t defined yet.***

***If you want this code to work the way you expect here, then you can use a `global` statement as follows:***


 `counter = 0  # A global name`
>>> `def update_counter():`
...     `global counter  # Declare counter as global`
...    ` counter = counter + 1  # Successfully update the counter`


***You can also use a global statement to create lazy global names by declaring them inside a function. Take a look at the following code:***

>>> `def create_lazy_name():`
...     `global lazy  # Create a global name, lazy`
...     `lazy = 100`
...    ` return lazy`
...
`create_lazy_name()`
100
`lazy  # The name is now available in the `
global scope
100

### The nonlocal Statement

***nonlocal names can be accessed from inner functions, but not assigned or updated. If you want to modify them, then you need to use a `nonlocal `statement. With a nonlocal statement, you can define a list of names that are going to be treated as nonlocal.***

***The nonlocal statement consists of the `nonlocal `keyword followed by one or more names separated by commas. These names will refer to the same names in the enclosing Python scope. ***
**Example:**

>>>`def func():`
...     `var = 100  # A nonlocal variable`
...     `def nested():`
...        ` nonlocal var  # Declare var as nonlocal`
...         `var += 100`
...
...    ` nested()`
...    ` print(var)`
...
`func()`
`200`


***if we tried to use it in the global scope Error will occur:***

>>>`nonlocal my_var  # Try to use nonlocal in the global scope`
  `File "<stdin>", line 1`

***In contrast to global, you can’t use nonlocal to create lazy nonlocal names. Names must already exist in the enclosing Python scope if you want to use them as nonlocal names.***


**Finally,to under stand the difference between both of them you can see the following picture:**

![](https://www.pythontutorial.net/wp-content/uploads/2020/11/Python-nonlocal-Scopes-nonlocal-variable-lookup.png)