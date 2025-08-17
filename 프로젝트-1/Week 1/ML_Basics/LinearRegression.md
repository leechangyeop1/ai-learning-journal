# Linear Regression

## Introduction
Linear regression is a fundamental statistical method used to model the relationship between a dependent variable and one or more independent variables. It assumes that there is a linear relationship between the input variables (features) and the output variable (target).

## Mathematical Representation
The linear regression model can be represented mathematically as:

Y = β0 + β1X1 + β2X2 + ... + βnXn + ε

Where:
- Y is the dependent variable (target).
- β0 is the y-intercept.
- β1, β2, ..., βn are the coefficients of the independent variables.
- X1, X2, ..., Xn are the independent variables (features).
- ε is the error term.

## Key Concepts
1. **Assumptions**: Linear regression relies on several key assumptions:
   - Linearity: The relationship between the independent and dependent variables is linear.
   - Independence: The residuals (errors) are independent.
   - Homoscedasticity: The residuals have constant variance at every level of X.
   - Normality: The residuals of the model are normally distributed.

2. **Cost Function**: The most common cost function used in linear regression is the Mean Squared Error (MSE), which measures the average of the squares of the errors.

   MSE = (1/n) * Σ(Yi - Ŷi)²

   Where:
   - Yi is the actual value.
   - Ŷi is the predicted value.
   - n is the number of observations.

3. **Gradient Descent**: This is an optimization algorithm used to minimize the cost function by iteratively adjusting the coefficients (β values) in the direction of the steepest descent.

## Example
Consider a simple example where we want to predict the price of a house based on its size:

- **Dataset**:
  | Size (sq ft) | Price ($) |
  |--------------|-----------|
  | 1500         | 300,000   |
  | 1600         | 320,000   |
  | 1700         | 340,000   |
  
- **Model**: After applying linear regression, we might find a model like:

  Price = 100,000 + 125 * Size

This indicates that for every additional square foot, the price increases by $125.

## Conclusion
Linear regression is a powerful and widely used technique in data science and machine learning for predictive modeling. Understanding its principles and applications is essential for anyone looking to work in these fields.