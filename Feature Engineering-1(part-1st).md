```python
Q1.What are missing values in a dataset? why is it essential to handle missing values? Name some algorithms 
that are not affected by missing values.
Ans-
   Missing values in a adataset refer to the absence of a value for a particular variables or feature in an observation
    
It is essential to handle missing values on a dataset because they can adversely affect the accuracy and reliability 

some algorithms that are not affected by missing values include tree-based models such as decision trees,random forest
```


```python
Q2.List down technique used to handle missing data.Give an example of each with python code.
Ans-
   There are several techniques used to handle missing data.some of the commonly used techniques are:
    
    1.Deletion:This involves removing the rows or columns that contain missing values.There are two type of deletion
    
    Example using python:
    
    # creating a sample dataset with missing values
    import pandas as pd
    import numpy as np
    
    data:= {'Name': ['John','Mike','Sarah','Kate','Tim'],
            'Age': [25,28,np.nan,31,27],
            'Salary': [50000,60000,45000,np.nan,55000]}
    
    df = pd.DataFrame(data)
    
    # Listwise deletion
    df1 = df.dropna() # remove rows with missing values
    print(df1)
    
    # pairwise deletion
    df2 = df.dropna(axis=1) # remove columns with missing values
    print(df2)
    
      2.ImputationLThis involves filling in the missing values with estimated values.There are several methods for imputation.
        
    Example using python:
    # using mean imputation
    df['Age'].fillna(df['Age'].mean()) # fill missing values with mean
    print(df)
    
    # using median imputation
    df['Salary'] = df['Salary'].fillna(df['Salary'].median()) # fill missing values with median
    print(df)
    
    # using mode imputation
    df['Name'] = df['Name'].fillna(df['Name'].mode()[0] # fill missing values with mode
    print(df)
                                   
            
       3.Prediction: This involves using machine learning algorithm to predict the missing values based on the other variable
    
    Example using pyton:
    # using k-Nearest Neighbors imputation
    from sklearn.impute import KNNImputer
                                   
    imputer = KNNImputer(n_neighbors=2)
    df_imputed = imputer.fit_transform(df[['Age','Salary]])
                                           
    print(df)
                                           
        4.Interpolation: This involves filling in the missing values using mathematical function that estimates the missing values
                                           
    Example using python:
    # using linear interpolation
    df['Age'] = df['Age'].onterpolate() #fill missing values using linear interpolation
    print(df)
                                   
```


```python
Q3. Explain the imbalanced data.what will happen if imbalanced data is not handled?
Ans-
    Imbalanced data refers to a dataset where the number of observations in one class is significantly higher or lower
    
    If imbalanced data is not handled , the machine learning model may perform poorly ,leading to incorrect predictions for
    
    For example, in a medical diagnosis problem where the positive cases (disease) are only 10& of the dataset
    
    To avoid this,it is essential to handle imbalanced data and apply techniques such as understanding ,oversampling.
```


```python
Q4.What are up-sampling and Down-sampling ? Explain when ip-sampling and 
down-sampling are required.
Ans-
  Up-sampling and down-sampling are techniques used to balance the clas  distribution in an imbalanced datset.
    
Down-sampling involves randomly removing samples from the majority class to match the number of samples in the minority

   Here is an example of downsampling using the pyton sklearn library:
        
from sklearn.utilis import resample

# assuming we have majority_class_samples , and minority_class_samples as datafames
# Downsample majority class
downsampled_majority = resample(majority_class_samples , replace=False , n_samples = len(minority_class_samples),random_states
                                
# Combine minority class with downsampled ,ajority class
downsampled_df = pd.concat[downsampled_majority,minority_class_samples])
up_sampling,on the other hand,involves randomly replicating samples from the minority of class to increase their number

     Here is an example of up-sampling using python sklearn library:
        
from sklearn.utilis import resample

# assuming we have majority_class_samples and minority_class_samples as dataframes
# upsample minority class
upsampled_minority = (minority_class_samples, replace = True, n_samples=len(majority_class_samples),random_states
                      
# Combine majority class with upsampled minority class
upsampled_df = pd.concat([majority_class_samples,upsampled_minority])
It is important to note that both up sampling and down-sampling have their own advantages and disadvantages 
```


```python
Q5.What is data Augmentation?Explain SMOTE.
Ans-
    Data augmentation is a technique used to increase the size of a dataset by creating new examples by applying various
    
SMOTE (synthetic minority over-sampling Technique) is a data augmenatation method used to deal with imbalanced datasets.

The SMOTE alorithm works as follows:
    
    1.For each sample in the minority class, find its k nearest neighbors.
    2. select one of the k neigbors randomly and compute the difference between the feature vector of the sampling 
    3.Multiply this differences by a random value betwee  0 and k and add  the result to the feature vector of the minority
    4.Repeat steps 2 and 3 to create the desired number if new synthetic samples.
    
    SMOTE helps to balance the class distribution in the dataset and improve the performances of machine learning models
    
```


```python
Q6.What are outliers in a dataset? why is it essential to handle outliers?
Ans-
    Outliers are data points that lie far away from the rest of the data in a dataset.Outliers can occur due to various
    
    It is essential to handle outliers because they can have a ignificant impct on statistical analysis and machine learn
    
    There are several techniques to handle outliers including:
        
    1.Removing outliers: In this approch , outliers are identified and removed from the dataset.however ,this approch
    
    2.Winsorizzing:This approch involves capping the extreme values in the dataset at a certain percentile value.
    
    3.Transformation:This approch involves transforming the data to reduce the impact of outliers
    
    4.Robust statistical methods: These methods are designed to be less sensitive to outliers.
    
    5.Machine learning algorithm: some mahine learning algorithms, such as trees and random forests,are less
    
        Example of outliers removal with python code.
        
    import pandas as pd 
    import numpy as np
    
    # create a sample dataset outliers
    data = pd.DataFrame({'A': np.random.normal(0,1,100),
                         'B': np.random.normal(0,1,100),
                         'C': np.random.normal(0,1,100)})
    data.loc.[0,'A'] = 10 # add outliers
    q1 = data.quantile(0.25)
    q3 = data.quantile(0.75)
    iqr = q3-q1
    data_clean = data[~((data <(q1-1.5 * iqr)) | (data >(q3 + 1.5 *iqr))).any (axis=1)]
    
    print('Original data shape:',data.shape)
    print('Cleaned data shape:',data_clean.shape)
    
       Example of Winsorizzing with pythion code;;
        
    import pandas as pd
    import numpy as np
    
    # create a sample dataset with outliers
    data = pd.DataFrame({'A':np.random.normal(0,1,100),
                         'B':np.random.normal(0,1,100),
                         'C':np.random.normal(0,1,100)})
    data.loc[0,'A'] = 10 # add outlier
    
    # Winsorize the extreme values 
    p = 0.05 # percentiles to cap at
    data_winsorized = data.apply(lambda x: np,clip(x,x.quantile(p),x.quantile(1-p)))
    
    print('Original data:\n',data.head())
    print('\nwinsorized data:\n',data_winsorized.haed())
```


```python

```
