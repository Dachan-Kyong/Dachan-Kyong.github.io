---
title:  "O(n^2), O(n^3), ...: Polynomial time complexity"

author: Dachan Kyong
date: 2022-09-02 02:00:00 +0900
categories: [Big-O Notation, "O(n^2), O(n^3), ..."]
tags: [big-o, java]
render_with_liquid: false
math: true
---

## **About Big-O Notation**
[What is Big-O Notation?](https://dachan-kyong.github.io/posts/about-big-O-notation/)


## **What is $$O(n^2)$$, $$O(n^3)$$, ...?**
The algorithm's performance grows polynomially with the input size. As the input size increases, the runtime or space usage increases significantly.



## **$$O(n^2)$$ Examples & Explanations: Java**

### Nested Loop
```java
int n = 5;
for (int i = 0; i < n; i++) {
    for (int j = 0; j < n; j++) {
        System.out.print("* ");  // Printing a square pattern
    }
    System.out.println();
}
```
Explanation: Printing a square pattern using nested loops has a time complexity of $$O(n^2)$$ because it involves two nested loops, each running `n` times.

### Selection Sort
```java
void selectionSort(int[] arr) {
    int n = arr.length;
    for (int i = 0; i < n - 1; i++) {
        for (int j = i + 1; j < n; j++) {
            if (arr[j] < arr[i]) {
                int temp = arr[i];
                arr[i] = arr[j];
                arr[j] = temp;
            }
        }
    }
}
```
Explanation: The selection sort algorithm involves nested loops and has a time complexity of $$O(n^2)$$ due to the two nested iterations.

## **O($$n^3$$) Examples & Explanations: Java**

### Triple Nested Loop
```java
int n = 3;
for (int i = 0; i < n; i++) {
    for (int j = 0; j < n; j++) {
        for (int k = 0; k < n; k++) {
            System.out.print("* ");  // Printing a cube pattern
        }
        System.out.println();
    }
    System.out.println();
}
```
Explanation: Printing a cube pattern using triple nested loops has a time complexity of $$O(n^3)$$ due to the three nested iterations.

### Matrix Multiplication
```java
int[][] matrix1 = {{1, 2}, {3, 4}};
int[][] matrix2 = {{5, 6}, {7, 8}};
int n = 2;

int[][] result = new int[n][n];
for (int i = 0; i < n; i++) {
    for (int j = 0; j < n; j++) {
        for (int k = 0; k < n; k++) {
            result[i][j] += matrix1[i][k] * matrix2[k][j];
        }
    }
}
```
Explanation: Matrix multiplication using nested loops has a time complexity of $$O(n^3)$$ due to the three nested iterations.

---
---
---
---
These examples demonstrate algorithms with polynomial time complexities, where the number of operations grows with the square or cube of the input size.

---
In the following posts, I will provide more examples and explanations for each type of complexity.

