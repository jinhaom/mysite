---
title: "Logistic Model"
date: 2021-12-16T23:08:20+08:00
summary: A tiny brief on logistic models
featuredImage: http://cloud.csss.co/pictures/logistic.png
featuredImagePreview: https://ambrapaliaidata.blob.core.windows.net/ai-storage/articles/MA_Au2YNN4.jpg
---

# Logistic Models

Sometimes we only need an indicator. Logistic regression can be used to estimate the probability that the future reutrn will turn up or down.

## Binary-choice response

### Example

Consider the financial status of a business firm which can be produced information to creditors, investors, stockholders and others for making decision. 

Suppose that we want to use financial information for predicting financial health of companies, where the response variable ($Y$) is assigned to failure companies for 0 and healthy companies for 1 and five explanatory varaibles are considered to explain the financial health, including 

- working capital to total assets ($X_1$),

- retained earning to total assets ($X_2$),

- earning before interest and taxes to total assets ($X_3$),

- net income (loss) to amount of shares ($X_4$), and

- sales to total sales ($X_5$).

## Problems of fitting a linear regression model with binary response

### Normality assumption not hold anymore

Actually the response variable $Y_i$ follows binomial distribution, with a probability of a success $\pi_{x_i} = P(Y_i = 1 |\bf{x_i})$

### Constant variance not satisfy

### Fundamental problem with the assumtion of linearity

## Some transformations

Here we do some transformations (called linear transformation) to find a proper function describing these relationships.

$$
P(Y_i = 1|x_{i1}) = E(Y_i) = g[\beta_0 +\beta_1x_{i1}]
$$

## Logistic/ Sigmoid function

It is defined by 

$$
g(t) = \frac{1}{1+e^{-t}}=\frac{e^t}{1+e^t}
$$

where $g$ is between 0 and 1.

As logistic function produces a smooth output between 0 and 1, we need *one more* thing to make it a **classifier**. 

$$
\text{Guess for } Y = 1. \text{ if } P(Y=1|\mathbf{x})>0.5, \text{ else }=0
$$

The decision boundary is $\mathbf{x^TB}=0$.

### To find parameters

There is no closed form for solving logistic formulation. We form a cost function and solve it by gradient decent algorithm.



