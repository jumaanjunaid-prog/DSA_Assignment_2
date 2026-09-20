# Quick Sort Trace

Input: `324, 125, 456, 218, 102, 389, 275, 147`


| Partition | Current index range | Pivot | Array immediately after partition | Pivot final index | Key comparisons | Swap calls |

| 1 | 0–7 | 147 | `[125, 102, 147, 218, 324, 389, 275, 456]` | 2 | 7 | 3 |
| 2 | 0–1 | 102 | `[102, 125, 147, 218, 324, 389, 275, 456]` | 0 | 1 | 1 |
| 3 | 3–7 | 456 | `[102, 125, 147, 218, 324, 389, 275, 456]` | 7 | 4 | 5 |
| 4 | 3–6 | 275 | `[102, 125, 147, 218, 275, 389, 324, 456]` | 4 | 3 | 2 |
| 5 | 5–6 | 324 | `[102, 125, 147, 218, 275, 324, 389, 456]` | 5 | 1 | 1 |

Final sorted array: `102, 125, 147, 218, 275, 324, 389, 456`

The execution performs 5 partitions and 16 key comparisons. It makes 12 calls to swap, of which 6 exchange different positions and 6 are harmless self-swaps.
