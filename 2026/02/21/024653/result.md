# Multi-thread benchmark result

* Pull request commit: [`08237149c082aad248bdfe18aa0a5d003a37820d`](https://github.com/JuliaFolds/Transducers.jl/commit/08237149c082aad248bdfe18aa0a5d003a37820d)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/243> (Update */Manifest.toml)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 21 Feb 2026 - 02:41
    - Baseline: 21 Feb 2026 - 02:46
* Package commits:
    - Target: 8ff9346
    - Baseline: 2a51f8d
* Julia commits:
    - Target: 742b9ab
    - Baseline: 742b9ab
* Julia command flags:
    - Target: None
    - Baseline: None
* Environment variables:
    - Target: `JULIA_NUM_THREADS => 2`
    - Baseline: `JULIA_NUM_THREADS => 2`

## Results
A ratio greater than `1.0` denotes a possible regression (marked with :x:), while a ratio less
than `1.0` denotes a possible improvement (marked with :white_check_mark:). Brackets display [tolerances](https://juliaci.github.io/BenchmarkTools.jl/stable/manual/#Benchmark-Parameters) for the benchmark estimates. Only significant results - results
that indicate possible regressions or improvements - are shown below (thus, an empty table means that all
benchmark results remained invariant between builds).

| ID                                                  | time ratio                   | memory ratio                 |
|-----------------------------------------------------|------------------------------|------------------------------|
| `["findfirst", "n=1000", "reduce", "basesize=256"]` |                   0.99 (5%)  | 0.97 (1%) :white_check_mark: |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` |                   1.00 (5%)  | 0.96 (1%) :white_check_mark: |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  |                   0.98 (5%)  | 0.98 (1%) :white_check_mark: |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 0.78 (5%) :white_check_mark: | 0.80 (1%) :white_check_mark: |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |                1.58 (5%) :x: |                1.38 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 0.89 (5%) :white_check_mark: | 0.94 (1%) :white_check_mark: |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |                1.12 (5%) :x: |                1.14 (1%) :x: |
| `["parallel_histogram", "comm", "basesize=16384"]`  |                   0.96 (5%)  | 0.98 (1%) :white_check_mark: |
| `["parallel_histogram", "comm", "basesize=4096"]`   |                   0.98 (5%)  |                1.02 (1%) :x: |
| `["splitby", "count", "reduce"]`                    |                1.14 (5%) :x: |                1.06 (1%) :x: |
| `["words", "nthreads=1"]`                           | 0.95 (5%) :white_check_mark: |                   0.99 (1%)  |
| `["words", "nthreads=2"]`                           |                1.19 (5%) :x: |                   1.00 (1%)  |
| `["words", "nthreads=4"]`                           |                1.14 (5%) :x: |                   0.99 (1%)  |

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
      Ubuntu 24.04.3 LTS
  uname: Linux 6.11.0-1018-azure #18~24.04.1-Ubuntu SMP Sat Jun 28 04:46:03 UTC 2025 x86_64 x86_64
  CPU: AMD EPYC 7763 64-Core Processor: 
              speed         user         nice          sys         idle          irq
       #1  3233 MHz       2733 s          0 s        149 s       3711 s          0 s
       #2  3238 MHz       2175 s          0 s        181 s       4234 s          0 s
       #3  3241 MHz       2739 s          0 s        185 s       3661 s          0 s
       #4  3242 MHz       2255 s          0 s        201 s       4130 s          0 s
       
  Memory: 15.620063781738281 GB (11931.15625 MB free)
  Uptime: 663.12 sec
  Load Avg:  1.69  1.44  0.84
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
      Ubuntu 24.04.3 LTS
  uname: Linux 6.11.0-1018-azure #18~24.04.1-Ubuntu SMP Sat Jun 28 04:46:03 UTC 2025 x86_64 x86_64
  CPU: AMD EPYC 7763 64-Core Processor: 
              speed         user         nice          sys         idle          irq
       #1  3244 MHz       3895 s          0 s        219 s       5584 s          0 s
       #2  3317 MHz       3522 s          0 s        271 s       5903 s          0 s
       #3  3236 MHz       3870 s          0 s        244 s       5578 s          0 s
       #4  3240 MHz       3419 s          0 s        265 s       6009 s          0 s
       
  Memory: 15.620063781738281 GB (11915.671875 MB free)
  Uptime: 974.15 sec
  Load Avg:  1.64  1.58  1.08
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, znver3)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 21 Feb 2026 - 02:41
* Package commit: 8ff9346
* Julia commit: 742b9ab
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
| `["collect", "assoc", "basesize=1"]`                | 149.809 ms (5%) |         |   4.36 MiB (1%) |       32800 |
| `["collect", "assoc", "basesize=1024"]`             | 148.172 ms (5%) |         |   1.09 MiB (1%) |          54 |
| `["collect", "assoc", "basesize=32"]`               | 148.303 ms (5%) |         |   1.48 MiB (1%) |        1052 |
| `["collect", "seq"]`                                | 296.033 ms (5%) |         | 256.05 KiB (1%) |           2 |
| `["collect", "unordered", "basesize=1"]`            | 246.346 ms (5%) |         |  23.68 MiB (1%) |      405851 |
| `["collect", "unordered", "basesize=1024"]`         | 158.175 ms (5%) |         |   1.01 MiB (1%) |        1002 |
| `["collect", "unordered", "basesize=32"]`           | 168.444 ms (5%) |         |   1.60 MiB (1%) |       15327 |
| `["findfirst", "n=1000", "foldl"]`                  | 510.185 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 277.861 ms (5%) |         | 232.83 KiB (1%) |        3275 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 396.341 ms (5%) |         | 167.67 KiB (1%) |        2366 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 793.021 ms (5%) |         | 161.47 KiB (1%) |        2294 |
| `["findfirst", "n=400", "foldl"]`                   | 381.766 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 196.812 ms (5%) |         | 383.12 KiB (1%) |        5454 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 198.225 ms (5%) |         | 200.19 KiB (1%) |        2866 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 205.071 ms (5%) |         | 110.66 KiB (1%) |        1588 |
| `["findfirst", "n=500", "foldl"]`                   |  66.280 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 110.562 ms (5%) |         | 194.66 KiB (1%) |        2705 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |  62.080 ms (5%) |         |  78.47 KiB (1%) |        1069 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  94.510 ms (5%) |         |  63.66 KiB (1%) |         865 |
| `["overhead", "default"]`                           |  50.113 μs (5%) |         |  32.73 KiB (1%) |         418 |
| `["overhead", "stoppable=false"]`                   |  50.705 μs (5%) |         |  32.75 KiB (1%) |         418 |
| `["overhead", "stoppable=true"]`                    |  57.598 μs (5%) |         |  44.25 KiB (1%) |         610 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   2.397 ms (5%) |         | 728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   2.946 ms (5%) |         |   1.79 MiB (1%) |         216 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   2.687 ms (5%) |         |   1.42 MiB (1%) |         118 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |   7.616 ms (5%) |         |   1.54 MiB (1%) |         982 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  12.769 ms (5%) |         |   1.36 MiB (1%) |       10739 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  11.311 ms (5%) |         |   1.29 MiB (1%) |        8018 |
| `["parallel_histogram", "seq"]`                     |   4.258 ms (5%) |         | 364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  31.311 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  15.696 ms (5%) |         |  736 bytes (1%) |          11 |
| `["splitby", "count", "foldl"]`                     |   1.506 ms (5%) |         |                 |             |
| `["splitby", "count", "man"]`                       |   1.165 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    | 826.623 μs (5%) |         |   1.12 KiB (1%) |          20 |
| `["sum", "random", "foldl"]`                        |  11.100 ms (5%) |         |                 |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   5.658 ms (5%) |         |  74.06 KiB (1%) |        1100 |
| `["sum", "random", "reduce", "basesize=256"]`       |   5.609 ms (5%) |         |  36.75 KiB (1%) |         546 |
| `["sum", "random", "reduce", "basesize=512"]`       |   5.583 ms (5%) |         |  18.11 KiB (1%) |         270 |
| `["sum", "uniform", "foldl"]`                       |  10.955 ms (5%) |         |                 |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   5.597 ms (5%) |         |  74.25 KiB (1%) |        1106 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   5.540 ms (5%) |         |  36.78 KiB (1%) |         547 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   5.515 ms (5%) |         |  18.05 KiB (1%) |         268 |
| `["sum", "valley", "foldl"]`                        |  11.175 ms (5%) |         |                 |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   5.716 ms (5%) |         |  74.12 KiB (1%) |        1102 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   5.671 ms (5%) |         |  36.78 KiB (1%) |         547 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   5.644 ms (5%) |         |  18.08 KiB (1%) |         269 |
| `["words", "nthreads=1"]`                           |  14.176 ms (5%) |         |  31.39 MiB (1%) |     1022697 |
| `["words", "nthreads=2"]`                           |  10.511 ms (5%) |         |  32.10 MiB (1%) |     1022770 |
| `["words", "nthreads=4"]`                           |  10.739 ms (5%) |         |  32.55 MiB (1%) |     1022861 |

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
      Ubuntu 24.04.3 LTS
  uname: Linux 6.11.0-1018-azure #18~24.04.1-Ubuntu SMP Sat Jun 28 04:46:03 UTC 2025 x86_64 x86_64
  CPU: AMD EPYC 7763 64-Core Processor: 
              speed         user         nice          sys         idle          irq
       #1  3233 MHz       2733 s          0 s        149 s       3711 s          0 s
       #2  3238 MHz       2175 s          0 s        181 s       4234 s          0 s
       #3  3241 MHz       2739 s          0 s        185 s       3661 s          0 s
       #4  3242 MHz       2255 s          0 s        201 s       4130 s          0 s
       
  Memory: 15.620063781738281 GB (11931.15625 MB free)
  Uptime: 663.12 sec
  Load Avg:  1.69  1.44  0.84
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, znver3)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 21 Feb 2026 - 02:46
* Package commit: 2a51f8d
* Julia commit: 742b9ab
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
| `["collect", "assoc", "basesize=1"]`                | 149.861 ms (5%) |         |   4.36 MiB (1%) |       32800 |
| `["collect", "assoc", "basesize=1024"]`             | 148.387 ms (5%) |         |   1.09 MiB (1%) |          53 |
| `["collect", "assoc", "basesize=32"]`               | 148.320 ms (5%) |         |   1.48 MiB (1%) |        1052 |
| `["collect", "seq"]`                                | 296.106 ms (5%) |         | 256.05 KiB (1%) |           2 |
| `["collect", "unordered", "basesize=1"]`            | 250.616 ms (5%) |         |  23.66 MiB (1%) |      405293 |
| `["collect", "unordered", "basesize=1024"]`         | 157.977 ms (5%) |         |   1.01 MiB (1%) |        1156 |
| `["collect", "unordered", "basesize=32"]`           | 169.615 ms (5%) |         |   1.60 MiB (1%) |       15327 |
| `["findfirst", "n=1000", "foldl"]`                  | 509.622 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 277.595 ms (5%) |         | 232.86 KiB (1%) |        3276 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 399.211 ms (5%) |         | 173.20 KiB (1%) |        2435 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 796.409 ms (5%) |         | 168.34 KiB (1%) |        2377 |
| `["findfirst", "n=400", "foldl"]`                   | 381.638 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 200.344 ms (5%) |         | 389.70 KiB (1%) |        5547 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 199.610 ms (5%) |         | 200.67 KiB (1%) |        2867 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 264.320 ms (5%) |         | 137.97 KiB (1%) |        1980 |
| `["findfirst", "n=500", "foldl"]`                   |  66.274 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |  70.185 ms (5%) |         | 140.84 KiB (1%) |        1935 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |  69.875 ms (5%) |         |  83.92 KiB (1%) |        1135 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  84.567 ms (5%) |         |  55.81 KiB (1%) |         756 |
| `["overhead", "default"]`                           |  52.167 μs (5%) |         |  32.73 KiB (1%) |         418 |
| `["overhead", "stoppable=false"]`                   |  50.715 μs (5%) |         |  32.75 KiB (1%) |         418 |
| `["overhead", "stoppable=true"]`                    |  56.576 μs (5%) |         |  44.25 KiB (1%) |         610 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   2.398 ms (5%) |         | 728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   2.953 ms (5%) |         |   1.79 MiB (1%) |         216 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   2.672 ms (5%) |         |   1.42 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |   7.969 ms (5%) |         |   1.56 MiB (1%) |        1787 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  13.029 ms (5%) |         |   1.33 MiB (1%) |        9894 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  11.582 ms (5%) |         |   1.28 MiB (1%) |        7675 |
| `["parallel_histogram", "seq"]`                     |   4.257 ms (5%) |         | 364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  31.313 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  15.692 ms (5%) |         |  736 bytes (1%) |          11 |
| `["splitby", "count", "foldl"]`                     |   1.495 ms (5%) |         |                 |             |
| `["splitby", "count", "man"]`                       |   1.166 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    | 723.009 μs (5%) |         |   1.06 KiB (1%) |          18 |
| `["sum", "random", "foldl"]`                        |  11.065 ms (5%) |         |                 |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   5.630 ms (5%) |         |  74.19 KiB (1%) |        1104 |
| `["sum", "random", "reduce", "basesize=256"]`       |   5.607 ms (5%) |         |  36.66 KiB (1%) |         543 |
| `["sum", "random", "reduce", "basesize=512"]`       |   5.565 ms (5%) |         |  18.08 KiB (1%) |         269 |
| `["sum", "uniform", "foldl"]`                       |  10.926 ms (5%) |         |                 |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   5.594 ms (5%) |         |  74.12 KiB (1%) |        1102 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   5.534 ms (5%) |         |  36.78 KiB (1%) |         547 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   5.497 ms (5%) |         |  18.05 KiB (1%) |         268 |
| `["sum", "valley", "foldl"]`                        |  11.166 ms (5%) |         |                 |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   5.728 ms (5%) |         |  74.12 KiB (1%) |        1102 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   5.666 ms (5%) |         |  36.75 KiB (1%) |         546 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   5.644 ms (5%) |         |  18.08 KiB (1%) |         269 |
| `["words", "nthreads=1"]`                           |  14.967 ms (5%) |         |  31.66 MiB (1%) |     1031236 |
| `["words", "nthreads=2"]`                           |   8.813 ms (5%) |         |  32.01 MiB (1%) |     1031304 |
| `["words", "nthreads=4"]`                           |   9.419 ms (5%) |         |  32.73 MiB (1%) |     1031418 |

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
      Ubuntu 24.04.3 LTS
  uname: Linux 6.11.0-1018-azure #18~24.04.1-Ubuntu SMP Sat Jun 28 04:46:03 UTC 2025 x86_64 x86_64
  CPU: AMD EPYC 7763 64-Core Processor: 
              speed         user         nice          sys         idle          irq
       #1  3244 MHz       3895 s          0 s        219 s       5584 s          0 s
       #2  3317 MHz       3522 s          0 s        271 s       5903 s          0 s
       #3  3236 MHz       3870 s          0 s        244 s       5578 s          0 s
       #4  3240 MHz       3419 s          0 s        265 s       6009 s          0 s
       
  Memory: 15.620063781738281 GB (11915.671875 MB free)
  Uptime: 974.15 sec
  Load Avg:  1.64  1.58  1.08
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
    Flags:                                fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush mmx fxsr sse sse2 ht syscall nx mmxext fxsr_opt pdpe1gb rdtscp lm constant_tsc rep_good nopl tsc_reliable nonstop_tsc cpuid extd_apicid aperfmperf tsc_known_freq pni pclmulqdq ssse3 fma cx16 pcid sse4_1 sse4_2 movbe popcnt aes xsave avx f16c rdrand hypervisor lahf_lm cmp_legacy svm cr8_legacy abm sse4a misalignsse 3dnowprefetch osvw topoext vmmcall fsgsbase bmi1 avx2 smep bmi2 erms invpcid rdseed adx smap clflushopt clwb sha_ni xsaveopt xsavec xgetbv1 xsaves user_shstk clzero xsaveerptr rdpru arat npt nrip_save tsc_scale vmcb_clean flushbyasid decodeassists pausefilter pfthreshold v_vmsave_vmload umip vaes vpclmulqdq rdpid fsrm
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

