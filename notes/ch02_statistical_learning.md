# Chapter 2 - Statistical Learning

## Input and Output Variables #
Input variables are typically $X$ with subscript to distinguish them: $X_1$, $X_2$, $X_3$ ... $X_P$  

Output variables (response, dependent) are typically $Y$.

Generally, if we see a quantitative response $Y$ for $p$ different predictors ($X_1$, $X_2$, $X_3$ ... $X_P$) we assume that there is a relationship between $Y$ and said $X$'s, written generally as:
<div align="center">

$Y$ = $f$(X) + $\epsilon$ (where $\epsilon$ is the error term)

</div>
Error terms are independent of $X$ and have approx. mean zero.

## Prediction vs. Inference #

The goal controls the model choice. For prediction, flexible models are often more accurate but harder to interpret. For inference, simple models are easier to interpret but can be less accurate. 

### Prediction #

You want a good value for $\hat{Y}$. You don't care how $\hat{f}$ works, and it can be a "black box". 

Sets of inputs $X$ are usually readily available, but $Y$ is not easily obtained. Since the error term is usually mean zero, we can predict $Y$ using:

<div align="center">

$\hat{Y}$ = $\hat{f}(X)$

</div>

Where $\hat{f}$ is our estimate for $f$, and $\hat{Y}$ represents the resulting prediction of $Y$.

The accuracy of this depends on reducible error and irreducible error: 

- Reducible error can be improved by using the most appropriate statistical learning technique to estimate $f$.


- Irreducible error is always going to be there because variability associated with $\epsilon$ which affects the accuracy of predictions. No matter how well we estimate $f$, we cannot reduce the error introduced by $\epsilon$.

### Inference #

You want to be able to understand how $X$ changes $Y$. 

Typical questions:

- Which predictors are related to $Y$?
- Is each relation positive or negative?
- Is the relation linear or more complex?

## How do we estimate $f$? #

### Parametric Methods # 

These assume a functional form of $f$ and assign coefficients to the parameters:

$f(X)$ = $\beta_0$ + $\beta_1$ $X_1$ + $\beta_2$ $X_2$ + ... + $\beta_p$ $X_p$

Above is a linear model example, but after any model is selected for estimating $f$, we need a procedure that uses training data to fit the model. 

In the linear example we need to estimate the parameters ($\beta_0$, $\beta_1$, $\beta_2$, $\beta_P$) such that $Y$ = the whole equation above. 

Overfitting is when models follow noise or errors to closely and wrongly estimate parameters based on said error, leading to bad real prediction.

### Non-Parametric Methods # 

These do not make an assumption about the general form of $f$. Instead they seek an estimate of $f$ that gets as close to the data points as possible without being too rough or wiggly. 

Since these do not reduce the problem of estimating $f$ to a small number of parameters, a very large number of observations is needed to obtain an accurate estimate of $f$

## Assessing Model Accuracy #

### Measuring the Quality of Fit #

We need a way to measure how close predictions are to the true values. In regression, the usual measure is the mean squared error (MSE):

$$MSE = \frac{1}{n}\sum_{i=1}^{n}(y_i - \hat{f}(x_i))^2$$

$\hat{f}(x_i)$ is the prediction that $\hat{f}$ gives for the $i$th observation. MSE is small if predictions are close to the true values. MSE is large if they differ a lot. When computed on the data used to fit the model, this is the training MSE.

What we actually care about is performance on new, unseen data, the test MSE:

$$\text{Ave}(y_0 - \hat{f}(x_0))^2$$

We want the method with the lowest test MSE, not the lowest training MSE. A low training MSE can just mean the model overfits.

As flexibility increases, training MSE keeps falling because the model fits the training data more and more closely, including its random noise.

Past a point, test MSE rises: the model learned patterns that do not exist in new data: overfitting.

### The Bias-Variance Trade-Off #

$$E(y_0 - \hat{f}(x_0))^2 = \text{Var}(\hat{f}(x_0)) + [\text{Bias}(\hat{f}(x_0))]^2 + \text{Var}(\epsilon)$$

Variance: how much $\hat{f}$ changes with a different training set. High for flexible models. 

Bias$^2$: error from a model too simple for the true $f$. High for rigid models.

$\text{Var}(\epsilon)$: irreducible noise. Test MSE can never go below it.

More flexibility generally produce lower bias and higher variance. Best model balances both: U-shaped test MSE curve. 

For classification models, $y_i$ is no longer quantitative and is qualitative. Quantifying the accuracy of the model is commonly using the training error rate (proportion of right and wrong classifications):

$$\frac{1}{n}\sum_{i=1}^{n} I(y_i \neq \hat{y}_i)$$

The test error rate for new, unseen observations is given by:

$$\text{Ave}(I(y_0 \neq \hat{y}_0))$$

Obviously, a good classifier is one with the smallest test error rate. 

#### The Bayes Classifier #

It is possible to show that the test error rate is minimized, on average, by a simple classifier that assigns each observation to the most likely class, given its predictor values. The equation below is a conditional probability:

$$\Pr(Y = j \mid X = x_0)$$

For two classes, this predicts class 1 if $\Pr(Y = 1 \mid X = x_0) > 0.5$, and class 2 otherwise. 

#### KNN #





