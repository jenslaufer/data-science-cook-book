# Algorithms

(http://blog.echen.me/2011/04/27/choosing-a-machine-learning-classifier/)


## Gaussian Naive Bayes

### Pros

   - Simple
   - Less training data is needed
   - Naïve Bayes Classifier algorithm performs well when the input variables are categorical.
   - A Naïve Bayes classifier converges faster, requiring relatively little training data than other discriminative models like logistic regression, when the Naïve Bayes conditional independence assumption holds.
   - With Naïve Bayes Classifier algorithm, it is easier to predict class of the test data set. A good bet for multi class predictions as well.
   - Though it requires conditional independence assumption, Naïve Bayes Classifier has presented good performance in various application domains.

### Cons

   - Problems when features are correlated


### Example

   - Spam filtering (https://www.dezyre.com/article/top-10-machine-learning-algorithms/202)
   - Document categorization

### When to use

   - If you have a moderate or large training data set.
   - If the instances have several attributes.
   - Given the classification parameter, attributes which describe the instances should be conditionally independent.




## Decision Trees


### Pros

   - Decision trees are very instinctual and can be explained to anyone with ease. People from a non-technical background, can also decipher the hypothesis drawn from a decision tree, as they are self-explanatory.
   - When using decision tree machine learning algorithms, data type is not a constraint as they can handle both categorical and numerical variables.
	- Decision tree machine learning algorithms do not require making any assumption on the linearity in the data and hence can be used in circumstances where the parameters are non-linearly related. These machine learning algorithms do not make any assumptions on the classifier structure and space distribution.
	- These algorithms are useful in data exploration. Decision trees implicitly perform feature selection which is very important in predictive analytics. When a decision tree is fit to a training dataset, the nodes at the top on which the decision tree is split, are considered as important variables within a given dataset and feature selection is completed by default.
	- Decision trees help save data preparation time, as they are not sensitive to missing values and outliers. Missing values will not stop you from splitting the data for building a decision tree. Outliers will also not affect the decision trees as data splitting happens based on some samples within the split range and not on exact absolute values.

### Cons

### Examples

### When to use

   - Decision trees are robust to errors and if the training data contains errors- decision tree algorithms will be best suited to address such problems.
   - Decision trees are best suited for problems where instances are represented by attribute value pairs.
   - If the training data has missing value then decision trees can be used, as they can handle missing values nicely by looking at the data in other columns.
   - Decision trees are best suited when the target function has discrete output values.



## Ensemble Methods (Bagging, AdaBoost, Random Forest, Gradient Boosting)



### Pros

### Cons

### Example)

### When to use



## K-Nearest Neighbors 


### Pros

### Cons

### Example)

### When to use



## Stochastic Gradient Descent Classifier (SGDC)



### Pros

### Cons

### Example)

### When to use



## Support Vector Machines (SVM)


### Pros

   - SVM offers best classification performance (accuracy) on the training data.
   - SVM renders more efficiency for correct classification of the future data.
   - The best thing about SVM is that it does not make any strong assumptions on data.
   - It does not over-fit the data.

### Cons

### Examples

SVM is commonly used for stock market forecasting by various financial institutions. For instance, it can be used to compare the relative performance of the stocks when compared to performance of other stocks in the same sector. The relative comparison of stocks helps manage investment making decisions based on the classifications made by the SVM learning algorithm.


### When to use


## Logistic Regression


### Pros

   - Fast, Simple

### Cons

### Example)

### When to use





## Suitable Algorithms


### Fast learning


### Fast prediction


### Size Data set

#### small

#### moderate

   - Naive Bayes

#### large

   - Naive Bayes


### Number of features