# credit_risk_classification
-   In this project we are going to use supervised learning to classify loan data as being high risk or healthy.
-   We will use logistic regrssion to accomplish the task.
-   Since the data class is highly imbalanced we will also use over sampling methods to bring the classes to balance. 
-   We will look at the confusion matrix and some model metrics to measure how well our model performed.
-   Results form the logistic model:

Confusion Matrix

                                    Predicted 0	    Predicted 1
            Actual 0	            18663	    102
            Actual 1	               56	    563

Accuracy Score : 0.99

Balanced Accuracy Score: 0.95

Classification Report

              precision    recall  f1-score   support

           0       1.00      0.99      1.00     18765
           1       0.85      0.91      0.88       619

    accuracy                           0.99     19384
    macro avg       0.92      0.95      0.94     19384
    weighted avg       0.99      0.99      0.99     19384

-   Precision suggest that model is performing well, the accuracy and balnced accuracy scores both suggest model is performing well. Since there is class imabalnce, the results could be suspect. We need to balance the classes for the results to be trustable.

-   Using random over sampling method to balnce the classes, here are the results:
Confusion Matrix

                        Predicted 0	    Predicted 1
        Actual 0	18649	        116
        Actual 1	    4	        615

Balanced Accuracy Score: 0.99

Classification Report

              precision    recall  f1-score   support

           0       1.00      0.99      1.00     18765
           1       0.84      0.99      0.91       619

    accuracy                           0.99     19384
    macro avg       0.92      0.99      0.95     19384
    weighted avg       0.99      0.99      0.99     19384

-   With over sampling to balance the classes, the balanced accuracy score improve from 0.95 to 0.99.
-   The recall improved for high-risk loan from 0.95 to 0.99 meaning that of all the high-risk loans, the model was able to correctly predict 99% as being high-risk.
-   The precison for healthy loan is 0.99 and that for high-risk is 0.84, this means that of the high-risk loan predicted as high-risk, about 84% were actually high-risk.
-   The model seems to be working well based on recall for both classes, precision is good for the healthy class and relatively good for the high-risk class. Generally the model seems to working well and can be used to predict high-risk loan.
