# Mini-course for Elizabeth Liu, Summer 2024

### From linear regression to Bayesian kernel regression

Focus on
* `Weight-space` view, so ideas in (Bayesian) linear regression can be retained for nonlinear case without resorting to kernel trick
* `Numerical` approaches to the extent possible
* `NumPy` and `Matplotlib`

`01`
* Linear regression: fit two 1D data points with a straight line $y=ax (+b)$
* Model formulation, model parameters, and matrix notation $y=A\theta$
* Inverse of a matrix $A$
* Compute inverse of 2x2 matrix
* Find model parameters through inverse

`02`
* Fit more 1D data points with a straight line
* Transpose of a matrix
* "Inverse" of nonsquare matrix
* Analytical expression to solve $y=A\theta$

`03`
* Iterative numerical approach to find parameters
* Cost or loss function to describe behavior we want our model to have
* Derivation of gradient of squared loss function with respect to parameters
* Gradient descent to iteratively find parameters that minimize loss function
* Compare to analytical expression

`04`
* Extend linear regression to do binary classification
* Step function for discrete output of either 1 or 0 for classification
* Sigmoid function to approximate step function
* Derivation of gradient of squared loss function for classification
* Classification of two clusters of 1D data points
