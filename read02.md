## In Tests We Trust — TDD with Python
![tdd](https://www.thinktocode.com/wp-content/uploads/2018/02/red-green-refactor.png)
### Unit tests and TDD?

***Unit tests are some pieces of code to exercise the input, the output and the behaviour of your code. You can write them anytime you want.***
***But Test-Driven Development is a strategy to think (and write!) tests first.***

#### The Cycle

***🆘 Write a unit test and make it fail (it needs to fail because the feature isn’t there, right? If this test passes, call the Ghostbusters, really)***
***✅ Write the feature and make the test pass! (you can dance after that)***
***🔵 Refactor the code — the first version doesn’t need to be the beautiful one (don’t be shy)***

## What does the if __name__ == “__main__”: do?

***Before executing code, Python interpreter reads source file and define few special variables/global variables.***
***If the python interpreter is running that module (the source file) as the main program, it sets the special` __name__ `variable to have a value `“__main__”`. If this file is being imported from another module, `__name__` will be set to the module’s name. Module’s name is available as value to `__name__` global variable.***

***A module is a file containing Python definitions and statements. The file name is the module name with the suffix .py appended.***

#### Advantages : 

* Every Python module has it’s `__name__` defined and if this is `‘__main__’`, it implies that the module is being run standalone by the user and we can do corresponding appropriate actions.

* If you import this script as a module in another script, the `__name__` is set to the name of the script/module.

* Python files can act as either reusable modules, or as standalone programs.

* if `__name__` ==` “main”`: is used to execute some code only if the file was run directly, and not imported.


## Recursion

### What is Recursion? 

***The process in which a function calls itself directly or indirectly is called recursion and the corresponding function is called as recursive function. Using recursive algorithm, certain problems can be solved quite easily. Examples of such problems are Towers of Hanoi (TOH), Inorder/Preorder/Postorder Tree Traversals, DFS of Graph, etc.***

**Example:**

>int fact(int n)
{
    if (n < = 1) // base case
        return 1;
    else    
        return n*fact(n-1);    
}

