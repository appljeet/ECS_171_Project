# ECS 171 Final Project

# Introduction

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

Classification Report from our first model: 

![Classification Report Model 1](project_images/Classification%20Report%20-%20Model%201.png)

## Model 2

Classification Report from our second model:

![Classification Report Model 2](project_images/Classification%20Report%20-%20Model%202.png)

# Discussion

## Model 1

When comparing the Classfication Report of our training data vs, testing data, we see that all our measures of error (precision, recall, f1-score, support, and accuracy) are all within <2% of eachother. This tells us that our graph is definitely NOT overfitted, because an overfitted model would mean that our testing data would perform much more poorly than than our training data. However, we can see that our accuracy and precision are both below 80%. This means that our model incorrectly predicted the outcome ~1/5 of the time, and we also classified around the same amount as false positives. 

So, from analyzing all the metrics of our Classification Reports, we can safely predict that our model IS underfitted. Our accuracy and precision both scored poorly (below 80%), however we see that the Classification Reports between our training and testing data perform very similarily (each error metric being 1-2% off of each other). 

Our next steps to improve our current underfitting model is to add more complexity to our model. In our first model, we only used one Linear SVC, in the future we plan to use neural networks for classification as well as an RBF SVC. 

## Model 2


# Conclusion

# Collaboration
