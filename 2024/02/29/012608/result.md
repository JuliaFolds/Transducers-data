# Multi-thread benchmark result

* Pull request commit: [`08224301df212945194fa70e253a115ab476591b`](https://github.com/JuliaFolds/Transducers.jl/commit/08224301df212945194fa70e253a115ab476591b)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/243> (Update */Manifest.toml)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 29 Feb 2024 - 01:20
    - Baseline: 29 Feb 2024 - 01:25
* Package commits:
    - Target: 7aea50
    - Baseline: 2a51f8
* Julia commits:
    - Target: 742b9a
    - Baseline: 742b9a
* Julia command flags:
    - Target: None
    - Baseline: None
* Environment variables:
    - Target: `JULIA_NUM_THREADS => 2`
    - Baseline: `JULIA_NUM_THREADS => 2`

## Results
A ratio greater than `1.0` denotes a possible regression (marked with :x:), while a ratio less
than `1.0` denotes a possible improvement (marked with :white_check_mark:). Only significant results - results
that indicate possible regressions or improvements - are shown below (thus, an empty table means that all
benchmark results remained invariant between builds).

| ID                                                  | time ratio                   | memory ratio                 |
|-----------------------------------------------------|------------------------------|------------------------------|
| `["collect", "unordered", "basesize=1"]`            | 0.77 (5%) :white_check_mark: |                   1.01 (1%)  |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 0.76 (5%) :white_check_mark: | 0.75 (1%) :white_check_mark: |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  |                   0.99 (5%)  | 0.98 (1%) :white_check_mark: |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |                1.13 (5%) :x: |                1.07 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |                1.51 (5%) :x: |                1.25 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |                1.15 (5%) :x: |                1.12 (1%) :x: |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |                   0.97 (5%)  | 0.87 (1%) :white_check_mark: |
| `["parallel_histogram", "comm", "basesize=16384"]`  | 0.91 (5%) :white_check_mark: | 0.97 (1%) :white_check_mark: |
| `["parallel_histogram", "comm", "basesize=4096"]`   |                1.08 (5%) :x: |                1.03 (1%) :x: |
| `["splitby", "count", "reduce"]`                    | 0.89 (5%) :white_check_mark: |                1.08 (1%) :x: |
| `["words", "nthreads=4"]`                           |                   1.01 (5%)  |                1.01 (1%) :x: |

## Benchmark Group List
Here's a list of all the benchmark groups executed by this job:

- `["collect", "assoc"]`
- `["collect"]`
- `["collect", "unordered"]`
- `["findfirst", "n=1000"]`
- `["findfirst", "n=1000", "reduce"]`
- `["findfirst", "n=400"]`
- `["findfirst", "n=400", "reduce"]`
- `["findfirst", "n=500"]`
- `["findfirst", "n=500", "reduce"]`
- `["overhead"]`
- `["parallel_histogram", "assoc"]`
- `["parallel_histogram", "comm"]`
- `["parallel_histogram"]`
- `["partition_length_maximum", "rand"]`
- `["splitby", "count"]`
- `["sum", "random"]`
- `["sum", "random", "reduce"]`
- `["sum", "uniform"]`
- `["sum", "uniform", "reduce"]`
- `["sum", "valley"]`
- `["sum", "valley", "reduce"]`
- `["words"]`

## Julia versioninfo

### Target
```
Julia Version 1.7.3
Commit 742b9abb4d (2022-05-06 12:58 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 22.04.4 LTS
  uname: Linux 6.5.0-1015-azure #15~22.04.1-Ubuntu SMP Tue Feb 13 01:15:12 UTC 2024 x86_64 x86_64
  CPU: AMD EPYC 7763 64-Core Processor: 
              speed         user         nice          sys         idle          irq
       #1  3246 MHz       2075 s          0 s        159 s       5614 s          0 s
       #2  3242 MHz       2589 s          0 s        161 s       5102 s          0 s
       #3  3209 MHz       3026 s          0 s        172 s       4660 s          0 s
       #4  2555 MHz       2326 s          0 s        173 s       5348 s          0 s
       
  Memory: 15.606491088867188 GB (12444.515625 MB free)
  Uptime: 789.22 sec
  Load Avg:  1.77  1.53  0.9
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, znver3)
```

### Baseline
```
Julia Version 1.7.3
Commit 742b9abb4d (2022-05-06 12:58 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 22.04.4 LTS
  uname: Linux 6.5.0-1015-azure #15~22.04.1-Ubuntu SMP Tue Feb 13 01:15:12 UTC 2024 x86_64 x86_64
  CPU: AMD EPYC 7763 64-Core Processor: 
              speed         user         nice          sys         idle          irq
       #1  2445 MHz       3176 s          0 s        238 s       7397 s          0 s
       #2  2445 MHz       3696 s          0 s        231 s       6886 s          0 s
       #3  3209 MHz       4310 s          0 s        249 s       6263 s          0 s
       #4  3243 MHz       3434 s          0 s        240 s       7136 s          0 s
       
  Memory: 15.606491088867188 GB (12332.75390625 MB free)
  Uptime: 1086.16 sec
  Load Avg:  1.76  1.69  1.15
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, znver3)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 29 Feb 2024 - 1:20
* Package commit: 7aea50
* Julia commit: 742b9a
* Julia command flags: None
* Environment variables: `JULIA_NUM_THREADS => 2`

## Results
Below is a table of this job's results, obtained by running the benchmarks.
The values listed in the `ID` column have the structure `[parent_group, child_group, ..., key]`, and can be used to
index into the BaseBenchmarks suite to retrieve the corresponding benchmarks.
The percentages accompanying time and memory values in the below table are noise tolerances. The "true"
time/memory value for a given benchmark is expected to fall within this percentage of the reported value.
An empty cell means that the value was zero.

| ID                                                  | time            | GC time | memory          | allocations |
|-----------------------------------------------------|----------------:|--------:|----------------:|------------:|
| `["collect", "assoc", "basesize=1"]`                | 148.594 ms (5%) |         |   4.36 MiB (1%) |       32800 |
| `["collect", "assoc", "basesize=1024"]`             | 147.350 ms (5%) |         |   1.09 MiB (1%) |          53 |
| `["collect", "assoc", "basesize=32"]`               | 147.511 ms (5%) |         |   1.48 MiB (1%) |        1052 |
| `["collect", "seq"]`                                | 294.494 ms (5%) |         | 256.05 KiB (1%) |           2 |
| `["collect", "unordered", "basesize=1"]`            | 240.101 ms (5%) |         |  23.79 MiB (1%) |      409406 |
| `["collect", "unordered", "basesize=1024"]`         | 155.869 ms (5%) |         |   1.01 MiB (1%) |         981 |
| `["collect", "unordered", "basesize=32"]`           | 162.854 ms (5%) |         |   1.60 MiB (1%) |       15224 |
| `["findfirst", "n=1000", "foldl"]`                  | 505.448 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 275.914 ms (5%) |         | 232.70 KiB (1%) |        3271 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 338.660 ms (5%) |         | 157.20 KiB (1%) |        2193 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 345.366 ms (5%) |         |  81.42 KiB (1%) |        1149 |
| `["findfirst", "n=400", "foldl"]`                   | 378.907 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 195.465 ms (5%) |         | 383.12 KiB (1%) |        5454 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 198.271 ms (5%) |         | 200.86 KiB (1%) |        2873 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 251.886 ms (5%) |         | 138.86 KiB (1%) |        1963 |
| `["findfirst", "n=500", "foldl"]`                   |  64.888 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |  88.443 ms (5%) |         | 167.59 KiB (1%) |        2296 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |  92.877 ms (5%) |         |  97.86 KiB (1%) |        1337 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  98.241 ms (5%) |         |  63.67 KiB (1%) |         866 |
| `["overhead", "default"]`                           |  50.003 μs (5%) |         |  32.73 KiB (1%) |         418 |
| `["overhead", "stoppable=false"]`                   |  50.714 μs (5%) |         |  32.72 KiB (1%) |         417 |
| `["overhead", "stoppable=true"]`                    |  57.587 μs (5%) |         |  44.22 KiB (1%) |         609 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   2.377 ms (5%) |         | 728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   2.920 ms (5%) |         |   1.79 MiB (1%) |         216 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   2.653 ms (5%) |         |   1.42 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |   7.709 ms (5%) |         |   1.54 MiB (1%) |        1218 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  13.364 ms (5%) |         |   1.34 MiB (1%) |        9951 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  11.397 ms (5%) |         |   1.26 MiB (1%) |        7287 |
| `["parallel_histogram", "seq"]`                     |   4.240 ms (5%) |         | 364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  31.107 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  15.583 ms (5%) |         |  736 bytes (1%) |          11 |
| `["splitby", "count", "foldl"]`                     |   1.547 ms (5%) |         |                 |             |
| `["splitby", "count", "man"]`                       |   1.157 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    | 765.832 μs (5%) |         |   1.09 KiB (1%) |          19 |
| `["sum", "random", "foldl"]`                        |  11.041 ms (5%) |         |                 |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   5.655 ms (5%) |         |  74.11 KiB (1%) |        1102 |
| `["sum", "random", "reduce", "basesize=256"]`       |   5.593 ms (5%) |         |  36.77 KiB (1%) |         547 |
| `["sum", "random", "reduce", "basesize=512"]`       |   5.556 ms (5%) |         |  18.11 KiB (1%) |         270 |
| `["sum", "uniform", "foldl"]`                       |  10.877 ms (5%) |         |                 |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   5.573 ms (5%) |         |  74.17 KiB (1%) |        1104 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   5.518 ms (5%) |         |  36.64 KiB (1%) |         543 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   5.477 ms (5%) |         |  18.03 KiB (1%) |         268 |
| `["sum", "valley", "foldl"]`                        |  11.107 ms (5%) |         |                 |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   5.684 ms (5%) |         |  74.05 KiB (1%) |        1100 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   5.629 ms (5%) |         |  36.77 KiB (1%) |         547 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   5.598 ms (5%) |         |  18.06 KiB (1%) |         269 |
| `["words", "nthreads=1"]`                           |  14.453 ms (5%) |         |  31.96 MiB (1%) |     1040999 |
| `["words", "nthreads=2"]`                           |  10.127 ms (5%) |         |  32.67 MiB (1%) |     1041077 |
| `["words", "nthreads=4"]`                           |  10.367 ms (5%) |         |  33.30 MiB (1%) |     1041211 |

## Benchmark Group List
Here's a list of all the benchmark groups executed by this job:

- `["collect", "assoc"]`
- `["collect"]`
- `["collect", "unordered"]`
- `["findfirst", "n=1000"]`
- `["findfirst", "n=1000", "reduce"]`
- `["findfirst", "n=400"]`
- `["findfirst", "n=400", "reduce"]`
- `["findfirst", "n=500"]`
- `["findfirst", "n=500", "reduce"]`
- `["overhead"]`
- `["parallel_histogram", "assoc"]`
- `["parallel_histogram", "comm"]`
- `["parallel_histogram"]`
- `["partition_length_maximum", "rand"]`
- `["splitby", "count"]`
- `["sum", "random"]`
- `["sum", "random", "reduce"]`
- `["sum", "uniform"]`
- `["sum", "uniform", "reduce"]`
- `["sum", "valley"]`
- `["sum", "valley", "reduce"]`
- `["words"]`

## Julia versioninfo
```
Julia Version 1.7.3
Commit 742b9abb4d (2022-05-06 12:58 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 22.04.4 LTS
  uname: Linux 6.5.0-1015-azure #15~22.04.1-Ubuntu SMP Tue Feb 13 01:15:12 UTC 2024 x86_64 x86_64
  CPU: AMD EPYC 7763 64-Core Processor: 
              speed         user         nice          sys         idle          irq
       #1  3246 MHz       2075 s          0 s        159 s       5614 s          0 s
       #2  3242 MHz       2589 s          0 s        161 s       5102 s          0 s
       #3  3209 MHz       3026 s          0 s        172 s       4660 s          0 s
       #4  2555 MHz       2326 s          0 s        173 s       5348 s          0 s
       
  Memory: 15.606491088867188 GB (12444.515625 MB free)
  Uptime: 789.22 sec
  Load Avg:  1.77  1.53  0.9
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, znver3)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 29 Feb 2024 - 1:25
* Package commit: 2a51f8
* Julia commit: 742b9a
* Julia command flags: None
* Environment variables: `JULIA_NUM_THREADS => 2`

## Results
Below is a table of this job's results, obtained by running the benchmarks.
The values listed in the `ID` column have the structure `[parent_group, child_group, ..., key]`, and can be used to
index into the BaseBenchmarks suite to retrieve the corresponding benchmarks.
The percentages accompanying time and memory values in the below table are noise tolerances. The "true"
time/memory value for a given benchmark is expected to fall within this percentage of the reported value.
An empty cell means that the value was zero.

| ID                                                  | time            | GC time | memory          | allocations |
|-----------------------------------------------------|----------------:|--------:|----------------:|------------:|
| `["collect", "assoc", "basesize=1"]`                | 148.576 ms (5%) |         |   4.36 MiB (1%) |       32800 |
| `["collect", "assoc", "basesize=1024"]`             | 147.837 ms (5%) |         |   1.09 MiB (1%) |          54 |
| `["collect", "assoc", "basesize=32"]`               | 147.540 ms (5%) |         |   1.48 MiB (1%) |        1052 |
| `["collect", "seq"]`                                | 294.512 ms (5%) |         | 256.05 KiB (1%) |           2 |
| `["collect", "unordered", "basesize=1"]`            | 310.162 ms (5%) |         |  23.67 MiB (1%) |      405332 |
| `["collect", "unordered", "basesize=1024"]`         | 156.433 ms (5%) |         |   1.01 MiB (1%) |         976 |
| `["collect", "unordered", "basesize=32"]`           | 168.609 ms (5%) |         |   1.60 MiB (1%) |       15275 |
| `["findfirst", "n=1000", "foldl"]`                  | 505.797 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 275.883 ms (5%) |         | 232.70 KiB (1%) |        3271 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 338.724 ms (5%) |         | 157.20 KiB (1%) |        2193 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 453.536 ms (5%) |         | 108.55 KiB (1%) |        1509 |
| `["findfirst", "n=400", "foldl"]`                   | 378.302 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 197.629 ms (5%) |         | 390.70 KiB (1%) |        5563 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 198.214 ms (5%) |         | 200.86 KiB (1%) |        2873 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 253.442 ms (5%) |         | 138.89 KiB (1%) |        1968 |
| `["findfirst", "n=500", "foldl"]`                   |  65.790 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |  77.988 ms (5%) |         | 156.84 KiB (1%) |        2142 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |  61.624 ms (5%) |         |  78.45 KiB (1%) |        1068 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  85.105 ms (5%) |         |  56.83 KiB (1%) |         778 |
| `["overhead", "default"]`                           |  52.438 μs (5%) |         |  32.70 KiB (1%) |         417 |
| `["overhead", "stoppable=false"]`                   |  51.786 μs (5%) |         |  32.75 KiB (1%) |         418 |
| `["overhead", "stoppable=true"]`                    |  58.308 μs (5%) |         |  44.28 KiB (1%) |         611 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   2.385 ms (5%) |         | 728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   3.010 ms (5%) |         |   2.05 MiB (1%) |         222 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   2.655 ms (5%) |         |   1.42 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |   8.477 ms (5%) |         |   1.58 MiB (1%) |        2557 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  12.415 ms (5%) |         |   1.30 MiB (1%) |        8849 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  11.839 ms (5%) |         |   1.27 MiB (1%) |        7802 |
| `["parallel_histogram", "seq"]`                     |   4.239 ms (5%) |         | 364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  31.112 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  15.572 ms (5%) |         |  736 bytes (1%) |          11 |
| `["splitby", "count", "foldl"]`                     |   1.526 ms (5%) |         |                 |             |
| `["splitby", "count", "man"]`                       |   1.157 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    | 857.262 μs (5%) |         |   1.02 KiB (1%) |          18 |
| `["sum", "random", "foldl"]`                        |  10.976 ms (5%) |         |                 |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   5.624 ms (5%) |         |  74.20 KiB (1%) |        1105 |
| `["sum", "random", "reduce", "basesize=256"]`       |   5.560 ms (5%) |         |  36.70 KiB (1%) |         545 |
| `["sum", "random", "reduce", "basesize=512"]`       |   5.523 ms (5%) |         |  18.08 KiB (1%) |         269 |
| `["sum", "uniform", "foldl"]`                       |  10.878 ms (5%) |         |                 |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   5.574 ms (5%) |         |  74.14 KiB (1%) |        1103 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   5.508 ms (5%) |         |  36.77 KiB (1%) |         547 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   5.477 ms (5%) |         |  18.00 KiB (1%) |         267 |
| `["sum", "valley", "foldl"]`                        |  11.106 ms (5%) |         |                 |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   5.683 ms (5%) |         |  74.14 KiB (1%) |        1103 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   5.622 ms (5%) |         |  36.73 KiB (1%) |         546 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   5.607 ms (5%) |         |  18.03 KiB (1%) |         268 |
| `["words", "nthreads=1"]`                           |  14.521 ms (5%) |         |  31.72 MiB (1%) |     1033115 |
| `["words", "nthreads=2"]`                           |  10.469 ms (5%) |         |  32.43 MiB (1%) |     1033230 |
| `["words", "nthreads=4"]`                           |  10.240 ms (5%) |         |  32.88 MiB (1%) |     1033307 |

## Benchmark Group List
Here's a list of all the benchmark groups executed by this job:

- `["collect", "assoc"]`
- `["collect"]`
- `["collect", "unordered"]`
- `["findfirst", "n=1000"]`
- `["findfirst", "n=1000", "reduce"]`
- `["findfirst", "n=400"]`
- `["findfirst", "n=400", "reduce"]`
- `["findfirst", "n=500"]`
- `["findfirst", "n=500", "reduce"]`
- `["overhead"]`
- `["parallel_histogram", "assoc"]`
- `["parallel_histogram", "comm"]`
- `["parallel_histogram"]`
- `["partition_length_maximum", "rand"]`
- `["splitby", "count"]`
- `["sum", "random"]`
- `["sum", "random", "reduce"]`
- `["sum", "uniform"]`
- `["sum", "uniform", "reduce"]`
- `["sum", "valley"]`
- `["sum", "valley", "reduce"]`
- `["words"]`

## Julia versioninfo
```
Julia Version 1.7.3
Commit 742b9abb4d (2022-05-06 12:58 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 22.04.4 LTS
  uname: Linux 6.5.0-1015-azure #15~22.04.1-Ubuntu SMP Tue Feb 13 01:15:12 UTC 2024 x86_64 x86_64
  CPU: AMD EPYC 7763 64-Core Processor: 
              speed         user         nice          sys         idle          irq
       #1  2445 MHz       3176 s          0 s        238 s       7397 s          0 s
       #2  2445 MHz       3696 s          0 s        231 s       6886 s          0 s
       #3  3209 MHz       4310 s          0 s        249 s       6263 s          0 s
       #4  3243 MHz       3434 s          0 s        240 s       7136 s          0 s
       
  Memory: 15.606491088867188 GB (12332.75390625 MB free)
  Uptime: 1086.16 sec
  Load Avg:  1.76  1.69  1.15
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, znver3)
```

---
# Runtime information
| Runtime Info | |
|:--|:--|
| BLAS #threads | 4 |
| `BLAS.vendor()` | `openblas64` |
| `Sys.CPU_THREADS` | 4 |

`lscpu` output:

    Architecture:                       x86_64
    CPU op-mode(s):                     32-bit, 64-bit
    Address sizes:                      48 bits physical, 48 bits virtual
    Byte Order:                         Little Endian
    CPU(s):                             4
    On-line CPU(s) list:                0-3
    Vendor ID:                          AuthenticAMD
    Model name:                         AMD EPYC 7763 64-Core Processor
    CPU family:                         25
    Model:                              1
    Thread(s) per core:                 2
    Core(s) per socket:                 2
    Socket(s):                          1
    Stepping:                           1
    BogoMIPS:                           4890.84
    Flags:                              fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush mmx fxsr sse sse2 ht syscall nx mmxext fxsr_opt pdpe1gb rdtscp lm constant_tsc rep_good nopl tsc_reliable nonstop_tsc cpuid extd_apicid aperfmperf pni pclmulqdq ssse3 fma cx16 pcid sse4_1 sse4_2 movbe popcnt aes xsave avx f16c rdrand hypervisor lahf_lm cmp_legacy svm cr8_legacy abm sse4a misalignsse 3dnowprefetch osvw topoext invpcid_single vmmcall fsgsbase bmi1 avx2 smep bmi2 erms invpcid rdseed adx smap clflushopt clwb sha_ni xsaveopt xsavec xgetbv1 xsaves clzero xsaveerptr rdpru arat npt nrip_save tsc_scale vmcb_clean flushbyasid decodeassists pausefilter pfthreshold v_vmsave_vmload umip vaes vpclmulqdq rdpid fsrm
    Virtualization:                     AMD-V
    Hypervisor vendor:                  Microsoft
    Virtualization type:                full
    L1d cache:                          64 KiB (2 instances)
    L1i cache:                          64 KiB (2 instances)
    L2 cache:                           1 MiB (2 instances)
    L3 cache:                           32 MiB (1 instance)
    NUMA node(s):                       1
    NUMA node0 CPU(s):                  0-3
    Vulnerability Gather data sampling: Not affected
    Vulnerability Itlb multihit:        Not affected
    Vulnerability L1tf:                 Not affected
    Vulnerability Mds:                  Not affected
    Vulnerability Meltdown:             Not affected
    Vulnerability Mmio stale data:      Not affected
    Vulnerability Retbleed:             Not affected
    Vulnerability Spec rstack overflow: Mitigation; safe RET, no microcode
    Vulnerability Spec store bypass:    Vulnerable
    Vulnerability Spectre v1:           Mitigation; usercopy/swapgs barriers and __user pointer sanitization
    Vulnerability Spectre v2:           Mitigation; Retpolines, STIBP disabled, RSB filling, PBRSB-eIBRS Not affected
    Vulnerability Srbds:                Not affected
    Vulnerability Tsx async abort:      Not affected
    

| Cpu Property       | Value                                                      |
|:------------------ |:---------------------------------------------------------- |
| Brand              | AMD EPYC 7763 64-Core Processor                            |
| Vendor             | :AMD                                                       |
| Architecture       | :Unknown                                                   |
| Model              | Family: 0xaf, Model: 0x01, Stepping: 0x01, Type: 0x00      |
| Cores              | 16 physical cores, 16 logical cores (on executing CPU)     |
|                    | No Hyperthreading hardware capability detected             |
| Clock Frequencies  | Not supported by CPU                                       |
| Data Cache         | Level 1:3 : (32, 512, 32768) kbytes                        |
|                    | 64 byte cache line size                                    |
| Address Size       | 48 bits virtual, 48 bits physical                          |
| SIMD               | 256 bit = 32 byte max. SIMD vector size                    |
| Time Stamp Counter | TSC is accessible via `rdtsc`                              |
|                    | TSC runs at constant rate (invariant from clock frequency) |
| Perf. Monitoring   | Performance Monitoring Counters (PMC) are not supported    |
| Hypervisor         | Yes, Microsoft                                             |

