# Multi-thread benchmark result

* Pull request commit: [`ec176f5af7d283bb0df106dd69e40c3cdc4d506e`](https://github.com/JuliaFolds/Transducers.jl/commit/ec176f5af7d283bb0df106dd69e40c3cdc4d506e)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/243> (Update */Manifest.toml)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 20 Sep 2024 - 01:49
    - Baseline: 20 Sep 2024 - 01:54
* Package commits:
    - Target: ca5641
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
| `["collect", "unordered", "basesize=1"]`            | 0.87 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 0.91 (5%) :white_check_mark: | 0.97 (1%) :white_check_mark: |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` |                1.28 (5%) :x: |                1.28 (1%) :x: |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  |                   0.97 (5%)  | 0.96 (1%) :white_check_mark: |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  |                   1.03 (5%)  |                1.02 (1%) :x: |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  |                   0.95 (5%)  | 0.96 (1%) :white_check_mark: |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |                1.54 (5%) :x: |                1.45 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 0.44 (5%) :white_check_mark: | 0.57 (1%) :white_check_mark: |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |                1.25 (5%) :x: |                1.13 (1%) :x: |
| `["parallel_histogram", "comm", "basesize=16384"]`  |                1.07 (5%) :x: |                   1.00 (1%)  |
| `["parallel_histogram", "comm", "basesize=4096"]`   |                   1.00 (5%)  | 0.98 (1%) :white_check_mark: |
| `["partition_length_maximum", "rand", "reduce"]`    |                   1.00 (5%)  | 0.96 (1%) :white_check_mark: |
| `["splitby", "count", "reduce"]`                    |                   1.01 (5%)  |                1.03 (1%) :x: |
| `["words", "nthreads=2"]`                           |                   1.00 (5%)  | 0.98 (1%) :white_check_mark: |

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
      Ubuntu 22.04.5 LTS
  uname: Linux 6.8.0-1014-azure #16~22.04.1-Ubuntu SMP Thu Aug 15 21:31:41 UTC 2024 x86_64 x86_64
  CPU: AMD EPYC 7763 64-Core Processor: 
              speed         user         nice          sys         idle          irq
       #1  3273 MHz       3062 s          0 s        170 s       3825 s          0 s
       #2  3243 MHz       2246 s          0 s        176 s       4636 s          0 s
       #3  2798 MHz       2271 s          0 s        233 s       4571 s          0 s
       #4  2445 MHz       2326 s          0 s        215 s       4516 s          0 s
       
  Memory: 15.61526870727539 GB (12340.23046875 MB free)
  Uptime: 709.99 sec
  Load Avg:  1.75  1.53  0.91
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
      Ubuntu 22.04.5 LTS
  uname: Linux 6.8.0-1014-azure #16~22.04.1-Ubuntu SMP Thu Aug 15 21:31:41 UTC 2024 x86_64 x86_64
  CPU: AMD EPYC 7763 64-Core Processor: 
              speed         user         nice          sys         idle          irq
       #1  3244 MHz       4254 s          0 s        249 s       5525 s          0 s
       #2  2445 MHz       3432 s          0 s        245 s       6354 s          0 s
       #3  2608 MHz       3403 s          0 s        316 s       6329 s          0 s
       #4  3171 MHz       3409 s          0 s        290 s       6330 s          0 s
       
  Memory: 15.61526870727539 GB (12292.6015625 MB free)
  Uptime: 1007.82 sec
  Load Avg:  1.77  1.64  1.13
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, znver3)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 20 Sep 2024 - 1:49
* Package commit: ca5641
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
| `["collect", "assoc", "basesize=1"]`                | 149.534 ms (5%) |         |   4.36 MiB (1%) |       32800 |
| `["collect", "assoc", "basesize=1024"]`             | 148.215 ms (5%) |         |   1.09 MiB (1%) |          54 |
| `["collect", "assoc", "basesize=32"]`               | 148.336 ms (5%) |         |   1.48 MiB (1%) |        1052 |
| `["collect", "seq"]`                                | 296.169 ms (5%) |         | 256.05 KiB (1%) |           2 |
| `["collect", "unordered", "basesize=1"]`            | 264.196 ms (5%) |         |  23.70 MiB (1%) |      406313 |
| `["collect", "unordered", "basesize=1024"]`         | 157.859 ms (5%) |         |   1.01 MiB (1%) |        1029 |
| `["collect", "unordered", "basesize=32"]`           | 170.255 ms (5%) |         |   1.60 MiB (1%) |       15345 |
| `["findfirst", "n=1000", "foldl"]`                  | 509.084 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 277.490 ms (5%) |         | 232.83 KiB (1%) |        3275 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 339.591 ms (5%) |         | 157.20 KiB (1%) |        2193 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 447.338 ms (5%) |         | 104.36 KiB (1%) |        1466 |
| `["findfirst", "n=400", "foldl"]`                   | 380.358 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 195.504 ms (5%) |         | 382.73 KiB (1%) |        5439 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 204.987 ms (5%) |         | 204.36 KiB (1%) |        2930 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 244.149 ms (5%) |         | 129.69 KiB (1%) |        1853 |
| `["findfirst", "n=500", "foldl"]`                   |  65.458 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 195.833 ms (5%) |         | 331.27 KiB (1%) |        4604 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |  62.416 ms (5%) |         |  77.08 KiB (1%) |        1047 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  84.623 ms (5%) |         |  55.91 KiB (1%) |         763 |
| `["overhead", "default"]`                           |  51.787 μs (5%) |         |  32.73 KiB (1%) |         418 |
| `["overhead", "stoppable=false"]`                   |  51.497 μs (5%) |         |  32.75 KiB (1%) |         418 |
| `["overhead", "stoppable=true"]`                    |  59.061 μs (5%) |         |  44.22 KiB (1%) |         609 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   2.398 ms (5%) |         | 728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   2.946 ms (5%) |         |   1.79 MiB (1%) |         216 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   2.685 ms (5%) |         |   1.42 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |   8.600 ms (5%) |         |   1.57 MiB (1%) |        2034 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  12.777 ms (5%) |         |   1.29 MiB (1%) |        8382 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  11.870 ms (5%) |         |   1.28 MiB (1%) |        7495 |
| `["parallel_histogram", "seq"]`                     |   4.257 ms (5%) |         | 364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  31.312 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  15.670 ms (5%) |         |  704 bytes (1%) |          10 |
| `["splitby", "count", "foldl"]`                     |   1.747 ms (5%) |         |                 |             |
| `["splitby", "count", "man"]`                       |   1.140 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    | 726.486 μs (5%) |         |   1.09 KiB (1%) |          19 |
| `["sum", "random", "foldl"]`                        |  11.051 ms (5%) |         |                 |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   5.670 ms (5%) |         |  74.02 KiB (1%) |        1099 |
| `["sum", "random", "reduce", "basesize=256"]`       |   5.579 ms (5%) |         |  36.73 KiB (1%) |         546 |
| `["sum", "random", "reduce", "basesize=512"]`       |   5.558 ms (5%) |         |  18.14 KiB (1%) |         271 |
| `["sum", "uniform", "foldl"]`                       |  10.937 ms (5%) |         |                 |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   5.582 ms (5%) |         |  74.14 KiB (1%) |        1103 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   5.536 ms (5%) |         |  36.77 KiB (1%) |         547 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   5.505 ms (5%) |         |  18.00 KiB (1%) |         267 |
| `["sum", "valley", "foldl"]`                        |  11.169 ms (5%) |         |                 |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   5.731 ms (5%) |         |  74.05 KiB (1%) |        1100 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   5.665 ms (5%) |         |  36.77 KiB (1%) |         547 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   5.642 ms (5%) |         |  18.03 KiB (1%) |         268 |
| `["words", "nthreads=1"]`                           |  14.084 ms (5%) |         |  31.77 MiB (1%) |     1034718 |
| `["words", "nthreads=2"]`                           |   9.369 ms (5%) |         |  32.12 MiB (1%) |     1034783 |
| `["words", "nthreads=4"]`                           |   9.739 ms (5%) |         |  32.84 MiB (1%) |     1034858 |

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
      Ubuntu 22.04.5 LTS
  uname: Linux 6.8.0-1014-azure #16~22.04.1-Ubuntu SMP Thu Aug 15 21:31:41 UTC 2024 x86_64 x86_64
  CPU: AMD EPYC 7763 64-Core Processor: 
              speed         user         nice          sys         idle          irq
       #1  3273 MHz       3062 s          0 s        170 s       3825 s          0 s
       #2  3243 MHz       2246 s          0 s        176 s       4636 s          0 s
       #3  2798 MHz       2271 s          0 s        233 s       4571 s          0 s
       #4  2445 MHz       2326 s          0 s        215 s       4516 s          0 s
       
  Memory: 15.61526870727539 GB (12340.23046875 MB free)
  Uptime: 709.99 sec
  Load Avg:  1.75  1.53  0.91
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, znver3)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 20 Sep 2024 - 1:54
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
| `["collect", "assoc", "basesize=1"]`                | 149.801 ms (5%) |         |   4.36 MiB (1%) |       32800 |
| `["collect", "assoc", "basesize=1024"]`             | 148.451 ms (5%) |         |   1.09 MiB (1%) |          53 |
| `["collect", "assoc", "basesize=32"]`               | 148.363 ms (5%) |         |   1.48 MiB (1%) |        1052 |
| `["collect", "seq"]`                                | 296.147 ms (5%) |         | 256.05 KiB (1%) |           2 |
| `["collect", "unordered", "basesize=1"]`            | 302.782 ms (5%) |         |  23.70 MiB (1%) |      406557 |
| `["collect", "unordered", "basesize=1024"]`         | 158.027 ms (5%) |         |   1.01 MiB (1%) |        1131 |
| `["collect", "unordered", "basesize=32"]`           | 170.725 ms (5%) |         |   1.60 MiB (1%) |       15321 |
| `["findfirst", "n=1000", "foldl"]`                  | 509.409 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 277.534 ms (5%) |         | 232.86 KiB (1%) |        3276 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 373.683 ms (5%) |         | 162.77 KiB (1%) |        2299 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 348.520 ms (5%) |         |  81.33 KiB (1%) |        1146 |
| `["findfirst", "n=400", "foldl"]`                   | 380.941 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 201.560 ms (5%) |         | 397.48 KiB (1%) |        5647 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 199.643 ms (5%) |         | 200.95 KiB (1%) |        2876 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 255.842 ms (5%) |         | 134.62 KiB (1%) |        1928 |
| `["findfirst", "n=500", "foldl"]`                   |  65.657 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 127.198 ms (5%) |         | 227.75 KiB (1%) |        3157 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 142.357 ms (5%) |         | 135.17 KiB (1%) |        1870 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  67.437 ms (5%) |         |  49.44 KiB (1%) |         664 |
| `["overhead", "default"]`                           |  51.547 μs (5%) |         |  32.73 KiB (1%) |         418 |
| `["overhead", "stoppable=false"]`                   |  49.283 μs (5%) |         |  32.75 KiB (1%) |         418 |
| `["overhead", "stoppable=true"]`                    |  57.909 μs (5%) |         |  44.25 KiB (1%) |         610 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   2.402 ms (5%) |         | 728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   2.954 ms (5%) |         |   1.79 MiB (1%) |         216 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   2.676 ms (5%) |         |   1.42 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |   8.013 ms (5%) |         |   1.56 MiB (1%) |        1803 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  12.753 ms (5%) |         |   1.32 MiB (1%) |        9342 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  11.703 ms (5%) |         |   1.28 MiB (1%) |        7708 |
| `["parallel_histogram", "seq"]`                     |   4.255 ms (5%) |         | 364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  31.312 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  15.676 ms (5%) |         |  736 bytes (1%) |          11 |
| `["splitby", "count", "foldl"]`                     |   1.745 ms (5%) |         |                 |             |
| `["splitby", "count", "man"]`                       |   1.140 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    | 718.889 μs (5%) |         |   1.06 KiB (1%) |          18 |
| `["sum", "random", "foldl"]`                        |  11.067 ms (5%) |         |                 |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   5.635 ms (5%) |         |  74.11 KiB (1%) |        1102 |
| `["sum", "random", "reduce", "basesize=256"]`       |   5.598 ms (5%) |         |  36.77 KiB (1%) |         547 |
| `["sum", "random", "reduce", "basesize=512"]`       |   5.557 ms (5%) |         |  18.08 KiB (1%) |         269 |
| `["sum", "uniform", "foldl"]`                       |  10.917 ms (5%) |         |                 |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   5.599 ms (5%) |         |  74.14 KiB (1%) |        1103 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   5.522 ms (5%) |         |  36.73 KiB (1%) |         546 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   5.492 ms (5%) |         |  18.00 KiB (1%) |         267 |
| `["sum", "valley", "foldl"]`                        |  11.167 ms (5%) |         |                 |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   5.720 ms (5%) |         |  74.05 KiB (1%) |        1100 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   5.667 ms (5%) |         |  36.73 KiB (1%) |         546 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   5.644 ms (5%) |         |  18.03 KiB (1%) |         268 |
| `["words", "nthreads=1"]`                           |  14.782 ms (5%) |         |  31.96 MiB (1%) |     1041753 |
| `["words", "nthreads=2"]`                           |   9.330 ms (5%) |         |  32.67 MiB (1%) |     1041833 |
| `["words", "nthreads=4"]`                           |   9.656 ms (5%) |         |  33.12 MiB (1%) |     1041899 |

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
      Ubuntu 22.04.5 LTS
  uname: Linux 6.8.0-1014-azure #16~22.04.1-Ubuntu SMP Thu Aug 15 21:31:41 UTC 2024 x86_64 x86_64
  CPU: AMD EPYC 7763 64-Core Processor: 
              speed         user         nice          sys         idle          irq
       #1  3244 MHz       4254 s          0 s        249 s       5525 s          0 s
       #2  2445 MHz       3432 s          0 s        245 s       6354 s          0 s
       #3  2608 MHz       3403 s          0 s        316 s       6329 s          0 s
       #4  3171 MHz       3409 s          0 s        290 s       6330 s          0 s
       
  Memory: 15.61526870727539 GB (12292.6015625 MB free)
  Uptime: 1007.82 sec
  Load Avg:  1.77  1.64  1.13
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

    Architecture:                         x86_64
    CPU op-mode(s):                       32-bit, 64-bit
    Address sizes:                        48 bits physical, 48 bits virtual
    Byte Order:                           Little Endian
    CPU(s):                               4
    On-line CPU(s) list:                  0-3
    Vendor ID:                            AuthenticAMD
    Model name:                           AMD EPYC 7763 64-Core Processor
    CPU family:                           25
    Model:                                1
    Thread(s) per core:                   2
    Core(s) per socket:                   2
    Socket(s):                            1
    Stepping:                             1
    BogoMIPS:                             4890.85
    Flags:                                fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush mmx fxsr sse sse2 ht syscall nx mmxext fxsr_opt pdpe1gb rdtscp lm constant_tsc rep_good nopl tsc_reliable nonstop_tsc cpuid extd_apicid aperfmperf pni pclmulqdq ssse3 fma cx16 pcid sse4_1 sse4_2 movbe popcnt aes xsave avx f16c rdrand hypervisor lahf_lm cmp_legacy svm cr8_legacy abm sse4a misalignsse 3dnowprefetch osvw topoext vmmcall fsgsbase bmi1 avx2 smep bmi2 erms invpcid rdseed adx smap clflushopt clwb sha_ni xsaveopt xsavec xgetbv1 xsaves user_shstk clzero xsaveerptr rdpru arat npt nrip_save tsc_scale vmcb_clean flushbyasid decodeassists pausefilter pfthreshold v_vmsave_vmload umip vaes vpclmulqdq rdpid fsrm
    Virtualization:                       AMD-V
    Hypervisor vendor:                    Microsoft
    Virtualization type:                  full
    L1d cache:                            64 KiB (2 instances)
    L1i cache:                            64 KiB (2 instances)
    L2 cache:                             1 MiB (2 instances)
    L3 cache:                             32 MiB (1 instance)
    NUMA node(s):                         1
    NUMA node0 CPU(s):                    0-3
    Vulnerability Gather data sampling:   Not affected
    Vulnerability Itlb multihit:          Not affected
    Vulnerability L1tf:                   Not affected
    Vulnerability Mds:                    Not affected
    Vulnerability Meltdown:               Not affected
    Vulnerability Mmio stale data:        Not affected
    Vulnerability Reg file data sampling: Not affected
    Vulnerability Retbleed:               Not affected
    Vulnerability Spec rstack overflow:   Vulnerable: Safe RET, no microcode
    Vulnerability Spec store bypass:      Vulnerable
    Vulnerability Spectre v1:             Mitigation; usercopy/swapgs barriers and __user pointer sanitization
    Vulnerability Spectre v2:             Mitigation; Retpolines; STIBP disabled; RSB filling; PBRSB-eIBRS Not affected; BHI Not affected
    Vulnerability Srbds:                  Not affected
    Vulnerability Tsx async abort:        Not affected
    

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

