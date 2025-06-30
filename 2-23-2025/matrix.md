# Introduction to Matrices

## Where They Come From and Why We Study Them

### **Where Do Matrices Come From?**
Matrices arise naturally in many areas of mathematics and real-world applications. Historically, they were developed to solve systems of linear equations, but their usefulness extends far beyond that. Here’s how they originated:

1. **Solving Systems of Linear Equations**  
   - Consider a simple system of equations:
$$
     \begin{cases} 
     2x + 3y = 5 \\
     4x - y = 1
     \end{cases}
$$
   - Instead of writing out these equations repeatedly, mathematicians realized they could represent the coefficients in a rectangular array:
$$
     \begin{bmatrix} 
     2 & 3 \\ 
     4 & -1 
     \end{bmatrix}
$$
   - This matrix contains all the necessary information about the system, and mathematical operations can be performed directly on it.

2. **Transformations in Geometry**  
   - When rotating, scaling, or reflecting objects in space, we can use matrices to describe these changes efficiently. For example, a 2D rotation of a point \((x, y)\) by an angle \(\theta\) can be represented as:
$$
     \begin{bmatrix} 
     \cos\theta & -\sin\theta \\ 
     \sin\theta & \cos\theta 
     \end{bmatrix}
     \begin{bmatrix} x \\ y \end{bmatrix}
$$
   - This concept is widely used in computer graphics and robotics.

3. **Networks and Graph Theory**  
   - Relationships between objects (such as connections in a social network) can be represented using **adjacency matrices**, where each entry indicates whether two nodes are connected.

4. **Data Science and Machine Learning**  
   - Data is often stored as large tables (e.g., images are matrices of pixel values, financial records are matrices of numbers), and matrix operations allow efficient processing and analysis.

### **Why Do We Need to Study Matrices?**
Now that we understand where matrices come from, let’s explore why they are essential:

1. **Efficient Problem Solving**  
   - Matrices allow us to solve systems of equations quickly using methods like **Gaussian elimination** and **inverse matrices**.
   - Linear algebra provides elegant and scalable ways to handle high-dimensional problems.

2. **Computer Graphics & Engineering**  
   - From video game development to architectural design, matrices are used to manipulate images, create 3D models, and simulate physics.

3. **Artificial Intelligence & Machine Learning**  
   - Modern AI relies heavily on **matrix operations** for training models. Deep learning algorithms use matrix multiplication extensively.

4. **Quantum Computing & Physics**  
   - Many physical laws are written in matrix form. Quantum mechanics, for example, uses **state vectors and operators**, which are deeply connected to matrices.

5. **Economics and Statistics**  
   - Matrices help in financial modeling, optimization problems, and statistical data analysis.

### **Conclusion**
Matrices are a fundamental tool in mathematics with widespread applications. They provide a structured way to represent and solve problems efficiently in physics, engineering, computer science, economics, and many other fields. By studying matrices, we gain powerful tools to understand and manipulate the world around us!

---

## What is a Matrix?
A **matrix** is a rectangular array of numbers, symbols, or expressions arranged in rows and columns. Matrices are used in various fields, including mathematics, physics, computer science, and engineering.

A general matrix of size $m \times n$ (where $m$ is the number of rows and $n$ is the number of columns) is written as:
$$
A = \begin{bmatrix} 
a_{11} & a_{12} & \cdots & a_{1n} \\ 
a_{21} & a_{22} & \cdots & a_{2n} \\ 
\vdots & \vdots & \ddots & \vdots \\ 
a_{m1} & a_{m2} & \cdots & a_{mn} 
\end{bmatrix}
$$
Each element $a_{ij}$ represents the entry in the $i$-th row and $j$-th column.

---

## Types of Matrices

### 1. **Row Matrix**
A matrix with only one row ($1 \times n$) is called a **row matrix**:
$$
R = \begin{bmatrix} 3 & 5 & 7 & 9 \end{bmatrix}
$$

### 2. **Column Matrix**
A matrix with only one column ($m \times 1$) is called a **column matrix**:
$$
C = \begin{bmatrix} 4 \\ 8 \\ 2 \end{bmatrix}
$$

### 3. **Square Matrix**
A matrix where the number of rows equals the number of columns ($n \times n$) is a **square matrix**:
$$
S = \begin{bmatrix} 2 & 4 & 6 \\ 1 & 3 & 5 \\ 7 & 8 & 9 \end{bmatrix}
$$

### 4. **Zero Matrix (Null Matrix)**
A matrix in which all elements are zero is called a **zero matrix**:
$$
O = \begin{bmatrix} 0 & 0 & 0 \\ 0 & 0 & 0 \end{bmatrix}
$$

### 5. **Identity Matrix**
A **square matrix** where all diagonal elements are $1$ and the rest are $0$ is called an **identity matrix** ($I_n$):
$$
I_3 = \begin{bmatrix} 1 & 0 & 0 \\ 0 & 1 & 0 \\ 0 & 0 & 1 \end{bmatrix}
$$

---

## Matrix Operations

### 1. **Addition of Matrices**
Two matrices of the *same size* can be added by adding their corresponding elements:
$$
A = \begin{bmatrix} 1 & 2 \\ 3 & 4 \end{bmatrix}, \quad
B = \begin{bmatrix} 5 & 6 \\ 7 & 8 \end{bmatrix}
$$
$$
A + B = \begin{bmatrix} 1+5 & 2+6 \\ 3+7 & 4+8 \end{bmatrix} = \begin{bmatrix} 6 & 8 \\ 10 & 12 \end{bmatrix}
$$

### 2. **Scalar Multiplication**
A matrix can be multiplied by a scalar (real number) by multiplying each element:
$$
k A = k \begin{bmatrix} a_{11} & a_{12} \\ a_{21} & a_{22} \end{bmatrix} = \begin{bmatrix} k a_{11} & k a_{12} \\ k a_{21} & k a_{22} \end{bmatrix}
$$

### Example:
If $k = 3$ and 
$
A = \begin{bmatrix} 2 & 4 \\ 6 & 8 \end{bmatrix}
$
then:
$
3A = \begin{bmatrix} 3 \times 2 & 3 \times 4 \\ 3 \times 6 & 3 \times 8 \end{bmatrix} = \begin{bmatrix} 6 & 12 \\ 18 & 24 \end{bmatrix}
$

### 3. **Matrix Multiplication**
If $A$ is an $m \times n$ matrix and $B$ is an $n \times p$ matrix, their product $AB$ is an $m \times p$ matrix obtained by computing the dot product of rows of $A$ with columns of $B$.

#### Example:
$$
A = \begin{bmatrix} 1 & 2 \\ 3 & 4 \end{bmatrix}, \quad
B = \begin{bmatrix} 5 & 6 \\ 7 & 8 \end{bmatrix}
$$
$$
AB = \begin{bmatrix} (1 \times 5 + 2 \times 7) & (1 \times 6 + 2 \times 8) \\ (3 \times 5 + 4 \times 7) & (3 \times 6 + 4 \times 8) \end{bmatrix}
$$
$$
= \begin{bmatrix} 5+14 & 6+16 \\ 15+28 & 18+32 \end{bmatrix} = \begin{bmatrix} 19 & 22 \\ 43 & 50 \end{bmatrix}
$$

---

## Transpose of a Matrix
The **transpose** of a matrix $A$, denoted as $A^T$, is obtained by swapping rows with columns.

Example:
$$
A = \begin{bmatrix} 1 & 2 & 3 \\ 4 & 5 & 6 \end{bmatrix}
$$
$$
A^T = \begin{bmatrix} 1 & 4 \\ 2 & 5 \\ 3 & 6 \end{bmatrix}
$$

---
## Python Code

[Linear Algebra](./linear_algebra.py)

---
## Lab

1. Write a function to add 2 matrices

2. Write a function to multiply 2 matrices

3. Write a function to tranpose a matrix

---
# Note

Using lists as vectors and or matrix is great for exposition but terrible for performance.

In production code, you would want to use the **[NumPy](https://numpy.org/doc/stable/user/absolute_beginners.html)** library, which includes a high-performance array class with all sorts of arithmetic operations included.
