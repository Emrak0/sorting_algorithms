# C - Sorting Algorithms & Big O

This is a project on sorting algorithms implemented in C language, along with their corresponding time complexity (big O notation).

## Table of Contents
- [Sorting Algorithms](#sorting-algorithms)
- [Time Complexity](#time-complexity)
- [Files](#files)
- [Compilation](#compilation)
- [Example](#example)

## Sorting Algorithms
- Bubble sort
- insertion sort
- selection sort
- quick sort
- shell sort
- cocktail sort
- counting sort
- merge sort
- heap sort
- radix sort
- bitonic sort
- quick sort hoare

## Time Complexity

| Algorithm     | Best Case | Average Case | Worst Case |
|----------------|------------|---------------|------------|
| bubble sort    | O(n)       | O(n^2)        | O(n^2)     |
| insertion sort | O(n)       | O(n^2)        | O(n^2)     |
| selection sort | O(n^2)     | O(n^2)        | O(n^2)     |
| quick sort     | O(n log n) | O(n log n)    | O(n^2)     |
| shell sort     | O(n log^2n)| O(n log^2n)   | O(n log^2n)|
| cocktail sort  | O(n)       | O(n^2)        | O(n^2)     |
| counting sort  | O(k+n)     | O(k+n)        | Ok+n)     |
| merge sort     | O(n log n) | O(n log n)    | O(n log n) |
| heap sort      | O(n log n) | O(n log n)    | O(n log n) |
| radix sort     | O(nk)      | O(nk)         | O(nk)      |
| bitonic sort   | O(n log^2n)| O(n log^2n)   | O(n log^2n)|
| quick sort hoare| O(n log n) | O(n log n)    | O(n^2)     |

## Files
- `sort.h` : header file which contains all the function prototypes
- `0-bubble_sort.c`, `0-O` : a function that sorts an array of integers in ascending order using the bubble sort algorithm
- `1-insertion_sort_list.c`, `1-O` : a function that sorts a doubly linked list of integers in ascending order using the insertion sort algorithm
- `2-selection_sort.c`, `2-O` : a function that sorts an array of integers in ascending order using the selection sort algorithm
- `3-quick_sort.c`, `3-O` : a function that sorts an array of integers in ascending order using the quick sort algorithm
- `100-shell_sort.c` : a function that sorts an array of integers in ascending order using the shell sort algorithm, using the Knuth sequence
101-cocktail_sort_list.c`, `101-O` : a function that sorts a doubly linked list of integers in ascending order using the cocktail shaker sort algorithm
- `102-counting_sort.c`, `102-O` : a function that sorts an array of integers in ascending order using the counting sort algorithm
- `103-merge_sort.c`, `103-O` : a function that sorts an array of integers in ascending order using the merge sort algorithm
- `104-heap_sort.c`, `104-O` : a function that sorts an array of integers in ascending order using the heap sort algorithm
- `105-radix_sort.c`, `105-O` : a function that sorts an array of integers in ascending order using the radix sort algorithm
- `106-bitonic_sort.c`, `106-O` : a function that sorts an array of integers in ascending order using the bitonic sort algorithm
- `107-quick_sort_hoare.c`, `107-O` : a function that sorts an array of integers in ascending order using the quick sort hoare algorithm
- `deck.h` : header file for the card deck structure
- `deck` : a directory containing the card deck files
- `print_array.c` : a function that prints an array of integers
- `print_list.c` : a function that prints a doubly linked list of integers

## Compilation
All the files should be compiled with `gcc -Wall -Wextra -Werror -pedantic -std=c89`.

## Example

/tmp/sort$ cat 0-main.c 
#include <stdio.h>
#include <stdlib.h>
#include "sort.h"

/**
 * main - Entry point
 *
 * Return: Always 0
 */
int main(void)
{
    int array[] = {19, 48, 99, 71, 13, 52, 96, 73, 86, 7};
    size_t n = sizeof(array) / sizeof(array[0]);

    print_array(array, n);
    printf("\n");
    bubble_sort(array, n);
    printf("\n");
    print_array(array, n);
    return (0);
}
alex@/tmp/sort$ gcc -Wall -Wextra -Werror -pedantic  -std=gnu89 0-bubble_sort.c 0-main.c print_array.c -o bubble
alex@/tmp/sort$ ./bubble
19, 48, 99, 71, 13, 52, 96, 73, 86, 7

19, 48, 71, 99, 13, 52, 96, 73, 86, 7
19, 48, 71, 13, 99, 52, 96, 73, 86, 7
19, 48, 71, 13, 52, 99, 96, 73, 86, 7
19, 48, 71, 13, 52, 96, 99, 73, 86, 7
19, 48, 71, 13, 52, 96, 73, 99, 86, 7
19, 48, 71, 13, 52, 96, 73, 86, 99, 7
19, 48, 71, 13, 52, 96, 73, 86, 7, 99
19, 48, 13, 71, 52, 96, 73, 86, 7, 99
19, 48, 13, 52, 71, 96, 73, 86, 7, 99
19, 48, 13, 52, 71, 73, 96, 86, 7, 99
19, 48, 13, 52, 71, 73, 86, 96, 7, 99
19, 48, 13, 52, 71, 73, 86, 7, 96, 99
19, 13, 48, 52, 71, 73, 86, 7, 96, 99
19, 13, 48, 52, 71, 73, 7, 86, 96, 99
13, 19, 48, 52, 71, 73, 7, 86, 96, 99
13, 19, 48, 52, 71, 7, 73, 86, 96, 99
13, 19, 48, 52, 7, 71, 73, 86, 96, 99
13, 19, 48, 7, 52, 71, 73, 86, 96, 99
13, 19, 7, 48, 52, 71, 73, 86, 96, 99
13, 7, 19, 48, 52, 71, 73, 86, 96, 99
7, 13, 19, 48, 52, 71, 73, 86, 96, 99

7, 13, 19, 48, 52, 71, 73, 86, 96, 99
alex@/tmp/sort$ 
