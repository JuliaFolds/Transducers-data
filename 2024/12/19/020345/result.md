# Multi-thread benchmark result

* Pull request commit: [`36aa5a68f71d93b57e8728de835f4f2ddcc3d240`](https://github.com/JuliaFolds/Transducers.jl/commit/36aa5a68f71d93b57e8728de835f4f2ddcc3d240)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/243> (Update */Manifest.toml)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 19 Dec 2024 - 01:58
    - Baseline: 19 Dec 2024 - 02:03
* Package commits:
    - Target: 945d65
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
| `["findfirst", "n=1000", "reduce", "basesize=128"]` |                1.25 (5%) :x: |                1.22 (1%) :x: |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` |                1.23 (5%) :x: |                1.10 (1%) :x: |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  |                   0.98 (5%)  | 0.98 (1%) :white_check_mark: |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 0.82 (5%) :white_check_mark: | 0.82 (1%) :white_check_mark: |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |                1.09 (5%) :x: |                1.12 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 0.39 (5%) :white_check_mark: | 0.52 (1%) :white_check_mark: |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |                   0.98 (5%)  | 0.87 (1%) :white_check_mark: |
| `["parallel_histogram", "comm", "basesize=4096"]`   |                   0.99 (5%)  |                1.01 (1%) :x: |
| `["splitby", "count", "foldl"]`                     |                1.12 (5%) :x: |                   1.00 (1%)  |
| `["splitby", "count", "reduce"]`                    | 0.84 (5%) :white_check_mark: | 0.97 (1%) :white_check_mark: |
| `["words", "nthreads=2"]`                           |                1.09 (5%) :x: |                   1.00 (1%)  |
| `["words", "nthreads=4"]`                           |                1.09 (5%) :x: |                   1.00 (1%)  |

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
      Ubuntu 24.04.1 LTS
  uname: Linux 6.8.0-1017-azure #20-Ubuntu SMP Tue Oct 22 03:43:13 UTC 2024 x86_64 x86_64
  CPU: AMD EPYC 7763 64-Core Processor: 
              speed         user         nice          sys         idle          irq
       #1  3242 MHz       2143 s          0 s        177 s       4730 s          0 s
       #2  3233 MHz       3269 s          0 s        178 s       3518 s          0 s
       #3  3246 MHz       2032 s          0 s        198 s       4756 s          0 s
       #4  3243 MHz       2550 s          0 s        237 s       4212 s          0 s
       
  Memory: 15.615280151367188 GB (8568.53515625 MB free)
  Uptime: 708.67 sec
  Load Avg:  1.64  1.47  0.88
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
      Ubuntu 24.04.1 LTS
  uname: Linux 6.8.0-1017-azure #20-Ubuntu SMP Tue Oct 22 03:43:13 UTC 2024 x86_64 x86_64
  CPU: AMD EPYC 7763 64-Core Processor: 
              speed         user         nice          sys         idle          irq
       #1  3245 MHz       3296 s          0 s        240 s       6470 s          0 s
       #2  3245 MHz       4373 s          0 s        243 s       5305 s          0 s
       #3  3249 MHz       3283 s          0 s        263 s       6399 s          0 s
       #4  3242 MHz       3649 s          0 s        317 s       5993 s          0 s
       
  Memory: 15.615280151367188 GB (8623.59765625 MB free)
  Uptime: 1004.97 sec
  Load Avg:  1.75  1.64  1.12
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, znver3)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 19 Dec 2024 - 1:58
* Package commit: 945d65
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
| `["collect", "assoc", "basesize=1"]`                | 149.793 ms (5%) |         |   4.36 MiB (1%) |       32800 |
| `["collect", "assoc", "basesize=1024"]`             | 148.111 ms (5%) |         |   1.09 MiB (1%) |          53 |
| `["collect", "assoc", "basesize=32"]`               | 148.289 ms (5%) |         |   1.48 MiB (1%) |        1052 |
| `["collect", "seq"]`                                | 295.940 ms (5%) |         | 256.05 KiB (1%) |           2 |
| `["collect", "unordered", "basesize=1"]`            | 249.516 ms (5%) |         |  23.71 MiB (1%) |      406798 |
| `["collect", "unordered", "basesize=1024"]`         | 158.090 ms (5%) |         |   1.01 MiB (1%) |        1024 |
| `["collect", "unordered", "basesize=32"]`           | 169.437 ms (5%) |         |   1.60 MiB (1%) |       15281 |
| `["findfirst", "n=1000", "foldl"]`                  | 509.382 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 348.142 ms (5%) |         | 284.94 KiB (1%) |        3997 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 418.974 ms (5%) |         | 172.27 KiB (1%) |        2444 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 349.125 ms (5%) |         |  81.33 KiB (1%) |        1146 |
| `["findfirst", "n=400", "foldl"]`                   | 380.968 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 196.636 ms (5%) |         | 382.48 KiB (1%) |        5449 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 199.803 ms (5%) |         | 200.86 KiB (1%) |        2873 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 221.461 ms (5%) |         | 112.62 KiB (1%) |        1623 |
| `["findfirst", "n=500", "foldl"]`                   |  65.743 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 109.675 ms (5%) |         | 207.28 KiB (1%) |        2841 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |  59.848 ms (5%) |         |  71.38 KiB (1%) |         970 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  85.470 ms (5%) |         |  56.83 KiB (1%) |         778 |
| `["overhead", "default"]`                           |  50.614 μs (5%) |         |  32.70 KiB (1%) |         417 |
| `["overhead", "stoppable=false"]`                   |  51.115 μs (5%) |         |  32.75 KiB (1%) |         418 |
| `["overhead", "stoppable=true"]`                    |  57.387 μs (5%) |         |  44.25 KiB (1%) |         610 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   2.387 ms (5%) |         | 728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   2.948 ms (5%) |         |   1.79 MiB (1%) |         216 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   2.669 ms (5%) |         |   1.42 MiB (1%) |         118 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |   8.326 ms (5%) |         |   1.58 MiB (1%) |        2488 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  12.319 ms (5%) |         |   1.32 MiB (1%) |        9337 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  11.169 ms (5%) |         |   1.28 MiB (1%) |        6996 |
| `["parallel_histogram", "seq"]`                     |   4.254 ms (5%) |         | 364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  31.321 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  15.720 ms (5%) |         |  736 bytes (1%) |          11 |
| `["splitby", "count", "foldl"]`                     |   1.743 ms (5%) |         |                 |             |
| `["splitby", "count", "man"]`                       |   1.141 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    | 718.688 μs (5%) |         |   1.06 KiB (1%) |          18 |
| `["sum", "random", "foldl"]`                        |  11.016 ms (5%) |         |                 |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   5.624 ms (5%) |         |  74.08 KiB (1%) |        1101 |
| `["sum", "random", "reduce", "basesize=256"]`       |   5.567 ms (5%) |         |  36.64 KiB (1%) |         543 |
| `["sum", "random", "reduce", "basesize=512"]`       |   5.541 ms (5%) |         |  18.05 KiB (1%) |         268 |
| `["sum", "uniform", "foldl"]`                       |  10.917 ms (5%) |         |                 |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   5.619 ms (5%) |         |  74.08 KiB (1%) |        1101 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   5.546 ms (5%) |         |  36.70 KiB (1%) |         545 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   5.511 ms (5%) |         |  17.97 KiB (1%) |         266 |
| `["sum", "valley", "foldl"]`                        |  11.170 ms (5%) |         |                 |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   5.722 ms (5%) |         |  74.14 KiB (1%) |        1103 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   5.662 ms (5%) |         |  36.73 KiB (1%) |         546 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   5.634 ms (5%) |         |  18.06 KiB (1%) |         269 |
| `["words", "nthreads=1"]`                           |  14.378 ms (5%) |         |  31.67 MiB (1%) |     1031999 |
| `["words", "nthreads=2"]`                           |  10.234 ms (5%) |         |  32.38 MiB (1%) |     1032072 |
| `["words", "nthreads=4"]`                           |  10.876 ms (5%) |         |  33.01 MiB (1%) |     1032211 |

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
      Ubuntu 24.04.1 LTS
  uname: Linux 6.8.0-1017-azure #20-Ubuntu SMP Tue Oct 22 03:43:13 UTC 2024 x86_64 x86_64
  CPU: AMD EPYC 7763 64-Core Processor: 
              speed         user         nice          sys         idle          irq
       #1  3242 MHz       2143 s          0 s        177 s       4730 s          0 s
       #2  3233 MHz       3269 s          0 s        178 s       3518 s          0 s
       #3  3246 MHz       2032 s          0 s        198 s       4756 s          0 s
       #4  3243 MHz       2550 s          0 s        237 s       4212 s          0 s
       
  Memory: 15.615280151367188 GB (8568.53515625 MB free)
  Uptime: 708.67 sec
  Load Avg:  1.64  1.47  0.88
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, znver3)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 19 Dec 2024 - 2:3
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
| `["collect", "assoc", "basesize=1"]`                | 149.800 ms (5%) |         |   4.36 MiB (1%) |       32800 |
| `["collect", "assoc", "basesize=1024"]`             | 148.369 ms (5%) |         |   1.09 MiB (1%) |          53 |
| `["collect", "assoc", "basesize=32"]`               | 148.210 ms (5%) |         |   1.48 MiB (1%) |        1052 |
| `["collect", "seq"]`                                | 296.006 ms (5%) |         | 256.05 KiB (1%) |           2 |
| `["collect", "unordered", "basesize=1"]`            | 247.462 ms (5%) |         |  23.70 MiB (1%) |      406388 |
| `["collect", "unordered", "basesize=1024"]`         | 158.472 ms (5%) |         |   1.01 MiB (1%) |        1083 |
| `["collect", "unordered", "basesize=32"]`           | 170.030 ms (5%) |         |   1.60 MiB (1%) |       15268 |
| `["findfirst", "n=1000", "foldl"]`                  | 509.243 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 278.097 ms (5%) |         | 232.86 KiB (1%) |        3276 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 341.345 ms (5%) |         | 157.20 KiB (1%) |        2193 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 348.830 ms (5%) |         |  81.33 KiB (1%) |        1146 |
| `["findfirst", "n=400", "foldl"]`                   | 380.949 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 200.224 ms (5%) |         | 391.67 KiB (1%) |        5579 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 199.790 ms (5%) |         | 200.86 KiB (1%) |        2873 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 269.529 ms (5%) |         | 137.97 KiB (1%) |        1980 |
| `["findfirst", "n=500", "foldl"]`                   |  65.806 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 100.519 ms (5%) |         | 184.27 KiB (1%) |        2552 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 154.391 ms (5%) |         | 137.09 KiB (1%) |        1907 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  89.147 ms (5%) |         |  56.84 KiB (1%) |         779 |
| `["overhead", "default"]`                           |  50.093 μs (5%) |         |  32.73 KiB (1%) |         418 |
| `["overhead", "stoppable=false"]`                   |  51.225 μs (5%) |         |  32.75 KiB (1%) |         418 |
| `["overhead", "stoppable=true"]`                    |  57.538 μs (5%) |         |  44.25 KiB (1%) |         610 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   2.396 ms (5%) |         | 728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   3.001 ms (5%) |         |   2.05 MiB (1%) |         222 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   2.677 ms (5%) |         |   1.42 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |   8.443 ms (5%) |         |   1.57 MiB (1%) |        2258 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  12.398 ms (5%) |         |   1.30 MiB (1%) |        8882 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  11.420 ms (5%) |         |   1.27 MiB (1%) |        6352 |
| `["parallel_histogram", "seq"]`                     |   4.258 ms (5%) |         | 364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  31.293 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  15.672 ms (5%) |         |  736 bytes (1%) |          11 |
| `["splitby", "count", "foldl"]`                     |   1.552 ms (5%) |         |                 |             |
| `["splitby", "count", "man"]`                       |   1.165 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    | 859.449 μs (5%) |         |   1.09 KiB (1%) |          19 |
| `["sum", "random", "foldl"]`                        |  11.097 ms (5%) |         |                 |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   5.660 ms (5%) |         |  74.11 KiB (1%) |        1102 |
| `["sum", "random", "reduce", "basesize=256"]`       |   5.624 ms (5%) |         |  36.67 KiB (1%) |         544 |
| `["sum", "random", "reduce", "basesize=512"]`       |   5.589 ms (5%) |         |  18.05 KiB (1%) |         268 |
| `["sum", "uniform", "foldl"]`                       |  10.915 ms (5%) |         |                 |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   5.577 ms (5%) |         |  74.17 KiB (1%) |        1104 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   5.524 ms (5%) |         |  36.70 KiB (1%) |         545 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   5.494 ms (5%) |         |  18.00 KiB (1%) |         267 |
| `["sum", "valley", "foldl"]`                        |  11.162 ms (5%) |         |                 |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   5.724 ms (5%) |         |  74.11 KiB (1%) |        1102 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   5.663 ms (5%) |         |  36.70 KiB (1%) |         545 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   5.625 ms (5%) |         |  18.03 KiB (1%) |         268 |
| `["words", "nthreads=1"]`                           |  14.515 ms (5%) |         |  31.78 MiB (1%) |     1035767 |
| `["words", "nthreads=2"]`                           |   9.414 ms (5%) |         |  32.49 MiB (1%) |     1035873 |
| `["words", "nthreads=4"]`                           |   9.971 ms (5%) |         |  33.12 MiB (1%) |     1036015 |

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
      Ubuntu 24.04.1 LTS
  uname: Linux 6.8.0-1017-azure #20-Ubuntu SMP Tue Oct 22 03:43:13 UTC 2024 x86_64 x86_64
  CPU: AMD EPYC 7763 64-Core Processor: 
              speed         user         nice          sys         idle          irq
       #1  3245 MHz       3296 s          0 s        240 s       6470 s          0 s
       #2  3245 MHz       4373 s          0 s        243 s       5305 s          0 s
       #3  3249 MHz       3283 s          0 s        263 s       6399 s          0 s
       #4  3242 MHz       3649 s          0 s        317 s       5993 s          0 s
       
  Memory: 15.615280151367188 GB (8623.59765625 MB free)
  Uptime: 1004.97 sec
  Load Avg:  1.75  1.64  1.12
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
    BogoMIPS:                             4890.86
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

