# **Self-Study Preparation Guide**

**⏳ Estimated Prep Time:** 30–45 minutes

Welcome to our flipped-classroom session, where you'll review foundational concepts beforehand to maximize our time for hands-on coding and debugging. This pre-study focuses on **Probability and Statistics**, the mathematical backbone of machine learning. Understanding these concepts is critical for quantifying uncertainty, evaluating model performance, and making data-driven decisions in professional environments.

## **⚡ Your Self-Study Tasks**

Please complete the following activities before our session.

### 🎥 Task 1: The "Engine" of Machine Learning (15 Minutes)

**Activity:** Watch the video titled [**"Prob & Statistics for ML"**](https://www.youtube.com/watch?v=9ZY9M0Q2gXk). Before we focus on on *how* to write the code, this resource explains *why* these math concepts are the "living, breathing engine" of AI.

[![video](https://img.youtube.com/vi/9ZY9M0Q2gXk/default.jpg)](https://youtu.be/9ZY9M0Q2gXk)

**Focus your attention on:**
* **The "Linda" Problem:** How human intuition often fails at probability (the "Conjunction Fallacy") and why machines need rigid mathematical rules to avoid these traps.
* **The "Fluke Detector":** The overview describes the **P-value** not as a dry formula, but as a tool to measure "pure dumb luck." Connect this explanation to the specific P-value (`6.402e-26`) mentioned in the Penguin example.

**Guiding Questions:**
* The overview mentions that knowing the "Center" (Mean/Median) is like knowing the capital of a country, but the **Histogram** gives you the "lay of the land." Why is seeing the *shape* of data often more important than just knowing the average?
* How does the transcript distinguish between a program that just "follows instructions" (a calculator) and a system that "learns" (ML)? What role does **Probability** play in that difference?

### 📝 Task 2: Journey from Randomness to Reliability (15 Minutes)

**Activity:** Watch the provided video [**Chance to Confidence.**](https://youtu.be/ybdM4U2KEM0) This video bridges the gap between basic probability theory and complex machine learning algorithms. As you watch, focus on the progression from observing a single random event to making statistical inferences about a population.

[![video](https://img.youtube.com/vi/ybdM4U2KEM0/default.jpg)](https://youtu.be/ybdM4U2KEM0)

**Guiding Questions:**

* **The Problem with "Messy" Data:** The video suggests the world is full of "noise" and missing pieces. How does the **Law of Large Numbers** help machines find the "signal" in this static, as illustrated by the coin flip example?
* **Defining Structure:** How do **Probability Distributions** act as a "map" for data? Specifically, differentiate between the scenarios where you would use a *discrete* distribution (like rolling a die) versus a *continuous* distribution (like height or time).
* **Scenario Matching:** Think of a decision you make in your work that involves uncertainty. If you had to assign a "confidence level" to that decision, what data would you need to increase that confidence, similar to the penguin weight example?
* **Concept Definition:** In your own words, write a one-sentence definition for **Statistical Inference** based on the video's explanation of studying a "small, well-chosen sample" to understand a whole group.

### 📝 Task 3: Understanding Distributions (15 Minutes)

**Activity:** Open the provided notebook file [`Part_2_probability_statistics_lesson.ipynb`](/notebooks/Part_2_probability_statistics_lesson.ipynb). Read through the Markdown explanations and examine the visual plots for **Uniform**, **Gaussian (Normal)**, and **Binomial** distributions. [Watch the video](https://youtu.be/Nn-uO_Y4RVQ) on **Central Limit Theorem (CLT)**. This is a cornerstone concept for why many ML models work. 

[![video](https://img.youtube.com/vi/Nn-uO_Y4RVQ/default.jpg)](https://youtu.be/Nn-uO_Y4RVQ)

**Focus your attention on:**

* The visual difference between discrete distributions (like coin flips) and continuous distributions (like height).  

**Guiding Questions:**

* Why is the Gaussian (Normal) distribution so prevalent in machine learning and natural sciences?  
* How does the "Law of Large Numbers" change the shape of a distribution as you increase the number of experiments?

## 📖 Additional Reading Material**

- [Introduction to Probability Rules](https://www.datacamp.com/cheat-sheet/introduction-to-probability-rules-cheat-sheet)
- Check out the topics on [Probability and Statistics](https://www.mathsisfun.com/data/index.html) section 


**Note:** In our live session, we will move quickly past *definitions* and jump straight into applying these statistical tests to real datasets to find anomalies. Your preparation here ensures you can focus on the code implementation rather than the theory.

### **🙋🏻‍♂️ See you in the session\!**
