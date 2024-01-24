# Detecting-Early-Alzheimer
Detecting Early Alzheimer’s


Exploratory Data Analysis

The Correlation heatmap was extremely useful in determining which columns are strongly correlated-
Now, picking up the most correlated columns with MMSE are Total Hippocampus Volume and Cdr. The column Age, Cortex Volume and total gray volume are also showing some average correlation with MMSE. 
Among all these the Hippocampus Volume is one of the factors that helps to detect the early Alzheimer.
When we check out how the distinct groups have the distribution of hippocampus volume, we reconfirmed that the people having high MMSE values also have more hippocampus volume hence low chance of AD.
 

Modelling
We started training our model with different machine learning techniques to find the best model which can be trained on our training dataset giving highest accuracy on the test dataset. The team's primary intention was to explore how machine learning can make a difference in the clinical environment.
For that we have developed several algorithms which perform at a good accuracy level. Below are the different types of models we ran,
Model Name 	Accuracy (%) 
Deep Learning Model (SGD)	91.30%
Change of Solver optimizer in MLP	89.30%
MLP	89.10%
Random Forest Classifier	88.46%
Logistic Regression	88.07%
MLP with early stopping	87.80%
Decision Tree	87.47%
AdaBoost	87.07%

After running above models, we found the SGD as the best model with highest accuracy on the test dataset. 
1) Logistic Regression:
Logistic Regression is a supervised learning classification algorithm used to predict the probability of a target variable. Mathematically, a logistic regression model predicts P(Y=1) as a function of X. It is one of the simplest ML algorithms that can be used for various classifications problems such as Alzheimer detection and many other.
The Y-of the Logistic Regression
During our Alzheimer detection experiment We have used “Group” as a target variable which is a multi-class variable having following classes:
•	NormalCognition
•	MildDementia
•	ModerateDementia
•	SevereDementia
Hence, we have used One-vs-rest (OvR) method which is a heuristic method for using binary classification algorithms for multi-class classification problems. 
The X-of the Logistic Regression
•	IntraCranialVol
•	CortexVol
•	TotalGrayVol
•	CorticalWhiteMatterVol
•	TOTAL_HIPPOCAMPUS_VOLUME
•	cdr
•	apoe
•	Age
•	Education
•	M/F
Results using Logistic Regression: The accuracy of the model is 88.07% (Coefficient of determination) which says that 90.45 % accurately the observed outcomes are replicated by model.
2) Random Forest Classifier:
This works by using a collection of multiple random decision trees and it’s much less sensitive to the training data and hence a change in training data creates low variance. Here, we use multiple trees and so it is called Forest. Random forest helps reduce overfitting in decision trees and helps to improve accuracy. This technique has a capability to focus both on observations and variables of a training data for developing individual decision trees and take maximum voting for classification. 
Training Model
Here we are building new data sets randomly from our original data by keeping the same number of rows. In our experiment we are creating random trees with estimators, random feature selections and then feeding to our RandomForestClassifier, values for number of trees, depth of trees and number of features are obtained from loops. After the model is built, we are performing k-fold cross validation in our experiment its 5-fold cross validation. After this we are computing mean cross-validation accuracy and storing better scores.
These steps are repetitively performed in each iteration of for loop.
Rebuilding model 
In this step we rebuild a model on the combined training and validation set then we predict model accuracy based on best accuracy on validation set, best parameters and Test accuracy with best paraments
Results:
Best accuracy on validation set is: 92%
Best parameters of M, d, m is: 12 ,5, 8
Test accuracy with the best parameters is: 88.46%
This shows that our model can predict with 88 % accuracy given patients data.


 	
3) AdaBoost:
AdaBoost was the first truly successful boosting algorithm created specifically for binary classification. Adaptive Boosting, or AdaBoost, is a prominent boosting strategy that combines several "weak classifiers" into a single "strong classifier." The weak learners in AdaBoost are decision trees with a single split, called decision stumps. AdaBoost works by putting more weight on difficult to classify instances and less on those already handled well. AdaBoost allows us to capture many of these non-linear relationships, which translates into better prediction accuracy on the problem of interest.  Most of the research papers we read used this model for predictions which intrigued us and thus led to us exploring how well this model will do compared to others. Interestingly, other models performed much better than this traditional approach. 
Training Model
We again iterate over loops to obtain the best values for our model parameters: n_estimators and learning_rate. The maximum number of estimators at which boosting is terminated is an important parameter as it determines the learning procedure. Learning rate is defined as the weight applied to each classifier at each boosting iteration. A higher learning rate increases the contribution of each classifier. There is a trade-off between the learning_rate and n_estimators parameters. A cross validation procedure is performed thereafter. After this we rebuild the model on the combined training and validation set. 
Results:
Best accuracy on validation set is: 0.9091
Best parameter of M is: 4
Best parameter of LR is: 0.1
Test accuracy with the best parameter is 0.8707



Sources
https://www.kaggle.com/jboysen/mri-and-alzheimers
https://www.kaggle.com/hyunseokc/detecting-early-alzheimer-s
