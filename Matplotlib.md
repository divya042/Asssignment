```python
Q1.What is Mtaplotlib ? Why is it used ? Nmae five plots that can be plotted using the python module of 
Matplotlib.
Ans- Matplotlib us a data visualization library for creating static, animated and interactive visualizations in python 

Matplotlib is used to create visvualization that help to understand data, communicate insights and support decision matplotlib

The pylot module of Matplotlib is a collection of functions that provide a simple and intitive interface for following

1.Line plot
2.Scatter plot
3.Histogram
4.Bar chart
5.Pie chart

```


```python
Q2.What is scatter plot ? Use the following code for x and y .Using this generated data 
plot a scatter plot.

    import numpy as np
    no.random.seed(3)
    X = 3 + np.random.normal(0,2,50)
    y = 3 + np.random.normal(0,2,len(X))
    Note:Also add title ,Xlabel and ylabel to the plot.
    
    Ans -
         A scatter plot is a type of plot that  displays value for two variables as points on a two -dimentional coordinate
        
    Here's how you can use the given code to generate data for x and y plot a scatter plot using 'matplotlib.pyplot':
    
    import matplotlib.pyplot as plt
    import numpy as np
    
    #Generate data for (x,y)
    
    #Add title and axis labels
    plt.title("Scatter Plot")
    plt.xlabel("X-axis")
    plt.ylabel("Y-axis")
    
    #show the plot
    plt.show()
    
    This will generate a scatter plot of x and y data points , with a title "Scatter Plot"and axis labels "X- axis" and Y- axis
    
```


```python
Q3.Why is the subplot() function used? Draw four line plots using the subplot() function
Use the following data:
    import numpy as np
    For line 1 : x = np.array([0,1,2,3,4,5]) and y = np. array([0,100,200,300,400,500])
    For line 2 : x = np.array([0,1,2,3,4,5]) and y = np.array([50,20,40,20,60,70])
    For line 3 : x = np.array([0,1,2,3,4,5]) and y = np.array([10,20,30,40,50,60])
    For line 4 : x = np.array([0,1,2,3,4,5]) and y = np.array([200,350,250,550,450,150])
Ans -
    The subplot() function is used to create plots in the same figure . It allows you to create a grid of plots 
    
               plt.subplot(num_rows, num_cols, plot_num)
        
    where num_rows and num_cols specify the number of rows and columns in the grid and plot_num specifies the posistion 
    
    Here is the code to create four line plots using the subplot() function:
        
        import numpy as np
        import matplotlib.pyplot as plt
        
        # create data for line 1
        x1 = np.array([0,1,2,3,4,5])
        y1 = np.array([0,100,200,300,400,500])
        
        # create data for line 2
        x2 = np.array([0,1,2,3,4,5])
        y2 = np.array[(50,20,40,20,60,70])
                      
        # create a data for line 3
        x3 = np.array([0,1,2,3,4,5])
        y3 = np.array([10,20,30,40,50,60])
            
        # create a line for line 4
        x4 = np.array([0,1,2,3,4,5])
        y5 = np.array([200,350,250,550.450,150])
          
        # create a 2x2 grid of plots
        plt.subplot(2,2,1)
        plt.plot(x1,y1)
        plt.title('Line 1')
        
        plt.subplot(2,2,2)
        plt.plot x2,y2)
        plt.title('Line 2')
                      
        plt.subplot(2,2,3)
        plt.plot(x3,y3)
        plt.title('Line 3')
                      
        plt.subplot(2,2,4)
        plt.plot(x3,y3)
        plt.title('Line 4')
                      
        # add overall title and axis label's
        plt.subtitle('Four Line Plots')
        plt.xlabel('x-axis')
        plt.ylabel('y=axis')
                      
        # display the plot
        plt.show()
                      
        The output of this code will be a figure with four line plots , arranged in a 2x2 grid . Each plot shoq the relatioship.
                      
                      
                      
                      
                      
```


```python
Q4.What is abar plot? Why is it used? Using the following data plot a bar plot and horizontal bar plot.

import numpy as np 
company = no. array(["Apple", "Microsoft","Google","AMD"])
Profit = np. array ([3000,8000,1000,10000])

Ans - 
   A plot is a way pf representing data using rectangular bars. It is used to compare visvualize the qualities
    
To create a bar plot and a horizontal bar plot usimg the given data, we can use the matplotlib,pyplot module as follows

impert matplotlib.pypot as plt
import numpy as np

company = np.array(["Apple","Microsoft","Google","AMD"])
Profit = np.array([3000,8000,1000,10000])

# creating a bar plot
plt.bar(company, profit)
plt.title("Company Profits")
plt.xlabel("Company")
plt.ylabel("profit(in billions)")
plt.show()

#creating a horizontal bar plot 
plt.barch(Company, profit)
plt.title("Company profits")
plt.xlabel("profit( in billions)")
plt.ylabel("Company")
plt.show()

       The first plot created using plt.bar() will show a vertical bar plot, where each company name is represented on x- axis and y- axis
    
```


```python
Q5.What is a box plot ? why is it used ? using the following data plot a box plot.
box1 = np. random. normal(100,10,200)
box2 = np. random. normal(90,20,200)
Ans - 
    A box plot , also known as a box and whisker plot , is a graphical representataion of a adataset that displays the dist
    
 Box plots are used to provide a visvual summary of the distribution of a dataset and to identify potential outliers.

To create a box plot for the given data , we can use the python library matplotlib. Here is an example code:
    
    import numpy as np 
    import matplotlib.pyplot as plt
    
    # Genertae the data
    box1 = np.random.normal(100,10,200)
    box2 = no.random.normal(90,20,200)
    
    # create the box plot
    ax.boxplot([box1,box2])
    
    # Add Labels and title 
    ax.set_xticlabels(['Box 1','Box2'])
    ax.set_ylabel('Value')
    ax.set.title('Box plot Example')
    
    # show the plot
    plt.show()
    
    In this example , we generate two sets of random data using numpy's normal distrubution, with ,means of 100 and 90 and 200
    
```
