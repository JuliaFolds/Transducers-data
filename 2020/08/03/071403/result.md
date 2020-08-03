# Multi-thread benchmark result

* Pull request commit: [`0db99d28c356ee476ab5718f9b5bbfcea68af244`](https://github.com/JuliaFolds/Transducers.jl/commit/0db99d28c356ee476ab5718f9b5bbfcea68af244)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/390> (Use protected branch instead of manual listing in .mergify.yml)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 3 Aug 2020 - 07:08
    - Baseline: 3 Aug 2020 - 07:13
* Package commits:
    - Target: e31ba7
    - Baseline: 64beaa
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

| ID                                                  | time ratio    | memory ratio  |
|-----------------------------------------------------|---------------|---------------|
| `["collect", "assoc", "basesize=1"]`                | 1.11 (5%) :x: |    1.00 (1%)  |
| `["collect", "unordered", "basesize=1"]`            | 1.05 (5%) :x: |    1.00 (1%)  |
| `["collect", "unordered", "basesize=1024"]`         | 1.38 (5%) :x: | 1.22 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 1.08 (5%) :x: |    1.00 (1%)  |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 1.08 (5%) :x: |    1.00 (1%)  |
| `["overhead", "default"]`                           | 1.16 (5%) :x: |    1.00 (1%)  |
| `["overhead", "stoppable=false"]`                   | 1.16 (5%) :x: |    1.00 (1%)  |
| `["overhead", "stoppable=true"]`                    | 1.24 (5%) :x: |    1.00 (1%)  |
| `["parallel_histogram", "assoc", "basesize=16384"]` | 1.34 (5%) :x: |    1.00 (1%)  |
| `["parallel_histogram", "assoc", "basesize=4096"]`  | 1.36 (5%) :x: |    1.00 (1%)  |
| `["parallel_histogram", "assoc", "basesize=8192"]`  | 1.39 (5%) :x: |    1.00 (1%)  |
| `["parallel_histogram", "comm", "basesize=16384"]`  | 1.10 (5%) :x: |    1.00 (1%)  |
| `["parallel_histogram", "comm", "basesize=4096"]`   | 1.12 (5%) :x: | 1.02 (1%) :x: |
| `["parallel_histogram", "comm", "basesize=8192"]`   | 1.12 (5%) :x: |    1.00 (1%)  |
| `["parallel_histogram", "seq"]`                     | 1.27 (5%) :x: |    1.00 (1%)  |
| `["sum", "random", "foldl"]`                        | 1.15 (5%) :x: |    1.00 (1%)  |
| `["sum", "random", "reduce", "basesize=128"]`       | 1.08 (5%) :x: |    1.00 (1%)  |
| `["sum", "uniform", "reduce", "basesize=256"]`      | 1.15 (5%) :x: |    1.00 (1%)  |
| `["sum", "uniform", "reduce", "basesize=512"]`      | 1.14 (5%) :x: |    1.00 (1%)  |
| `["words", "nthreads=1"]`                           | 1.21 (5%) :x: |    1.00 (1%)  |
| `["words", "nthreads=2"]`                           | 1.14 (5%) :x: |    0.99 (1%)  |
| `["words", "nthreads=4"]`                           | 1.19 (5%) :x: |    1.00 (1%)  |

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
       #1  2095 MHz      50061 s          0 s       2350 s      18577 s          0 s
       #2  2095 MHz      51140 s          0 s       2596 s      17468 s          0 s
       
  Memory: 6.764884948730469 GB (2890.28515625 MB free)
  Uptime: 733.0 sec
  Load Avg:  1.7197265625  1.55859375  0.96630859375
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
       #1  2095 MHz      72429 s          0 s       2821 s      25032 s          0 s
       #2  2095 MHz      74055 s          0 s       3090 s      23528 s          0 s
       
  Memory: 6.764884948730469 GB (2890.20703125 MB free)
  Uptime: 1029.0 sec
  Load Avg:  1.65673828125  1.57763671875  1.1337890625
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, skylake)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 3 Aug 2020 - 7:8
* Package commit: e31ba7
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
| `["collect", "assoc", "basesize=1"]`                | 376.698 ms (5%) | 14.118 ms |  87.55 MiB (1%) |     1590793 |
| `["collect", "assoc", "basesize=1024"]`             | 239.744 ms (5%) |           |   1.84 MiB (1%) |        1811 |
| `["collect", "assoc", "basesize=32"]`               | 246.597 ms (5%) |           |   5.64 MiB (1%) |       54010 |
| `["collect", "seq"]`                                | 481.416 ms (5%) |           |   1.50 MiB (1%) |       32784 |
| `["collect", "unordered", "basesize=1"]`            | 476.277 ms (5%) |           |  29.15 MiB (1%) |      402719 |
| `["collect", "unordered", "basesize=1024"]`         | 380.709 ms (5%) |           | 947.59 KiB (1%) |       13738 |
| `["collect", "unordered", "basesize=32"]`           | 272.162 ms (5%) |           |   1.47 MiB (1%) |       16685 |
| `["findfirst", "n=1000", "foldl"]`                  | 756.105 ms (5%) |           |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 382.198 ms (5%) |           | 563.86 KiB (1%) |       10214 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 382.898 ms (5%) |           | 287.34 KiB (1%) |        5228 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 386.030 ms (5%) |           | 149.30 KiB (1%) |        2720 |
| `["findfirst", "n=400", "foldl"]`                   | 558.091 ms (5%) |           |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 281.672 ms (5%) |           |   1.02 MiB (1%) |       18978 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 286.386 ms (5%) |           | 525.98 KiB (1%) |        9559 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 281.205 ms (5%) |           | 267.31 KiB (1%) |        4881 |
| `["findfirst", "n=500", "foldl"]`                   |  95.482 ms (5%) |           |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |  50.140 ms (5%) |           | 157.33 KiB (1%) |        2846 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |  50.021 ms (5%) |           |  84.56 KiB (1%) |        1534 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  52.303 ms (5%) |           |  48.31 KiB (1%) |         879 |
| `["overhead", "default"]`                           | 180.402 μs (5%) |           | 146.25 KiB (1%) |        2632 |
| `["overhead", "stoppable=false"]`                   | 181.502 μs (5%) |           | 146.28 KiB (1%) |        2633 |
| `["overhead", "stoppable=true"]`                    | 354.503 μs (5%) |           | 146.55 KiB (1%) |        2650 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   4.926 ms (5%) |           | 732.06 KiB (1%) |         103 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   5.695 ms (5%) |           |   1.80 MiB (1%) |         497 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   5.453 ms (5%) |           |   1.43 MiB (1%) |         242 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  16.320 ms (5%) |           |   1.22 MiB (1%) |         159 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  26.265 ms (5%) |           |   1.07 MiB (1%) |        5896 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  21.434 ms (5%) |           |   1.27 MiB (1%) |        3244 |
| `["parallel_histogram", "seq"]`                     |   8.525 ms (5%) |           | 364.61 KiB (1%) |          24 |
| `["sum", "random", "foldl"]`                        |  18.453 ms (5%) |           |   64 bytes (1%) |           3 |
| `["sum", "random", "reduce", "basesize=128"]`       |   9.845 ms (5%) |           | 313.38 KiB (1%) |        6068 |
| `["sum", "random", "reduce", "basesize=256"]`       |   9.613 ms (5%) |           | 155.14 KiB (1%) |        3012 |
| `["sum", "random", "reduce", "basesize=512"]`       |   9.517 ms (5%) |           |  76.33 KiB (1%) |        1487 |
| `["sum", "uniform", "foldl"]`                       |  18.226 ms (5%) |           |   64 bytes (1%) |           3 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   9.748 ms (5%) |           | 313.44 KiB (1%) |        6072 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   9.664 ms (5%) |           | 155.16 KiB (1%) |        3013 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   9.468 ms (5%) |           |  76.31 KiB (1%) |        1486 |
| `["sum", "valley", "foldl"]`                        |  18.504 ms (5%) |           |   64 bytes (1%) |           3 |
| `["sum", "valley", "reduce", "basesize=128"]`       |   9.956 ms (5%) |           | 313.36 KiB (1%) |        6067 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   9.694 ms (5%) |           | 155.14 KiB (1%) |        3012 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   9.560 ms (5%) |           |  76.31 KiB (1%) |        1486 |
| `["words", "nthreads=1"]`                           |  47.772 ms (5%) |  7.339 ms |  63.52 MiB (1%) |     2075426 |
| `["words", "nthreads=2"]`                           |  24.189 ms (5%) |           |  64.13 MiB (1%) |     2083571 |
| `["words", "nthreads=4"]`                           |  24.375 ms (5%) |           |  65.09 MiB (1%) |     2091818 |

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
       #1  2095 MHz      50061 s          0 s       2350 s      18577 s          0 s
       #2  2095 MHz      51140 s          0 s       2596 s      17468 s          0 s
       
  Memory: 6.764884948730469 GB (2890.28515625 MB free)
  Uptime: 733.0 sec
  Load Avg:  1.7197265625  1.55859375  0.96630859375
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, skylake)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 3 Aug 2020 - 7:13
* Package commit: 64beaa
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
| `["collect", "assoc", "basesize=1"]`                | 338.191 ms (5%) | 13.112 ms |  87.55 MiB (1%) |     1590781 |
| `["collect", "assoc", "basesize=1024"]`             | 239.788 ms (5%) |           |   1.84 MiB (1%) |        1813 |
| `["collect", "assoc", "basesize=32"]`               | 244.210 ms (5%) |           |   5.64 MiB (1%) |       54023 |
| `["collect", "seq"]`                                | 472.806 ms (5%) |           |   1.50 MiB (1%) |       32784 |
| `["collect", "unordered", "basesize=1"]`            | 453.205 ms (5%) |           |  29.15 MiB (1%) |      402435 |
| `["collect", "unordered", "basesize=1024"]`         | 276.187 ms (5%) |           | 778.17 KiB (1%) |        2559 |
| `["collect", "unordered", "basesize=32"]`           | 268.939 ms (5%) |           |   1.46 MiB (1%) |       16032 |
| `["findfirst", "n=1000", "foldl"]`                  | 741.229 ms (5%) |           |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 378.181 ms (5%) |           | 564.14 KiB (1%) |       10232 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 375.504 ms (5%) |           | 287.25 KiB (1%) |        5222 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 378.396 ms (5%) |           | 149.38 KiB (1%) |        2725 |
| `["findfirst", "n=400", "foldl"]`                   | 550.628 ms (5%) |           |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 281.517 ms (5%) |           |   1.02 MiB (1%) |       18917 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 279.844 ms (5%) |           | 526.17 KiB (1%) |        9571 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 280.309 ms (5%) |           | 267.22 KiB (1%) |        4875 |
| `["findfirst", "n=500", "foldl"]`                   |  94.167 ms (5%) |           |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |  46.620 ms (5%) |           | 157.42 KiB (1%) |        2852 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |  46.268 ms (5%) |           |  84.56 KiB (1%) |        1534 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  50.172 ms (5%) |           |  48.31 KiB (1%) |         879 |
| `["overhead", "default"]`                           | 156.001 μs (5%) |           | 146.27 KiB (1%) |        2633 |
| `["overhead", "stoppable=false"]`                   | 156.101 μs (5%) |           | 146.28 KiB (1%) |        2633 |
| `["overhead", "stoppable=true"]`                    | 285.602 μs (5%) |           | 146.55 KiB (1%) |        2650 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   3.681 ms (5%) |           | 732.06 KiB (1%) |         103 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   4.192 ms (5%) |           |   1.80 MiB (1%) |         496 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   3.935 ms (5%) |           |   1.43 MiB (1%) |         243 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  14.808 ms (5%) |           |   1.22 MiB (1%) |         159 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  23.525 ms (5%) |           |   1.05 MiB (1%) |        5274 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  19.124 ms (5%) |           |   1.27 MiB (1%) |        3282 |
| `["parallel_histogram", "seq"]`                     |   6.723 ms (5%) |           | 364.61 KiB (1%) |          24 |
| `["sum", "random", "foldl"]`                        |  16.020 ms (5%) |           |   64 bytes (1%) |           3 |
| `["sum", "random", "reduce", "basesize=128"]`       |   9.144 ms (5%) |           | 313.36 KiB (1%) |        6067 |
| `["sum", "random", "reduce", "basesize=256"]`       |   9.309 ms (5%) |           | 155.14 KiB (1%) |        3012 |
| `["sum", "random", "reduce", "basesize=512"]`       |   9.077 ms (5%) |           |  76.31 KiB (1%) |        1486 |
| `["sum", "uniform", "foldl"]`                       |  17.571 ms (5%) |           |   64 bytes (1%) |           3 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   9.531 ms (5%) |           | 313.42 KiB (1%) |        6071 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   8.439 ms (5%) |           | 155.16 KiB (1%) |        3013 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   8.332 ms (5%) |           |  76.31 KiB (1%) |        1486 |
| `["sum", "valley", "foldl"]`                        |  18.468 ms (5%) |           |   64 bytes (1%) |           3 |
| `["sum", "valley", "reduce", "basesize=128"]`       |   9.696 ms (5%) |           | 313.30 KiB (1%) |        6063 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   9.515 ms (5%) |           | 155.14 KiB (1%) |        3012 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   9.569 ms (5%) |           |  76.31 KiB (1%) |        1486 |
| `["words", "nthreads=1"]`                           |  39.570 ms (5%) |  6.711 ms |  63.41 MiB (1%) |     2072191 |
| `["words", "nthreads=2"]`                           |  21.193 ms (5%) |           |  64.50 MiB (1%) |     2084512 |
| `["words", "nthreads=4"]`                           |  20.569 ms (5%) |           |  65.14 MiB (1%) |     2090779 |

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
       #1  2095 MHz      72429 s          0 s       2821 s      25032 s          0 s
       #2  2095 MHz      74055 s          0 s       3090 s      23528 s          0 s
       
  Memory: 6.764884948730469 GB (2890.20703125 MB free)
  Uptime: 1029.0 sec
  Load Avg:  1.65673828125  1.57763671875  1.1337890625
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
    CPU MHz:             2095.078
    BogoMIPS:            4190.15
    Hypervisor vendor:   Microsoft
    Virtualization type: full
    L1d cache:           32K
    L1i cache:           32K
    L2 cache:            1024K
    L3 cache:            36608K
    NUMA node0 CPU(s):   0,1
    Flags:               fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush mmx fxsr sse sse2 ss ht syscall nx pdpe1gb rdtscp lm constant_tsc rep_good nopl xtopology cpuid pni pclmulqdq ssse3 fma cx16 pcid sse4_1 sse4_2 movbe popcnt aes xsave avx f16c rdrand hypervisor lahf_lm abm 3dnowprefetch invpcid_single pti fsgsbase bmi1 hle avx2 smep bmi2 erms invpcid rtm mpx avx512f avx512dq rdseed adx smap clflushopt avx512cd avx512bw avx512vl xsaveopt xsavec xsaves
    

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

