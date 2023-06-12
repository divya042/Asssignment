```python
Q1.What is the Gradient Boosting Regression?
Ans-
    Gradient Boosting Regression is a mechanism learning algorithm used for regression tasks ,which involves predicting a
    
The algorithm works by combining multiple weak predictions models ,typically decision tress ,to create  strong predactive 

Here's high level overviews of how Gradient Boosting REgression works:

1.Initialize the model with a constant value ,usually the mean of the taret variable
2.Calculate the negative gradient of the loss function with respect to the current model's predictions.
3.Fit a weak model ,such as a decision tree ,to the negative gradient,trying to minimize the loss function.
4.Add the weak model to the ensemble ,butbwith a small learning rate (shrinkage parameter) to prevent overfitting 
5.Repeat steps 2 to 5 for a specified number of iterations or until a certain stopping criterion is met.
6.The final predictions is obtained by summing the predictions of all the weal models .

```


```python
By iteratively improving the model's predictions , Gradient Boosting Regression can create a powerfull ensembles model capabke
```


```python
Q2.Impliment a simple gradient boosting algorithm fromscratch using python and Numpy.Use a 
simple regression problem as an example and train the model on a small dataset .Evaluate the model's performance
using metrics such as an mean squared error and R-shaped.
Ans-
   
     import numpy as np
from sklearn.datasets import make_regression
from sklearn.metrics import mean_squared_error ,r2_score 

# generate some random data for our regression problem
x , y = make_regression(n_samples=100 , n_features=1, noise=10 , random_state=42)

## generate data into training and testing sets:
split = int(len(X)*0,8)
x_train , y_train = X[:split],y[:split]
x_test ,y_test = X[split:],y[split:]

class GradientBoostingRegressor:
    def __init__(self, n_estimators , learning_rate):
        self.n_estimators = n_estimators
        self.learning_rate = learning-rate
        self.models = []
        
    def fit(self , x,y):
        # initialize the predictons
        y_pred = np.zeros(len(y))
        
        # iterate over the number of estimators
        for i in range(self.n_estimators):
            # compute the gradient of the loss function
            gradient = y - y_pred
            
            # fit a regression model to the gradient
            model = DecisionTreeRegression(max_depth=1)
            model.fit(x,gradient)
            
            # add the model to the list of models 
            self.models.append(model)
            
            # update the predictions
            y_pred += self.learning_rate = model.predict(x)
            
        def predic(self,X):
            # initialize the predictions
            y_pred = np.zeros(len(x))
            
            # iterate over the models and update the predictions
            for model in self.models:
                y_pred +=self.learning_rate +=model.predict(X)
                
            return _ypred
        
        fromsklearn.tree import DecisionTreeRegressor
        
    gb = GradientBoostingRegressor(n_estimators=100 ,learning_rate=0.1)
    gb.fit(X_train,y_train)
    
    y_pred = gb.predict(X_test)
                
    y_pred
    
    array([-77.31321482,   4.16102018,  4.16102018,  -63.05652357,
           41.633057  ,    0.53797017,  -22.76934693,   0.53797017,
           -38.30103698,   0.53797017,  -44.09854195,    63.40594491,
             0.53797017,  -22.76934693,  -22.76934693,   62.99436584,
            -63.05652357, -34.1208811,    0.53797017,     -8.95011837])
    
    mse = mean_squared_error(y_test,y_pred)
    r2 = r2_score(y_test,y_pred)
    print("Mean squared Error:",mse)
    print("R-squared score:",r2)
    
    Mean squared Error:67.715820905791
    R-squared Score: 0.9575588436634127
```


```python
Q3.Experiment with different hyperoarameters such as learning rate,numbe of trees, and tree depth to 
optimise the performance of the model .Use grid search or random search to find the best
hyperparameters
Ans-
  import numpy as np 
from sklearn.datasets import make_regression
from sklearn.metrics import mean_squared_error,r2_score
from sklearn.tree import DecisionTreeRegressor
from sklearn.ensemble import GradientBoostingRegressor
from.sklearn.model_selection import GridsearchchCv

X,y = make_regression(n_samples=1000, n_features=10,noise=10, random_state=42
        
split = int(len(X)*0.8)
X_train,y_train = X[:split], y[:split]
X_test, y_test = X[split:],y[split:]
                      
# define the hyperparameter grid
param_grid = {
    'n_estimators': [10,20,30,40,50],
    'learning-rate': [0.01,0.01,1],
    'max_depth': [1,2,3]
    
}
        
# create an instance of the GradientBoostingRegressor
gb = GradientBoostingRegressor()
                    
# create an intance of GridsearchCV
grid_search = GridsearchchCv(estimator=gb,param_grid=param_grid,cv=5)
                      
# fit the grid search to the training data
grid_search.fit(X_train ,y_train)
        
GridsearchCV(cv=5, estimator=GradientBoostingRegressor(),
             param_grid={'learning_rate': [0.01,0.01,1],
                         'max_depth': [1,2,3]
                         'n_estimators': [10,20,30,40,50]}
             
# get the best hyperparameters
best_params = grid_search.best_params_
             
# create an instance of the GradientBoostingRegressor with the best hyperparameters
gb = GradientBoostingRegressor(**best_params)
             
# fit the model to the training data 
gb.fit(X_train, y_train)
             
# get the best hyperparameters
best_params = grid_search.best_params_
             
# create an instance of the GradientBoostingRegressor with the best hyperparameters
gb = GradientBoostingRegressor(**best_params)
             
# fit the model to the training data
gb.fit(X_train ,y_train)
             
                            

```
