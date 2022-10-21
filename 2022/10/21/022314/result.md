# Multi-thread benchmark result

* Pull request commit: [`1e9f0479e5cb0f7d456f2cea57c2a7ed8156d4fd`](https://github.com/JuliaFolds/Transducers.jl/commit/1e9f0479e5cb0f7d456f2cea57c2a7ed8156d4fd)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/243> (Update */Manifest.toml)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 21 Oct 2022 - 02:17
    - Baseline: 21 Oct 2022 - 02:22
* Package commits:
    - Target: 49d538
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
| `["collect", "assoc", "basesize=1024"]`             |                1.08 (5%) :x: |                   1.00 (1%)  |
| `["collect", "unordered", "basesize=1"]`            |                1.09 (5%) :x: |                1.01 (1%) :x: |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` |                1.11 (5%) :x: |                1.06 (1%) :x: |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 0.82 (5%) :white_check_mark: | 0.83 (1%) :white_check_mark: |
| `["findfirst", "n=400", "foldl"]`                   |                1.08 (5%) :x: |                   1.00 (1%)  |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  |                   1.03 (5%)  |                1.01 (1%) :x: |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  |                1.43 (5%) :x: |                1.37 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 0.56 (5%) :white_check_mark: | 0.61 (1%) :white_check_mark: |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 0.93 (5%) :white_check_mark: | 0.96 (1%) :white_check_mark: |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 0.42 (5%) :white_check_mark: | 0.57 (1%) :white_check_mark: |
| `["overhead", "stoppable=false"]`                   |                1.08 (5%) :x: |                   1.00 (1%)  |
| `["overhead", "stoppable=true"]`                    |                1.08 (5%) :x: |                   1.00 (1%)  |
| `["parallel_histogram", "assoc", "basesize=4096"]`  | 0.92 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["parallel_histogram", "assoc", "basesize=8192"]`  | 0.89 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["parallel_histogram", "comm", "basesize=16384"]`  | 0.93 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["parallel_histogram", "comm", "basesize=4096"]`   |                   0.98 (5%)  | 0.97 (1%) :white_check_mark: |
| `["parallel_histogram", "comm", "basesize=8192"]`   |                1.22 (5%) :x: | 0.93 (1%) :white_check_mark: |
| `["partition_length_maximum", "rand", "reduce"]`    |                1.09 (5%) :x: |                   1.00 (1%)  |
| `["splitby", "count", "foldl"]`                     |                1.08 (5%) :x: |                   1.00 (1%)  |
| `["splitby", "count", "reduce"]`                    |                1.06 (5%) :x: |                   1.00 (1%)  |
| `["sum", "uniform", "reduce", "basesize=128"]`      |                1.08 (5%) :x: |                   1.00 (1%)  |
| `["sum", "uniform", "reduce", "basesize=256"]`      |                1.08 (5%) :x: |                   1.00 (1%)  |
| `["words", "nthreads=1"]`                           |                1.07 (5%) :x: |                   1.01 (1%)  |

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
      Ubuntu 20.04.5 LTS
  uname: Linux 5.15.0-1022-azure #27~20.04.1-Ubuntu SMP Mon Oct 17 02:03:50 UTC 2022 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz: 
              speed         user         nice          sys         idle          irq
       #1  2294 MHz       4817 s          2 s        290 s       2385 s          0 s
       #2  2294 MHz       5866 s          1 s        300 s       1353 s          0 s
       
  Memory: 6.78125 GB (3690.05859375 MB free)
  Uptime: 757.59 sec
  Load Avg:  1.56  1.53  1.0
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, broadwell)
```

### Baseline
```
Julia Version 1.7.3
Commit 742b9abb4d (2022-05-06 12:58 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 20.04.5 LTS
  uname: Linux 5.15.0-1022-azure #27~20.04.1-Ubuntu SMP Mon Oct 17 02:03:50 UTC 2022 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz: 
              speed         user         nice          sys         idle          irq
       #1  2294 MHz       6770 s          2 s        389 s       3635 s          0 s
       #2  2294 MHz       8816 s          1 s        403 s       1612 s          0 s
       
  Memory: 6.78125 GB (3650.04296875 MB free)
  Uptime: 1089.2 sec
  Load Avg:  1.65  1.57  1.18
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, broadwell)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 21 Oct 2022 - 2:17
* Package commit: 49d538
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
| `["collect", "assoc", "basesize=1"]`                | 246.641 ms (5%) |         |  25.97 MiB (1%) |      306838 |
| `["collect", "assoc", "basesize=1024"]`             | 191.640 ms (5%) |         |   2.61 MiB (1%) |         456 |
| `["collect", "assoc", "basesize=32"]`               | 191.593 ms (5%) |         |   4.82 MiB (1%) |       11710 |
| `["collect", "seq"]`                                | 350.049 ms (5%) |         | 812.73 KiB (1%) |          11 |
| `["collect", "unordered", "basesize=1"]`            | 396.933 ms (5%) |         |  23.88 MiB (1%) |      412448 |
| `["collect", "unordered", "basesize=1024"]`         | 193.977 ms (5%) |         |   1.02 MiB (1%) |        1497 |
| `["collect", "unordered", "basesize=32"]`           | 226.450 ms (5%) |         |   1.60 MiB (1%) |       15236 |
| `["findfirst", "n=1000", "foldl"]`                  | 580.556 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 526.746 ms (5%) |         | 359.92 KiB (1%) |        5035 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 401.404 ms (5%) |         | 157.23 KiB (1%) |        2194 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 708.586 ms (5%) |         | 134.03 KiB (1%) |        1893 |
| `["findfirst", "n=400", "foldl"]`                   | 449.559 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 237.446 ms (5%) |         | 388.41 KiB (1%) |        5519 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 240.500 ms (5%) |         | 202.81 KiB (1%) |        2909 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 352.479 ms (5%) |         | 146.98 KiB (1%) |        2111 |
| `["findfirst", "n=500", "foldl"]`                   |  70.174 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 113.305 ms (5%) |         | 167.00 KiB (1%) |        2291 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 160.011 ms (5%) |         | 130.48 KiB (1%) |        1780 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 110.681 ms (5%) |         |  63.69 KiB (1%) |         864 |
| `["overhead", "default"]`                           |  79.000 μs (5%) |         |  32.73 KiB (1%) |         418 |
| `["overhead", "stoppable=false"]`                   |  80.100 μs (5%) |         |  32.78 KiB (1%) |         419 |
| `["overhead", "stoppable=true"]`                    |  93.700 μs (5%) |         |  44.25 KiB (1%) |         610 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   2.754 ms (5%) |         | 728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   3.491 ms (5%) |         |   1.79 MiB (1%) |         216 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   3.031 ms (5%) |         |   1.42 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  18.277 ms (5%) |         |   1.61 MiB (1%) |        3389 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  25.355 ms (5%) |         |   1.27 MiB (1%) |        7665 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  23.158 ms (5%) |         |   1.19 MiB (1%) |        5292 |
| `["parallel_histogram", "seq"]`                     |   4.845 ms (5%) |         | 364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  36.349 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  19.989 ms (5%) |         |  736 bytes (1%) |          11 |
| `["splitby", "count", "foldl"]`                     |   1.888 ms (5%) |         |                 |             |
| `["splitby", "count", "man"]`                       |   1.334 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    | 859.899 μs (5%) |         |   1.06 KiB (1%) |          18 |
| `["sum", "random", "foldl"]`                        |  13.879 ms (5%) |         |                 |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   7.184 ms (5%) |         |  74.11 KiB (1%) |        1102 |
| `["sum", "random", "reduce", "basesize=256"]`       |   6.886 ms (5%) |         |  36.73 KiB (1%) |         546 |
| `["sum", "random", "reduce", "basesize=512"]`       |   7.094 ms (5%) |         |  18.11 KiB (1%) |         270 |
| `["sum", "uniform", "foldl"]`                       |  13.394 ms (5%) |         |                 |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   7.412 ms (5%) |         |  74.11 KiB (1%) |        1102 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   7.289 ms (5%) |         |  36.70 KiB (1%) |         545 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   6.593 ms (5%) |         |  18.03 KiB (1%) |         268 |
| `["sum", "valley", "foldl"]`                        |  14.135 ms (5%) |         |                 |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   7.413 ms (5%) |         |  74.08 KiB (1%) |        1101 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   7.254 ms (5%) |         |  36.70 KiB (1%) |         545 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   7.288 ms (5%) |         |  18.00 KiB (1%) |         267 |
| `["words", "nthreads=1"]`                           |  30.651 ms (5%) |         |  31.63 MiB (1%) |     1030263 |
| `["words", "nthreads=2"]`                           |  18.054 ms (5%) |         |  32.34 MiB (1%) |     1030336 |
| `["words", "nthreads=4"]`                           |  18.613 ms (5%) |         |  32.79 MiB (1%) |     1030402 |

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
      Ubuntu 20.04.5 LTS
  uname: Linux 5.15.0-1022-azure #27~20.04.1-Ubuntu SMP Mon Oct 17 02:03:50 UTC 2022 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz: 
              speed         user         nice          sys         idle          irq
       #1  2294 MHz       4817 s          2 s        290 s       2385 s          0 s
       #2  2294 MHz       5866 s          1 s        300 s       1353 s          0 s
       
  Memory: 6.78125 GB (3690.05859375 MB free)
  Uptime: 757.59 sec
  Load Avg:  1.56  1.53  1.0
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, broadwell)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 21 Oct 2022 - 2:22
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
| `["collect", "assoc", "basesize=1"]`                | 249.086 ms (5%) |         |  25.97 MiB (1%) |      306835 |
| `["collect", "assoc", "basesize=1024"]`             | 177.974 ms (5%) |         |   2.61 MiB (1%) |         456 |
| `["collect", "assoc", "basesize=32"]`               | 185.177 ms (5%) |         |   4.82 MiB (1%) |       11702 |
| `["collect", "seq"]`                                | 353.306 ms (5%) |         | 812.73 KiB (1%) |          11 |
| `["collect", "unordered", "basesize=1"]`            | 364.392 ms (5%) |         |  23.55 MiB (1%) |      401634 |
| `["collect", "unordered", "basesize=1024"]`         | 200.013 ms (5%) |         |   1.02 MiB (1%) |        1417 |
| `["collect", "unordered", "basesize=32"]`           | 218.523 ms (5%) |         |   1.60 MiB (1%) |       15255 |
| `["findfirst", "n=1000", "foldl"]`                  | 573.608 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 475.703 ms (5%) |         | 338.77 KiB (1%) |        4769 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 403.027 ms (5%) |         | 157.42 KiB (1%) |        2200 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 864.053 ms (5%) |         | 161.78 KiB (1%) |        2284 |
| `["findfirst", "n=400", "foldl"]`                   | 417.276 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 231.958 ms (5%) |         | 386.69 KiB (1%) |        5496 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 233.635 ms (5%) |         | 200.70 KiB (1%) |        2868 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 246.676 ms (5%) |         | 107.09 KiB (1%) |        1549 |
| `["findfirst", "n=500", "foldl"]`                   |  73.480 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 201.230 ms (5%) |         | 274.03 KiB (1%) |        3805 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 172.773 ms (5%) |         | 136.58 KiB (1%) |        1912 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 262.970 ms (5%) |         | 111.03 KiB (1%) |        1536 |
| `["overhead", "default"]`                           |  77.500 μs (5%) |         |  32.73 KiB (1%) |         418 |
| `["overhead", "stoppable=false"]`                   |  74.199 μs (5%) |         |  32.78 KiB (1%) |         419 |
| `["overhead", "stoppable=true"]`                    |  86.899 μs (5%) |         |  44.22 KiB (1%) |         609 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   2.769 ms (5%) |         | 728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   3.777 ms (5%) |         |   1.79 MiB (1%) |         215 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   3.419 ms (5%) |         |   1.42 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  19.566 ms (5%) |         |   1.60 MiB (1%) |        3133 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  25.960 ms (5%) |         |   1.30 MiB (1%) |        8809 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  19.037 ms (5%) |         |   1.28 MiB (1%) |        2971 |
| `["parallel_histogram", "seq"]`                     |   4.688 ms (5%) |         | 364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  36.379 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  18.335 ms (5%) |         |  736 bytes (1%) |          11 |
| `["splitby", "count", "foldl"]`                     |   1.742 ms (5%) |         |                 |             |
| `["splitby", "count", "man"]`                       |   1.334 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    | 807.799 μs (5%) |         |   1.06 KiB (1%) |          18 |
| `["sum", "random", "foldl"]`                        |  13.694 ms (5%) |         |                 |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   7.173 ms (5%) |         |  74.17 KiB (1%) |        1104 |
| `["sum", "random", "reduce", "basesize=256"]`       |   6.949 ms (5%) |         |  36.73 KiB (1%) |         546 |
| `["sum", "random", "reduce", "basesize=512"]`       |   6.998 ms (5%) |         |  18.08 KiB (1%) |         269 |
| `["sum", "uniform", "foldl"]`                       |  13.432 ms (5%) |         |                 |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   6.866 ms (5%) |         |  74.11 KiB (1%) |        1102 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   6.718 ms (5%) |         |  36.73 KiB (1%) |         546 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   6.780 ms (5%) |         |  18.03 KiB (1%) |         268 |
| `["sum", "valley", "foldl"]`                        |  14.066 ms (5%) |         |                 |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   7.353 ms (5%) |         |  74.05 KiB (1%) |        1100 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   7.050 ms (5%) |         |  36.73 KiB (1%) |         546 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   6.998 ms (5%) |         |  18.00 KiB (1%) |         267 |
| `["words", "nthreads=1"]`                           |  28.625 ms (5%) |         |  31.46 MiB (1%) |     1025247 |
| `["words", "nthreads=2"]`                           |  17.829 ms (5%) |         |  32.17 MiB (1%) |     1025320 |
| `["words", "nthreads=4"]`                           |  18.067 ms (5%) |         |  32.80 MiB (1%) |     1025468 |

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
      Ubuntu 20.04.5 LTS
  uname: Linux 5.15.0-1022-azure #27~20.04.1-Ubuntu SMP Mon Oct 17 02:03:50 UTC 2022 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz: 
              speed         user         nice          sys         idle          irq
       #1  2294 MHz       6770 s          2 s        389 s       3635 s          0 s
       #2  2294 MHz       8816 s          1 s        403 s       1612 s          0 s
       
  Memory: 6.78125 GB (3650.04296875 MB free)
  Uptime: 1089.2 sec
  Load Avg:  1.65  1.57  1.18
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, broadwell)
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
    Byte Order:                      Little Endian
    Address sizes:                   46 bits physical, 48 bits virtual
    CPU(s):                          2
    On-line CPU(s) list:             0,1
    Thread(s) per core:              1
    Core(s) per socket:              2
    Socket(s):                       1
    NUMA node(s):                    1
    Vendor ID:                       GenuineIntel
    CPU family:                      6
    Model:                           79
    Model name:                      Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz
    Stepping:                        1
    CPU MHz:                         2294.687
    BogoMIPS:                        4589.37
    Hypervisor vendor:               Microsoft
    Virtualization type:             full
    L1d cache:                       64 KiB
    L1i cache:                       64 KiB
    L2 cache:                        512 KiB
    L3 cache:                        50 MiB
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
    Flags:                           fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush mmx fxsr sse sse2 ss ht syscall nx pdpe1gb rdtscp lm constant_tsc rep_good nopl xtopology cpuid pni pclmulqdq ssse3 fma cx16 pcid sse4_1 sse4_2 movbe popcnt aes xsave avx f16c rdrand hypervisor lahf_lm abm 3dnowprefetch invpcid_single pti fsgsbase bmi1 hle avx2 smep bmi2 erms invpcid rtm rdseed adx smap xsaveopt md_clear
    

| Cpu Property       | Value                                                   |
|:------------------ |:------------------------------------------------------- |
| Brand              | Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz               |
| Vendor             | :Intel                                                  |
| Architecture       | :Broadwell                                              |
| Model              | Family: 0x06, Model: 0x4f, Stepping: 0x01, Type: 0x00   |
| Cores              | 2 physical cores, 2 logical cores (on executing CPU)    |
|                    | No Hyperthreading hardware capability detected          |
| Clock Frequencies  | Not supported by CPU                                    |
| Data Cache         | Level 1:3 : (32, 256, 51200) kbytes                     |
|                    | 64 byte cache line size                                 |
| Address Size       | 48 bits virtual, 46 bits physical                       |
| SIMD               | 256 bit = 32 byte max. SIMD vector size                 |
| Time Stamp Counter | TSC is accessible via `rdtsc`                           |
|                    | TSC increased at every clock cycle (non-invariant TSC)  |
| Perf. Monitoring   | Performance Monitoring Counters (PMC) are not supported |
| Hypervisor         | Yes, Microsoft                                          |

