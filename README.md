# Programming-Assignment-2
This is my submission for the Second Programming Assignment. It introduces us to Numerical Python. In C++, we used to have cmath as the standard numerical library that provides mathematical functions for handling complex numbers but in Python, we now use NumPy.

# Codes below:

# Normalization Problem (Number 1)

import numpy as np

X = np.random.rand(5,5)

mean_X = X.mean()
std_X = X.std()

X_normalized = (X - mean_X) / std_X

np.save('X_normalized.npy', X_normalized)

X, X_normalized

## Output Produced: (Normalization Problem)

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

# Divisible by 3 Problem (Number 2)

import numpy as np

A = np.arange(1, 101).reshape(10, 10) ** 2

div_by_3 = A[A % 3 == 0]

np.save('div_by_3.npy', div_by_3)

A, div_by_3

## Output Produced: (Divisible by 3 Problem)

(array([[    1,     4,     9,    16,    25,    36,    49,    64,    81,
           100],
        [  121,   144,   169,   196,   225,   256,   289,   324,   361,
           400],
        [  441,   484,   529,   576,   625,   676,   729,   784,   841,
           900],
        [  961,  1024,  1089,  1156,  1225,  1296,  1369,  1444,  1521,
          1600],
        [ 1681,  1764,  1849,  1936,  2025,  2116,  2209,  2304,  2401,
          2500],
        [ 2601,  2704,  2809,  2916,  3025,  3136,  3249,  3364,  3481,
          3600],
        [ 3721,  3844,  3969,  4096,  4225,  4356,  4489,  4624,  4761,
          4900],
        [ 5041,  5184,  5329,  5476,  5625,  5776,  5929,  6084,  6241,
          6400],
        [ 6561,  6724,  6889,  7056,  7225,  7396,  7569,  7744,  7921,
          8100],
        [ 8281,  8464,  8649,  8836,  9025,  9216,  9409,  9604,  9801,
         10000]]),
 array([   9,   36,   81,  144,  225,  324,  441,  576,  729,  900, 1089,
        1296, 1521, 1764, 2025, 2304, 2601, 2916, 3249, 3600, 3969, 4356,
        4761, 5184, 5625, 6084, 6561, 7056, 7569, 8100, 8649, 9216, 9801]))

# Authors

Jerome Oldan