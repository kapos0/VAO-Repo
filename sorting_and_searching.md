# Sorting and Searching (Cheat Sheet)

## Contents
- Searching algorithms
  - Linear search
  - Binary search
- Sorting algorithms
  - Bubble sort
  - Selection sort
  - Insertion sort
  - Merge sort
  - Quick sort
- Time and space complexities (comparison table)
- Tips and best practices
- Example C code (copyable)

---

## Searching algorithms

### Linear search
- Description: Checks each element in the array from start to end.
- Use when: Array is unsorted or very small.
- Time: O(n) average and worst-case.
- Space: O(1).

```c
#include <stdbool.h>

bool linear_search(int value, int array[], int n)
{
    for (int i = 0; i < n; i++)
        if (array[i] == value) return true;
    return false;
}
```

### Binary search
- Description: Repeatedly compares target with middle element and halves the search range.
- Precondition: Array must be sorted.
- Time: O(log n).
- Space: O(1) iterative, O(log n) recursive (call stack).

```c
#include <stdbool.h>

bool binary_search(int value, int array[], int n)
{
    int low = 0, high = n - 1;
    while (low <= high)
    {
        int mid = low + (high - low) / 2;
        if (array[mid] == value) return true;
        else if (array[mid] < value) low = mid + 1;
        else high = mid - 1;
    }
    return false;
}
```

---

## Sorting algorithms

### Bubble sort
- Description: Repeatedly swaps adjacent elements if out of order; larger elements "bubble" to the end each pass.
- Time: O(n^2) average and worst, O(n) best (with optimization).
- Space: O(1).

```c
void bubble_sort(int array[], int n)
{
    bool swapped;
    for (int i = 0; i < n - 1; i++)
    {
        swapped = false;
        for (int j = 0; j < n - 1 - i; j++)
            if (array[j] > array[j + 1])
            {
                int tmp = array[j];
                array[j] = array[j + 1];
                array[j + 1] = tmp;
                swapped = true;
            }
        if (!swapped) break;
    }
}
```

### Selection sort
- Description: Selects the smallest (or largest) element from the unsorted portion and swaps it into place.
- Time: O(n^2) all cases.
- Space: O(1).

```c
void selection_sort(int array[], int n)
{
    for (int i = 0; i < n - 1; i++)
    {
        int min_idx = i;
        for (int j = i + 1; j < n; j++)
            if (array[j] < array[min_idx]) min_idx = j;
        int tmp = array[i];
        array[i] = array[min_idx];
        array[min_idx] = tmp;
    }
}
```

### Insertion sort
- Description: Builds a sorted left portion by inserting each new element into its correct position.
- Time: O(n^2) worst, O(n) best (nearly sorted data).
- Space: O(1).

```c
void insertion_sort(int array[], int n)
{
    for (int i = 1; i < n; i++)
    {
        int key = array[i];
        int j = i - 1;
        while (j >= 0 && array[j] > key)
        {
            array[j + 1] = array[j];
            j--;
        }
        array[j + 1] = key;
    }
}
```

### Merge sort
- Description: Divide-and-conquer: split array, sort halves, merge.
- Time: O(n log n) all cases.
- Space: O(n) auxiliary.
- Stable sort.

```c
#include <stdlib.h>

void merge(int a[], int l, int m, int r, int temp[])
{
    int i = l, j = m + 1, k = l;
    while (i <= m && j <= r)
        temp[k++] = (a[i] <= a[j]) ? a[i++] : a[j++];
    while (i <= m) temp[k++] = a[i++];
    while (j <= r) temp[k++] = a[j++];
    for (int x = l; x <= r; x++) a[x] = temp[x];
}

void merge_sort_recursive(int a[], int l, int r, int temp[])
{
    if (l >= r) return;
    int m = l + (r - l) / 2;
    merge_sort_recursive(a, l, m, temp);
    merge_sort_recursive(a, m + 1, r, temp);
    merge(a, l, m, r, temp);
}

void merge_sort(int a[], int n)
{
    int *temp = malloc(n * sizeof(int));
    if (!temp) return; // allocation failure handling simplified
    merge_sort_recursive(a, 0, n - 1, temp);
    free(temp);
}
```

### Quick sort
- Description: Choose a pivot, partition elements around pivot, recursively sort partitions.
- Time: O(n log n) average, O(n^2) worst (poor pivot).
- Space: O(log n) average for recursion.
- Tips: Randomize pivot or use median-of-three to avoid worst-case.

```c
int partition(int a[], int low, int high)
{
    int pivot = a[high];
    int i = low - 1;
    for (int j = low; j <= high - 1; j++)
        if (a[j] < pivot)
        {
            i++;
            int tmp = a[i]; a[i] = a[j]; a[j] = tmp;
        }
    int tmp = a[i + 1]; a[i + 1] = a[high]; a[high] = tmp;
    return i + 1;
}

void quick_sort(int a[], int low, int high)
{
    if (low < high)
    {
        int pi = partition(a, low, high);
        quick_sort(a, low, pi - 1);
        quick_sort(a, pi + 1, high);
    }
}
```

---

## Time and space complexities

| Algorithm       | Average time | Worst time  | Space       |
|----------------|-------------:|------------:|------------:|
| Linear search  | O(n)         | O(n)        | O(1)        |
| Binary search  | O(log n)     | O(log n)    | O(1)        |
| Bubble sort    | O(n^2)       | O(n^2)      | O(1)        |
| Selection sort | O(n^2)       | O(n^2)      | O(1)        |
| Insertion sort | O(n^2)       | O(n^2)      | O(1)        |
| Merge sort     | O(n log n)   | O(n log n)  | O(n)        |
| Quick sort     | O(n log n)   | O(n^2)      | O(log n)    |

---

## Tips and best practices
- For very small arrays or nearly sorted data, use insertion sort.
- For large arrays, use merge sort or a well-implemented quick sort.
- If stability matters, prefer merge sort.
- If memory is constrained, prefer in-place sorts (quick sort, insertion, selection).
- If you need to perform many searches, sort once and use binary search for subsequent queries.

---

## Example usage (main)
```c
#include <stdio.h>

int main(void)
{
    int a[] = {5, 2, 9, 1, 5, 6};
    int n = sizeof(a) / sizeof(a[0]);

    // sort example
    merge_sort(a, n);

    // print
    for (int i = 0; i < n; i++) printf("%d ", a[i]);
    printf("\n");

    // search example
    if (binary_search(5, a, n)) printf("Found\n");
    else printf("Not found\n");

    return 0;
}
```

---
