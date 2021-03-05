# Multi-thread benchmark result

* Pull request commit: [`f59dde6dc4942a291de2aaeb9ef26ad3f52ba9b0`](https://github.com/JuliaFolds/Transducers.jl/commit/f59dde6dc4942a291de2aaeb9ef26ad3f52ba9b0)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/458> (Add ReducePartitionBy)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 5 Mar 2021 - 00:14
    - Baseline: 5 Mar 2021 - 00:19
* Package commits:
    - Target: c6c0a3
    - Baseline: eb0a9e
* Julia commits:
    - Target: 788b2c
    - Baseline: 788b2c
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
| `["collect", "unordered", "basesize=1024"]`         | 0.82 (5%) :white_check_mark: | 0.94 (1%) :white_check_mark: |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` |                1.49 (5%) :x: |                1.37 (1%) :x: |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` |                1.05 (5%) :x: |                   1.00 (1%)  |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` |                1.08 (5%) :x: |                1.16 (1%) :x: |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  |                   1.04 (5%)  |                1.02 (1%) :x: |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  |                1.08 (5%) :x: |                1.01 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |                   1.05 (5%)  |                1.21 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 0.87 (5%) :white_check_mark: | 0.94 (1%) :white_check_mark: |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 0.47 (5%) :white_check_mark: | 0.56 (1%) :white_check_mark: |
| `["parallel_histogram", "comm", "basesize=16384"]`  |                   1.05 (5%)  | 0.96 (1%) :white_check_mark: |
| `["parallel_histogram", "comm", "basesize=4096"]`   |                   0.96 (5%)  | 0.98 (1%) :white_check_mark: |
| `["words", "nthreads=2"]`                           |                1.06 (5%) :x: |                1.02 (1%) :x: |
| `["words", "nthreads=4"]`                           |                   1.00 (5%)  |                1.01 (1%) :x: |

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
Julia Version 1.5.3
Commit 788b2c77c1 (2020-11-09 13:37 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 20.04.2 LTS
  uname: Linux 5.4.0-1040-azure #42-Ubuntu SMP Fri Feb 5 15:39:06 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz: 
              speed         user         nice          sys         idle          irq
       #1  2294 MHz      54396 s         10 s       2451 s      60017 s          0 s
       #2  2294 MHz      47914 s          6 s       2526 s      66040 s          0 s
       
  Memory: 6.7913818359375 GB (3747.8125 MB free)
  Uptime: 1202.0 sec
  Load Avg:  1.67138671875  1.46875  0.88427734375
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, broadwell)
```

### Baseline
```
Julia Version 1.5.3
Commit 788b2c77c1 (2020-11-09 13:37 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 20.04.2 LTS
  uname: Linux 5.4.0-1040-azure #42-Ubuntu SMP Fri Feb 5 15:39:06 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz: 
              speed         user         nice          sys         idle          irq
       #1  2294 MHz      80048 s         10 s       2998 s      61509 s          0 s
       #2  2294 MHz      65424 s          6 s       3075 s      75702 s          0 s
       
  Memory: 6.7913818359375 GB (3793.9296875 MB free)
  Uptime: 1480.0 sec
  Load Avg:  1.5703125  1.52685546875  1.06298828125
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, broadwell)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 5 Mar 2021 - 0:14
* Package commit: c6c0a3
* Julia commit: 788b2c
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
| `["collect", "assoc", "basesize=1"]`                | 193.494 ms (5%) |         |  32.66 MiB (1%) |      286759 |
| `["collect", "assoc", "basesize=1024"]`             | 146.956 ms (5%) |         |   1.79 MiB (1%) |         570 |
| `["collect", "assoc", "basesize=32"]`               | 147.275 ms (5%) |         |   3.97 MiB (1%) |       13305 |
| `["collect", "seq"]`                                | 290.841 ms (5%) |         | 512.72 KiB (1%) |          15 |
| `["collect", "unordered", "basesize=1"]`            | 365.734 ms (5%) |         |  30.01 MiB (1%) |      360583 |
| `["collect", "unordered", "basesize=1024"]`         | 171.951 ms (5%) |         | 782.95 KiB (1%) |        1776 |
| `["collect", "unordered", "basesize=32"]`           | 173.087 ms (5%) |         |   1.48 MiB (1%) |       12701 |
| `["findfirst", "n=1000", "foldl"]`                  | 484.101 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 471.949 ms (5%) |         |   1.07 MiB (1%) |       19149 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 370.695 ms (5%) |         | 484.97 KiB (1%) |        8496 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 497.920 ms (5%) |         | 372.56 KiB (1%) |        6531 |
| `["findfirst", "n=400", "foldl"]`                   | 349.438 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 198.643 ms (5%) |         |   1.09 MiB (1%) |       19589 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 198.274 ms (5%) |         | 585.91 KiB (1%) |       10325 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 218.990 ms (5%) |         | 345.95 KiB (1%) |        6103 |
| `["findfirst", "n=500", "foldl"]`                   |  59.861 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 147.165 ms (5%) |         | 842.44 KiB (1%) |       14666 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 105.291 ms (5%) |         | 356.61 KiB (1%) |        6200 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  80.636 ms (5%) |         | 181.08 KiB (1%) |        3161 |
| `["overhead", "default"]`                           |  52.100 μs (5%) |         |  47.36 KiB (1%) |         382 |
| `["overhead", "stoppable=false"]`                   |  52.399 μs (5%) |         |  47.39 KiB (1%) |         382 |
| `["overhead", "stoppable=true"]`                    | 139.399 μs (5%) |         | 139.67 KiB (1%) |        2464 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   3.040 ms (5%) |         | 730.06 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   3.634 ms (5%) |         |   1.79 MiB (1%) |         213 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   3.337 ms (5%) |         |   1.43 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  12.657 ms (5%) |         | 987.11 KiB (1%) |         160 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  18.444 ms (5%) |         |   1.02 MiB (1%) |        1849 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  17.673 ms (5%) |         |   1.26 MiB (1%) |        1400 |
| `["parallel_histogram", "seq"]`                     |   5.452 ms (5%) |         | 364.61 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  28.881 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  14.529 ms (5%) |         |   2.66 KiB (1%) |          48 |
| `["sum", "random", "foldl"]`                        |  11.210 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "random", "reduce", "basesize=128"]`       |   5.806 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "random", "reduce", "basesize=256"]`       |   5.689 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "random", "reduce", "basesize=512"]`       |   5.713 ms (5%) |         |  25.30 KiB (1%) |         252 |
| `["sum", "uniform", "foldl"]`                       |  10.956 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   5.681 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   5.557 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   5.507 ms (5%) |         |  25.25 KiB (1%) |         251 |
| `["sum", "valley", "foldl"]`                        |  11.359 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "valley", "reduce", "basesize=128"]`       |   5.942 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   5.818 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   5.791 ms (5%) |         |  25.25 KiB (1%) |         251 |
| `["words", "nthreads=1"]`                           |  18.742 ms (5%) |         |  31.83 MiB (1%) |     1036745 |
| `["words", "nthreads=2"]`                           |  13.534 ms (5%) |         |  32.55 MiB (1%) |     1036860 |
| `["words", "nthreads=4"]`                           |  13.604 ms (5%) |         |  33.00 MiB (1%) |     1036954 |

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
- `["sum", "random"]`
- `["sum", "random", "reduce"]`
- `["sum", "uniform"]`
- `["sum", "uniform", "reduce"]`
- `["sum", "valley"]`
- `["sum", "valley", "reduce"]`
- `["words"]`

## Julia versioninfo
```
Julia Version 1.5.3
Commit 788b2c77c1 (2020-11-09 13:37 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 20.04.2 LTS
  uname: Linux 5.4.0-1040-azure #42-Ubuntu SMP Fri Feb 5 15:39:06 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz: 
              speed         user         nice          sys         idle          irq
       #1  2294 MHz      54396 s         10 s       2451 s      60017 s          0 s
       #2  2294 MHz      47914 s          6 s       2526 s      66040 s          0 s
       
  Memory: 6.7913818359375 GB (3747.8125 MB free)
  Uptime: 1202.0 sec
  Load Avg:  1.67138671875  1.46875  0.88427734375
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, broadwell)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 5 Mar 2021 - 0:19
* Package commit: eb0a9e
* Julia commit: 788b2c
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
| `["collect", "assoc", "basesize=1"]`                | 191.692 ms (5%) |         |  32.66 MiB (1%) |      286757 |
| `["collect", "assoc", "basesize=1024"]`             | 146.104 ms (5%) |         |   1.79 MiB (1%) |         570 |
| `["collect", "assoc", "basesize=32"]`               | 149.645 ms (5%) |         |   3.97 MiB (1%) |       13306 |
| `["collect", "seq"]`                                | 285.659 ms (5%) |         | 512.72 KiB (1%) |          15 |
| `["collect", "unordered", "basesize=1"]`            | 360.422 ms (5%) |         |  30.01 MiB (1%) |      360593 |
| `["collect", "unordered", "basesize=1024"]`         | 208.550 ms (5%) |         | 834.95 KiB (1%) |        3440 |
| `["collect", "unordered", "basesize=32"]`           | 174.562 ms (5%) |         |   1.47 MiB (1%) |       12529 |
| `["findfirst", "n=1000", "foldl"]`                  | 470.956 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 315.798 ms (5%) |         | 800.08 KiB (1%) |       13998 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 352.696 ms (5%) |         | 485.00 KiB (1%) |        8497 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 459.035 ms (5%) |         | 319.91 KiB (1%) |        5616 |
| `["findfirst", "n=400", "foldl"]`                   | 353.071 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 191.495 ms (5%) |         |   1.07 MiB (1%) |       19264 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 190.305 ms (5%) |         | 588.44 KiB (1%) |       10375 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 203.383 ms (5%) |         | 341.39 KiB (1%) |        6026 |
| `["findfirst", "n=500", "foldl"]`                   |  59.412 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 140.230 ms (5%) |         | 695.41 KiB (1%) |       12156 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 120.575 ms (5%) |         | 377.84 KiB (1%) |        6588 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 173.302 ms (5%) |         | 320.95 KiB (1%) |        5587 |
| `["overhead", "default"]`                           |  50.900 μs (5%) |         |  47.36 KiB (1%) |         382 |
| `["overhead", "stoppable=false"]`                   |  52.500 μs (5%) |         |  47.39 KiB (1%) |         382 |
| `["overhead", "stoppable=true"]`                    | 139.800 μs (5%) |         | 139.67 KiB (1%) |        2464 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   3.057 ms (5%) |         | 730.06 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   3.651 ms (5%) |         |   1.79 MiB (1%) |         213 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   3.330 ms (5%) |         |   1.43 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  12.070 ms (5%) |         |   1.00 MiB (1%) |         160 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  19.291 ms (5%) |         |   1.05 MiB (1%) |        2605 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  17.149 ms (5%) |         |   1.25 MiB (1%) |        1247 |
| `["parallel_histogram", "seq"]`                     |   5.500 ms (5%) |         | 364.61 KiB (1%) |          24 |
| `["sum", "random", "foldl"]`                        |  11.211 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "random", "reduce", "basesize=128"]`       |   5.854 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "random", "reduce", "basesize=256"]`       |   5.706 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "random", "reduce", "basesize=512"]`       |   5.754 ms (5%) |         |  25.30 KiB (1%) |         252 |
| `["sum", "uniform", "foldl"]`                       |  11.013 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   5.656 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   5.572 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   5.508 ms (5%) |         |  25.25 KiB (1%) |         251 |
| `["sum", "valley", "foldl"]`                        |  11.367 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "valley", "reduce", "basesize=128"]`       |   5.886 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   5.769 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   5.743 ms (5%) |         |  25.25 KiB (1%) |         251 |
| `["words", "nthreads=1"]`                           |  19.122 ms (5%) |         |  31.59 MiB (1%) |     1029010 |
| `["words", "nthreads=2"]`                           |  12.746 ms (5%) |         |  31.94 MiB (1%) |     1029057 |
| `["words", "nthreads=4"]`                           |  13.650 ms (5%) |         |  32.66 MiB (1%) |     1029135 |

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
- `["sum", "random"]`
- `["sum", "random", "reduce"]`
- `["sum", "uniform"]`
- `["sum", "uniform", "reduce"]`
- `["sum", "valley"]`
- `["sum", "valley", "reduce"]`
- `["words"]`

## Julia versioninfo
```
Julia Version 1.5.3
Commit 788b2c77c1 (2020-11-09 13:37 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 20.04.2 LTS
  uname: Linux 5.4.0-1040-azure #42-Ubuntu SMP Fri Feb 5 15:39:06 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz: 
              speed         user         nice          sys         idle          irq
       #1  2294 MHz      80048 s         10 s       2998 s      61509 s          0 s
       #2  2294 MHz      65424 s          6 s       3075 s      75702 s          0 s
       
  Memory: 6.7913818359375 GB (3793.9296875 MB free)
  Uptime: 1480.0 sec
  Load Avg:  1.5703125  1.52685546875  1.06298828125
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, broadwell)
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
    CPU MHz:                         2294.685
    BogoMIPS:                        4589.37
    Hypervisor vendor:               Microsoft
    Virtualization type:             full
    L1d cache:                       64 KiB
    L1i cache:                       64 KiB
    L2 cache:                        512 KiB
    L3 cache:                        50 MiB
    NUMA node0 CPU(s):               0,1
    Vulnerability Itlb multihit:     KVM: Vulnerable
    Vulnerability L1tf:              Mitigation; PTE Inversion
    Vulnerability Mds:               Mitigation; Clear CPU buffers; SMT Host state unknown
    Vulnerability Meltdown:          Mitigation; PTI
    Vulnerability Spec store bypass: Vulnerable
    Vulnerability Spectre v1:        Mitigation; usercopy/swapgs barriers and __user pointer sanitization
    Vulnerability Spectre v2:        Mitigation; Full generic retpoline, STIBP disabled, RSB filling
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
|                    | No Hyperthreading detected                              |
| Clock Frequencies  | Not supported by CPU                                    |
| Data Cache         | Level 1:3 : (32, 256, 51200) kbytes                     |
|                    | 64 byte cache line size                                 |
| Address Size       | 48 bits virtual, 46 bits physical                       |
| SIMD               | 256 bit = 32 byte max. SIMD vector size                 |
| Time Stamp Counter | TSC is accessible via `rdtsc`                           |
|                    | TSC increased at every clock cycle (non-invariant TSC)  |
| Perf. Monitoring   | Performance Monitoring Counters (PMC) are not supported |
| Hypervisor         | Yes, Microsoft                                          |

