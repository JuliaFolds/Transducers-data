# Multi-thread benchmark result

* Pull request commit: [`2059c2e209e744c53eab10f1b178555ce630e6de`](https://github.com/JuliaFolds/Transducers.jl/commit/2059c2e209e744c53eab10f1b178555ce630e6de)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/553> (Add fast pathway for `copy`, `collect`, `tcollect`, and `tcopy` for size-stable operations)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 4 May 2023 - 06:17
    - Baseline: 4 May 2023 - 06:22
* Package commits:
    - Target: 75980b
    - Baseline: f8d0df
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
| `["collect", "assoc", "basesize=1"]`                | 0.83 (5%) :white_check_mark: | 0.17 (1%) :white_check_mark: |
| `["collect", "assoc", "basesize=1024"]`             |                   1.01 (5%)  | 0.42 (1%) :white_check_mark: |
| `["collect", "assoc", "basesize=32"]`               |                   0.99 (5%)  | 0.31 (1%) :white_check_mark: |
| `["collect", "seq"]`                                |                   0.96 (5%)  | 0.32 (1%) :white_check_mark: |
| `["collect", "unordered", "basesize=1"]`            |                   1.02 (5%)  | 0.99 (1%) :white_check_mark: |
| `["collect", "unordered", "basesize=32"]`           |                1.14 (5%) :x: |                   1.00 (1%)  |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` |                1.10 (5%) :x: |                1.01 (1%) :x: |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 0.76 (5%) :white_check_mark: | 0.75 (1%) :white_check_mark: |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 0.94 (5%) :white_check_mark: | 0.98 (1%) :white_check_mark: |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 0.68 (5%) :white_check_mark: | 0.70 (1%) :white_check_mark: |
| `["findfirst", "n=500", "foldl"]`                   |                1.07 (5%) :x: |                   1.00 (1%)  |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 0.36 (5%) :white_check_mark: | 0.44 (1%) :white_check_mark: |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 0.38 (5%) :white_check_mark: | 0.48 (1%) :white_check_mark: |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |                1.09 (5%) :x: |                1.17 (1%) :x: |
| `["overhead", "default"]`                           |                1.10 (5%) :x: |                   1.00 (1%)  |
| `["overhead", "stoppable=true"]`                    |                1.09 (5%) :x: |                   1.00 (1%)  |
| `["parallel_histogram", "assoc", "basesize=16384"]` |                1.11 (5%) :x: |                   1.00 (1%)  |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |                1.13 (5%) :x: |                   1.00 (1%)  |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |                1.06 (5%) :x: |                   1.00 (1%)  |
| `["parallel_histogram", "comm", "basesize=16384"]`  |                1.22 (5%) :x: |                1.03 (1%) :x: |
| `["parallel_histogram", "comm", "basesize=4096"]`   | 0.85 (5%) :white_check_mark: | 0.94 (1%) :white_check_mark: |
| `["parallel_histogram", "comm", "basesize=8192"]`   |                1.05 (5%) :x: | 0.98 (1%) :white_check_mark: |
| `["parallel_histogram", "seq"]`                     |                1.13 (5%) :x: |                   1.00 (1%)  |
| `["partition_length_maximum", "rand", "foldl"]`     | 0.94 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["splitby", "count", "reduce"]`                    | 0.94 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["sum", "uniform", "reduce", "basesize=128"]`      |                1.07 (5%) :x: |                   1.00 (1%)  |
| `["sum", "uniform", "reduce", "basesize=256"]`      |                1.09 (5%) :x: |                   1.00 (1%)  |
| `["words", "nthreads=2"]`                           |                1.07 (5%) :x: |                   1.01 (1%)  |
| `["words", "nthreads=4"]`                           |                1.07 (5%) :x: |                   1.01 (1%)  |

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
  uname: Linux 5.15.0-1036-azure #43-Ubuntu SMP Wed Mar 29 16:11:05 UTC 2023 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz       5715 s          0 s        320 s       1777 s          0 s
       #2  2095 MHz       5039 s          0 s        374 s       2300 s          0 s
       
  Memory: 6.7812042236328125 GB (3723.375 MB free)
  Uptime: 801.71 sec
  Load Avg:  1.72  1.56  0.97
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
  uname: Linux 5.15.0-1036-azure #43-Ubuntu SMP Wed Mar 29 16:11:05 UTC 2023 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz       7693 s          0 s        360 s       2789 s          0 s
       #2  2095 MHz       7743 s          0 s        420 s       2581 s          0 s
       
  Memory: 6.7812042236328125 GB (3874.15625 MB free)
  Uptime: 1105.33 sec
  Load Avg:  1.61  1.56  1.14
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, skylake-avx512)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 4 May 2023 - 6:17
* Package commit: 75980b
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
| `["collect", "assoc", "basesize=1"]`                | 222.577 ms (5%) |         |   4.36 MiB (1%) |       32800 |
| `["collect", "assoc", "basesize=1024"]`             | 217.286 ms (5%) |         |   1.09 MiB (1%) |          53 |
| `["collect", "assoc", "basesize=32"]`               | 214.182 ms (5%) |         |   1.48 MiB (1%) |        1053 |
| `["collect", "seq"]`                                | 404.843 ms (5%) |         | 256.05 KiB (1%) |           2 |
| `["collect", "unordered", "basesize=1"]`            | 392.694 ms (5%) |         |  23.59 MiB (1%) |      402887 |
| `["collect", "unordered", "basesize=1024"]`         | 232.013 ms (5%) |         |   1.00 MiB (1%) |         849 |
| `["collect", "unordered", "basesize=32"]`           | 273.306 ms (5%) |         |   1.58 MiB (1%) |       14532 |
| `["findfirst", "n=1000", "foldl"]`                  | 686.418 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 405.817 ms (5%) |         | 230.48 KiB (1%) |        3245 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 527.836 ms (5%) |         | 159.23 KiB (1%) |        2234 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 493.817 ms (5%) |         |  81.33 KiB (1%) |        1146 |
| `["findfirst", "n=400", "foldl"]`                   | 514.827 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 273.243 ms (5%) |         | 385.66 KiB (1%) |        5489 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 287.643 ms (5%) |         | 200.86 KiB (1%) |        2873 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 287.001 ms (5%) |         | 107.16 KiB (1%) |        1551 |
| `["findfirst", "n=500", "foldl"]`                   |  90.044 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |  61.013 ms (5%) |         |  99.36 KiB (1%) |        1354 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |  99.628 ms (5%) |         |  80.11 KiB (1%) |        1088 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 122.979 ms (5%) |         |  63.67 KiB (1%) |         866 |
| `["overhead", "default"]`                           |  76.904 μs (5%) |         |  32.70 KiB (1%) |         417 |
| `["overhead", "stoppable=false"]`                   |  72.704 μs (5%) |         |  32.72 KiB (1%) |         417 |
| `["overhead", "stoppable=true"]`                    |  85.704 μs (5%) |         |  44.25 KiB (1%) |         610 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   3.238 ms (5%) |         | 728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   4.034 ms (5%) |         |   1.79 MiB (1%) |         216 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   3.597 ms (5%) |         |   1.42 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  19.837 ms (5%) |         |   1.58 MiB (1%) |        2342 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  21.447 ms (5%) |         |   1.14 MiB (1%) |        3548 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  24.483 ms (5%) |         |   1.29 MiB (1%) |        2606 |
| `["parallel_histogram", "seq"]`                     |   5.938 ms (5%) |         | 364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  34.072 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  18.701 ms (5%) |         |  736 bytes (1%) |          11 |
| `["splitby", "count", "foldl"]`                     |   1.868 ms (5%) |         |                 |             |
| `["splitby", "count", "man"]`                       |   1.181 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    | 914.045 μs (5%) |         |   1.09 KiB (1%) |          19 |
| `["sum", "random", "foldl"]`                        |  15.546 ms (5%) |         |                 |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   7.727 ms (5%) |         |  74.11 KiB (1%) |        1102 |
| `["sum", "random", "reduce", "basesize=256"]`       |   7.506 ms (5%) |         |  36.73 KiB (1%) |         546 |
| `["sum", "random", "reduce", "basesize=512"]`       |   7.217 ms (5%) |         |  18.08 KiB (1%) |         269 |
| `["sum", "uniform", "foldl"]`                       |  14.220 ms (5%) |         |                 |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   7.723 ms (5%) |         |  74.17 KiB (1%) |        1104 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   8.015 ms (5%) |         |  36.77 KiB (1%) |         547 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   7.371 ms (5%) |         |  18.03 KiB (1%) |         268 |
| `["sum", "valley", "foldl"]`                        |  15.518 ms (5%) |         |                 |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   7.851 ms (5%) |         |  74.11 KiB (1%) |        1102 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   7.534 ms (5%) |         |  36.70 KiB (1%) |         545 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   7.717 ms (5%) |         |  18.00 KiB (1%) |         267 |
| `["words", "nthreads=1"]`                           |  24.235 ms (5%) |         |  31.84 MiB (1%) |     1037008 |
| `["words", "nthreads=2"]`                           |  15.957 ms (5%) |         |  32.19 MiB (1%) |     1037061 |
| `["words", "nthreads=4"]`                           |  16.319 ms (5%) |         |  32.91 MiB (1%) |     1037164 |

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
  uname: Linux 5.15.0-1036-azure #43-Ubuntu SMP Wed Mar 29 16:11:05 UTC 2023 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz       5715 s          0 s        320 s       1777 s          0 s
       #2  2095 MHz       5039 s          0 s        374 s       2300 s          0 s
       
  Memory: 6.7812042236328125 GB (3723.375 MB free)
  Uptime: 801.71 sec
  Load Avg:  1.72  1.56  0.97
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, skylake-avx512)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 4 May 2023 - 6:22
* Package commit: f8d0df
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
| `["collect", "assoc", "basesize=1"]`                | 266.952 ms (5%) |         |  25.97 MiB (1%) |      306862 |
| `["collect", "assoc", "basesize=1024"]`             | 214.376 ms (5%) |         |   2.61 MiB (1%) |         455 |
| `["collect", "assoc", "basesize=32"]`               | 216.082 ms (5%) |         |   4.82 MiB (1%) |       11704 |
| `["collect", "seq"]`                                | 419.901 ms (5%) |         | 812.73 KiB (1%) |          11 |
| `["collect", "unordered", "basesize=1"]`            | 386.430 ms (5%) |         |  23.93 MiB (1%) |      414105 |
| `["collect", "unordered", "basesize=1024"]`         | 232.694 ms (5%) |         |   1.01 MiB (1%) |        1031 |
| `["collect", "unordered", "basesize=32"]`           | 239.894 ms (5%) |         |   1.58 MiB (1%) |       14521 |
| `["findfirst", "n=1000", "foldl"]`                  | 700.874 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 389.576 ms (5%) |         | 230.61 KiB (1%) |        3249 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 477.808 ms (5%) |         | 157.20 KiB (1%) |        2193 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 651.964 ms (5%) |         | 108.55 KiB (1%) |        1509 |
| `["findfirst", "n=400", "foldl"]`                   | 518.539 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 291.709 ms (5%) |         | 395.48 KiB (1%) |        5623 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 281.655 ms (5%) |         | 201.03 KiB (1%) |        2879 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 422.795 ms (5%) |         | 153.14 KiB (1%) |        2194 |
| `["findfirst", "n=500", "foldl"]`                   |  84.170 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 169.393 ms (5%) |         | 223.42 KiB (1%) |        3092 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 264.801 ms (5%) |         | 167.88 KiB (1%) |        2371 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 112.988 ms (5%) |         |  54.50 KiB (1%) |         748 |
| `["overhead", "default"]`                           |  70.204 μs (5%) |         |  32.73 KiB (1%) |         418 |
| `["overhead", "stoppable=false"]`                   |  70.904 μs (5%) |         |  32.72 KiB (1%) |         417 |
| `["overhead", "stoppable=true"]`                    |  78.805 μs (5%) |         |  44.25 KiB (1%) |         610 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   2.920 ms (5%) |         | 728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   3.570 ms (5%) |         |   1.79 MiB (1%) |         215 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   3.403 ms (5%) |         |   1.42 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  16.326 ms (5%) |         |   1.53 MiB (1%) |         810 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  25.273 ms (5%) |         |   1.21 MiB (1%) |        5779 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  23.254 ms (5%) |         |   1.32 MiB (1%) |        4737 |
| `["parallel_histogram", "seq"]`                     |   5.238 ms (5%) |         | 364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  36.073 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  18.242 ms (5%) |         |  736 bytes (1%) |          11 |
| `["splitby", "count", "foldl"]`                     |   1.883 ms (5%) |         |                 |             |
| `["splitby", "count", "man"]`                       |   1.184 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    | 970.459 μs (5%) |         |   1.09 KiB (1%) |          19 |
| `["sum", "random", "foldl"]`                        |  15.519 ms (5%) |         |                 |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   7.847 ms (5%) |         |  74.08 KiB (1%) |        1101 |
| `["sum", "random", "reduce", "basesize=256"]`       |   7.269 ms (5%) |         |  36.70 KiB (1%) |         545 |
| `["sum", "random", "reduce", "basesize=512"]`       |   7.482 ms (5%) |         |  18.11 KiB (1%) |         270 |
| `["sum", "uniform", "foldl"]`                       |  14.921 ms (5%) |         |                 |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   7.202 ms (5%) |         |  74.20 KiB (1%) |        1105 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   7.385 ms (5%) |         |  36.77 KiB (1%) |         547 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   7.538 ms (5%) |         |  18.03 KiB (1%) |         268 |
| `["sum", "valley", "foldl"]`                        |  15.358 ms (5%) |         |                 |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   7.978 ms (5%) |         |  74.05 KiB (1%) |        1100 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   7.698 ms (5%) |         |  36.77 KiB (1%) |         547 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   8.022 ms (5%) |         |  18.06 KiB (1%) |         269 |
| `["words", "nthreads=1"]`                           |  24.648 ms (5%) |         |  31.66 MiB (1%) |     1031064 |
| `["words", "nthreads=2"]`                           |  14.933 ms (5%) |         |  32.02 MiB (1%) |     1031100 |
| `["words", "nthreads=4"]`                           |  15.298 ms (5%) |         |  32.73 MiB (1%) |     1031179 |

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
  uname: Linux 5.15.0-1036-azure #43-Ubuntu SMP Wed Mar 29 16:11:05 UTC 2023 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz       7693 s          0 s        360 s       2789 s          0 s
       #2  2095 MHz       7743 s          0 s        420 s       2581 s          0 s
       
  Memory: 6.7812042236328125 GB (3874.15625 MB free)
  Uptime: 1105.33 sec
  Load Avg:  1.61  1.56  1.14
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
    Model name:                      Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz
    CPU family:                      6
    Model:                           85
    Thread(s) per core:              1
    Core(s) per socket:              2
    Socket(s):                       1
    Stepping:                        4
    BogoMIPS:                        4190.34
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
| Brand              | Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz           |
| Vendor             | :Intel                                                  |
| Architecture       | :Skylake                                                |
| Model              | Family: 0x06, Model: 0x55, Stepping: 0x04, Type: 0x00   |
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

