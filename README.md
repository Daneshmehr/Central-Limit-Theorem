# PHSX815_Week10

The Central Limit Theorem states that as the sample size increases, the distribution of the sample means approaches a normal distribution regardless of the distribution of the population. This means that even if the population distribution is not normal, the distribution of the sample means will become normal as the sample size increases.

For the exponential distribution, we can use Python to demonstrate the Central Limit Theorem. The exponential distribution has a probability density function given by:

f(x; λ) = λe^(-λx), x ≥ 0

where λ is the rate parameter.

To demonstrate the Central Limit Theorem for the exponential distribution, we can generate a large number of samples of different sizes and compute their means. We can then plot a histogram of the means and compare it to a normal distribution with the same mean and variance.


In this code, we first set the rate parameter lambd to 0.5. We then generate 1000 samples of different sizes using the np.random.exponential() function. We compute the mean of each sample using the np.mean() function and store them in the sample_means list.

We then plot a histogram of the sample means for each sample size using the plt.hist() function. We also plot a normal distribution with the same mean and variance using the stats.norm.pdf() function from the scipy.stats module.

When we run this code, we should see a plot with nine subplots, each showing a histogram of the sample means for a different sample size. We should also see a red line on each plot representing the normal distribution with the same mean and variance. We can observe that as the sample size increases, the distribution of the sample means approaches a normal distribution, as predicted by the Central Limit Theorem.
