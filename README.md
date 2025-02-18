# **Linear Regression**

* Linear regression is a classic supervised learning algorithm used for predicting continuous values. It models the relationship between an independent variable (input, *X*) and a dependent variable (output, *Y*).

**1) Mathematical foundation**

The equation of a simple linear regression (with one feature) is:

$Y = wX + b$

where:

- *Y* is the predicted output;
- *X* is the input feature;
- *w* is the weight (slope of the line);
- *b* is the bias (intercept).

For multiple features (*n* features), the equation can be generalized to:

$Y = w_1X_1 + w_2X_2 + ... + w_nX_n + b$

**2) Cost function**

To measure how well our model is performing, we use the Mean Squared Error (MSE):

$MSE = \frac{1}{m}\sum_{i=1}^{m}(Y_i - \hat{Y_i})^2$

where:

- *m* is the number of samples;
- *$Y_i$* is the actual output;
- *$\hat{Y_i}$* is the predicted output.

Our goal is to minimize this cost function.

**3) Optimization (Gradient Descent)**

We optimize *w* and *b* using Gradient Descent, which updates parameters iteratively:

$w:=w-\alpha \frac{\partial J}{\partial w}$

$b:=b-\alpha \frac{\partial J}{\partial b}$

where:

- $\alpha$ (learning rate) controls the step size;
- $\frac{\partial J}{\partial w}$ and $\frac{\partial J}{\partial b}$ are gradients of the cost function.

The gradients are computed as:

$\frac{\partial J}{\partial w} = -\frac{2}{m}\sum (Y_i - \hat{Y_i})X_i$

$\frac{\partial J}{\partial b} = -\frac{2}{m}\sum (Y_i - \hat{Y_i})$
