# 🔄 Push_swap

![42 Badge](https://img.shields.io/badge/42-Project-blue)
![C Badge](https://img.shields.io/badge/Language-C-lightgrey)
![Algorithm Badge](https://img.shields.io/badge/Algorithm-Sorting-orange)

## 📋 Overview

Push_swap is an algorithm project from 42 School that challenges students to sort data using two stacks with a limited set of operations. The goal is to write a C program that calculates and displays the smallest sequence of operations needed to sort a given list of integers.

## 🎯 Objectives

- Implement an efficient sorting algorithm
- Understand algorithmic complexity
- Master stack manipulation
- Write clean, optimized C code
- Achieve sorting with minimal operations

## 🧠 Concept

The project works with two stacks (a and b) and a set of specific operations:

- `sa`: Swap the first 2 elements of stack a
- `sb`: Swap the first 2 elements of stack b
- `ss`: `sa` and `sb` simultaneously
- `pa`: Push the top element from stack b to stack a
- `pb`: Push the top element from stack a to stack b
- `ra`: Rotate stack a (first element becomes last)
- `rb`: Rotate stack b (first element becomes last)
- `rr`: `ra` and `rb` simultaneously
- `rra`: Reverse rotate stack a (last element becomes first)
- `rrb`: Reverse rotate stack b (last element becomes first)
- `rrr`: `rra` and `rrb` simultaneously

## 💻 Implementation

My push_swap implementation features:

- **Custom Algorithm for Small Sets**: Optimized sorting strategies for handling 2-5 numbers with the minimum possible operations
- **Radix Sort for Large Sets**: Implementation of a base-10 radix sort algorithm for efficiently sorting larger datasets
- **Error Handling**: Comprehensive input validation (duplicates, non-integers, overflow)
- **Memory Management**: Careful allocation and freeing to prevent memory leaks

## 🛠️ Technical Details

### Algorithm Selection

- **For 2-5 Numbers**: Custom hardcoded algorithms to achieve optimal operation count
- **For 6+ Numbers**: Radix sort implementation that performs well with large datasets

### Performance Benchmarks

- **100 Random Numbers**: Consistently sorts with fewer than 700 operations
- **500 Random Numbers**: Consistently sorts with fewer than 5500 operations

## 📊 Performance Analysis

The Radix Sort implementation offers:
- Time Complexity: O(d * n) where d is the number of digits and n is the number of integers
- Space Complexity: O(n)

This approach is particularly effective for this project as:
1. It has a predictable performance pattern
2. It adapts well to the available stack operations
3. It achieves the operation count requirements for both 100 and 500 number tests

## 🚀 Usage

### Compilation

```bash
make
```

### Running the Program

```bash
./push_swap [list of integers]
```

Example:
```bash
./push_swap 42 1 99 -5 32
```

### Output

The program will display the list of operations needed to sort the given integers:

```
pb
ra
pb
ra
sa
pa
pa
```

## 📌 Important Notes

- The integers must be unique
- The program handles errors (non-integers, duplicates, overflow) by displaying "Error"
- The goal is to use the minimum number of operations possible

## 🧪 Testing

You can verify the sorting operations using the checker program:

```bash
ARG="4 67 3 87 23"; ./push_swap $ARG | ./checker_OS $ARG
```

If the sorting is successful, it will display "OK".

## 📚 Skills Developed

- Algorithm design and implementation
- Optimization techniques
- Data structure manipulation
- Problem-solving
- C programming best practices

## 📝 License

This project is part of the 42 School curriculum and is licensed for educational purposes.
