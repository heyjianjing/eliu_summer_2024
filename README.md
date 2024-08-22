# eliu_summer_2024
Mini-course for Elizabeth Liu, Summer 2024

From linear regression to Bayesian kernel regression 

Linear regression:
* Concept of `loss function`: desired `behavior` of function we want to have
* Gradient descent: maximum-likelihood (ML) or maximum-a-posteriori (MAP) `estimate of model parameters`, based on training data
* Adjust for `classification` tasks: squared loss and cross-entropy loss, sigmoid function

Bayesian linear regression:
* Taylor approximation/Laplace method: approximate `posterior distribution of parameters`, so we can `sample` from it to get `model uncertainty`
* Metropolis sampling: another way to `sample` from posterior distribution of parameters using Metropolis algorithm, to avoid derivation in Laplace method
* Bayesian marginalization: obtain `posterior prediction mean and uncertainty` for testing data, accounting for all possible parameters
* Monte Carlo integration: approximate Bayesian marginalization using `Monte Carlo integration`

Bayesian kernel regression:
* Radial basis function: capture `local function behavior` through projection of model input $x$ into feature space $\phi(x)$, so we can better model nonlinearity
* Virtual sample via eigendecomposition: approximate $\phi(x)$ such that concept from linear case can be `retained`
* Bayesian optimization: utilize Bayesian kernel regression for `optimization` of (not-so-complicated) functions

Focus
* `weight-space` view, so ideas in Bayesian linear regression can be retained for nonlinear case
* `numerical` solutions to the extent possible
