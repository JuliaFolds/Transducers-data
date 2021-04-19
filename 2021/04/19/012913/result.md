# Multi-thread benchmark result

* Pull request commit: [`cd022493ef0a5dcb7ffacc5efc4bd96181c25fdc`](https://github.com/JuliaFolds/Transducers.jl/commit/cd022493ef0a5dcb7ffacc5efc4bd96181c25fdc)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/243> (Update */Manifest.toml)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 19 Apr 2021 - 01:22
    - Baseline: 19 Apr 2021 - 01:28
* Package commits:
    - Target: 977419
    - Baseline: 2cc4af
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
| `["collect", "assoc", "basesize=1"]`                | 0.94 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["collect", "unordered", "basesize=1"]`            |                1.12 (5%) :x: |                   1.00 (1%)  |
| `["collect", "unordered", "basesize=1024"]`         |                   1.00 (5%)  | 0.96 (1%) :white_check_mark: |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 0.92 (5%) :white_check_mark: | 0.91 (1%) :white_check_mark: |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` |                1.34 (5%) :x: |                1.28 (1%) :x: |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 0.86 (5%) :white_check_mark: |                1.04 (1%) :x: |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 0.92 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  |                   1.03 (5%)  |                1.06 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |                1.40 (5%) :x: |                1.16 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 0.84 (5%) :white_check_mark: | 0.88 (1%) :white_check_mark: |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |                1.53 (5%) :x: |                1.27 (1%) :x: |
| `["parallel_histogram", "comm", "basesize=16384"]`  |                1.13 (5%) :x: | 0.82 (1%) :white_check_mark: |
| `["parallel_histogram", "comm", "basesize=4096"]`   |                1.29 (5%) :x: |                   1.00 (1%)  |
| `["parallel_histogram", "comm", "basesize=8192"]`   |                1.15 (5%) :x: |                   0.99 (1%)  |
| `["splitby", "count", "man"]`                       |                1.14 (5%) :x: |                   1.00 (1%)  |
| `["splitby", "count", "reduce"]`                    |                   1.00 (5%)  |                1.01 (1%) :x: |
| `["sum", "valley", "reduce", "basesize=256"]`       | 0.93 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["words", "nthreads=1"]`                           | 0.93 (5%) :white_check_mark: | 0.98 (1%) :white_check_mark: |
| `["words", "nthreads=2"]`                           |                   0.97 (5%)  | 0.99 (1%) :white_check_mark: |
| `["words", "nthreads=4"]`                           |                   0.97 (5%)  | 0.98 (1%) :white_check_mark: |

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
  uname: Linux 5.4.0-1043-azure #45-Ubuntu SMP Fri Mar 19 17:33:38 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz: 
              speed         user         nice          sys         idle          irq
       #1  2294 MHz      60502 s         28 s       3078 s      65445 s          0 s
       #2  2294 MHz      55903 s          2 s       3430 s      69651 s          0 s
       
  Memory: 6.791343688964844 GB (3651.87109375 MB free)
  Uptime: 1304.0 sec
  Load Avg:  1.521484375  1.43896484375  0.93017578125
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
  uname: Linux 5.4.0-1043-azure #45-Ubuntu SMP Fri Mar 19 17:33:38 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz: 
              speed         user         nice          sys         idle          irq
       #1  2294 MHz      84166 s         28 s       3915 s      78672 s          0 s
       #2  2294 MHz      86294 s          2 s       4198 s      76225 s          0 s
       
  Memory: 6.791343688964844 GB (3626.12109375 MB free)
  Uptime: 1684.0 sec
  Load Avg:  1.48046875  1.4990234375  1.13427734375
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, broadwell)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 19 Apr 2021 - 1:22
* Package commit: 977419
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
| `["collect", "assoc", "basesize=1"]`                | 254.453 ms (5%) |         |   32.66 MiB (1%) |      286774 |
| `["collect", "assoc", "basesize=1024"]`             | 191.295 ms (5%) |         |    1.79 MiB (1%) |         570 |
| `["collect", "assoc", "basesize=32"]`               | 192.473 ms (5%) |         |    3.97 MiB (1%) |       13305 |
| `["collect", "seq"]`                                | 376.087 ms (5%) |         |  512.72 KiB (1%) |          15 |
| `["collect", "unordered", "basesize=1"]`            | 540.320 ms (5%) |         |   30.03 MiB (1%) |      361125 |
| `["collect", "unordered", "basesize=1024"]`         | 328.458 ms (5%) |         |  801.98 KiB (1%) |        2403 |
| `["collect", "unordered", "basesize=32"]`           | 229.887 ms (5%) |         |    1.48 MiB (1%) |       12786 |
| `["findfirst", "n=1000", "foldl"]`                  | 647.958 ms (5%) |         |                  |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 439.935 ms (5%) |         |  774.73 KiB (1%) |       13557 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 492.773 ms (5%) |         |  482.64 KiB (1%) |        8451 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 841.847 ms (5%) |         |  446.11 KiB (1%) |        7813 |
| `["findfirst", "n=400", "foldl"]`                   | 464.010 ms (5%) |         |                  |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 261.142 ms (5%) |         |    1.09 MiB (1%) |       19615 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 270.484 ms (5%) |         |  593.23 KiB (1%) |       10466 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 295.354 ms (5%) |         |  366.75 KiB (1%) |        6469 |
| `["findfirst", "n=500", "foldl"]`                   |  79.475 ms (5%) |         |                  |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 190.574 ms (5%) |         |  740.00 KiB (1%) |       12868 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 147.787 ms (5%) |         |  405.39 KiB (1%) |        7060 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 183.197 ms (5%) |         |  268.05 KiB (1%) |        4669 |
| `["overhead", "default"]`                           |  70.700 μs (5%) |         |   47.33 KiB (1%) |         381 |
| `["overhead", "stoppable=false"]`                   |  68.500 μs (5%) |         |   47.36 KiB (1%) |         381 |
| `["overhead", "stoppable=true"]`                    | 191.800 μs (5%) |         |  139.67 KiB (1%) |        2464 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   4.212 ms (5%) |         |  730.06 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   4.986 ms (5%) |         |    1.79 MiB (1%) |         213 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   4.580 ms (5%) |         |    1.43 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  17.778 ms (5%) |         | 1020.33 KiB (1%) |         160 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  26.478 ms (5%) |         |    1.01 MiB (1%) |         763 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  21.921 ms (5%) |         |    1.23 MiB (1%) |         474 |
| `["parallel_histogram", "seq"]`                     |   7.548 ms (5%) |         |  364.61 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  39.655 ms (5%) |         |                  |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  19.853 ms (5%) |         |    2.66 KiB (1%) |          48 |
| `["splitby", "count", "foldl"]`                     |   4.832 ms (5%) |         |    96 bytes (1%) |           4 |
| `["splitby", "count", "man"]`                       |   2.141 ms (5%) |         |                  |             |
| `["splitby", "count", "reduce"]`                    |   1.028 ms (5%) |         |    2.84 KiB (1%) |          54 |
| `["sum", "random", "foldl"]`                        |  15.588 ms (5%) |         |    32 bytes (1%) |           2 |
| `["sum", "random", "reduce", "basesize=128"]`       |   8.038 ms (5%) |         |  103.23 KiB (1%) |        1018 |
| `["sum", "random", "reduce", "basesize=256"]`       |   7.926 ms (5%) |         |   51.23 KiB (1%) |         506 |
| `["sum", "random", "reduce", "basesize=512"]`       |   7.856 ms (5%) |         |   25.30 KiB (1%) |         252 |
| `["sum", "uniform", "foldl"]`                       |  15.095 ms (5%) |         |    32 bytes (1%) |           2 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   7.782 ms (5%) |         |  103.23 KiB (1%) |        1018 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   7.665 ms (5%) |         |   51.23 KiB (1%) |         506 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   7.597 ms (5%) |         |   25.25 KiB (1%) |         251 |
| `["sum", "valley", "foldl"]`                        |  15.634 ms (5%) |         |    32 bytes (1%) |           2 |
| `["sum", "valley", "reduce", "basesize=128"]`       |   8.057 ms (5%) |         |  103.23 KiB (1%) |        1018 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   7.437 ms (5%) |         |   51.23 KiB (1%) |         506 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   7.872 ms (5%) |         |   25.25 KiB (1%) |         251 |
| `["words", "nthreads=1"]`                           |  26.372 ms (5%) |         |   31.32 MiB (1%) |     1020263 |
| `["words", "nthreads=2"]`                           |  16.052 ms (5%) |         |   32.03 MiB (1%) |     1020371 |
| `["words", "nthreads=4"]`                           |  16.774 ms (5%) |         |   32.48 MiB (1%) |     1020437 |

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
  uname: Linux 5.4.0-1043-azure #45-Ubuntu SMP Fri Mar 19 17:33:38 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz: 
              speed         user         nice          sys         idle          irq
       #1  2294 MHz      60502 s         28 s       3078 s      65445 s          0 s
       #2  2294 MHz      55903 s          2 s       3430 s      69651 s          0 s
       
  Memory: 6.791343688964844 GB (3651.87109375 MB free)
  Uptime: 1304.0 sec
  Load Avg:  1.521484375  1.43896484375  0.93017578125
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, broadwell)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 19 Apr 2021 - 1:28
* Package commit: 2cc4af
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

| ID                                                  | time            | GC time   | memory          | allocations |
|-----------------------------------------------------|----------------:|----------:|----------------:|------------:|
| `["collect", "assoc", "basesize=1"]`                | 270.243 ms (5%) | 19.879 ms |  32.66 MiB (1%) |      286769 |
| `["collect", "assoc", "basesize=1024"]`             | 193.335 ms (5%) |           |   1.79 MiB (1%) |         569 |
| `["collect", "assoc", "basesize=32"]`               | 194.011 ms (5%) |           |   3.97 MiB (1%) |       13307 |
| `["collect", "seq"]`                                | 379.509 ms (5%) |           | 512.72 KiB (1%) |          15 |
| `["collect", "unordered", "basesize=1"]`            | 483.598 ms (5%) |           |  30.02 MiB (1%) |      360856 |
| `["collect", "unordered", "basesize=1024"]`         | 327.411 ms (5%) |           | 837.30 KiB (1%) |        3533 |
| `["collect", "unordered", "basesize=32"]`           | 237.065 ms (5%) |           |   1.49 MiB (1%) |       13204 |
| `["findfirst", "n=1000", "foldl"]`                  | 636.771 ms (5%) |           |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 443.427 ms (5%) |           | 774.81 KiB (1%) |       13560 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 537.951 ms (5%) |           | 529.06 KiB (1%) |        9274 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 629.482 ms (5%) |           | 347.30 KiB (1%) |        6087 |
| `["findfirst", "n=400", "foldl"]`                   | 463.645 ms (5%) |           |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 302.337 ms (5%) |           |   1.05 MiB (1%) |       18869 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 295.360 ms (5%) |           | 593.25 KiB (1%) |       10467 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 285.871 ms (5%) |           | 345.89 KiB (1%) |        6098 |
| `["findfirst", "n=500", "foldl"]`                   |  79.482 ms (5%) |           |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 135.939 ms (5%) |           | 638.20 KiB (1%) |       11097 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 175.208 ms (5%) |           | 462.91 KiB (1%) |        8053 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 119.487 ms (5%) |           | 210.83 KiB (1%) |        3677 |
| `["overhead", "default"]`                           |  67.497 μs (5%) |           |  47.36 KiB (1%) |         382 |
| `["overhead", "stoppable=false"]`                   |  69.397 μs (5%) |           |  47.36 KiB (1%) |         381 |
| `["overhead", "stoppable=true"]`                    | 189.502 μs (5%) |           | 139.67 KiB (1%) |        2464 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   4.208 ms (5%) |           | 730.06 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   5.016 ms (5%) |           |   1.79 MiB (1%) |         213 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   4.594 ms (5%) |           |   1.43 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  15.714 ms (5%) |           |   1.22 MiB (1%) |         159 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  20.546 ms (5%) |           |   1.01 MiB (1%) |        1029 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  19.070 ms (5%) |           |   1.24 MiB (1%) |         664 |
| `["parallel_histogram", "seq"]`                     |   7.505 ms (5%) |           | 364.61 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  39.568 ms (5%) |           |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  19.847 ms (5%) |           |   2.66 KiB (1%) |          48 |
| `["splitby", "count", "foldl"]`                     |   4.825 ms (5%) |           |   96 bytes (1%) |           4 |
| `["splitby", "count", "man"]`                       |   1.882 ms (5%) |           |                 |             |
| `["splitby", "count", "reduce"]`                    |   1.028 ms (5%) |           |   2.81 KiB (1%) |          54 |
| `["sum", "random", "foldl"]`                        |  15.435 ms (5%) |           |   32 bytes (1%) |           2 |
| `["sum", "random", "reduce", "basesize=128"]`       |   7.949 ms (5%) |           | 103.23 KiB (1%) |        1018 |
| `["sum", "random", "reduce", "basesize=256"]`       |   7.840 ms (5%) |           |  51.23 KiB (1%) |         506 |
| `["sum", "random", "reduce", "basesize=512"]`       |   7.792 ms (5%) |           |  25.30 KiB (1%) |         252 |
| `["sum", "uniform", "foldl"]`                       |  15.097 ms (5%) |           |   32 bytes (1%) |           2 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   7.782 ms (5%) |           | 103.23 KiB (1%) |        1018 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   7.670 ms (5%) |           |  51.23 KiB (1%) |         506 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   7.602 ms (5%) |           |  25.25 KiB (1%) |         251 |
| `["sum", "valley", "foldl"]`                        |  15.628 ms (5%) |           |   32 bytes (1%) |           2 |
| `["sum", "valley", "reduce", "basesize=128"]`       |   8.057 ms (5%) |           | 103.23 KiB (1%) |        1018 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   7.974 ms (5%) |           |  51.23 KiB (1%) |         506 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   7.891 ms (5%) |           |  25.25 KiB (1%) |         251 |
| `["words", "nthreads=1"]`                           |  28.345 ms (5%) |           |  32.03 MiB (1%) |     1043674 |
| `["words", "nthreads=2"]`                           |  16.525 ms (5%) |           |  32.39 MiB (1%) |     1043710 |
| `["words", "nthreads=4"]`                           |  17.217 ms (5%) |           |  33.28 MiB (1%) |     1043842 |

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
  uname: Linux 5.4.0-1043-azure #45-Ubuntu SMP Fri Mar 19 17:33:38 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz: 
              speed         user         nice          sys         idle          irq
       #1  2294 MHz      84166 s         28 s       3915 s      78672 s          0 s
       #2  2294 MHz      86294 s          2 s       4198 s      76225 s          0 s
       
  Memory: 6.791343688964844 GB (3626.12109375 MB free)
  Uptime: 1684.0 sec
  Load Avg:  1.48046875  1.4990234375  1.13427734375
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
    CPU MHz:                         2294.684
    BogoMIPS:                        4589.36
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

