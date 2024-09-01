# Mini-course for Elizabeth Liu, Summer 2024

### From linear regression to Bayesian kernel regression

Focus on
* `Weight-space` view, so ideas in (Bayesian) linear regression can be retained for nonlinear case without resorting to kernel trick
* `Numerical` approaches to the extent possible
* `NumPy` and `Matplotlib`

`01`
* Regression problem: fit 2 1D data points with a straight line
* Model formulation, model parameters, and matrix notation
* Inverse of a matrix
* Compute inverse of 2x2 matrix
* Find model parameters through inverse

`02`
* Fit more 1D data points with a straight line
* Transpose of a matrix
* "Inverse" of non-square matrix

`03`
* Iterative numerical approach to find parameters
* Cost or loss function to describe behavior we want our model to have
* Derivation of gradient of loss function with respect to parameters
* Gradient descent to iteratively find parameters that minimize loss function
* Compare to analytical expression

`04`
* Classification problem
* Sigmoid function to convert regression into classification
* Derivation of gradient for classification using chain rule
* Classification of two clusters of 1D data points
