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

### When to use?

   - If you have a moderate or large training data set.
   - If the instances have several attributes.
   - Given the classification parameter, attributes which describe the instances should be conditionally independent.




## Decision Trees


### Pros

   	+ Decision trees are very instinctual and can be explained to anyone with ease. People from a non-technical background, can also decipher the hypothesis drawn from a decision tree, as they are self-explanatory.
   - When using decision tree machine learning algorithms, data type is not a constraint as they can handle both categorical and numerical variables.
	- Decision tree machine learning algorithms do not require making any assumption on the linearity in the data and hence can be used in circumstances where the parameters are non-linearly related. These machine learning algorithms do not make any assumptions on the classifier structure and space distribution.
	- These algorithms are useful in data exploration. Decision trees implicitly perform feature selection which is very important in predictive analytics. When a decision tree is fit to a training dataset, the nodes at the top on which the decision tree is split, are considered as important variables within a given dataset and feature selection is completed by default.
	- Decision trees help save data preparation time, as they are not sensitive to missing values and outliers. Missing values will not stop you from splitting the data for building a decision tree. Outliers will also not affect the decision trees as data splitting happens based on some samples within the split range and not on exact absolute values.

### Cons

	- The more the number of decisions in a tree, less is the accuracy of any expected outcome.
	- A major drawback of decision tree machine learning algorithms, is that the outcomes may be based on expectations. When decisions are made in real-time, the payoffs and resulting outcomes might not be the same as expected or planned. There are chances that this could lead to unrealistic decision trees leading to bad decision making. Any irrational expectations could lead to major errors and flaws in decision tree analysis, as it is not always possible to plan for all eventualities that can arise from a decision.
	- Decision Trees do not fit well for continuous variables and result in instability and classification plateaus.
	- Decision trees are easy to use when compared to other decision making models but creating large decision trees that contain several branches is a complex and time consuming task.
	- Decision tree machine learning algorithms consider only one attribute at a time and might not be best suited for actual data in the decision space.
	Large sized decision trees with multiple branches are not comprehensible and pose several presentation difficulties.

### Examples

	- Decision trees are among the popular machine learning algorithms that find great use in finance for option pricing.
	Remote sensing is an application area for pattern recognition based on decision trees.
	- Decision tree algorithms are used by banks to classify loan applicants by their probability of defaulting payments.
	- Gerber Products, a popular baby product company, used decision tree machine learning algorithm to decide whether they should continue using the plastic PVC (Poly Vinyl Chloride) in their products.
	- Rush University Medical Centre has developed a tool named Guardian that uses a decision tree machine learning algorithm to identify at-risk patients and disease trends.

### When to use?

   - Decision trees are robust to errors and if the training data contains errors- decision tree algorithms will be best suited to address such problems.
   - Decision trees are best suited for problems where instances are represented by attribute value pairs.
   - If the training data has missing value then decision trees can be used, as they can handle missing values nicely by looking at the data in other columns.
   - Decision trees are best suited when the target function has discrete output values.



## Ensemble Methods (Bagging, AdaBoost, Random Forest, Gradient Boosting)



### Pros

	- Overfitting is less of an issue with Random Forests, unlike decision tree machine learning algorithms. There is no need of pruning the random forest.
	- These algorithms are fast but not in all cases. A random forest algorithm, when run on an 800 MHz machine with a dataset of 100 variables and 50,000 cases produced 100 decision trees in 11 minutes.
	- Random Forest is one of the most effective and versatile machine learning algorithm for wide variety of classification and regression tasks, as they are more robust to noise.
	- It is difficult to build a bad random forest. In the implementation of Random Forest Machine Learning algorithms, it is easy to determine which parameters to use because they are not sensitive to the parameters that are used to run the algorithm. One can easily build a decent model without much tuning.
	- Random Forest machine learning algorithms can be grown in parallel.
	- This algorithm runs efficiently on large databases.
	- Has higher classification accuracy.


### Cons

	-  They might be easy to use but analysing them theoretically, is difficult.
	- Large number of decision trees in the random forest can slow down the algorithm in making real-time predictions.
	- If the data consists of categorical variables with different number of levels, then the algorithm gets biased in favour of those attributes that have more levels. In such situations, variable importance scores do not seem to be reliable.
	- When using RandomForest algorithm for regression tasks, it does not predict beyond the range of the response values in the training data.

### Examples

	- Random Forest algorithms are used by banks to predict if a loan applicant is a likely high risk.
	- They are used in the automobile industry to predict the failure or breakdown of a mechanical part.
	- These algorithms are used in the healthcare industry to predict if a patient is likely to develop a chronic disease or not.
	- They can also be used for regression tasks like predicting the average number of social media shares and performance scores.
	- Recently, the algorithm has also made way into predicting patterns in speech recognition software and classifying images and texts.

### When to use?

	- There are many good open source, free implementations of the algorithm available in Python and R.
	- It maintains accuracy when there is missing data and is also resistant to outliers.
	- Simple to use as the basic random forest algorithm can be implemented with just a few lines of code.
	- Random Forest machine learning algorithms help data scientists save data preparation time, as they do not require any input preparation and are capable of handling numerical, binary and categorical features, without scaling, transformation or modification.
	- Implicit feature selection as it gives estimates on what variables are important in the classification.



## Logistic Regression 


### Pros

	- Easier to inspect and less complex.
	- Robust algorithm as the independent variables need not have equal variance or normal distribution.
	- These algorithms do not assume a linear relationship between the dependent and independent variables and hence can also handle non-linear effects.
	- Controls confounding and tests interaction.

### Cons

	- When the training data is sparse and high dimensional, in such situations a logistic model may over fit the training data.
	- Logistic regression algorithms cannot predict continuous outcomes. For instance, logistic regression cannot be applied when the goal is to determine how heavily it will rain because the scale of measuring rainfall is continuous. Data scientists can predict heavy or low rainfall but this would make some compromises with the precision of the dataset.
	- Logistic regression algorithms require more data to achieve stability and meaningful results. These algorithms require minimum of 50 data points per predictor to achieve stable outcomes.
	- It predicts outcomes depending on a group of independent variables and if a data scientist or a machine learning expert goes wrong in identifying the independent variables then the developed model will have minimal or no predictive value.
	- It is not robust to outliers and missing values.

### Examples

	- Logistic regression algorithm is applied in the field of epidemiology to identify risk factors for diseases and plan accordingly for preventive measures.
	- Used to predict whether a candidate will win or lose a political election or to predict whether a voter will vote for a particular candidate.
	- Used to classify a set of words as nouns, pronouns, verbs, adjectives.
	- Used in weather forecasting to predict the probability of rain.
	- Used in credit scoring systems for risk management to predict the defaulting of an account.

### When to use?

	- Use logistic regression algorithms when there is a requirement to model the probabilities of the response variable as a function of some other explanatory variable. For example,  probability of buying a product X as a function of gender
	- Use logistic regression algorithms when there is a need to predict probabilities that categorical dependent variable will fall into two categories of the binary response as a function of some explanatory variables. For example, what is the probability that a customer will buy a perfume given that the customer is a female?
	- Logistic regression algorithms is also best suited when the need is to classify elements two categories based on the explanatory variable. For example-classify females into ‘young’ or ‘old’ group based on their age.




## Support Vector Machines (SVM)


### Pros

   - SVM offers best classification performance (accuracy) on the training data.
   - SVM renders more efficiency for correct classification of the future data.
   - The best thing about SVM is that it does not make any strong assumptions on data.
   - It does not over-fit the data.

### Cons

### Examples

	- SVM is commonly used for stock market forecasting by various financial institutions. For instance, it can be used to compare the relative performance of the stocks when compared to performance of other stocks in the same sector. The relative comparison of stocks helps manage investment making decisions based on the classifications made by the SVM learning algorithm.


### When to use?





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