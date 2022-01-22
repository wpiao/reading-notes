# Read: 13 - Linear Regressions - 01/22/2022

`scikit-learn` is a powerful python module for machine learning. It contains function for regression, classfication, clustering, model selection and dimensionality reduction.

- assume `data` is a dictionary
- `data.keys()`: get keys
- `data.DESCR`: get description about data
- `pd.DataFrame(data.data)`: convert to panda data frame

```python
# Scikit learn
from sklearn.linear_model import LinearRegression
# Creae a LinearRegression object
lm = LinearRegression()
lm.fit() # fits a linear model
lm.predict() # predict using the linear model with estimated coefficients
lm.score() # returns the coefficient of determination
```
