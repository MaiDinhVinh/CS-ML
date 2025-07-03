# Probability

---

## What is Probability?

Probability is a branch of mathematics that deals with measuring the likelihood of events occurring. It is used in various fields such as science, business, artificial intelligence, and everyday decision-making.

**Example:**
- When you flip a coin, will it land on heads or tails?
- When rolling a dice, what is the chance of getting a 6?
- If it's cloudy today, will it rain?

Probability helps answer these questions with numerical values that represent likelihood.

---

## Why Probability Matters?

Probability is important because it helps us:
- Make informed decisions under uncertainty.
- Predict future events based on past data.
- Understand risks in finance, healthcare, and technology.

**Example:**
- A doctor uses probability to determine the likelihood of a patient having a disease based on symptoms.
- Weather forecasts predict rain using probability.
- A business predicts customer demand for a product.

---

## Basic Terminologies

1. **Experiment**: A process that leads to a result.
   - Example: Tossing a coin.
2. **Outcome**: A possible result of an experiment.
   - Example: Heads or tails when flipping a coin.
3. **Sample Space (S)**: The set of all possible outcomes.
   - Example: When rolling a 6-sided die, the sample space is {1, 2, 3, 4, 5, 6}.
4. **Event (E)**: A subset of the sample space.
   - Example: Rolling an even number {2, 4, 6}.
5. **Probability of an Event (P(E))**: A number between 0 and 1 that represents how likely an event is to occur.
   
   Formula:
$$
   P(E) = \frac{\text{Number of favorable outcomes}}{\text{Total number of outcomes}}
$$

$$
    0 \leq P(E) \leq 1
$$
---

## Basic Probability Calculation (Counting)

### Example 1: Tossing a Fair Coin
- Sample Space: {Heads, Tails}
- Probability of getting heads:
  $$
  P(Heads) = \frac{1}{2} = 0.5 (or\ 50\%)
  $$

### Example 2: Rolling a 6-Sided Die
- Sample Space: {1, 2, 3, 4, 5, 6}
- Probability of rolling a 4:
  $$
  P(4) = \frac{1}{6} \approx 0.1667 (or\ 16.67\%)
  $$
- Probability of rolling an even number:
  - Favorable outcomes: {2, 4, 6}
  - Total outcomes: 6
    $$
  P(Even) = \frac{3}{6} = 0.5 (or\ 50\%)
    $$

---

## Real-Life Applications of Probability

1. **Sports:** Coaches analyze player performance probabilities.
2. **Medicine:** Doctors use probabilities to diagnose diseases.
3. **Gaming:** Casinos use probability to design games.
4. **Weather Forecasting:** Meteorologists predict rain probabilities.
5. **Artificial Intelligence:** AI predicts user behavior using probability models.

---
## Independence and Dependence   of Events

### Independent Events

Two events are **independent** if the outcome of one event does not affect the outcome of the other.

**Example:**

- Rolling a die and flipping a coin: The result of the die roll does not impact whether you get heads or tails.

- Choosing a random person’s birthday: One person’s birthday does not affect another’s birthday probability.

For independent events, the probability of both occurring is:

$$
P(A \cap B) = P(A) \times P(B)
$$

**Example Calculation:**

- The probability of rolling a 6 on a fair die: \(P(A) = \frac{1}{6}\)
- The probability of getting heads on a fair coin: \(P(B) = \frac{1}{2}\)
- Since these events are independent, their combined probability is:
  $$
  P(A \cap B) = \frac{1}{6} \times \frac{1}{2} = \frac{1}{12} \approx 8.33%
  $$

### Dependent Events

Two events are **dependent** if the outcome of one event affects the outcome of the other.

**Example:**

- Drawing two cards from a deck **without replacement** (not put back). The probability of drawing an Ace changes after the first card is drawn.

- Weather and outdoor plans: If it rains, the probability of a picnic happening decreases.

Mathematically, the probability of event B occurring given that event A has already occurred  (or the probability of B **conditional on** A) is denoted as:

$$
P(B | A) = \frac{P(A \cap B)}{P(A)}
$$

given that $$P(A) \neq 0$$

When A and B are independent i.e $$P(A \cap B) = P(A) \times P(B)$$

then $$P(B|A) = \frac{ P(A) \times P(B)}{P(A)} = P(B)$$

We ofter rewrite this as 
$$P(A \cap B) = P(B | A) \times P(A)$$

---
## **Bayes' Theorem**

### **What is Bayes' Theorem?**
Bayes’ Theorem is a mathematical formula used to **update probabilities** based on new information. It helps us determine the likelihood of an event occurring, given that we already know some other event has happened.

### **Why Do We Need Bayes' Theorem?**
Bayes' Theorem is useful because it helps us make better predictions and decisions under uncertainty. It allows us to **update our beliefs** when new data is available.

It helps avoid **misleading conclusions** by considering prior probabilities.

### **Real-Life Examples**
1. **Medical Diagnosis**  
   Suppose a patient tests positive for a rare disease. The test is **90% accurate**, but the disease only affects **1 in 10,000 people**. Should the patient panic?  
   - Without Bayes' Theorem, we might think the person has a 90% chance of being sick.  
   - But with Bayes' Theorem, we see that since the disease is rare, the probability of actually being sick is **much lower** than expected.

2. **Spam Filtering in Emails**  
   - Given an email contains the word "lottery," Bayes' Theorem helps calculate the probability that the email is spam based on past data.
   - If past spam emails frequently contain "lottery," the probability increases that the new email is spam.

3. **Self-Driving Cars**  
   - If a self-driving car detects an object in its path, Bayes' Theorem helps determine whether it's a **pedestrian, a car, or a shadow** based on previous observations.


### **The Formula**
It is named after **Thomas Bayes**, an 18th-century mathematician who developed a method to calculate conditional probabilities.

Bayes' Theorem is derived from the basic formula of conditional probability:

$$
P(A | B) = \frac{P(B | A) \times P(A)}{P(B)}
$$

where:
- $P(A | B) = $ Probability of event **A** happening given that **B** has already happened (**posterior probability**)
- $P(B | A) = $Probability of event **B** happening given that **A** has already happened (**likelihood**)
- $P(A) = $ Probability of event **A** happening (**prior probability**)
- $P(B) = $ Probability of event **B** happening (**marginal probability**)


### Rewriten Formla
The **event B** can be **split** into the two mutually exclusive events **"B and A"** and **"B and not A"**. 

**"not A"** ($\neg A$) means A does not happen, then:

$$
P(B) = P(B | A) P(A) + P(B | \neg A) P(\neg A)
$$

Therefore:
$$
P(A|B) = \frac{P(B | A) \times P(A)}{
P(B | A) P(A) + P(B | \neg A) P(\neg A)
}
$$

### **Example: Medical Diagnosis**
Let's say there’s a rare disease that affects **1% of a population** $P(A) = 0.01$, and there is a test for the disease that is **90% accurate** when a person actually has the disease $P(B | A) = 0.9$. However, **5% of healthy people** also get a false positive result $P(B | \neg A) = 0.05$.

We want to find the probability that a person **actually has the disease** given that they **tested positive** $P(A | B)$.

#### **Step 1: Identify the Values**
- **Prior probability:** $P(A) = 0.01$ (1% of people have the disease)
- **Likelihood:** $P(B | A) = 0.9$ (90% of sick people test positive)
- **False positive rate:** $P(B | \neg A) = 0.05$ (5% of healthy people test positive)
- **Total probability of testing positive \( P(B) \):** We use the law of total probability:
  
  $$
  P(B) = P(B | A) P(A) + P(B | \neg A) P(\neg A)
  $$

  Since $P(\neg A) = 1 - P(A) = 0.99$,

  $$
  P(B) = (0.9 \times 0.01) + (0.05 \times 0.99)
  $$

  $$
  = 0.009 + 0.0495 = 0.0585
  $$

#### **Step 2: Apply Bayes' Theorem**
$$
P(A | B) = \frac{P(B | A) P(A)}{P(B)} = \frac{(0.9 \times 0.01)}{0.0585}
$$

$$
= \frac{0.009}{0.0585} = 0.1538\ (or\ 15.38\%)
$$

---

### **What Does This Mean?**
Even though the test is **90% accurate**, if someone tests positive, they **only have a 15.38% chance** of actually having the disease! This is because the disease is very rare, and false positives are common.

---

### **Why Is This Important?**
- **Prevents Misinterpretation of Probabilities**: Many people assume a positive test means they **definitely** have the disease, but Bayes' Theorem shows that the real probability is much lower.
- **Used in Decision Making**: Doctors, AI systems, and even fraud detection use it to **weigh new evidence properly**.
- **Reduces Uncertainty**: It helps adjust beliefs when new data is introduced.

---
## **Random Variable**  

### **What is a Random Variable?**  
A **random variable** is a numerical value assigned to the outcome of a random event. It helps us describe uncertainty in a **mathematical way**. Instead of dealing with words like "win" or "lose," we convert them into numbers that we can analyze.  

For example:
- When flipping a coin, we can assign **0 for tails** and **1 for heads** instead of just saying "heads or tails."
- When rolling a die, we can use the numbers **1, 2, 3, 4, 5, 6**, which naturally represent different outcomes.  

---

### **Types of Random Variables**  
There are two main types:  

#### **1. Discrete Random Variables**  
A **discrete random variable** takes on a **finite or countable** number of values. These values are often whole numbers.  

**Example 1: Rolling a Die**  
- Let $X$ be the random variable representing the outcome of rolling a fair 6-sided die.  
- The possible values of $X$ are:  
  $$
  X = \{1, 2, 3, 4, 5, 6\}
  $$
- Each outcome has a probability of **1/6**.  

**Example 2: Number of Heads in 3 Coin Tosses**  
- Let $Y$ represent the number of heads when flipping a coin 3 times.  
- The possible values of $Y$ are:  
  $$
  Y = \{0, 1, 2, 3\}
  $$
  - 0 heads (TTT)  
  - 1 head (HTT, THT, TTH)  
  - 2 heads (HHT, HTH, THH)  
  - 3 heads (HHH)  

Each outcome can be counted, making it a **discrete** random variable.

---

#### **2. Continuous Random Variables**  
A **continuous random variable** can take on an **infinite** number of values within a range. It is typically used to measure things like height, temperature, time, or weight.  

**Example 3: Temperature in a City**  
- Let $T$ represent the temperature in New York tomorrow.  
- Possible values could be **any real number** like:  
  $$
  T = 25.4°C, 25.43°C, 25.437°C, 25.4371°C, \dots
  $$
- Since the temperature can take **any** value within a range (like 25°C to 30°C), it is **continuous**.  

**Example 4: Time Taken to Finish a Race**  
- Let $Z$ be the time taken for a runner to finish a marathon.  
- The possible values of $Z$ could be:  
  $$
  Z = 2.3, 2.31, 2.314, 2.3142, \dots \text{ (in hours)}
  $$
- Since the time can be **any decimal value**, it is **continuous**.  

---

### **Probability Distributions of Random Variables**  
A **probability distribution** describes how likely different values of a random variable are.  

**For Discrete Random Variables: Probability Mass Function (PMF)**  
For a discrete random variable, we use a **probability mass function (PMF)** to describe how probabilities are distributed.  

**Example: Rolling a Die**  
- Let $X$ be the outcome of rolling a die.  
- The **PMF** gives the probability of each outcome:  
  $$
  P(X = k) = \frac{1}{6}, \quad k = 1, 2, 3, 4, 5, 6
  $$
This means each number has a **1/6 (or 16.67%) chance** of occurring.

**:two: For Continuous Random Variables: Probability Density Function (PDF)**  
For continuous variables, we use a **probability density function (PDF)** instead of a PMF.  

**Example: Height of People in a City**  
- Let $H$ be the height of a randomly selected person.  
- The **PDF** describes the likelihood of different height values.  
- **Probability of an exact value is considered to be 0**
$$
P(an\ exact\ value) = \frac{1}{Number\ of\ all\ exact\ values}
$$

$$
= \frac{1}{\infty} = 0
$$
- We don’t talk about exact probabilities but rather **probabilities within a range** (e.g., 170 cm to 175 cm).

**Example: Probability of a range**
![Probability of a range](./probability%20within%20a%20range.png)

Here is the **Exponential Probability Density Function (PDF)** with $\lambda = 1$. The **orange-shaded region** represents the probability of the random variable falling between **$1 \leq X \leq 1.2$**. The **dashed black lines** indicate the boundaries of this range.

---
### Cumulative Distribution Function 

The **Cumulative Distribution Function (CDF)** provides the probability that a **random variable** $X$ takes on a value **less than or equal to** a certain number $x$. In other words, it gives the accumulated probability up to $x$.

For a random variable $X$, the **Cumulative Distribution Function (CDF)**, denoted as $F(x)$, is defined as:

$$
F(x) = P(X \leq x)
$$

This means that for any value $x$, $F(x)$ represents the **total probability mass (or density) accumulated up to $x$**.


**:triangular_flag_on_post: Relationship Between CDF and PDF**
:one: For a **continuous random variable**, the **Probability Density Function (PDF)** and the **Cumulative Distribution Function (CDF)** are related as:

$$
F(x) = \int_{-\infty}^{x} f(t) dt
$$

where:
- $f(x)$ is the **PDF** (probability density function).
- The **CDF is the integral of the PDF**.

:two: For **discrete distributions**, the **CDF is the sum** of the probabilities:

$$
F(x) = \sum_{X \leq x} P(X)
$$

---

**Example of CDF for a Discrete Random Variable**
Let \( X \) be the number of heads when flipping a coin 3 times. The possible values of \( X \) and their probabilities are:

| $X$ | Probability $P(X)$ | CDF $F(x) = P(X \leq x)$ |
|-----|--------------------|--------------------------|
| 0   | 1/8 (0.125)        | 0.125                    |
| 1   | 3/8 (0.375)        | 0.125 + 0.375 = 0.500    |
| 2   | 3/8 (0.375)        | 0.500 + 0.375 = 0.875    |
| 3   | 1/8 (0.125)        | 0.875 + 0.125 = 1.000    |

So:
- $P(X \leq 1) = 0.5$ (50% probability of getting at most 1 head).
- $P(X \leq 2) = 0.875$ (87.5% probability of getting at most 2 heads).

🔹 **Graph:** The CDF would be a **step function**, increasing at each valid $X$.

![_]()

---

**Example of CDF for a Continuous Random Variable**
For an **Exponential Distribution** with rate $\lambda = 1$, the **PDF** is:

$$
f(x) = e^{-x}, \quad x \geq 0
$$

To compute the **CDF**:

$$
F(x) = \int_{0}^{x} e^{-t} dt = 1 - e^{-x}, \quad x \geq 0
$$

✅ **Example Values**:

| $x$ | $F(x)$    |
|-----|-----------|
| 0   | 0         |
| 1   | 0.632     |
| 2   | 0.864     |
| 3   | 0.950     |
| 4   | 0.982     |

This means:
- **63.2% of values are ≤ 1**.
- **86.4% of values are ≤ 2**.
- **95% of values are ≤ 3**.

🔹 **Graph:** The CDF is a smooth, increasing curve approaching 1 as $x \to \infty$.



---

**Plotting a CDF for a Continuous Distribution**
Now, let’s visualize a CDF using an **Exponential Distribution** $ Exp(\lambda=1) $

![CDF](./cdf.png)

 **$ P(1 \leq X \leq 2) $ is the vertical difference between $ F(1) $ and $ F(2) $**:

- **The blue curve** represents the **Cumulative Distribution Function (CDF)**.
- **The orange vertical line** represents the probability $ P(1 \leq X \leq 2) = F(2) - F(1) $.
- **Dashed black horizontal lines** indicate the cumulative probabilities at $x = 1$ and $ x = 2 $.

---
**Key Takeaways About CDF**
✅ **CDF accumulates probabilities**, giving the probability that $ X $ is **less than or equal to** a certain value.  
✅ **For discrete variables**, the CDF is a **step function**.  
✅ **For continuous variables**, the CDF is a **smooth, increasing function**.  
✅ **The CDF is the integral of the PDF**:  
   $$
   F(x) = \int_{-\infty}^{x} f(t) dt
   $$
✅ **To find probabilities over a range**, subtract the CDF values:
$$
   P(a \leq X \leq b) = F(b) - F(a)
$$


---

### **Expectation (Mean) of a Random Variable**  
The **expected value** (mean) is the **average outcome** you would get if you repeated an experiment many times.  

**:one: For a Discrete Random Variable**  
$$
E(X) = \sum [x \cdot P(X = x)]
$$
**Example: Rolling a Die**  
$$
E(X) = (1 \times \frac{1}{6}) + (2 \times \frac{1}{6}) + (3 \times \frac{1}{6}) + (4 \times \frac{1}{6}) + (5 \times \frac{1}{6}) + (6 \times \frac{1}{6})
$$
$$
= \frac{1+2+3+4+5+6}{6} = \frac{21}{6} = 3.5
$$
This means that, on average, rolling a die many times will give a result **close to 3.5**.

**:two: For a Continuous Random Variable**  
For continuous variables, we use integration:
$$
E(X) = \int x f(x) dx
$$
where $ f(x) $ is the probability density function.

---

### **Variance and Standard Deviation of a Random Variable**  
- **Variance $Var(X)$** measures how **spread out** the values are.
- **Standard Deviation $\sigma(X)$** is just the square root of variance.

**:one: For a discrete random variable:**
$$
Var(X) = E(X^2) - [E(X)]^2
$$

**:two: For a continuous random variable**, 
A continuous random variable $ X $ has probability density function (PDF) $ f(x) $, the variance is given by:

$$
\text{Var}(X) = E[X^2] - [E[X]]^2
$$

where:

1. **Expected value (Mean):**
   $$
   E[X] = \int_{-\infty}^{\infty} x f(x) dx
   $$
2. **Expected value of \(X^2\):**
   $$
   E[X^2] = \int_{-\infty}^{\infty} x^2 f(x) dx
   $$
3. **Variance:**
   $$
   \text{Var}(X) = \int_{-\infty}^{\infty} (x - \mu)^2 f(x) dx
   $$
   where $ \mu = E[X] $.

---

### **Key Takeaways**
✅ A **random variable** assigns numerical values to outcomes of a random event.  
✅ **Discrete random variables** take on countable values (e.g., rolling a die).  
✅ **Continuous random variables** take on infinite values in a range (e.g., temperature).  
✅ The **probability distribution** tells us the likelihood of different values occurring.  
✅ **Mean (Expectation)** gives the long-run average outcome.  
✅ **Variance and Standard Deviation** measure how spread out the values are.  


---
# LAB - Monte Carlo Simulation

:large_blue_diamond: **Monte Carlo Simulation** is a statistical technique used to model uncertainty and estimate probabilities by running a large number of random simulations. Instead of solving a probability problem mathematically, we use random sampling to approximate the outcome.

:large_blue_diamond: **Real-World Applications:**
- Finance: Estimating stock market risk.
- Engineering: Predicting system failures.
- Medicine: Simulating drug effectiveness.

:large_blue_diamond: **How Does It Work?**
1. Define the Problem: 
  Identify the independent or dependent probability events.
2. Generate Random Events:
  Use Python’s random module to simulate random trials.
3. Count Successful Outcomes:
   Track how often the desired event occurs.
4. Estimate Probability:
   Divide successful trials by total trials:

$$
P(event) \approx \frac{Successful Simulations}{Total Simulations}
$$


:large_blue_diamond: **Scenario:** 

You are playing a complex game in casino which involves 4 mini games: rolling a dice, flipping a fair coin, drawing cards from a 52-card deck and spinning a roulette wheel. 
To **win the game**, you need to achieve **all** of the following independent conditions:  

1. **Roll a fair 6-sided dice and get a 5 or a 6**.
2. **Flip a fair coin and get heads**.
3. **Draw a red card from a shuffled standard deck of 52 cards** 
   (26 red cards: 13 hearts + 13 diamonds).
4. **Spin a roulette wheel and land on a number divisible by 3** 
   (Roulette wheel has 36 numbers from 1 to 36).

:large_blue_diamond: **Task:**  
1. **Theoritical Probability** 
   Use Maths to calculate the probability of winning the game

2. **Empirical Probability**
   Write a **Monte Carlo simulation** in Python to estimate the probability of winning the game by running **1,000,000 simulations**.

3. Discuss the theoritical vs. empirical probabilities
