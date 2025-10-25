# NumPy Cheat Sheet (Minimal & Clean)

## Importing NumPy

```python
import numpy as np
```

## Creating Arrays

* `np.array([1, 2, 3])` – 1D array
* `np.array([[1, 2, 3], [4, 5, 6]])` – 2D array
* `np.zeros((3,3))` – 3x3 matrix of zeros
* `np.ones((2,4))` – 2x4 matrix of ones
* `np.full((2,3), 7)` – Filled with constant value
* `np.eye(4)` – Identity matrix (4x4)
* `np.arange(0, 10, 2)` – 0 to 10 step 2
* `np.linspace(0, 1, 5)` – 5 values between 0 and 1

## Random Values

* `np.random.seed(42)` – For reproducibility
* `np.random.randint(1, 10, 5)` – Random integers
* `np.random.rand(3,2)` – Uniform random floats (0–1)
* `np.random.randn(3,2)` – Normal distribution
* `np.random.choice([1,2,3,4])` – Random choice

## Array Inspection

* `arr.shape` – Dimensions
* `arr.ndim` – Number of dimensions
* `arr.size` – Total elements
* `arr.dtype` – Data type

## Indexing & Slicing

* `arr[0]` – First element
* `arr[-1]` – Last element
* `arr[1:4]` – Slice
* `arr[:,0]` – First column
* `arr[0,:]` – First row
* `arr[1:3, 2:4]` – 2D slice

## Reshaping & Combining

* `arr.reshape(3,4)` – Change shape
* `arr.flatten()` – To 1D
* `np.concatenate([a,b])` – Join
* `np.vstack((a,b))` – Vertical stack
* `np.hstack((a,b))` – Horizontal stack
* `np.column_stack((a,b))` – Stack as columns

## Math Operations

* `arr + 5`, `arr * 2` – Element-wise
* `arr1 + arr2`
* `np.add(arr1, arr2)`
* `np.sum(arr)`
* `np.mean(arr)`
* `np.median(arr)`
* `np.std(arr)` – Standard deviation
* `np.min(arr)` / `np.max(arr)`
* `np.abs(arr)`

## Boolean Filtering

* `arr > 10`
* `arr[arr > 10]`
* `np.where(arr > 10, "Yes", "No")`

## Matrix Operations

* `np.dot(a,b)` – Dot product
* `a @ b` – Dot (shorthand)
* `np.transpose(arr)`
* `np.linalg.inv(arr)` – Inverse
* `np.linalg.det(arr)` – Determinant
* `np.linalg.eig(arr)` – Eigenvalues & eigenvectors

## Handling Missing Data

* `np.isnan(arr)`
* `np.nanmean(arr)`
* `np.nan_to_num(arr)` – Replace NaN with 0

## Copy vs View

* `b = arr.copy()` – Independent copy
* `c = arr.view()` – Linked view

## Broadcasting

Works even with different shapes (if compatible):

```python
arr + 5
arr + np.array([1,2,3])
```
