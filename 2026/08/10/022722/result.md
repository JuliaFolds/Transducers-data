# Multi-thread benchmark result

* Pull request commit: [`07cee12d2f8599a9fd31b076c301e093240786a7`](https://github.com/JuliaFolds/Transducers.jl/commit/07cee12d2f8599a9fd31b076c301e093240786a7)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/243> (Update */Manifest.toml)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 10 Aug 2026 - 02:21
    - Baseline: 10 Aug 2026 - 02:26
* Package commits:
    - Target: 5866879
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
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 0.73 (5%) :white_check_mark: | 0.74 (1%) :white_check_mark: |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` |                   1.05 (5%)  |                1.09 (1%) :x: |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` |                   1.01 (5%)  |                1.01 (1%) :x: |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  |                   1.02 (5%)  |                1.05 (1%) :x: |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  |                   1.00 (5%)  | 0.99 (1%) :white_check_mark: |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 0.87 (5%) :white_check_mark: | 0.81 (1%) :white_check_mark: |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |                   0.96 (5%)  | 0.89 (1%) :white_check_mark: |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |                1.76 (5%) :x: |                1.57 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |                1.07 (5%) :x: | 0.92 (1%) :white_check_mark: |
| `["overhead", "default"]`                           |                1.07 (5%) :x: |                   1.00 (1%)  |
| `["parallel_histogram", "comm", "basesize=16384"]`  | 0.93 (5%) :white_check_mark: |                   0.99 (1%)  |
| `["parallel_histogram", "comm", "basesize=8192"]`   |                   1.03 (5%)  | 0.99 (1%) :white_check_mark: |
| `["splitby", "count", "foldl"]`                     | 0.85 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["words", "nthreads=2"]`                           |                   0.96 (5%)  | 0.98 (1%) :white_check_mark: |

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
      Ubuntu 24.04.4 LTS
  uname: Linux 6.17.0-1020-azure #20~24.04.1-Ubuntu SMP Fri Jun 19 20:09:14 UTC 2026 x86_64 x86_64
  CPU: AMD EPYC 7763 64-Core Processor: 
              speed         user         nice          sys         idle          irq
       #1  3237 MHz       2120 s          0 s        142 s       4313 s          0 s
       #2  3226 MHz       2651 s          0 s        189 s       3735 s          0 s
       #3  3243 MHz       2822 s          0 s        170 s       3585 s          0 s
       #4  3235 MHz       2487 s          0 s        165 s       3937 s          0 s
       
  Memory: 15.614948272705078 GB (11218.1171875 MB free)
  Uptime: 664.11 sec
  Load Avg:  1.75  1.5  0.88
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
      Ubuntu 24.04.4 LTS
  uname: Linux 6.17.0-1020-azure #20~24.04.1-Ubuntu SMP Fri Jun 19 20:09:14 UTC 2026 x86_64 x86_64
  CPU: AMD EPYC 7763 64-Core Processor: 
              speed         user         nice          sys         idle          irq
       #1  3243 MHz       3029 s          0 s        188 s       6429 s          0 s
       #2  3274 MHz       3809 s          0 s        244 s       5591 s          0 s
       #3  3232 MHz       4042 s          0 s        232 s       5378 s          0 s
       #4  3243 MHz       3965 s          0 s        242 s       5456 s          0 s
       
  Memory: 15.614948272705078 GB (11146.46875 MB free)
  Uptime: 972.17 sec
  Load Avg:  1.74  1.64  1.12
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, znver3)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 10 Aug 2026 - 02:21
* Package commit: 5866879
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
| `["collect", "assoc", "basesize=1"]`                | 149.962 ms (5%) |         |   4.36 MiB (1%) |       32800 |
| `["collect", "assoc", "basesize=1024"]`             | 148.534 ms (5%) |         |   1.09 MiB (1%) |          53 |
| `["collect", "assoc", "basesize=32"]`               | 148.669 ms (5%) |         |   1.48 MiB (1%) |        1052 |
| `["collect", "seq"]`                                | 296.477 ms (5%) |         | 256.05 KiB (1%) |           2 |
| `["collect", "unordered", "basesize=1"]`            | 252.054 ms (5%) |         |  23.72 MiB (1%) |      407116 |
| `["collect", "unordered", "basesize=1024"]`         | 158.148 ms (5%) |         |   1.01 MiB (1%) |        1183 |
| `["collect", "unordered", "basesize=32"]`           | 168.812 ms (5%) |         |   1.60 MiB (1%) |       15307 |
| `["findfirst", "n=1000", "foldl"]`                  | 507.903 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 276.631 ms (5%) |         | 232.73 KiB (1%) |        3272 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 384.235 ms (5%) |         | 172.02 KiB (1%) |        2405 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 401.128 ms (5%) |         |  97.78 KiB (1%) |        1365 |
| `["findfirst", "n=400", "foldl"]`                   | 380.134 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 201.399 ms (5%) |         | 397.50 KiB (1%) |        5644 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 198.760 ms (5%) |         | 198.83 KiB (1%) |        2855 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 220.520 ms (5%) |         | 112.62 KiB (1%) |        1623 |
| `["findfirst", "n=500", "foldl"]`                   |  65.967 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |  66.230 ms (5%) |         | 141.73 KiB (1%) |        1915 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 104.299 ms (5%) |         | 119.03 KiB (1%) |        1613 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  85.244 ms (5%) |         |  56.84 KiB (1%) |         779 |
| `["overhead", "default"]`                           |  55.754 μs (5%) |         |  32.70 KiB (1%) |         417 |
| `["overhead", "stoppable=false"]`                   |  54.191 μs (5%) |         |  32.75 KiB (1%) |         418 |
| `["overhead", "stoppable=true"]`                    |  56.996 μs (5%) |         |  44.19 KiB (1%) |         608 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   2.395 ms (5%) |         | 728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   2.950 ms (5%) |         |   1.79 MiB (1%) |         216 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   2.674 ms (5%) |         |   1.42 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |   8.084 ms (5%) |         |   1.57 MiB (1%) |        2119 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  12.872 ms (5%) |         |   1.35 MiB (1%) |       10309 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  11.850 ms (5%) |         |   1.29 MiB (1%) |        8331 |
| `["parallel_histogram", "seq"]`                     |   4.260 ms (5%) |         | 364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  31.365 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  15.724 ms (5%) |         |  736 bytes (1%) |          11 |
| `["splitby", "count", "foldl"]`                     |   1.493 ms (5%) |         |                 |             |
| `["splitby", "count", "man"]`                       |   1.167 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    | 720.749 μs (5%) |         |   1.06 KiB (1%) |          18 |
| `["sum", "random", "foldl"]`                        |  11.034 ms (5%) |         |                 |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   5.647 ms (5%) |         |  74.19 KiB (1%) |        1104 |
| `["sum", "random", "reduce", "basesize=256"]`       |   5.594 ms (5%) |         |  36.81 KiB (1%) |         548 |
| `["sum", "random", "reduce", "basesize=512"]`       |   5.557 ms (5%) |         |  18.08 KiB (1%) |         269 |
| `["sum", "uniform", "foldl"]`                       |  10.946 ms (5%) |         |                 |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   5.617 ms (5%) |         |  74.19 KiB (1%) |        1104 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   5.553 ms (5%) |         |  36.75 KiB (1%) |         546 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   5.509 ms (5%) |         |  18.08 KiB (1%) |         269 |
| `["sum", "valley", "foldl"]`                        |  11.184 ms (5%) |         |                 |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   5.746 ms (5%) |         |  74.09 KiB (1%) |        1101 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   5.681 ms (5%) |         |  36.75 KiB (1%) |         546 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   5.666 ms (5%) |         |  18.05 KiB (1%) |         268 |
| `["words", "nthreads=1"]`                           |  14.743 ms (5%) |         |  31.56 MiB (1%) |     1028164 |
| `["words", "nthreads=2"]`                           |   9.776 ms (5%) |         |  31.92 MiB (1%) |     1028207 |
| `["words", "nthreads=4"]`                           |  10.507 ms (5%) |         |  32.64 MiB (1%) |     1028306 |

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
      Ubuntu 24.04.4 LTS
  uname: Linux 6.17.0-1020-azure #20~24.04.1-Ubuntu SMP Fri Jun 19 20:09:14 UTC 2026 x86_64 x86_64
  CPU: AMD EPYC 7763 64-Core Processor: 
              speed         user         nice          sys         idle          irq
       #1  3237 MHz       2120 s          0 s        142 s       4313 s          0 s
       #2  3226 MHz       2651 s          0 s        189 s       3735 s          0 s
       #3  3243 MHz       2822 s          0 s        170 s       3585 s          0 s
       #4  3235 MHz       2487 s          0 s        165 s       3937 s          0 s
       
  Memory: 15.614948272705078 GB (11218.1171875 MB free)
  Uptime: 664.11 sec
  Load Avg:  1.75  1.5  0.88
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, znver3)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 10 Aug 2026 - 02:26
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
| `["collect", "assoc", "basesize=1"]`                | 150.178 ms (5%) |         |   4.36 MiB (1%) |       32801 |
| `["collect", "assoc", "basesize=1024"]`             | 148.832 ms (5%) |         |   1.09 MiB (1%) |          54 |
| `["collect", "assoc", "basesize=32"]`               | 148.742 ms (5%) |         |   1.48 MiB (1%) |        1052 |
| `["collect", "seq"]`                                | 296.502 ms (5%) |         | 256.05 KiB (1%) |           2 |
| `["collect", "unordered", "basesize=1"]`            | 253.901 ms (5%) |         |  23.72 MiB (1%) |      407102 |
| `["collect", "unordered", "basesize=1024"]`         | 158.181 ms (5%) |         |   1.01 MiB (1%) |        1146 |
| `["collect", "unordered", "basesize=32"]`           | 169.285 ms (5%) |         |   1.60 MiB (1%) |       15207 |
| `["findfirst", "n=1000", "foldl"]`                  | 507.970 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 379.873 ms (5%) |         | 314.34 KiB (1%) |        4431 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 367.157 ms (5%) |         | 158.27 KiB (1%) |        2240 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 395.843 ms (5%) |         |  96.75 KiB (1%) |        1346 |
| `["findfirst", "n=400", "foldl"]`                   | 380.049 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 196.716 ms (5%) |         | 376.78 KiB (1%) |        5372 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 198.753 ms (5%) |         | 201.08 KiB (1%) |        2880 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 254.327 ms (5%) |         | 138.98 KiB (1%) |        1971 |
| `["findfirst", "n=500", "foldl"]`                   |  65.983 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |  69.266 ms (5%) |         | 159.34 KiB (1%) |        2159 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |  59.422 ms (5%) |         |  76.05 KiB (1%) |        1036 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  79.776 ms (5%) |         |  61.64 KiB (1%) |         820 |
| `["overhead", "default"]`                           |  51.917 μs (5%) |         |  32.73 KiB (1%) |         418 |
| `["overhead", "stoppable=false"]`                   |  53.089 μs (5%) |         |  32.75 KiB (1%) |         418 |
| `["overhead", "stoppable=true"]`                    |  58.850 μs (5%) |         |  44.25 KiB (1%) |         610 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   2.396 ms (5%) |         | 728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   2.955 ms (5%) |         |   1.79 MiB (1%) |         216 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   2.668 ms (5%) |         |   1.42 MiB (1%) |         118 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |   8.709 ms (5%) |         |   1.58 MiB (1%) |        2442 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  12.809 ms (5%) |         |   1.34 MiB (1%) |       10224 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  11.516 ms (5%) |         |   1.30 MiB (1%) |        7902 |
| `["parallel_histogram", "seq"]`                     |   4.264 ms (5%) |         | 364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  31.359 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  15.755 ms (5%) |         |  736 bytes (1%) |          11 |
| `["splitby", "count", "foldl"]`                     |   1.751 ms (5%) |         |                 |             |
| `["splitby", "count", "man"]`                       |   1.167 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    | 726.831 μs (5%) |         |   1.06 KiB (1%) |          18 |
| `["sum", "random", "foldl"]`                        |  10.996 ms (5%) |         |                 |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   5.632 ms (5%) |         |  74.06 KiB (1%) |        1100 |
| `["sum", "random", "reduce", "basesize=256"]`       |   5.584 ms (5%) |         |  36.75 KiB (1%) |         546 |
| `["sum", "random", "reduce", "basesize=512"]`       |   5.555 ms (5%) |         |  18.08 KiB (1%) |         269 |
| `["sum", "uniform", "foldl"]`                       |  10.955 ms (5%) |         |                 |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   5.617 ms (5%) |         |  74.16 KiB (1%) |        1103 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   5.551 ms (5%) |         |  36.78 KiB (1%) |         547 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   5.506 ms (5%) |         |  18.11 KiB (1%) |         270 |
| `["sum", "valley", "foldl"]`                        |  11.178 ms (5%) |         |                 |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   5.734 ms (5%) |         |  74.12 KiB (1%) |        1102 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   5.673 ms (5%) |         |  36.78 KiB (1%) |         547 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   5.675 ms (5%) |         |  18.08 KiB (1%) |         269 |
| `["words", "nthreads=1"]`                           |  14.878 ms (5%) |         |  31.75 MiB (1%) |     1034491 |
| `["words", "nthreads=2"]`                           |  10.134 ms (5%) |         |  32.46 MiB (1%) |     1034564 |
| `["words", "nthreads=4"]`                           |  10.399 ms (5%) |         |  32.91 MiB (1%) |     1034652 |

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
      Ubuntu 24.04.4 LTS
  uname: Linux 6.17.0-1020-azure #20~24.04.1-Ubuntu SMP Fri Jun 19 20:09:14 UTC 2026 x86_64 x86_64
  CPU: AMD EPYC 7763 64-Core Processor: 
              speed         user         nice          sys         idle          irq
       #1  3243 MHz       3029 s          0 s        188 s       6429 s          0 s
       #2  3274 MHz       3809 s          0 s        244 s       5591 s          0 s
       #3  3232 MHz       4042 s          0 s        232 s       5378 s          0 s
       #4  3243 MHz       3965 s          0 s        242 s       5456 s          0 s
       
  Memory: 15.614948272705078 GB (11146.46875 MB free)
  Uptime: 972.17 sec
  Load Avg:  1.74  1.64  1.12
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

    Architecture:                            x86_64
    CPU op-mode(s):                          32-bit, 64-bit
    Address sizes:                           48 bits physical, 48 bits virtual
    Byte Order:                              Little Endian
    CPU(s):                                  4
    On-line CPU(s) list:                     0-3
    Vendor ID:                               AuthenticAMD
    Model name:                              AMD EPYC 7763 64-Core Processor
    CPU family:                              25
    Model:                                   1
    Thread(s) per core:                      2
    Core(s) per socket:                      2
    Socket(s):                               1
    Stepping:                                1
    BogoMIPS:                                4890.85
    Flags:                                   fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush mmx fxsr sse sse2 ht syscall nx mmxext fxsr_opt pdpe1gb rdtscp lm constant_tsc rep_good nopl tsc_reliable nonstop_tsc cpuid extd_apicid aperfmperf tsc_known_freq pni pclmulqdq ssse3 fma cx16 pcid sse4_1 sse4_2 movbe popcnt aes xsave avx f16c rdrand hypervisor lahf_lm cmp_legacy svm cr8_legacy abm sse4a misalignsse 3dnowprefetch osvw topoext vmmcall fsgsbase bmi1 avx2 smep bmi2 erms invpcid rdseed adx smap clflushopt clwb sha_ni xsaveopt xsavec xgetbv1 xsaves user_shstk clzero xsaveerptr rdpru arat npt nrip_save tsc_scale vmcb_clean flushbyasid decodeassists pausefilter pfthreshold v_vmsave_vmload umip vaes vpclmulqdq rdpid fsrm
    Virtualization:                          AMD-V
    Hypervisor vendor:                       Microsoft
    Virtualization type:                     full
    L1d cache:                               64 KiB (2 instances)
    L1i cache:                               64 KiB (2 instances)
    L2 cache:                                1 MiB (2 instances)
    L3 cache:                                32 MiB (1 instance)
    NUMA node(s):                            1
    NUMA node0 CPU(s):                       0-3
    Vulnerability Gather data sampling:      Not affected
    Vulnerability Ghostwrite:                Not affected
    Vulnerability Indirect target selection: Not affected
    Vulnerability Itlb multihit:             Not affected
    Vulnerability L1tf:                      Not affected
    Vulnerability Mds:                       Not affected
    Vulnerability Meltdown:                  Not affected
    Vulnerability Mmio stale data:           Not affected
    Vulnerability Old microcode:             Not affected
    Vulnerability Reg file data sampling:    Not affected
    Vulnerability Retbleed:                  Not affected
    Vulnerability Spec rstack overflow:      Vulnerable: Safe RET, no microcode
    Vulnerability Spec store bypass:         Vulnerable
    Vulnerability Spectre v1:                Mitigation; usercopy/swapgs barriers and __user pointer sanitization
    Vulnerability Spectre v2:                Mitigation; Retpolines; STIBP disabled; RSB filling; PBRSB-eIBRS Not affected; BHI Not affected
    Vulnerability Srbds:                     Not affected
    Vulnerability Tsa:                       Vulnerable: No microcode
    Vulnerability Tsx async abort:           Not affected
    Vulnerability Vmscape:                   Not affected
    

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

