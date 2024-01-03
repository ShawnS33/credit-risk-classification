# Module 12 Report Template

## Overview of the Analysis

In this section, describe the analysis you completed for the machine learning models used in this Challenge. This might include:

* Explain the purpose of the analysis.
The objective was to assess the accuracy of the logistic regression model in predicting healthy loans versus high-risk loans, comparing its performance on the original dataset against resampled data, aimed at augmenting the size of the minority class.

* Explain what financial information the data was on, and what you needed to predict.
The aim was to evaluate the logistic regression model's accuracy in predicting loan status and risk assessment, considering both the original dataset and resampled data designed to augment the size of the minority class.

* Provide basic information about the variables you were trying to predict (e.g., `value_counts`).
The original data showed a count of 75,036 for the Zero class and 2,500 for the One class. After oversampling, the counts were adjusted to 56,271 for both the Zero and One classes, ensuring a balanced representation of both classes in the dataset

* Describe the stages of the machine learning process you went through as part of this analysis.
In the initial step, we prepared our data by separating it into X and Y columns, where X represents the features, and Y represents the outcome. Subsequently, we performed a train-test split on the data, allocating 75% for training and 25% for testing. We then selected the logistic regression model for classification. Following this, we trained the model using the training data. Once trained, we utilized the model to make predictions on the test data, comprising 25% of the overall dataset. In the final step, we evaluated the predictions by examining various metrics, including the confusion matrix and classification report

* Briefly touch on any methods you used (e.g., `LogisticRegression`, or any resampling method).
Panda Data Frames
SKLearn LogisticRegression
Train_test_split
Confusion_matrix
Classification report

## Results

Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all machine learning models.

* Machine Learning Model 1:
  * Description of Model 1 
  Accuracy: 0.99 
  Precision: 1.00, Class: 0.85  
  Recall scores: 0.99, Class 1: 0.91



* Machine Learning Model 2:
  Accuracy: 0.99 
  Precision: 1.00, Class 1: 0.84  
  Recall scores: 0.99, Class 1: 0.99

## Summary

Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. For example:
* Which one seems to perform best? How do you know it performs best?
The Logistic Regression model demonstrated strong performance, particularly in predicting the outcome of healthy loans (class Zero). Both precision and recall metrics indicated highly accurate results for this class, showcasing the model's effectiveness in making accurate predictions for loans categorized as Zero.


* Does performance depend on the problem we are trying to solve? (For example, is it more important to predict the `1`'s, or predict the `0`'s? )
For the high-risk loans (class One), the Logistic Regression model exhibited a precision of 0.84 and a recall of 0.91. These metrics suggest that the model tends to generate more false positives than false negatives. Despite this, considering the provided information, it appears that the Logistic Regression model performs admirably in predicting both healthy and high-risk loans, given the specific columns used in the training set data.


If you do not recommend any of the models, please justify your reasoning.

While the Logistic Regression model shows promise in predicting the health status of loans, a comprehensive evaluation against various datasets is essential to validate its robustness and generalizability. Testing the model against diverse datasets ensures that its performance is not specific to a particular set of circumstances and provides more confidence in its suitability for predicting loan health status across different scenarios.