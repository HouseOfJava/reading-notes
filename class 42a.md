What are dunder methods in Python, and how do they allow for the customization of built-in behavior in classes? Provide an example of a common dunder method and its purpose.

Are special functions in a Python class that allow for the customization fo built-in behaviors. By implementing them into a class , you can define how that class responds to these operations. 
```
class Car:
    def __init__(self, brand, model, year):
        self.brand = brand
        self.model = model
        self.year = year

    def __str__(self):
        return f"{self.brand} {self.model} ({self.year})"

my_car = Car("Toyota", "Camry", 2022)
print(my_car)
```


Explain the concept of an iterator in Python. How do you create a custom iterator using the iter() and next() methods, and why are they important for enabling iteration in a class?

```
class MyRange:
    def __init__(self, start, end):
        self.start = start
        self.end = end

    def __iter__(self):
        return self

    def __next__(self):
        if self.start < self.end:
            current = self.start
            self.start += 1
            return current
        else:
            raise StopIteration()

# Using the custom iterator
my_range = MyRange(1, 5)
my_iter = iter(my_range)

print(next(my_iter))  # Output: 1
print(next(my_iter))  # Output: 2
print(next(my_iter))  # Output: 3
print(next(my_iter))  # Output: 4
print(next(my_iter))  # Output: StopIteration exception
```
By creating a custom iterator, you have fine-grained control over the iteration process in your class. It allows you to define how the elements are generated or accessed, enabling iteration over complex data structures or custom-defined objects.

Iterator is an object that omplements the iterator protocol. It provides a way to access elements of a cllection sequentially, one at a time, without needing to know the structure of the collection. 

What is a generator in Python, and how does it differ from a regular function? Illustrate your answer with an example of a generator function using the ‘yield’ keyword.

A generator is a special type of function that allows you to create iterators in more concise and memory-efficient way. It uses the 'yield' keywordl to define the generator. 
The key difference between a generator function and a regular function is that a generator function returns an iterator object when called, rather than executing the entire function body and returning a single value
```
def fibonacci_generator():
    a, b = 0, 1
    while True:
        yield a
        a, b = b, a + b

# Using the generator function
fibonacci = fibonacci_generator()

print(next(fibonacci))  # Output: 0
print(next(fibonacci))  # Output: 1
print(next(fibonacci))  # Output: 1
print(next(fibonacci))  # Output: 2
print(next(fibonacci))  # Output: 3
```


Define decorators in Python and explain their primary use case. How can you create and apply a custom decorator to a function or method? Provide a simple example to demonstrate this concept.

Are a way to modify or enhance the behavior of functions or methods without directly modifying their source code. Decorators allow you to wrap a function or method with another function, adding additional functionality to the original function's behavior.

```
import time

def timer_decorator(func):
    def wrapper(*args, **kwargs):
        start_time = time.time()
        result = func(*args, **kwargs)
        end_time = time.time()
        execution_time = end_time - start_time
        print(f"Execution time: {execution_time} seconds")
        return result
    return wrapper

@timer_decorator
def my_function():
    # Some time-consuming operation
    time.sleep(2)
    print("Function execution complete.")

my_function()
```

Chatgpt used
