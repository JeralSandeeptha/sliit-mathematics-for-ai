# Linear Algebra

`Linear Algebra` scales basic algebra up to handle thousands or millions of variables simultaneously using arrays.

<br/>

## Vectors (1D Arrays)

`Math`: A vector is an ordered list of numbers representing a point or a direction in space.

\(\vec{v}=\left[\begin{matrix}4\\ 3\end{matrix}\right]\)

`Geometric Intuition`: Start at the origin \((0,0)\), move 4 units right, and 3 units up.

`NumPy Equivalent`:

```python
import numpy as np
v = np.array([4, 3])
```

<br/>

## The Vector Dot Product

`Math`: Multiply corresponding components of two vectors and sum the results. It outputs a single scalar number.

\(\left[\begin{matrix}1\\ 2\\ 3\end{matrix}\right]\cdot \left[\begin{matrix}4\\ 5\\ 6\end{matrix}\right]=(1\times 4)+(2\times 5)+(3\times 6)=4+10+18=32\)

`ML Application`: The dot product measures similarity. If you dot-product a user's preferences vector with a movie's features vector, a high score means a great recommendation.

`NumPy Equivalent`:

```python
a = np.array([1, 2, 3])
b = np.array([4, 5, 6])
similarity = np.dot(a, b)  # Returns 32
```

<br/>

## Matrices (2D Arrays)

`Math`: A grid of numbers with \(m\) rows and \(n\) columns (dimension: \(m \times n\)).

\(A=\left[\begin{matrix}1&2\\ 3&4\end{matrix}\right]\)

`ML Application`: Your dataset. Each row is a different sample (e.g., a patient); each column is a feature (e.g., blood pressure, age).

`NumPy Equivalent`:

```python
A = np.array([[1, 2], [3, 4]])
```

<br/>

## Matrix Multiplication

`Math`: To multiply matrix \(A\) by matrix \(B\), compute the dot product of each row of \(A\) with each column of \(B\).

`The Golden Rule`: You can only multiply matrices if the number of columns in \(A\) matches the number of rows in \(B\). If \(A\) is \((2 \times \mathbf{3})\) and \(B\) is \((\mathbf{3} \times 4)\), the output matrix will be \((2 \times 4)\)

`ML Application`: This is the forward pass of every neural network layer. Input features (\(X\)) are multiplied by a weight matrix (\(W\)) to compute predictions (\(Y\)).

```python
# Neural network layer simulation: 1 sample with 3 features
X = np.array([[0.5, 1.2, -0.8]])  # Shape: (1, 3)
W = np.array([[0.1, 0.4], 
              [0.2, 0.5], 
              [0.3, 0.6]])       # Shape: (3, 2)

# Compute forward pass: X multiplied by W
Y = np.matmul(X, W)               # Shape: (1, 2)
# Or using the shorthand operator: Y = X @ W
```

<br/>

## Summary

| Concept | Algebraic Notation | NumPy Syntax | PyTorch Syntax (Deep Learning) |
| :--- | :--- | :--- | :--- |
| **Vector Dot Product** | \(\vec{u} \cdot \vec{v}\) | `np.dot(u, v)` | `torch.dot(u, v)` |
| **Matrix Multiplication** | \(A \times B\) or \(AB\) | `np.matmul(A, B)` or `A @ B` | `torch.matmul(A, B)` or `A @ B` |
| **Matrix Transpose** | \(A^{T}\) | `A.T` | `A.T` or `A.t()` |
| **Element-wise Mult.** | \(A \odot B\) | `A * B` | `A * B` |
