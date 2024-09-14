# Mini-course for Elizabeth Liu, summer 2024

From linear regression to Bayesian kernel regression
* Focus on weight-space view, numerical approach (to the extent possible), NumPy and Matplotlib

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
* Implement binary classification of 1D data points

`05`
* Cross-entropy loss function and intuition
* Derivation of gradient of cross-entropy loss function
* Implement binary classification of 1D data points

`06`
* Implement binary classification of 2D data points with cross-entropy loss function

`07`
* Use linear model to handle nonlinearity
* Projection of input into feature space
* Global and local function behavior
* An infeasbile way of perfectly modeling local function behavior
* From exact matching to correlation
* Handle correlation with radial basis function (RBF)
* Keep linear form of the model
* Implement binary classification of 1D data points that are not linearly separable

`08`
* Extend RBF kernel method to classify 2D data points that are not linearly separable

### Part `two`: uncertainty quantification and optimization

`09`
* Uncertainty in data
* Likelihood function and essence of minimizing squared loss function
* Expression of likelihood interpreted as prediction distribution
* Prior distribution and maximum-a-posteriori estimator of parameters
* Uncertainty in model induced by posterior distribution of parameters
* Sampling from posterior distribution of parameters
* Taylor approximation (`notes_01`) and Laplace's method (`notes_02`)
* Posterior distribution of prediction via Bayesian marginalization
* Approximate Bayesian marginalization via Monte Carlo integration
* Approximate prediction distribution for MC integration using sampling
* Implement Bayesian linear regression over 1D data points

`10`
* Extend Bayesian linear regression to Bayesian kernel regression
* Kernel function and correlation preservation
* Virtual samples through eigendecomposition (`notes_03`)
* Retain linear form with virtual samples for nonlinear regression
* Vector form of Taylor approximation for sampling from posterior distribution of parameters
* Correction step for prediction uncertainty (`notes_04`, `notes_05`)
* Implement Bayesian kernel regression over 1D data points

`11`
* Revisit Bayesian linear regression from `09`
* Replace Taylor approximation and Laplace's method by Metropolis algorithm (`notes_06`) to sample from posterior distribution of parameters

`12`
* Revisit Bayesian kernel regression from `10`
* Replace Taylor approximation and Laplace's method by Metropolis algorithm

`13`
* Organize and speed up Bayesian kernel regression from `12`
* Package algorithm using Python Class
* Vectorize (`notes_07`) kernel function and Monte Carlo integration in NumPy
* Avoid computation of full kernel matrix for testing data points
* Evaluate over 250,000 1D testing data points using Bayesian kernel regression in 30 seconds

`14`
* Use Bayesian kernel regression from `13` to optimize the underlying (but unknown) function that generates our data
* Lower confidence bound and the balance between exploitation and exploration in optimization
* Implement Bayesian optimization to minimize a 1D function

`15`
* Extend Bayesian kernel regression from `13` to handle 2D data points

`16`
* Implement Bayesian optimization to minimize a 2D function, using Bayesian kernel regression from `15`

### Part `three`: data-independent virtual samples

`17`
* Virtual samples from eigendecomposition is data-dependent, causing issues
* Concept of random Fourier features (`notes_08`) as data-independent virtual samples
* Implement Bayesian kernel regression from `13` using random Fourier features to avoid correction of prediction variance

`18`
* Implement Bayesian kernel regression from `17` to minimize a 1D function with Bayesian optimization
