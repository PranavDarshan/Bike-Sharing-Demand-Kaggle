# Report: Predict Bike Sharing Demand with AutoGluon Solution
#### PRANAV DARSHAN

## Initial Training
### What did you realize when you tried to submit your predictions? What changes were needed to the output of the predictor to submit your results?
I realised that my score was very low compared to the ones that were already submitted. There were some features I hadn't included in my result. I got an error if I directly submitted the values with the negative values.

### What was the top ranked model that performed?
My best model from the Kaggle score was the model in which I added new features and tuned the model hyperparameters. According to the AutoGluon's Tabular Predictor, the model with the new features but unchanged hyperparameters got the best score. I think this is because of the overfitting of the model. That is why this model performed bad on the test set compared to hyperparameter tuned model.

## Exploratory data analysis and feature creation
### What did the exploratory analysis find and how did you add additional features?
EDA helped me find out that different times of the day also had some importance for predicting the bike sharing demand. A lot of people have travelled during the peak hours and this is the reason why the demand shoots up during peak hours. That is the reason for adding time as a new feature.

### How much better did your model preform after adding additional features and why do you think that is?
My model performance was increased by two times when I added the new feature. This is because one of the most important feature was being neglected and this was a strong feature which would help in the correct prediction of the output.

## Hyper parameter tuning
### How much better did your model preform after trying different hyper parameters?
My model performed 4 times better than the original model without any new features.

### If you were given more time with this dataset, where do you think you would spend more time?
I would figure out the best features which have the most importance. I would categorize the different times as busy, peak hour, no demand.

### Create a table with the models you ran, the hyperparameters modified, and the kaggle score.
|model|hpo1|hpo2|hpo3|score|
|--|--|--|--|--|
|initial|-53.106980|-53.371709|-55.236966|1.80125|
|add_features|-30.192097|-30.565250|-30.842822|0.75225|
|hpo|-35.451844|-35.776083|-36.480231|0.47249|

### Create a line plot showing the top model score for the three (or more) training runs during the project.

![model_train_score.png](https://github.com/PranavDarshan/Bike-Sharing-Demand-Kaggle/blob/main/model_train_score.png)

### Create a line plot showing the top kaggle score for the three (or more) prediction submissions during the project.

![model_test_score.png](https://github.com/PranavDarshan/Bike-Sharing-Demand-Kaggle/blob/main/model_test_score.png)

## Summary
My best model from the Kaggle score was the model in which I added new features and tuned the model hyperparameters. The previous model without the hyperparameter tuning did not perform very well on the test data set but performed very good on the training data set in fact better than this model. This is due to overfitting. Finally autogluon helps us give a baseline model on which we need to improve on. That is why in the third model I have chosen only the top 2 models in the leaderboard and changed their parameters to finally train a good model.
