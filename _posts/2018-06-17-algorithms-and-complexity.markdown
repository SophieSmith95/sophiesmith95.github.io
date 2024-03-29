---
layout: post
title:  "Algorithms and Complexity"
date:   2018-06-17 15:45:57 +0100
---

After learning about algorithms and complexity in 3rd year of univesity here is my basic overview of a numeber of algorithms and their complexities.

## Insertion Sort

Insertion sort uses 2 different arrays, an unsorted array and a sorted array. Each iteration of the algorithm involves taking an element from the unsorted array and placing it into the correct location in the sorted array.

The first iteration takes the first element of the input data (unsorted array) and places it into a new array (sorted array). The second iteration will take the next element from the unsorted array and will put it into the correct location in the sorted array. The correct location is determined by comparing the element from the unsorted array against the last element in the sorted array. If the 2 elements are out of order they will be swapped around the next pair will be compared and swapped if out of place. This will continue until the element from the unsorted array is in the correct location in the sorted array. The iterations will continue until the unsorted list is empty.

Worse case complexity of this algorithm is \\(O(n^2)\\). This occurs when the array is reverse sorted. The best case complexity is \\(O(n^2)\\)and this occurs when the list is already sorted.

## Selection Sort

Selection sort will begin by going over the array and finding the smallest value in the array. Once the smallest value is found, the element will be swapped from its current position to the first position in the array. Next the second smallest element will be found and once found moved to the 2nd position in the array. This continues until the array is sorted.

The best and worst case complexity of this algorithm is \\(O(n^2)\\).

## Bubble Sort

Bubble sort compares each adjacent elements during each iteration and will swap the elements if out of order. Iterations over the array will continue until there are no more adjacent elements that need swapping. To make this algorithm more efficient it can be designed so that each iteration iterates over \\(n-1\\) elements. This is because after the first iteration the largest number should be in the last position of the array, after the second iteration the last 2 elements should be sorted and therefore no comparison needed etc.

This algorithm has a worst case complexity of \\(O(n^2)\\) which occurs when the array is reverse sorted. The best case complexity is \\(O(n^2)\\) which is when the array is sorted.


## Merge Sort

Merge sort sorts the input data into n sub lists, each containing just one element. Each sub lists is then repeatedly merged to produce and new sorted sublist until all of the sub lists have been merged to create one final sorted list.

The worst case complexity for this algorithm is \\(O(n\log{}n)\\)

## Quick Sort

Quick sort is a divide and conquer algorithm. Pick an element from the input data. This is called the pivot. Split the input data into 2 arrays comprised of elements larger and smaller than the pivot. Recursively apply these steps to the subarrays until you are left with n number of sorted arrays which can then be combined into one sorted array.

Worst case complexity is \\(O(n^2)\\). This occurs when the pivot is either the smallest or largest element in the array. The best case complexity is \\(O(n\log{}n)\\) and this occurs when the pivot divides the array into almost equal sized arrays.

## Binary Search

Binary search is used on sorted arrays to find out if a given element exists in the array. Binary sort does this by taking the middle element of the array and comparing to see if this element it greater than or smaller than the element we are trying to find in the array. If the middle element is greater than then we can eliminate the left hand side of the array and the right hand side if smaller than.

Worst case complexity is \\(O(n)\\) and the best case is \\(O(log_{2}n)\\).

## Computing Complexity

The following is a naive way of computing the complexity of an alogrith which can be used to give a best guess of an alogrithms complexity.

### \\(O(n)\\)

This is liner time and tends to occur when there is a loop which is executed N times e.g.

```
for (int i=0; i<n; i++):
	Do something
```

### \\(O(n^2)\\)

This is quadratic time and tends to occur when there are nested loops where the outer loop executes N times and the inner loop executes N times, so \\(N\*N) = O(n^2)\\) e.g.

```
for (int i=0; i<n; i++):
	for (int j=0; j<n; j++):
		Do Something
```

### \\(O(\log{}n)\\)

This is logarithmic time and tends to occur when the counting variable in a loop doubles e.g.

```
for (int i=0; i<n; i\*=2):
	Do Something
```

This also applies to something that is constantly being halved

### \\(O(n\log{}n)\\)

This is linerithmic time and combines \\(O(n)\\) and \\(O(\log{}n)\\) e.g.

```
for (int i=0; i<n; i++): #<-- O(n)
	for (int j=0; j<n; j++): #<-- O(logn)
		Do Something
```
<script src='https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.7.5/latest.js?config=TeX-MML-AM_CHTML' async></script>