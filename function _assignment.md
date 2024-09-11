#  Functions Assignments

## 1. Theory



### Question : 1 What is the difference between a function and a method in python?
Ans : Function: A function is an independent block of code that is not associated with any object.
You can define a function using the def keyword, and it can be called by its name anywhere in the program. 

```python
def minakshi(name):
    return f"Hello, {name}!"
print(minakshi("Sachin"))

```
Method : A method is a function that is associated with an object, typically defined inside a class.  And operates on the data (attributes) contained in the object it is associated with. It implicitly takes the instance (self) of the object as its first parameter
```python
class mina:
    def __init__(self, name):
        self.name = name
    
    def minakshi(self):
        return f"Hello, {self.name}!"

greeter = mina("Sachin")
print(mina.minakshi())

```






### Question : 2 Explain the concept of function arguments and parameters in python
Ans : In Python, parameters are the variables listed in a function’s definition, while arguments are the actual values passed to the function when it is called. Parameters define what inputs the function expects, and arguments provide those inputs during execution. There are several types of arguments in Python, including positional arguments, keyword arguments, default arguments, and variable-length arguments. Positional arguments are passed in order, while keyword arguments use parameter names. Default arguments provide fallback values. Variable-length arguments allow passing an arbitrary number of values using *args (for tuples) and **kwargs (for dictionaries). 

```python
# Parameters: 'a' and 'b'
def add(a, b):  
    return a + b

# Arguments: 5 and 10
result = add(5, 10)  
print(result)  # Output: 15


```















## 2. Practical 


### Practical 1  Sum of Even Numbers in a List

```python
def sum_even_numbers(numbers):
    return sum(num for num in numbers if num % 2 == 0)

# Example usage
numbers = [1, 2, 3, 4, 5, 6]
print(sum_even_numbers(numbers))  # Output: 12


```


