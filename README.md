# DSA Sorting Assignment — Merge Sort and Quick Sort

This repository contains a complete C-language comparison of Merge Sort and Quick Sort using the assigned input:

324, 125, 456, 218, 102, 389, 275, 147


Both programs produce:

102, 125, 147, 218, 275, 324, 389, 456


## Run the programs

From the repository root, compile and run with a C compiler such as GCC:

gcc -std=c11 -Wall -Wextra -pedantic src/merge_sort.c -o merge_sort
./merge_sort

gcc -std=c11 -Wall -Wextra -pedantic src/quick_sort.c -o quick_sort
./quick_sort


On Windows, run the generated executables as `merge_sort.exe` and `quick_sort.exe`.


## Results for the assigned input

| Algorithm | Sorted output | Key comparisons | Recorded additional operations |

| Merge Sort | `102, 125, 147, 218, 275, 324, 389, 456` | 17 | 24 writes to the main array while merging |
| Quick Sort | `102, 125, 147, 218, 275, 324, 389, 456` | 16 | 12 swap calls, including 6 non-self exchanges |


## Documentation

- [Merge Sort trace](trace/merge_sort_trace.md)
- [Quick Sort trace](trace/quick_sort_trace.md)
- [Complexity analysis](analysis/complexity_analysis.md)
- [Comparison table](analysis/comparison_table.md)
- [Conclusion for large fixed-length keys](conclusion/conclusion.md)
