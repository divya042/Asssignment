```python
Q1. Name any five plots that we can plot using the seaborn library.Also, state the user of each plot.
Ans -
     seaborn is a python visualization library based on Matplotlib that provides a high -level interface for creating in
    
    1.scatter plot - A scatter is a graph in which the values of two variables are plotted along two  axes 
    
    2.Line plot - A line plot is a graph that displays information as a series of data points connected by straight 
    
    3.Bar plot - A bar plot is a graph that ses rectangular bars to represent bars to represent data.It is useful for compairing values
    
    4.Histogram - A histogram is a graoh that shows the distribution of a dataset.It is useful for identifying 
    
    5.Heatmap - A heatmap is a graphical representation of data in which values are represented for colours.
```


```python
Q2. Load the "fmri" dataset using the load_dataset function of seaborn . plot a line using x ="timepoint" and y = "Signal"
for different events and regions.

Ans -  
 here is the code to load the "fmri" dataset  using the load_dataset functionof seaborn and plot a line using x = "timepoint" and y = "Signal"
    
          import seaborn as sns
        
    # Load the fmri dataset
    fmri_data = sns.load_dataset("fmri")
    
    #plot the line plot using seaborn
    sns.lineplot(X="timepoint",Y="Signal",hue="event",style="region",data=fmri_data)
    
    In this code , we first load the "fmri" datasetnusing the load_dataset function of seaborn and store it in the fmri_data
```


      File <tokenize>:10
        fmri_data = sns.load_dataset("fmri")
        ^
    IndentationError: unindent does not match any outer indentation level




```python
Q3.Load the "titanic " dataset using the load_daatet function of seaborn . plot two box plots using x = 'pclass',  = 'age'
and y = 'fare'.
Note:pclass , age, and fare are columns in the titanic dataset.
Ans-
     here is the code to load the "titanic" dataset using the load_dataset function of seaborn and plot two box plots us
    
    import seaborn as sns 
    # Load the titanic dataset 
    titanic_data = sns.load_dataset("titanic")
    
    #Ploat the box plots using seaborn 
    sns.boxplot(x="pclass",  y="age", data=titanic_data)
    sns.boxplot(x="pclass",  y="fre", data=titanic_data)
    
    In this code , we first load the "titanic" dataset using the load_dataset function of seaborn and store it in the titanic

```


```python
Q4.Use the "diamonds" dataset from seaborn to plot a histogram for the 'price' column , use the hue
parameter for the 'cut' column of the diamonds dataset.
Ans -
      Here is the code to laod the "diamonds" dataset using the load_dataset function of seaborn and plot a histogram for the price
    
 import seaborn as sns

#Load the diamonds dataset
diamonds_data = sns.load_dataset("diamonds")

#plot the histogram using seaborn
sns. histplot(data=diamonds_data, x="price",hue="cut"
              
              In this code , we first load the "diamonds" dataset using the load_dataset function of seaborn and store it in the diamonds

```


```python
Q5. Use the "iris" datasetfrom seaborn to a pair plot. Use the hue parameter for the "species" column
of the iris dataset.
Ans- 
    Here is the code to load the "iris" dataset using the load__dataset  function of dseaborn and plot a pair plot, using seaborn
    import seaborn as sns
    
    #Load the iris adataset
    iris_data = sns. load_dataset("iris")
    
    #Plot the pair plot using seaborn
    sns.pairplot(data=iris_data , hue ="species")
    
    In this code, we first load the "iris" dataset using the load_dataset function of seaborn and store it in the iris_dataset
```


```python
Q6. Use the "flights" dataset from seaborn to plot a heatmap.
Ans- 
   Here is the code to load te "flights" dataset using the load_dataset function of seaborn and pot a heatmap:
        
    import seaborn as sns
    
    #Load the flights dataset
    flights_data = sns.load_dataset("flights")
    
    #pivot the data to get it in the right format for the heatmap
    flights_data = flights_data.pivot("month","year",passengers")
    
    #plot the heatmap using using seaborn
    sns.hetmap(flights_data,cmap="YlGnBu")
                                      
    in this code , we first load the "flights"datset using the load_dataset function and store it in the flights
```
