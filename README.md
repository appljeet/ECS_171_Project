# ECS 171 Final Project

# Introduction

 - Blood is a crucial resource for life-saving transfusions. Unfortunately, it is often in short supply and blood banks regularly face shortages due to the volunteer-based sourcing of an already scarce resource
 - Using a dataset describing blood donors, we will train a model to predict whether a given patient will donate blood or not based on information like how many times they have previously donated blood and whether they have donated blood recently or not.
 - Such a model could help blood banks and hospitals predict starvation periods and ration resources accordingly.

# Figures
Our Data Table:

![Data Table](project_images/Data%20Table.png)

Our Data Pairplot:

![Data Pairplot](project_images/Data%20Pairplot.png)

# Methods

## Data Preprocessing

1. Read in data and drop any NA values.
2. Rename features to have simpler names.
3. Drop any unnecessary features.
4. Scale the data with MinMaxScaler().
5. Partition into training and test data.


## Model 1 - SVC with linear kernel

How Does Model Fit Into Fitting Graph?

Since our dataset represents a classification problem, Classification Report is a good measure of error because we are able to find accuracy, precision, recall, f1-score, and support. 

## Model 2 - SVM with RBF kernel


```
y_pred_train = model.predict(X_train)
y_pred_test = model.predict(X_test)


print(classification_report(y_train, y_pred_train))
print(classification_report(y_test, y_pred_test))
```

# Results

## Model 1

Classification Report for train data:

![Classification Report Model 1 - Train](project_images/Classification%20Report%20Model%201%20-%20Train.png)

Classifcation Report for test data:

![Classification Report Model 1 - Test](project_images/Classification%20Report%20Model%201%20-%20Test.png)

## Model 2

Classification Report for train data:

![Classification Report Model 2 - Train](project_images/Classification%20Report%20Model%202%20-%20Train.png)

Classification Report for test data:

![Classification Report Model 2 - Test](project_images/Classification%20Report%20Model%202%20-%20Test.png)

# Discussion

## Model 1

When comparing the Classfication Report of our training data vs, testing data, we see that all our measures of error (precision, recall, f1-score, support, and accuracy) are all within <2% of eachother. This tells us that our graph is definitely NOT overfitted, because an overfitted model would mean that our testing data would perform much more poorly than than our training data. However, we can see that our accuracy and precision are both below 80%. This means that our model incorrectly predicted the outcome ~1/5 of the time, and we also classified around the same amount as false positives. 

So, from analyzing all the metrics of our Classification Reports, we can safely predict that our model IS underfitted. Our accuracy and precision both scored poorly (below 80%), however we see that the Classification Reports between our training and testing data perform very similarily (each error metric being 1-2% off of each other). 

Our next steps to improve our current underfitting model is to add more complexity to our model. In our first model, we only used one Linear SVC, in the future we plan to use neural networks for classification as well as an RBF SVC. 

## Model 2

When comparing the Classification Report for our training and testing data, we get different results than we did from Model 1. Looking at our measures of error, we can clearly see that our values have a greater difference for precision, recall, f1-score, and support, than we had for Model 1. What is apparent about this, though, is that our precision value did go up from our previous model, showing that there was some kind of improvement in our second model. Moreover, our accuracy value did go up by .01%, meaning that our second model did perform slightly better in terms of accuracy than Model 1 did. 

It appears that our model still is underfitted. Our accuracy and precision values both went up from the previous model, leading us to believe that our second model did, in fact, do a better job of correctly predicting whether a person donated blood or not. It's also important to note that our Classification Reports for our training and testing data in Model 2 were still relatively similar.

# Conclusion

- Blood donation can be reliably predicted based on donor information.
- Lack of data was our greatest limitation, as we only had data from one year. Training the model on data spanning multiple years would likely significantly increase performance.
- Further research would consist of fitting and evaluating different classification models, as well as obtaining a more robust data set.

# Collaboration
