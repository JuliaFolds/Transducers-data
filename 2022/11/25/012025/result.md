# Multi-thread benchmark result

* Pull request commit: [`f1e24fe99551812139ebc4c080c64b35286e1b02`](https://github.com/JuliaFolds/Transducers.jl/commit/f1e24fe99551812139ebc4c080c64b35286e1b02)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/536> (Update for v1.9 compatability)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 25 Nov 2022 - 01:14
    - Baseline: 25 Nov 2022 - 01:19
* Package commits:
    - Target: 6e4c91
    - Baseline: 958213
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
| `["collect", "assoc", "basesize=1"]`                | 0.90 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["collect", "unordered", "basesize=1"]`            | 0.92 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["collect", "unordered", "basesize=32"]`           |                1.05 (5%) :x: |                   1.00 (1%)  |
| `["findfirst", "n=1000", "foldl"]`                  |                1.12 (5%) :x: |                   1.00 (1%)  |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 0.64 (5%) :white_check_mark: | 0.64 (1%) :white_check_mark: |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` |                1.12 (5%) :x: |                1.04 (1%) :x: |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` |                   1.05 (5%)  |                1.08 (1%) :x: |
| `["findfirst", "n=400", "foldl"]`                   |                1.05 (5%) :x: |                   1.00 (1%)  |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  |                   0.98 (5%)  |                1.03 (1%) :x: |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 0.79 (5%) :white_check_mark: | 0.95 (1%) :white_check_mark: |
| `["findfirst", "n=500", "foldl"]`                   |                1.06 (5%) :x: |                   1.00 (1%)  |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |                1.10 (5%) :x: |                1.16 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |                1.08 (5%) :x: |                1.23 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 0.81 (5%) :white_check_mark: | 0.81 (1%) :white_check_mark: |
| `["overhead", "stoppable=false"]`                   | 0.93 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["overhead", "stoppable=true"]`                    | 0.95 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["parallel_histogram", "comm", "basesize=16384"]`  |                   1.04 (5%)  |                1.02 (1%) :x: |
| `["splitby", "count", "reduce"]`                    |                   1.05 (5%)  |                1.03 (1%) :x: |
| `["sum", "random", "foldl"]`                        | 0.87 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["sum", "random", "reduce", "basesize=128"]`       | 0.88 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["sum", "random", "reduce", "basesize=256"]`       | 0.85 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["sum", "random", "reduce", "basesize=512"]`       | 0.85 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["sum", "uniform", "foldl"]`                       | 0.87 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["sum", "uniform", "reduce", "basesize=128"]`      |                1.08 (5%) :x: |                   1.00 (1%)  |
| `["sum", "uniform", "reduce", "basesize=512"]`      | 0.94 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["words", "nthreads=1"]`                           |                1.06 (5%) :x: |                   1.00 (1%)  |

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
      Ubuntu 22.04.1 LTS
  uname: Linux 5.15.0-1023-azure #29-Ubuntu SMP Wed Oct 19 22:37:08 UTC 2022 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz: 
              speed         user         nice          sys         idle          irq
       #1  2294 MHz       5626 s          0 s        270 s       1499 s          0 s
       #2  2294 MHz       5070 s          0 s        280 s       2027 s          0 s
       
  Memory: 6.781219482421875 GB (3758.63671875 MB free)
  Uptime: 746.69 sec
  Load Avg:  1.63  1.52  0.94
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, broadwell)
```

### Baseline
```
Julia Version 1.7.3
Commit 742b9abb4d (2022-05-06 12:58 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 22.04.1 LTS
  uname: Linux 5.15.0-1023-azure #29-Ubuntu SMP Wed Oct 19 22:37:08 UTC 2022 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz: 
              speed         user         nice          sys         idle          irq
       #1  2294 MHz       8485 s          0 s        326 s       1656 s          0 s
       #2  2294 MHz       6878 s          0 s        322 s       3244 s          0 s
       
  Memory: 6.781219482421875 GB (3854.796875 MB free)
  Uptime: 1054.49 sec
  Load Avg:  1.54  1.55  1.12
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, broadwell)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 25 Nov 2022 - 1:14
* Package commit: 6e4c91
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
| `["collect", "assoc", "basesize=1"]`                | 212.930 ms (5%) |         |  25.97 MiB (1%) |      306830 |
| `["collect", "assoc", "basesize=1024"]`             | 156.203 ms (5%) |         |   2.61 MiB (1%) |         455 |
| `["collect", "assoc", "basesize=32"]`               | 159.474 ms (5%) |         |   4.82 MiB (1%) |       11702 |
| `["collect", "seq"]`                                | 308.137 ms (5%) |         | 812.73 KiB (1%) |          11 |
| `["collect", "unordered", "basesize=1"]`            | 333.548 ms (5%) |         |  23.89 MiB (1%) |      412799 |
| `["collect", "unordered", "basesize=1024"]`         | 178.594 ms (5%) |         |   1.02 MiB (1%) |        1325 |
| `["collect", "unordered", "basesize=32"]`           | 186.618 ms (5%) |         |   1.60 MiB (1%) |       15421 |
| `["findfirst", "n=1000", "foldl"]`                  | 568.785 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 321.913 ms (5%) |         | 232.95 KiB (1%) |        3279 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 413.030 ms (5%) |         | 162.80 KiB (1%) |        2293 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 463.371 ms (5%) |         | 108.58 KiB (1%) |        1510 |
| `["findfirst", "n=400", "foldl"]`                   | 384.455 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 223.649 ms (5%) |         | 399.75 KiB (1%) |        5675 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 200.153 ms (5%) |         | 200.86 KiB (1%) |        2873 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 286.268 ms (5%) |         | 127.30 KiB (1%) |        1819 |
| `["findfirst", "n=500", "foldl"]`                   |  69.700 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 178.579 ms (5%) |         | 279.12 KiB (1%) |        3879 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |  75.905 ms (5%) |         |  91.53 KiB (1%) |        1233 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  60.243 ms (5%) |         |  43.11 KiB (1%) |         581 |
| `["overhead", "default"]`                           |  70.800 μs (5%) |         |  32.73 KiB (1%) |         418 |
| `["overhead", "stoppable=false"]`                   |  67.500 μs (5%) |         |  32.75 KiB (1%) |         418 |
| `["overhead", "stoppable=true"]`                    |  81.901 μs (5%) |         |  44.25 KiB (1%) |         610 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   2.398 ms (5%) |         | 728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   2.941 ms (5%) |         |   1.79 MiB (1%) |         215 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   2.724 ms (5%) |         |   1.42 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  17.365 ms (5%) |         |   1.67 MiB (1%) |        5391 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  21.695 ms (5%) |         |   1.25 MiB (1%) |        7014 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  19.737 ms (5%) |         |   1.23 MiB (1%) |         170 |
| `["parallel_histogram", "seq"]`                     |   4.181 ms (5%) |         | 364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  32.343 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  15.949 ms (5%) |         |  736 bytes (1%) |          11 |
| `["splitby", "count", "foldl"]`                     |   1.611 ms (5%) |         |                 |             |
| `["splitby", "count", "man"]`                       |   1.223 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    | 787.602 μs (5%) |         |   1.09 KiB (1%) |          19 |
| `["sum", "random", "foldl"]`                        |  11.961 ms (5%) |         |                 |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   6.108 ms (5%) |         |  74.17 KiB (1%) |        1104 |
| `["sum", "random", "reduce", "basesize=256"]`       |   5.894 ms (5%) |         |  36.70 KiB (1%) |         545 |
| `["sum", "random", "reduce", "basesize=512"]`       |   5.875 ms (5%) |         |  18.08 KiB (1%) |         269 |
| `["sum", "uniform", "foldl"]`                       |  11.421 ms (5%) |         |                 |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   6.263 ms (5%) |         |  74.17 KiB (1%) |        1104 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   5.823 ms (5%) |         |  36.73 KiB (1%) |         546 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   5.641 ms (5%) |         |  18.03 KiB (1%) |         268 |
| `["sum", "valley", "foldl"]`                        |  11.948 ms (5%) |         |                 |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   6.019 ms (5%) |         |  74.14 KiB (1%) |        1103 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   5.949 ms (5%) |         |  36.73 KiB (1%) |         546 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   5.941 ms (5%) |         |  18.00 KiB (1%) |         267 |
| `["words", "nthreads=1"]`                           |  25.203 ms (5%) |         |  31.66 MiB (1%) |     1031308 |
| `["words", "nthreads=2"]`                           |  15.268 ms (5%) |         |  32.02 MiB (1%) |     1031344 |
| `["words", "nthreads=4"]`                           |  15.685 ms (5%) |         |  32.92 MiB (1%) |     1031542 |

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
      Ubuntu 22.04.1 LTS
  uname: Linux 5.15.0-1023-azure #29-Ubuntu SMP Wed Oct 19 22:37:08 UTC 2022 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz: 
              speed         user         nice          sys         idle          irq
       #1  2294 MHz       5626 s          0 s        270 s       1499 s          0 s
       #2  2294 MHz       5070 s          0 s        280 s       2027 s          0 s
       
  Memory: 6.781219482421875 GB (3758.63671875 MB free)
  Uptime: 746.69 sec
  Load Avg:  1.63  1.52  0.94
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, broadwell)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 25 Nov 2022 - 1:19
* Package commit: 958213
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
| `["collect", "assoc", "basesize=1"]`                | 236.325 ms (5%) |         |  25.97 MiB (1%) |      306825 |
| `["collect", "assoc", "basesize=1024"]`             | 162.628 ms (5%) |         |   2.61 MiB (1%) |         456 |
| `["collect", "assoc", "basesize=32"]`               | 165.628 ms (5%) |         |   4.82 MiB (1%) |       11710 |
| `["collect", "seq"]`                                | 320.194 ms (5%) |         | 812.73 KiB (1%) |          11 |
| `["collect", "unordered", "basesize=1"]`            | 363.773 ms (5%) |         |  23.95 MiB (1%) |      414518 |
| `["collect", "unordered", "basesize=1024"]`         | 170.239 ms (5%) |         |   1.02 MiB (1%) |        1432 |
| `["collect", "unordered", "basesize=32"]`           | 176.959 ms (5%) |         |   1.61 MiB (1%) |       15482 |
| `["findfirst", "n=1000", "foldl"]`                  | 508.942 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 500.207 ms (5%) |         | 362.44 KiB (1%) |        5087 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 368.580 ms (5%) |         | 157.20 KiB (1%) |        2193 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 442.782 ms (5%) |         | 100.12 KiB (1%) |        1399 |
| `["findfirst", "n=400", "foldl"]`                   | 365.334 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 227.692 ms (5%) |         | 388.58 KiB (1%) |        5522 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 252.588 ms (5%) |         | 212.41 KiB (1%) |        3040 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 281.407 ms (5%) |         | 127.28 KiB (1%) |        1816 |
| `["findfirst", "n=500", "foldl"]`                   |  65.934 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 161.816 ms (5%) |         | 239.91 KiB (1%) |        3318 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |  70.605 ms (5%) |         |  74.34 KiB (1%) |        1012 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  74.648 ms (5%) |         |  53.09 KiB (1%) |         709 |
| `["overhead", "default"]`                           |  71.300 μs (5%) |         |  32.73 KiB (1%) |         418 |
| `["overhead", "stoppable=false"]`                   |  72.200 μs (5%) |         |  32.75 KiB (1%) |         418 |
| `["overhead", "stoppable=true"]`                    |  86.300 μs (5%) |         |  44.25 KiB (1%) |         610 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   2.524 ms (5%) |         | 728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   2.948 ms (5%) |         |   1.79 MiB (1%) |         216 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   2.669 ms (5%) |         |   1.42 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  16.762 ms (5%) |         |   1.64 MiB (1%) |        4447 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  22.388 ms (5%) |         |   1.24 MiB (1%) |        6936 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  20.653 ms (5%) |         |   1.23 MiB (1%) |        3288 |
| `["parallel_histogram", "seq"]`                     |   4.218 ms (5%) |         | 364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  31.712 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  15.976 ms (5%) |         |  736 bytes (1%) |          11 |
| `["splitby", "count", "foldl"]`                     |   1.596 ms (5%) |         |                 |             |
| `["splitby", "count", "man"]`                       |   1.223 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    | 750.304 μs (5%) |         |   1.06 KiB (1%) |          18 |
| `["sum", "random", "foldl"]`                        |  13.694 ms (5%) |         |                 |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   6.967 ms (5%) |         |  74.17 KiB (1%) |        1104 |
| `["sum", "random", "reduce", "basesize=256"]`       |   6.972 ms (5%) |         |  36.77 KiB (1%) |         547 |
| `["sum", "random", "reduce", "basesize=512"]`       |   6.907 ms (5%) |         |  18.08 KiB (1%) |         269 |
| `["sum", "uniform", "foldl"]`                       |  13.139 ms (5%) |         |                 |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   5.815 ms (5%) |         |  74.17 KiB (1%) |        1104 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   6.013 ms (5%) |         |  36.77 KiB (1%) |         547 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   5.985 ms (5%) |         |  18.03 KiB (1%) |         268 |
| `["sum", "valley", "foldl"]`                        |  11.738 ms (5%) |         |                 |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   5.992 ms (5%) |         |  74.02 KiB (1%) |        1099 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   5.972 ms (5%) |         |  36.73 KiB (1%) |         546 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   5.960 ms (5%) |         |  18.00 KiB (1%) |         267 |
| `["words", "nthreads=1"]`                           |  23.849 ms (5%) |         |  31.54 MiB (1%) |     1027585 |
| `["words", "nthreads=2"]`                           |  15.844 ms (5%) |         |  32.25 MiB (1%) |     1027658 |
| `["words", "nthreads=4"]`                           |  15.768 ms (5%) |         |  32.70 MiB (1%) |     1027753 |

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
      Ubuntu 22.04.1 LTS
  uname: Linux 5.15.0-1023-azure #29-Ubuntu SMP Wed Oct 19 22:37:08 UTC 2022 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz: 
              speed         user         nice          sys         idle          irq
       #1  2294 MHz       8485 s          0 s        326 s       1656 s          0 s
       #2  2294 MHz       6878 s          0 s        322 s       3244 s          0 s
       
  Memory: 6.781219482421875 GB (3854.796875 MB free)
  Uptime: 1054.49 sec
  Load Avg:  1.54  1.55  1.12
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, broadwell)
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
    Address sizes:                   46 bits physical, 48 bits virtual
    Byte Order:                      Little Endian
    CPU(s):                          2
    On-line CPU(s) list:             0,1
    Vendor ID:                       GenuineIntel
    Model name:                      Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz
    CPU family:                      6
    Model:                           79
    Thread(s) per core:              1
    Core(s) per socket:              2
    Socket(s):                       1
    Stepping:                        1
    BogoMIPS:                        4589.37
    Flags:                           fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush mmx fxsr sse sse2 ss ht syscall nx pdpe1gb rdtscp lm constant_tsc rep_good nopl xtopology cpuid pni pclmulqdq ssse3 fma cx16 pcid sse4_1 sse4_2 movbe popcnt aes xsave avx f16c rdrand hypervisor lahf_lm abm 3dnowprefetch invpcid_single pti fsgsbase bmi1 hle avx2 smep bmi2 erms invpcid rtm rdseed adx smap xsaveopt md_clear
    Hypervisor vendor:               Microsoft
    Virtualization type:             full
    L1d cache:                       64 KiB (2 instances)
    L1i cache:                       64 KiB (2 instances)
    L2 cache:                        512 KiB (2 instances)
    L3 cache:                        50 MiB (1 instance)
    NUMA node(s):                    1
    NUMA node0 CPU(s):               0,1
    Vulnerability Itlb multihit:     KVM: Mitigation: VMX unsupported
    Vulnerability L1tf:              Mitigation; PTE Inversion
    Vulnerability Mds:               Mitigation; Clear CPU buffers; SMT Host state unknown
    Vulnerability Meltdown:          Mitigation; PTI
    Vulnerability Mmio stale data:   Vulnerable: Clear CPU buffers attempted, no microcode; SMT Host state unknown
    Vulnerability Retbleed:          Not affected
    Vulnerability Spec store bypass: Vulnerable
    Vulnerability Spectre v1:        Mitigation; usercopy/swapgs barriers and __user pointer sanitization
    Vulnerability Spectre v2:        Mitigation; Retpolines, STIBP disabled, RSB filling, PBRSB-eIBRS Not affected
    Vulnerability Srbds:             Not affected
    Vulnerability Tsx async abort:   Mitigation; Clear CPU buffers; SMT Host state unknown
    

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

