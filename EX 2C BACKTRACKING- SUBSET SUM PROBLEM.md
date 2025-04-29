# EX 2C BACKTRACKING- SUBSET SUM PROBLEM
## DATE:

## AIM:
To demonstrate that the sum of the subset of a given set is equal to the given sum.


## Algorithm
1. Take an integer input `n` representing the number of elements in the list.  
2. Read `n` integers from the user and store them in the list `arr`.  
3. Take an integer input `x` which is the target sum.  
4. Define a function `subsetSum` that takes `n`, `arr`, and `x` as parameters.  
5. In the function, iterate `i` from 0 to `n` to generate all possible subset sizes.  
6. For each size `i`, generate all combinations of `arr` of length `i` using `combinations(arr, i)`.  
7. For each subset generated, check if the sum of its elements is equal to `x`.  
8. If the sum matches `x`, print the subset as a list.  
9. Call the `subsetSum` function with the input values to find and display all matching subsets.

## Program:
```
/*
Program to implement Subset sum problem.
Developed by: harithashree
Register Number: 212222230046
from itertools import combinations
def subsetSum(n,arr,x):
    for i in range(n+1):
        for subset in combinations(arr,i):
            if sum(subset)==x:
                print(list(subset))
n =int(input())
arr=[]
for i in range(0,n):
    a=int(input())
    arr.append(a)
x=int(input())
subsetSum(n,arr,x)
*/
```

## Output:

![Screenshot 2025-04-29 140638](https://github.com/user-attachments/assets/34c0a3a1-e86c-4858-9dee-b78e1e78c313)



## Result:
The Subset Sum program executed successfully, and the result was determined based on whether a subset matching the target sum was found or not.
