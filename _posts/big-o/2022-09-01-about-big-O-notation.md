---
title:  What is Big-O Notation?
author: Dachan Kyong
date: 2022-09-01 00:00:00 +0900
categories: [Big-O Notation, Definition]
tags: [big-o]
render_with_liquid: false
---

## **About Big-O Notation**
`Big-O notation`, often written as "`O(f(n))`," is a mathematical notation used in computer science and mathematics to describe the upper bound or worst-case behavior of an algorithm's runtime or space complexity. It provides a way to characterize how the performance of an algorithm changes as the size of the input data increases.

In simple terms, "`Big-O notation`" helps us understand the efficiency of an algorithm by focusing on how it scales with larger inputs. It allows us to make comparisons between different algorithms and choose the most suitable one for a given problem.

The `O(f(n))`'s "`O`" stands for "order of magnitude", and it represents an approximation of how the runtime or space usage of an algorithm changes relative to the input size. The function "`f(n)`" inside the parentheses represents the upper limit of the growth rate as the input size "`n`" becomes very large.


Here's what we need to know about Big O notation:


## **Types of Complexity**
Different notations indicate different complexities:


### O(1) : Constant time complexity
The algorithm's runtime or space usage remains constant regardless of the input size. It takes the same amount of time or space to execute, regardless of how large the input is.

### O(n): Linear time complexity
The algorithm's performance grows linearly with the input size. As the input size doubles, the runtime or space usage also doubles.

### O(n^2), O(n^3), ... : Polynomial time complexity
The algorithm's performance grows polynomially with the input size. As the input size increases, the runtime or space usage increases significantly.

### O(2^n), O(3^n), ... : Exponential time complexity
The algorithm's performance grows exponentially as the input size increases. These algorithms can become very slow for even moderately large input sizes.

### O(log n) : Logarithmic time complexity
The algorithm's performance grows logarithmically as the input size increases. Common in algorithms that divide the input into smaller parts in each step, like binary search in a sorted array.

### O(n log n) : Linearithmic time complexity.
The algorithm's performance grows linearithmically, which is faster than quadratic but slower than linear. Common in efficient sorting algorithms like mergesort and heapsort.

### O(n!) : Factorial time complexity
The algorithm's performance grows factorially with the input size. This is very inefficient and becomes impractical even for small input sizes.


---
In the following posts, I will provide explanations and examples for each type of complexity.

