# NYC-Taxi-Fare-Prediction

This project demonstrates some of the machine learning techniques from [Scikit-learn](https://scikit-learn.org/stable/) module in Python. We use the dataset from a Kaggle competition: [New York City Taxi Fare Prediction](https://www.kaggle.com/c/new-york-city-taxi-fare-prediction/overview), the goal is to build a machine learning model to predict the fare amount for a taxi ride in NYC given pickup and dropoff locations, and the result is evaluated on RMSE of the predictions.  
Scikit-learn provides a bunch of handy tools for machine learning, such as feature preprocessing, model selection and pipeline so that it makes more easier to test out different models under the same structure and makes the code more tidier. In this project, we tested a handful of regression models, including *linear regression, polynomial regression, random forest regression and SVM regression*. We chose the best model based on RMSE from 5-folds cross-validation on the training set, after fine-tuned the hyperparameters for each models with grid search.    
However, building a model is not the hardest part of the project, it takes more or less just two lines of code that you can come out a basic one, thanks to Scikit-learn. The most interesting part would be to decide what features chosen to fit into the models, explore the data with descriptive statistics and preprocess features to what applicable to the algorithm are very important steps in order to yield good predictions. So in this project you'd see how to use **pipeline** module to integrate data preprocessing into part of model building.

 - What's pipeline: Pipeline connects a sequential of transformers and a final estimator that allows data to be processed in the right order. For example, in this project we want to fit categorical feature in the model, such as day of week, however, most of machine learning algorithms take only numbers as input so we need to encode categories into binaries before throwing them into the model. And for numerical features we want to normalize or standardize them before fitting them in the model so that the model can perform better. In this case, we'd create pipelines to run different processes for different types of feature and combine them together, then on top of that, we'd make another pipeline to connect preprocessing steps with an estimator of any machine learning algorithm.     
 - Why is pipeline necessary:
