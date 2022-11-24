# Multi-thread benchmark result

* Pull request commit: [`00dd3eb855d19e0171404a88fbc2c61a8d94b9ad`](https://github.com/JuliaFolds/Transducers.jl/commit/00dd3eb855d19e0171404a88fbc2c61a8d94b9ad)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/536> (Update for v1.9 compatability)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 24 Nov 2022 - 20:25
    - Baseline: 24 Nov 2022 - 20:30
* Package commits:
    - Target: 623210
    - Baseline: 958213
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
| `["findfirst", "n=1000", "reduce", "basesize=256"]` |                1.14 (5%) :x: |                1.08 (1%) :x: |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 0.87 (5%) :white_check_mark: | 0.85 (1%) :white_check_mark: |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  |                1.07 (5%) :x: |                   1.00 (1%)  |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  |                   0.98 (5%)  | 0.97 (1%) :white_check_mark: |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  |                1.16 (5%) :x: |                1.12 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |                1.46 (5%) :x: |                1.45 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |                1.83 (5%) :x: |                1.62 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 0.78 (5%) :white_check_mark: | 0.74 (1%) :white_check_mark: |
| `["parallel_histogram", "comm", "basesize=4096"]`   | 0.89 (5%) :white_check_mark: |                1.02 (1%) :x: |
| `["parallel_histogram", "comm", "basesize=8192"]`   |                   0.98 (5%)  |                1.01 (1%) :x: |
| `["splitby", "count", "man"]`                       |                1.09 (5%) :x: |                   1.00 (1%)  |
| `["splitby", "count", "reduce"]`                    | 0.91 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["words", "nthreads=2"]`                           |                   0.97 (5%)  |                1.02 (1%) :x: |

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
  CPU: Intel(R) Xeon(R) CPU E5-2673 v3 @ 2.40GHz: 
              speed         user         nice          sys         idle          irq
       #1  2394 MHz       5276 s          0 s        254 s       2089 s          0 s
       #2  2394 MHz       5684 s          0 s        268 s       1607 s          0 s
       
  Memory: 6.781219482421875 GB (3593.39453125 MB free)
  Uptime: 770.1 sec
  Load Avg:  1.68  1.57  1.02
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, haswell)
```

### Baseline
```
Julia Version 1.7.3
Commit 742b9abb4d (2022-05-06 12:58 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 22.04.1 LTS
  uname: Linux 5.15.0-1023-azure #29-Ubuntu SMP Wed Oct 19 22:37:08 UTC 2022 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v3 @ 2.40GHz: 
              speed         user         nice          sys         idle          irq
       #1  2394 MHz       7989 s          0 s        301 s       2444 s          0 s
       #2  2394 MHz       7703 s          0 s        308 s       2662 s          0 s
       
  Memory: 6.781219482421875 GB (3643.7578125 MB free)
  Uptime: 1082.41 sec
  Load Avg:  1.55  1.57  1.18
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, haswell)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 24 Nov 2022 - 20:25
* Package commit: 623210
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
| `["collect", "assoc", "basesize=1"]`                | 316.061 ms (5%) |         |  25.97 MiB (1%) |      306799 |
| `["collect", "assoc", "basesize=1024"]`             | 251.534 ms (5%) |         |   2.61 MiB (1%) |         456 |
| `["collect", "assoc", "basesize=32"]`               | 255.740 ms (5%) |         |   4.82 MiB (1%) |       11702 |
| `["collect", "seq"]`                                | 501.488 ms (5%) |         | 812.73 KiB (1%) |          11 |
| `["collect", "unordered", "basesize=1"]`            | 420.052 ms (5%) |         |  23.88 MiB (1%) |      412473 |
| `["collect", "unordered", "basesize=1024"]`         | 270.102 ms (5%) |         |   1.01 MiB (1%) |        1109 |
| `["collect", "unordered", "basesize=32"]`           | 283.533 ms (5%) |         |   1.59 MiB (1%) |       15070 |
| `["findfirst", "n=1000", "foldl"]`                  | 733.801 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 414.232 ms (5%) |         | 234.45 KiB (1%) |        3296 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 565.380 ms (5%) |         | 170.53 KiB (1%) |        2386 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 570.326 ms (5%) |         |  96.67 KiB (1%) |        1343 |
| `["findfirst", "n=400", "foldl"]`                   | 552.004 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 307.830 ms (5%) |         | 391.53 KiB (1%) |        5574 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 292.086 ms (5%) |         | 201.05 KiB (1%) |        2879 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 399.923 ms (5%) |         | 139.09 KiB (1%) |        1980 |
| `["findfirst", "n=500", "foldl"]`                   |  94.085 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 204.120 ms (5%) |         | 246.56 KiB (1%) |        3401 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 196.050 ms (5%) |         | 143.27 KiB (1%) |        1955 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 119.751 ms (5%) |         |  58.09 KiB (1%) |         789 |
| `["overhead", "default"]`                           |  80.001 μs (5%) |         |  32.73 KiB (1%) |         418 |
| `["overhead", "stoppable=false"]`                   |  77.801 μs (5%) |         |  32.75 KiB (1%) |         418 |
| `["overhead", "stoppable=true"]`                    |  90.801 μs (5%) |         |  44.25 KiB (1%) |         610 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   3.848 ms (5%) |         | 728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   4.548 ms (5%) |         |   1.79 MiB (1%) |         215 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   4.221 ms (5%) |         |   1.42 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  12.129 ms (5%) |         |   1.51 MiB (1%) |         226 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  16.144 ms (5%) |         |   1.03 MiB (1%) |        1072 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  15.975 ms (5%) |         |   1.09 MiB (1%) |         996 |
| `["parallel_histogram", "seq"]`                     |   6.816 ms (5%) |         | 364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  62.654 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  32.082 ms (5%) |         |  736 bytes (1%) |          11 |
| `["splitby", "count", "foldl"]`                     |   1.848 ms (5%) |         |                 |             |
| `["splitby", "count", "man"]`                       |   1.655 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    | 898.713 μs (5%) |         |   1.06 KiB (1%) |          18 |
| `["sum", "random", "foldl"]`                        |  18.328 ms (5%) |         |                 |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   9.554 ms (5%) |         |  74.17 KiB (1%) |        1104 |
| `["sum", "random", "reduce", "basesize=256"]`       |   9.476 ms (5%) |         |  36.67 KiB (1%) |         544 |
| `["sum", "random", "reduce", "basesize=512"]`       |   9.427 ms (5%) |         |  18.11 KiB (1%) |         270 |
| `["sum", "uniform", "foldl"]`                       |  17.546 ms (5%) |         |                 |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   9.367 ms (5%) |         |  74.17 KiB (1%) |        1104 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   9.246 ms (5%) |         |  36.67 KiB (1%) |         544 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   9.162 ms (5%) |         |  18.00 KiB (1%) |         267 |
| `["sum", "valley", "foldl"]`                        |  18.099 ms (5%) |         |                 |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   9.647 ms (5%) |         |  74.11 KiB (1%) |        1102 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   9.553 ms (5%) |         |  36.73 KiB (1%) |         546 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   9.515 ms (5%) |         |  18.00 KiB (1%) |         267 |
| `["words", "nthreads=1"]`                           |  28.402 ms (5%) |         |  31.86 MiB (1%) |     1038123 |
| `["words", "nthreads=2"]`                           |  17.209 ms (5%) |         |  32.57 MiB (1%) |     1038196 |
| `["words", "nthreads=4"]`                           |  17.245 ms (5%) |         |  33.02 MiB (1%) |     1038269 |

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
  CPU: Intel(R) Xeon(R) CPU E5-2673 v3 @ 2.40GHz: 
              speed         user         nice          sys         idle          irq
       #1  2394 MHz       5276 s          0 s        254 s       2089 s          0 s
       #2  2394 MHz       5684 s          0 s        268 s       1607 s          0 s
       
  Memory: 6.781219482421875 GB (3593.39453125 MB free)
  Uptime: 770.1 sec
  Load Avg:  1.68  1.57  1.02
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, haswell)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 24 Nov 2022 - 20:30
* Package commit: 958213
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
| `["collect", "assoc", "basesize=1"]`                | 306.475 ms (5%) |         |  25.97 MiB (1%) |      306816 |
| `["collect", "assoc", "basesize=1024"]`             | 250.648 ms (5%) |         |   2.61 MiB (1%) |         456 |
| `["collect", "assoc", "basesize=32"]`               | 257.027 ms (5%) |         |   4.82 MiB (1%) |       11716 |
| `["collect", "seq"]`                                | 501.057 ms (5%) |         | 812.73 KiB (1%) |          11 |
| `["collect", "unordered", "basesize=1"]`            | 427.339 ms (5%) |         |  23.88 MiB (1%) |      412236 |
| `["collect", "unordered", "basesize=1024"]`         | 264.581 ms (5%) |         |   1.01 MiB (1%) |        1113 |
| `["collect", "unordered", "basesize=32"]`           | 281.839 ms (5%) |         |   1.60 MiB (1%) |       15159 |
| `["findfirst", "n=1000", "foldl"]`                  | 741.895 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 400.634 ms (5%) |         | 232.70 KiB (1%) |        3271 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 496.670 ms (5%) |         | 157.27 KiB (1%) |        2195 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 654.995 ms (5%) |         | 114.16 KiB (1%) |        1585 |
| `["findfirst", "n=400", "foldl"]`                   | 553.805 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 286.386 ms (5%) |         | 389.80 KiB (1%) |        5531 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 297.823 ms (5%) |         | 207.17 KiB (1%) |        2958 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 345.107 ms (5%) |         | 123.98 KiB (1%) |        1764 |
| `["findfirst", "n=500", "foldl"]`                   |  93.848 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 140.103 ms (5%) |         | 170.02 KiB (1%) |        2365 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 107.068 ms (5%) |         |  88.70 KiB (1%) |        1200 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 152.728 ms (5%) |         |  78.22 KiB (1%) |        1047 |
| `["overhead", "default"]`                           |  77.101 μs (5%) |         |  32.70 KiB (1%) |         417 |
| `["overhead", "stoppable=false"]`                   |  77.301 μs (5%) |         |  32.78 KiB (1%) |         419 |
| `["overhead", "stoppable=true"]`                    |  90.201 μs (5%) |         |  44.28 KiB (1%) |         611 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   3.841 ms (5%) |         | 728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   4.529 ms (5%) |         |   1.79 MiB (1%) |         215 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   4.189 ms (5%) |         |   1.42 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  11.930 ms (5%) |         |   1.51 MiB (1%) |         288 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  18.106 ms (5%) |         |   1.01 MiB (1%) |        1842 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  16.224 ms (5%) |         |   1.08 MiB (1%) |        1495 |
| `["parallel_histogram", "seq"]`                     |   6.958 ms (5%) |         | 364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  64.237 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  32.326 ms (5%) |         |  736 bytes (1%) |          11 |
| `["splitby", "count", "foldl"]`                     |   1.896 ms (5%) |         |                 |             |
| `["splitby", "count", "man"]`                       |   1.515 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    | 984.914 μs (5%) |         |   1.06 KiB (1%) |          18 |
| `["sum", "random", "foldl"]`                        |  18.933 ms (5%) |         |                 |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   9.624 ms (5%) |         |  74.14 KiB (1%) |        1103 |
| `["sum", "random", "reduce", "basesize=256"]`       |   9.492 ms (5%) |         |  36.77 KiB (1%) |         547 |
| `["sum", "random", "reduce", "basesize=512"]`       |   9.420 ms (5%) |         |  18.05 KiB (1%) |         268 |
| `["sum", "uniform", "foldl"]`                       |  18.422 ms (5%) |         |                 |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   9.408 ms (5%) |         |  74.14 KiB (1%) |        1103 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   9.302 ms (5%) |         |  36.80 KiB (1%) |         548 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   9.191 ms (5%) |         |  18.03 KiB (1%) |         268 |
| `["sum", "valley", "foldl"]`                        |  18.851 ms (5%) |         |                 |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   9.724 ms (5%) |         |  74.11 KiB (1%) |        1102 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   9.562 ms (5%) |         |  36.70 KiB (1%) |         545 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   9.471 ms (5%) |         |  18.00 KiB (1%) |         267 |
| `["words", "nthreads=1"]`                           |  28.571 ms (5%) |         |  31.62 MiB (1%) |     1029644 |
| `["words", "nthreads=2"]`                           |  17.780 ms (5%) |         |  31.97 MiB (1%) |     1029680 |
| `["words", "nthreads=4"]`                           |  17.553 ms (5%) |         |  32.87 MiB (1%) |     1029847 |

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
  CPU: Intel(R) Xeon(R) CPU E5-2673 v3 @ 2.40GHz: 
              speed         user         nice          sys         idle          irq
       #1  2394 MHz       7989 s          0 s        301 s       2444 s          0 s
       #2  2394 MHz       7703 s          0 s        308 s       2662 s          0 s
       
  Memory: 6.781219482421875 GB (3643.7578125 MB free)
  Uptime: 1082.41 sec
  Load Avg:  1.55  1.57  1.18
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, haswell)
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
    Model name:                      Intel(R) Xeon(R) CPU E5-2673 v3 @ 2.40GHz
    CPU family:                      6
    Model:                           63
    Thread(s) per core:              1
    Core(s) per socket:              2
    Socket(s):                       1
    Stepping:                        2
    BogoMIPS:                        4788.91
    Flags:                           fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush mmx fxsr sse sse2 ss ht syscall nx pdpe1gb rdtscp lm constant_tsc rep_good nopl xtopology cpuid pni pclmulqdq ssse3 fma cx16 pcid sse4_1 sse4_2 movbe popcnt aes xsave avx f16c rdrand hypervisor lahf_lm abm invpcid_single pti fsgsbase bmi1 avx2 smep bmi2 erms invpcid xsaveopt md_clear
    Hypervisor vendor:               Microsoft
    Virtualization type:             full
    L1d cache:                       64 KiB (2 instances)
    L1i cache:                       64 KiB (2 instances)
    L2 cache:                        512 KiB (2 instances)
    L3 cache:                        30 MiB (1 instance)
    NUMA node(s):                    1
    NUMA node0 CPU(s):               0,1
    Vulnerability Itlb multihit:     KVM: Mitigation: VMX unsupported
    Vulnerability L1tf:              Mitigation; PTE Inversion
    Vulnerability Mds:               Mitigation; Clear CPU buffers; SMT Host state unknown
    Vulnerability Meltdown:          Mitigation; PTI
    Vulnerability Mmio stale data:   Vulnerable: Clear CPU buffers attempted, no microcode; SMT Host state unknown
    Vulnerability Retbleed:          Not affected
    Vulnerability Spec store bypass: Vulnerable
    Vulnerability Spectre v1:        Mitigation; usercopy/swapgs barriers and __user pointer sanitization
    Vulnerability Spectre v2:        Mitigation; Retpolines, STIBP disabled, RSB filling, PBRSB-eIBRS Not affected
    Vulnerability Srbds:             Not affected
    Vulnerability Tsx async abort:   Not affected
    

| Cpu Property       | Value                                                   |
|:------------------ |:------------------------------------------------------- |
| Brand              | Intel(R) Xeon(R) CPU E5-2673 v3 @ 2.40GHz               |
| Vendor             | :Intel                                                  |
| Architecture       | :Haswell                                                |
| Model              | Family: 0x06, Model: 0x3f, Stepping: 0x02, Type: 0x00   |
| Cores              | 2 physical cores, 2 logical cores (on executing CPU)    |
|                    | No Hyperthreading hardware capability detected          |
| Clock Frequencies  | Not supported by CPU                                    |
| Data Cache         | Level 1:3 : (32, 256, 30720) kbytes                     |
|                    | 64 byte cache line size                                 |
| Address Size       | 48 bits virtual, 46 bits physical                       |
| SIMD               | 256 bit = 32 byte max. SIMD vector size                 |
| Time Stamp Counter | TSC is accessible via `rdtsc`                           |
|                    | TSC increased at every clock cycle (non-invariant TSC)  |
| Perf. Monitoring   | Performance Monitoring Counters (PMC) are not supported |
| Hypervisor         | Yes, Microsoft                                          |

