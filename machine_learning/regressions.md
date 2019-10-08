## Logistic Regression

Logistic regression does not make many of the key assumptions of linear regression and general linear models that are based on ordinary least squares algorithms – particularly regarding linearity, normality, homoscedasticity, and measurement level.

### Assumptions

Note required:

- does not require a linear relationship between the dependent and independent variables
- error terms (residuals) do not need to be normally distributed
- homoscedasticity is not required

Required:

- binary logistic regression requires the dependent variable to be binary and ordinal logistic regression requires the dependent variable to be ordinal.
- The observations should be independent of each other.  In other words, the observations should not come from repeated measurements or matched data.
- There is little or no multi-collinearity among the independent variables.  This means that the independent variables should not be too highly correlated with each other.

## Refs

- https://www.statisticssolutions.com/assumptions-of-logistic-regression/
- Homoscedasticity: The assumption of homoscedasticity (meaning “same variance”) is central to linear regression models. Homoscedasticity describes a situation in which the error term (that is, the “noise” or random disturbance in the relationship between the independent variables and the dependent variable) is the same across all values of the independent variables. Heteroscedasticity (the violation of homoscedasticity) is present when the size of the error term differs across values of an independent variable. The impact of violating the assumption of homoscedasticity is a matter of degree, increasing as heteroscedasticity increases.
