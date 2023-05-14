```python
Q1. What is exception in python? write the difference between Exceptions and syntax errors.
Ans - 
    An exception is an event , which occurs during the execution of a program that disrupts the flow of the program 
    
     Both exception and erros are the subclasses of a throwable class. The error implies the problem that mostly arises
```


```python
Q2. What happens when an exception is not handled? Explain with an example?
Ans- 
    It will cause the program to terminate abruptly and display message to the user, which can lead to data loss or other
    
    Theexception is raised after the finally clause has been excecuted.
    
    Foe example.
    def divided(X,Y):
        return x / y
    
    a = 10
    b = 0
    result = divide(a,b)
    print(result)
    
    This code will raise a 'ZeroDivisionError' because we are trying to divided by zero.
    
```


```python
Q3. Which python statements are used to catch and handle exception? Explain with an example.
Ans- 

     In python ,'try-exception' statements are used to catch and habdle exceptions . The 'try' block contains the code 
    
    for example -
                  x = 10/0
        except ZeroDivisionError:
            print("cannot divide by zero")
            
```


```python
3. Explain with an example .
     a. try and else
     b.finally
     c. raise
    
    Ans-  
        try:
            x = 10/0
        except ZeroDivisionError:
            print("cannot divide by zero")
        elase:
            print("Division Successful")
        finally:
            print("This block always executes")
            raise ValueError("custom error message")
            
    In this example , the 'try ' block attempts to divide the number10 by zero, which raises 'ZeroDivisionError'exception.
    
    since, the execution was caught and handled by the 'except' block, the code in the 'else' block is ececuted, which prints  message
    
    'finally' block is executed , which always runs rahardless of whether an exception was raised or not
```


```python
5.What are custom exception in python? why do need custom Exceptions?Explains with an example.
Ans-
   In python , custom exception are user-defined exceptions that allow you to create and raise your own exceptions in your code.
They are useful when you want to create a specific exception for a particular situations that is not covered by the built- in exceptions.
We need custom exceptions to add more meaning and cintext to the exception raised by our code.By creating custom exceptions.
We can provide more specific and informative error messages that can help with debugging and troubleshooting our code.

Here is an example of how to create and use a custom exception in python.

class Custom Exception(Exception):pass

def divided (a,b);if b==0; raise CustomException("cannot divide by zero")return a/b

try:result = Divide(10,0)except CustomException as e;print(e)

In this example , we define a custom exception called"CustomException" by creating a new class that inherits from build

we then use a 'try- except' block to call the 'divide' function with the arguments 10 and 0.Since the denominator is zero,

overall, this example demonstrate how to create and use a custom exception to handle a specific error condition

```


```python
Q6. create a custom exception class . we use this class to handle an exception.
Ans- 
   class NegativeNumberException(Exception):
   
   def square_root(x)
          if x < 0:
              raise NegativeNumberException("cannot take square root of a negative number")
            return x * *0.5
        try:
            result = square_root(-1)
        except NegativeNumberException as e:
            print(e)
            
    we define a custom exception class called "NegativeNumberException" by creating a new class that inherits from the build
    we define a function called 'square_root' that raises the custom if the input arguments is negative.
    
    we then use 'try-except' block to call the 'square_root' function with the argument-1.since the inputis negativethe 'square_root'
        
            

```
