# Introductory machine learning

From linear regression to Bayesian kernel regression
* Focus on weight-space view (linear form), numerical approach (to the extent possible), NumPy and Matplotlib

### Part `one`: regression

`01`
* Fit two 1D data points with a straight line, or linear model
* Model formulation, model parameters, and matrix notation
* Matrix inverse
* Compute inverse of 2x2 matrix
* Find model parameters through matrix inverse

`02`
* Fit more 1D data points with a straight line
* Matrix transpose
* Analytical solution
* Geometric interpretation of analytical solution as projection

`03`
* Iterative numerical approach to find parameters
* Loss or cost function to describe behavior we want our model to have
* Choice of loss function (`notes_01`)
* Derivation of gradient of squared loss function with respect to parameters
* Gradient descent to iteratively find parameters that minimize loss function
* Compare numerical solution to analytical solution
* Gradient descent as minimizing regularized 1st order Taylor approximation (`notes_02`) of loss function

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

### Part `two`: uncertainty

`09`
* Uncertainty in data
* Likelihood function and essence of minimizing squared loss function
* Expression of likelihood interpreted as prediction distribution
* Prior distribution and maximum-a-posteriori estimator of parameters
* Uncertainty in model induced by posterior distribution of parameters
* Sampling from posterior distribution of parameters
* Taylor approximation (`notes_02`) and Laplace's method (`notes_03`)
* Posterior distribution of prediction via Bayesian marginalization
* Approximate Bayesian marginalization via Monte Carlo integration
* Approximate prediction distribution for MC integration using sampling
* Implement Bayesian linear regression over 1D data points

`10`
* Extend Bayesian linear regression to Bayesian kernel regression
* Kernel function and correlation preservation
* Virtual samples through eigendecomposition (`notes_04`)
* Retain linear form with virtual samples for nonlinear regression
* Vector form of Taylor approximation for sampling from posterior distribution of parameters
* Correction step for prediction uncertainty (`notes_05`, `notes_06`)
* Implement Bayesian kernel regression over 1D data points

`11`
* Revisit Bayesian linear regression from `09`
* Replace Taylor approximation and Laplace's method by Metropolis algorithm (`notes_07`) to sample from posterior distribution of parameters

`12`
* Revisit Bayesian kernel regression from `10`
* Replace Taylor approximation and Laplace's method by Metropolis algorithm

`13`
* Organize and speed up Bayesian kernel regression from `12`
* Package algorithm using Python Class
* Vectorize (`notes_08`) kernel function and Monte Carlo integration in NumPy
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

### Part `three`: look for `better` virtual samples

`17`
* Need for data independent virtual samples
* Random features
* Random Fourier features (RFFs)
* Matrix notation
* Dot product of RFFs to approximate RBF kernel function
  
### Notes

`notes_01`
* Squared loss function and influence of outliers
* Absolute value loss function is less sensitive to outliers
* Comparison of common loss functions (squared, absolute value, deadzone, Huber)

`notes_02`
* Taylor approximation of functions with scalar input
* Taylor approximation of functions with vector input

`notes_03`
* Sampling from a distribution
* Laplace's method for sampling based on 2nd order Taylor approximation of distribution
* Use finite difference to compute second derivatives

`notes_04`
* Concept of eigenvalues and eigenvectors
* Compute eigenvalues and eigenvectors based on definition
* Diagonalization of a matrix using eigenvalues and eigenvectors
* Kernel matrix is symmetric
* Symmetric matrices have real eigenvalues and orthonormal eigenvectors
* Equivalence between transpose and inverse for orthonormal eigenvectors
* Power iterations and Rayleigh quotient to numerically compute dominant eigenvalue and eigenvector
* Generalize power iterations to compute all eigenvalues and eigenvectors for symmetric matrices

`notes_05`
* Transformation of data induced by RBF kernel is infinite-dimensional

`notes_06`
* Correction of posterior prediction variance due to finite-dimensional approximation of infinite-dimensional transformation under RBF kernel

`notes_07`
* Metropolis algorithm for sampling
* Proposal distribution to generate new sample candidates
* Acceptance rate

`notes_08`
* Vectorization and broadcasting in NumPy
* Broadcasting rules

`notes_09`
* Hamiltonian Monte-Carlo (HMC) sampling
* Euler-Lagrange equation
* Lagrangian mechanics
* Hamiltonian equations
* Leapfrog method
* HMC and Metropolis algorithm
