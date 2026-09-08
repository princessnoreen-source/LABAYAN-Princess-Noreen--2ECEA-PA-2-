## PROGRAMMING ASSIGNMENT #2
### by: LABAYAN, Princess Noreen - 2ECEA

This repository is a partial requirement to ECE 2112 "Advanced Computer Programming and Algorithms" as Programming Assignment #2. Its objective is to demonstrate the use of the NumPy library in performing numerical computations, array manipulation, Boolean filtering, and file handling through three different problems.


## A. REPRODUCIBLE NORMALIZATION PROBLEM

The goal of this problem is to create a reproducible 5 × 5 NumPy array of random integers and normalize all of its elements using the array's mean and standard deviation.

Following were the operators used to execute the code:

1. ```np.random.seed(seed_value)```

   This function initializes the random number generator to produce the same sequence of random numbers every time the program is executed.

Example:

```python
np.random.seed(2112)
```

2. ```np.random.randint(start, stop, size=(rows, columns))```

   This function generates random integers within a specified range and stores them in a NumPy array of the given dimensions.

Example:

```python
np.random.randint(10, 101, size=(5,5))
```

3. ```variable_name.mean()```

   This function returns the average value of all elements in a NumPy array.

Example:

```python
np.mean(X)
```

4. ```variable_name.std()```

   This function returns the population standard deviation of all elements in a NumPy array.

Example:

```python
np.std(X)
```

5. ```np.save("filename.npy", variable_name)```

   This function saves a NumPy array as a `.npy` file.

Example:

```python
np.save("X_normalized.npy", X_normalized)
```

Using the operators discussed above, the function below was created to normalize every element in the array and save the resulting array as a NumPy file.

```python
np.random.seed(2112)
X = np.random.randint(10, 101, size=(5, 5))
Z = (X - np.mean(X)) / (np.std(X))
X_normalized = Z
```

---

## B. CUBES DIVISIBLE BY 4 PROBLEM

The goal of this problem is to create the first 100 positive integers, cube every element, reshape the result into a 10 × 10 array, then select only the cubed values divisible by 4.

Following were the operators used to execute the code:

1. ```np.arange(start, stop, step)```

   This function generates evenly spaced integer values within a specified range.

Example:

```python
np.arange(1, 101, 1)
```

2. ```np.power(variable_name, exponent)```

   This function raises every element of a NumPy array to the specified exponent.

Example:

```python
np.power(C, 3)
```

3. ```variable_name.reshape(rows, columns)```

   This function changes the shape of a NumPy array without changing its data.

Example:

```python
C.reshape(10,10)
```

4. ```variable_name[condition]```

   This operator performs Boolean indexing by selecting only the elements that satisfy the given condition.

Example:

```python
C[C % 4 == 0]
```

5. ```len(variable_name)```

   This function returns the number of elements stored in the array.

Example:

```python
len(div_by_4)
```

Using the operators discussed above, the function below was created to generate the cubed values divisible by 4 and save the selected values as a NumPy file.

```python
c = np.arange (1, 101, 1)
C = np.power (c,3)
C = C.reshape (10,10)
div_by_4 = C[C % 4 == 0]
```

---

## C. ABOVE-MEAN SQUARES PROBLEM

The goal of this problem is to create a 6 × 6 NumPy array containing the squares of the first 36 positive integers, compute the mean of all elements, and select only the values greater than the computed mean.

Following were the operators used to execute the code:

1. ```np.arange(start, stop, step)```

   This function generates evenly spaced integer values within a specified range.

Example:

```python
np.arange(1, 37, 1)
```

2. ```np.power(variable_name, exponent)```

   This function raises every element of a NumPy array to the specified exponent.

Example:

```python
np.power(S, 2)
```

3. ```variable_name.reshape(rows, columns)```

   This function changes the dimensions of a NumPy array while preserving all of its elements.

Example:

```python
S.reshape(6,6)
```

4. ```variable_name.mean()```

   This function computes and returns the average value of all elements in a NumPy array.

Example:

```python
S.mean()
```

5. ```variable_name[condition]```

   This operator selects only the elements that satisfy the specified Boolean condition.

Example:

```python
S[S > S_mean]
```

Using the operators discussed above, the function below was created to obtain all values greater than the mean of the array and save the selected values as a NumPy file.

```python
S = np.arange (1, 37, 1)
S = np.power (S,2)
S = S.reshape (6,6)
S_mean = np.mean(S)
above_mean = S[S > S_mean ]
```

Thank youuu for reading! <3
