# Complexity Analysis

## Merge Sort

Merge Sort divides the array into halves until single-element runs remain, then merges those runs.

| Case | Time complexity | Reason |

| Best | O(n log n) | All levels of splitting and merging are still performed. |
| Average | O(n log n) | There are log n merge levels, each processing n elements. |
| Worst | O(n log n) | The same number of levels and linear merging work occur regardless of input order. |

- Extra space: O(n) for the temporary merge arrays.
- Stability: Stable. Equal keys retain their relative order because the merge uses `<=` to take the left value first.
- In-place: No, in this implementation.
- Given input: 3 merge-pass levels, 7 merge calls, 17 key comparisons, and 24 writes to the main array during merging.

## Quick Sort

Quick Sort chooses a pivot, partitions the current subarray, and recursively sorts the two resulting subarrays. This implementation uses the last element as its pivot.

| Case | Time complexity | Reason |

| Best | O(n log n) | Each pivot divides the subarray into nearly equal parts. |
| Average | O(n log n) | Partitions are reasonably balanced on average. |
| Worst | O(n²) | Repeatedly choosing an extreme pivot creates subarrays of sizes 0 and n − 1. |

- Extra space: O(log n) average recursion-stack space; **O(n)** in the worst case.
- Stability: Not stable in general.
- In-place: Yes with respect to the array (apart from recursive call-stack space).
- Given input: 5 partitions, 16 key comparisons, 12 swap calls (6 non-self exchanges).

## Counting convention

A key comparison means one comparison between an array key and another key: `left_part[i] <= right_part[j]` in Merge Sort and `a[j] <= pivot` in Quick Sort. Loop-condition checks, index checks, and copying to temporary arrays are not included in the comparison total. This makes the displayed counts reproducible from the source code.
