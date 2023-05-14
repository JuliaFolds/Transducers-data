# Multi-thread benchmark result

* Pull request commit: [`09ab4e69d7a18e7ac1a2c1da65f2189cac213faf`](https://github.com/JuliaFolds/Transducers.jl/commit/09ab4e69d7a18e7ac1a2c1da65f2189cac213faf)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/243> (Update */Manifest.toml)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 14 May 2023 - 01:40
    - Baseline: 14 May 2023 - 01:45
* Package commits:
    - Target: 287422
    - Baseline: 2a51f8
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
| `["findfirst", "n=1000", "reduce", "basesize=512"]` |                   1.01 (5%)  |                1.05 (1%) :x: |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 0.94 (5%) :white_check_mark: | 0.96 (1%) :white_check_mark: |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 0.72 (5%) :white_check_mark: | 0.78 (1%) :white_check_mark: |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |                1.57 (5%) :x: |                1.28 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |                1.06 (5%) :x: |                1.03 (1%) :x: |
| `["overhead", "stoppable=true"]`                    | 0.95 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["parallel_histogram", "comm", "basesize=16384"]`  |                1.11 (5%) :x: |                   1.01 (1%)  |
| `["parallel_histogram", "comm", "basesize=4096"]`   |                   1.02 (5%)  |                1.01 (1%) :x: |
| `["parallel_histogram", "comm", "basesize=8192"]`   | 0.84 (5%) :white_check_mark: | 0.97 (1%) :white_check_mark: |
| `["splitby", "count", "man"]`                       | 0.81 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["splitby", "count", "reduce"]`                    | 0.95 (5%) :white_check_mark: |                1.04 (1%) :x: |

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
      Ubuntu 22.04.2 LTS
  uname: Linux 5.15.0-1037-azure #44-Ubuntu SMP Thu Apr 20 13:19:31 UTC 2023 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2593 MHz       6024 s          0 s        232 s       1984 s          0 s
       #2  2593 MHz       4434 s          0 s        235 s       3544 s          0 s
       
  Memory: 6.7812042236328125 GB (3682.01953125 MB free)
  Uptime: 828.46 sec
  Load Avg:  1.73  1.51  0.91
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, skylake-avx512)
```

### Baseline
```
Julia Version 1.7.3
Commit 742b9abb4d (2022-05-06 12:58 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 22.04.2 LTS
  uname: Linux 5.15.0-1037-azure #44-Ubuntu SMP Thu Apr 20 13:19:31 UTC 2023 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2593 MHz       8623 s          0 s        302 s       2413 s          0 s
       #2  2593 MHz       6592 s          0 s        297 s       4419 s          0 s
       
  Memory: 6.7812042236328125 GB (3630.25 MB free)
  Uptime: 1138.54 sec
  Load Avg:  1.76  1.66  1.16
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, skylake-avx512)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 14 May 2023 - 1:40
* Package commit: 287422
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
| `["collect", "assoc", "basesize=1"]`                | 199.919 ms (5%) |         |   4.36 MiB (1%) |       32800 |
| `["collect", "assoc", "basesize=1024"]`             | 197.928 ms (5%) |         |   1.09 MiB (1%) |          53 |
| `["collect", "assoc", "basesize=32"]`               | 198.312 ms (5%) |         |   1.48 MiB (1%) |        1052 |
| `["collect", "seq"]`                                | 394.660 ms (5%) |         | 256.05 KiB (1%) |           2 |
| `["collect", "unordered", "basesize=1"]`            | 349.452 ms (5%) |         |  23.90 MiB (1%) |      413010 |
| `["collect", "unordered", "basesize=1024"]`         | 211.954 ms (5%) |         |   1.01 MiB (1%) |         994 |
| `["collect", "unordered", "basesize=32"]`           | 224.123 ms (5%) |         |   1.58 MiB (1%) |       14600 |
| `["findfirst", "n=1000", "foldl"]`                  | 630.003 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 345.710 ms (5%) |         | 232.77 KiB (1%) |        3273 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 424.584 ms (5%) |         | 157.20 KiB (1%) |        2193 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 565.178 ms (5%) |         | 108.55 KiB (1%) |        1509 |
| `["findfirst", "n=400", "foldl"]`                   | 472.722 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 250.182 ms (5%) |         | 386.50 KiB (1%) |        5505 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 248.376 ms (5%) |         | 200.86 KiB (1%) |        2873 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 258.690 ms (5%) |         | 107.81 KiB (1%) |        1554 |
| `["findfirst", "n=500", "foldl"]`                   |  81.963 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 123.414 ms (5%) |         | 177.81 KiB (1%) |        2453 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 243.974 ms (5%) |         | 167.81 KiB (1%) |        2369 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 106.640 ms (5%) |         |  56.86 KiB (1%) |         779 |
| `["overhead", "default"]`                           |  73.601 μs (5%) |         |  32.73 KiB (1%) |         418 |
| `["overhead", "stoppable=false"]`                   |  75.701 μs (5%) |         |  32.75 KiB (1%) |         418 |
| `["overhead", "stoppable=true"]`                    |  83.601 μs (5%) |         |  44.25 KiB (1%) |         610 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   3.258 ms (5%) |         | 728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   3.907 ms (5%) |         |   1.79 MiB (1%) |         216 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   3.612 ms (5%) |         |   1.42 MiB (1%) |         118 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  18.480 ms (5%) |         |   1.60 MiB (1%) |        3223 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  24.851 ms (5%) |         |   1.25 MiB (1%) |        7065 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  18.766 ms (5%) |         |   1.26 MiB (1%) |        4127 |
| `["parallel_histogram", "seq"]`                     |   5.780 ms (5%) |         | 364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  35.205 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  17.589 ms (5%) |         |  736 bytes (1%) |          11 |
| `["splitby", "count", "foldl"]`                     |   2.243 ms (5%) |         |                 |             |
| `["splitby", "count", "man"]`                       |   1.417 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    |   1.090 ms (5%) |         |   1.09 KiB (1%) |          19 |
| `["sum", "random", "foldl"]`                        |  16.277 ms (5%) |         |                 |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   8.225 ms (5%) |         |  74.14 KiB (1%) |        1103 |
| `["sum", "random", "reduce", "basesize=256"]`       |   8.124 ms (5%) |         |  36.70 KiB (1%) |         545 |
| `["sum", "random", "reduce", "basesize=512"]`       |   8.068 ms (5%) |         |  18.11 KiB (1%) |         270 |
| `["sum", "uniform", "foldl"]`                       |  15.709 ms (5%) |         |                 |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   8.005 ms (5%) |         |  74.14 KiB (1%) |        1103 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   7.905 ms (5%) |         |  36.73 KiB (1%) |         546 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   7.845 ms (5%) |         |  18.03 KiB (1%) |         268 |
| `["sum", "valley", "foldl"]`                        |  16.136 ms (5%) |         |                 |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   8.236 ms (5%) |         |  74.05 KiB (1%) |        1100 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   8.146 ms (5%) |         |  36.73 KiB (1%) |         546 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   8.138 ms (5%) |         |  18.03 KiB (1%) |         268 |
| `["words", "nthreads=1"]`                           |  23.186 ms (5%) |         |  31.79 MiB (1%) |     1036208 |
| `["words", "nthreads=2"]`                           |  15.053 ms (5%) |         |  32.14 MiB (1%) |     1036246 |
| `["words", "nthreads=4"]`                           |  14.845 ms (5%) |         |  33.04 MiB (1%) |     1036414 |

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
      Ubuntu 22.04.2 LTS
  uname: Linux 5.15.0-1037-azure #44-Ubuntu SMP Thu Apr 20 13:19:31 UTC 2023 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2593 MHz       6024 s          0 s        232 s       1984 s          0 s
       #2  2593 MHz       4434 s          0 s        235 s       3544 s          0 s
       
  Memory: 6.7812042236328125 GB (3682.01953125 MB free)
  Uptime: 828.46 sec
  Load Avg:  1.73  1.51  0.91
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, skylake-avx512)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 14 May 2023 - 1:45
* Package commit: 2a51f8
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
| `["collect", "assoc", "basesize=1"]`                | 199.550 ms (5%) |         |   4.36 MiB (1%) |       32800 |
| `["collect", "assoc", "basesize=1024"]`             | 198.096 ms (5%) |         |   1.09 MiB (1%) |          54 |
| `["collect", "assoc", "basesize=32"]`               | 198.202 ms (5%) |         |   1.48 MiB (1%) |        1052 |
| `["collect", "seq"]`                                | 394.968 ms (5%) |         | 256.05 KiB (1%) |           2 |
| `["collect", "unordered", "basesize=1"]`            | 348.464 ms (5%) |         |  23.89 MiB (1%) |      412777 |
| `["collect", "unordered", "basesize=1024"]`         | 213.457 ms (5%) |         |   1.00 MiB (1%) |         877 |
| `["collect", "unordered", "basesize=32"]`           | 223.874 ms (5%) |         |   1.58 MiB (1%) |       14679 |
| `["findfirst", "n=1000", "foldl"]`                  | 626.570 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 342.633 ms (5%) |         | 230.58 KiB (1%) |        3248 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 419.823 ms (5%) |         | 157.20 KiB (1%) |        2193 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 559.674 ms (5%) |         | 103.56 KiB (1%) |        1455 |
| `["findfirst", "n=400", "foldl"]`                   | 470.318 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 248.312 ms (5%) |         | 389.67 KiB (1%) |        5543 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 246.274 ms (5%) |         | 200.67 KiB (1%) |        2867 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 274.020 ms (5%) |         | 112.59 KiB (1%) |        1622 |
| `["findfirst", "n=500", "foldl"]`                   |  81.517 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 171.134 ms (5%) |         | 229.16 KiB (1%) |        3202 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 154.921 ms (5%) |         | 130.80 KiB (1%) |        1793 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 100.609 ms (5%) |         |  55.44 KiB (1%) |         763 |
| `["overhead", "default"]`                           |  76.801 μs (5%) |         |  32.73 KiB (1%) |         418 |
| `["overhead", "stoppable=false"]`                   |  75.501 μs (5%) |         |  32.75 KiB (1%) |         418 |
| `["overhead", "stoppable=true"]`                    |  88.202 μs (5%) |         |  44.22 KiB (1%) |         609 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   3.222 ms (5%) |         | 728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   3.850 ms (5%) |         |   1.79 MiB (1%) |         216 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   3.568 ms (5%) |         |   1.42 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  16.673 ms (5%) |         |   1.59 MiB (1%) |        2840 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  24.411 ms (5%) |         |   1.23 MiB (1%) |        6482 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  22.222 ms (5%) |         |   1.30 MiB (1%) |        5748 |
| `["parallel_histogram", "seq"]`                     |   5.727 ms (5%) |         | 364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  35.191 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  17.608 ms (5%) |         |  736 bytes (1%) |          11 |
| `["splitby", "count", "foldl"]`                     |   2.257 ms (5%) |         |                 |             |
| `["splitby", "count", "man"]`                       |   1.753 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    |   1.148 ms (5%) |         |   1.05 KiB (1%) |          19 |
| `["sum", "random", "foldl"]`                        |  16.221 ms (5%) |         |                 |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   8.202 ms (5%) |         |  74.11 KiB (1%) |        1102 |
| `["sum", "random", "reduce", "basesize=256"]`       |   8.098 ms (5%) |         |  36.67 KiB (1%) |         544 |
| `["sum", "random", "reduce", "basesize=512"]`       |   8.061 ms (5%) |         |  18.08 KiB (1%) |         269 |
| `["sum", "uniform", "foldl"]`                       |  15.751 ms (5%) |         |                 |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   7.977 ms (5%) |         |  74.08 KiB (1%) |        1101 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   7.884 ms (5%) |         |  36.73 KiB (1%) |         546 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   7.809 ms (5%) |         |  18.00 KiB (1%) |         267 |
| `["sum", "valley", "foldl"]`                        |  16.066 ms (5%) |         |                 |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   8.208 ms (5%) |         |  74.11 KiB (1%) |        1102 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   8.105 ms (5%) |         |  36.73 KiB (1%) |         546 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   8.096 ms (5%) |         |  18.06 KiB (1%) |         269 |
| `["words", "nthreads=1"]`                           |  23.623 ms (5%) |         |  31.67 MiB (1%) |     1031492 |
| `["words", "nthreads=2"]`                           |  14.788 ms (5%) |         |  32.03 MiB (1%) |     1031535 |
| `["words", "nthreads=4"]`                           |  15.208 ms (5%) |         |  32.74 MiB (1%) |     1031633 |

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
      Ubuntu 22.04.2 LTS
  uname: Linux 5.15.0-1037-azure #44-Ubuntu SMP Thu Apr 20 13:19:31 UTC 2023 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2593 MHz       8623 s          0 s        302 s       2413 s          0 s
       #2  2593 MHz       6592 s          0 s        297 s       4419 s          0 s
       
  Memory: 6.7812042236328125 GB (3630.25 MB free)
  Uptime: 1138.54 sec
  Load Avg:  1.76  1.66  1.16
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, skylake-avx512)
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
    Model name:                      Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz
    CPU family:                      6
    Model:                           85
    Thread(s) per core:              1
    Core(s) per socket:              2
    Socket(s):                       1
    Stepping:                        7
    BogoMIPS:                        5187.81
    Flags:                           fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush mmx fxsr sse sse2 ss ht syscall nx pdpe1gb rdtscp lm constant_tsc rep_good nopl xtopology cpuid pni pclmulqdq ssse3 fma cx16 pcid sse4_1 sse4_2 movbe popcnt aes xsave avx f16c rdrand hypervisor lahf_lm abm 3dnowprefetch invpcid_single pti fsgsbase bmi1 hle avx2 smep bmi2 erms invpcid rtm avx512f avx512dq rdseed adx smap clflushopt avx512cd avx512bw avx512vl xsaveopt xsavec xsaves md_clear
    Hypervisor vendor:               Microsoft
    Virtualization type:             full
    L1d cache:                       64 KiB (2 instances)
    L1i cache:                       64 KiB (2 instances)
    L2 cache:                        2 MiB (2 instances)
    L3 cache:                        35.8 MiB (1 instance)
    NUMA node(s):                    1
    NUMA node0 CPU(s):               0,1
    Vulnerability Itlb multihit:     KVM: Mitigation: VMX unsupported
    Vulnerability L1tf:              Mitigation; PTE Inversion
    Vulnerability Mds:               Mitigation; Clear CPU buffers; SMT Host state unknown
    Vulnerability Meltdown:          Mitigation; PTI
    Vulnerability Mmio stale data:   Vulnerable: Clear CPU buffers attempted, no microcode; SMT Host state unknown
    Vulnerability Retbleed:          Vulnerable
    Vulnerability Spec store bypass: Vulnerable
    Vulnerability Spectre v1:        Mitigation; usercopy/swapgs barriers and __user pointer sanitization
    Vulnerability Spectre v2:        Mitigation; Retpolines, STIBP disabled, RSB filling, PBRSB-eIBRS Not affected
    Vulnerability Srbds:             Not affected
    Vulnerability Tsx async abort:   Mitigation; Clear CPU buffers; SMT Host state unknown
    

| Cpu Property       | Value                                                   |
|:------------------ |:------------------------------------------------------- |
| Brand              | Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz          |
| Vendor             | :Intel                                                  |
| Architecture       | :Skylake                                                |
| Model              | Family: 0x06, Model: 0x55, Stepping: 0x07, Type: 0x00   |
| Cores              | 2 physical cores, 2 logical cores (on executing CPU)    |
|                    | No Hyperthreading hardware capability detected          |
| Clock Frequencies  | Not supported by CPU                                    |
| Data Cache         | Level 1:3 : (32, 1024, 36608) kbytes                    |
|                    | 64 byte cache line size                                 |
| Address Size       | 48 bits virtual, 46 bits physical                       |
| SIMD               | 512 bit = 64 byte max. SIMD vector size                 |
| Time Stamp Counter | TSC is accessible via `rdtsc`                           |
|                    | TSC increased at every clock cycle (non-invariant TSC)  |
| Perf. Monitoring   | Performance Monitoring Counters (PMC) are not supported |
| Hypervisor         | Yes, Microsoft                                          |

