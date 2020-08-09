# Multi-thread benchmark result

* Pull request commit: [`efcc6ba48d51b8f527480e8fab1d0dadc7bd7b1e`](https://github.com/JuliaFolds/Transducers.jl/commit/efcc6ba48d51b8f527480e8fab1d0dadc7bd7b1e)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/408> (Define is_prelude on Tuple and NamedTuple)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 9 Aug 2020 - 09:28
    - Baseline: 9 Aug 2020 - 09:33
* Package commits:
    - Target: e0cc36
    - Baseline: b8efee
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
| `["collect", "assoc", "basesize=1"]`                | 1.09 (5%) :x: |    1.00 (1%)  |
| `["collect", "assoc", "basesize=1024"]`             | 1.11 (5%) :x: |    1.00 (1%)  |
| `["collect", "assoc", "basesize=32"]`               | 1.18 (5%) :x: |    1.00 (1%)  |
| `["collect", "seq"]`                                | 1.09 (5%) :x: |    1.00 (1%)  |
| `["collect", "unordered", "basesize=1"]`            | 1.20 (5%) :x: |    1.00 (1%)  |
| `["collect", "unordered", "basesize=1024"]`         | 1.41 (5%) :x: | 1.17 (1%) :x: |
| `["collect", "unordered", "basesize=32"]`           | 1.06 (5%) :x: |    1.00 (1%)  |
| `["findfirst", "n=1000", "foldl"]`                  | 1.05 (5%) :x: |    1.00 (1%)  |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 1.08 (5%) :x: |    1.00 (1%)  |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 1.09 (5%) :x: |    1.00 (1%)  |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 1.09 (5%) :x: |    1.00 (1%)  |
| `["findfirst", "n=400", "foldl"]`                   | 1.10 (5%) :x: |    1.00 (1%)  |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 1.13 (5%) :x: |    1.00 (1%)  |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 1.17 (5%) :x: |    1.00 (1%)  |
| `["findfirst", "n=500", "foldl"]`                   | 1.08 (5%) :x: |    1.00 (1%)  |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 1.06 (5%) :x: |    1.00 (1%)  |
| `["overhead", "default"]`                           | 1.09 (5%) :x: |    1.00 (1%)  |
| `["parallel_histogram", "assoc", "basesize=16384"]` | 1.13 (5%) :x: |    1.00 (1%)  |
| `["parallel_histogram", "comm", "basesize=4096"]`   | 1.10 (5%) :x: |    1.01 (1%)  |
| `["parallel_histogram", "comm", "basesize=8192"]`   | 1.05 (5%) :x: |    1.00 (1%)  |
| `["sum", "random", "reduce", "basesize=128"]`       | 1.07 (5%) :x: |    1.00 (1%)  |
| `["sum", "uniform", "reduce", "basesize=128"]`      | 1.09 (5%) :x: |    1.00 (1%)  |
| `["sum", "uniform", "reduce", "basesize=256"]`      | 1.10 (5%) :x: |    1.00 (1%)  |
| `["sum", "valley", "foldl"]`                        | 1.13 (5%) :x: |    1.00 (1%)  |
| `["words", "nthreads=2"]`                           | 1.08 (5%) :x: |    1.00 (1%)  |
| `["words", "nthreads=4"]`                           | 1.07 (5%) :x: |    1.01 (1%)  |

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
  uname: Linux 5.3.0-1034-azure #35~18.04.1-Ubuntu SMP Mon Jul 13 12:54:45 UTC 2020 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz: 
              speed         user         nice          sys         idle          irq
       #1  2294 MHz      49114 s          0 s       2612 s      22465 s          0 s
       #2  2294 MHz      52435 s          0 s       2610 s      18988 s          0 s
       
  Memory: 6.764881134033203 GB (2933.296875 MB free)
  Uptime: 760.0 sec
  Load Avg:  1.560546875  1.47900390625  0.93115234375
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, broadwell)
```

### Baseline
```
Julia Version 1.4.2
Commit 44fa15b150* (2020-05-23 18:35 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 18.04.4 LTS
  uname: Linux 5.3.0-1034-azure #35~18.04.1-Ubuntu SMP Mon Jul 13 12:54:45 UTC 2020 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz: 
              speed         user         nice          sys         idle          irq
       #1  2294 MHz      74252 s          0 s       3350 s      26007 s          0 s
       #2  2294 MHz      72592 s          0 s       3089 s      27901 s          0 s
       
  Memory: 6.764881134033203 GB (2952.05859375 MB free)
  Uptime: 1057.0 sec
  Load Avg:  1.64111328125  1.56005859375  1.11572265625
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, broadwell)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 9 Aug 2020 - 9:28
* Package commit: e0cc36
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
| `["collect", "assoc", "basesize=1"]`                | 314.592 ms (5%) | 11.773 ms |  87.55 MiB (1%) |     1590702 |
| `["collect", "assoc", "basesize=1024"]`             | 167.019 ms (5%) |           |   1.84 MiB (1%) |        1807 |
| `["collect", "assoc", "basesize=32"]`               | 190.459 ms (5%) |           |   5.64 MiB (1%) |       54017 |
| `["collect", "seq"]`                                | 320.743 ms (5%) |           |   1.50 MiB (1%) |       32784 |
| `["collect", "unordered", "basesize=1"]`            | 455.267 ms (5%) |           |  29.20 MiB (1%) |      405584 |
| `["collect", "unordered", "basesize=1024"]`         | 264.537 ms (5%) |           | 913.06 KiB (1%) |       11528 |
| `["collect", "unordered", "basesize=32"]`           | 191.760 ms (5%) |           |   1.50 MiB (1%) |       18468 |
| `["findfirst", "n=1000", "foldl"]`                  | 517.023 ms (5%) |           |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 270.998 ms (5%) |           | 564.13 KiB (1%) |       10231 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 266.281 ms (5%) |           | 287.25 KiB (1%) |        5222 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 277.632 ms (5%) |           | 149.34 KiB (1%) |        2723 |
| `["findfirst", "n=400", "foldl"]`                   | 407.838 ms (5%) |           |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 196.419 ms (5%) |           |   1.02 MiB (1%) |       18966 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 206.892 ms (5%) |           | 526.19 KiB (1%) |        9572 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 216.565 ms (5%) |           | 267.30 KiB (1%) |        4880 |
| `["findfirst", "n=500", "foldl"]`                   |  65.308 ms (5%) |           |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |  34.047 ms (5%) |           | 157.47 KiB (1%) |        2855 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |  34.308 ms (5%) |           |  84.59 KiB (1%) |        1536 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  35.779 ms (5%) |           |  48.30 KiB (1%) |         878 |
| `["overhead", "default"]`                           | 176.600 μs (5%) |           | 146.25 KiB (1%) |        2632 |
| `["overhead", "stoppable=false"]`                   | 174.800 μs (5%) |           | 146.27 KiB (1%) |        2632 |
| `["overhead", "stoppable=true"]`                    | 311.500 μs (5%) |           | 146.55 KiB (1%) |        2650 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   3.826 ms (5%) |           | 732.06 KiB (1%) |         103 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   4.240 ms (5%) |           |   1.80 MiB (1%) |         497 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   3.846 ms (5%) |           |   1.43 MiB (1%) |         242 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  12.071 ms (5%) |           |   1.22 MiB (1%) |         159 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  20.127 ms (5%) |           |   1.05 MiB (1%) |        4951 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  16.718 ms (5%) |           |   1.23 MiB (1%) |         874 |
| `["parallel_histogram", "seq"]`                     |   6.360 ms (5%) |           | 364.61 KiB (1%) |          24 |
| `["sum", "random", "foldl"]`                        |  11.645 ms (5%) |           |   64 bytes (1%) |           3 |
| `["sum", "random", "reduce", "basesize=128"]`       |   6.535 ms (5%) |           | 313.42 KiB (1%) |        6071 |
| `["sum", "random", "reduce", "basesize=256"]`       |   6.001 ms (5%) |           | 155.13 KiB (1%) |        3011 |
| `["sum", "random", "reduce", "basesize=512"]`       |   5.850 ms (5%) |           |  76.33 KiB (1%) |        1487 |
| `["sum", "uniform", "foldl"]`                       |  11.777 ms (5%) |           |   64 bytes (1%) |           3 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   6.599 ms (5%) |           | 313.39 KiB (1%) |        6069 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   6.467 ms (5%) |           | 155.16 KiB (1%) |        3013 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   5.938 ms (5%) |           |  76.30 KiB (1%) |        1485 |
| `["sum", "valley", "foldl"]`                        |  13.264 ms (5%) |           |   64 bytes (1%) |           3 |
| `["sum", "valley", "reduce", "basesize=128"]`       |   6.137 ms (5%) |           | 313.30 KiB (1%) |        6063 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   6.046 ms (5%) |           | 155.14 KiB (1%) |        3012 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   5.988 ms (5%) |           |  76.31 KiB (1%) |        1486 |
| `["words", "nthreads=1"]`                           |  39.421 ms (5%) |  9.075 ms |  63.25 MiB (1%) |     2066808 |
| `["words", "nthreads=2"]`                           |  18.023 ms (5%) |           |  63.85 MiB (1%) |     2074924 |
| `["words", "nthreads=4"]`                           |  17.827 ms (5%) |           |  65.12 MiB (1%) |     2087319 |

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
  uname: Linux 5.3.0-1034-azure #35~18.04.1-Ubuntu SMP Mon Jul 13 12:54:45 UTC 2020 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz: 
              speed         user         nice          sys         idle          irq
       #1  2294 MHz      49114 s          0 s       2612 s      22465 s          0 s
       #2  2294 MHz      52435 s          0 s       2610 s      18988 s          0 s
       
  Memory: 6.764881134033203 GB (2933.296875 MB free)
  Uptime: 760.0 sec
  Load Avg:  1.560546875  1.47900390625  0.93115234375
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, broadwell)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 9 Aug 2020 - 9:33
* Package commit: b8efee
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
| `["collect", "assoc", "basesize=1"]`                | 288.315 ms (5%) | 12.876 ms |  87.55 MiB (1%) |     1590712 |
| `["collect", "assoc", "basesize=1024"]`             | 150.875 ms (5%) |           |   1.84 MiB (1%) |        1813 |
| `["collect", "assoc", "basesize=32"]`               | 161.003 ms (5%) |           |   5.64 MiB (1%) |       54012 |
| `["collect", "seq"]`                                | 293.900 ms (5%) |           |   1.50 MiB (1%) |       32784 |
| `["collect", "unordered", "basesize=1"]`            | 380.095 ms (5%) |           |  29.20 MiB (1%) |      405798 |
| `["collect", "unordered", "basesize=1024"]`         | 186.980 ms (5%) |           | 783.08 KiB (1%) |        3209 |
| `["collect", "unordered", "basesize=32"]`           | 180.824 ms (5%) |           |   1.50 MiB (1%) |       18752 |
| `["findfirst", "n=1000", "foldl"]`                  | 490.719 ms (5%) |           |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 251.397 ms (5%) |           | 564.20 KiB (1%) |       10236 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 243.196 ms (5%) |           | 287.28 KiB (1%) |        5224 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 253.684 ms (5%) |           | 149.38 KiB (1%) |        2725 |
| `["findfirst", "n=400", "foldl"]`                   | 369.657 ms (5%) |           |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 200.109 ms (5%) |           |   1.02 MiB (1%) |       18979 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 183.529 ms (5%) |           | 526.25 KiB (1%) |        9576 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 184.860 ms (5%) |           | 267.27 KiB (1%) |        4878 |
| `["findfirst", "n=500", "foldl"]`                   |  60.622 ms (5%) |           |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |  32.462 ms (5%) |           | 157.47 KiB (1%) |        2855 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |  32.492 ms (5%) |           |  84.59 KiB (1%) |        1536 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  35.167 ms (5%) |           |  48.31 KiB (1%) |         879 |
| `["overhead", "default"]`                           | 162.500 μs (5%) |           | 146.27 KiB (1%) |        2633 |
| `["overhead", "stoppable=false"]`                   | 173.300 μs (5%) |           | 146.28 KiB (1%) |        2633 |
| `["overhead", "stoppable=true"]`                    | 309.500 μs (5%) |           | 146.55 KiB (1%) |        2650 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   3.384 ms (5%) |           | 732.06 KiB (1%) |         103 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   4.279 ms (5%) |           |   1.80 MiB (1%) |         497 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   3.699 ms (5%) |           |   1.43 MiB (1%) |         242 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  12.008 ms (5%) |           |   1.22 MiB (1%) |         157 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  18.304 ms (5%) |           |   1.04 MiB (1%) |        2806 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  15.868 ms (5%) |           |   1.23 MiB (1%) |         556 |
| `["parallel_histogram", "seq"]`                     |   6.061 ms (5%) |           | 364.61 KiB (1%) |          24 |
| `["sum", "random", "foldl"]`                        |  11.615 ms (5%) |           |   64 bytes (1%) |           3 |
| `["sum", "random", "reduce", "basesize=128"]`       |   6.083 ms (5%) |           | 313.41 KiB (1%) |        6070 |
| `["sum", "random", "reduce", "basesize=256"]`       |   5.939 ms (5%) |           | 155.16 KiB (1%) |        3013 |
| `["sum", "random", "reduce", "basesize=512"]`       |   5.801 ms (5%) |           |  76.31 KiB (1%) |        1486 |
| `["sum", "uniform", "foldl"]`                       |  11.268 ms (5%) |           |   64 bytes (1%) |           3 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   6.080 ms (5%) |           | 313.44 KiB (1%) |        6072 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   5.861 ms (5%) |           | 155.14 KiB (1%) |        3012 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   5.676 ms (5%) |           |  76.31 KiB (1%) |        1486 |
| `["sum", "valley", "foldl"]`                        |  11.769 ms (5%) |           |   64 bytes (1%) |           3 |
| `["sum", "valley", "reduce", "basesize=128"]`       |   6.121 ms (5%) |           | 313.31 KiB (1%) |        6064 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   5.949 ms (5%) |           | 155.16 KiB (1%) |        3013 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   5.923 ms (5%) |           |  76.33 KiB (1%) |        1487 |
| `["words", "nthreads=1"]`                           |  39.208 ms (5%) |  7.939 ms |  63.05 MiB (1%) |     2059821 |
| `["words", "nthreads=2"]`                           |  16.740 ms (5%) |           |  64.14 MiB (1%) |     2072078 |
| `["words", "nthreads=4"]`                           |  16.631 ms (5%) |           |  64.77 MiB (1%) |     2078279 |

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
  uname: Linux 5.3.0-1034-azure #35~18.04.1-Ubuntu SMP Mon Jul 13 12:54:45 UTC 2020 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz: 
              speed         user         nice          sys         idle          irq
       #1  2294 MHz      74252 s          0 s       3350 s      26007 s          0 s
       #2  2294 MHz      72592 s          0 s       3089 s      27901 s          0 s
       
  Memory: 6.764881134033203 GB (2952.05859375 MB free)
  Uptime: 1057.0 sec
  Load Avg:  1.64111328125  1.56005859375  1.11572265625
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, broadwell)
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
    Model:               79
    Model name:          Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz
    Stepping:            1
    CPU MHz:             2294.690
    BogoMIPS:            4589.38
    Hypervisor vendor:   Microsoft
    Virtualization type: full
    L1d cache:           32K
    L1i cache:           32K
    L2 cache:            256K
    L3 cache:            51200K
    NUMA node0 CPU(s):   0,1
    Flags:               fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush mmx fxsr sse sse2 ss ht syscall nx pdpe1gb rdtscp lm constant_tsc rep_good nopl xtopology cpuid pni pclmulqdq ssse3 fma cx16 pcid sse4_1 sse4_2 movbe popcnt aes xsave avx f16c rdrand hypervisor lahf_lm abm 3dnowprefetch invpcid_single pti fsgsbase bmi1 hle avx2 smep bmi2 erms invpcid rtm rdseed adx smap xsaveopt md_clear
    

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
| Address Size       | 48 bits virtual, 44 bits physical                       |
| SIMD               | 256 bit = 32 byte max. SIMD vector size                 |
| Time Stamp Counter | TSC is accessible via `rdtsc`                           |
|                    | TSC increased at every clock cycle (non-invariant TSC)  |
| Perf. Monitoring   | Performance Monitoring Counters (PMC) are not supported |
| Hypervisor         | Yes, Microsoft                                          |

