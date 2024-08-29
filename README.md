# eliu_summer_2024
Mini-course for Elizabeth Liu, Summer 2024

From linear regression to Bayesian kernel regression 

Focus on
* `weight-space` view, so ideas in (Bayesian) linear regression can be retained for nonlinear case without resorting to kernel trick
* `numerical` approaches to the extent possible

Linear regression (notebook #01~08)
* Concept of `loss function`: quantify how `behavior` of a function (model) deviates from the `desired` behavior we want the model to have
* Gradient descent: maximum-likelihood (ML) or maximum-a-posteriori (MAP) `estimate of model parameters` based on training data to `minimize` loss function
* Tweak for `classification` tasks: from squared loss function to cross-entropy loss function, sigmoid function

Bayesian linear regression (notebook #09~13, #16)
* Taylor series/Laplace method: approximate `posterior distribution of parameters` given data, so we can `sample` from it to get a sense of model `uncertainty`
* Metropolis algorithm: another way to `sample` from posterior distribution of parameters, which avoids derivation needed for Laplace method
* Bayesian marginalization: obtain `posterior prediction mean and uncertainty` for testing data, by taking into account all possible parameters
* Monte Carlo method: approximate Bayesian marginalization using `Monte Carlo integration`

Bayesian kernel regression (notebook #14~15, #17)
* Radial basis function (RBF kernel): capture function `local behavior` through projection of input $x$ into feature space $\phi(x)$, so we can better handle nonlinearity
* Virtual sample via eigendecomposition: approximate $\phi(x)$, so we can retain steps in Bayesian linear regression by replacing $x$ with $\phi(x)$
* Well, no free-lunch, some additional `correction` needed when using virtual samples
* Bayesian optimization: finally, utilize Bayesian kernel regression for `optimization` of (not-too-complicated) functions

(Everything above can be done analytically using maybe 10 lines of code with Gaussian processes, but, gosh, that would be boring...)
