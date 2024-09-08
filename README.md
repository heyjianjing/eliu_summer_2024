# Mini-course for Elizabeth Liu, summer 2024

Focus
* Weight-space view, numerical approach, NumPy and Matplotlib

### Part `one`: regression and classification

`01`
* Fit two 1D data points with a straight line, or linear model
* Model formulation, model parameters, and matrix notation
* Matrix inverse
* Compute inverse of 2x2 matrix
* Find model parameters through matrix inverse

`02`
* Fit more 1D data points with a straight line
* Matrix transpose
* "Inverse" of nonsquare matrix
* Analytical solution

`03`
* Iterative numerical approach to find parameters
* Loss or cost function to describe behavior we want our model to have
* Derivation of gradient of squared loss function with respect to parameters
* Gradient descent to iteratively find parameters that minimize loss function
* Compare numerical solution to analytical solution

`04`
* Extend linear regression to binary classification
* Step function for discrete output of either 1 or 0 for classification
* Sigmoid function to approximate step function
* Derivation of gradient of squared loss function for classification
* Binary classification of 1D data points

`05`
* Cross-entropy loss function and intuition
* Derivation of gradient of cross-entropy loss function
* Binary classification of 1D data points

`06`
* Binary classification of 2D data points with cross-entropy loss function

`07`
* Use linear model to handle nonlinearity
* Projection of input into feature space
* Global and local function behavior
* An infeasbile way of perfectly modeling local function behavior
* From exact matching to correlation
* Handle correlation with radial basis function (RBF)
* Keep linear form of the model
* Binary classification of 1D data points that are not linearly separable

`08`
* Extend RBF kernel method to classify 2D data points that are not linearly separable

### Part `two`: uncertainty quantification and optimization

`09`
* Uncertainty in data
* Likelihood function and essence of minimizing squared loss function
* Expression of likelihood interpreted as prediction distribution
* Prior distribution and maximum-a-posteriori estimator of parameter
* Uncertainty in model induced by posterior distribution of parameter
* Sampling from posterior distribution of parameter
* Taylor approximation and Laplace's method
* Posterior distribution of prediction via Bayesian marginalization
* Approximate Bayesian marginalization via Monte Carlo integration
* Approximate prediction distribution for MC integration using sampling
* Uncertainty quantification of linear model over 1D data points
