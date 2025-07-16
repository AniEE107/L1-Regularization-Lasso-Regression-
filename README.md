# L1-Regularization-Lasso-Regression-
This Jupyter Notebook demonstrates L1 Regularization (Lasso Regression). It applies Lasso with varying alpha values to synthetic regression data, illustrating its ability to perform feature selection by driving less important coefficients to zero, enhancing model simplicity.

#  Overview & Purpose
This Jupyter Notebook provides a hands-on demonstration of L1 Regularization, commonly known as Lasso Regression. In machine learning, especially with high-dimensional datasets, models can suffer from overfitting due to excessive complexity or multicollinearity. Regularization techniques are used to penalize large coefficients, thereby reducing model complexity and improving generalization. Lasso Regression is particularly powerful because it can perform feature selection by shrinking the coefficients of less important features exactly to zero.

# The primary purpose of this notebook is to:
Illustrate Lasso Regression: Provide a clear, practical example of how Lasso Regression works.
Demonstrate Feature Selection: Show how Lasso can automatically select relevant features by driving the coefficients of irrelevant features to zero.
Explain Regularization Impact: Visualize the effect of different regularization strengths (alpha values) on model coefficients and the regression line.
Address Overfitting: Highlight how L1 regularization helps in building more robust and interpretable models by preventing overfitting.

#  Key Concepts & Functionality
The notebook covers the following aspects of L1 Regularization:
Synthetic Data Generation: Creates a synthetic 1-dimensional regression dataset using sklearn.datasets.make_regression with added noise, providing a controlled environment to observe Lasso's behavior.
Data Splitting: Divides the dataset into training and testing sets using train_test_split.
Linear Regression Baseline: A standard LinearRegression model is fitted to the data to establish a baseline for comparison, showing its coefficients and intercept.
Polynomial Features: PolynomialFeatures is used to create higher-order polynomial terms (e.g., degree=16), intentionally introducing complexity and potential for overfitting, which Lasso will then address.
Lasso Regression Implementation:
The Lasso model from sklearn.linear_model is used.
A Pipeline combines PolynomialFeatures and Lasso, allowing for seamless application of the transformation and the model.
The notebook iterates through different alpha values (regularization strengths) for the Lasso model.
Visualization of Lasso's Effect: Plots are generated to show:
The original data points.
The regression lines fitted by Lasso with different alpha values. This visually demonstrates how increasing alpha leads to simpler models and potentially straighter lines, reflecting the shrinkage of coefficients.
Coefficient Analysis (Implicit): Although not explicitly printed in the provided snippet, the core idea of Lasso is to observe how coefficients change (and become zero) with varying alpha. The visual effect on the regression line implicitly shows this.

#  Technologies Used
Python
Pandas (for data manipulation, though not heavily used in the snippet)
NumPy (for numerical operations)
Matplotlib (for plotting and visualization)
Scikit-learn (make_regression, train_test_split, LinearRegression, Lasso, Pipeline, PolynomialFeatures)
Jupyter Notebook
