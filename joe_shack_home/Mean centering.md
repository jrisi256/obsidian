---
aliases:
  - mean centered
  - Mean centered
  - mean centering
  - grand-mean centering
  - Grand-mean centering
---
$$X - \overline{X}$$
* where $X$ is a random variable and $\overline{X}$ is the mean of $X$.

You subtract the mean of $X$ from each observation, essentially. This transforms the mean of your variable to 0. This often done in the context of [[multilevel modeling]] because it transforms the interpretation of the intercept. Traditionally, the intercept is the predicted outcome when the independent variable of interest is 0. With mean centering, the intercept becomes the predicted outcome when the centered independent variable(s) are at their average value (and non-centered independent variable(s) are at 0).

The estimated coefficient for X also takes on a slightly different interpretation where a unit increase in variable $X_1$ from its mean will increase/decrease Y by $\beta_1$.

Variables are also sometimes mean-centered when calculating interaction terms. If you have the equation: $Y = \beta_0 + \beta_1X_1 + \beta_2X_2 + \beta_3(X_1X_2)$, and you mean-centered all the variables, then $\beta_1$ has the interpretation, "A one-unit increase in $X_1$ while all other variables are held constant and $X_2$ is 0, will lead to a $\beta_1$ increase in $Y$." When you mean-center your variables, the interpretation changes to one where $X_2$ is at its mean value.

Mean centering also, critically, can help alleviate concerns of multicollinearity with interaction terms and higher-order polynomial terms.