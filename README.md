# SPAM-MAIL-CLASSIFICATION

This Repository was created to showcase how the best performing classification algorithm can be selected for Spam Mail Classification.

**Introduction**

The dataset used in this project is the Spambase Dataset available from the UCI Machine Learning Repository. It can be downloaded from http://archive.ics.uci.edu/ml/datasets/Spambase

The Spambase data set consists of 4,601 e-mails, of which 1,813 are spam (39.4%). The data set archive contains a processed version of the e-mails wherein 57 real-valued features have been extracted and the spam/non-spam label has been assigned.

I compared the performance of 5 classification algorithms on the dataset and measured their performance based on False positive rate, False negative rate and Overall error rate. The best performing classification algorithm was selected on the basis of the best average Overall error rate. I also used K-fold crossvalidation technique to better assess each algorithm.

Below is the list and description of all the classification algorithms used.

**Classification Algorithms:**

1. **Logistic Regression**: Logistic regression is a statistical model that in its basic form uses a logistic function to model a binary dependent variable, although many more complex extensions exist. In regression analysis, logistic regression[1] (or logit regression) is estimating the parameters of a logistic model (a form of binary regression). Mathematically, a binary logistic model has a dependent variable with two possible values, such as pass/fail which is represented by an indicator variable, where the two values are labeled "0" and "1".

2. **K Nearest Neighbors**: In k-NN classification, the output is a class membership. An object is classified by a plurality vote of its neighbors, with the object being assigned to the class most common among its k nearest neighbors (k is a positive integer, typically small). If k = 1, then the object is simply assigned to the class of that single nearest neighbor.

3. **Support Vector Machine**: A support-vector machine constructs a hyperplane or set of hyperplanes in a high- or infinite-dimensional space, which can be used for classification, regression, or other tasks like outliers detection.[3] Intuitively, a good separation is achieved by the hyperplane that has the largest distance to the nearest training-data point of any class (so-called functional margin), since in general the larger the margin, the lower the generalization error of the classifier.

4. **Naive Bayes**: Naive Bayes classifiers are a family of simple "probabilistic classifiers" based on applying Bayes' theorem with strong (naïve) independence assumptions between the features. These classifiers are highly scalable, requiring a number of parameters linear in the number of variables (features/predictors) in a learning problem. Maximum-likelihood training can be done by evaluating a closed-form expression, which takes linear time, rather than by expensive iterative approximation as used for many other types of classifiers.

5. **Random Forest**: Random forests or random decision forests are an ensemble learning method for classification, regression and other tasks that operate by constructing a multitude of decision trees at training time and outputting the class that is the mode of the classes (classification) or mean/average prediction (regression) of the individual trees.[1][2] Random decision forests correct for decision trees' habit of overfitting to their training set.

**PERFORMANCE**

|ALGORITHM  | FOLD NUMBER | FALSE POSITIVE RATE  | FALSE NEGATIVE RATE | OVERALL ERROR RATE|
| :-------------: | :-------------: |:-------------: | :-------------: |:-------------: | 
| Logistic_Regression  | 1 | 0.04078 | 0.12324 | 0.07274 | 
| Logistic_Regression  | 2 | 0.02996 |  0.15025 | 0.08043 | 
| Logistic_Regression  | 3 | 0.06398 |  0.12332 | 0.08804 | 
| Logistic_Regression  | 4 | 0.05226 | 0.11271  | 0.075 | 
| Logistic_Regression  | 5 | 0.05096 | 0.06267  | 0.05543 | 
| K_Nearest_Neighbors  | 1 | 0.05673 | 0.14005 | 0.08903 | 
| K_Nearest_Neighbors  | 2 | 0.04681 |  0.14507 | 0.08804 | 
| K_Nearest_Neighbors  | 3 | 0.08043 |  0.13672 | 0.10326 | 
| K_Nearest_Neighbors  | 4 | 0.06271 | 0.13005 | 0.08804 | 
| K_Nearest_Neighbors  | 5 | 0.09138 | 0.11680 | 0.10108 | 
| Support_Vector_Machine  | 1 | 0.03014 | 0.12324 | 0.06623 | 
| Support_Vector_Machine  | 2 | 0.03558 |  0.11658 | 0.06956 | 
| Support_Vector_Machine  | 3 | 0.05484 |  0.12064 | 0.08152 | 
| Support_Vector_Machine  | 4 | 0.03484 | 0.09248 | 0.05652 | 
| Support_Vector_Machine  | 5 | 0.04569 | 0.07977 | 0.05869 | 
| Naive_Bayes  | 1 | 0.29078 | 0.06442 | 0.20304 | 
| Naive_Bayes  | 2 | 0.24906 | 0.04922 | 0.16521 | 
| Naive_Bayes  | 3 | 0.31809 |  0.04557 | 0.20760 | 
| Naive_Bayes  | 4 | 0.23519 | 0.03757 | 0.16086 | 
| Naive_Bayes  | 5 | 0.27240 | 0.02564 | 0.17826 | 
| Random_Forest  | 1 | 0.02482 | 0.06722 | 0.04125 | 
| Random_Forest  | 2 | 0.02434 |  0.09067 | 0.05217 | 
| Random_Forest  | 3 | 0.04387 |  0.06970 | 0.05434 | 
| Random_Forest  | 4 | 0.01916 | 0.06069  | 0.03478 | 
| Random_Forest  | 5 | 0.02460 | 0.06267  | 0.03913 | 

--------------------------------------------------------------------------------------------------------------------------------------------------------------------

|BEST PERFORMING ALGORITHM  |  AVERAGE FALSE POSITIVE RATE  | AVERAGE FALSE NEGATIVE RATE | AVERAGE OVERALL ERROR RATE|
| :-------------: | :-------------: | :-------------: |:-------------: | 
| Random_Forest  |  0.02736 | 0.07019 | 0.04433 | 

**Note**:\
 FALSE POSITIVE RATE = FALSE POSITIVE / (FALSE POSITIVE + TRUE NEGATIVE)\
 FALSE NEGATIVE RATE = FALSE NEGATIVE / (FALSE NEGATIVE + TRUE POSITIVE)\
 OVERALL ERROR RATE = (FALSE POSITIVE + FALSE NEGATIVE) / ( TRUE NEGATIVE + FALSE POSITIVE + FALSE NEGATIVE + TRUE POSITIVE)

**References:**

1. https://en.wikipedia.org/wiki/Logistic_regression
2. https://en.wikipedia.org/wiki/K-nearest_neighbors_algorithm
3. https://en.wikipedia.org/wiki/Support-vector_machine
4. https://en.wikipedia.org/wiki/Naive_Bayes_classifier
5. https://en.wikipedia.org/wiki/Random_forest
