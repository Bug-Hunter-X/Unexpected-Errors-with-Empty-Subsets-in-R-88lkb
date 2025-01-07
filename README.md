# Unexpected Errors with Empty Subsets in R

This repository demonstrates a common yet subtle error in R programming related to subsetting data frames. The error arises when a subsetting condition does not return any TRUE values, leading to an empty subset. Subsequent operations on this empty subset may result in unexpected errors or warnings, causing unexpected behaviour in the code, especially when inside loops.

The `bug.R` file contains the problematic code. The `bugSolution.R` file provides a solution to prevent this error.

## Problem
Subsetting operations that fail to return any matching rows can result in an empty data frame.  Using functions such as `mean()` on an empty data frame, can result in errors.  This problem often goes unnoticed, especially in loops, where the condition may not be true for all iterations. 