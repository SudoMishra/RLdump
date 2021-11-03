## Guidelines for RL research
1. General Baselines ( First thing when doing anything)
* Try Cross-entropy method
* Tuned Policy Gradient
* Tuned SARSA
* Tuned Q-learning

2. Setup Benchmarks
3. Use multiple random seeds

4. How to approach a new algorithm?
* Use a familiar and small test problem.
* Do multiple experiments quickly
* Play with lots of hyperparameter values
* Interpret and visualise the learning process: state visitation, Value function

5. What to do when approached with a new task?

* Simplify the problem as much as you can
* Give good input features, shape reward function
* See what happens in the case of a random policy?
* Is the task humanly solvable with the given data?
* Plot time series of observations and rewards to check their scale

6. Usually try more samples than expected during the start.

7. Always do sensitivity analysis to each parameter.

8. Indicators to see how algorithm health
* VF fit quality
* Policy entropy
* Update size in output space and parameter space
* Standardize Data

9. If the range of the observations and rewards are unknown, compute running estimate of mean and standard deviation
* Clip rewards to a given range
* Rescale rewards but don’t shift their mean

10. Important Params:
* Discount (𝛾)
* Action frequency

11. Observe min/max/mean/stdev of episode returns
12. Look at episode lengths (Solving problems faster, losing games slower?)

13. Policy Gradient Strategies:
* Observe policy entropy
* KL divergence of old policy and new policy

14. Initialization of policy is extremely important as it determines the initial states that will be visited
