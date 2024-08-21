# eliu_summer_2024
Mini-course for Elizabeth Liu, Summer 2024

From linear regression to Bayesian kernel regression 

Linear case:
* Gradient descent (find maximum-likelihood (ML) or maximum-a-posteriori (MAP) `estimate of model parameters`)
* Taylor approximation/Laplace method (approximate `posterior distribution of parameters`, so we can `sample` from it to get `model uncertainty`)
* Metropolis sampling (also `sample` from posterior distribution of parameters, but using Metropolis algorithm to avoid derivation in Laplace method)
* Bayesian marginalization (obtain `posterior prediction mean and uncertainty` for testing data, considering all possible parameters)
* Monte Carlo integration (approximate Bayesian marginalization using Monte Carlo)

Nonlinear case:
* Radial basis function (RBF kernel) (enable capture of `local function behavior` through projection into feature space $\phi(x)$)
* Virtual sample via eigendecomposition (approximate $\phi(x)$ such that steps from linear case can be utilized)
* Bayesian optimization (utilization of Bayesian kernel regression for optimization)

Focus on `weight-space` view, so ideas in Bayesian linear regression can be retained for nonlinear case
Focus on `numerical` solutions to the extent possible
