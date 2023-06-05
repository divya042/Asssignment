```python
#Que1
class password:
    def __init__(self,aa):
        self.aa=aa
    def check(self,*args):
        a=list(self.aa)
        for i in a:
            count1,count2,count3,count4,count5=0,0,0,0,0
            if i == i.upper() and i.isalpha()==True:
                count1 +=1
                continue
            elif i == i.lower() and i.isalpha() == True:
                count2 += 1
                continue
            elif i.isdigit() ==False:
                count3 += 1
                continue
            elif i.isalnum() == False:
                count4 += 1
                continue
        if count1>=2 and count2>=2 and count3>=1 and count4==3 and len(a)==10:
            print("Valid password")
        else:
            print("Invalid password")
        b = input("Enter password")
        passs = password(b)
        passs.check()
```


```python
Invalid password
```


```python
#Que2
# a
a1 = "ABCD"
a = lambda x: "Matched" if x[0]=="A" else " "
print(a(a1))
```

    Matched



```python
# b
a = "12234"
b = lambda x: "Numeric string" if x.isnumeric()==True else" "
print(b(a))
```

    Numeric string



```python
# c
a = [("mango",99),("orange",80),("grapes",1000)]
def sort1(x):
    x.sort(key=lambda x: x[0])
    return x
print(sort1(a))
```

    [('grapes', 1000), ('mango', 99), ('orange', 80)]



```python
# d
a = [i*i for i in range(1,11)]
print(a)
```

    [1, 4, 9, 16, 25, 36, 49, 64, 81, 100]



```python
# e 
a = map(lambda x:x**2,a)
print(list(b))
```


    ---------------------------------------------------------------------------

    TypeError                                 Traceback (most recent call last)

    Cell In[12], line 3
          1 # e 
          2 a = map(lambda x:x**2,a)
    ----> 3 print(list(b))


    TypeError: 'function' object is not iterable



```python
# f
a = int(input("Enter a number:"))
b = lambda x:"Even" if x%2==0 else "Odd"
print(b(a))

```

    Enter a number: 3


    Odd



```python
# g
a = [1,2,3,4,5,6,7,8,9,10]
b = filter(lambda x: x%2!=0,a)
print(list(b))
    
```

    [1, 3, 5, 7, 9]



```python
# h
a = [1,2,3,4,5,6,-1,-2,-3,-4,-5,0]
b = filter(lambda x: x>=0,a)
c = ("Positive Integers:",list(b))
print("Negative Integers:",list(c))
```

    Negative Integers: ['Positive Integers:', [1, 2, 3, 4, 5, 6, 0]]



```python

```
