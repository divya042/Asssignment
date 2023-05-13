```python
Q1. What is a database ? differentiate between sql and nosql database.
Ans - 
       A database is a organized collection of data can be accessed , managed and updated.Databases are used to store 
    
    SQL databases , also known as relational databases, store data in tables with predefined column and rows. 
    
    nosql databases , do not use tables with predefined columns and rows . they store data in a verity of ways , such as key 
    Examples of nosql databases include MongoDB , Cassandro and Redis.
    
    Nosql databases are better suited for real-time applications,SQL databases are typically have better support for
    The choice between SQL and Nosql and SQL databses on the specific needs of the application and data being stored.
      
    
```


```python
Q2.What is DDL? Explain why CREATE,DROP,ALTER and TRUNCATE re used with an example.
Ans-
      DDL standas for Data Definition language , which is a subset of SQL used to define and manage the strutcture of data 
    
    Here are some common DDL statements and their uses:
        
        1.CREATE:statements is used to create a new databse object, such as table or index. For example. The following
        
               CREATE TABLE employee(
                            id INT primary key,
                            name VARCHAR(50),
                            salary DECIMAL(10,2)
               );
            
            2.DROP;This statement is used to delete an existing database object such as table or index.For example.
            
                     DROP TABLE employee;
            
            3.ALTER:This statement is used to modify an existing database object, such as table or column .For example
            
                          ALTER TABLE employee ADD COLUMN department VARCHAR(50);
                
            4.TRUNCATE:This statement is used to remove all the data from a table , while leaving the table structure
                          
                          TRUNCATE TABLE employee;
                
               
                            
```


```python
3.What is DML? Explin INSERT, UPDATE, AND DELETE with a example.
Ans-
     DML stands for Data Manupulation Language, which is subject of SQL used to manipulate data in databses.DML statement
    
    1.INSERT: This statement is used to insert new into a table.
            INSERT INTO employees(id, name, salary)VALUES(1,'JOHN Doe', 50000);
        
    2.UPDATE:This statement is used to upadate existing data in a table . For example the following statement update
            UPDATE employee SET salary = 55000 WHERE id = 1;
        
    3.DELETE:This statement is sued to delete existing data from a table. For example, The following statement deletes 
            DELETE FROMemployee WHERE id = 1;
        
        
```


```python
Q4. What is DQL? Explain SELECT with ana example.
Ans-
   DQl stand for Data QUERY Language, which is subset of SQL used to retrive data from databases . DQL statement are used
    
    The most common SQL statement is SELECT .
       SELECT from employees;
        
            This statement selects all column from the "employees" table and rows in the table . The 
            
            SELECT id, name , salary FROM employee WHERE salary>50000;
            
            this statemens selects the "id","name" and "salary" columns from the "employees" table and returns only rows 
    
```


```python
Q5. Explain primary key and foreign key.
Ans-
     A primary key is a unique identifier for a record or row ina a database table. It is used to ensure that each row in 
     A primary key is a column or set of column that are selected to identify ecah row in atable . It must be unique
        
     A foreign key is afield in a table that is used to referenec the primary key of another table. It is used to establish
     The foreign key column must have the same data type and size as the primary key column it refreneces , ots volues must 
        
        
```


```python
Q6. Write a python code to connect Mysql to python. Explain the cursor()and execute() method.
Ans-
    To connect Mysql to python , we need to use a apython Mysql connector. The most common python Mysql connectorb is the 
    e.g. 
        import mysql.connector
        
        # establish connection to Mysql
        
        mydb = mysql.connector .connect(
            host = "localhost",
            user = "username"
            password = "password",
            database = "databse_name"
        )
         #create a cursor object
            
         mycursor = mydb.cursor()
         
         #exexute a SQL query 
         mycursor.execute("SELECT * from table_name")
            
         #fetch all rows from the query resut
         myresult = mycursor.fetchall()
            
         # print the result
         for row in myresult:
                print(row)
                
        We create a cusrsor object the 'cursor()' method of the connection object. The cursor objecrt is used to execute SQL 
        The 'exexute()' method of the cursor object is used to execute a SQL query . we pass the query as a parameter
            
            
```


```python
Q7. Give the order of execution ofbSQL clauses in a SQL query 
Ans -
     1.'FROM'clauses: This clause specifies the table(s) from which data is retrieved.
    
     2.'JOIN'clauses: If there are any joins in the query , they are executednext.This clause specifies how tables are joins 
        
    3. 'WHERE'clauses: This clause is used to filter the data based on specified conditions.
    
    4."GROUP BY"clause : This clause is used to group the dtaa based on specified column.
    
    5.'HAVING'clause: This clause is used to group created by the 'GROUP BY'clause baed on specified conditions.
    
    6.'SELECT' clause: This clause is used to select the columns that will be included in the result set.
    
    7.'DISTINCT'clause: If the query includes the 'DISTICT' keywords , duplicates in the result set are removed at this state
    
    8.'ORDER BY' clause: This clause is used to sort the result set based on specified columns.
    
    9.'LIMIT' and 'OFSET'clauses:If specified , these clauses are used to limit the number pf rows returned by the query 
```
