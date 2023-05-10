```python
Q1.What is MongoDB? Explain non-relational database in short. In which scenarios it is preferred to use
MongoDB over SQL databases?
Ans- 
    MongoDb is a popular document based no SQL database that is designed to be highly scalable and flexible . It is 
Non-relational databases, also lnown as noSQL databases, differ from traditional relational database in that they do 
MongoDB is often preferred over SQL databases in scenarios where there is a need for:
    
1.Flexibility:MongoDB allows developers to work with semi-structured and unstructured data easily , which males it more flexibility

2.Scalability: MongoDB is designed to scale out horizontally , which makes it easy to scale up to handle large amount 

3.Performance:MongoDB can provide better performance tan SQL databases,especially for read-intensive workloads 

4.High availability:MongoDB provides features like replica sets and sharding, wich helps to ensure high availability

5.Real time analytics: MongoDB can provide real-time analytics on large databses,which can helpful for businesses

In summary,MongoDB is a popular noSQL database that is preferred in scenarios where there i a need for flexibility
```


```python
Q2.State and Explain features of MongoDB.
Ans-
    MongoDB is a popular document oriented noSQL database that offers several features that set it apart from traditional
    
1.Flexible data model: MongoDB is a document-oriented database, ehich means the data is stored in flexible JSON-like 

2.scale out architecture: MongoDB supports horizontal scaling, which means that it can easily scale out across multiple

3.Indexing: MongoDB supports secondary indexes , which can be used to improve query performance.It also supports a various 

4.Aggregation Framework: MongoDB has a powerful aggregation framework that allows you to perform complex data processsing

5.Ad hoc queries: MongoDB supports ad hoc queries, which means that you can query your data without define 

6. Automatic sharding: MongoDB can automatically partition your data across multiple servers or nodes, which make it easy

7.Replication and high availability: MongoDb supports replication, which means that ypou can easily create 

```


```python
Q3.Write a code to connect MongoDB to python.Also,create a database and a collection in MongoDB .
Ans-
    import pymongo
    
# connect to MongoDB server 
client = pymongo.MongoClient("mongodb://localhost:27017/")

#create a database
mydb = Client["my database"]

#create a collection
mycol = mydb["customers"]

In this example, we first import the pymongo module,which provides the necessary tools to work with MongoDb . Then, we
Next , we create a new collection named "customes" in the "mydatabases" by calling the client["mydatabase"]metod.If the database does not 
Finally , we create a new collection named "customers"in the "mydatabase" database by calling the mydb["customers"] method


```


```python
Q4.Using the database and the collection  created in question number 3, write a code to insert one record,
and insert many record .Use the find() and _one() methods to print the insert record.
Ans -
      import pymongo
    
    #establish a collection to the MongoDb server
    client = pymongo.MongoClient('mongodb://localhost:27017/')
    
    #create a adatabase a collection
    mydb = client['mydatabse']
    mycol = mydb['customers']
    
    #insert the record
    mydict = {'name':'John','adress':'Highway 37}
    result = mycol.insert_one(mydict)
    print(f"Inserted record with ID:{result.inserted_id}")
              
    # insert many record
    mylist =[
        {'name':'peter','address':'Lowstreet 27'},
        {'name':'Amy','address':'Apple st 652'},
        {'name':'Hannah','address':'Mountain 21'},
        {'name':'Michael','address':'Valley 345'},
        {'name':'sandy','address':'Ocean blvd'},
        {'name':'Betty':'address':'Green Grass 1'},
        {'name':'Richard:'address':''Sky st 331'},
        {'name':'Susan','address':'One way 98'},
        {'name':'Vickey','address':'Yellow Garden 2'},
        {'name':'Ben','address':'Park Lane 38'},
        {'name':'William','address':'Central st 954'},
        {'name':'Chuck','address':'Main road 989'},
        {'name':'Viola','address':'Sideway 1633'}
    ]
    
    result = mycol.insert_many(mylist)
    print(f"Inserted {len(result.inserted_ids)} records")
              
    # find and print the inserted records
    print("Inserted records:")
    for doc in mycol.find():
              print(doc)
              
    #find and print the first inserted record
    print("First inserted record:")
    print(mycol.find_one("_id":result.insertes_ids[0]}))
              
In this example code, we establish a connection to the MongoDB server and create a database called mydatabase.
              
              
```


```python
Q5. Expplain how you can use the find ()method to query the MongoDb database. Write  a simple code to
demonstrate this.
Ans - 
     from pymongo import MongoClient
    
    #connect to the MongoDB server
    client = MongoDB()
    
    #select te database and collection
    db = client.mydatabase
    collection = db.mycollection
    
    # define a query to find all document where the field 'age' is greater than or equal to 18
    query = {"age":{"$gte":18}}
    
    # find all document that mtch the query and print them
    for document in collection . find(query):
        print(document)
        
        In this code example, we first create a connection to e MongoDB server using the MongoClient()method.
        Next, we define a query to find all document where the 'age' field is greater than or equal to 18. we pass this query
        Finally , we loop over the cursor object and print each document that matches the query.
        
    
```


```python
Q6.Explain the sort()method .Give an example to demonstrate sorting in MongoDB.
Ans -
     The sort()method is used in MongoDB to sort the results of a query in ascending or desending order . It can be used
    
    For example:
        from pymongo importClient
        
    #connect to the MongoDB sever
    client = MongoClient()
    
    #select the database and collection
    db = client.mydatabase
    collection = db.students
    
    #sort the documents by name in ascending order
    results = collection.find().sort("name",1)
    
    #print the sorted documents
    for doc in results:
        print(doc)
```


```python
Q7. Explain why delete_one(),and drop() is used.
Ans-
    In MongoDB , the delete_one() and delete_many() methods are used to remove documents from a collection. 
    
The drop() method is used to remove an entire collection from the database. This is sueful when you want to delete all

 For example lets's say we can have a collection called users and want to remove all documents where the status field 
    from pymongo import MongoClient
    
    Client = MongoClient()
    db = client.mydatabase
    users = db.users 
    
    result = users_many({"status";"inactive"})
    
    print(result.deleted_count,"documents deleted")
    
    This code will remove all the documents where the status field id "inactive" and print
    
    If we want to remove the entire users collection , we can use the drop()method:
        
        users.drop()
        
        This code will remove the users collection from the database
```
