# ECE-2112-PA-1

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



#  B.CUBES DIVISIBLE BY 4 PROBLEM
Instructions:
Using NumPy, create the first 100 positive integers, cube every element, and reshape the result into a 10 × 10 ndarray named C.
Thus, C begins with 13 and ends with 1003. Use a Boolean condition on C to obtain every cubed value divisible by 4. Store the selected values in
div by 4. Preserve NumPy’s normal row-major selection order. 


#  C.ABOVE-MEAN SQUARES PROBLEM

Instructions:
Create a 6 × 6 ndarray named S containing the squares of the first 36 positive integers in increasing
row-major order. Compute the mean of all elements of S and store it in S mean. Then use Boolean
filtering to select only the elements strictly greater than S mean. Store these values in above mean
