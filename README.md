# Fibonacci Search Algorithm

## Description
This C++ program implements the **Fibonacci Search algorithm** to find the position of a target element in a sorted array. It uses Fibonacci numbers to divide the array into sections, providing a comparison-efficient alternative to binary search in certain cases.

## Files
- `fibonacci_search.cpp` – main source file containing  
  - `min` – utility function to find the minimum of two integers  
  - `fibSearch` – performs the Fibonacci search  
  - `main` – reads input array and target, invokes search, prints result  

## Requirements
- C++11 (or later) compiler  

## Compilation
```bash
g++ -std=c++11 -O2 -o fibonacci_search fibonacci_search.cpp
```

## Usage
```bash
./fibonacci_search
```

### Input
- First line: integer *n* – the number of elements in the array  
- Next *n* integers – the sorted array elements  
- (In the code provided, the target to search is hardcoded as `7`)  

### Output
- Integer index of the element `7` in the array (or `-1` if not found)  

## Example
```
5
1 3 5 7 9
```
produces
```
3
```

## Algorithm Details
- **Initialize**: Generate the smallest Fibonacci number greater than or equal to the size of the array  
- **Loop**:  
  - Use Fibonacci offsets to divide the array  
  - Compare target with value at the current index  
  - Update Fibonacci variables and offset based on comparison  
- **Final Check**: If one element remains, compare it directly  
## Running Time
-Best Case: O(1) – if the target is found in the first comparison
-Average and Worst Case: O(log n) – similar to Binary Search
-The number of comparisons is determined by the Fibonacci series rather than powers of 2

## Memory Management
- Dynamic memory is allocated for the input array using `new[]`  
- Memory is properly deallocated at the end using `delete[]`
