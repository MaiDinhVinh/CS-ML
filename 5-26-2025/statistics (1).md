# 📊 Introduction to Statistics

## What is Statistics?
**Statistics** is the branch of mathematics that involves collecting, organizing, analyzing, interpreting, and presenting data. It helps us make informed decisions based on data patterns and trends.

There are two main types of statistics:
1. **Descriptive Statistics** – Summarizes and describes the main features of a dataset.
2. **Inferential Statistics** – Uses sample data to make predictions or inferences about a larger population.

---

# 📌 Central Tendencies
In statistics, the concept of central tendency is essential because it helps summarize a large set of data with a single representative value. This value gives us an idea of the general trend of the data.
Measures of central tendency describe the "center" of a dataset.

## 1️⃣ Mean (Average)
The **mean** is the sum of all values divided by the total number of values:
$$
\text{Mean} (\mu) = \frac{\sum X_i}{n}
$$
Where:
- $X_i$ are the individual values.
- $n$ is the total number of values.

Why Use It?
- The mean is useful for normally distributed data where values are symmetrically spread.
- It considers every data point, making it highly informative.

Limitations:
- **It is sensitive to outliers**. A few extreme values can skew the mean, making it misleading.


**Example:**

For $\{2, 4, 6, 8, 10\}$:
$$
\mu = \frac{2+4+6+8+10}{5} = \frac{30}{5} = 6
$$

## 2️⃣ Median
The **median** is the middle value when data is **sorted**.

- If $n$ is odd, it is the middle value.
- If $n$ is even, it is the average of the two middle values.

Why Use It?
- The median is **not affected by outliers**. It is useful for **skewed data** or when extreme values exist.

Limitations:
- It does not consider all values in a dataset.
- Less useful for precise calculations compared to the mean.

**Example:**

For $\{3, 5, 7, 9, 11\}$, the median is **7**.

## 3️⃣ Mode
The **mode** is the most frequently occurring value in a dataset.

Why Use It?
- The mode is useful for categorical data where mean and median don’t make sense (e.g., "blue," "red," "green").
- It helps identify the most common outcome in a dataset.

Limitations:
- A dataset can have no mode, one mode (unimodal), or multiple modes (bimodal, multimodal).
- Less informative when all values are unique.

**Example:**

For $\{1, 2, 2, 3, 3, 3, 4, 5\}$, the mode is **3** (since it appears the most times).

---
# 📌 Dispersion (Spread of Data)

## **Why Study Dispersion in Statistics?**  

In statistics, **dispersion** refers to the **spread** or **variability** of data points in a dataset. While **central tendency** (mean, median, mode) tells us the middle or most typical value, **dispersion** tells us **how much the data varies** around that central value. Studying dispersion is crucial for a deeper understanding of data distribution. Here are the main reasons why:

---

### **1. Understanding Data Variability**
- Dispersion helps us determine **how spread out or concentrated** the data is.
- Two datasets can have the **same mean** but very different spreads.

**Example**:  
- Test Scores in Two Classes:  
  - **Class A:** 60, 62, 63, 65, 67 → (low dispersion, scores are close to the mean)  
  - **Class B:** 40, 50, 60, 70, 90 → (high dispersion, scores vary widely)  

✅ **Class A has more consistent student performance.**  
✅ **Class B has a wider range of student abilities.**  

---

### **2. Comparing Different Datasets**
- If two datasets have the **same central tendency**, we need dispersion to compare them accurately.
- Helps businesses, researchers, and analysts **choose the best dataset** for decision-making.

**Example**:  
- Two investment options have the **same average return**, but:
  - **Investment A:** Returns vary between 8% and 12% → Low Risk (low dispersion).
  - **Investment B:** Returns vary between -5% and 20% → High Risk (high dispersion).  

✅ **A risk-averse investor would prefer Investment A due to lower dispersion.**  

---

### **3. Identifying Consistency & Reliability**
- A lower dispersion means **more consistency**.
- A higher dispersion means **more unpredictability**.

**Example**:  
- **Manufacturing Quality Control:**  
  - Factory A produces bolts with lengths between **9.8 cm and 10.2 cm** (low dispersion).  
  - Factory B produces bolts with lengths between **9.0 cm and 11.0 cm** (high dispersion).  

✅ **Factory A produces more reliable products with less variation.**  

---

### **4. Detecting Outliers & Extreme Values**
- Measures of dispersion help detect **unusual values** that might distort analysis.
- Outliers can **skew** the mean and lead to incorrect conclusions.

**Example**:  
- **Patient Blood Pressure Readings:**  
  - Most patients have readings between **110–130 mmHg**, but one has **180 mmHg**.  
  - A high dispersion measure (e.g., standard deviation) would flag this outlier.  

✅ **Doctors can investigate and treat the outlier patient.**  

## **Dispersion Measures**  

### 1️⃣ Range
The **range** is the difference between the maximum and minimum values:
$$
\text{Range} = \max(X) - \min(X)
$$

Why use it?
- Quick and easy way to measure spread.
- Only considers two values (max & min), so it ignores the rest of the data.

Limitations:
- **Sensitive to outliers** (one extreme value can distort the range).
- Ignores how the data is distributed (doesn't tell us if most values are clustered or widely spread).

**Example:**

For $\{4, 6, 8, 10, 12\}$:
$$
\text{Range} = 12 - 4 = 8
$$

### 2️⃣ Variance ($\sigma^2$)
Variance measures the spread of data:
$$
\sigma^2 = \frac{\sum (X_i - \mu)^2}{n}
$$

Why use it?
- Measures how far each data point is from the mean.
- Takes all values into account, unlike range.
- Uses squared differences to avoid negative values canceling each other out.

Limitation:
- **Units are squared**, which makes it hard to interpret (e.g., squared dollars, squared meters).
- It **exaggerates dispersion** compared to the original data scale.

✅**Use Variance when comparing datasets mathematically, but not for interpretation.**

### 3️⃣ Standard Deviation ($\sigma$)
The **standard deviation** is the square root of variance:
$$
\sigma = \sqrt{\sigma^2} = \sqrt{\frac{\sum (X_i - \mu)^2}{n}}
$$

Why use it?
- Solves the problem of variance by bringing the measure **back to the original units**.
- Directly tells us how much the data typically deviates from the mean.
- Helps in probability and normal distribution analysis.

✅ Use Standard Deviation when making real-world decisions and comparing datasets.

**Example:**

For $X = \{2, 4, 6\}$:
1. Mean: $\mu = 4$
2. Variance: 
   $$
   \sigma^2 = \frac{(2-4)^2 + (4-4)^2 + (6-4)^2}{3} = \frac{4+0+4}{3} = 2.67
   $$
3. Standard Deviation: 
   $
   \sigma = \sqrt{2.67} \approx 1.63
   $

---

# 📌 Covariance
## **Why Study Covariance in Statistics?**
Covariance is a fundamental concept in statistics that measures the direction of the relationship between two variables. It helps us understand how two variables move together, making it useful in finance, economics, science, and machine learning.

### Understanding Relationships Between Variables
- Covariance tells us whether two variables increase or decrease together.
- A positive covariance means they move in the same direction (if one increases, the other also increases).
- A negative covariance means they move in opposite directions (if one increases, the other decreases).

### Covariance Equation  

$$
\text{Cov}(X, Y) = \frac{\sum (X_i - \bar{X}) (Y_i - \bar{Y})}{N}
$$

where:
- $ X_i $ and $ Y_i $ are individual data points for variables $ X $ and $ Y $.
- $ \bar{X} $ and $ \bar{Y} $ are the **mean** (average) values of $ X $ and $ Y $.
- $ N $ is the **number of data points**.

## **Limitations of Using Covariance in Statistics**  

While **covariance** is useful for understanding relationships between variables, it has several **limitations** that make it difficult to use in certain analyses. Here are the key drawbacks:

---

### **1. Covariance Does Not Show Strength of Relationship**  
- **Problem**: Covariance only tells us **the direction** (positive or negative), but **not how strong the relationship is**.  
- **Solution**: We use **correlation**, which standardizes covariance and gives a **bounded value (-1 to +1)** for easy interpretation.  

**Example:**  
- If **cov(X, Y) = 1000** and **cov(A, B) = 5**, does this mean X and Y have a stronger relationship?  
- **Not necessarily**—covariance values depend on the unit of measurement, making direct comparisons meaningless.  

✅ **Fix**: Use **correlation** instead of raw covariance to measure strength.  

---

### **2. Covariance Depends on the Scale of Measurement**  
- **Problem**: Covariance is affected by the **units of measurement**, which makes it hard to compare datasets.  
- **Solution**: Convert covariance into **correlation** to remove unit dependence.  

**Example:**  
- If we measure **height in centimeters**, the covariance with weight might be **3000**.  
- If we switch height to **meters**, the covariance might change to **30**, even though the relationship hasn’t changed!  

✅ **Fix**: Use **correlation**, which is unit-free.  

---

### **3. Covariance Does Not Prove Causation**  
- **Problem**: A **high covariance** does **not** mean one variable **causes** the other to change.  
- **Solution**: Use **controlled experiments** or causal inference methods to establish causation.  

**Example:**  
- **Ice Cream Sales & Shark Attacks** have **positive covariance** because both increase in summer.  
- **But eating ice cream doesn’t cause shark attacks!**  
- A **hidden variable (temperature)** affects both.  

✅ **Fix**: Use **causal analysis** methods to verify cause-effect relationships.  

---

### **4. Sensitive to Outliers**  
- **Problem**: A single extreme value can **distort** covariance and make it unreliable.  
- **Solution**: Use **robust statistics** like **Spearman’s rank correlation** for skewed data.  

**Example:**  
- Suppose we measure **income vs. happiness** in a small town.  
- If one billionaire moves in, the covariance **skyrockets**, even though most people’s income and happiness haven’t changed.  

✅ **Fix**: Remove outliers or use **rank-based correlation**.  

---

### **5. Cannot Compare Covariance Across Different Datasets**  
- **Problem**: Since covariance values depend on the **scale of the data**, comparing across datasets is meaningless.  
- **Solution**: Convert to **correlation** for meaningful comparisons.  

**Example:**  
- **Cov(Stock A, Stock B) = 5000**, but **Cov(Temperature, Ice Cream Sales) = 20**.  
- Does this mean Stock A and Stock B are more strongly related than temperature and ice cream sales? **No!** The numbers are not on the same scale.  

✅ **Fix**: Convert to **correlation coefficient** for proper comparison.  

### **Conclusion: Why Covariance Has Limitations**
📌 **It only shows direction, not strength.**  
📌 **It depends on the unit of measurement, making comparisons hard.**  
📌 **It does not imply causation—correlation does not equal causation!**  
📌 **It is sensitive to outliers, which can distort results.**  
📌 **It cannot be used to compare relationships across different datasets.**  

✅ **Best Alternative?** Use **correlation**, which solves many of these problems!  

---
# 📌 Correlation

## **Why Study Correlation in Statistics?**  

In statistics, **correlation** measures the **strength and direction** of a relationship between two variables. Studying correlation is important because it helps us understand how one variable changes in relation to another. Here are the main reasons why correlation is useful in data analysis and decision-making:

---

### **1. Identifying Relationships Between Variables**  
- Correlation helps determine **whether two variables are related** and if they move together.  
- A strong correlation suggests a **predictable relationship**, while a weak or no correlation means **little to no connection**.  

**Example:**  
- **Height & Weight:** Taller people tend to weigh more (positive correlation).  
- **Temperature & Sweater Sales:** Warmer weather reduces sweater sales (negative correlation).  

✅ **Understanding relationships helps in making predictions and strategic decisions.**  

---

### **2. Making Predictions**  
- If two variables have a **strong correlation**, we can use one to predict the other.  
- This is useful in **business, economics, healthcare, and science**.  

**Example:**  
- **Advertising & Sales:** If a company finds a strong positive correlation between ad spending and product sales, they can predict future sales based on their advertising budget.  
- **Study Hours & Exam Scores:** If there’s a strong positive correlation, teachers can encourage students to study more to improve grades.  

✅ **Correlation helps in forecasting trends and making data-driven decisions.**  

---

### **3. Understanding Cause-and-Effect Relationships (But Not Proving Them!)**  
- Correlation **does not imply causation** but can suggest a possible relationship worth further investigation.  
- Helps researchers identify **potential causes** before conducting deeper studies.  

**Example:**  
- **Smoking & Lung Cancer:** Strong correlation, but further studies needed to prove causation.  
- **Ice Cream Sales & Shark Attacks:** Both increase in summer (correlation), but eating ice cream doesn’t cause shark attacks!  

✅ **Correlation is a starting point for deeper research into causal relationships.**  

---


## **Correlation Coefficient ($r$)**
The **Pearson correlation coefficient** ($r$) is calculated as:
$$
r = \frac{\text{Cov}(X, Y)}{\sigma_X \sigma_Y}
$$
$$
r = \frac{\sum (X - \bar{X})(Y - \bar{Y})}{\sqrt{\sum (X - \bar{X})^2 \sum (Y - \bar{Y})^2}}
$$
- **$r$ is unit-free**
- If **$r = 1$**, perfect positive correlation (as X increases, Y increases).
- If **$r = -1$**, perfect negative correlation (as X increases, Y decreases).
- If **$r = 0$**, no correlation.

**Example**:

If study hours ($X$) and test scores ($Y$) are positively correlated, an increase in study hours will likely lead to higher test scores.

---

## Correlational Caveat
1️⃣ Correlation does not always imply a meaningful relationship. Sometimes, data may appear correlated due to **coincidence** or a **hidden variable**.

**Example**:
Ice cream sales and shark attacks are correlated because both increase in summer. However, eating ice cream does **not** cause shark attacks. The **hidden variable** here is the **summer season**.

2️⃣ There may be **other sorts of relationship**.

**Example**:

$x = [-2, -1, 0, 1, 2]$

$y = [ 2,  1, 0, 1, 2]$

$r_{x,y} = 0$ (i.e. **zero correlation**)

There is a relationship between $x$ and $y$, which is $y = |x|$

---

## Correlation vs. Causation
A key rule in statistics: **correlation does NOT imply causation**. Just because two variables are correlated does not mean one causes the other.

**Example**:
Studies might show that students who drink more coffee score higher on exams. However:
1. Coffee might improve focus (**causation**).
2. Hardworking students might drink more coffee and study longer (**third variable**).
3. The relationship might be purely **coincidental**.

To establish **causation**, we need **controlled experiments** where external factors are eliminated.

---
# 📌 Simpson's Paradox
## **Scenario of Medical Treatment Recovery**  
A hospital is evaluating the effectiveness of two drugs (**Drug A and Drug B**) for treating patients with **mild and severe illnesses**. Initially, the **overall recovery rates** suggest that both drugs are equally effective, but a deeper look at the data reveals a paradox.

### **Data Summary**  
| **Severity** | **Treatment** | **Patients** | **Recovered** | **Recovery Rate (%)** |
|-------------|--------------|-------------|-------------|------------------|
| **Mild**    | Drug A       | 400         | 380         | **95.0%**        |
| **Mild**    | Drug B       | 200         | 190         | **95.0%**        |
| **Severe**  | Drug A       | 100         | 20          | **20.0%**        |
| **Severe**  | Drug B       | 300         | 210         | **70.0%**        |

### **Overall Recovery Rates (Aggregated Data)**
| **Category** | **Drug A (%)** | **Drug B (%)** |
|-------------|--------------|--------------|
| **Overall Recovery Rate** | **80.0%** | **80.0%** |

---

### **What’s the Paradox?**  
- **For mild cases:** Both drugs have the **same recovery rate** (95%).  
- **For severe cases:** **Drug B** has a **much higher recovery rate** (70%) compared to **Drug A (20%)**.  
- **But when looking at overall recovery rates, both drugs seem equally effective (80%).**  

### **Why Does This Happen?**
- **More patients with severe illness were given Drug B (300 patients), whereas Drug A was mostly given to mild cases (400 patients).**  
- The **difference in patient distribution** causes the overall numbers to be misleading.  

**Lesson:** **Never rely on overall statistics alone—always analyze data within subgroups to avoid incorrect conclusions!**  

--- 

# 📌 Same Stats, Difference Graphs

[The Datasaurus Dozen](https://www.research.autodesk.com/publications/same-stats-different-graphs/)

--- 

# 🎯 Conclusion
Statistics helps us understand data and make informed decisions. However, it’s essential to analyze data carefully to avoid **misinterpretation**, **bias**, and **false conclusions**. 🚀

---
# Python code
- [statistics.py](../statistics.py)
- Explore various python library for statistics e.g. [NumPy](https://numpy.org/doc/stable/reference/routines.statistics.html) and [scipy_stats](https://docs.scipy.org/doc/scipy/reference/stats.html)
---
# LAB

**Ex1:** Find Outliers in a Dataset Using Standard Deviation

Write a Python program that identifies outliers in a dataset using the mean and standard deviation.

Any value that is more than 2 standard deviations away from the mean is considered an outlier.

```python
data = [10, 12, 14, 15, 18, 21, 22, 23, 50]  # 50 is an outlier
```

**Ex2:** Calculate Weighted Mean for a Grading System

Given student grades and their respective weights, compute the weighted mean.

```python
grades = [90, 85, 80, 95]
weights = [0.3, 0.2, 0.2, 0.3]  # Sum of weights should be 1
```

**Ex3:** Analyzing the Effect of Marketing Spend on Sales Using Correlation
Task: Given a dataset of monthly marketing spend (\$) and monthly sales (\$), calculate the correlation coefficient to see if marketing spend influences sales.

```python
marketing_spend = [1000, 2000, 3000, 4000, 5000, 6000]
sales = [5000, 7000, 9000, 11000, 13000, 15000]
```

**Ex4:** Detecting Skewness in a Dataset Using Mean, Median, and Mode
Task: 
1. Write a Python function that analyzes the skewness of a dataset using the mean, median, and mode.

- Right (Positive) Skew: Mean > Median > Mode
- Left (Negative) Skew: Mean < Median < Mode
- Normal Distribution: Mean ≈ Median ≈ Mode

2. Load 3 datasets from [data_source](./three_skewed_datasets.csv) and use the function above to determine the skewness of each dataset. Draw 3 distributions of the datasets on 1 chart to visualize the skewness.


