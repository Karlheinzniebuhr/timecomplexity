## Pythonbenchmark

<h6>The Python library that makes benchmarking easy and fun</h6>
#pip install pythonbenchmark  
The timeit module that comes with python is only useful for small bits of Python code not for functions.
<hr>
This library solves that. It provides an intuitive way to measure the execution time of functions and compare the relative speed of two functions.
<hr>
Optimizing your code? Curious how much speed you gained? No problem
<hr>
Pythonbenchmark allows this by letting you compare two functions which take the same input and measure which one gets the job done faster.
<hr>
<h4>@measure</h4>
Additionally you can just put a decorator on the functions, pythonbenchmark will measure them and print out the execution time in the console.

How to use:
Import pythonbenchmark.py

The typical use case could be: You have functionX, and optimized functionX. Now you want to know if your modified version is faster and how much.

```python
from pythonbenchmark import compare, measure
import time

a,b,c,d,e = 10,10,10,10,10
something = [a,b,c,d,e]

def myFunction(something):
	time.sleep(0.4)

def myOptimizedFunction(something):
	time.sleep(0.2)

# comparing test
compare(myFunction, myOptimizedFunction, 10, input)
```

<h4>Output</h4>
![alt tag](https://github.com/Karlheinzniebuhr/pythonbenchmark/blob/master/images/test_compare.PNG)


Measuring execution time with the @measure decorator
```python
from pythonbenchmark import compare, measure
import time

a,b,c,d,e = 10,10,10,10,10
something = [a,b,c,d,e]

@measure
def myFunction(something):
	time.sleep(0.4)

@measure
def myOptimizedFunction(something):
	time.sleep(0.2)

myFunction(input)
myOptimizedFunction(input)

```
<h4>Output</h4>
![alt tag](https://github.com/Karlheinzniebuhr/pythonbenchmark/blob/master/images/test_decorator.PNG)

<hr>
<h3>TODO</h3>
Adding support to compare multiple functions maybe? 
Any ideas are welcome

[![Analytics](https://ga-beacon.appspot.com/UA-37427094-2/Karlheinzniebuhr/pythonbenchmark/)](https://github.com/igrigorik/ga-beacon)
