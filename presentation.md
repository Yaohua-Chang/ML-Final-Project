
**Transformation of target value**
Machine Learning algorithms work well with features that are normally distributed.

The distribution of target values is positive skewed. 

And in order to solve this problem, we took the log of sale price and made it normally distributed as shown in the figure.

**Identify and Remove Outliers**
Next, we want to remove outliers to improve the accuracy of prediction.

First, I fit a linear regression Ridge model, because it immediately gives good results with default values. My goal here is to use this model to identify outliers.

Then I compute the residuals between the model's predicted sale prices and the true sale prices. The standard deviation of the residuals is calculated, and these residuals greater than three times this standard deviation are removed from the training data.

**Make function**
Here, we use k-fold cross-validation to avoid overfitting.

**ElasticNet**
The main difference between Lasso and Ridge is the penalty term they use. Ridge uses 𝐿2 penalty term which make coefficient of not important features tend to smaller but not 0. Lasso uses 𝐿1 penalty which make coefficient of these not important features tend to 0. Elasticnet has a penalty which is a mix of 𝐿1 and 𝐿2 norms.

**Random forest**
Random forest builds multiple decision trees and merges them together to get a more accurate and stable prediction