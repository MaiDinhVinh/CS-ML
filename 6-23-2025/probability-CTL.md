# **Lecture: The Central Limit Theorem (CLT)**  

---

## **1. What is the Central Limit Theorem?**  

The **Central Limit Theorem (CLT)** is one of the most important results in probability and statistics. It states that:

> If we take a large enough **random sample** from any population (regardless of the original distribution), the **sampling distribution of the sample mean** will follow a **normal distribution**.

This means that even if the original data is **not normally distributed**, the **average (mean)** of many random samples will be **approximately normal**.

### **Why is This Important?**
- Many real-world data sets are **not normally distributed** (e.g., income, population growth, sales data).
- The **CLT allows us to use normal probability models** even when the population distribution is unknown or non-normal.
- It helps in **statistical inference**, enabling us to make predictions and estimate unknown parameters.

---

## **2. Why Do We Need the Central Limit Theorem?**
The CLT is useful because it:
1. **Allows us to use the normal distribution in real-world problems.**  
   - Example: The heights of people may not be perfectly normal, but if we take the average height of a **large group**, the distribution of these averages will be **normal**.
  
2. **Enables statistical inference and hypothesis testing.**  
   - We often want to estimate unknown parameters, such as the average test score of all students in a country. Instead of surveying millions, we take a **random sample** and apply the CLT to make accurate estimates.

3. **Is widely used in machine learning and artificial intelligence.**  
   - Many machine learning algorithms assume **normally distributed data**. The CLT justifies using normal-based techniques, even when data is not exactly normal.

---

## **3. Understanding CLT with Dice Rolling**  

Let’s say we have a **fair six-sided die** with possible outcomes:
$$
X = \{1, 2, 3, 4, 5, 6\}
$$
Since each face is equally likely, the **mean** (expected value) of rolling one die is:

$$
\mu = \frac{1 + 2 + 3 + 4 + 5 + 6}{6} = 3.5
$$

The **variance** (spread) is:

$$
\sigma^2 = \frac{(1-3.5)^2 + (2-3.5)^2 + (3-3.5)^2 + (4-3.5)^2 + (5-3.5)^2 + (6-3.5)^2}{6} = 2.92
$$

- **Roll 1 dice** → Outcomes are **uniform**.
- **Roll 5 dice & take the mean** → The mean fluctuates but starts forming a shape.
- **Roll 30 dice & take the mean** → The mean follows a **normal distribution**!

This happens because as the **sample size increases**, the distribution of sample means **converges to a normal distribution**.

---

## **4. The Central Limit Theorem Formula**
If a population has:
- Mean $ \mu $
- Standard deviation $ \sigma $
  
Then for **large samples** of size $ n $, the sample mean $ \bar{X} $ follows:

$$
\bar{X} \sim N \left( \mu, \frac{\sigma}{\sqrt{n}} \right)
$$

where:
- $ N(\mu, \frac{\sigma}{\sqrt{n}})$ is a normal distribution with mean $ \mu $ and variance $ (\frac{\sigma}{\sqrt{n}})^2 $.
- $ \frac{\sigma}{\sqrt{n}} $ is the **standard deviation of the sample mean**, also called the **standard error**.

### **Key Observations:**
1. **As $ n $ increases, $ \frac{\sigma}{\sqrt{n}} $ gets smaller, meaning less variation in sample means**.
2. **Larger sample sizes produce more precise estimates** of the population mean.

---

## **5. Example: Estimating the Average Height of Students**
Suppose we want to estimate the **average height** of students in a university, but we **cannot measure all students**. Instead, we:
- Take **random samples** of 50 students each.
- Measure their **average height**.
- Repeat the process 1,000 times.

Even if individual heights are **not normally distributed**, the **distribution of sample means will be normal**.

---

## **6. Applications of the Central Limit Theorem**
The CLT is **widely used** in many fields:

| **Application** | **How CLT Helps** |
|--------------|----------------|
| **Polling & Surveys** | Estimating public opinion without surveying everyone. |
| **A/B Testing** | Comparing two website versions to see which performs better. |
| **Stock Market Analysis** | Predicting average stock returns. |
| **Medical Trials** | Estimating drug effectiveness based on sample groups. |
| **Machine Learning** | Many ML models assume normality for efficiency. |

---

## **8. Summary**
✅ **The CLT states that the distribution of sample means becomes normal as sample size increases.**  
✅ **It allows us to use the normal distribution in real-world problems, even if the data isn’t normal.**  
✅ **Larger samples reduce variability and give better estimates of the population mean.**  
✅ **Used in business, healthcare, finance, machine learning, and many other fields.**  

---
# LAB

Using Python, simulate the experiment of rolling 1, 5 and 30 dice and take the mean.
For each case, simulate $100,000$ times then draw a histogram of the mean
Discuss your findings.
