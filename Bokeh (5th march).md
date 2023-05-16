```python
Q1. How can you create a bokeh plot using python code?
Ans- 
   To create a bokeh plot using python code , you cam follow these steps:
        
1.Import the necessary modules:Bokeh, Numpy, and pandas(if you are working with data).

2.Prepare your data: This could involve loading a datasetbor generating your own data.

3.Create a figure: Use the figure function to create a new plot figure.you can set various parameteres.

4.Add glyphs:Use the various glyph functions (e.g.circle,line,react)to add visvual elemsnts to the plot

5.Add tool:Use the tools parameter to specify which interactions tols should be included with the plot.

6.Display the plot:Use the show function to display the plot in the current output device (usually the browser)

Here is an example code snippet that creates a simple Bokeh plot:
    
from bokeh , plotting.import figureouput_file,show
import numpy as np

# Generate some data:
x = np.arrange(0,10,0.1)
y = np.sin(x)

#create a new plot with title ad axis labels
p = figure(title ='simple Bokeh plot',_axis_label='x',y_axis_label='y')

#Add a ine glyph
p.line(x,y,line_width=2)

#specify which interactive tools to include
p.tools=[]

#Display the plot in the browser
show(p)

This code generates some data using Numpy,creates a new bokeh plot figure using the function , adds a line glyph
```


```python
Q2.What are glyph in Bokeh,and how can you add them to a Bokeh plot?Explain with an example.
Ans-
    In Bokeh, glyph are the basic visvual elements that are used to display data on a plot,glyphs are geometrical in shape
    
    To add glyph to a Bokeh plot, you can use on eof the functions provided by the bokeh.plotting module
    
    1.circle:draw circles at the pecified x and y coordinates.
    2.square:draw squares at the specified x and y coordinates.
    3.line:draw lines connecting the specified x and y coordinates.
    4.rect:drwas rectangles with the specified x, y ,width and height values.
    
    Here is an example code nippet that adds some circles and lines to a Bokeh plot:
        
        from bokeh.plotting import figure,output_file,show
        import numpy as np
        
        #Generate some data
        x = np.arrange(0,10,0.1)
        y1 = np.sin(x)
        y2 = np.cos(x)
        
        # create a new plot with title and axis labels0
        p = figure(title='Bokeh plot with glyphs',x_axis_label='x',y_axis_label='y'
                   
        # Add some circles and lines
        p.circle(x, y1, size=10,color:'blue')
        p.line(x, y1, line_width=2, color:'blue')
        p.circle(x, y2, size=10, color='red')
        p.line(x, y2, line_width=2, color='red')
                   
        # specify which interactive tools to browser
        p.tools =[]
                   
        # Display the plot in the browser
        show(p)
    
    In the example , we generate some data using Numpy and create a new Bokeh plot figure using the figure function
```


```python
Q3. How can you customize the apperance of a Bokeh plot ,including the axis , titles and legend?
Ans-
    Bokeh provides several ways to customize the apperance of a plot, including the axes, totles and legend.here are some 

    1. Customize the title:You can set the title of plot using the title property of the figure object.for ex.p.title
    
    2.Customize the axes: You can customize the appearance of the x and y axes using the x-axis and y-axis proprties 
    
    3.Customize the legend :You can customize the appearance of the legend using the legend property of the figure object.
    
    Here is an example code snippet that demonstrates these customization options:
        
    from bokeh.plotting import figure,output_files,show
    
    # Generate some data
    x = np. arrange(0,10,0.1)
    y1= np.sin(x)
    y2= np.cos(x)
    
    # Create a new plot with titles and axis labels
    p = figure(title= 'My Bokeh Plot',x_axis_labels='X label',y_axis_label='Y label')
    
    # Add some lines with legend labels
    p.line(x, y1, line_font_size = '20pt'
    p.xaxis.axis_label_text_font_size = '16py'
    p.yaxis.axis_label_text_font_size = '14pt'
    p.legend.label_text_font_size = '14pt'
    p.legend.label_text_font_style = 'bold'
    p.legend.location = 'top left'
           
    # specify which interactive tools to include
    p.tools =[]
           
    # Display the plot in the browser
    show(p)
           
    In this example, we create a plot with a title and axis labels using the figure function . We add some lines to the ploy
           
        
```


```python
Q4. What is a Bokeh server, and how can you use it to create interactive plots that acn be updated in
real time?
Ans-
    A Bokeh server is a python server that allows for the creation of interactive plots that can be upated in real time
    
    To create a Bokeh server application , you need to define a funcyion that creates the plot and updates it as necessary.
    
    Here is an example of how to use a Bokeh server to create an interactive plot that updates in real-time:
        
    from bokeh.io import curdoc
    from bokeh.modules import ColumnDataSource
    from bokeh.plotting import figure
    import numpy as np
    
    # create a data source
    x = np.arrange(0,10,0.1)
    y = np.sin(x)
    source = ColumnDataSource(data=dict(x=x,y=y))
    
    #create a figure
    plot = figure (plot_width=400,plot_height=400)
    plot.line)'x','y',source=source,line_width=2)
    
    #Define a callback function to update the data source
    def update_data(attrname,old,new):
        # Generate new y values baesd on the selected freqency
        freq = frequency.value
        new_y =np.sin(freq * x)
        source.data = dict(x=x,y=new_y)
        
        # Add a slider widget ti the plot
        freqency = Slider(title='Freqency", value=1 ,start=0.1, end=5 ,step=0.1)
        freqency.on_change('Value',update_data)
                          
        # Add the plotand widget to the current document
        curdoc().add_root(column(plot,freqency))
        
        In this example, we first create a data source containing x and y data. we then create a plot using the figure()function
                          
       Next , we define a callback function update_data() that updates y data in the data source based on the value of slider 
                          
    Finally , we add the plot and slider widget to the current document using the curdopc().add_root()function
        
    
```


```python
Q5. How can you embed a Bokeh plot into a web page or dashboard using Flask or Django?
Ans-
    To embed a Bokeh plot using into a web page or dashboard using Flask or Django, you can follow these general steps:
        
    1.create a Bokeh plot using Bokeh library in python.
    
    2.save the plot using save()method and provide a filename and directory where the plot will be saved.
    
    3.create a Flask or Django application and add a route for the page where the plot will be displayed.
    
    4.In the flask or Django route function ,use the file_html() function from Bokeh's embed module to generate the html code.
    
    5.Return the HTML code to the web page using Flask's or Django's render_template() function.
    
    Here is an example of embedding a Bokeh plot in a Flask application:
        
    from flask import Flask,render_template
    from bokeh.plotting import figure,output_file,save
    from.embed import file_html
    
    app = Flask(_name_)
    
    @app.route('/')
    def index():
        # createb a Bokeh plot
        plot = figure(title='My plot',x_axis_label='X' , y_axis_label='Y')
        plot.line([1,2,3,4,5],[2,4,6,8,10])
        
        #save the plot as an HTML file
        output_file('templates/plot.html')
        save(plot)
        
        #  Load the HTML file and return it to the template
        with open ('template/plot.html')as f:
            plot_html = f.read()
        return render_template('index.html',plot_html=plot_html)
    
    In this example, we create a simple line plot using Bokeh , save it as an HTML file in the Flask application's templates
    
    <!doctype html>
    <html>
      <head>
         <title>My App</title>
        {{plot_html|safe }}
        </head>
        <body>
           <h1>Welcome to my app</h1>
        </body>
    </html>
    
    This is a basic example, but the same approch can be used to embed more complex Bokeh plots into Flask or Django application
        
```
