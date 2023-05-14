```python
1. Explain why we have to use the Execution class while crafting a custom Exception 
Ans- 
    In python, the built-in 'Exception'class is the base class for all exception. when we create a custom exception , we use class
    
    By inheriting from the 'exception' class our custom exception inherits all the functionally of base class, such as 
    
    in addition , by inheriting from the 'Exception' class, we can make use of the built-in exception hierarchy in python.
```


```python
2.Write a program to print python Exception Hierarchy.
Ans-
     import sys
    
    def print_exception_hierarchy(exc):
        print(type(exc))
        for subclass in exc._subclasses_():
             print_exception_hierarchy(subclass)
                
    print_execution_hierarchy(BaseException)
    
```


```python
3.What errors are defined in the ArithmeticError class? Explain any two with an example.
Ans-
    The 'ArithmeticError' class ia a built-in exception class in python that serves as base for all exception 
    
    1. "ZeroDivisionError":
            This execution is raised when we try to divide a number by zero.
            
        for example:
                     a = 10
                     b = 0
            try:
                    c = a/b
            except ZeroDivisionError:
                print("Error cannot divide by zero")
                
        "overflowError":
            This exception is raised when a calculation exceeds the maximum representable value for a numerical type
            
            foe example:
                         import sys
                         a = sys.maxsize
                        try:
                            b = a * a
                        except OverflowError:
                            print("Error:Result too ;large to represent as a number")
                            
overall , The "ArithmeticError" class and its derived exceptions are useful for handling errors that occurs during arithmetiError

                
```


```python
4. Why LookupError class is used ? Explain with an example keyError and IndexError.
Ans -
    The "LookupError" class is a bulit-in exception class in python that serves as a base class for all exceptions 
    
    1. KeyError:- This exception is raised when a dictionary key i not found in the dictionary.
    
    for example:
                my_dict = {'a':1,'b':2,'c':3}
            try:
                value = my_dict['d']
            except keyError:
                print("Error:key 'd'not found in dictionary")
                
    2.IndexError: This exception is raised when we try to access an index that is out of range for a list or other seqesnce
    
       for example:
                    my_list =  [1,2,3]
                     try:
                         value = my_list[3]
                    except IndexError:
                        print("Error:Index 3 is out of range for list")
                        
                        
```


```python
5. Explain ImportError. What is ModuleNotFoundError?
Ans-
    "ImportError" is a built-in Exception class in python that is raised when an imported module ,package or name cannot
    for example. "ModuleNotFoundError" is a more specific type of "ImportError" that was introduced in python3.6.
    
    #python 3.6 and later
    import foo #eaises ModuleNotFoundError: No module named 'foo'
    
    #python 3.5 and earlier
    import foo #raises ImportError: no module named 'foo'
    
    "ModuleNotFoundError" some other types of "ImportError" that we may encounter include:
        
        1."ImportError:cannot import name"
        2."importError:Dll load fILED"
    
```


      Cell In[2], line 2
        Ans-
            ^
    SyntaxError: invalid syntax




```python
6. List down some best practices for exception handling in python .
Ans-
        1.Catch specific exceptions
        2.Use try-except blocks
        3.Use finally block
        4.Raise exception
        5.provide useful error messages
        6.Log the exceptions
        7.Use context managers
        8.Test exception handling
```
