# Multi-thread benchmark result

* Pull request commit: [`7013bc907aba559ac30273efc5769018e7e8abe9`](https://github.com/JuliaFolds/Transducers.jl/commit/7013bc907aba559ac30273efc5769018e7e8abe9)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/553> (Add fast pathway for `copy`, `collect`, `tcollect`, and `tcopy` for size-stable operations)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 5 May 2023 - 00:22
    - Baseline: 5 May 2023 - 00:27
* Package commits:
    - Target: f86a0b
    - Baseline: f8d0df
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
| `["collect", "assoc", "basesize=1"]`                | 0.86 (5%) :white_check_mark: | 0.17 (1%) :white_check_mark: |
| `["collect", "assoc", "basesize=1024"]`             |                   1.00 (5%)  | 0.42 (1%) :white_check_mark: |
| `["collect", "assoc", "basesize=32"]`               |                   0.99 (5%)  | 0.31 (1%) :white_check_mark: |
| `["collect", "seq"]`                                |                   1.00 (5%)  | 0.32 (1%) :white_check_mark: |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` |                1.45 (5%) :x: |                1.41 (1%) :x: |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` |                   0.98 (5%)  | 0.95 (1%) :white_check_mark: |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  |                   1.00 (5%)  |                1.02 (1%) :x: |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  |                   1.03 (5%)  |                1.06 (1%) :x: |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  |                1.35 (5%) :x: |                1.36 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 0.43 (5%) :white_check_mark: | 0.54 (1%) :white_check_mark: |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |                1.23 (5%) :x: |                1.15 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |                   1.00 (5%)  | 0.98 (1%) :white_check_mark: |
| `["parallel_histogram", "comm", "basesize=4096"]`   |                   0.97 (5%)  |                1.04 (1%) :x: |

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
      Ubuntu 22.04.2 LTS
  uname: Linux 5.15.0-1036-azure #43-Ubuntu SMP Wed Mar 29 16:11:05 UTC 2023 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8370C CPU @ 2.80GHz: 
              speed         user         nice          sys         idle          irq
       #1  2793 MHz       5294 s          0 s        234 s       2515 s          0 s
       #2  2793 MHz       5179 s          0 s        246 s       2607 s          0 s
       
  Memory: 6.781208038330078 GB (3534.48828125 MB free)
  Uptime: 810.31 sec
  Load Avg:  1.72  1.52  0.94
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, icelake-server)
```

### Baseline
```
Julia Version 1.7.3
Commit 742b9abb4d (2022-05-06 12:58 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 22.04.2 LTS
  uname: Linux 5.15.0-1036-azure #43-Ubuntu SMP Wed Mar 29 16:11:05 UTC 2023 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8370C CPU @ 2.80GHz: 
              speed         user         nice          sys         idle          irq
       #1  2793 MHz       7795 s          0 s        272 s       2894 s          0 s
       #2  2793 MHz       7254 s          0 s        276 s       3420 s          0 s
       
  Memory: 6.781208038330078 GB (3729.14453125 MB free)
  Uptime: 1102.56 sec
  Load Avg:  1.6  1.55  1.11
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, icelake-server)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 5 May 2023 - 0:22
* Package commit: f86a0b
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
| `["collect", "assoc", "basesize=1"]`                | 240.499 ms (5%) |         |   4.36 MiB (1%) |       32800 |
| `["collect", "assoc", "basesize=1024"]`             | 239.061 ms (5%) |         |   1.09 MiB (1%) |          53 |
| `["collect", "assoc", "basesize=32"]`               | 239.094 ms (5%) |         |   1.48 MiB (1%) |        1052 |
| `["collect", "seq"]`                                | 477.078 ms (5%) |         | 256.05 KiB (1%) |           2 |
| `["collect", "unordered", "basesize=1"]`            | 368.668 ms (5%) |         |  23.92 MiB (1%) |      413557 |
| `["collect", "unordered", "basesize=1024"]`         | 250.944 ms (5%) |         |   1.01 MiB (1%) |         943 |
| `["collect", "unordered", "basesize=32"]`           | 260.909 ms (5%) |         |   1.59 MiB (1%) |       14959 |
| `["findfirst", "n=1000", "foldl"]`                  | 735.993 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 616.129 ms (5%) |         | 343.20 KiB (1%) |        4831 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 496.785 ms (5%) |         | 157.20 KiB (1%) |        2193 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 645.068 ms (5%) |         | 103.53 KiB (1%) |        1454 |
| `["findfirst", "n=400", "foldl"]`                   | 552.682 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 286.624 ms (5%) |         | 380.70 KiB (1%) |        5421 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 300.462 ms (5%) |         | 212.14 KiB (1%) |        3028 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 435.769 ms (5%) |         | 153.03 KiB (1%) |        2185 |
| `["findfirst", "n=500", "foldl"]`                   |  95.698 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 116.919 ms (5%) |         | 162.91 KiB (1%) |        2210 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 274.490 ms (5%) |         | 167.88 KiB (1%) |        2371 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 124.507 ms (5%) |         |  56.89 KiB (1%) |         780 |
| `["overhead", "default"]`                           |  69.299 μs (5%) |         |  32.67 KiB (1%) |         416 |
| `["overhead", "stoppable=false"]`                   |  70.199 μs (5%) |         |  32.75 KiB (1%) |         418 |
| `["overhead", "stoppable=true"]`                    |  78.299 μs (5%) |         |  44.28 KiB (1%) |         611 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   3.744 ms (5%) |         | 728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   4.508 ms (5%) |         |   1.79 MiB (1%) |         216 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   4.125 ms (5%) |         |   1.42 MiB (1%) |         118 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  14.332 ms (5%) |         |   1.64 MiB (1%) |        4458 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  22.516 ms (5%) |         |   1.37 MiB (1%) |       11053 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  20.512 ms (5%) |         |   1.35 MiB (1%) |        9560 |
| `["parallel_histogram", "seq"]`                     |   6.653 ms (5%) |         | 364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  41.351 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  20.622 ms (5%) |         |  736 bytes (1%) |          11 |
| `["splitby", "count", "foldl"]`                     |   2.307 ms (5%) |         |                 |             |
| `["splitby", "count", "man"]`                       |   1.528 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    |   1.082 ms (5%) |         |   1.09 KiB (1%) |          19 |
| `["sum", "random", "foldl"]`                        |  17.974 ms (5%) |         |                 |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   9.208 ms (5%) |         |  74.14 KiB (1%) |        1103 |
| `["sum", "random", "reduce", "basesize=256"]`       |   9.131 ms (5%) |         |  36.70 KiB (1%) |         545 |
| `["sum", "random", "reduce", "basesize=512"]`       |   9.068 ms (5%) |         |  18.08 KiB (1%) |         269 |
| `["sum", "uniform", "foldl"]`                       |  17.728 ms (5%) |         |                 |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   9.070 ms (5%) |         |  74.17 KiB (1%) |        1104 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   8.991 ms (5%) |         |  36.77 KiB (1%) |         547 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   8.931 ms (5%) |         |  18.03 KiB (1%) |         268 |
| `["sum", "valley", "foldl"]`                        |  18.142 ms (5%) |         |                 |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   9.303 ms (5%) |         |  74.05 KiB (1%) |        1100 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   9.224 ms (5%) |         |  36.73 KiB (1%) |         546 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   9.242 ms (5%) |         |  18.00 KiB (1%) |         267 |
| `["words", "nthreads=1"]`                           |  18.528 ms (5%) |         |  31.94 MiB (1%) |     1040662 |
| `["words", "nthreads=2"]`                           |  11.761 ms (5%) |         |  32.30 MiB (1%) |     1040701 |
| `["words", "nthreads=4"]`                           |  12.684 ms (5%) |         |  33.01 MiB (1%) |     1040792 |

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
      Ubuntu 22.04.2 LTS
  uname: Linux 5.15.0-1036-azure #43-Ubuntu SMP Wed Mar 29 16:11:05 UTC 2023 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8370C CPU @ 2.80GHz: 
              speed         user         nice          sys         idle          irq
       #1  2793 MHz       5294 s          0 s        234 s       2515 s          0 s
       #2  2793 MHz       5179 s          0 s        246 s       2607 s          0 s
       
  Memory: 6.781208038330078 GB (3534.48828125 MB free)
  Uptime: 810.31 sec
  Load Avg:  1.72  1.52  0.94
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, icelake-server)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 5 May 2023 - 0:27
* Package commit: f8d0df
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
| `["collect", "assoc", "basesize=1"]`                | 278.474 ms (5%) |         |  25.97 MiB (1%) |      306841 |
| `["collect", "assoc", "basesize=1024"]`             | 239.163 ms (5%) |         |   2.61 MiB (1%) |         456 |
| `["collect", "assoc", "basesize=32"]`               | 240.436 ms (5%) |         |   4.82 MiB (1%) |       11704 |
| `["collect", "seq"]`                                | 476.818 ms (5%) |         | 812.73 KiB (1%) |          11 |
| `["collect", "unordered", "basesize=1"]`            | 369.159 ms (5%) |         |  23.93 MiB (1%) |      413989 |
| `["collect", "unordered", "basesize=1024"]`         | 250.370 ms (5%) |         |   1.01 MiB (1%) |        1009 |
| `["collect", "unordered", "basesize=32"]`           | 260.906 ms (5%) |         |   1.59 MiB (1%) |       14976 |
| `["findfirst", "n=1000", "foldl"]`                  | 736.518 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 426.002 ms (5%) |         | 244.09 KiB (1%) |        3424 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 496.239 ms (5%) |         | 157.20 KiB (1%) |        2193 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 660.820 ms (5%) |         | 108.55 KiB (1%) |        1509 |
| `["findfirst", "n=400", "foldl"]`                   | 552.399 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 287.580 ms (5%) |         | 373.66 KiB (1%) |        5332 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 291.310 ms (5%) |         | 200.86 KiB (1%) |        2873 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 323.918 ms (5%) |         | 112.56 KiB (1%) |        1621 |
| `["findfirst", "n=500", "foldl"]`                   |  95.799 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 270.831 ms (5%) |         | 303.77 KiB (1%) |        4234 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 223.792 ms (5%) |         | 145.81 KiB (1%) |        2026 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 125.024 ms (5%) |         |  58.28 KiB (1%) |         794 |
| `["overhead", "default"]`                           |  70.600 μs (5%) |         |  32.70 KiB (1%) |         417 |
| `["overhead", "stoppable=false"]`                   |  71.500 μs (5%) |         |  32.75 KiB (1%) |         418 |
| `["overhead", "stoppable=true"]`                    |  80.400 μs (5%) |         |  44.22 KiB (1%) |         609 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   3.720 ms (5%) |         | 728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   4.490 ms (5%) |         |   1.79 MiB (1%) |         215 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   4.113 ms (5%) |         |   1.42 MiB (1%) |         118 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  14.193 ms (5%) |         |   1.66 MiB (1%) |        4992 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  23.144 ms (5%) |         |   1.32 MiB (1%) |        9422 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  21.163 ms (5%) |         |   1.36 MiB (1%) |       10563 |
| `["parallel_histogram", "seq"]`                     |   6.652 ms (5%) |         | 364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  41.293 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  20.578 ms (5%) |         |  736 bytes (1%) |          11 |
| `["splitby", "count", "foldl"]`                     |   2.297 ms (5%) |         |                 |             |
| `["splitby", "count", "man"]`                       |   1.528 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    |   1.101 ms (5%) |         |   1.09 KiB (1%) |          19 |
| `["sum", "random", "foldl"]`                        |  17.954 ms (5%) |         |                 |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   9.171 ms (5%) |         |  74.17 KiB (1%) |        1104 |
| `["sum", "random", "reduce", "basesize=256"]`       |   9.088 ms (5%) |         |  36.73 KiB (1%) |         546 |
| `["sum", "random", "reduce", "basesize=512"]`       |   9.043 ms (5%) |         |  18.11 KiB (1%) |         270 |
| `["sum", "uniform", "foldl"]`                       |  17.727 ms (5%) |         |                 |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   9.058 ms (5%) |         |  74.20 KiB (1%) |        1105 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   8.965 ms (5%) |         |  36.77 KiB (1%) |         547 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   8.912 ms (5%) |         |  18.00 KiB (1%) |         267 |
| `["sum", "valley", "foldl"]`                        |  18.142 ms (5%) |         |                 |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   9.263 ms (5%) |         |  74.02 KiB (1%) |        1099 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   9.191 ms (5%) |         |  36.73 KiB (1%) |         546 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   9.233 ms (5%) |         |  18.00 KiB (1%) |         267 |
| `["words", "nthreads=1"]`                           |  18.405 ms (5%) |         |  31.75 MiB (1%) |     1034443 |
| `["words", "nthreads=2"]`                           |  12.191 ms (5%) |         |  32.46 MiB (1%) |     1034528 |
| `["words", "nthreads=4"]`                           |  12.405 ms (5%) |         |  32.91 MiB (1%) |     1034602 |

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
      Ubuntu 22.04.2 LTS
  uname: Linux 5.15.0-1036-azure #43-Ubuntu SMP Wed Mar 29 16:11:05 UTC 2023 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8370C CPU @ 2.80GHz: 
              speed         user         nice          sys         idle          irq
       #1  2793 MHz       7795 s          0 s        272 s       2894 s          0 s
       #2  2793 MHz       7254 s          0 s        276 s       3420 s          0 s
       
  Memory: 6.781208038330078 GB (3729.14453125 MB free)
  Uptime: 1102.56 sec
  Load Avg:  1.6  1.55  1.11
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, icelake-server)
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
    Model name:                      Intel(R) Xeon(R) Platinum 8370C CPU @ 2.80GHz
    CPU family:                      6
    Model:                           106
    Thread(s) per core:              1
    Core(s) per socket:              2
    Socket(s):                       1
    Stepping:                        6
    BogoMIPS:                        5586.87
    Flags:                           fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush mmx fxsr sse sse2 ss ht syscall nx pdpe1gb rdtscp lm constant_tsc rep_good nopl xtopology cpuid pni pclmulqdq ssse3 fma cx16 pcid sse4_1 sse4_2 movbe popcnt aes xsave avx f16c rdrand hypervisor lahf_lm abm 3dnowprefetch invpcid_single pti fsgsbase bmi1 hle avx2 smep bmi2 erms invpcid rtm avx512f avx512dq rdseed adx smap clflushopt avx512cd avx512bw avx512vl xsaveopt xsavec xsaves md_clear
    Hypervisor vendor:               Microsoft
    Virtualization type:             full
    L1d cache:                       96 KiB (2 instances)
    L1i cache:                       64 KiB (2 instances)
    L2 cache:                        2.5 MiB (2 instances)
    L3 cache:                        48 MiB (1 instance)
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
    Vulnerability Tsx async abort:   Mitigation; Clear CPU buffers; SMT Host state unknown
    

| Cpu Property       | Value                                                   |
|:------------------ |:------------------------------------------------------- |
| Brand              | Intel(R) Xeon(R) Platinum 8370C CPU @ 2.80GHz           |
| Vendor             | :Intel                                                  |
| Architecture       | :UnknownIntel                                           |
| Model              | Family: 0x06, Model: 0x6a, Stepping: 0x06, Type: 0x00   |
| Cores              | 2 physical cores, 2 logical cores (on executing CPU)    |
|                    | No Hyperthreading hardware capability detected          |
| Clock Frequencies  | Not supported by CPU                                    |
| Data Cache         | Level 1:3 : (48, 1280, 49152) kbytes                    |
|                    | 64 byte cache line size                                 |
| Address Size       | 48 bits virtual, 46 bits physical                       |
| SIMD               | 512 bit = 64 byte max. SIMD vector size                 |
| Time Stamp Counter | TSC is accessible via `rdtsc`                           |
|                    | TSC increased at every clock cycle (non-invariant TSC)  |
| Perf. Monitoring   | Performance Monitoring Counters (PMC) are not supported |
| Hypervisor         | Yes, Microsoft                                          |

