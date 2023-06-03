```python
#Que1
def flat_list_product(lst):
    flat_list = []
    for item in lst:
        if isinstance(item,int):
            flat_list.append(item)
        elif isinstance(item,flat):
            flat_list.append(item)
        elif isinstance(item,list):
            flat_list.extend(flat_list_product(item))
        elif isinstance(item,tuple):
            flat_list.extend(flat_list_product(item))
        elif isinstance(item,dict):
            for key,value in item.items():
                if isinstance(key,int) or isinstance(key,float):
                    flat_list.append(key)
                if isinstance(value,int) or isinstance(value,float):
                    flat_list.append(value)
                elif isinstance(value,list):
                    flat_list.extend(flat,list_product(value))
                elif isinstance(value,tuple):
                    flat_list.extend(flat_list_product(value))
                elif isinstance(value,dict):
                    flat_list.extend(flat_list_product(value))
            return flat_list
                                     
list1 = [1,2,3,4,[44,55,66,True],False,(34,56,78,89,34),{1,2,3,3,2,1},{1:34,"key2":[55,67,78,89],4:(45,22,61,34)}[56,'data science'],'Machine Learning']
flat_list = flat_list_product(list1)
product = 1
for num in flat_list:
    product *=num
print(product)
```


    ---------------------------------------------------------------------------

    KeyError                                  Traceback (most recent call last)

    Cell In[6], line 27
         24                     flat_list.extend(flat_list_product(value))
         25             return flat_list
    ---> 27 list1 = [1,2,3,4,[44,55,66,True],False,(34,56,78,89,34),{1,2,3,3,2,1},{1:34,"key2":[55,67,78,89],4:(45,22,61,34)}[56,'data science'],'Machine Learning']
         28 flat_list = flat_list_product(list1)
         29 product = 1


    KeyError: (56, 'data science')



```python
#Que2
class encrypt:
    def__init__self,a):
        self.a=a
    def enc(self,*args):
        b = ""
        for i in a :
            if i!="a" and i!="b" and i!="c" and i!=" ":
                b = b + i
            elif i =="a":
                b = b + "z"
            elif i == "c":
                b = b +"x"
            elif i == " ":
                b = b +"$"
                
                
x = "I want to become a data scientist."
c=encrypt(x)
c.enc()
            
```
