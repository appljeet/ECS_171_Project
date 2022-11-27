# ECS 171 Final Project

## Data Preprocessing

1. Read in data and drop any NA values.
2. Rename features to have simpler names.
3. Drop any unnecessary features.
4. Scale the data with MinMaxScaler().
5. Partition into training and test data.


## Model 1 - SVC with linear kernel

- MSE:
  - Training Error: **0.23**
  - Test Error: **0.22**
  
- Notes:
  - Train and Test error do not significantly differ. 
  
- Conclusion: 
  - There does not appear to be evidence of overfitting.