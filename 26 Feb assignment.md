```python
#Que1
import numpy as np

list_ = ['1','2','3','4','5']
array_list = np.array(object=list_)
```


```python
#Yes,there is a difference in the data type of variables list_ and array_list.list_is a python list object,while_array

```


```python
type(list_)
```


```python
list
```


```python
type(array_list)
```


```python
numpy.ndarray
```


```python
#Que2
list_ = ['1','2','3','4','5']
array_list = np.array(object=list_)
```


```python
# Each element is string class
for i in list_:
    print(type(i))
```


    ---------------------------------------------------------------------------

    NameError                                 Traceback (most recent call last)

    Cell In[3], line 2
          1 # Each element is string class
    ----> 2 for i in list_:
          3     print(type(i))


    NameError: name 'list_' is not defined



```python
# Each element is numpy_string class
for i in array_list:
    print(type(i))
```


    ---------------------------------------------------------------------------

    NameError                                 Traceback (most recent call last)

    Cell In[4], line 2
          1 # Each element is numpy_string class
    ----> 2 for i in array_list:
          3     print(type(i))


    NameError: name 'array_list' is not defined



```python
#Que3
#array_list = np.array(object = list_,dtype = int)
```


```python
list_ = ['1','2','3','4','5']
array_list = np.array(object = list_,dtype = int)
```


```python
# Each element is string class
for i in list_:
    print(type(i))
```


    ---------------------------------------------------------------------------

    NameError                                 Traceback (most recent call last)

    Cell In[5], line 2
          1 # Each element is string class
    ----> 2 for i in list_:
          3     print(type(i))


    NameError: name 'list_' is not defined



```python
# Each element is numpy_integer class
for i in array_list:
    print(type(i))
```


```python
"""The first loop will print the data type of each element in list_,which will be <class 'str'>,since all the time elements

The second loop will print the data type of each elemnt in array_list, which will be <class 'nimpy.int64'>
```


```python
"The first loop will print the data type of each element in list_,which will be <class 'str'>,since all the elements in list
st_ are strings.\n\nThe second loop will print the data type of element in array_list, which will be <class 'numpy.int64
4'>,since all the elements in array_list are now integers due to the dtype=int parameter passed to the np.array() function
n."
```


```python
#Que4
import numpy as np 
num_list = [ [ 1 , 2 , 3 ], [ 4 , 5 , 6 ] ]
nummm_array = np.array(object = num_list)
```


```python
#(i) shape of num_array
#The shape attribute of a numpy array returns a tuple containing

num_array.shape
```


```python
(2 , 3)
```


```python
#(ii) size of num_array
#The size attribute of a NUmpy array returns the total number of elements in the array.

num_array.size
```


```python
6
```


```python
#Que5
a=np.zeros((3,3))
```


```python
np.array([[0,0,0],[0,0,0],[0,0,0]])
```


```python
a
```


```python
array([[ 0., 0., 0],
       [0., 0.,  0]'
       [0., 0.,  0.]])
```


```python
array([[0, 0, 0],
       [0, 0 ,0],
       [0, 0 ,0]])
```


```python
a.shape
```


    ---------------------------------------------------------------------------

    NameError                                 Traceback (most recent call last)

    Cell In[7], line 1
    ----> 1 a.shape


    NameError: name 'a' is not defined



```python
(3,3)
```


```python
9
```


```python
#Que6
a=np.eye(5,5)
```


```python
a
```


```python
array([[1.,0.,0.,0.,0.],
       [0.,1.,0.,0.,0.],
       [0.,0.,1.,0.,0.]'
       [0.,0.,0.,0.,1.]])
```


```python
a.shape

```


```python
(5,5)
```


```python
a.size
```


```python
25
```


```python

```
