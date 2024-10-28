### Conclusion:
##Test/Training Accuracy Results
Prior to improving the model, Decision Tree had the highest training accuracy at 0.9954 but also the lowest test accuracy at 0.8375. This would suggest overfitting could be occuring in the model. The SVM model had the longest training time by a wide margin at 27.22s whereas Log Regression was at 2.58s and the others were at 0.01 and 0.32. This could be because the algorithm of the vector. Logistric Regression had the highest test accuracy at 0.8963 with SVM close behind at 0.8948.

In short, Log Regression produced the best results so that would be the best model to use.

After changing the train/test split to 40/60, SVM training time went down to 6.97s. Decision Tree still had the highest training accuracy at 0.9975. Once again, Log regression produced the best results with the highest test accuracy at 0.8988. Overall, there were slight improvements in the majority of the categories, training time went down, training accuracy increased slightly, and test accuracy increased slightly. Log Regression is still the best model to use.

##Grid Search and ROC Curves Results
Prior to using the grid search, the Log Regression had the highest AUC of 0.78, KNN had an AUC of 0.72, Decision Tree had an AUC of 0.62, and SVM had an AUC of 0.65. For Decision Tree and SVM the ROC has oddly shapped to say the least.

After using Grid Search, I was able to find the following:

Decision Tree:
Best Parameters: {'criterion': 'entropy', 'max_depth': 5, 'max_features': None, 'min_samples_leaf': 1, 'min_samples_split': 5, 'splitter': 'random'}.

Best Score for Decision Tree was 0.9019119878603945.

KNN:
Best Parameters for KNN: {'metric': 'manhattan', 'n_neighbors': 11, 'weights': 'uniform'}.

Best Score for KNN: 0.8977238239757208.

Log Regression:
Best Parameters for Logistic Regression: {'C': 0.1, 'penalty': 'l2'}

Logistic Regression Score with Grid Search: 0.8980293772508396

SVM:
Best Parameters for Linear SVC: {'C': 0.01}

SVC Score with Grid Search: 0.8966131186015458

The ROC curves for each method also changed: Log Regression regressed to 0.76, KNN had an AUC of 0.76, Decision tree improved to 0.78, and SVM also improved to 0.76. The shape looked alot better for all models. Overall, it seems like Decision Tree produced the best outputs. I personally would still use Logistic Regression due to potential overfitting.
