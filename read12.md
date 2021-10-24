## Pandas

***Pandas is a python library responisble for Data analysis by giving the suitable tools to deal with it.***

***with padas you can load , analyze , merge ,and join Data , eventhough you can collect data from different databases and analyze them , literally you can do what ever you want with data using pandas.***


### Object creation

***first and before everything we must know how to import pandas.***

>`import pandas as pd`

***using pandas we can create objects contains data in a very reliable and easy way.***

Example:

>`dates = pd.date_range("20130101", periods=6)`
`dates`

Output:

>DatetimeIndex(['2013-01-01', '2013-01-02', '2013-01-03', '2013-01-04',
               '2013-01-05', '2013-01-06'],
              dtype='datetime64[ns]', freq='D')


***if we want to combine these date data with another random numbers for specific amount of coloums  we can do the following:***

`df = pd.DataFrame(np.random.randn(6, 4), index=dates, columns=list("ABCD"))`

We will have :

>                   A         B         C         D
>2013-01-01  0.469112 -0.282863 -1.509059 -1.135632
>2013-01-02  1.212112 -0.173215  0.119209 -1.044236
>2013-01-03 -0.861849 -2.104569 -0.494929  1.071804
>2013-01-04  0.721555 -0.706771 -1.039575  0.271860
>2013-01-05 -0.424972  0.567020  0.276232 -1.087401
>2013-01-06 -0.673690  0.113648 -1.478427  0.524988


Differnce between Numpy and Pandas


***NumPy arrays have one `dtype` for the entire array, while pandas DataFrames have one `dtype` per column.***

***actually `dtype` describes how the bytes in the fixed-size block of memory corresponding to an array item should be interpreted.***

***this bytes that the `dtype` descripes them are the basic unit of information in computer storage and processing. A byte consists of 8 adjacent binary digits (bits), each of which consists of a 0 or 1***


**Example of dtype in pandas :**
`Index(['A', 'B', 'C', 'D'], dtype='object')`



### String Methods



***Series is equipped with a set of string processing methods in the str attribute that make it easy to operate on each element of the array, as in the code snippet below. Note that pattern-matching in str generally uses regular expressions by default (and in some cases always uses them).***

>`s = pd.Series(["A", "B", "C", "Aaba", "Baca", np.nan, "CABA", "dog", "cat"])`
>s.str.lower()

Output:

0       a
1       b
2       c
3    aaba
4    baca
5     NaN
6    caba
7     dog
8     cat

dtype: object



### Grouping


***By “group by” we are referring to a process involving one or more of the following steps:***

* Splitting the data into groups based on some criteria

* Applying a function to each group independently

* Combining the results into a data structure

For example , if we have :

>df = pd.DataFrame(
    {
        "A": ["foo", "bar", "foo", "bar", "foo", "bar", "foo", "foo"],
        "B": ["one", "one", "two", "three", "two", "two", "one", "three"],
        "C": np.random.randn(8),
        "D": np.random.randn(8),
    }
)



**We can use Group by here to group the according to the coloum C And coloum D by the follwoing command:**

`df.groupby("A").sum()`
