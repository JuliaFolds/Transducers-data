# Multi-thread benchmark result

* Pull request commit: [`13d185049319d16509e1d0880daddcd011c9f38f`](https://github.com/JuliaFolds/Transducers.jl/commit/13d185049319d16509e1d0880daddcd011c9f38f)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/243> (Update */Manifest.toml)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 9 Nov 2021 - 01:19
    - Baseline: 9 Nov 2021 - 01:25
* Package commits:
    - Target: a8fc42
    - Baseline: ed4189
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
| `["collect", "unordered", "basesize=1"]`            |                1.06 (5%) :x: |                   1.00 (1%)  |
| `["collect", "unordered", "basesize=1024"]`         |                   1.01 (5%)  |                1.05 (1%) :x: |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` |                   0.97 (5%)  | 0.93 (1%) :white_check_mark: |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 0.82 (5%) :white_check_mark: | 0.88 (1%) :white_check_mark: |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` |                   1.02 (5%)  | 0.98 (1%) :white_check_mark: |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  |                   0.97 (5%)  | 0.97 (1%) :white_check_mark: |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  |                1.06 (5%) :x: | 0.98 (1%) :white_check_mark: |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  |                   1.04 (5%)  |                1.03 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |                2.70 (5%) :x: |                2.19 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |                1.22 (5%) :x: |                1.03 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |                1.26 (5%) :x: |                1.16 (1%) :x: |
| `["parallel_histogram", "comm", "basesize=4096"]`   | 0.91 (5%) :white_check_mark: | 0.97 (1%) :white_check_mark: |

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
      Ubuntu 20.04.3 LTS
  uname: Linux 5.11.0-1020-azure #21~20.04.1-Ubuntu SMP Mon Oct 11 18:54:28 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v3 @ 2.40GHz: 
              speed         user         nice          sys         idle          irq
       #1  2397 MHz      57986 s         15 s       2572 s      36427 s          0 s
       #2  2397 MHz      56834 s          8 s       2999 s      37288 s          0 s
       
  Memory: 6.7889862060546875 GB (3011.45703125 MB free)
  Uptime: 980.0 sec
  Load Avg:  1.5830078125  1.46142578125  0.91650390625
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, haswell)
```

### Baseline
```
Julia Version 1.5.4
Commit 69fcb5745b (2021-03-11 19:13 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 20.04.3 LTS
  uname: Linux 5.11.0-1020-azure #21~20.04.1-Ubuntu SMP Mon Oct 11 18:54:28 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v3 @ 2.40GHz: 
              speed         user         nice          sys         idle          irq
       #1  2397 MHz      79648 s         15 s       3150 s      50543 s          0 s
       #2  2397 MHz      89001 s          8 s       3678 s      40866 s          0 s
       
  Memory: 6.7889862060546875 GB (2966.08203125 MB free)
  Uptime: 1345.0 sec
  Load Avg:  1.48681640625  1.49169921875  1.1064453125
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, haswell)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 9 Nov 2021 - 1:19
* Package commit: a8fc42
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

| ID                                                  | time            | GC time | memory          | allocations |
|-----------------------------------------------------|----------------:|--------:|----------------:|------------:|
| `["collect", "assoc", "basesize=1"]`                | 304.900 ms (5%) |         |  32.66 MiB (1%) |      286752 |
| `["collect", "assoc", "basesize=1024"]`             | 254.670 ms (5%) |         |   1.79 MiB (1%) |         570 |
| `["collect", "assoc", "basesize=32"]`               | 258.344 ms (5%) |         |   3.97 MiB (1%) |       13305 |
| `["collect", "seq"]`                                | 513.114 ms (5%) |         | 512.72 KiB (1%) |          15 |
| `["collect", "unordered", "basesize=1"]`            | 554.475 ms (5%) |         |  30.02 MiB (1%) |      360782 |
| `["collect", "unordered", "basesize=1024"]`         | 326.873 ms (5%) |         | 876.86 KiB (1%) |        4799 |
| `["collect", "unordered", "basesize=32"]`           | 287.015 ms (5%) |         |   1.47 MiB (1%) |       12560 |
| `["findfirst", "n=1000", "foldl"]`                  | 748.095 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 446.073 ms (5%) |         | 726.30 KiB (1%) |       12725 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 502.040 ms (5%) |         | 466.45 KiB (1%) |        8173 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 696.283 ms (5%) |         | 328.97 KiB (1%) |        5773 |
| `["findfirst", "n=400", "foldl"]`                   | 568.165 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 297.434 ms (5%) |         |   1.09 MiB (1%) |       19585 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 322.678 ms (5%) |         | 593.20 KiB (1%) |       10463 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 333.024 ms (5%) |         | 350.50 KiB (1%) |        6181 |
| `["findfirst", "n=500", "foldl"]`                   |  96.659 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 232.058 ms (5%) |         | 824.95 KiB (1%) |       14399 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 219.092 ms (5%) |         | 430.92 KiB (1%) |        7517 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 166.413 ms (5%) |         | 215.53 KiB (1%) |        3753 |
| `["overhead", "default"]`                           |  61.301 μs (5%) |         |  47.36 KiB (1%) |         382 |
| `["overhead", "stoppable=false"]`                   |  60.901 μs (5%) |         |  47.39 KiB (1%) |         382 |
| `["overhead", "stoppable=true"]`                    | 180.405 μs (5%) |         | 139.67 KiB (1%) |        2464 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   4.805 ms (5%) |         | 730.06 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   5.676 ms (5%) |         |   1.79 MiB (1%) |         213 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   5.182 ms (5%) |         |   1.43 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  12.728 ms (5%) |         |   1.22 MiB (1%) |         146 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  19.320 ms (5%) |         |   1.00 MiB (1%) |        1044 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  15.285 ms (5%) |         |   1.23 MiB (1%) |         516 |
| `["parallel_histogram", "seq"]`                     |   8.620 ms (5%) |         | 364.61 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  65.310 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  32.385 ms (5%) |         |   2.66 KiB (1%) |          48 |
| `["splitby", "count", "foldl"]`                     |   4.506 ms (5%) |         |   96 bytes (1%) |           4 |
| `["splitby", "count", "man"]`                       |   1.727 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    |   1.007 ms (5%) |         |   2.88 KiB (1%) |          55 |
| `["sum", "random", "foldl"]`                        |  18.724 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "random", "reduce", "basesize=128"]`       |   9.507 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "random", "reduce", "basesize=256"]`       |   9.405 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "random", "reduce", "basesize=512"]`       |   9.364 ms (5%) |         |  25.30 KiB (1%) |         252 |
| `["sum", "uniform", "foldl"]`                       |  18.143 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   9.374 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   9.213 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   9.166 ms (5%) |         |  25.25 KiB (1%) |         251 |
| `["sum", "valley", "foldl"]`                        |  18.676 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "valley", "reduce", "basesize=128"]`       |   9.605 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   9.503 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   9.476 ms (5%) |         |  25.25 KiB (1%) |         251 |
| `["words", "nthreads=1"]`                           |  27.891 ms (5%) |         |  31.72 MiB (1%) |     1033546 |
| `["words", "nthreads=2"]`                           |  16.636 ms (5%) |         |  32.08 MiB (1%) |     1033593 |
| `["words", "nthreads=4"]`                           |  17.267 ms (5%) |         |  32.97 MiB (1%) |     1033740 |

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
      Ubuntu 20.04.3 LTS
  uname: Linux 5.11.0-1020-azure #21~20.04.1-Ubuntu SMP Mon Oct 11 18:54:28 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v3 @ 2.40GHz: 
              speed         user         nice          sys         idle          irq
       #1  2397 MHz      57986 s         15 s       2572 s      36427 s          0 s
       #2  2397 MHz      56834 s          8 s       2999 s      37288 s          0 s
       
  Memory: 6.7889862060546875 GB (3011.45703125 MB free)
  Uptime: 980.0 sec
  Load Avg:  1.5830078125  1.46142578125  0.91650390625
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, haswell)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 9 Nov 2021 - 1:25
* Package commit: ed4189
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
| `["collect", "assoc", "basesize=1"]`                | 302.818 ms (5%) |           |  32.66 MiB (1%) |      286756 |
| `["collect", "assoc", "basesize=1024"]`             | 257.204 ms (5%) |           |   1.79 MiB (1%) |         570 |
| `["collect", "assoc", "basesize=32"]`               | 259.078 ms (5%) |           |   3.97 MiB (1%) |       13307 |
| `["collect", "seq"]`                                | 512.545 ms (5%) |           | 512.72 KiB (1%) |          15 |
| `["collect", "unordered", "basesize=1"]`            | 522.990 ms (5%) | 12.552 ms |  30.01 MiB (1%) |      360645 |
| `["collect", "unordered", "basesize=1024"]`         | 324.368 ms (5%) |           | 836.92 KiB (1%) |        3521 |
| `["collect", "unordered", "basesize=32"]`           | 280.822 ms (5%) |           |   1.48 MiB (1%) |       12704 |
| `["findfirst", "n=1000", "foldl"]`                  | 749.273 ms (5%) |           |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 459.581 ms (5%) |           | 781.91 KiB (1%) |       13691 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 609.272 ms (5%) |           | 529.53 KiB (1%) |        9302 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 684.135 ms (5%) |           | 335.88 KiB (1%) |        5891 |
| `["findfirst", "n=400", "foldl"]`                   | 558.948 ms (5%) |           |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 307.621 ms (5%) |           |   1.12 MiB (1%) |       20101 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 304.704 ms (5%) |           | 604.52 KiB (1%) |       10652 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 321.331 ms (5%) |           | 339.06 KiB (1%) |        5985 |
| `["findfirst", "n=500", "foldl"]`                   |  92.934 ms (5%) |           |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |  85.813 ms (5%) |           | 376.80 KiB (1%) |        6571 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 179.293 ms (5%) |           | 416.69 KiB (1%) |        7252 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 132.228 ms (5%) |           | 185.75 KiB (1%) |        3243 |
| `["overhead", "default"]`                           |  59.101 μs (5%) |           |  47.36 KiB (1%) |         382 |
| `["overhead", "stoppable=false"]`                   |  60.202 μs (5%) |           |  47.39 KiB (1%) |         382 |
| `["overhead", "stoppable=true"]`                    | 174.704 μs (5%) |           | 139.64 KiB (1%) |        2463 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   4.661 ms (5%) |           | 730.06 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   5.496 ms (5%) |           |   1.79 MiB (1%) |         213 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   5.148 ms (5%) |           |   1.43 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  12.822 ms (5%) |           |   1.22 MiB (1%) |         194 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  21.166 ms (5%) |           |   1.03 MiB (1%) |        1613 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  15.061 ms (5%) |           |   1.23 MiB (1%) |         389 |
| `["parallel_histogram", "seq"]`                     |   8.521 ms (5%) |           | 364.61 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  64.746 ms (5%) |           |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  32.039 ms (5%) |           |   2.66 KiB (1%) |          48 |
| `["splitby", "count", "foldl"]`                     |   4.499 ms (5%) |           |   96 bytes (1%) |           4 |
| `["splitby", "count", "man"]`                       |   1.731 ms (5%) |           |                 |             |
| `["splitby", "count", "reduce"]`                    | 989.126 μs (5%) |           |   2.88 KiB (1%) |          55 |
| `["sum", "random", "foldl"]`                        |  18.168 ms (5%) |           |   32 bytes (1%) |           2 |
| `["sum", "random", "reduce", "basesize=128"]`       |   9.492 ms (5%) |           | 103.23 KiB (1%) |        1018 |
| `["sum", "random", "reduce", "basesize=256"]`       |   9.389 ms (5%) |           |  51.23 KiB (1%) |         506 |
| `["sum", "random", "reduce", "basesize=512"]`       |   9.330 ms (5%) |           |  25.30 KiB (1%) |         252 |
| `["sum", "uniform", "foldl"]`                       |  17.798 ms (5%) |           |   32 bytes (1%) |           2 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   9.317 ms (5%) |           | 103.23 KiB (1%) |        1018 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   9.109 ms (5%) |           |  51.23 KiB (1%) |         506 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   9.102 ms (5%) |           |  25.25 KiB (1%) |         251 |
| `["sum", "valley", "foldl"]`                        |  18.804 ms (5%) |           |   32 bytes (1%) |           2 |
| `["sum", "valley", "reduce", "basesize=128"]`       |   9.637 ms (5%) |           | 103.23 KiB (1%) |        1018 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   9.526 ms (5%) |           |  51.23 KiB (1%) |         506 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   9.436 ms (5%) |           |  25.25 KiB (1%) |         251 |
| `["words", "nthreads=1"]`                           |  26.767 ms (5%) |           |  31.53 MiB (1%) |     1027149 |
| `["words", "nthreads=2"]`                           |  17.364 ms (5%) |           |  32.25 MiB (1%) |     1027223 |
| `["words", "nthreads=4"]`                           |  17.981 ms (5%) |           |  32.88 MiB (1%) |     1027385 |

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
      Ubuntu 20.04.3 LTS
  uname: Linux 5.11.0-1020-azure #21~20.04.1-Ubuntu SMP Mon Oct 11 18:54:28 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v3 @ 2.40GHz: 
              speed         user         nice          sys         idle          irq
       #1  2397 MHz      79648 s         15 s       3150 s      50543 s          0 s
       #2  2397 MHz      89001 s          8 s       3678 s      40866 s          0 s
       
  Memory: 6.7889862060546875 GB (2966.08203125 MB free)
  Uptime: 1345.0 sec
  Load Avg:  1.48681640625  1.49169921875  1.1064453125
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, haswell)
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
    Model:                           63
    Model name:                      Intel(R) Xeon(R) CPU E5-2673 v3 @ 2.40GHz
    Stepping:                        2
    CPU MHz:                         2397.222
    BogoMIPS:                        4794.44
    Hypervisor vendor:               Microsoft
    Virtualization type:             full
    L1d cache:                       64 KiB
    L1i cache:                       64 KiB
    L2 cache:                        512 KiB
    L3 cache:                        30 MiB
    NUMA node0 CPU(s):               0,1
    Vulnerability Itlb multihit:     KVM: Mitigation: VMX unsupported
    Vulnerability L1tf:              Mitigation; PTE Inversion
    Vulnerability Mds:               Mitigation; Clear CPU buffers; SMT Host state unknown
    Vulnerability Meltdown:          Mitigation; PTI
    Vulnerability Spec store bypass: Vulnerable
    Vulnerability Spectre v1:        Mitigation; usercopy/swapgs barriers and __user pointer sanitization
    Vulnerability Spectre v2:        Mitigation; Full generic retpoline, STIBP disabled, RSB filling
    Vulnerability Srbds:             Not affected
    Vulnerability Tsx async abort:   Not affected
    Flags:                           fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush mmx fxsr sse sse2 ss ht syscall nx pdpe1gb rdtscp lm constant_tsc rep_good nopl xtopology cpuid pni pclmulqdq ssse3 fma cx16 pcid sse4_1 sse4_2 movbe popcnt aes xsave avx f16c rdrand hypervisor lahf_lm abm invpcid_single pti fsgsbase bmi1 avx2 smep bmi2 erms invpcid xsaveopt md_clear
    

| Cpu Property       | Value                                                   |
|:------------------ |:------------------------------------------------------- |
| Brand              | Intel(R) Xeon(R) CPU E5-2673 v3 @ 2.40GHz               |
| Vendor             | :Intel                                                  |
| Architecture       | :Haswell                                                |
| Model              | Family: 0x06, Model: 0x3f, Stepping: 0x02, Type: 0x00   |
| Cores              | 2 physical cores, 2 logical cores (on executing CPU)    |
|                    | No Hyperthreading hardware capability detected          |
| Clock Frequencies  | Not supported by CPU                                    |
| Data Cache         | Level 1:3 : (32, 256, 30720) kbytes                     |
|                    | 64 byte cache line size                                 |
| Address Size       | 48 bits virtual, 46 bits physical                       |
| SIMD               | 256 bit = 32 byte max. SIMD vector size                 |
| Time Stamp Counter | TSC is accessible via `rdtsc`                           |
|                    | TSC increased at every clock cycle (non-invariant TSC)  |
| Perf. Monitoring   | Performance Monitoring Counters (PMC) are not supported |
| Hypervisor         | Yes, Microsoft                                          |

