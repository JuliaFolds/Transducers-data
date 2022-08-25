# Multi-thread benchmark result

* Pull request commit: [`a7626ec825186254455005fd289dcdd42fb01164`](https://github.com/JuliaFolds/Transducers.jl/commit/a7626ec825186254455005fd289dcdd42fb01164)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/243> (Update */Manifest.toml)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 25 Aug 2022 - 02:37
    - Baseline: 25 Aug 2022 - 02:42
* Package commits:
    - Target: d849fb
    - Baseline: 6125fe
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
| `["collect", "unordered", "basesize=1"]`            | 0.94 (5%) :white_check_mark: |                   0.99 (1%)  |
| `["findfirst", "n=1000", "foldl"]`                  | 0.87 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` |                1.71 (5%) :x: |                1.68 (1%) :x: |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 0.92 (5%) :white_check_mark: | 0.94 (1%) :white_check_mark: |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` |                1.12 (5%) :x: |                1.10 (1%) :x: |
| `["findfirst", "n=400", "foldl"]`                   | 0.86 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  |                   1.04 (5%)  |                1.08 (1%) :x: |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  |                   0.99 (5%)  | 0.97 (1%) :white_check_mark: |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  |                1.05 (5%) :x: |                1.02 (1%) :x: |
| `["findfirst", "n=500", "foldl"]`                   | 0.87 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 0.65 (5%) :white_check_mark: | 0.71 (1%) :white_check_mark: |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 0.63 (5%) :white_check_mark: | 0.69 (1%) :white_check_mark: |
| `["overhead", "default"]`                           | 0.91 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |                1.09 (5%) :x: |                1.15 (1%) :x: |
| `["parallel_histogram", "comm", "basesize=16384"]`  | 0.86 (5%) :white_check_mark: | 0.99 (1%) :white_check_mark: |
| `["parallel_histogram", "comm", "basesize=4096"]`   | 0.88 (5%) :white_check_mark: | 0.96 (1%) :white_check_mark: |
| `["parallel_histogram", "comm", "basesize=8192"]`   | 0.89 (5%) :white_check_mark: | 0.92 (1%) :white_check_mark: |
| `["parallel_histogram", "seq"]`                     |                1.15 (5%) :x: |                   1.00 (1%)  |
| `["partition_length_maximum", "rand", "foldl"]`     | 0.85 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["splitby", "count", "reduce"]`                    |                1.05 (5%) :x: |                   1.00 (1%)  |
| `["words", "nthreads=1"]`                           |                1.07 (5%) :x: |                   1.00 (1%)  |
| `["words", "nthreads=2"]`                           |                   0.98 (5%)  | 0.99 (1%) :white_check_mark: |

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
      Ubuntu 20.04.4 LTS
  uname: Linux 5.15.0-1017-azure #20~20.04.1-Ubuntu SMP Fri Aug 5 12:16:53 UTC 2022 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2593 MHz       5437 s          1 s        213 s       1445 s          0 s
       #2  2593 MHz       4670 s          1 s        213 s       2231 s          0 s
       
  Memory: 6.781246185302734 GB (3716.609375 MB free)
  Uptime: 715.56 sec
  Load Avg:  1.72  1.52  0.9
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
      Ubuntu 20.04.4 LTS
  uname: Linux 5.15.0-1017-azure #20~20.04.1-Ubuntu SMP Fri Aug 5 12:16:53 UTC 2022 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2593 MHz       7644 s          1 s        282 s       2274 s          0 s
       #2  2593 MHz       7234 s          1 s        268 s       2718 s          0 s
       
  Memory: 6.781246185302734 GB (3645.296875 MB free)
  Uptime: 1026.51 sec
  Load Avg:  1.64  1.6  1.12
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, skylake-avx512)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 25 Aug 2022 - 2:37
* Package commit: d849fb
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
| `["collect", "assoc", "basesize=1"]`                | 231.565 ms (5%) |         |  25.97 MiB (1%) |      306857 |
| `["collect", "assoc", "basesize=1024"]`             | 185.819 ms (5%) |         |   2.61 MiB (1%) |         455 |
| `["collect", "assoc", "basesize=32"]`               | 187.983 ms (5%) |         |   4.82 MiB (1%) |       11700 |
| `["collect", "seq"]`                                | 394.956 ms (5%) |         | 812.73 KiB (1%) |          11 |
| `["collect", "unordered", "basesize=1"]`            | 325.817 ms (5%) |         |  23.83 MiB (1%) |      410543 |
| `["collect", "unordered", "basesize=1024"]`         | 200.064 ms (5%) |         |   1.01 MiB (1%) |        1069 |
| `["collect", "unordered", "basesize=32"]`           | 211.053 ms (5%) |         |   1.60 MiB (1%) |       15316 |
| `["findfirst", "n=1000", "foldl"]`                  | 550.857 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 550.440 ms (5%) |         | 390.39 KiB (1%) |        5501 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 367.844 ms (5%) |         | 143.05 KiB (1%) |        2007 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 517.919 ms (5%) |         | 106.31 KiB (1%) |        1484 |
| `["findfirst", "n=400", "foldl"]`                   | 409.330 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 235.648 ms (5%) |         | 400.23 KiB (1%) |        5689 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 231.348 ms (5%) |         | 200.78 KiB (1%) |        2870 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 322.494 ms (5%) |         | 142.44 KiB (1%) |        2031 |
| `["findfirst", "n=500", "foldl"]`                   |  71.260 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 125.227 ms (5%) |         | 202.19 KiB (1%) |        2762 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 112.503 ms (5%) |         |  98.36 KiB (1%) |        1355 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  99.787 ms (5%) |         |  55.88 KiB (1%) |         762 |
| `["overhead", "default"]`                           |  68.400 μs (5%) |         |  32.73 KiB (1%) |         418 |
| `["overhead", "stoppable=false"]`                   |  65.801 μs (5%) |         |  32.72 KiB (1%) |         417 |
| `["overhead", "stoppable=true"]`                    |  80.101 μs (5%) |         |  44.25 KiB (1%) |         610 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   3.225 ms (5%) |         | 728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   3.968 ms (5%) |         |   2.05 MiB (1%) |         221 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   3.541 ms (5%) |         |   1.42 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  15.303 ms (5%) |         |   1.56 MiB (1%) |        1759 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  21.263 ms (5%) |         |   1.18 MiB (1%) |        4794 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  18.557 ms (5%) |         |   1.21 MiB (1%) |        3519 |
| `["parallel_histogram", "seq"]`                     |   5.749 ms (5%) |         | 364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  30.078 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  17.526 ms (5%) |         |  736 bytes (1%) |          11 |
| `["splitby", "count", "foldl"]`                     |   2.333 ms (5%) |         |                 |             |
| `["splitby", "count", "man"]`                       |   1.752 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    |   1.150 ms (5%) |         |   1.09 KiB (1%) |          19 |
| `["sum", "random", "foldl"]`                        |  13.723 ms (5%) |         |                 |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   7.614 ms (5%) |         |  74.20 KiB (1%) |        1105 |
| `["sum", "random", "reduce", "basesize=256"]`       |   7.520 ms (5%) |         |  36.67 KiB (1%) |         544 |
| `["sum", "random", "reduce", "basesize=512"]`       |   7.461 ms (5%) |         |  18.11 KiB (1%) |         270 |
| `["sum", "uniform", "foldl"]`                       |  13.278 ms (5%) |         |                 |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   7.420 ms (5%) |         |  74.14 KiB (1%) |        1103 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   7.336 ms (5%) |         |  36.73 KiB (1%) |         546 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   7.334 ms (5%) |         |  18.03 KiB (1%) |         268 |
| `["sum", "valley", "foldl"]`                        |  13.636 ms (5%) |         |                 |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   7.570 ms (5%) |         |  74.11 KiB (1%) |        1102 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   7.485 ms (5%) |         |  36.70 KiB (1%) |         545 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   7.513 ms (5%) |         |  18.03 KiB (1%) |         268 |
| `["words", "nthreads=1"]`                           |  24.618 ms (5%) |         |  31.75 MiB (1%) |     1034188 |
| `["words", "nthreads=2"]`                           |  14.816 ms (5%) |         |  32.10 MiB (1%) |     1034224 |
| `["words", "nthreads=4"]`                           |  14.525 ms (5%) |         |  33.00 MiB (1%) |     1034367 |

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
      Ubuntu 20.04.4 LTS
  uname: Linux 5.15.0-1017-azure #20~20.04.1-Ubuntu SMP Fri Aug 5 12:16:53 UTC 2022 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2593 MHz       5437 s          1 s        213 s       1445 s          0 s
       #2  2593 MHz       4670 s          1 s        213 s       2231 s          0 s
       
  Memory: 6.781246185302734 GB (3716.609375 MB free)
  Uptime: 715.56 sec
  Load Avg:  1.72  1.52  0.9
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, skylake-avx512)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 25 Aug 2022 - 2:42
* Package commit: 6125fe
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
| `["collect", "assoc", "basesize=1"]`                | 231.288 ms (5%) |         |  25.97 MiB (1%) |      306801 |
| `["collect", "assoc", "basesize=1024"]`             | 185.767 ms (5%) |         |   2.61 MiB (1%) |         458 |
| `["collect", "assoc", "basesize=32"]`               | 188.151 ms (5%) |         |   4.82 MiB (1%) |       11708 |
| `["collect", "seq"]`                                | 395.257 ms (5%) |         | 812.73 KiB (1%) |          11 |
| `["collect", "unordered", "basesize=1"]`            | 347.256 ms (5%) |         |  24.04 MiB (1%) |      417727 |
| `["collect", "unordered", "basesize=1024"]`         | 200.628 ms (5%) |         |   1.01 MiB (1%) |        1093 |
| `["collect", "unordered", "basesize=32"]`           | 210.943 ms (5%) |         |   1.60 MiB (1%) |       15339 |
| `["findfirst", "n=1000", "foldl"]`                  | 631.511 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 321.422 ms (5%) |         | 232.33 KiB (1%) |        3259 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 398.484 ms (5%) |         | 151.83 KiB (1%) |        2127 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 462.906 ms (5%) |         |  96.88 KiB (1%) |        1350 |
| `["findfirst", "n=400", "foldl"]`                   | 473.953 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 226.645 ms (5%) |         | 371.95 KiB (1%) |        5308 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 233.318 ms (5%) |         | 206.97 KiB (1%) |        2949 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 305.881 ms (5%) |         | 139.09 KiB (1%) |        1976 |
| `["findfirst", "n=500", "foldl"]`                   |  82.154 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 193.178 ms (5%) |         | 286.39 KiB (1%) |        3941 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 177.400 ms (5%) |         | 142.33 KiB (1%) |        1961 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 100.442 ms (5%) |         |  55.92 KiB (1%) |         764 |
| `["overhead", "default"]`                           |  75.501 μs (5%) |         |  32.64 KiB (1%) |         415 |
| `["overhead", "stoppable=false"]`                   |  69.200 μs (5%) |         |  32.75 KiB (1%) |         418 |
| `["overhead", "stoppable=true"]`                    |  83.101 μs (5%) |         |  44.25 KiB (1%) |         610 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   3.209 ms (5%) |         | 728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   3.652 ms (5%) |         |   1.79 MiB (1%) |         216 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   3.523 ms (5%) |         |   1.42 MiB (1%) |         118 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  17.843 ms (5%) |         |   1.58 MiB (1%) |        2491 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  24.294 ms (5%) |         |   1.23 MiB (1%) |        6589 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  20.887 ms (5%) |         |   1.31 MiB (1%) |        5036 |
| `["parallel_histogram", "seq"]`                     |   4.990 ms (5%) |         | 364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  35.224 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  17.568 ms (5%) |         |  736 bytes (1%) |          11 |
| `["splitby", "count", "foldl"]`                     |   2.405 ms (5%) |         |                 |             |
| `["splitby", "count", "man"]`                       |   1.754 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    |   1.091 ms (5%) |         |   1.09 KiB (1%) |          19 |
| `["sum", "random", "foldl"]`                        |  13.981 ms (5%) |         |                 |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   7.536 ms (5%) |         |  74.17 KiB (1%) |        1104 |
| `["sum", "random", "reduce", "basesize=256"]`       |   7.502 ms (5%) |         |  36.77 KiB (1%) |         547 |
| `["sum", "random", "reduce", "basesize=512"]`       |   7.452 ms (5%) |         |  18.11 KiB (1%) |         270 |
| `["sum", "uniform", "foldl"]`                       |  13.337 ms (5%) |         |                 |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   7.324 ms (5%) |         |  74.14 KiB (1%) |        1103 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   7.282 ms (5%) |         |  36.67 KiB (1%) |         544 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   7.339 ms (5%) |         |  18.06 KiB (1%) |         269 |
| `["sum", "valley", "foldl"]`                        |  13.868 ms (5%) |         |                 |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   7.655 ms (5%) |         |  74.11 KiB (1%) |        1102 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   7.470 ms (5%) |         |  36.67 KiB (1%) |         544 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   7.509 ms (5%) |         |  18.06 KiB (1%) |         269 |
| `["words", "nthreads=1"]`                           |  22.999 ms (5%) |         |  31.75 MiB (1%) |     1034695 |
| `["words", "nthreads=2"]`                           |  15.044 ms (5%) |         |  32.47 MiB (1%) |     1034770 |
| `["words", "nthreads=4"]`                           |  14.995 ms (5%) |         |  32.91 MiB (1%) |     1034840 |

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
      Ubuntu 20.04.4 LTS
  uname: Linux 5.15.0-1017-azure #20~20.04.1-Ubuntu SMP Fri Aug 5 12:16:53 UTC 2022 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2593 MHz       7644 s          1 s        282 s       2274 s          0 s
       #2  2593 MHz       7234 s          1 s        268 s       2718 s          0 s
       
  Memory: 6.781246185302734 GB (3645.296875 MB free)
  Uptime: 1026.51 sec
  Load Avg:  1.64  1.6  1.12
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
    Model:                           85
    Model name:                      Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz
    Stepping:                        7
    CPU MHz:                         2593.906
    BogoMIPS:                        5187.81
    Hypervisor vendor:               Microsoft
    Virtualization type:             full
    L1d cache:                       64 KiB
    L1i cache:                       64 KiB
    L2 cache:                        2 MiB
    L3 cache:                        35.8 MiB
    NUMA node0 CPU(s):               0,1
    Vulnerability Itlb multihit:     KVM: Mitigation: VMX unsupported
    Vulnerability L1tf:              Mitigation; PTE Inversion
    Vulnerability Mds:               Mitigation; Clear CPU buffers; SMT Host state unknown
    Vulnerability Meltdown:          Mitigation; PTI
    Vulnerability Mmio stale data:   Vulnerable: Clear CPU buffers attempted, no microcode; SMT Host state unknown
    Vulnerability Retbleed:          Vulnerable
    Vulnerability Spec store bypass: Vulnerable
    Vulnerability Spectre v1:        Mitigation; usercopy/swapgs barriers and __user pointer sanitization
    Vulnerability Spectre v2:        Mitigation; Retpolines, STIBP disabled, RSB filling
    Vulnerability Srbds:             Not affected
    Vulnerability Tsx async abort:   Mitigation; Clear CPU buffers; SMT Host state unknown
    Flags:                           fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush mmx fxsr sse sse2 ss ht syscall nx pdpe1gb rdtscp lm constant_tsc rep_good nopl xtopology cpuid pni pclmulqdq ssse3 fma cx16 pcid sse4_1 sse4_2 movbe popcnt aes xsave avx f16c rdrand hypervisor lahf_lm abm 3dnowprefetch invpcid_single pti fsgsbase bmi1 hle avx2 smep bmi2 erms invpcid rtm mpx avx512f avx512dq rdseed adx smap clflushopt avx512cd avx512bw avx512vl xsaveopt xsavec xsaves md_clear
    

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

