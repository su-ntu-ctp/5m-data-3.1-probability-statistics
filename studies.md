# **Self-Study Preparation Guide**

**⏳ Estimated Prep Time:** 60–80 minutes

Welcome to our flipped-classroom session, where you'll review foundational concepts beforehand to maximize our time for hands-on coding and debugging. This pre-study focuses on the mathematical pillars of Machine Learning: **Probability Distributions** and **Statistical Inference**. 

By mastering these concepts now, you will be better equipped to understand how algorithms handle uncertainty, identify outliers in datasets and validate model results during our live session.

## ⚡ Your Self-Study Tasks

Please complete the following activities before our session.

### 📝 Task 1: The Foundations of Probability (20 Minutes)

**Activity:** 

Watch the video titled [**"The Statistics of Uncertainty"**](https://youtu.be/u2Hgz9jtOHc).

[![video](https://img.youtube.com/vi/u2Hgz9jtOHc/default.jpg)](https://youtu.be/u2Hgz9jtOHc)

Open the [`Part_1_probability_statistics_lesson.ipynb`](/notebooks/Part_1_probability_statistics_lesson.ipynb) notebook. Skim through the sections on **The Law of Large Numbers**, **Measures of Central Tendency**, and **Measures of Dispersion** (do not run the code)

Review the code cells that utilize `np.random.binomial` and `np.mean`. Pay close attention to how the sample mean stabilizes as the number of experiments increases.

**Guiding Questions:**
* **Law of Large Numbers:** In the coin flip simulation, why does the probability line appear "jittery" with small sample sizes but flatten out as $N$ increases?
* **Descriptive Stats:** Why might we prefer the **Median** over the **Mean** when analyzing a dataset with extreme outliers (skewed distribution)?
* **Correlation:** How does the `np.cov` (covariance) matrix relate to `st.pearsonr` (correlation)? Why is correlation often preferred for measuring relatedness?

### 📝 Task 2: Distributions and The Central Limit Theorem (20 Minutes)

**Activity:** 

Watch the video titled [**"The Central Limit Theorem"**](https://youtu.be/ITs5zp1Xv2w).

[![video](https://img.youtube.com/vi/ITs5zp1Xv2w/default.jpg)](https://youtu.be/ITs5zp1Xv2w)

Open the [`Part_2_probability_statistics_lesson.ipynb`](./notebooks/Part_2_probability_statistics_lesson.ipynb) notebook. Skim through the sections **"Part 2: Distributions in Machine Learning"** up to **"The Central Limit Theorem."**

Examine the visual difference between Uniform, Normal (Gaussian), and Skewed distributions using the `seaborn` plots provided.

**Guiding Questions:**
* **Normal Distribution:** Why is the "Bell Curve" (Gaussian distribution) the default assumption for noise in many Machine Learning models?
* **Central Limit Theorem (CLT):** Look at the code where we sample from a *skewed* or *uniform* distribution. What happens to the shape of the distribution of the **sample means** as the sample size increases? Why is this phenomenon powerful for data science?

### 📝 Task 3: Statistical Inference and Hypothesis Testing (20 Minutes)

**Activity:** 

Watch the video titled [**"Statistical Testing"**](https://youtu.be/Uos-xeDAvqA). 

[![video](https://img.youtube.com/vi/Uos-xeDAvqA/default.jpg)](https://youtu.be/Uos-xeDAvqA)

Continue in [`Part_3_probability_statistics_lesson.ipynb`](/notebooks/Part_3_probability_statistics_lesson.ipynb), moving to **"Part 3: Introduction to Statistics."** Review the concepts of **Z-scores**, **p-values**, and the **t-test**.

Trace the logic of the "Penguin Hypothesis Testing" scenario. Do not worry about writing the code yet, but understand *why* we are separating the data into Male and Female groups.

**Guiding Questions:**
* **Z-Scores:** If a data point has a z-score of +2.5, what does that tell you about its relationship to the average data point? How might this help you detect anomalies?
* **T-Test:** When comparing the flipper lengths of two groups of penguins, what does a p-value lower than 0.05 imply about the difference between those groups?

## 🙌🏻 Active Engagement Strategies

To deepen your retention, try one of the following while you review:

* **"Code Commentary":** Select a code block involving `np.random` or `scipy.stats` (st) and write a mental or scratchpad note explaining exactly what the parameters (like `loc`, `scale`, or `size`) control.
* **Visualization Prediction:** Before running a cell that generates a plot (like `sns.displot`), try to sketch what you think the distribution will look like based on the code provided.
* **Real-World Connection:** Think of a dataset you work with. Is it normally distributed? If you calculated the z-score of a specific metric, what would constitute an outlier in your business context?

## 📖 Additional Reading Material

- [Introduction to Probability Rules](https://www.datacamp.com/cheat-sheet/introduction-to-probability-rules-cheat-sheet)
- Check out the topics on [Probability and Statistics](https://www.mathsisfun.com/data/index.html) section 

### 🙋🏻‍♂️ See you in the session!