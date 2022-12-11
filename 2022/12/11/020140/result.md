# Multi-thread benchmark result

* Pull request commit: [`52ec96b09865f533cb0e1204baf5f9a4fed621e1`](https://github.com/JuliaFolds/Transducers.jl/commit/52ec96b09865f533cb0e1204baf5f9a4fed621e1)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/243> (Update */Manifest.toml)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 11 Dec 2022 - 01:56
    - Baseline: 11 Dec 2022 - 02:01
* Package commits:
    - Target: bf2f74
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
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 0.61 (5%) :white_check_mark: | 0.62 (1%) :white_check_mark: |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 0.88 (5%) :white_check_mark: | 0.93 (1%) :white_check_mark: |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 0.92 (5%) :white_check_mark: | 0.95 (1%) :white_check_mark: |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  |                1.05 (5%) :x: |                1.06 (1%) :x: |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  |                1.18 (5%) :x: |                1.13 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |                1.26 (5%) :x: |                1.22 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |                2.53 (5%) :x: |                1.72 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 0.43 (5%) :white_check_mark: | 0.57 (1%) :white_check_mark: |
| `["parallel_histogram", "comm", "basesize=16384"]`  |                   1.02 (5%)  |                1.22 (1%) :x: |
| `["parallel_histogram", "comm", "basesize=4096"]`   |                1.05 (5%) :x: | 0.85 (1%) :white_check_mark: |
| `["words", "nthreads=2"]`                           |                1.15 (5%) :x: |                   1.01 (1%)  |
| `["words", "nthreads=4"]`                           |                1.10 (5%) :x: |                   1.00 (1%)  |

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
  uname: Linux 5.15.0-1024-azure #30-Ubuntu SMP Wed Nov 16 23:37:59 UTC 2022 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8370C CPU @ 2.80GHz: 
              speed         user         nice          sys         idle          irq
       #1  2793 MHz       5528 s          0 s        197 s       2654 s          0 s
       #2  2793 MHz       4751 s          0 s        201 s       3411 s          0 s
       
  Memory: 6.781219482421875 GB (3770.671875 MB free)
  Uptime: 842.32 sec
  Load Avg:  1.64  1.48  0.88
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
      Ubuntu 22.04.1 LTS
  uname: Linux 5.15.0-1024-azure #30-Ubuntu SMP Wed Nov 16 23:37:59 UTC 2022 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8370C CPU @ 2.80GHz: 
              speed         user         nice          sys         idle          irq
       #1  2793 MHz       8019 s          0 s        261 s       3154 s          0 s
       #2  2793 MHz       7001 s          0 s        250 s       4169 s          0 s
       
  Memory: 6.781219482421875 GB (3732.5234375 MB free)
  Uptime: 1148.45 sec
  Load Avg:  1.71  1.58  1.1
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, icelake-server)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 11 Dec 2022 - 1:56
* Package commit: bf2f74
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
| `["collect", "assoc", "basesize=1"]`                | 282.070 ms (5%) |         |  25.97 MiB (1%) |      306821 |
| `["collect", "assoc", "basesize=1024"]`             | 238.879 ms (5%) |         |   2.61 MiB (1%) |         455 |
| `["collect", "assoc", "basesize=32"]`               | 241.699 ms (5%) |         |   4.82 MiB (1%) |       11710 |
| `["collect", "seq"]`                                | 476.790 ms (5%) |         | 812.73 KiB (1%) |          11 |
| `["collect", "unordered", "basesize=1"]`            | 376.558 ms (5%) |         |  23.90 MiB (1%) |      413013 |
| `["collect", "unordered", "basesize=1024"]`         | 251.357 ms (5%) |         |   1.01 MiB (1%) |        1062 |
| `["collect", "unordered", "basesize=32"]`           | 262.993 ms (5%) |         |   1.59 MiB (1%) |       15056 |
| `["findfirst", "n=1000", "foldl"]`                  | 738.924 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 404.391 ms (5%) |         | 230.52 KiB (1%) |        3246 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 494.086 ms (5%) |         | 157.20 KiB (1%) |        2193 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 504.590 ms (5%) |         |  81.33 KiB (1%) |        1146 |
| `["findfirst", "n=400", "foldl"]`                   | 555.291 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 295.188 ms (5%) |         | 391.36 KiB (1%) |        5570 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 315.246 ms (5%) |         | 219.44 KiB (1%) |        3129 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 402.152 ms (5%) |         | 137.72 KiB (1%) |        1961 |
| `["findfirst", "n=500", "foldl"]`                   |  95.962 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 220.670 ms (5%) |         | 263.53 KiB (1%) |        3656 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 275.652 ms (5%) |         | 168.62 KiB (1%) |        2380 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 124.273 ms (5%) |         |  56.83 KiB (1%) |         778 |
| `["overhead", "default"]`                           |  70.899 μs (5%) |         |  32.73 KiB (1%) |         418 |
| `["overhead", "stoppable=false"]`                   |  73.500 μs (5%) |         |  32.75 KiB (1%) |         418 |
| `["overhead", "stoppable=true"]`                    |  84.500 μs (5%) |         |  44.25 KiB (1%) |         610 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   3.744 ms (5%) |         | 728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   4.509 ms (5%) |         |   1.79 MiB (1%) |         216 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   4.126 ms (5%) |         |   1.42 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  14.632 ms (5%) |         |   1.62 MiB (1%) |        3731 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  24.351 ms (5%) |         |   1.18 MiB (1%) |        4879 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  21.399 ms (5%) |         |   1.37 MiB (1%) |       10375 |
| `["parallel_histogram", "seq"]`                     |   6.691 ms (5%) |         | 364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  41.225 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  20.626 ms (5%) |         |  736 bytes (1%) |          11 |
| `["splitby", "count", "foldl"]`                     |   2.330 ms (5%) |         |                 |             |
| `["splitby", "count", "man"]`                       |   1.528 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    |   1.153 ms (5%) |         |   1.09 KiB (1%) |          19 |
| `["sum", "random", "foldl"]`                        |  18.044 ms (5%) |         |                 |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   9.270 ms (5%) |         |  74.14 KiB (1%) |        1103 |
| `["sum", "random", "reduce", "basesize=256"]`       |   9.171 ms (5%) |         |  36.73 KiB (1%) |         546 |
| `["sum", "random", "reduce", "basesize=512"]`       |   9.113 ms (5%) |         |  18.08 KiB (1%) |         269 |
| `["sum", "uniform", "foldl"]`                       |  17.730 ms (5%) |         |                 |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   9.074 ms (5%) |         |  74.20 KiB (1%) |        1105 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   8.978 ms (5%) |         |  36.73 KiB (1%) |         546 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   8.932 ms (5%) |         |  18.03 KiB (1%) |         268 |
| `["sum", "valley", "foldl"]`                        |  18.150 ms (5%) |         |                 |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   9.290 ms (5%) |         |  74.11 KiB (1%) |        1102 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   9.202 ms (5%) |         |  36.73 KiB (1%) |         546 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   9.223 ms (5%) |         |  18.03 KiB (1%) |         268 |
| `["words", "nthreads=1"]`                           |  18.906 ms (5%) |         |  31.60 MiB (1%) |     1029663 |
| `["words", "nthreads=2"]`                           |  13.121 ms (5%) |         |  32.32 MiB (1%) |     1029770 |
| `["words", "nthreads=4"]`                           |  13.663 ms (5%) |         |  32.95 MiB (1%) |     1029951 |

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
  uname: Linux 5.15.0-1024-azure #30-Ubuntu SMP Wed Nov 16 23:37:59 UTC 2022 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8370C CPU @ 2.80GHz: 
              speed         user         nice          sys         idle          irq
       #1  2793 MHz       5528 s          0 s        197 s       2654 s          0 s
       #2  2793 MHz       4751 s          0 s        201 s       3411 s          0 s
       
  Memory: 6.781219482421875 GB (3770.671875 MB free)
  Uptime: 842.32 sec
  Load Avg:  1.64  1.48  0.88
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, icelake-server)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 11 Dec 2022 - 2:1
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
| `["collect", "assoc", "basesize=1"]`                | 277.787 ms (5%) |         |  25.97 MiB (1%) |      306774 |
| `["collect", "assoc", "basesize=1024"]`             | 238.926 ms (5%) |         |   2.61 MiB (1%) |         456 |
| `["collect", "assoc", "basesize=32"]`               | 240.072 ms (5%) |         |   4.82 MiB (1%) |       11705 |
| `["collect", "seq"]`                                | 477.344 ms (5%) |         | 812.73 KiB (1%) |          11 |
| `["collect", "unordered", "basesize=1"]`            | 371.641 ms (5%) |         |  23.92 MiB (1%) |      413773 |
| `["collect", "unordered", "basesize=1024"]`         | 251.262 ms (5%) |         |   1.01 MiB (1%) |        1058 |
| `["collect", "unordered", "basesize=32"]`           | 262.610 ms (5%) |         |   1.59 MiB (1%) |       14957 |
| `["findfirst", "n=1000", "foldl"]`                  | 740.746 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 665.548 ms (5%) |         | 369.11 KiB (1%) |        5158 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 560.925 ms (5%) |         | 168.66 KiB (1%) |        2354 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 508.181 ms (5%) |         |  81.42 KiB (1%) |        1149 |
| `["findfirst", "n=400", "foldl"]`                   | 555.618 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 320.791 ms (5%) |         | 411.83 KiB (1%) |        5850 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 299.056 ms (5%) |         | 207.89 KiB (1%) |        2967 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 341.053 ms (5%) |         | 121.80 KiB (1%) |        1740 |
| `["findfirst", "n=500", "foldl"]`                   |  96.405 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 175.232 ms (5%) |         | 216.00 KiB (1%) |        2960 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 108.900 ms (5%) |         |  98.09 KiB (1%) |        1323 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 288.245 ms (5%) |         |  99.86 KiB (1%) |        1355 |
| `["overhead", "default"]`                           |  70.200 μs (5%) |         |  32.77 KiB (1%) |         419 |
| `["overhead", "stoppable=false"]`                   |  70.300 μs (5%) |         |  32.75 KiB (1%) |         418 |
| `["overhead", "stoppable=true"]`                    |  81.699 μs (5%) |         |  44.25 KiB (1%) |         610 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   3.733 ms (5%) |         | 728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   4.506 ms (5%) |         |   1.79 MiB (1%) |         215 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   4.122 ms (5%) |         |   1.42 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  14.346 ms (5%) |         |   1.32 MiB (1%) |        2727 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  23.134 ms (5%) |         |   1.39 MiB (1%) |       11564 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  20.728 ms (5%) |         |   1.38 MiB (1%) |        9573 |
| `["parallel_histogram", "seq"]`                     |   6.732 ms (5%) |         | 364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  41.218 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  20.605 ms (5%) |         |  736 bytes (1%) |          11 |
| `["splitby", "count", "foldl"]`                     |   2.375 ms (5%) |         |                 |             |
| `["splitby", "count", "man"]`                       |   1.528 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    |   1.151 ms (5%) |         |   1.09 KiB (1%) |          19 |
| `["sum", "random", "foldl"]`                        |  18.131 ms (5%) |         |                 |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   9.290 ms (5%) |         |  74.11 KiB (1%) |        1102 |
| `["sum", "random", "reduce", "basesize=256"]`       |   9.181 ms (5%) |         |  36.70 KiB (1%) |         545 |
| `["sum", "random", "reduce", "basesize=512"]`       |   9.130 ms (5%) |         |  18.05 KiB (1%) |         268 |
| `["sum", "uniform", "foldl"]`                       |  17.724 ms (5%) |         |                 |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   9.076 ms (5%) |         |  74.11 KiB (1%) |        1102 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   8.983 ms (5%) |         |  36.77 KiB (1%) |         547 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   8.920 ms (5%) |         |  18.03 KiB (1%) |         268 |
| `["sum", "valley", "foldl"]`                        |  18.137 ms (5%) |         |                 |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   9.303 ms (5%) |         |  74.08 KiB (1%) |        1101 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   9.214 ms (5%) |         |  36.70 KiB (1%) |         545 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   9.238 ms (5%) |         |  18.00 KiB (1%) |         267 |
| `["words", "nthreads=1"]`                           |  18.080 ms (5%) |         |  31.68 MiB (1%) |     1032144 |
| `["words", "nthreads=2"]`                           |  11.441 ms (5%) |         |  32.04 MiB (1%) |     1032180 |
| `["words", "nthreads=4"]`                           |  12.425 ms (5%) |         |  32.93 MiB (1%) |     1032352 |

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
  uname: Linux 5.15.0-1024-azure #30-Ubuntu SMP Wed Nov 16 23:37:59 UTC 2022 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8370C CPU @ 2.80GHz: 
              speed         user         nice          sys         idle          irq
       #1  2793 MHz       8019 s          0 s        261 s       3154 s          0 s
       #2  2793 MHz       7001 s          0 s        250 s       4169 s          0 s
       
  Memory: 6.781219482421875 GB (3732.5234375 MB free)
  Uptime: 1148.45 sec
  Load Avg:  1.71  1.58  1.1
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

