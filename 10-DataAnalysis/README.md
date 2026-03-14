# NumPy Notes (Data Analysis Basics)

## What is NumPy?

**NumPy (Numerical Python)** is a fundamental library for scientific computing in Python.
It provides:

* High-performance **multidimensional arrays**
* Mathematical functions to operate on arrays
* Tools for **linear algebra, statistics, and random numbers**

NumPy is widely used in **Data Science, Machine Learning, and Data Analysis**.

---

# Installation

```bash
pip install numpy
```

---

# Importing NumPy

```python
import numpy as np
print(np.__version__)
```

`np` is a common alias used for NumPy.

---

# Creating NumPy Arrays

## 1D Array

```python
import numpy as np

arr1 = np.array([1,2,3,4,5,6])

print(arr1)
print(type(arr1))
print(arr1.shape)
```

Output explanation:

* `type()` → shows it is a NumPy array
* `shape` → tells number of rows and columns

---

## Reshaping Arrays

```python
arr2 = np.array([1,2,3,4,5,6,7,8])
arr2.reshape(2,4)
```

Converts a **1D array → 2D array**

Rows = 2
Columns = 4

---

## Creating 2D Arrays

```python
arr2 = np.array([[12,21,34],
                 [45,87,10]])

print(arr2.shape)
print(arr2)
```

---

# Useful Array Creation Functions

## arange()

Creates evenly spaced values.

```python
np.arange(0,10,2).reshape(5,1)
```

Output example:

```
[[0]
 [2]
 [4]
 [6]
 [8]]
```

---

## ones()

Creates an array filled with **1s**

```python
np.ones((3,4))
```

Output:

```
[[1. 1. 1. 1.]
 [1. 1. 1. 1.]
 [1. 1. 1. 1.]]
```

---

## Identity Matrix

```python
np.eye(3)
```

Output:

```
[[1 0 0]
 [0 1 0]
 [0 0 1]]
```

Diagonal elements = **1**

---

# NumPy Array Attributes

```python
arr = np.array([[1,2,3],
                [4,5,6]])

print("Shape:",arr.shape)
print("Number of dimensions:",arr.ndim)
print("Size:",arr.size)
print("Data type:",arr.dtype)
print("Item size:",arr.itemsize)
```

Explanation:

| Attribute | Meaning                     |
| --------- | --------------------------- |
| shape     | rows × columns              |
| ndim      | number of dimensions        |
| size      | total elements              |
| dtype     | data type                   |
| itemsize  | memory size of each element |

---

# Vectorized Operations

NumPy performs **fast element-wise operations**.

```python
arr1 = np.array([1,2,3,4,5])
arr2 = np.array([10,20,30,40,50])

print(arr1 + arr2)
print(arr1 - arr2)
print(arr1 * arr2)
print(arr1 / arr2)
print(arr1 % arr2)
```

Output is calculated **element by element**.

This is much **faster than Python loops**.

---

# Universal Functions (ufunc)

Functions applied to the **entire array**.

```python
arr = np.array([2,3,4,5,6])

np.sqrt(arr)
np.exp(arr)
np.sin(arr)
np.log(arr)
```

Examples:

* `sqrt()` → square root
* `exp()` → exponential
* `sin()` → sine
* `log()` → natural logarithm

---

# Array Indexing

```python
arr = np.array([[1,2,3],
                [4,5,6],
                [7,8,9]])

print(arr[0][0])
```

Output:

```
1
```

---

# Array Slicing

```python
print(arr[0:2,2:])
```

Meaning:

Rows → `0 to 1`
Columns → `2 to end`

Example output:

```
[[3]
 [6]]
```

---

# More Slicing Examples

```python
print(arr[1:])
```

Output:

```
[[4 5 6]
 [7 8 9]]
```

---

```python
print(arr[1:,2:])
```

Output:

```
[[6]
 [9]]
```

---

# Modifying Array Elements

```python
arr[0,0] = 100
print(arr)
```

Output:

```
[[100   2   3]
 [  4   5   6]
 [  7   8   9]]
```

---

# Modify Multiple Values

```python
arr[1:] = 200
print(arr)
```

Output:

```
[[100   2   3]
 [200 200 200]
 [200 200 200]]
```

---

# Broadcasting (Important Concept)

Broadcasting allows operations between arrays of **different shapes**.

Example:

```python
arr = np.array([1,2,3])
print(arr + 5)
```

Output:

```
[6 7 8]
```

NumPy automatically adds **5 to each element**.

---

# Random Number Generation

```python
np.random.rand(3,3)
```

Creates random numbers between **0 and 1**

---

```python
np.random.randint(1,10,(3,3))
```

Random integers between **1 and 9**

---

# Statistical Functions

```python
arr = np.array([10,20,30,40])

np.mean(arr)
np.median(arr)
np.std(arr)
np.sum(arr)
```

---

# Why NumPy is Important in Data Science

NumPy is used because it is:

* Faster than Python lists
* Memory efficient
* Supports vectorized operations
* Foundation of libraries like:

  * Pandas
  * Scikit-Learn
  * TensorFlow
  * PyTorch

---

# Summary

NumPy provides:

* Powerful **array structures**
* Fast **mathematical operations**
* Efficient **data manipulation**
* Core functionality for **Data Science and Machine Learning**

---
