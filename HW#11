import numpy as np
import matplotlib.pyplot as plt
from scipy import stats

# Set the rate parameter
lambd = 0.5

# Generate 1000 samples of different sizes
sample_sizes = [5, 10, 30, 50, 100, 500, 1000]
sample_means = []
for n in sample_sizes:
    samples = np.random.exponential(scale=1/lambd, size=(n, 1000))
    means = np.mean(samples, axis=0)
    sample_means.append(means)

# Plot the histogram of the sample means
fig, axs = plt.subplots(3, 3, figsize=(12, 8))
axs = axs.flatten()
for i, n in enumerate(sample_sizes):
    axs[i].hist(sample_means[i], bins=30, density=True, alpha=0.7)
    axs[i].set_title("Sample Size = {}".format(n))
    axs[i].set_xlabel("Sample Mean")
    axs[i].set_ylabel("Density")
    
# Plot the normal distribution with the same mean and variance
x = np.linspace(0, 6, 1000)
for i, n in enumerate(sample_sizes):
    axs[i].plot(x, stats.norm.pdf(x, loc=1/lambd, scale=np.sqrt(1/(n*lambd**2))), color='r')
    
plt.tight_layout()
plt.show()
