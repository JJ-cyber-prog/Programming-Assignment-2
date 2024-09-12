# Programming-Assignment-2
This is my submission for the Second Programming Assignment. It introduces us to Numerical Python. In C++, we used to have cmath as the standard numerical library that provides mathematical functions for handling complex numbers but in Python, we now use NumPy.

# Codes below:

# Normalization Problem

import numpy as np

X = np.random.rand(5,5)

mean_X = X.mean()
std_X = X.std()

X_normalized = (X - mean_X) / std_X

np.save('X_normalized.npy', X_normalized)

X, X_normalized

## Output Produced:

(array([[0.4272085 , 0.73938683, 0.30739049, 0.47560545, 0.26809221],
        [0.95168975, 0.74927265, 0.18365677, 0.9644595 , 0.46775763],
        [0.71868748, 0.44998209, 0.30445559, 0.72839006, 0.8826961 ],
        [0.36463972, 0.59649713, 0.42370154, 0.64967402, 0.29178766],
        [0.455464  , 0.20363935, 0.31962733, 0.67481973, 0.46794046]]),
 array([[-0.42441031,  0.96362946, -0.9571576 , -0.20922277, -1.13188971],
        [ 1.9075928 ,  1.00758484, -1.50731535,  1.96437098, -0.24411655],
        [ 0.87159387, -0.32315199, -0.97020709,  0.91473449,  1.60082603],
        [-0.70261016,  0.3282984 , -0.44000331,  0.56473901, -1.02653254],
        [-0.29877776, -1.41846673, -0.90274889,  0.67654448, -0.24330362]]))

# Divisible by 3 Problem

import numpy as np

A = np.arange(1, 101).reshape(10, 10) ** 2

div_by_3 = A[A % 3 == 0]

np.save('div_by_3.npy', div_by_3)

A, div_by_3

## Output Produced:

