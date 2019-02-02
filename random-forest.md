---
title: Random Forest
category: Others
layout: sheet
tags: [Featured]
updated: 2019-02-02
keywords:
  - Random Forest
  - Bagging
  - Tree
---



Getting started
---------------
{: .-two-column}


### Explanation

A Random Forest is a method of classification and regression that works by constructing a multitude of Decision Trees. Each of these trees will output a prediction.

**Classification**: The prediction of the Random Forest is the class that is predicted by the most Decision Trees.

**Regression**: The prediction of the Random Forest is the mean of all the predictions from all the Decision Trees.


### Schema for Classification

![randomForest classifier](images/randomforest.png)


How do I code it?
---------------
{: .-two-column}

### Scikit-learn

```python
from sklearn.ensemble import RandomForestClassifier
from sklearn.datasets import make_classification

X, y = make_classification(n_samples=1000, n_features=4,
                           n_informative=2, n_redundant=0,
                           random_state=0, shuffle=False)
clf = RandomForestClassifier(n_estimators=100, max_depth=2,
                             random_state=0)
clf.fit(X, y)

print(clf.feature_importances_)  # [0.14205973 0.76664038 0.0282433  0.06305659]
print(clf.predict([[0, 0, 0, 0]]))  # [1]
```

### R

```Rscript
require(randomForest)
require(MASS)#Package which contains the Boston housing dataset
attach(Boston)
set.seed(101)

train=sample(1:nrow(Boston),300)
Boston.rf=randomForest(medv ~ . , data = Boston , subset = train)
Boston.rf

plot(Boston.rf)
```
