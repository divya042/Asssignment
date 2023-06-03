```python
#Que1
#def keyword is used to create a function
def get_odd_numbers():
    old_number=[i for i in range(1,260) if i%2!=0]
    return odd_numbers

odd_numbers=get_odd__numbers()
print(odd_numbers)
```


    ---------------------------------------------------------------------------

    NameError                                 Traceback (most recent call last)

    Cell In[2], line 7
          4     old_number=[i for i in range(1,260) if i%2!=0]
          5     return odd_numbers
    ----> 7 odd_numbers=get_odd__numbers()
          8 print(odd_numbers)


    NameError: name 'get_odd__numbers' is not defined



```python
#Que2
#The *args and **kwargs syntax in python functions is used to allow the function a variable number of arguments
# *args is used to pass a variable number of non-keyword arguments to a function.when a function is defined with *args

def print_args(*args):
    for arg in args:
        print(arg)
        
print_args(1,2,3,4,5)

```

    1
    2
    3
    4
    5



```python
#**kargs is used to pass a vraible number of keyword arguments to a function.whe a function is defined with **kwargs

def print_kwargs(**kwargs):
    for key, value in kwargs.items():
        print(f"{key}: {value}")
        
    print_kwargs(a=1, b=2, c=3)
```


```python
#Que3
#In python ,an iterator is an object that can be iterated upon.An object is considered iterable if it defines the_

my_list = [2,4,6,8,10,12,14,16,18,20]

#initialize the iterator object
iterator = iter(my_list)

# use the next() method to retrieve the first five elements
for i in range(5):
    print(next(iterator))
```

    2
    4
    6
    8
    10



```python
#Que4
#A generator function in python is a function that uses the yield keyword to retirn a generato object.Unlike  a normal
#The yield keyword is used to return a value from the generator function and pause its execution until the next value

def even_numbers(n):
    for i in range(2, n+1, 2):
        yield i 
        
# initialize the generator object
even_gen = even_numbers(20)

#use the next() method to retrieve the values
print(next(even_gen))
print(next(even_gen))
print(next(even_gen))
...
```

    2
    4
    6





    Ellipsis




```python

```
