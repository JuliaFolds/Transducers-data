# Multi-thread benchmark result

* Pull request commit: [`440db01921f2dda504b23c1cfd417b938574d91a`](https://github.com/JuliaFolds/Transducers.jl/commit/440db01921f2dda504b23c1cfd417b938574d91a)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/388> (Deprecate `reduce` and `dreduce`)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 1 Aug 2020 - 06:21
    - Baseline: 1 Aug 2020 - 06:26
* Package commits:
    - Target: ec6d2b
    - Baseline: d1995c
* Julia commits:
    - Target: 44fa15
    - Baseline: 44fa15
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

| ID                                                  | time ratio                   | memory ratio  |
|-----------------------------------------------------|------------------------------|---------------|
| `["collect", "assoc", "basesize=1024"]`             | 0.92 (5%) :white_check_mark: |    1.00 (1%)  |
| `["collect", "assoc", "basesize=32"]`               | 0.94 (5%) :white_check_mark: |    1.00 (1%)  |
| `["collect", "seq"]`                                | 0.95 (5%) :white_check_mark: |    1.00 (1%)  |
| `["collect", "unordered", "basesize=1"]`            | 0.95 (5%) :white_check_mark: |    1.00 (1%)  |
| `["collect", "unordered", "basesize=1024"]`         | 0.88 (5%) :white_check_mark: | 1.09 (1%) :x: |
| `["collect", "unordered", "basesize=32"]`           | 0.94 (5%) :white_check_mark: |    1.00 (1%)  |
| `["findfirst", "n=1000", "foldl"]`                  |                1.06 (5%) :x: |    1.00 (1%)  |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 0.91 (5%) :white_check_mark: |    1.00 (1%)  |
| `["findfirst", "n=400", "foldl"]`                   |                1.06 (5%) :x: |    1.00 (1%)  |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  |                1.05 (5%) :x: |    1.00 (1%)  |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 0.91 (5%) :white_check_mark: |    1.00 (1%)  |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 0.90 (5%) :white_check_mark: |    1.00 (1%)  |
| `["overhead", "default"]`                           | 0.87 (5%) :white_check_mark: |    1.00 (1%)  |
| `["overhead", "stoppable=true"]`                    | 0.83 (5%) :white_check_mark: |    1.00 (1%)  |
| `["parallel_histogram", "assoc", "basesize=16384"]` | 0.77 (5%) :white_check_mark: |    1.00 (1%)  |
| `["parallel_histogram", "assoc", "basesize=4096"]`  | 0.79 (5%) :white_check_mark: |    1.00 (1%)  |
| `["parallel_histogram", "assoc", "basesize=8192"]`  | 0.76 (5%) :white_check_mark: |    1.00 (1%)  |
| `["parallel_histogram", "comm", "basesize=16384"]`  | 0.93 (5%) :white_check_mark: |    1.00 (1%)  |
| `["parallel_histogram", "comm", "basesize=4096"]`   |                1.06 (5%) :x: |    1.00 (1%)  |
| `["parallel_histogram", "comm", "basesize=8192"]`   |                1.12 (5%) :x: |    1.01 (1%)  |
| `["parallel_histogram", "seq"]`                     | 0.89 (5%) :white_check_mark: |    1.00 (1%)  |
| `["sum", "random", "reduce", "basesize=128"]`       |                1.14 (5%) :x: |    1.00 (1%)  |
| `["sum", "uniform", "reduce", "basesize=128"]`      | 0.79 (5%) :white_check_mark: |    1.00 (1%)  |
| `["sum", "uniform", "reduce", "basesize=256"]`      | 0.90 (5%) :white_check_mark: |    1.00 (1%)  |
| `["sum", "valley", "foldl"]`                        |                1.14 (5%) :x: |    1.00 (1%)  |
| `["sum", "valley", "reduce", "basesize=256"]`       | 0.93 (5%) :white_check_mark: |    1.00 (1%)  |
| `["words", "nthreads=1"]`                           | 0.91 (5%) :white_check_mark: | 1.01 (1%) :x: |
| `["words", "nthreads=2"]`                           |                   0.95 (5%)  | 1.01 (1%) :x: |
| `["words", "nthreads=4"]`                           | 0.91 (5%) :white_check_mark: | 1.02 (1%) :x: |

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
Julia Version 1.4.2
Commit 44fa15b150* (2020-05-23 18:35 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 18.04.4 LTS
  uname: Linux 5.3.0-1032-azure #33~18.04.1-Ubuntu SMP Fri Jun 26 15:01:15 UTC 2020 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz      50808 s          0 s       2643 s      19787 s          0 s
       #2  2095 MHz      52032 s          0 s       2610 s      19440 s          0 s
       
  Memory: 6.764884948730469 GB (2927.859375 MB free)
  Uptime: 763.0 sec
  Load Avg:  1.73193359375  1.5166015625  0.93017578125
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, skylake)
```

### Baseline
```
Julia Version 1.4.2
Commit 44fa15b150* (2020-05-23 18:35 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 18.04.4 LTS
  uname: Linux 5.3.0-1032-azure #33~18.04.1-Ubuntu SMP Fri Jun 26 15:01:15 UTC 2020 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz      70801 s          0 s       3324 s      27407 s          0 s
       #2  2095 MHz      78109 s          0 s       3226 s      22494 s          0 s
       
  Memory: 6.764884948730469 GB (2662.91015625 MB free)
  Uptime: 1068.0 sec
  Load Avg:  2.60009765625  1.892578125  1.23193359375
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, skylake)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 1 Aug 2020 - 6:21
* Package commit: ec6d2b
* Julia commit: 44fa15
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
| `["collect", "assoc", "basesize=1"]`                | 385.614 ms (5%) | 11.847 ms |  87.55 MiB (1%) |     1590743 |
| `["collect", "assoc", "basesize=1024"]`             | 221.100 ms (5%) |           |   1.84 MiB (1%) |        1812 |
| `["collect", "assoc", "basesize=32"]`               | 229.997 ms (5%) |           |   5.64 MiB (1%) |       54011 |
| `["collect", "seq"]`                                | 431.627 ms (5%) |           |   1.50 MiB (1%) |       32784 |
| `["collect", "unordered", "basesize=1"]`            | 477.718 ms (5%) |           |  29.17 MiB (1%) |      404250 |
| `["collect", "unordered", "basesize=1024"]`         | 288.439 ms (5%) |           | 831.38 KiB (1%) |        6300 |
| `["collect", "unordered", "basesize=32"]`           | 249.110 ms (5%) |           |   1.47 MiB (1%) |       16917 |
| `["findfirst", "n=1000", "foldl"]`                  | 684.581 ms (5%) |           |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 354.208 ms (5%) |           | 563.95 KiB (1%) |       10220 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 346.805 ms (5%) |           | 287.31 KiB (1%) |        5226 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 362.195 ms (5%) |           | 149.41 KiB (1%) |        2727 |
| `["findfirst", "n=400", "foldl"]`                   | 511.730 ms (5%) |           |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 259.626 ms (5%) |           |   1.02 MiB (1%) |       18911 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 266.784 ms (5%) |           | 525.88 KiB (1%) |        9552 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 260.740 ms (5%) |           | 267.09 KiB (1%) |        4867 |
| `["findfirst", "n=500", "foldl"]`                   |  83.527 ms (5%) |           |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |  41.755 ms (5%) |           | 157.25 KiB (1%) |        2841 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |  40.926 ms (5%) |           |  84.52 KiB (1%) |        1531 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  46.495 ms (5%) |           |  48.30 KiB (1%) |         878 |
| `["overhead", "default"]`                           | 162.910 μs (5%) |           | 146.25 KiB (1%) |        2632 |
| `["overhead", "stoppable=false"]`                   | 185.211 μs (5%) |           | 146.28 KiB (1%) |        2633 |
| `["overhead", "stoppable=true"]`                    | 270.515 μs (5%) |           | 146.53 KiB (1%) |        2649 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   3.852 ms (5%) |           | 732.06 KiB (1%) |         103 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   4.355 ms (5%) |           |   2.07 MiB (1%) |         503 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   4.081 ms (5%) |           |   1.43 MiB (1%) |         243 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  14.801 ms (5%) |           |   1.22 MiB (1%) |         159 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  23.955 ms (5%) |           |   1.05 MiB (1%) |        5013 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  20.984 ms (5%) |           |   1.25 MiB (1%) |        2208 |
| `["parallel_histogram", "seq"]`                     |   7.574 ms (5%) |           | 364.61 KiB (1%) |          24 |
| `["sum", "random", "foldl"]`                        |  14.991 ms (5%) |           |   64 bytes (1%) |           3 |
| `["sum", "random", "reduce", "basesize=128"]`       |   9.144 ms (5%) |           | 313.33 KiB (1%) |        6065 |
| `["sum", "random", "reduce", "basesize=256"]`       |   7.977 ms (5%) |           | 155.14 KiB (1%) |        3012 |
| `["sum", "random", "reduce", "basesize=512"]`       |   7.657 ms (5%) |           |  76.30 KiB (1%) |        1485 |
| `["sum", "uniform", "foldl"]`                       |  14.224 ms (5%) |           |   64 bytes (1%) |           3 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   7.469 ms (5%) |           | 313.42 KiB (1%) |        6071 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   7.180 ms (5%) |           | 155.14 KiB (1%) |        3012 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   7.341 ms (5%) |           |  76.31 KiB (1%) |        1486 |
| `["sum", "valley", "foldl"]`                        |  16.834 ms (5%) |           |   64 bytes (1%) |           3 |
| `["sum", "valley", "reduce", "basesize=128"]`       |   7.951 ms (5%) |           | 313.33 KiB (1%) |        6065 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   7.484 ms (5%) |           | 155.13 KiB (1%) |        3011 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   7.565 ms (5%) |           |  76.31 KiB (1%) |        1486 |
| `["words", "nthreads=1"]`                           |  45.604 ms (5%) |  7.671 ms |  63.37 MiB (1%) |     2070510 |
| `["words", "nthreads=2"]`                           |  23.986 ms (5%) |           |  63.97 MiB (1%) |     2078635 |
| `["words", "nthreads=4"]`                           |  24.182 ms (5%) |           |  65.25 MiB (1%) |     2091186 |

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
Julia Version 1.4.2
Commit 44fa15b150* (2020-05-23 18:35 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 18.04.4 LTS
  uname: Linux 5.3.0-1032-azure #33~18.04.1-Ubuntu SMP Fri Jun 26 15:01:15 UTC 2020 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz      50808 s          0 s       2643 s      19787 s          0 s
       #2  2095 MHz      52032 s          0 s       2610 s      19440 s          0 s
       
  Memory: 6.764884948730469 GB (2927.859375 MB free)
  Uptime: 763.0 sec
  Load Avg:  1.73193359375  1.5166015625  0.93017578125
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, skylake)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 1 Aug 2020 - 6:26
* Package commit: d1995c
* Julia commit: 44fa15
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
| `["collect", "assoc", "basesize=1"]`                | 392.913 ms (5%) | 11.657 ms |  87.55 MiB (1%) |     1590796 |
| `["collect", "assoc", "basesize=1024"]`             | 239.905 ms (5%) |           |   1.84 MiB (1%) |        1812 |
| `["collect", "assoc", "basesize=32"]`               | 245.170 ms (5%) |           |   5.64 MiB (1%) |       54018 |
| `["collect", "seq"]`                                | 455.709 ms (5%) |           |   1.50 MiB (1%) |       32784 |
| `["collect", "unordered", "basesize=1"]`            | 505.373 ms (5%) |           |  29.10 MiB (1%) |      399672 |
| `["collect", "unordered", "basesize=1024"]`         | 328.880 ms (5%) |           | 759.67 KiB (1%) |        1711 |
| `["collect", "unordered", "basesize=32"]`           | 264.251 ms (5%) |           |   1.47 MiB (1%) |       16630 |
| `["findfirst", "n=1000", "foldl"]`                  | 648.205 ms (5%) |           |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 363.129 ms (5%) |           | 563.86 KiB (1%) |       10218 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 380.798 ms (5%) |           | 287.16 KiB (1%) |        5220 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 380.493 ms (5%) |           | 149.27 KiB (1%) |        2722 |
| `["findfirst", "n=400", "foldl"]`                   | 483.333 ms (5%) |           |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 260.850 ms (5%) |           |   1.02 MiB (1%) |       18888 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 253.445 ms (5%) |           | 525.94 KiB (1%) |        9560 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 260.974 ms (5%) |           | 267.16 KiB (1%) |        4875 |
| `["findfirst", "n=500", "foldl"]`                   |  84.206 ms (5%) |           |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |  43.827 ms (5%) |           | 157.22 KiB (1%) |        2843 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |  45.068 ms (5%) |           |  84.41 KiB (1%) |        1528 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  51.650 ms (5%) |           |  48.19 KiB (1%) |         875 |
| `["overhead", "default"]`                           | 187.221 μs (5%) |           | 146.14 KiB (1%) |        2628 |
| `["overhead", "stoppable=false"]`                   | 189.221 μs (5%) |           | 146.16 KiB (1%) |        2629 |
| `["overhead", "stoppable=true"]`                    | 325.936 μs (5%) |           | 146.41 KiB (1%) |        2645 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   5.007 ms (5%) |           | 732.02 KiB (1%) |         101 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   5.539 ms (5%) |           |   2.07 MiB (1%) |         501 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   5.395 ms (5%) |           |   1.43 MiB (1%) |         240 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  15.882 ms (5%) |           |   1.22 MiB (1%) |         157 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  22.676 ms (5%) |           |   1.05 MiB (1%) |        3482 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  18.702 ms (5%) |           |   1.24 MiB (1%) |        1635 |
| `["parallel_histogram", "seq"]`                     |   8.554 ms (5%) |           | 364.61 KiB (1%) |          24 |
| `["sum", "random", "foldl"]`                        |  14.700 ms (5%) |           |   64 bytes (1%) |           3 |
| `["sum", "random", "reduce", "basesize=128"]`       |   8.039 ms (5%) |           | 313.38 KiB (1%) |        6070 |
| `["sum", "random", "reduce", "basesize=256"]`       |   8.374 ms (5%) |           | 155.11 KiB (1%) |        3012 |
| `["sum", "random", "reduce", "basesize=512"]`       |   7.831 ms (5%) |           |  76.30 KiB (1%) |        1487 |
| `["sum", "uniform", "foldl"]`                       |  14.232 ms (5%) |           |   64 bytes (1%) |           3 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   9.437 ms (5%) |           | 313.33 KiB (1%) |        6067 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   7.943 ms (5%) |           | 155.08 KiB (1%) |        3010 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   7.600 ms (5%) |           |  76.27 KiB (1%) |        1485 |
| `["sum", "valley", "foldl"]`                        |  14.768 ms (5%) |           |   64 bytes (1%) |           3 |
| `["sum", "valley", "reduce", "basesize=128"]`       |   7.965 ms (5%) |           | 313.28 KiB (1%) |        6064 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   8.042 ms (5%) |           | 155.05 KiB (1%) |        3008 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   7.635 ms (5%) |           |  76.25 KiB (1%) |        1484 |
| `["words", "nthreads=1"]`                           |  49.873 ms (5%) |  7.258 ms |  62.69 MiB (1%) |     2048350 |
| `["words", "nthreads=2"]`                           |  25.125 ms (5%) |           |  63.30 MiB (1%) |     2056466 |
| `["words", "nthreads=4"]`                           |  26.570 ms (5%) |           |  64.26 MiB (1%) |     2064687 |

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
Julia Version 1.4.2
Commit 44fa15b150* (2020-05-23 18:35 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 18.04.4 LTS
  uname: Linux 5.3.0-1032-azure #33~18.04.1-Ubuntu SMP Fri Jun 26 15:01:15 UTC 2020 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz      70801 s          0 s       3324 s      27407 s          0 s
       #2  2095 MHz      78109 s          0 s       3226 s      22494 s          0 s
       
  Memory: 6.764884948730469 GB (2662.91015625 MB free)
  Uptime: 1068.0 sec
  Load Avg:  2.60009765625  1.892578125  1.23193359375
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, skylake)
```

---
# Runtime information
| Runtime Info | |
|:--|:--|
| BLAS #threads | 2 |
| `BLAS.vendor()` | `openblas64` |
| `Sys.CPU_THREADS` | 2 |

`lscpu` output:

    Architecture:        x86_64
    CPU op-mode(s):      32-bit, 64-bit
    Byte Order:          Little Endian
    CPU(s):              2
    On-line CPU(s) list: 0,1
    Thread(s) per core:  1
    Core(s) per socket:  2
    Socket(s):           1
    NUMA node(s):        1
    Vendor ID:           GenuineIntel
    CPU family:          6
    Model:               85
    Model name:          Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz
    Stepping:            4
    CPU MHz:             2095.192
    BogoMIPS:            4190.38
    Hypervisor vendor:   Microsoft
    Virtualization type: full
    L1d cache:           32K
    L1i cache:           32K
    L2 cache:            1024K
    L3 cache:            36608K
    NUMA node0 CPU(s):   0,1
    Flags:               fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush mmx fxsr sse sse2 ss ht syscall nx pdpe1gb rdtscp lm constant_tsc rep_good nopl xtopology cpuid pni pclmulqdq ssse3 fma cx16 pcid sse4_1 sse4_2 movbe popcnt aes xsave avx f16c rdrand hypervisor lahf_lm abm 3dnowprefetch invpcid_single pti fsgsbase bmi1 hle avx2 smep bmi2 erms invpcid rtm mpx avx512f avx512dq rdseed adx smap clflushopt avx512cd avx512bw avx512vl xsaveopt xsavec xsaves md_clear
    

| Cpu Property       | Value                                                   |
|:------------------ |:------------------------------------------------------- |
| Brand              | Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz           |
| Vendor             | :Intel                                                  |
| Architecture       | :Skylake                                                |
| Model              | Family: 0x06, Model: 0x55, Stepping: 0x04, Type: 0x00   |
| Cores              | 2 physical cores, 2 logical cores (on executing CPU)    |
|                    | No Hyperthreading detected                              |
| Clock Frequencies  | Not supported by CPU                                    |
| Data Cache         | Level 1:3 : (32, 1024, 36608) kbytes                    |
|                    | 64 byte cache line size                                 |
| Address Size       | 48 bits virtual, 44 bits physical                       |
| SIMD               | 512 bit = 64 byte max. SIMD vector size                 |
| Time Stamp Counter | TSC is accessible via `rdtsc`                           |
|                    | TSC increased at every clock cycle (non-invariant TSC)  |
| Perf. Monitoring   | Performance Monitoring Counters (PMC) are not supported |
| Hypervisor         | Yes, Microsoft                                          |

