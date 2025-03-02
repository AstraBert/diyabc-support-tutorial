# How to approach DIYABC?

> _Disclaimer: This are best practice that worked for me, that does not necessarily mean that will work universally_

DIYABC offers you the possibility of running a certain number of simulations with a specified number of data units (we will work with SNPs from now on).

The workflow that I follow is pretty much this:

- **Multi-turn simulations aimed at model selection**: In this phase, you run simulations on sets of similar scenarios, extracting the best and re-using it in other simulations with different sets of scenarios. At the end of this phase, you will have the absolute winner for all your scenarios. We will discuss what and why to perform model selection in detail [later](../model-selection/what-and-why.md). For this phase, it is advise to run quick simulations with 2000 SNPs and 2000 iterations per scenario (which means that if you have 10 scenarios you should run a total of 20000 iterations).
- **Goodness of fit and parameters estimation**: In this phase, you take the best scenario overall and simulate for (at least) 50000 iterations with 2000 or more SNPs. This will allow you to run Goodness of Fit tests and parameter estimation.

