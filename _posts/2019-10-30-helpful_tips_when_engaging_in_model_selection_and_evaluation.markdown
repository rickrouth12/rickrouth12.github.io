---
layout: post
title:      "Helpful Tips when Engaging in Model Selection and  Evaluation"
date:       2019-10-30 14:13:52 +0000
permalink:  helpful_tips_when_engaging_in_model_selection_and_evaluation
---



1. Properly assess the size of data set before moving forward - is it too large or too small?
2. Select the best hyperparameters
3. Choose the right model parameters
4. Be thorough during the model evaluation process - measuring accuracy, detecting overfitting or underfitting of models to training or test data sets
5. Perform an unbias evaluation before implementing any model into production - does it answer your original question?

**Properly assess the size of data set before moving forward - is it too large or too small?**
Choosing to pursue a data science project often begins by evaluating the size of available data sets used as the input for machine learning models. The quantity and quality of observations are a key factor in the potential outcome of any machine learning model. There is a lot of truth to the notion, “Garbage in, garbage out.” Knowing in advance that you are going to be conducting deep learning and leverage artificial neural networks will influence your decision of whether to use a data set with 1,400 observations versus another data set with 1.3 million data points. It is important to have enough usable data to create train, test, and validation sets to create proper ML models.

**Selecting the Best Hyperparameters**
Hyperparameters are the set conditions of a learning method before the actual learning process takes place. Experience plays a key role in choosing initial hyperparameters for any partciular model, however there are useful tools and strategies that data scientists use for hyperparameter selection. K-fold cross validation can be leveraged as a resampling procedure to evaluate machine learning models on a limited data sample. One of the advantages of this strategy over repeated sampling is that all observations are used in both training and validation steps, but each observation is only used once for validation. Cross-validation techniques can be used to detect overfitting as well.

**Choosing the right model parameters**
Model parameters are involved further downstream in the learning process and have tremendous influence on determining a model’s skill or aptitude in learning patterns based on the input data sets. GridSearchCV, or grid search cross-validation, is a popular technique used by data scientists for model parameter tuning after a series of machine learning models have successfully run and have been initially evaluated. It is a key step in the iterative process of discovering the best fit or optimized parameters to reduce error and improve accuracy.

**Be thorough during the model evaluation process**
Model evaluation not only includes measuring the accuracy of your models that you created using the training, testing, and validation data sets, but it also incorporates estimating how the models will perform on future unknown data sets. Holdout and cross-validation techniques are often used at this step to simulate the input of unseen data to properly assess the accuracy of any given model on new data. This way you as a data scientist can measure the true worth of your creations - are they universally applicable or narrow in scope and use?

**Perform an unbias evaluation before implementing any model into production - does it answer your original question?**
At this point in the process, I often like to take a step back and re-ask myself the original question I sought to answer. Can I make a more informed decision based on the learnings of my selected models or have I opened up a massive can of worms? It is often that simple an assessment that can steer one toward pursuing an implementation of a model in a production environment (the end goal) or deciding to go back to the drawing board and rest on the lessons learned throughout the process.

**A recent experience of mine**
In a recent project, I asked the question, “What features would be best for the classification of winning and losing players in Player Unknown's Battleground, a very popular battle royale videogame. I began with a dataset containing player statistics gathered from a series of first player perspective squad matches. This dataset held 1.7 million player records and 29 features (numerical and categorical) to describe the actions that occurred over the duration of a single match and some historical stats representative of past performance.

Moving through the steps of the OSEMN Data Science Framework, I gathered the data, prepared it for modelling, then executed three separate machine learning algorithms on training and testing sample datasets to determine the accuracy with which they could succesfully classify winning and losing players. Each test delivered separate results and we saw more success with one over the competing two methods.

Along the journey, I was very careful in my attempts to use the data to generate insights in order to answer our primary question. Careful because I did not want to misrepresent the data, create overfitting of our training dataset, or manipulate the results in our favor. I put checks in place to remove features that demonstrate multi-collinearity, insignificant data features and to balance the classes within our data with resampling.

My evaluations of the 3 models chosen resulted in Logistic Regression having the lowest training and testing accuracy while XGBoost demonstrated higher (95.5%) accuracy for both training and testing data.  My Random Forest model delivered the highest accuracy with 99.9% Training and 98.1% Testing.

With the above results in mind, I would still feel more confident with the XGBoost model as the chosen classification technique. XGBoost offers more controls that reduce the risk of overfitting and consistently delivers a higher accuracy rate than Random Forest or Logistic Regression.

