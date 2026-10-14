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

### How do we estimate $f$? #