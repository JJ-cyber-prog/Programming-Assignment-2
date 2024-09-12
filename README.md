# Programming-Assignment-2
This is my submission for the Second Programming Assignment. It introduces us to Numerical Python. In C++, we used to have cmath as the standard numerical library that provides mathematical functions for handling complex numbers but in Python, we now use NumPy.

# Codes below:

# For number 1: Normalization Problem

import numpy as np

X = np.random.rand(5,5)

mean_X = X.mean()
std_X = X.std()

X_normalized = (X - mean_X) / std_X

np.save('X_normalized.npy', X_normalized)

X, X_normalized

# For number 2: Divisible by 3 Problem

import numpy as np

A = np.arange(1, 101).reshape(10, 10) ** 2

div_by_3 = A[A % 3 == 0]

np.save('div_by_3.npy', div_by_3)

A, div_by_3
