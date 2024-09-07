# Mini-course for Elizabeth Liu, summer 2024

### Part `one`: regression and classification

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
* Classification of two classes of 1D data points

`05`
* Cross-entropy loss function and intuition
* Derivation of gradient of cross-entropy loss function
* Classification of two classes of 1D data points

`06`
* Classification of two classes of 2D data points with cross-entropy loss function

`07`
* Use linear model to handle nonlinearity
* Projection of input into feature space
* Global and local function behavior
* An infeasbile way of perfectly modeling local function behavior
* From exact matching to correlation
* Handle correlation with radial basis function
* Keep linear form of the model
* Classification of 1D data points that are not linearly separable

`08`
* Extend RBF kernel method to classify 2D data points that are not linearly separable

### Part `two`: uncertainty quantification and optimization
