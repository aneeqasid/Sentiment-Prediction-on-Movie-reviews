# Sentiment-Prediction-on-Movie-reviews

This project aims to predict the sentiment of movie reviews using different machine learning models. I will be using the following models:

logistic regression
linear SVC, and
multinomial naive Bayes.

## Understanding Data


The train data frame has 162758 rows and 5 columns, while the movies data frame has 143258 rows and 14 columns.
The train data frame has four object columns, one bool column, and no numeric columns. The object columns are movieid, reviewerName, reviewText, and sentiment. The sentiment is our TARGET variable.
The movies data frame has 12 object columns, two numeric columns, and no bool columns.
releaseDateTheaters Column and releaseDateStreaming are date columns but they are of object type by default.
boxOffice column is the gross revenue of the movie in US dollars, is it of object type though it should be numeric, so we will work on these columns.

![image](https://github.com/user-attachments/assets/700f29ea-2277-4017-bbb3-f2244ab3bf26)
![image](https://github.com/user-attachments/assets/c09f9b1f-a746-457c-985e-4b8b67985fe7)
![image](https://github.com/user-attachments/assets/9fd0ad1f-6226-4fc9-9516-26c7eb336423)
![image](https://github.com/user-attachments/assets/b6459cd9-5d3b-433b-82d7-f97de02ea961)

## Evaluation Metric

I have used the F1 micro score as the evaluation metric, which is the harmonic mean of precision and recall for each class, weighted by the number of instances in each class. This metric is suitable for imbalanced classification problems, where some classes have more instances than others.
I have also used the log loss as another evaluation metric, which is the negative log-probability of the true labels given the predictions. This metric is suitable for probabilistic models, where the predictions are not binary but continuous between 0 and 1. The lower the log loss, the better the model fits the data.

I have compared the performance of different models with and without hyperparameter tuning (HPT), which is a process of finding the optimal values for the parameters that control the behavior and complexity of the models.
I have used grid search as a method of HPT, which is a technique that exhaustively searches over a predefined set of values for each parameter.
