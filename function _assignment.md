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



###Question : 3 Describe how to access, modify, and delete elements in a list with examples. 

### Accessing Elements

Use indexing to retrieve elements. Indexing starts at 0.

```python
fruits = ['apple', 'banana', 'cherry']
first_fruit = fruits[0]  # 'apple'
last_fruit = fruits[-1]  # 'cherry'
```

### Modifying Elements

Assign a new value to a specific index to change an element.

```python
fruits = ['apple', 'banana', 'cherry']
fruits[1] = 'blueberry'  # Change 'banana' to 'blueberry'
```

### Deleting Elements

1. **Using `del` keyword:**

   ```python
   fruits = ['apple', 'banana', 'cherry']
   del fruits[1]  # Remove 'banana'
   ```

2. **Using `pop()` method:**

   ```python
   fruits = ['apple', 'banana', 'cherry']
   removed_fruit = fruits.pop(1)  # Remove 'banana'
   ```

3. **Using `remove()` method:**

   ```python
   fruits = ['apple', 'banana', 'cherry']
   fruits.remove('banana')  # Remove the first occurrence of 'banana'
   ```

4. **Using list comprehension:**

   ```python
   fruits = ['apple', 'banana', 'cherry']
   fruits = [fruit for fruit in fruits if fruit != 'banana']  # Remove 'banana'
   ```

These methods allow you to efficiently handle elements in a list.

###Question : 4 Compare and contrast tuples and lists in example.


Tuples and lists are both used to store collections of items, but they have some key differences. Here's a comparison with examples:

1. Mutability
Lists are mutable: You can change their contents (e.g., add, remove, or modify elements).
Tuples are immutable: Once created, their contents cannot be changed.
Example:
python
Copy code
# Lists
my_list = [1, 2, 3]
my_list[0] = 10  # Modifying an element
my_list.append(4)  # Adding an element
print(my_list)  # Output: [10, 2, 3, 4]

# Tuples
my_tuple = (1, 2, 3)
# my_tuple[0] = 10  # This will raise a TypeError
# my_tuple.append(4)  # This will raise an AttributeError
2. Syntax
Lists use square brackets [].
Tuples use parentheses ().
Example:
python
Copy code
# List
my_list = [1, 2, 3]

# Tuple
my_tuple = (1, 2, 3)
3. Performance
Tuples generally have a slight performance advantage over lists because they are immutable. They use less memory and can be faster for iteration.
Lists are more flexible but have a bit more overhead due to their mutability.
Example:
python
Copy code
import sys
import timeit

# Measuring memory size
list_size = sys.getsizeof([1, 2, 3])
tuple_size = sys.getsizeof((1, 2, 3))

print(f"Size of list: {list_size} bytes")
print(f"Size of tuple: {tuple_size} bytes")

# Measuring iteration speed
list_time = timeit.timeit('for i in [1, 2, 3]: pass', number=1000000)
tuple_time = timeit.timeit('for i in (1, 2, 3): pass', number=1000000)

print(f"List iteration time: {list_time}")
print(f"Tuple iteration time: {tuple_time}")
4. Use Cases
Lists are suitable when you need a collection of items that may change over time. They are commonly used when the order of elements is important and you may need to update the collection.
Tuples are suitable for fixed collections of items. They are often used for heterogeneous (different types) data where the content shouldn't change, like storing coordinates or function return values.
Example:
python
Copy code
# List (mutable)
shopping_list = ['milk', 'bread', 'eggs']  # Can be changed as needed

# Tuple (immutable)
coordinates = (40.7128, -74.0060)  # Latitude and longitude; shouldn't change
5. Methods
Lists come with several methods for modification (e.g., append(), remove(), extend()).
Tuples have fewer methods because they are immutable (e.g., count(), index()).
Example:
python
Copy code
# List methods
my_list = [1, 2, 3]
my_list.append(4)  # Add element
my_list.remove(2)  # Remove element
print(my_list)  # Output: [1, 3, 4]

# Tuple methods
my_tuple = (1, 2, 3, 2)
print(my_tuple.count(2))  # Count occurrences of 2
print(my_tuple.index(3))  # Find index of 3
In summary:

Lists: Mutable, flexible, more methods, suitable for changing collections.
Tuples: Immutable, slightly faster and memory-efficient, suitable for fixed collections.






## 2. Practical 


### Practical 1  Sum of Even Numbers in a List

```python
def sum_even_numbers(numbers):
    return sum(num for num in numbers if num % 2 == 0)

# Example usage
numbers = [1, 2, 3, 4, 5, 6]
print(sum_even_numbers(numbers))  # Output: 12


```


