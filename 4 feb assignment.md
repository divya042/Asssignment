```python
#Q.1.
list_of_tuples = [('Sachin Tendulkar',34357), ('Ricky Ponting',27483),('Jack Ksllis' ,25534), ('Virat Kohli' ,24936)]
                  
# Using the lambda function to sort the list of tuples based on the second element of the tuple 
sorted_list = sorted(list_of_tuples ,key=lambda x: x[1])
                  
print("Sorted list of tuples:",sorted_list)
```

    Sorted list of tuples: [('Virat Kohli', 24936), ('Jack Ksllis', 25534), ('Ricky Ponting', 27483), ('Sachin Tendulkar', 34357)]



```python
#Que2
l=[1,2,3,4,5,6,7,8,9,10]
list(map(lambda x:x**2,1))
```


    ---------------------------------------------------------------------------

    TypeError                                 Traceback (most recent call last)

    Cell In[7], line 3
          1 #Que2
          2 l=[1,2,3,4,5,6,7,8,9,10]
    ----> 3 list(map(lambda x:x**2,1))


    TypeError: 'int' object is not iterable



```python
#Que3
l1=[1,2,3,4,5,6,7,8,9,10]
tuple(map(lambda x:str(x),l))
```




    ('1', '2', '3', '4', '5', '6', '7', '8', '9', '10')




```python
#Que4
l=[i for i in range(1,26)]
```


```python
l
```




    [1,
     2,
     3,
     4,
     5,
     6,
     7,
     8,
     9,
     10,
     11,
     12,
     13,
     14,
     15,
     16,
     17,
     18,
     19,
     20,
     21,
     22,
     23,
     24,
     25]




```python
from funtools import reduce
```


```python
reduce(lambda x,y:x*y,l)
```


```python
#Que5
l2= [2,3,6,27,60,90,120,55,46]
list(filter(lambda x:x%2==0 and x%3==0,12))

```


    ---------------------------------------------------------------------------

    TypeError                                 Traceback (most recent call last)

    Cell In[13], line 3
          1 #Que5
          2 l2= [2,3,6,27,60,90,120,55,46]
    ----> 3 list(filter(lambda x:x%2==0 and x%3==0,12))


    TypeError: 'int' object is not iterable



```python
#Que6
l3=['python','php','aba','radar','level']
list(filter(lambda x:x==x[::-1],l3))
```
