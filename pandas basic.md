```python

```


```python
Q1. Create a pandas series that contains the following data: 4,8,15,23 and 42. Then print the series .
Ans - 
     import pandas as pd 
    
    # create a list with 10 elements 
    my_list = [1,2,3,4,5,6,7,8,9,10]
    
    #convert the list to a pandas series
    my_series = pd.seies(my_list)
    
    #print the series
    print(my_series)
    
    output:
        
    0  1
    1  2
    2  3
    3  4
    4  5
    5  6
    6  7
    7  8
    8  9
    9  10
    
    dtype:int64
In this code we first create a list my_list containing 10 elements.Then we use the pd.series()function

    
```


```python
Q2. Create a pandas DataFrame that contains the following list.

Name
Alice
Bob
Claire

Age
25
30
27

Gender
Female
Male 
Female

Then, print the DataFrame.

 Ans -
    
    import pandas as pd 

# create a dictionary containing the data 
data =b {'Name':['Alice','Bob','Claire'],
         'Age':[25,30,27],
         'Gender':['Female','Male','Female']}

# create a pandas DataFrame from the dictionary
df = pd.DartaFrame(data)

# create a pandas DataFrame from the dictionary
df = pd.DataFrame(data)

# print the DataFrame
print(df)

output:
  
       Name      Age      Gender
0  Alice         25       Female
1  Bob           30       Male
2  Claire        27       Female

 In this code, we first create a dictionary datab containing the Name, Age, Gender .Then we used pd.DataFrame
```


```python
Q4. What is 'DataFrame' in pandas and how is it different from pandas. series?Explain with an example.

Ans - 
A DataFrame in pandas is a two-dimentional labeled data structure with columns of potentionally different types.

 A series in pandas , on the other hand , it is a one-dimentional labeled data strutcture with a homogeneous data type
    
     Here is an example to illustrate the difference between the DataFrame and series:
            
            import pandas as pd 
            
    # create a pandas series
    s = pd.Series([1,2,3,4,5])
    
   #create a padas DataFrame
    df = pd.DataFrame({'A':[1,2,3],'B':[4,5,6],'C':[7,8,9]})
    
    # print the series and DataFrame
    print(s)
    print(df)
    
    
    output:
    0  1
    1  2
    2  3
    3  4
    4  5
    dtype:int64
        A  B  C
    0  1  4  7
    1  2  5  8
    2  3  6  9
    
                       
```


```python
Q5. What are some common functions you can use to manipulate data in a pandas DataFrame? can 
you give an example of when you might use one of these functions?
Ans - 
1. head() and tail():Returns the first or last n rows of the DataFrame. This is useful for quickly checking the data

2.describe(): Generates descriptive statistics for numerical columns in the DataFrame, such as count, mean, standard deviation

3.dropna():Removes rows or columns with missing values from the DataFrame. This is useful for cleansing the data

4.groupby(): Groups the data in the DataFrame by one or more columns and applies an aggregate functions, such as sum

5.merge(): combines two or more DataFrames into a single DataFrame based on a column oe index. This is useful 

       Here is an example of head() and tail() functions:
        
        import pandas as pd 
    
    data = {'Name':['JOhn','Jane','Jim','Joan','Jack','Jill','Jerry','Judy','Jacob','Jenna'],
            'Age':[25,30,35,40,45,50,55,60,65,70],
            'Gender':['Male','Female','Male','Female','Male','Female','Male','Female','Male','Female']}
    df = pd.DataFrame(data)
    
    output od df:
        
          Name     Age   Gender
0       John       25    Male
1       Jane       30    Female
2       Jim        35    Male
3       Joan       40    Female
4       Jack       45    Male
5       Jill       50    Female
6       Jerry      55    Male
7       Judy       60    Female
8       Jacob      65    Male
9       Jenna      70    Female
10
```
