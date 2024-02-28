# Multi-thread benchmark result

* Pull request commit: [`89aaf425bad4b239027959ffd6f5b9aad6e78c90`](https://github.com/JuliaFolds/Transducers.jl/commit/89aaf425bad4b239027959ffd6f5b9aad6e78c90)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/243> (Update */Manifest.toml)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 28 Feb 2024 - 01:20
    - Baseline: 28 Feb 2024 - 01:25
* Package commits:
    - Target: 1fd9a6
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
| `["findfirst", "n=1000", "reduce", "basesize=256"]` |                1.23 (5%) :x: |                1.10 (1%) :x: |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` |                1.91 (5%) :x: |                1.82 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 0.94 (5%) :white_check_mark: | 0.98 (1%) :white_check_mark: |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |                1.63 (5%) :x: |                1.63 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 0.71 (5%) :white_check_mark: | 0.78 (1%) :white_check_mark: |
| `["parallel_histogram", "comm", "basesize=16384"]`  |                   1.05 (5%)  |                1.01 (1%) :x: |
| `["parallel_histogram", "comm", "basesize=4096"]`   | 0.93 (5%) :white_check_mark: | 0.97 (1%) :white_check_mark: |
| `["splitby", "count", "reduce"]`                    |                   1.01 (5%)  |                1.03 (1%) :x: |
| `["words", "nthreads=4"]`                           | 0.93 (5%) :white_check_mark: |                   0.99 (1%)  |

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
  uname: Linux 6.2.0-1019-azure #19~22.04.1-Ubuntu SMP Wed Jan 10 22:57:03 UTC 2024 x86_64 x86_64
  CPU: AMD EPYC 7763 64-Core Processor: 
              speed         user         nice          sys         idle          irq
       #1  2544 MHz       2620 s          0 s        151 s       5425 s          0 s
       #2  3227 MHz       2484 s          0 s        179 s       5527 s          0 s
       #3  3243 MHz       2238 s          0 s        162 s       5799 s          0 s
       #4  2445 MHz       2642 s          0 s        164 s       5391 s          0 s
       
  Memory: 15.60690689086914 GB (12399.09375 MB free)
  Uptime: 823.32 sec
  Load Avg:  1.72  1.51  0.88
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
  uname: Linux 6.2.0-1019-azure #19~22.04.1-Ubuntu SMP Wed Jan 10 22:57:03 UTC 2024 x86_64 x86_64
  CPU: AMD EPYC 7763 64-Core Processor: 
              speed         user         nice          sys         idle          irq
       #1  3243 MHz       3266 s          0 s        209 s       7598 s          0 s
       #2  2445 MHz       3811 s          0 s        224 s       7034 s          0 s
       #3  2445 MHz       3559 s          0 s        211 s       7308 s          0 s
       #4  2851 MHz       3915 s          0 s        205 s       6956 s          0 s
       
  Memory: 15.60690689086914 GB (12394.75 MB free)
  Uptime: 1111.87 sec
  Load Avg:  1.76  1.63  1.11
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, znver3)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 28 Feb 2024 - 1:20
* Package commit: 1fd9a6
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
| `["collect", "assoc", "basesize=1"]`                | 148.639 ms (5%) |         |   4.36 MiB (1%) |       32800 |
| `["collect", "assoc", "basesize=1024"]`             | 147.409 ms (5%) |         |   1.09 MiB (1%) |          53 |
| `["collect", "assoc", "basesize=32"]`               | 147.548 ms (5%) |         |   1.48 MiB (1%) |        1052 |
| `["collect", "seq"]`                                | 294.502 ms (5%) |         | 256.05 KiB (1%) |           2 |
| `["collect", "unordered", "basesize=1"]`            | 248.659 ms (5%) |         |  23.80 MiB (1%) |      409651 |
| `["collect", "unordered", "basesize=1024"]`         | 156.787 ms (5%) |         |   1.01 MiB (1%) |        1036 |
| `["collect", "unordered", "basesize=32"]`           | 163.303 ms (5%) |         |   1.60 MiB (1%) |       15218 |
| `["findfirst", "n=1000", "foldl"]`                  | 507.537 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 275.448 ms (5%) |         | 232.83 KiB (1%) |        3275 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 417.007 ms (5%) |         | 172.19 KiB (1%) |        2444 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 664.898 ms (5%) |         | 148.22 KiB (1%) |        2086 |
| `["findfirst", "n=400", "foldl"]`                   | 379.064 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 196.657 ms (5%) |         | 387.38 KiB (1%) |        5519 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 198.462 ms (5%) |         | 201.02 KiB (1%) |        2878 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 219.144 ms (5%) |         | 112.56 KiB (1%) |        1621 |
| `["findfirst", "n=500", "foldl"]`                   |  65.936 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 136.089 ms (5%) |         | 242.27 KiB (1%) |        3360 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 146.145 ms (5%) |         | 155.06 KiB (1%) |        2110 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  66.882 ms (5%) |         |  49.59 KiB (1%) |         671 |
| `["overhead", "default"]`                           |  52.609 μs (5%) |         |  32.73 KiB (1%) |         418 |
| `["overhead", "stoppable=false"]`                   |  51.837 μs (5%) |         |  32.75 KiB (1%) |         418 |
| `["overhead", "stoppable=true"]`                    |  58.540 μs (5%) |         |  44.28 KiB (1%) |         611 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   2.375 ms (5%) |         | 728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   2.923 ms (5%) |         |   1.79 MiB (1%) |         216 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   2.649 ms (5%) |         |   1.42 MiB (1%) |         118 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |   8.299 ms (5%) |         |   1.58 MiB (1%) |        2427 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  12.312 ms (5%) |         |   1.34 MiB (1%) |       10086 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  11.460 ms (5%) |         |   1.28 MiB (1%) |        7800 |
| `["parallel_histogram", "seq"]`                     |   4.238 ms (5%) |         | 364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  31.110 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  15.563 ms (5%) |         |  736 bytes (1%) |          11 |
| `["splitby", "count", "foldl"]`                     |   1.502 ms (5%) |         |                 |             |
| `["splitby", "count", "man"]`                       |   1.157 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    | 725.635 μs (5%) |         |   1.09 KiB (1%) |          19 |
| `["sum", "random", "foldl"]`                        |  11.038 ms (5%) |         |                 |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   5.655 ms (5%) |         |  73.95 KiB (1%) |        1097 |
| `["sum", "random", "reduce", "basesize=256"]`       |   5.588 ms (5%) |         |  36.67 KiB (1%) |         544 |
| `["sum", "random", "reduce", "basesize=512"]`       |   5.557 ms (5%) |         |  18.08 KiB (1%) |         269 |
| `["sum", "uniform", "foldl"]`                       |  10.867 ms (5%) |         |                 |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   5.582 ms (5%) |         |  74.11 KiB (1%) |        1102 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   5.527 ms (5%) |         |  36.77 KiB (1%) |         547 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   5.482 ms (5%) |         |  18.00 KiB (1%) |         267 |
| `["sum", "valley", "foldl"]`                        |  11.113 ms (5%) |         |                 |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   5.695 ms (5%) |         |  74.02 KiB (1%) |        1099 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   5.629 ms (5%) |         |  36.70 KiB (1%) |         545 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   5.604 ms (5%) |         |  18.03 KiB (1%) |         268 |
| `["words", "nthreads=1"]`                           |  14.279 ms (5%) |         |  31.60 MiB (1%) |     1029437 |
| `["words", "nthreads=2"]`                           |   9.842 ms (5%) |         |  32.32 MiB (1%) |     1029528 |
| `["words", "nthreads=4"]`                           |   9.917 ms (5%) |         |  32.76 MiB (1%) |     1029603 |

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
  uname: Linux 6.2.0-1019-azure #19~22.04.1-Ubuntu SMP Wed Jan 10 22:57:03 UTC 2024 x86_64 x86_64
  CPU: AMD EPYC 7763 64-Core Processor: 
              speed         user         nice          sys         idle          irq
       #1  2544 MHz       2620 s          0 s        151 s       5425 s          0 s
       #2  3227 MHz       2484 s          0 s        179 s       5527 s          0 s
       #3  3243 MHz       2238 s          0 s        162 s       5799 s          0 s
       #4  2445 MHz       2642 s          0 s        164 s       5391 s          0 s
       
  Memory: 15.60690689086914 GB (12399.09375 MB free)
  Uptime: 823.32 sec
  Load Avg:  1.72  1.51  0.88
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, znver3)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 28 Feb 2024 - 1:25
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
| `["collect", "assoc", "basesize=1"]`                | 148.540 ms (5%) |         |   4.36 MiB (1%) |       32800 |
| `["collect", "assoc", "basesize=1024"]`             | 147.430 ms (5%) |         |   1.09 MiB (1%) |          53 |
| `["collect", "assoc", "basesize=32"]`               | 147.518 ms (5%) |         |   1.48 MiB (1%) |        1052 |
| `["collect", "seq"]`                                | 294.563 ms (5%) |         | 256.05 KiB (1%) |           2 |
| `["collect", "unordered", "basesize=1"]`            | 243.036 ms (5%) |         |  23.85 MiB (1%) |      411282 |
| `["collect", "unordered", "basesize=1024"]`         | 156.145 ms (5%) |         |   1.02 MiB (1%) |        1347 |
| `["collect", "unordered", "basesize=32"]`           | 163.376 ms (5%) |         |   1.60 MiB (1%) |       15304 |
| `["findfirst", "n=1000", "foldl"]`                  | 506.707 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 275.915 ms (5%) |         | 232.58 KiB (1%) |        3267 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 339.395 ms (5%) |         | 157.20 KiB (1%) |        2193 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 347.251 ms (5%) |         |  81.33 KiB (1%) |        1146 |
| `["findfirst", "n=400", "foldl"]`                   | 379.771 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 196.256 ms (5%) |         | 385.75 KiB (1%) |        5479 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 198.751 ms (5%) |         | 200.86 KiB (1%) |        2873 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 220.115 ms (5%) |         | 112.59 KiB (1%) |        1622 |
| `["findfirst", "n=500", "foldl"]`                   |  65.130 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 144.263 ms (5%) |         | 248.08 KiB (1%) |        3438 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |  89.657 ms (5%) |         |  94.86 KiB (1%) |        1302 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  94.024 ms (5%) |         |  63.67 KiB (1%) |         866 |
| `["overhead", "default"]`                           |  52.047 μs (5%) |         |  32.73 KiB (1%) |         418 |
| `["overhead", "stoppable=false"]`                   |  52.529 μs (5%) |         |  32.75 KiB (1%) |         418 |
| `["overhead", "stoppable=true"]`                    |  55.994 μs (5%) |         |  44.22 KiB (1%) |         609 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   2.372 ms (5%) |         | 728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   2.924 ms (5%) |         |   1.79 MiB (1%) |         216 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   2.648 ms (5%) |         |   1.42 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |   7.905 ms (5%) |         |   1.56 MiB (1%) |        1765 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  13.198 ms (5%) |         |   1.38 MiB (1%) |       11529 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  11.482 ms (5%) |         |   1.28 MiB (1%) |        8283 |
| `["parallel_histogram", "seq"]`                     |   4.242 ms (5%) |         | 364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  31.105 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  15.585 ms (5%) |         |  736 bytes (1%) |          11 |
| `["splitby", "count", "foldl"]`                     |   1.480 ms (5%) |         |                 |             |
| `["splitby", "count", "man"]`                       |   1.132 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    | 721.007 μs (5%) |         |   1.06 KiB (1%) |          18 |
| `["sum", "random", "foldl"]`                        |  11.024 ms (5%) |         |                 |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   5.615 ms (5%) |         |  74.14 KiB (1%) |        1103 |
| `["sum", "random", "reduce", "basesize=256"]`       |   5.578 ms (5%) |         |  36.80 KiB (1%) |         548 |
| `["sum", "random", "reduce", "basesize=512"]`       |   5.545 ms (5%) |         |  18.11 KiB (1%) |         270 |
| `["sum", "uniform", "foldl"]`                       |  10.872 ms (5%) |         |                 |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   5.564 ms (5%) |         |  74.08 KiB (1%) |        1101 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   5.498 ms (5%) |         |  36.77 KiB (1%) |         547 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   5.461 ms (5%) |         |  18.03 KiB (1%) |         268 |
| `["sum", "valley", "foldl"]`                        |  11.112 ms (5%) |         |                 |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   5.691 ms (5%) |         |  74.05 KiB (1%) |        1100 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   5.633 ms (5%) |         |  36.73 KiB (1%) |         546 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   5.613 ms (5%) |         |  18.09 KiB (1%) |         270 |
| `["words", "nthreads=1"]`                           |  14.724 ms (5%) |         |  31.67 MiB (1%) |     1031763 |
| `["words", "nthreads=2"]`                           |  10.218 ms (5%) |         |  32.38 MiB (1%) |     1031839 |
| `["words", "nthreads=4"]`                           |  10.694 ms (5%) |         |  33.01 MiB (1%) |     1031991 |

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
  uname: Linux 6.2.0-1019-azure #19~22.04.1-Ubuntu SMP Wed Jan 10 22:57:03 UTC 2024 x86_64 x86_64
  CPU: AMD EPYC 7763 64-Core Processor: 
              speed         user         nice          sys         idle          irq
       #1  3243 MHz       3266 s          0 s        209 s       7598 s          0 s
       #2  2445 MHz       3811 s          0 s        224 s       7034 s          0 s
       #3  2445 MHz       3559 s          0 s        211 s       7308 s          0 s
       #4  2851 MHz       3915 s          0 s        205 s       6956 s          0 s
       
  Memory: 15.60690689086914 GB (12394.75 MB free)
  Uptime: 1111.87 sec
  Load Avg:  1.76  1.63  1.11
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
    BogoMIPS:                           4890.85
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

