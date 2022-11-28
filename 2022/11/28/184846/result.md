# Multi-thread benchmark result

* Pull request commit: [`edf05b784f11993ad553fe66be70e568687e479f`](https://github.com/JuliaFolds/Transducers.jl/commit/edf05b784f11993ad553fe66be70e568687e479f)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/547> (Better example of GetIndex)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 28 Nov 2022 - 18:43
    - Baseline: 28 Nov 2022 - 18:48
* Package commits:
    - Target: 3b42e4
    - Baseline: 142abc
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
| `["findfirst", "n=1000", "reduce", "basesize=512"]` |                   1.01 (5%)  | 0.95 (1%) :white_check_mark: |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  |                   1.04 (5%)  |                1.05 (1%) :x: |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  |                   1.04 (5%)  |                1.03 (1%) :x: |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 0.88 (5%) :white_check_mark: | 0.91 (1%) :white_check_mark: |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 0.76 (5%) :white_check_mark: | 0.85 (1%) :white_check_mark: |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |                1.33 (5%) :x: |                1.27 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |                1.32 (5%) :x: |                1.25 (1%) :x: |
| `["parallel_histogram", "comm", "basesize=16384"]`  |                   1.01 (5%)  | 0.98 (1%) :white_check_mark: |
| `["parallel_histogram", "comm", "basesize=8192"]`   |                1.29 (5%) :x: |                1.53 (1%) :x: |
| `["partition_length_maximum", "rand", "reduce"]`    |                   1.00 (5%)  | 0.96 (1%) :white_check_mark: |
| `["splitby", "count", "man"]`                       | 0.81 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["splitby", "count", "reduce"]`                    |                   1.04 (5%)  |                1.03 (1%) :x: |
| `["words", "nthreads=2"]`                           | 0.95 (5%) :white_check_mark: |                   0.99 (1%)  |

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
      Ubuntu 22.04.1 LTS
  uname: Linux 5.15.0-1023-azure #29-Ubuntu SMP Wed Oct 19 22:37:08 UTC 2022 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2593 MHz       5070 s          0 s        219 s       2530 s          0 s
       #2  2593 MHz       5397 s          0 s        239 s       2162 s          0 s
       
  Memory: 6.781219482421875 GB (3750.50390625 MB free)
  Uptime: 787.26 sec
  Load Avg:  1.67  1.49  0.91
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, skylake-avx512)
```

### Baseline
```
Julia Version 1.7.3
Commit 742b9abb4d (2022-05-06 12:58 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 22.04.1 LTS
  uname: Linux 5.15.0-1023-azure #29-Ubuntu SMP Wed Oct 19 22:37:08 UTC 2022 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2593 MHz       7398 s          0 s        262 s       3093 s          0 s
       #2  2593 MHz       7636 s          0 s        273 s       2823 s          0 s
       
  Memory: 6.781219482421875 GB (3792.49609375 MB free)
  Uptime: 1081.04 sec
  Load Avg:  1.71  1.59  1.11
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, skylake-avx512)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 28 Nov 2022 - 18:43
* Package commit: 3b42e4
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
| `["collect", "assoc", "basesize=1"]`                | 244.582 ms (5%) |         |  25.97 MiB (1%) |      306790 |
| `["collect", "assoc", "basesize=1024"]`             | 198.353 ms (5%) |         |   2.61 MiB (1%) |         456 |
| `["collect", "assoc", "basesize=32"]`               | 200.105 ms (5%) |         |   4.82 MiB (1%) |       11713 |
| `["collect", "seq"]`                                | 395.059 ms (5%) |         | 812.73 KiB (1%) |          11 |
| `["collect", "unordered", "basesize=1"]`            | 342.795 ms (5%) |         |  23.91 MiB (1%) |      413407 |
| `["collect", "unordered", "basesize=1024"]`         | 212.392 ms (5%) |         |   1.01 MiB (1%) |         963 |
| `["collect", "unordered", "basesize=32"]`           | 222.643 ms (5%) |         |   1.57 MiB (1%) |       14417 |
| `["findfirst", "n=1000", "foldl"]`                  | 629.835 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 345.050 ms (5%) |         | 232.86 KiB (1%) |        3276 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 423.959 ms (5%) |         | 157.20 KiB (1%) |        2193 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 564.929 ms (5%) |         | 103.53 KiB (1%) |        1454 |
| `["findfirst", "n=400", "foldl"]`                   | 472.569 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 254.445 ms (5%) |         | 402.06 KiB (1%) |        5723 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 255.543 ms (5%) |         | 206.42 KiB (1%) |        2952 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 332.853 ms (5%) |         | 138.97 KiB (1%) |        1972 |
| `["findfirst", "n=500", "foldl"]`                   |  81.942 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 145.590 ms (5%) |         | 225.91 KiB (1%) |        3098 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 118.528 ms (5%) |         | 106.44 KiB (1%) |        1447 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 117.030 ms (5%) |         |  63.66 KiB (1%) |         865 |
| `["overhead", "default"]`                           |  73.600 μs (5%) |         |  32.73 KiB (1%) |         418 |
| `["overhead", "stoppable=false"]`                   |  74.700 μs (5%) |         |  32.75 KiB (1%) |         418 |
| `["overhead", "stoppable=true"]`                    |  84.401 μs (5%) |         |  44.25 KiB (1%) |         610 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   3.253 ms (5%) |         | 728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   3.899 ms (5%) |         |   1.79 MiB (1%) |         216 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   3.606 ms (5%) |         |   1.42 MiB (1%) |         118 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  16.662 ms (5%) |         |   1.58 MiB (1%) |        2440 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  23.906 ms (5%) |         |   1.25 MiB (1%) |        7227 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  22.389 ms (5%) |         |   1.69 MiB (1%) |        6022 |
| `["parallel_histogram", "seq"]`                     |   5.785 ms (5%) |         | 364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  35.174 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  17.582 ms (5%) |         |  704 bytes (1%) |          10 |
| `["splitby", "count", "foldl"]`                     |   2.239 ms (5%) |         |                 |             |
| `["splitby", "count", "man"]`                       |   1.418 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    |   1.124 ms (5%) |         |   1.09 KiB (1%) |          19 |
| `["sum", "random", "foldl"]`                        |  16.243 ms (5%) |         |                 |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   8.168 ms (5%) |         |  74.05 KiB (1%) |        1100 |
| `["sum", "random", "reduce", "basesize=256"]`       |   8.081 ms (5%) |         |  36.70 KiB (1%) |         545 |
| `["sum", "random", "reduce", "basesize=512"]`       |   8.026 ms (5%) |         |  18.08 KiB (1%) |         269 |
| `["sum", "uniform", "foldl"]`                       |  15.668 ms (5%) |         |                 |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   7.982 ms (5%) |         |  74.02 KiB (1%) |        1099 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   7.878 ms (5%) |         |  36.70 KiB (1%) |         545 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   7.817 ms (5%) |         |  18.03 KiB (1%) |         268 |
| `["sum", "valley", "foldl"]`                        |  16.138 ms (5%) |         |                 |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   8.229 ms (5%) |         |  74.08 KiB (1%) |        1101 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   8.127 ms (5%) |         |  36.77 KiB (1%) |         547 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   8.112 ms (5%) |         |  18.03 KiB (1%) |         268 |
| `["words", "nthreads=1"]`                           |  21.930 ms (5%) |         |  31.60 MiB (1%) |     1029456 |
| `["words", "nthreads=2"]`                           |  13.571 ms (5%) |         |  31.95 MiB (1%) |     1029492 |
| `["words", "nthreads=4"]`                           |  14.324 ms (5%) |         |  32.67 MiB (1%) |     1029603 |

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
      Ubuntu 22.04.1 LTS
  uname: Linux 5.15.0-1023-azure #29-Ubuntu SMP Wed Oct 19 22:37:08 UTC 2022 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2593 MHz       5070 s          0 s        219 s       2530 s          0 s
       #2  2593 MHz       5397 s          0 s        239 s       2162 s          0 s
       
  Memory: 6.781219482421875 GB (3750.50390625 MB free)
  Uptime: 787.26 sec
  Load Avg:  1.67  1.49  0.91
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, skylake-avx512)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 28 Nov 2022 - 18:48
* Package commit: 142abc
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
| `["collect", "assoc", "basesize=1"]`                | 242.716 ms (5%) |         |  25.97 MiB (1%) |      306818 |
| `["collect", "assoc", "basesize=1024"]`             | 198.815 ms (5%) |         |   2.61 MiB (1%) |         456 |
| `["collect", "assoc", "basesize=32"]`               | 200.159 ms (5%) |         |   4.82 MiB (1%) |       11703 |
| `["collect", "seq"]`                                | 395.153 ms (5%) |         | 812.73 KiB (1%) |          11 |
| `["collect", "unordered", "basesize=1"]`            | 340.117 ms (5%) |         |  23.94 MiB (1%) |      414202 |
| `["collect", "unordered", "basesize=1024"]`         | 211.820 ms (5%) |         |   1.01 MiB (1%) |        1091 |
| `["collect", "unordered", "basesize=32"]`           | 222.819 ms (5%) |         |   1.58 MiB (1%) |       14539 |
| `["findfirst", "n=1000", "foldl"]`                  | 623.960 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 342.401 ms (5%) |         | 232.86 KiB (1%) |        3276 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 421.290 ms (5%) |         | 157.20 KiB (1%) |        2193 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 560.689 ms (5%) |         | 108.55 KiB (1%) |        1509 |
| `["findfirst", "n=400", "foldl"]`                   | 469.304 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 244.852 ms (5%) |         | 381.64 KiB (1%) |        5438 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 246.537 ms (5%) |         | 200.86 KiB (1%) |        2873 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 379.491 ms (5%) |         | 153.14 KiB (1%) |        2194 |
| `["findfirst", "n=500", "foldl"]`                   |  81.414 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 191.663 ms (5%) |         | 266.22 KiB (1%) |        3704 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |  89.300 ms (5%) |         |  84.03 KiB (1%) |        1143 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  88.726 ms (5%) |         |  50.92 KiB (1%) |         686 |
| `["overhead", "default"]`                           |  72.801 μs (5%) |         |  32.70 KiB (1%) |         417 |
| `["overhead", "stoppable=false"]`                   |  73.400 μs (5%) |         |  32.78 KiB (1%) |         419 |
| `["overhead", "stoppable=true"]`                    |  83.200 μs (5%) |         |  44.22 KiB (1%) |         609 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   3.227 ms (5%) |         | 728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   3.887 ms (5%) |         |   1.79 MiB (1%) |         215 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   3.575 ms (5%) |         |   1.42 MiB (1%) |         118 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  16.450 ms (5%) |         |   1.60 MiB (1%) |        3246 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  23.971 ms (5%) |         |   1.25 MiB (1%) |        7030 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  17.338 ms (5%) |         |   1.11 MiB (1%) |        2461 |
| `["parallel_histogram", "seq"]`                     |   5.755 ms (5%) |         | 364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  35.176 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  17.600 ms (5%) |         |  736 bytes (1%) |          11 |
| `["splitby", "count", "foldl"]`                     |   2.293 ms (5%) |         |                 |             |
| `["splitby", "count", "man"]`                       |   1.754 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    |   1.081 ms (5%) |         |   1.06 KiB (1%) |          18 |
| `["sum", "random", "foldl"]`                        |  16.340 ms (5%) |         |                 |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   8.134 ms (5%) |         |  74.11 KiB (1%) |        1102 |
| `["sum", "random", "reduce", "basesize=256"]`       |   8.091 ms (5%) |         |  36.77 KiB (1%) |         547 |
| `["sum", "random", "reduce", "basesize=512"]`       |   8.018 ms (5%) |         |  18.08 KiB (1%) |         269 |
| `["sum", "uniform", "foldl"]`                       |  15.752 ms (5%) |         |                 |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   7.954 ms (5%) |         |  74.23 KiB (1%) |        1106 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   7.867 ms (5%) |         |  36.77 KiB (1%) |         547 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   7.805 ms (5%) |         |  18.00 KiB (1%) |         267 |
| `["sum", "valley", "foldl"]`                        |  16.158 ms (5%) |         |                 |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   8.194 ms (5%) |         |  74.05 KiB (1%) |        1100 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   8.103 ms (5%) |         |  36.77 KiB (1%) |         547 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   8.084 ms (5%) |         |  18.06 KiB (1%) |         269 |
| `["words", "nthreads=1"]`                           |  22.168 ms (5%) |         |  31.76 MiB (1%) |     1034794 |
| `["words", "nthreads=2"]`                           |  14.335 ms (5%) |         |  32.12 MiB (1%) |     1034838 |
| `["words", "nthreads=4"]`                           |  14.319 ms (5%) |         |  32.83 MiB (1%) |     1034917 |

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
      Ubuntu 22.04.1 LTS
  uname: Linux 5.15.0-1023-azure #29-Ubuntu SMP Wed Oct 19 22:37:08 UTC 2022 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2593 MHz       7398 s          0 s        262 s       3093 s          0 s
       #2  2593 MHz       7636 s          0 s        273 s       2823 s          0 s
       
  Memory: 6.781219482421875 GB (3792.49609375 MB free)
  Uptime: 1081.04 sec
  Load Avg:  1.71  1.59  1.11
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, skylake-avx512)
```

---
# Runtime information
| Runtime Info | |
|:--|:--|
| BLAS #threads | 2 |
| `BLAS.vendor()` | `openblas64` |
| `Sys.CPU_THREADS` | 2 |

`lscpu` output:

    Architecture:                    x86_64
    CPU op-mode(s):                  32-bit, 64-bit
    Address sizes:                   46 bits physical, 48 bits virtual
    Byte Order:                      Little Endian
    CPU(s):                          2
    On-line CPU(s) list:             0,1
    Vendor ID:                       GenuineIntel
    Model name:                      Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz
    CPU family:                      6
    Model:                           85
    Thread(s) per core:              1
    Core(s) per socket:              2
    Socket(s):                       1
    Stepping:                        7
    BogoMIPS:                        5187.81
    Flags:                           fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush mmx fxsr sse sse2 ss ht syscall nx pdpe1gb rdtscp lm constant_tsc rep_good nopl xtopology cpuid pni pclmulqdq ssse3 fma cx16 pcid sse4_1 sse4_2 movbe popcnt aes xsave avx f16c rdrand hypervisor lahf_lm abm 3dnowprefetch invpcid_single pti fsgsbase bmi1 hle avx2 smep bmi2 erms invpcid rtm mpx avx512f avx512dq rdseed adx smap clflushopt avx512cd avx512bw avx512vl xsaveopt xsavec xsaves md_clear
    Hypervisor vendor:               Microsoft
    Virtualization type:             full
    L1d cache:                       64 KiB (2 instances)
    L1i cache:                       64 KiB (2 instances)
    L2 cache:                        2 MiB (2 instances)
    L3 cache:                        35.8 MiB (1 instance)
    NUMA node(s):                    1
    NUMA node0 CPU(s):               0,1
    Vulnerability Itlb multihit:     KVM: Mitigation: VMX unsupported
    Vulnerability L1tf:              Mitigation; PTE Inversion
    Vulnerability Mds:               Mitigation; Clear CPU buffers; SMT Host state unknown
    Vulnerability Meltdown:          Mitigation; PTI
    Vulnerability Mmio stale data:   Vulnerable: Clear CPU buffers attempted, no microcode; SMT Host state unknown
    Vulnerability Retbleed:          Vulnerable
    Vulnerability Spec store bypass: Vulnerable
    Vulnerability Spectre v1:        Mitigation; usercopy/swapgs barriers and __user pointer sanitization
    Vulnerability Spectre v2:        Mitigation; Retpolines, STIBP disabled, RSB filling, PBRSB-eIBRS Not affected
    Vulnerability Srbds:             Not affected
    Vulnerability Tsx async abort:   Mitigation; Clear CPU buffers; SMT Host state unknown
    

| Cpu Property       | Value                                                   |
|:------------------ |:------------------------------------------------------- |
| Brand              | Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz          |
| Vendor             | :Intel                                                  |
| Architecture       | :Skylake                                                |
| Model              | Family: 0x06, Model: 0x55, Stepping: 0x07, Type: 0x00   |
| Cores              | 2 physical cores, 2 logical cores (on executing CPU)    |
|                    | No Hyperthreading hardware capability detected          |
| Clock Frequencies  | Not supported by CPU                                    |
| Data Cache         | Level 1:3 : (32, 1024, 36608) kbytes                    |
|                    | 64 byte cache line size                                 |
| Address Size       | 48 bits virtual, 46 bits physical                       |
| SIMD               | 512 bit = 64 byte max. SIMD vector size                 |
| Time Stamp Counter | TSC is accessible via `rdtsc`                           |
|                    | TSC increased at every clock cycle (non-invariant TSC)  |
| Perf. Monitoring   | Performance Monitoring Counters (PMC) are not supported |
| Hypervisor         | Yes, Microsoft                                          |

