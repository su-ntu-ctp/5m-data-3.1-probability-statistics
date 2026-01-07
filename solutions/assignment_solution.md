# Assignment

## Instructions

Complete the following exercises using Python.

1. **Probability and Expected Value**

   - Generate 10,000 random samples of flipping 3 coins (use `np.random.binomial()`)
   - Plot the probability distribution of getting 0, 1, 2, or 3 heads
   - Calculate the expected value (mean) of your distribution
   - Compare your empirical results with the theoretical probability for each outcome

   ```python
   import numpy as np
   import matplotlib.pyplot as plt
   import seaborn as sns
   import scipy.stats as st

   # Generate 10,000 samples of 3 coin flips
   samples = np.random.binomial(n=3, p=0.5, size=10000)

   # Calculate empirical probabilities
   values, counts = np.unique(samples, return_counts=True)
   empirical_probs = counts / len(samples)

   # Calculate theoretical probabilities
   def theoretical_prob(n, k):
       return (st.binom.pmf(k, n, 0.5))

   theoretical_probs = [theoretical_prob(3, k) for k in range(4)]

   # Plot results
   plt.figure(figsize=(10, 6))
   width = 0.35
   plt.bar(values - width/2, empirical_probs, width, label='Empirical')
   plt.bar(values + width/2, theoretical_probs, width, label='Theoretical')
   plt.xlabel('Number of Heads')
   plt.ylabel('Probability')
   plt.title('Distribution of Heads in 3 Coin Flips')
   plt.legend()
   plt.show()

   # Calculate expected value
   empirical_mean = np.mean(samples)
   theoretical_mean = 3 * 0.5  # n * p

   print(f"Empirical mean: {empirical_mean:.3f}")
   print(f"Theoretical mean: {theoretical_mean:.3f}")
   ```

2. **Normal Distribution and Statistical Testing**

   - Generate two samples from normal distributions:
     - Sample A: 100 values with mean=70, std=5
     - Sample B: 100 values with mean=73, std=5
   - Create a box plot comparing the two distributions
   - Conduct an independent t-test to determine if the means are significantly different
   - Calculate and visualize the 95% confidence intervals for both samples

   ```python
   # Generate samples
   np.random.seed(42)
   sample_A = np.random.normal(loc=70, scale=5, size=100)
   sample_B = np.random.normal(loc=73, scale=5, size=100)

   # Create box plot
   plt.figure(figsize=(8, 6))
   plt.boxplot([sample_A, sample_B], labels=['Sample A', 'Sample B'])
   plt.title('Box Plot of Samples A and B')
   plt.ylabel('Values')
   plt.show()

   # Conduct t-test
   t_stat, p_value = st.ttest_ind(sample_A, sample_B)
   print(f"T-statistic: {t_stat:.3f}")
   print(f"P-value: {p_value:.6f}")

   # Calculate confidence intervals
   def conf_interval(data):
       return st.t.interval(confidence=0.95,
                          df=len(data)-1,
                          loc=np.mean(data),
                          scale=st.sem(data))

   ci_A = conf_interval(sample_A)
   ci_B = conf_interval(sample_B)

   # Plot means with confidence intervals
   plt.figure(figsize=(8, 6))
   plt.errorbar(['Sample A', 'Sample B'],
                [np.mean(sample_A), np.mean(sample_B)],
                yerr=[[np.mean(sample_A)-ci_A[0], np.mean(sample_B)-ci_B[0]],
                      [ci_A[1]-np.mean(sample_A), ci_B[1]-np.mean(sample_B)]],
                fmt='o')
   plt.title('Means with 95% Confidence Intervals')
   plt.ylabel('Values')
   plt.show()
   ```

3. **Correlation Analysis**

   - Using the iris dataset (from seaborn), analyze the relationship between:
     - Sepal length and petal length
     - Sepal width and petal width
   - For each pair:
     - Create a scatter plot
     - Calculate the Pearson correlation coefficient and p-value
     - Calculate and interpret the R-squared value
   - Which pair shows a stronger relationship? Explain why.

   ```python
   # Load iris dataset
   iris = sns.load_dataset('iris')

   # Sepal length vs petal length
   plt.figure(figsize=(10, 5))
   plt.subplot(121)
   sns.scatterplot(data=iris, x='sepal_length', y='petal_length')
   plt.title('Sepal Length vs Petal Length')

   # Sepal width vs petal width
   plt.subplot(122)
   sns.scatterplot(data=iris, x='sepal_width', y='petal_width')
   plt.title('Sepal Width vs Petal Width')
   plt.tight_layout()
   plt.show()

   # Calculate correlations and R-squared
   def analyze_correlation(x, y, label):
       r, p = st.pearsonr(x, y)
       r_squared = r ** 2
       print(f"\n{label}:")
       print(f"Correlation coefficient (r): {r:.3f}")
       print(f"P-value: {p:.6f}")
       print(f"R-squared: {r_squared:.3f}")

   analyze_correlation(iris.sepal_length, iris.petal_length,
                      "Sepal Length vs Petal Length")
   analyze_correlation(iris.sepal_width, iris.petal_width,
                      "Sepal Width vs Petal Width")
   ```

## Submission

- Submit the URL of the GitHub Repository that contains your work to NTU black board.
- Should you reference the work of your classmate(s) or online resources, give them credit by adding either the name of your classmate or URL.
