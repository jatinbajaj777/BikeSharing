# Report: Predict Bike Sharing Demand with AutoGluon Solution
#### NAME HERE

## Initial Training
### What did you realize when you tried to submit your predictions? What changes were needed to the output of the predictor to submit your results?
Set negative values to zero

### What was the top ranked model that performed?
WeightedEnsemble_L2

## Exploratory data analysis and feature creation
### What did the exploratory analysis find and how did you add additional features?
Found features that could be extracted form data

### How much better did your model preform after adding additional features and why do you think that is?
With hyperparams,
it had about 15% improvement in kaggle score (0.61-0.52772/0.52772)
With new features,
It has about about 2% decrese in kaggle score (0.51-0.52772/0.52772)

## Hyper parameter tuning
### How much better did your model preform after trying different hyper parameters?
Had memory issues with num_bag_folds params, so tried some alternatives

### If you were given more time with this dataset, where do you think you would spend more time?
EDA

### Create a table with the models you ran, the hyperparameters modified, and the kaggle score.
|model|hpo1|hpo2|hpo3|score|
|--|--|--|--|--|
|initial|default|default|default|0.52772|
|add_features|default|default|default|0.51745|
|hpo|num_boost_round: 100 learning_rate:0.4|'num_boost_round': 100,'learning_rate':0.4,num_leaves:100|'num_boost_round':100,'learning_rate':0.6,num_leaves':100,'metric':'rmse'|0.61000|

### Create a line plot showing the top model score for the three (or more) training runs during the project.

TODO: Replace the image below with your own.

![model_train_score.png](img/model_train_score.png)

### Create a line plot showing the top kaggle score for the three (or more) prediction submissions during the project.

TODO: Replace the image below with your own.

![model_test_score.png](img/model_test_score.png)

## Summary
Measured the project across different features and hyperparamteres.
