# ECE-2112-PA-2

**Made by: Lanz Joseph S. Pelayo || 2ECE-B**

# Introduction
This repository contains an explanation of the code for the programming assignment, which the author has made available for viewing. Specifically, the contents of this repository aim to address Programming Assignment #2, which comprises 3 problems, for the Academic year of 2026-2027 in ECE 2112. This aims to help viewers explain how the author used the functions for the program to work, using the author's knowledge of numerical Python from module 2. 

# A. REPRODUCIBLE NORMALIZATION PROBLEM

Instructions:
Create a reproducible random 5 × 5 integer ndarray named X. Use the following two statements before
performing any calculation:

`np.random.seed(2112)
X = np.random.randint(10, 101, size=(5, 5))`

And normalize the array using the standard score formula. Store the normalized array in X normalized and save X normalized in:
`X_normalized.npy`

The following methods were used in this problem to create a unique function:

• `np.mean()` = A built-in function in numpy that automatically takes the average or mean value from an list or an array without manually calculating the mean through hard code.

Example: 
`
X = [ 10, 20, 30, 40, 50]
np.mean(X) = 30.0
`

• `np.std()` = A built-in function in the Numpy library that automatically shows how much the numbers within the dataset or array are spread out or far from the mean.

Example:
`
X = np.array([2, 4, 6, 10])
mean =  X.mean() #---> 6.0
standard deviation #--->  2.83
`

With the use of `np.mean()` and `np.std()`  ,this allows the author to take the mean and standard deviation of the random 5X5 array much more quickly instead 
of hardcoding it. It also allows the author to formulate and create the normalized array by utilizing the two functions to calculate its normalized value
or z-score. Afterward, It allows to show the mean and it's standard deviation of the normalized values

```python
import numpy as np
np.random.seed(2112)
X = np.random.randint(10, 101, size=(5, 5))

X_normalized = (X-(np.mean(X)))/(np.std(X)) #---> Used the mean and standard deviation functions to calculate the random 5x56array's mean and standard deviation
print("Required Check #A.3:\n", "Mean of Normalized 5X5 Array Integer:", np.mean(X_normalized)) # --> Prints the mean of the normalized array data set which is shown to be 0 in the notebook.
print("Required Check #A.4:\n", "Standard Deviation of Random 5X5 Array Integer:", np.std(X_normalized))  Prints the Standard Deviation of the normalized array data set, which is shown to be 0.999... or 1 in the notebook.
```

#  B.CUBES DIVISIBLE BY 4 PROBLEM
Instructions:
Using NumPy, create the first 100 positive integers, cube every element, and reshape the result into a 10 × 10 ndarray named C.
Thus, C begins with 13 and ends with 1003. Use a Boolean condition on C to obtain every cubed value divisible by 4. Store the selected values in
div by 4. Preserve NumPy’s normal row-major selection order. 

The following methods were used in this problem to create a unique function:

• `np.arange(X,Y,Z,)` = A built-in function in numpy that allows the user to create a dataset starting from X and the value before Y and Z is the difference 
between the datasets.

Example:
`C = np.arange(1,101,1)` --> Creates a dataset from 1 to 100 with a difference of 1 in each element.

• `.reshape()` = A built-in function in Numpy that allows us to arrange or rearrange the array dataset into another format as long as it has the same elements.

Example:
`C = C.reshape(5,5)` --> Arrange the array dataset into a 5x5 array.

• Boolean Indexing =  A built-in function in Numpy that allows taking elements or values from a dataset in specific conditions
Example:
`
S = np.arange(1,11,1) --> Makes a Dataset from 1 to 11
Above_6 = S[S>6] --> Assigns Above_6 with values from 7,8,9,10.
`
• `.size` -  A built-in function in Numpy that shows how many elements are there in the array,

Example:

`S = [1,2,3]
print(S.size) --> Prints out 3 as the size of the dataset
`

With the functions mentioned, the author can create a program for the problem using `np.arange()`. It creates the first 100 integers, cubes them, and stores them in a variable.
Using the `.reshape()` function, this allows the author to reorganize the variable with the first 100 integers that were cubed and organize it in 
a 10x10 array. Boolean indexing allows the author to create a new variable that stores the values divisible by 4, which solves the problem. Lastly, with the size, it allows the author to tell what the size of the array is that is divisible by 4.

```python
C = np.arange(1,101,1) #--> Makes a dataset for the first 100 integers.
C =  C**3 #--> Cubed the first 100 integers
C = C.reshape(10,10) #--> Re-organized the dataset into a 10x10 array.
div_by_4 = C[C % 4 == 0] #--> Collects the values from the 10x10 array that is divisible by 4.
print("Required Check #B.3:\n", "The Size of the array of Array C that is Divisible by 4:", div_by_4.size) #--> Prints out how many elements are divisible by 4.

```

Example:


#  C.ABOVE-MEAN SQUARES PROBLEM

Instructions:
Create a 6 × 6 ndarray named S containing the squares of the first 36 positive integers in increasing
row-major order. Compute the mean of all elements of S and store it in S mean. Then use Boolean
filtering to select only the elements strictly greater than S mean. Store these values in above mean

The following methods were used in this problem to create a unique function:

• `np.arange(X,Y,Z,)` = A built-in function in numpy that allows the user to create a dataset starting from X and the value before Y and Z is the difference 
between the datasets.

• `.reshape()` = A built-in function in Numpy that allows us to arrange or rearrange the array dataset into another format as long as it has the same elements.

• `np.mean()` = A built-in function in numpy that automatically takes the average or mean value from an list or an array without manually calculating the mean through hard code.

• Boolean Indexing =  A built-in function in Numpy that allows taking elements or values from a dataset under specific conditions

• `.size` -  A built-in function in Numpy that shows how many elements are there in the array,

With the functions mentioned, the author was able to create the program for the said problem. Using `np.arange`, it allowed the author to create the 
dataset of the first 36 positive integers, where he squared it immediately while also using the `.reshape()`to make it as an 6x6 array.
Next, the `np.mean()` allows us to create a value of the mean with the squared dataset S, and stored in S_mean, which is later used for the boolean indexing, where it was used to extract the elements in the S data dataset that are above the mean value from the S_mean and stored in a variable called above_mean.
Lastly, the `.size` function tells how many elements are in the above_mean variable.

```python
S = (np.arange(1,37,1)**2).reshape(6,6) #--> Creates the dataset by forming the first 36 positive integers and then squaring them immediately
reshaped it a 6x6 array.
S_mean = np.mean(S) #--> Takes the mean of the array S.
above_mean = S[S > S_mean] #--> Takes the values that are above the mean from the s_mean
above_mean.size #--> takes the size of the elements from the values that is above the mean
```
Thank you for Reading!

Version History
9/2/2026 - Uploaded Content
9/3/2026 - Replaced .mean() to np.mean()
