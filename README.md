# Neural_Network_Charity_Analysis

## Purpose of analysis

Applying the knowledge of Machine Learning and Nerual networks that we learnt in the module, we use the features in the Alphabet Soup Charity dataset to help Beks create a binary classifier that can predict whether applicants will be successful if funded by Alphabet Soup.

We first preprocess the data for the Nerual Network Model, and then compile, train and evaluate the model.

In the deliverable 3 we optimize the model with different approaches to try to get the accuracy over 75%

## Resources

Dataset: [Alphabet Soup Charity dataset (charity_data.csv)](https://2u-data-curriculum-team.s3.amazonaws.com/dataviz-online/module_19/charity_data.csv)

Software: Python 3.10, Conda 4.13, jupyter notebook 6.4.11

## Result

- Data Preprocessing

What variable(s) are considered the target(s) for your model?
The target for model is "Is-Successful"

What variable(s) are considered to be the features for your model?
NAME, APPLICATION, TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, INCOME_AMT, SPECIAL_CONSIDERATIONS, STATUS, and ASK_AMT

What variable(s) are neither targets nor features, and should be removed from the input data?
I removed EIN (employer identification) because it is not significant to the model. We can consider removing the STATUS since all rows are the same value of 1

- Compiling, Training, and Evaluating the Model

How many neurons, layers, and activation functions did you select for your neural network model, and why?
There are 3 hidden layers with many neurons. The 1st layer I used was "relu", 2nd and 3rd layer I used were "sigmoid". Having these amendments, the accuracy is increased from 72.58% originally to 75.33%. It only increased a bit but it passes the standard of 75%

Were you able to achieve the target model performance?
Yes

What steps did you take to try and increase model performance?
I first convert the NAME column to data points because it seems significant to the model result since some applicants applied more than 5 times. I also increase the bucket size for "CLASSIFICATION" from 500 to 1000.  However these changes did not increase the accuracy of model, it produced a even lower accuracy which is 58.78%,

After that I added one more hidden layer with more neurons and changed the 2nd and 3rd layers to sigmoid, it increased the accuracy to 75.33%

## Summary

To sum up, after the three attempts to modify the learning model, the performance is increased to 75.33% and it passes the standard.

For further attempts, we can also have more modification by removing more features, changing the bucket size, or increasing the epochs size to increase accuracy. We can also collect more data and inputs to boast up accuracy if the company is within the budget.

Another way is that we can change to use another learning model.

I recommend using Random Forest classifiers since the dataset is robust and tabular, the data also contains more than 34,000 organizations information, Random Forest classifiers can achieve comparable predictive accuracy on large tabular data with less code and faster performance.

