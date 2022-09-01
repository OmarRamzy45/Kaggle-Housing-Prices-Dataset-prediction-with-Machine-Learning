# Housing Prices Prediction
in this code I used House Prices dataset from Kaggle website to train a linear regression model and try to predict the price of the house based on given features.

## Dealing with Data:
 - ### Data Importing 
 Using pandas inbuilt function pd.read_csv( ) I imported data from the given CSV file into my code.
 - ### Filling missing values
 For numerical values, I used KNeighborsRegressor to impute for missing numerical values based on other given values in the same column.

 For categorical values, Some of the missing values are not actually missing but N/A means something from the data descrption file so I replaced the missing values for these features to None.
 And for the other features that N/A doesn't mean something I used mode imputation method to impute for those missing values.
 - ### transforming Categorical values to string
 from "data_description.txt" I found some featurs with type "object" that have numerical values like "MSSubClass" feature so in order not to let the model deal with it as numerical value I converted its data to string to make sure it won't take unwanted values that doesn't represent any thing
 - ### Reducing Skewing of Data
 I used log transformation method to reduce the skew of data and make it more closer to normal distribution.
 - ### Replace categorical data (strings) with numerical values
 I replaced data with categorical datatype and gave them unique values.
 - ### Adding Bias Column
 - ### Splitting the dataset
 Finally, I splitted the dataset into training data to train the model on and validation data to test the model and check for its accuracy

## Linear Regression Model:
I created a class for the linear regression model and used the Normal Equations to train the model and calculate the weights then used these weights to predict the output for new values.
## Calculating the Error 
I used MAE (mean absolute error) method to check for the model accuracy and calculate the error between the predicted and the actual values
## Comparing with Linear Regression model from sklearn
In the Last step I compared between the model I created and the built-in model from sklearn linear_model library to make sure it will make the same predictions.

That's All. I hope you found this usefull.
Thank you for reading :).
