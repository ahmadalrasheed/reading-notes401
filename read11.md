## What is Jupyter Lab


***JupyterLab is an interactive development environment for working with notebooks, code and data.***

### Why Jupyter Lab
***JupyterLab provides a high level of integration between notebooks, documents, and activities, bu using JupyterLab we can parse the page into many cells and activate each cell on different type of  implementation.***

***we can combine MardDown text, and codes in a single page but in different cells , and we can see the result for our code instantly by clicking `shift+enter`***

***You can arrange multiple documents and activities side by side in the work area using tabs and splitters. Documents and activities integrate with each other, enabling new workflows for interactive computing.***

***JupyterLab understands many file formats (images, CSV, JSON, Markdown, PDF, Vega, Vega-Lite, etc.) and can also display rich kernel output in these formats. See File and Output Formats for more information.***

***JupyterLab is served from the same server and uses the same notebook document format as the classic Jupyter Notebook.***

#### Commands for jupyter labs

* `b` to start a new cell 
* `c` to copy the cell
* `x`to cut the cell
* `v` to paste the cell
* press on `d` two times to delete the cell
* you can write mark down in the cell by pressing `m`
* you can write code in the cell by pressing `y`


## NumPy Tutorial


***NumPy, which stands for Numerical Python, is a library consisting of multidimensional array objects and a collection of routines for processing those arrays.***


***NumPy is a commonly used Python data analysis package. By using NumPy, you can speed up your workflow, and interface with other packages in the Python ecosystem.***

***NumPy was originally developed in the mid 2000s, and arose from an even older package called Numeric. This longevity means that almost every data analysis or machine learning package for Python leverages NumPy in some way.***




### Lists Of Lists for CSV Data

***Before using NumPy, we’ll first try to work with the data using Python and the csv package. We can read in the file using the csv.reader object, which will allow us to read in and split up all the content from the ssv file.***

`CSV` which is Comma-separated values File format used to store data

first we have to:
1. Import the csv library.
2. Open the winequality-red.csv file
* With the file open, create a new csv.reader object,Pass in the keyword argument delimiter=";" to make sure that the records are split up on the semicolon character instead of the default comma character.
* Call the list type to get all the rows from the file.
* Assign the result to wines.

And here is the following Example :

>`import csv`
`with open('winequality-red.csv', 'r') as f:`
` wines = list(csv.reader(f, delimiter=';'))`


Once we’ve read in the data, we can print out the first 3 rows:

`print(wines[:3])`

and from here we can print all of these data into a table so its easier to read and view then we can calculate all of the information we need from it.


### Numpy 2-Dimensional Arrays

***A 2-dimensional array is also known as a matrix, and is something you should be familiar with. In fact, it’s just a different way of thinking about a list of lists. A matrix has rows and columns. By specifying a row number and a column number, we’re able to extract an element from a matrix.***

***Now we have to convert the list into a NumPy array.***

#### Creating A NumPy Array

* Import the numpy package.
* Pass the list of lists wines into the array function, which converts it into a NumPy array.


>`import csv`
`with open("winequality-red.csv", 'r') as f:`
   ` wines = list(csv.reader(f, delimiter=";"))`
`import numpy as np`
`wines = np.array(wines[1:], dtype=np.float)`


Now , If we display wines, we’ll now get a NumPy array:


>array([[ 7.4 , 0.7 , 0. , ..., 0.56 , 9.4 , 5. ],
[ 7.8 , 0.88 , 0. , ..., 0.68 , 9.8 , 5. ],
[ 7.8 , 0.76 , 0.04 , ..., 0.65 , 9.8 , 5. ],
...,
[ 6.3 , 0.51 , 0.13 , ..., 0.75 , 11. , 6. ],
[ 5.9 , 0.645, 0.12 , ..., 0.71 , 10.2 , 5. ],
[ 6. , 0.31 , 0.47 , ..., 0.66 , 11. , 6. ]])


>wines.shape


**Output:**

`(1599, 12)`









