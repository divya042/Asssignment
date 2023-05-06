```python
Q1.List any five functions of the pandas . Library with execution 
Ans- 

1.read_CSV():This function reads a CSV file and returns a DataFrame:
                import pandas as pd 
                df = pd.read_csv('filename.csv')
2.head(): This function displays the first n rows of a DataFrame (by default n=5).
                 df.head()
3.info(): This function provides information about a DataFrame, such as the number of rows and columns, data types and memory
                 df.info()
4.groupby(): This function groups the DataFrame by one or more columns and returns a GroupBy object.
                 grouped = df.groupby('column_name')
5.describe(): This function generates descriptive statistics of a DataFrame, such as count, mean and standard deviation.
                 df.describe()

```


```python
Q2.Given a pandas DataFrame df with column 'A','B' and 'C' write a python function to re-index the 
DataFrame with a new index that starts from 1 and increments by 2 for each row.
Ans- 
       import pandas as pd 
    
 def reindex_dataframe(df):
     new_index = pd.Index(range(1,2*len(df)+1,2)) # create a new index
     df = df.set_index(new_index) # set new index
     return df 
    
 This function creates a new index using the pd.Index() function with a range that starts from 1 and increments by 2 for each 

To use this function on a DataFrame with columns 'A','B' and 'c', you would simply call it like this:
    
df = pd.DataFrame({'A':[1,2,3],'B':[4,5,6],'C':[7,8,9]})
df = reindex_dataframe(df)
print(df)

This would output the following DataFrame:
    
    A  B  C
   1  1  4  7
   3  2  5  8
   5  3  6  9

 As youn can see, the DataFrame has been re-indexed with a new index that starts from 1 and increments by each two row

    
```


```python
Q3.You have a pandas DataFrame fd with a column named 'Values' . write a python function that 
iterates over the DataFrame and calculates the sum of the first three in the 'Values' column. The 
function should be print the sum to the console.
Ans -

def sum_first_three_values(df):
    total=0
    for i , row in df.iterrows():
        if i<3:
            total+=row['Values']
            print("sum of the first three 'Values' column:",total)
            
This function iterates over the DataFrame using the iterrows() function, which returns a pair of index and row data for each 

To use this function on a DataFrame df with column named 'Values', you woulf simply call it like this:
    
      df = pd.DataFrame({'Values':[10,20,30,40,50]})
      sum_first_three_values(df)
    
 This would output:
    
    sum of the first three values in 'Values' column:60
    
As you can see, the function correctly calculates and prints the sum of the first three values in the 'Values' column 

    
    
```


```python
Q4. Given a pandas DataFrame df with a column 'Text', write a python function to create a new column
'Word_Count' that contains the number of words in each row of the 'Text' column.
Ans- import pandas as pd 
   
     def count_words(df):
         df['Word_Count'] = df['Text'].apply(lambda x: len(str(x).split(" ")))
        
This function creates a new column 'Word_Count' by using the apply() function on the 'Text' column .The lambda function pass

To use this function on a DataFrame df with a column 'Text', you would simply call it like this:
    
    df = pd.DataFrame({'Text':['This is the first row','second row contains more words ','Third row with even more words']})
    df = count_words(df)
    
This would output:
    
     Text Word_Count
    0            This is the first row              5
    1        second row contains more words         5
    2     Third row contains even more words here   7
    
```


```python
Q5.How are DataFrame.size() and DataFrame.shape() different?
Ans- 

        1.DataFrame.size() returns the total number of elements in the DataFrame,which is equal to the number of rows multiplication

        2.DataFrame.shape() returns a tuple thatcontains the number of rows and columns in the DataFrame.The first element of 
        
        here is an example of to illustrate the difference:
            
        import pandas as pd
        
        df = pd.DataFrame({A':[1,2,3],'B':[4,5,6],'C':[7,8,9]})
        print("DataFrame size:",df.size)
        print("DataFrame shape:",df.shape)
                           
    This would output:
        
    DataFrame:9
    DataFrame shape:(3,3)

 As you can see ,the DataFrame.size() method returns the total number of elements in the DataFrame,which is 9

```


```python
Q6.  Which function of pandas do we use to read and excel file?
Ans- 
    The function of pandas that we used to read an Excel file is read_excel(). The function can read data from an excel file
    
    import pandas as pd 
    
    #Read Excel file into a pandas DataFrame
    df = pd.read_excel('example.xlsx')
    
    # Display the DataFrame
    print(df)
    
    In thi example , the read_excel() function reads the data from the Excel file named example.xlsx and creates a DaaFrame object
    
    you can also specify the sheet name (or index) from which you want to read data using the sheet_name parameter.For example
    
       import pandas as pd 
        
        
        
    # Read data from sheet named 'sheet1' in the Excel file
    df = pd.raed_excel("example.xlsx',sheet_name='Sheet1')
                       
    # Display the DataFrame
    print(df)
                       
    In this example, the read_excel() function reads data from the sheet named 'Sheet1'in the Excel file
```


```python
Q7. You have a pandas DataFrame df that contains a column named 'Email' that contains email
addresses in the format 'username@domain.com'.write a python function that creates a new column
'username' in df that contains only the username part of each email address. 

The username is the part of the email adress that appears before the '@' symbol. For exmple , if the function 
should extract the username from each email address and store it in the new 'Username'column.

Ans- 
    to extract the username from each email address in a pandas DataFrame df that contains as 'Email' column, you can use
    
    Hewre is a python function that creates a new column 'Username' in th DataFrame df that contains only the username part of 
    
      def extract_username(df):
      #split the 'Email' column into two parts : the username and the domain
      df[['Username','domain']] = df['Email'].str.split('@',expand=True)
        
      #Return the updated DataFrame
      return df
     
    In this function , the str.split() method is used to split the 'Email' column of the DataFramerame df into two parts:the username
    
    After the split , the 'Username'column contains the username part of each email address and the 'Doamin column contains
    
      import pandas as pd 
    
    # create a simple DataFrame
    df = pd.DataFrame({'Email':['john.doe@example.com','jane.doe@example.com','james.smith@example.com']})
    
    # call the function to extract the usernames
    df = extract_username(df)
    
    #Display the updated DataFrames
    print(df)
    
    this woulf output:
           Email              Username     Domain
    0 john.doe@example.com    john.doe     example.com
    1 jane.doe@example.com    jane.doe     example.com
    2 james.smithQ@example.com james.smith example.com
    
    
    As you can see, functions has created a new 'Username' column in the DataFrame df that contains only the usernme part
```


```python
Q8. You have a pandas DataFrame df with columns 'A','B', 'C'.write a python function that selects all rows where 
the value in column 'A' is greater than 5 and the value in column 'B' is less than 10. The function should 
return a new DataFrame the following value:
A  B  C
0  3  5  1
1  8  2  7
2  6  9  4
4  9  1  2

Your function should select the following rows:A B C
1  8  2  7
4  9  1  2
 Ans - 
    
To select all rows where the value in column 'A' is greater than 5 and the value in column 'B' is less than 10 in a pandas

def select_rows(df):
    #Use boolean indexing to select rows where 'A'> 5 and 'B' < 10
    return selected_rows

In this function , the [(df['A'] . 5) & (df['B'] <10)] syntax is used to select only the rows where the value in column 'A'

After the selection, the selected_rows DataFrame contains only the selected rows. YOu can then return this new 
Dataframe.

Here is an example of how to use this function:
 
import pandas as pd 

# create a sample DataFrame
df= pd.DataFrame({'A':[3,8,6,2,9],
                  'B':[5,2,9,3,1],
                  'C':[1,7,4,5,2]})

#call the function to select the rows
selected_rows = select_rows(df)

# Display the selected rows 
print(selected_rows)
  
    
 This would output:
  A  B  C
  1  8  2  7
  4  9  1  2
 As you can see, the function has selected only the rows where thw value in coumn 'A' is greater than 5 and the value in column 'B' is less than 10
    
    

```


```python
Given a pandas DataFrame  df with a column 'Values', write a python function to calculate the mean , median, 
and standard deviation of the values in the 'Values' column .
Ans - 
    To calculate the mean, median and standard deviation of the values in the 'Values' column of a pandas DataFrame df 
    
    def calculate_stats(df)
      #calculates the mean , median and standard deviation of the 'values column 
      mean = df['Vslue'].mean()
      median = df['Values'].median()
      std_dev = df['Values'].std()
    
    # print the statistrics to the console
    print("Mean:",mean)
    print("Median:",median)
    print("Standard deviation:", std_dev)
    
I this function , the ,ean(), median(),and std() methods are used to calculate the mean, median and standard deviation

 After calculating these statistics, the function prints them to the console using the print() function.
     
Here is an example of how to use this function:
    
import pandas as pd 

#create a sample DataFrame
df = pd .DataFrame({'Vlues':[10,20,30,40,50]})

# call the function to calculate the statistics 
calculate_stats(df)

 This would output:
        
    Mean:30.0
    Median:30.0
    Standard deviation:15.8113008496
    
    As you can see . the function has calculated the mean , median and  standard deviation 
    
```


```python
Q10. Given a pandas DataFrame df with a column 'Sales' and a column 'Date', write a python function to create a new 
column 'MovingAverage'that contains the moving average of the sales for the past 7 days for each row in the 
DataFrame. The moving average shoulf be calculated using a window of size7 and should include the current day.
Ans - 
     to calculate a new column 'MovingAverage' in a pandas DataFrame df that contains the moving average of the sales for the prize
    
    def calculate_moving_average(df):
        # calculate the moving average of the 'sales' column with a window of size 7
        ma = df['Sales'].rolling(window=7,min_periods=1).mean()
        
        #add the moving average as a new column in the DataFrame
        df['MovingAverage']=ma
        
        #Returned the modified DataFrame
        return df
    In this function , the rolling ()method is used to create a rolling window of size 7 for the 'Sales' column
    
    The resulting moving average is then added as a new column 'MovingAverage' in the DataFrame using the df['MovingAverage']
    
     Finally the modified DataFrame is returned from the function.
        
        Here is an example of how to use this function:
            import pandas as pd 
            
    # create a sample DataFrame 
    df = pd.DataFrame({'Sales':[10,20,30,40,50,60,70,80,90,100],
                       'Date':pd.date_range(start ='2022-01-01',periods = 10, freq = 'D')})
    
    
    # call the function to calculate the movin average
    df = calculate_moving_average(df)
    
    #print the modified DataFrame with the  new 'Moving Average' column 
    print(df)
    
    This would output:
        
        
    0       10 2022-01-01  10.000000
    1       20 2022-01-02  15.000000
    2       30 2022-01-03  20.000000
    3       40 2022-01-04  25.000000
    4       50 2022-01-05  30.000000
    5       60 2022-01-06  35.000000
    6       70 2022-01-07  40.000000 
    7       80 2022-01-08  45.000000
    8       90 2022-01-09  50.000000
    9       1002022-01-10  55.555556
    
```


```python
Q11.You have a pandas DataFRme of with a column 'Date'. write a python function  that creates the moving 
average of the column 'Weekday' in the DataFrame. The 'Weekday' column  should contains  the weelday name(e. g.
 For example , if  df cotains  the following  values:
  Date
   0 2023-01-01
   1 2023-01-02
   2 2023-01-03
   3 2023-01-04
   4 2023-01-05                                                                                                     
    Your function should create the following DataFrame:
 Ans- 
     import pandas as pd 
     
   def add_weekday(df):
        df['weekday'] = df['Date'].dt.strftime('%A')
        return df 
        
The dt accessor allows you to access the datatime properties of a pandas series, and strftime formats the datetime value as 
 you can call this function with your pandas DataFrame df as an argument:
    
df = pd.DataFrame({'Date':['2023-01-01', '2023-01-02','2023-01-03','2023-01-04','2023-01-05']})
df['Date'] = pd.to_datetime(df['Date'])
df = add _weekday(df)
print(df)
 
This will output the modified DataFrame with the weekday column:
        date               weekday                                                                                   
 0 2023-01-01              sunday
 1 2023-01-02              monday
 2 2023-01-03              tuesday
 3 2023-01-04              wednesday
 4 2023-01-05              thursday
                                                                                                          
```


```python
Q12.Given a pandas DataFrame df with a column 'Date' that contains timestamps, write a python function
to select all the rows where the data is between '2023-01-01' and '2023-01-31'
Ans- 

 between() function of pandas to selct all rows where the date is between '2023-01-01' and '2023-01-31 
     Here is the
    
    import pandas as pd 

def select_rows_by_date(df):
    start_date = '2023-01-01'
    end_date = '2023-01-31'
    mask = (df['Date'] >= start_date) & (df['Date'] <= end_date)
    return df.loc[mask]
You can pass your DtaFrame df to this function and it will return a new DataFrame that contains only the rows 
```


```python
Q13. TO use the basic functions of pandas , what is the first and farmost necessary library that needs to be imported?

Ans -
    The first and formost necessary library that needs to be imported to use the basic functions of pandas itself
    
          import pandas as pd 
```
