# Merge Sort Trace

Input: `324, 125, 456, 218, 102, 389, 275, 147`


| Merge-pass level (run size) | Merge operation | Left sorted run | Right sorted run | Resulting sorted run | Key comparisons |

| 1 (1 element) | 1 | `[324]` | `[125]` | `[125, 324]` | 1 |
| 1 (1 element) | 2 | `[456]` | `[218]` | `[218, 456]` | 1 |
| 1 (1 element) | 3 | `[102]` | `[389]` | `[102, 389]` | 1 |
| 1 (1 element) | 4 | `[275]` | `[147]` | `[147, 275]` | 1 |
| 2 (2 elements) | 5 | `[125, 324]` | `[218, 456]` | `[125, 218, 324, 456]` | 3 |
| 2 (2 elements) | 6 | `[102, 389]` | `[147, 275]` | `[102, 147, 275, 389]` | 3 |
| 3 (4 elements) | 7 | `[125, 218, 324, 456]` | `[102, 147, 275, 389]` | `[102, 125, 147, 218, 275, 324, 389, 456]` | 7 |

## State after each merge-pass level

| Stage | Ordered runs after the stage |

| Initial | `[324] [125] [456] [218] [102] [389] [275] [147]` |
| Pass 1 — merge runs of size 1 | `[125, 324] [218, 456] [102, 389] [147, 275]` |
| Pass 2 — merge runs of size 2 | `[125, 218, 324, 456] [102, 147, 275, 389]` |
| Pass 3 — merge runs of size 4 | `[102, 125, 147, 218, 275, 324, 389, 456]` |

There are 3 merge-pass levels, 7 merge calls, and 17 key comparisons. Each of the 8 values is written back to the main array once per level, giving 24 main-array writes.
