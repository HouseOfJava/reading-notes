# Recursion 


Recursion is a programming technique where a function calls itself to perform a specific task. In Python, recursion is implemented by defining a function that calls itself within its own definition

def factorial(n):
    if n == 0:
        return 1
    else:
        return n * factorial(n-1)


Just remember the base stops the recursion and feeds back the argument to resolve the stack. An exdmple of this would be if you had alot of boxes stacked inside of each other but your ruler was very unique and could only measure the original box. You would then need need to define the original box size and use that as the parameter to fidn the remaining box sizes. 
