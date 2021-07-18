# Multi-thread benchmark result

* Pull request commit: [`4f2365de9b106968b651b82e31893e3797b025d4`](https://github.com/JuliaFolds/Transducers.jl/commit/4f2365de9b106968b651b82e31893e3797b025d4)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/243> (Update */Manifest.toml)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 18 Jul 2021 - 01:17
    - Baseline: 18 Jul 2021 - 01:23
* Package commits:
    - Target: 0cd892
    - Baseline: 2cfb4c
* Julia commits:
    - Target: 69fcb5
    - Baseline: 69fcb5
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
| `["collect", "unordered", "basesize=1024"]`         |                1.10 (5%) :x: |                1.09 (1%) :x: |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` |                1.05 (5%) :x: |                1.11 (1%) :x: |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` |                   1.04 (5%)  |                1.05 (1%) :x: |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 0.90 (5%) :white_check_mark: | 0.90 (1%) :white_check_mark: |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  |                   1.01 (5%)  | 0.94 (1%) :white_check_mark: |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  |                   1.00 (5%)  |                1.01 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |                1.08 (5%) :x: |                1.06 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 0.90 (5%) :white_check_mark: | 0.91 (1%) :white_check_mark: |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 0.87 (5%) :white_check_mark: | 0.95 (1%) :white_check_mark: |
| `["overhead", "stoppable=false"]`                   |                1.11 (5%) :x: |                   1.00 (1%)  |
| `["parallel_histogram", "assoc", "basesize=4096"]`  | 0.94 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["parallel_histogram", "comm", "basesize=16384"]`  |                   0.98 (5%)  | 0.85 (1%) :white_check_mark: |
| `["parallel_histogram", "comm", "basesize=4096"]`   | 0.88 (5%) :white_check_mark: | 0.98 (1%) :white_check_mark: |
| `["parallel_histogram", "comm", "basesize=8192"]`   |                   0.99 (5%)  | 0.87 (1%) :white_check_mark: |
| `["parallel_histogram", "seq"]`                     | 0.93 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["splitby", "count", "foldl"]`                     |                2.14 (5%) :x: |                6.00 (1%) :x: |
| `["splitby", "count", "man"]`                       |                1.10 (5%) :x: |                   1.00 (1%)  |
| `["splitby", "count", "reduce"]`                    |                   0.99 (5%)  |                1.01 (1%) :x: |
| `["words", "nthreads=4"]`                           | 0.94 (5%) :white_check_mark: |                   1.00 (1%)  |

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
Julia Version 1.5.4
Commit 69fcb5745b (2021-03-11 19:13 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 20.04.2 LTS
  uname: Linux 5.8.0-1036-azure #38~20.04.1-Ubuntu SMP Thu Jun 17 14:14:18 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz: 
              speed         user         nice          sys         idle          irq
       #1  2294 MHz      51165 s         10 s       2049 s      23594 s          0 s
       #2  2294 MHz      59232 s         16 s       2612 s      14822 s          0 s
       
  Memory: 6.790924072265625 GB (3524.73046875 MB free)
  Uptime: 775.0 sec
  Load Avg:  1.73828125  1.53515625  0.94384765625
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, broadwell)
```

### Baseline
```
Julia Version 1.5.4
Commit 69fcb5745b (2021-03-11 19:13 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 20.04.2 LTS
  uname: Linux 5.8.0-1036-azure #38~20.04.1-Ubuntu SMP Thu Jun 17 14:14:18 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz: 
              speed         user         nice          sys         idle          irq
       #1  2294 MHz      82148 s         10 s       2707 s      26324 s          0 s
       #2  2294 MHz      79446 s         16 s       3190 s      28555 s          0 s
       
  Memory: 6.790924072265625 GB (3515.30078125 MB free)
  Uptime: 1121.0 sec
  Load Avg:  1.66943359375  1.5673828125  1.14013671875
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, broadwell)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 18 Jul 2021 - 1:17
* Package commit: 0cd892
* Julia commit: 69fcb5
* Julia command flags: None
* Environment variables: `JULIA_NUM_THREADS => 2`

## Results
Below is a table of this job's results, obtained by running the benchmarks.
The values listed in the `ID` column have the structure `[parent_group, child_group, ..., key]`, and can be used to
index into the BaseBenchmarks suite to retrieve the corresponding benchmarks.
The percentages accompanying time and memory values in the below table are noise tolerances. The "true"
time/memory value for a given benchmark is expected to fall within this percentage of the reported value.
An empty cell means that the value was zero.

| ID                                                  | time            | GC time | memory           | allocations |
|-----------------------------------------------------|----------------:|--------:|-----------------:|------------:|
| `["collect", "assoc", "basesize=1"]`                | 228.893 ms (5%) |         |   32.66 MiB (1%) |      286768 |
| `["collect", "assoc", "basesize=1024"]`             | 182.259 ms (5%) |         |    1.79 MiB (1%) |         569 |
| `["collect", "assoc", "basesize=32"]`               | 184.199 ms (5%) |         |    3.97 MiB (1%) |       13306 |
| `["collect", "seq"]`                                | 361.100 ms (5%) |         |  512.72 KiB (1%) |          15 |
| `["collect", "unordered", "basesize=1"]`            | 469.103 ms (5%) |         |   30.01 MiB (1%) |      360623 |
| `["collect", "unordered", "basesize=1024"]`         | 262.809 ms (5%) |         |  883.27 KiB (1%) |        5004 |
| `["collect", "unordered", "basesize=32"]`           | 217.390 ms (5%) |         |    1.47 MiB (1%) |       12543 |
| `["findfirst", "n=1000", "foldl"]`                  | 586.736 ms (5%) |         |                  |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 349.561 ms (5%) |         |  730.83 KiB (1%) |       12800 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 448.392 ms (5%) |         |  510.41 KiB (1%) |        8941 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 543.687 ms (5%) |         |  324.39 KiB (1%) |        5692 |
| `["findfirst", "n=400", "foldl"]`                   | 430.361 ms (5%) |         |                  |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 242.086 ms (5%) |         |    1.08 MiB (1%) |       19423 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 242.481 ms (5%) |         |  590.66 KiB (1%) |       10413 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 266.916 ms (5%) |         |  350.56 KiB (1%) |        6183 |
| `["findfirst", "n=500", "foldl"]`                   |  72.497 ms (5%) |         |                  |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 171.905 ms (5%) |         |  804.88 KiB (1%) |       13995 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 124.425 ms (5%) |         |  334.02 KiB (1%) |        5830 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 123.127 ms (5%) |         |  210.89 KiB (1%) |        3671 |
| `["overhead", "default"]`                           |  61.300 μs (5%) |         |   47.36 KiB (1%) |         382 |
| `["overhead", "stoppable=false"]`                   |  64.100 μs (5%) |         |   47.36 KiB (1%) |         381 |
| `["overhead", "stoppable=true"]`                    | 161.001 μs (5%) |         |  139.67 KiB (1%) |        2464 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   3.624 ms (5%) |         |  730.06 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   4.408 ms (5%) |         |    1.79 MiB (1%) |         213 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   3.959 ms (5%) |         |    1.43 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  13.412 ms (5%) |         |    1.04 MiB (1%) |         160 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  18.666 ms (5%) |         | 1023.97 KiB (1%) |        1039 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  17.961 ms (5%) |         |    1.07 MiB (1%) |        1192 |
| `["parallel_histogram", "seq"]`                     |   6.359 ms (5%) |         |  364.61 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  35.832 ms (5%) |         |                  |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  17.730 ms (5%) |         |    2.66 KiB (1%) |          48 |
| `["splitby", "count", "foldl"]`                     |   3.977 ms (5%) |         |    96 bytes (1%) |           4 |
| `["splitby", "count", "man"]`                       |   1.684 ms (5%) |         |                  |             |
| `["splitby", "count", "reduce"]`                    | 856.805 μs (5%) |         |    2.78 KiB (1%) |          52 |
| `["sum", "random", "foldl"]`                        |  13.502 ms (5%) |         |    32 bytes (1%) |           2 |
| `["sum", "random", "reduce", "basesize=128"]`       |   7.099 ms (5%) |         |  103.23 KiB (1%) |        1018 |
| `["sum", "random", "reduce", "basesize=256"]`       |   6.884 ms (5%) |         |   51.23 KiB (1%) |         506 |
| `["sum", "random", "reduce", "basesize=512"]`       |   6.758 ms (5%) |         |   25.30 KiB (1%) |         252 |
| `["sum", "uniform", "foldl"]`                       |  13.264 ms (5%) |         |    32 bytes (1%) |           2 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   6.746 ms (5%) |         |  103.23 KiB (1%) |        1018 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   6.851 ms (5%) |         |   51.23 KiB (1%) |         506 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   6.917 ms (5%) |         |   25.25 KiB (1%) |         251 |
| `["sum", "valley", "foldl"]`                        |  13.667 ms (5%) |         |    32 bytes (1%) |           2 |
| `["sum", "valley", "reduce", "basesize=128"]`       |   7.068 ms (5%) |         |  103.23 KiB (1%) |        1018 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   7.025 ms (5%) |         |   51.23 KiB (1%) |         506 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   7.042 ms (5%) |         |   25.25 KiB (1%) |         251 |
| `["words", "nthreads=1"]`                           |  24.757 ms (5%) |         |   31.92 MiB (1%) |     1039941 |
| `["words", "nthreads=2"]`                           |  15.460 ms (5%) |         |   32.63 MiB (1%) |     1040013 |
| `["words", "nthreads=4"]`                           |  15.756 ms (5%) |         |   33.08 MiB (1%) |     1040082 |

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
Julia Version 1.5.4
Commit 69fcb5745b (2021-03-11 19:13 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 20.04.2 LTS
  uname: Linux 5.8.0-1036-azure #38~20.04.1-Ubuntu SMP Thu Jun 17 14:14:18 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz: 
              speed         user         nice          sys         idle          irq
       #1  2294 MHz      51165 s         10 s       2049 s      23594 s          0 s
       #2  2294 MHz      59232 s         16 s       2612 s      14822 s          0 s
       
  Memory: 6.790924072265625 GB (3524.73046875 MB free)
  Uptime: 775.0 sec
  Load Avg:  1.73828125  1.53515625  0.94384765625
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, broadwell)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 18 Jul 2021 - 1:23
* Package commit: 2cfb4c
* Julia commit: 69fcb5
* Julia command flags: None
* Environment variables: `JULIA_NUM_THREADS => 2`

## Results
Below is a table of this job's results, obtained by running the benchmarks.
The values listed in the `ID` column have the structure `[parent_group, child_group, ..., key]`, and can be used to
index into the BaseBenchmarks suite to retrieve the corresponding benchmarks.
The percentages accompanying time and memory values in the below table are noise tolerances. The "true"
time/memory value for a given benchmark is expected to fall within this percentage of the reported value.
An empty cell means that the value was zero.

| ID                                                  | time            | GC time  | memory          | allocations |
|-----------------------------------------------------|----------------:|---------:|----------------:|------------:|
| `["collect", "assoc", "basesize=1"]`                | 235.008 ms (5%) |          |  32.66 MiB (1%) |      286773 |
| `["collect", "assoc", "basesize=1024"]`             | 184.109 ms (5%) |          |   1.79 MiB (1%) |         570 |
| `["collect", "assoc", "basesize=32"]`               | 182.350 ms (5%) |          |   3.97 MiB (1%) |       13306 |
| `["collect", "seq"]`                                | 355.780 ms (5%) |          | 512.72 KiB (1%) |          15 |
| `["collect", "unordered", "basesize=1"]`            | 449.020 ms (5%) |          |  30.01 MiB (1%) |      360639 |
| `["collect", "unordered", "basesize=1024"]`         | 238.962 ms (5%) |          | 812.33 KiB (1%) |        2734 |
| `["collect", "unordered", "basesize=32"]`           | 217.846 ms (5%) |          |   1.47 MiB (1%) |       12578 |
| `["findfirst", "n=1000", "foldl"]`                  | 584.431 ms (5%) |          |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 332.490 ms (5%) |          | 659.38 KiB (1%) |       11574 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 429.361 ms (5%) |          | 485.00 KiB (1%) |        8497 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 605.749 ms (5%) |          | 361.09 KiB (1%) |        6333 |
| `["findfirst", "n=400", "foldl"]`                   | 444.649 ms (5%) |          |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 240.343 ms (5%) |          |   1.15 MiB (1%) |       20648 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 243.598 ms (5%) |          | 591.13 KiB (1%) |       10437 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 267.034 ms (5%) |          | 345.86 KiB (1%) |        6098 |
| `["findfirst", "n=500", "foldl"]`                   |  73.141 ms (5%) |          |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 158.777 ms (5%) |          | 758.70 KiB (1%) |       13202 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 138.131 ms (5%) |          | 366.20 KiB (1%) |        6383 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 140.874 ms (5%) |          | 222.45 KiB (1%) |        3883 |
| `["overhead", "default"]`                           |  60.500 μs (5%) |          |  47.33 KiB (1%) |         381 |
| `["overhead", "stoppable=false"]`                   |  57.501 μs (5%) |          |  47.39 KiB (1%) |         382 |
| `["overhead", "stoppable=true"]`                    | 159.801 μs (5%) |          | 139.67 KiB (1%) |        2464 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   3.607 ms (5%) |          | 730.06 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   4.698 ms (5%) |          |   1.79 MiB (1%) |         213 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   3.934 ms (5%) |          |   1.43 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  13.705 ms (5%) |          |   1.22 MiB (1%) |         238 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  21.323 ms (5%) |          |   1.02 MiB (1%) |        1852 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  18.076 ms (5%) | 2.593 ms |   1.23 MiB (1%) |         392 |
| `["parallel_histogram", "seq"]`                     |   6.825 ms (5%) |          | 364.61 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  36.127 ms (5%) |          |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  18.348 ms (5%) |          |   2.66 KiB (1%) |          48 |
| `["splitby", "count", "foldl"]`                     |   1.858 ms (5%) |          |   16 bytes (1%) |           1 |
| `["splitby", "count", "man"]`                       |   1.538 ms (5%) |          |                 |             |
| `["splitby", "count", "reduce"]`                    | 861.704 μs (5%) |          |   2.75 KiB (1%) |          52 |
| `["sum", "random", "foldl"]`                        |  13.748 ms (5%) |          |   32 bytes (1%) |           2 |
| `["sum", "random", "reduce", "basesize=128"]`       |   7.172 ms (5%) |          | 103.23 KiB (1%) |        1018 |
| `["sum", "random", "reduce", "basesize=256"]`       |   7.014 ms (5%) |          |  51.23 KiB (1%) |         506 |
| `["sum", "random", "reduce", "basesize=512"]`       |   6.962 ms (5%) |          |  25.30 KiB (1%) |         252 |
| `["sum", "uniform", "foldl"]`                       |  13.385 ms (5%) |          |   32 bytes (1%) |           2 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   6.863 ms (5%) |          | 103.23 KiB (1%) |        1018 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   6.550 ms (5%) |          |  51.23 KiB (1%) |         506 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   6.704 ms (5%) |          |  25.25 KiB (1%) |         251 |
| `["sum", "valley", "foldl"]`                        |  13.942 ms (5%) |          |   32 bytes (1%) |           2 |
| `["sum", "valley", "reduce", "basesize=128"]`       |   7.233 ms (5%) |          | 103.23 KiB (1%) |        1018 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   7.156 ms (5%) |          |  51.23 KiB (1%) |         506 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   7.044 ms (5%) |          |  25.25 KiB (1%) |         251 |
| `["words", "nthreads=1"]`                           |  24.174 ms (5%) |          |  31.68 MiB (1%) |     1031717 |
| `["words", "nthreads=2"]`                           |  16.042 ms (5%) |          |  32.39 MiB (1%) |     1031829 |
| `["words", "nthreads=4"]`                           |  16.700 ms (5%) |          |  33.02 MiB (1%) |     1031987 |

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
Julia Version 1.5.4
Commit 69fcb5745b (2021-03-11 19:13 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 20.04.2 LTS
  uname: Linux 5.8.0-1036-azure #38~20.04.1-Ubuntu SMP Thu Jun 17 14:14:18 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz: 
              speed         user         nice          sys         idle          irq
       #1  2294 MHz      82148 s         10 s       2707 s      26324 s          0 s
       #2  2294 MHz      79446 s         16 s       3190 s      28555 s          0 s
       
  Memory: 6.790924072265625 GB (3515.30078125 MB free)
  Uptime: 1121.0 sec
  Load Avg:  1.66943359375  1.5673828125  1.14013671875
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
    Vulnerability Itlb multihit:     KVM: Mitigation: VMX unsupported
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

