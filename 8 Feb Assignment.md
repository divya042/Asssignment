```python
#Que1
"""Abstraction is used to hide internal functionality of function from the user .user will be able to see the function 
"""Here we have created a abstract method "st" Then we have inherited te base class "student" in subclasses "std1"
from abc import ABC, abstractmethod
class student(ABC):
      @abstractmethod
      def st(self,a,b):
          pass
class std1(student):
      def st(self,a,b):
          return a 
class std2(student):
      def st(self,a,b):
          return b
x = std1()
x.st(2,3)
```


      Cell In[5], line 3
        """Here we have created a abstract method "st" Then we have inherited te base class "student" in subclasses "std1"
           ^
    SyntaxError: invalid syntax




```python
1
```


```python
#Que2
"""Abstraction is used to hide internal functionality of function from user while encaptulation is used to rest 
"""Example-The school class is a abstarct class with abstract method result.when this class is inherited into subclass
   never invoked only the child class method is invoked.Abstract class acts like a standard interface for other class
In class class1 we are encapsulating the variable by using "__"as prefix which stops it to be accessed rather we
to hidden variables."""

from abc import ABC,absractmethod
class school(ABC):
     @abstractmethod
     def result(self,res):
         pass
class school1(school):
     def result(self,res):
         return res
class class1:
     def __init__(self,a):
        self.__a=a
     def seta(self,b):
        self.__a = b if>0 else a
     def geta(self):
        return self.__a
        
        
x = school()
print("Abstraction:", x.result(78))
y = class1(34)
y.seta(23)
print("Encaptulation:",y.geta())
```


      Cell In[7], line 6
        to hidden variables."""
                            ^
    SyntaxError: unterminated triple-quoted string literal (detected at line 29)




```python
Abstraction: 78
Encaptulation: 23
```


```python
#Que3
#ABC module stands for abstract base class module.It makes the inherited subclasses bind to apply methods declared 
```


```python
#Que4
#We can achieve data abstraction by importing ABC and abstractmethod from abc module.Abc is to be passes through
```


```python
#Que5
""" we cannot create an instance from abstract class. """
""" Abstract class works like template for developing the code .It is of no use other than this hence it cannot be 
from abc import ABC,abstractmetod
class Aircraft(ABC):

    @abstractmethod 
    def fly(self):
        pass
a = Aircraft()
```


      Cell In[8], line 3
        """ Abstract class works like template for developing the code .It is of no use other than this hence it cannot be
        ^
    SyntaxError: incomplete input




```python

```
