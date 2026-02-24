# NumPy Fundamentals: Arrays, Operations, and Matrix Manipulation

## Overview

This project introduces core features of the NumPy library for numerical computing in Python. It covers:

* Array creation (1D and multi-dimensional)
* Data types and type conversion
* Array initialization methods
* Random number generation
* Mathematical operations
* Indexing and slicing
* Matrix operations
* Logical expressions and conditional selection

The notebook serves as a foundational guide to working with NumPy arrays in scientific and data-oriented applications.

---

## Environment

* Python 3.12.4
* NumPy
* Jupyter Notebook
* Conda base environment

---

## 1. Array Creation

### One-Dimensional Arrays

```python
mt = np.array([12, 34, 26, 18, 10])
```

NumPy arrays are instances of `numpy.ndarray` and provide optimized storage and vectorized operations.

---

### Specifying Data Types

Arrays can be created with explicit data types:

```python
np.array([1, 2, 3], dtype=np.float64)
np.array([1, 2, 3], dtype=np.int32)
```

Controlling data types is important for:

* Memory efficiency
* Numerical precision
* Performance

---

### Type Conversion

```python
mt.astype(np.int32)
mt.astype(float)
```

When converting from float to integer, values are truncated (not rounded).

---

## 2. Multi-Dimensional Arrays

### Two-Dimensional Arrays

```python
np.array([[7, 2, 23],
          [12, 27, 4],
          [5, 34, 23]])
```

NumPy supports N-dimensional arrays for matrix and tensor operations.

---

### Predefined Array Constructors

* `np.empty(shape)` – uninitialized values
* `np.zeros(shape)` – filled with zeros
* `np.ones(shape)` – filled with ones
* `np.eye(n)` – identity matrix

These functions allow efficient initialization for numerical workflows.

---

## 3. Random Number Generation

### Basic Random Values

```python
np.random.random(5)
np.random.randn(5)
```

* `random()` generates values in [0, 1)
* `randn()` generates values from a normal distribution

---

### Using a Random Generator with Seed

```python
rng = np.random.default_rng(1)
rng.random(3)
rng.integers(10, size=(3,4))
```

Seeding ensures reproducibility, which is critical in simulations and data science experiments.

---

## 4. Array Utilities

### Removing Duplicates

```python
np.unique(array)
```

Returns sorted unique elements.

---

### Shape and Dimensions

```python
k.shape
```

Returns a tuple representing array dimensions.

---

## 5. Mathematical Operations

NumPy provides optimized mathematical functions:

```python
k.max()
k.min()
k.sum()
k.mean()
k.std()
```

These operations are vectorized and significantly faster than manual Python loops.

---

### Universal Functions (ufuncs)

Operate element-wise:

```python
np.sqrt(array)
np.exp(array)
```

These functions apply automatically to every element in the array.

---

## 6. Indexing and Slicing

### One-Dimensional Slicing

```python
m[1]
m[0:2]
m[1:]
m[-3:]
```

Supports:

* Standard slicing
* Negative indexing
* Subarray extraction

---

### Multi-Dimensional Indexing

```python
array[row, column]
array[row, :]
array[:, column]
```

Allows extraction of specific rows or columns efficiently.

---

## 7. Matrix Operations

### Element-wise Operations

```python
n + o
n * o
```

Multiplication with `*` performs element-wise multiplication, not matrix multiplication.

---

### Reshaping and Transpose

```python
np.arange(15).reshape((3,5))
array.T
array.transpose((1,0))
```

Reshaping reorganizes data layout without copying when possible.
Transpose swaps axes.

---

## 8. Logical Operations and Conditional Selection

### Boolean Masks

```python
v > 0
```

Produces a boolean array.

---

### Conditional Replacement with `where`

```python
np.where(condition, value_if_true, value_if_false)
```

Enables vectorized conditional logic across arrays.

---

## Learning Objectives

By completing this notebook, you should understand:

* How NumPy arrays differ from Python lists
* The importance of data types in numerical computing
* Efficient array initialization techniques
* Vectorized mathematical operations
* Indexing and slicing multi-dimensional data
* Broadcasting and element-wise computation
* Logical filtering and conditional transformations

NumPy is foundational for:

* Data science
* Machine learning
* Scientific computing
* Numerical simulation
* Signal processing
