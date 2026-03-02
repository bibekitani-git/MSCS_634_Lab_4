# Lab 4: Regression Analysis with Regularization Techniques

## Purpose
The purpose of this lab is to explore and implement various regression techniques to predict disease progression using the Scikit-Learn Diabetes dataset. The assignment demonstrates the progression from Simple Linear Regression to Multiple Regression, introduces polynomial feature expansion, and applies Ridge and Lasso regularization methods to mitigate overfitting. 

## Key Insights
* **Feature Importance:** Using multiple health metrics (Multiple Regression) yields a vastly superior predictive model compared to using a single metric like BMI.
* **The Danger of Complexity:** Expanding the feature space with Polynomial Regression (Degree 2) introduced too much complexity for the limited sample size, demonstrating real-world overfitting where the model memorizes noise rather than signal.
* **Power of Regularization:** Applying L1 (Lasso) and L2 (Ridge) penalties successfully constrained model coefficients. Notably, Lasso acted as an automated feature selector by reducing less relevant feature coefficients exactly to zero, resulting in a simpler, more interpretable model.
* **Inherent Dataset Noise:** The maximum R-squared achieved across all models indicates that disease progression is influenced by factors beyond the 10 baseline variables provided in this dataset.

## Challenges & Decisions
* **Challenge:** Determining the correct degree for Polynomial Regression. 
* **Decision:** I restricted the polynomial degree to 2. A degree of 3 or higher caused catastrophic overfitting due to the combinatorial explosion of features against a relatively small dataset (442 rows).
* **Challenge:** Choosing the `alpha` penalty for regularization.
* **Decision:** An alpha of `0.5` was chosen for demonstration purposes to clearly visualize the coefficient shrinkage in the comparison plot without completely underfitting the model.
