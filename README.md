# eliu_summer_2024
Mini-course for Elizabeth Liu, Summer 2024

From linear regression to Bayesian kernel regression 

Linear regression:
* Concept of `loss function`: desired `behavior` of function we want to have
* Gradient descent: maximum-likelihood (ML) or maximum-a-posteriori (MAP) `estimate of model parameters`, based on training data
* Adjust for `classification` tasks: squared loss function and cross-entropy loss function, sigmoid function

Bayesian linear regression:
* Taylor series/Laplace method: approximate `posterior distribution of parameters`, so we can `sample` from it to get `model uncertainty`
* Metropolis sampling: another way to `sample` from posterior distribution of parameters, which avoids some derivation in Laplace method
* Bayesian marginalization: obtain `posterior prediction mean and uncertainty` for testing data, by taking into account all possible parameters
* Monte Carlo method: approximate Bayesian marginalization using `Monte Carlo integration`

Bayesian kernel regression:
* Radial basis function (RBF kernel): capture function `local behavior` through projection of input $x$ into feature space $\phi(x)$, so we can better handle nonlinearity
* Virtual sample via eigendecomposition: approximate $\phi(x)$, so we can retain steps in Bayesian linear regression by simply replacing $x$ with $\phi(x)$
* Bayesian optimization: utilize Bayesian kernel regression for `optimization` of (not-too-complicated) functions

Focus on
* `weight-space` view, so ideas in Bayesian linear regression can be retained for nonlinear case without resorting to kernel trick
* `numerical` solutions to the extent possible
