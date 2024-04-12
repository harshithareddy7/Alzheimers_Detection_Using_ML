# Alzheimer-s_Detection_Using_Machine_Learning

### Description:

This code aims to detect Alzheimer's Disease using machine learning techniques. It includes data preprocessing, exploratory data analysis, feature engineering, and the training of several machine learning models. The code also uses ensemble methods like Random Forest and Support Vector Machine (SVM) to improve classification performance.

### Code Overview:

#### Importing Libraries: 
The code starts by importing necessary libraries for data manipulation, visualization, and machine learning.

#### Data Loading and Exploration: 
It loads the Alzheimer's dataset from a CSV file and performs an initial exploration of the data, including checking for missing values and correlation analysis.

#### Data Preprocessing:
Some columns are dropped as they are not needed for the analysis.
The 'Group' column is transformed into binary values (1 for Demented, 0 for Nondemented).
The 'M/F' column is transformed into binary values (1 for Male, 0 for Female).
Missing values in the 'SES' and 'MMSE' columns are imputed using the most frequent value and median, respectively.
The data is normalized using StandardScaler.

#### Data Splitting: 
The dataset is split into training and testing sets.

##### Support Vector Machine (SVM):
Hyperparameter tuning is performed for the SVM classifier using GridSearchCV to find the best combination of parameters.
The code uses 20-fold cross-validation and the ROC AUC score as the evaluation metric.
The best SVM model is trained on the entire dataset.

### Ensemble Learning for Predictive Modeling
This code implements ensemble learning techniques for predictive modeling. It utilizes several ensemble algorithms to predict outcomes based on a given dataset.

Models Used
##### Random Forest (RF):
Hyperparameter tuning is performed for the Random Forest classifier using RandomizedSearchCV.
The code tests various combinations of hyperparameters such as the number of estimators, maximum depth, and minimum samples to split.
The best RF model is trained on the training data.

##### AdaBoost (ADA):
Adaptive boosting technique that combines multiple weak learners to create a strong learner.
Feature importances have been calculated and visualized.

##### Gradient Boosting (GB):
Ensemble technique that builds multiple decision trees sequentially to improve prediction accuracy.
Feature importances have been calculated and visualized.

##### Extra Trees (ET):
Ensemble method similar to Random Forest but with differences in the way trees are constructed.
Feature importances have been calculated and visualized.

##### XGBoost (XGB)
An optimized and efficient gradient boosting library.
Feature importances have been calculated and visualized.

#### Feature Importance Visualization
Feature importances for each model have been computed and plotted as scatter plots to demonstrate the importance of different features in the prediction process. This helps in understanding which features are most influential in the models' predictions.

#### Model Evaluation
The models have been evaluated using various performance metrics such as accuracy, recall, and AUC (Area Under the Curve). These metrics provide insights into how well the models perform in classifying data points.

#### Results
The performance metrics for each model are as follows:

Random Forest (RF)

Accuracy: 0.807
Recall: 0.818
AUC: 0.759
AdaBoost (ADA)

Accuracy: 0.814
Recall: 0.795
AUC: 0.728
Gradient Boosting (GB)

Accuracy: 0.817
Recall: 0.864
AUC: 0.862
Extra Trees (ET)

Accuracy: 0.878
Recall: 0.841
AUC: 0.820
Support Vector Machine (SVM)

Accuracy: 0.799
Recall: 0.795
AUC: 0.788
XGBoost (XGB)

Accuracy: 0.824
Recall: 0.818
AUC: 0.789

### Conclusion
Ensemble learning techniques such as Random Forest, AdaBoost, Gradient Boosting, Extra Trees, Support Vector Machine, and XGBoost have been applied to the dataset, and their performance has been evaluated. Among these models, Extra Trees and Gradient Boosting have demonstrated the highest accuracy and recall, making them potential candidates for further consideration in predictive modeling tasks.
