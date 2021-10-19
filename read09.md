## Dunder (Magic, Special) Methods

### What Are Dunder Methods?

predefined methods you can use to enrich your classes. They are easy to recognize because they start and end with double underscores, for example `__init__` or `__str__.`

instead of calling it `under-under-method-under-under` Pythonistas decided to name it “dunder methods” as a short term

**Example of using dunder method:**

>class LenSupport:
    def `__len__`(self):
        `return 42`
obj = LenSupport()
len(obj)

So now we defined `__len__` as it always have to return 42 , so always it will return 42 for this class

**Output:**

42


#### Object Initialization: __init__

To construct account objects from the Account class I need a constructor which in Python is the __init__ dunder.

**Example:**

>`class Account:`
   ` def __init__(self, owner, amount=0):`
       ` """`
        `This is the constructor that lets us create`
        `objects from this class`
       ` """`
        `self.owner = owner`
        `self.amount = amount`
        `self._transactions = []`


The constructor takes care of setting up the object. In this case it receives the owner name, an optional start amount and defines an internal transactions list to keep track of deposits and withdrawals.


#### Object Representation: __str__, __repr__

* `__repr__`: The “official” string representation of an object. This is how you would make an object of the class. The goal of` __repr__ `is to be unambiguous.

* `__str__`: The “informal” or nicely printable string representation of an object. This is for the enduser.

**Example:**

>`class Account:`
`def __repr__(self):`
    `return 'Account({!r}, {!r})'.format(self.owner, self.amount)`
`def __str__(self):`
        `return 'Account of {} with starting amount: {}'.format(`
           ` self.owner, self.amount)`

If we print them , we will have :

>`str(acc)`
`'Account of bob with starting amount: 10'`

>`print(acc)`
`"Account of bob with starting amount: 10"`

>`repr(acc)`
`"Account('bob', 10)"`


## Python — Probability

### What is probability?
Probability is knowing what is the chance of an event to happen, for example In a coin toss the only events that can happen are: 

* `Flipping a heads`

* `Flipping a tails`

so every one of them the probablity of it to occur is 1/2 , which is the (num-of-face-type-of-coin/number of types).



### Z-score

The Z-score is a simple calculation that answers the question, “Given a data point, how many standard deviations is it away from the mean?” The equation below is the Z-score equation.


![z](https://i.imgur.com/3TuDF4G.jpg)

If a Z-score is 0, it indicates that the data point's score is identical to the mean score

