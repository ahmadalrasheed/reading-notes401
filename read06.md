## Random Module in Python

### When to use it?

We want the computer to pick a random number in a given range Pick a random element from a list, pick a random card from a deck, flip a coin etc. When making your password database more secure or powering a random page feature of your website.

### Random functions

#### Randint
Generate integers between two numbers (a,b). The first value should be less than the second.

**Example:**
`import random`

`print random.randint(0, 5)`

**Output:**
This will output either 1, 2, 3, 4 or 5.

#### Random
generates a flot number between 0 and 1 

**Example:**

`import random`

`print(random.random() )`

#### Choice

Generate a random value from the sequence sequence.

**Example :**

`random.choice( ['red', 'black', 'green'] ).`

**output:**
select one of the elements in this list
#### Shuffle

The shuffle function, shuffles the elements in list in place, so they are in a random order.

`from random import shuffle`
`x = [[i] for i in range(10)]`
`shuffle(x)`

**Output:**
[[9], [2], [7], [0], [4], [5], [3], [1], [8], [6]]


## Risk Analysis

risk analysis is the process of identifying the risks in applications or software that you built and prioritizing them to test.


### Why use Risk Analysis?

In any software, using risk analysis at the beginning of a project highlights the potential problem areas. After knowing about the risk areas, it helps the developers and managers to mitigate the risks.

Now, you must know there are certain risks that are unavoidable. I am enumerating them below:

* The time that you allocated for testing

* A defect leakage due to the complexity or size of the application

* Urgency from the clients to deliver the project

* Incomplete requirements

In such cases, you have to tackle the situation with care. Following points can be taken care of:

* Conduct Risk Assessment review meeting

* Use maximum resources to work on high-risk areas

* Create a Risk Assessment database for future use

* Identify and notice the risk magnitude indicators: high, medium, low.

#### Risk magnitude indicators

* High: means the effect of the risk would be very high and non-tolerable. The company might face loss.

* Medium: it is tolerable but not desirable. The company may suffer financially but there is a limited risk.

* Low: it is tolerable. There lies little or no external exposure or no financial loss.

#### Risk Identification
There are different sets of risks included in the risk identification process. Those are as follows:

1. **Business Risks**: This risk is the most common risk associated with our topic. It is the risk that may come from your company or your customer, not from your project.

2. **Testing Risks**: You should be well acquainted with the platform you are working on, along with the software testing tools being used.

3. **Premature Release Risk**: a fair amount of knowledge to analyze the risk associated with releasing unsatisfactory or untested software is required

4. **Software Risks**: You should be well versed with the risks associated with the software development process.


## TestCoverage

Test coverage is a useful tool for finding untested parts of a codebase. Test coverage is of little use as a numeric statement of how good your tests are.

Certainly low coverage numbers, say below half, are a sign of trouble. But high numbers don't necessarily mean much

I would say you are doing enough testing if the following is true:

* You rarely get bugs that escape into production

* You are rarely hesitant to change some code for fear it will cause production bugs.

