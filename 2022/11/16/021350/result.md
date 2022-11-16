# Multi-thread benchmark result

* Pull request commit: [`bb51578092d50f5b9ae435d92453208c637e677e`](https://github.com/JuliaFolds/Transducers.jl/commit/bb51578092d50f5b9ae435d92453208c637e677e)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/243> (Update */Manifest.toml)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 16 Nov 2022 - 02:08
    - Baseline: 16 Nov 2022 - 02:13
* Package commits:
    - Target: c3697e
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
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 0.70 (5%) :white_check_mark: | 0.71 (1%) :white_check_mark: |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` |                1.19 (5%) :x: |                1.18 (1%) :x: |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` |                   0.99 (5%)  |                1.05 (1%) :x: |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  |                   1.03 (5%)  |                1.02 (1%) :x: |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 0.88 (5%) :white_check_mark: | 0.92 (1%) :white_check_mark: |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |                   1.05 (5%)  |                1.06 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 0.33 (5%) :white_check_mark: | 0.47 (1%) :white_check_mark: |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |                1.42 (5%) :x: |                1.25 (1%) :x: |
| `["parallel_histogram", "comm", "basesize=16384"]`  |                   1.01 (5%)  |                1.02 (1%) :x: |
| `["parallel_histogram", "comm", "basesize=4096"]`   |                   0.97 (5%)  | 0.89 (1%) :white_check_mark: |
| `["parallel_histogram", "comm", "basesize=8192"]`   |                1.19 (5%) :x: |                1.03 (1%) :x: |
| `["splitby", "count", "reduce"]`                    |                   0.98 (5%)  | 0.97 (1%) :white_check_mark: |
| `["words", "nthreads=2"]`                           |                   1.05 (5%)  |                1.01 (1%) :x: |
| `["words", "nthreads=4"]`                           |                1.05 (5%) :x: |                   1.00 (1%)  |

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
      Ubuntu 20.04.5 LTS
  uname: Linux 5.15.0-1022-azure #27~20.04.1-Ubuntu SMP Mon Oct 17 02:03:50 UTC 2022 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8370C CPU @ 2.80GHz: 
              speed         user         nice          sys         idle          irq
       #1  2793 MHz       5138 s          1 s        217 s       3691 s          0 s
       #2  2793 MHz       5162 s          2 s        239 s       3648 s          0 s
       
  Memory: 6.781246185302734 GB (3230.64453125 MB free)
  Uptime: 908.92 sec
  Load Avg:  1.7  1.48  0.87
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, icelake-server)
```

### Baseline
```
Julia Version 1.7.3
Commit 742b9abb4d (2022-05-06 12:58 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 20.04.5 LTS
  uname: Linux 5.15.0-1022-azure #27~20.04.1-Ubuntu SMP Mon Oct 17 02:03:50 UTC 2022 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8370C CPU @ 2.80GHz: 
              speed         user         nice          sys         idle          irq
       #1  2793 MHz       7545 s          1 s        276 s       4298 s          0 s
       #2  2793 MHz       7519 s          2 s        298 s       4307 s          0 s
       
  Memory: 6.781246185302734 GB (3117.59375 MB free)
  Uptime: 1216.8 sec
  Load Avg:  1.45  1.54  1.08
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, icelake-server)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 16 Nov 2022 - 2:8
* Package commit: c3697e
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
| `["collect", "assoc", "basesize=1"]`                | 281.234 ms (5%) |         |  25.97 MiB (1%) |      306869 |
| `["collect", "assoc", "basesize=1024"]`             | 238.838 ms (5%) |         |   2.61 MiB (1%) |         456 |
| `["collect", "assoc", "basesize=32"]`               | 240.927 ms (5%) |         |   4.82 MiB (1%) |       11708 |
| `["collect", "seq"]`                                | 477.376 ms (5%) |         | 812.73 KiB (1%) |          11 |
| `["collect", "unordered", "basesize=1"]`            | 380.435 ms (5%) |         |  23.90 MiB (1%) |      413148 |
| `["collect", "unordered", "basesize=1024"]`         | 251.723 ms (5%) |         |   1.01 MiB (1%) |        1007 |
| `["collect", "unordered", "basesize=32"]`           | 262.724 ms (5%) |         |   1.59 MiB (1%) |       15122 |
| `["findfirst", "n=1000", "foldl"]`                  | 741.675 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 407.689 ms (5%) |         | 232.86 KiB (1%) |        3276 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 592.507 ms (5%) |         | 185.80 KiB (1%) |        2583 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 666.865 ms (5%) |         | 108.55 KiB (1%) |        1509 |
| `["findfirst", "n=400", "foldl"]`                   | 556.502 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 285.046 ms (5%) |         | 371.16 KiB (1%) |        5297 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 300.370 ms (5%) |         | 202.47 KiB (1%) |        2897 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 366.682 ms (5%) |         | 132.86 KiB (1%) |        1892 |
| `["findfirst", "n=500", "foldl"]`                   |  96.380 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 160.462 ms (5%) |         | 198.19 KiB (1%) |        2735 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |  90.824 ms (5%) |         |  78.36 KiB (1%) |        1065 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 138.419 ms (5%) |         |  63.69 KiB (1%) |         866 |
| `["overhead", "default"]`                           |  70.999 μs (5%) |         |  32.73 KiB (1%) |         418 |
| `["overhead", "stoppable=false"]`                   |  71.800 μs (5%) |         |  32.75 KiB (1%) |         418 |
| `["overhead", "stoppable=true"]`                    |  81.900 μs (5%) |         |  44.28 KiB (1%) |         611 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   3.728 ms (5%) |         | 728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   4.496 ms (5%) |         |   1.79 MiB (1%) |         215 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   4.121 ms (5%) |         |   1.42 MiB (1%) |         118 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  16.235 ms (5%) |         |   1.70 MiB (1%) |        6218 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  25.710 ms (5%) |         |   1.30 MiB (1%) |        8802 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  23.600 ms (5%) |         |   1.39 MiB (1%) |       11774 |
| `["parallel_histogram", "seq"]`                     |   6.723 ms (5%) |         | 364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  41.300 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  20.581 ms (5%) |         |  736 bytes (1%) |          11 |
| `["splitby", "count", "foldl"]`                     |   2.305 ms (5%) |         |                 |             |
| `["splitby", "count", "man"]`                       |   1.529 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    |   1.128 ms (5%) |         |   1.06 KiB (1%) |          18 |
| `["sum", "random", "foldl"]`                        |  18.015 ms (5%) |         |                 |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   9.248 ms (5%) |         |  74.17 KiB (1%) |        1104 |
| `["sum", "random", "reduce", "basesize=256"]`       |   9.142 ms (5%) |         |  36.80 KiB (1%) |         548 |
| `["sum", "random", "reduce", "basesize=512"]`       |   9.081 ms (5%) |         |  18.11 KiB (1%) |         270 |
| `["sum", "uniform", "foldl"]`                       |  17.723 ms (5%) |         |                 |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   9.076 ms (5%) |         |  74.17 KiB (1%) |        1104 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   8.988 ms (5%) |         |  36.77 KiB (1%) |         547 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   8.924 ms (5%) |         |  18.00 KiB (1%) |         267 |
| `["sum", "valley", "foldl"]`                        |  18.135 ms (5%) |         |                 |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   9.306 ms (5%) |         |  74.05 KiB (1%) |        1100 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   9.181 ms (5%) |         |  36.70 KiB (1%) |         545 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   9.220 ms (5%) |         |  18.03 KiB (1%) |         268 |
| `["words", "nthreads=1"]`                           |  18.931 ms (5%) |         |  31.78 MiB (1%) |     1035771 |
| `["words", "nthreads=2"]`                           |  12.718 ms (5%) |         |  32.50 MiB (1%) |     1035862 |
| `["words", "nthreads=4"]`                           |  13.487 ms (5%) |         |  33.13 MiB (1%) |     1036009 |

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
      Ubuntu 20.04.5 LTS
  uname: Linux 5.15.0-1022-azure #27~20.04.1-Ubuntu SMP Mon Oct 17 02:03:50 UTC 2022 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8370C CPU @ 2.80GHz: 
              speed         user         nice          sys         idle          irq
       #1  2793 MHz       5138 s          1 s        217 s       3691 s          0 s
       #2  2793 MHz       5162 s          2 s        239 s       3648 s          0 s
       
  Memory: 6.781246185302734 GB (3230.64453125 MB free)
  Uptime: 908.92 sec
  Load Avg:  1.7  1.48  0.87
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, icelake-server)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 16 Nov 2022 - 2:13
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
| `["collect", "assoc", "basesize=1"]`                | 283.647 ms (5%) |         |  25.97 MiB (1%) |      306830 |
| `["collect", "assoc", "basesize=1024"]`             | 239.145 ms (5%) |         |   2.61 MiB (1%) |         456 |
| `["collect", "assoc", "basesize=32"]`               | 241.374 ms (5%) |         |   4.82 MiB (1%) |       11706 |
| `["collect", "seq"]`                                | 477.751 ms (5%) |         | 812.73 KiB (1%) |          11 |
| `["collect", "unordered", "basesize=1"]`            | 382.534 ms (5%) |         |  23.91 MiB (1%) |      413267 |
| `["collect", "unordered", "basesize=1024"]`         | 252.365 ms (5%) |         |   1.01 MiB (1%) |        1006 |
| `["collect", "unordered", "basesize=32"]`           | 264.296 ms (5%) |         |   1.59 MiB (1%) |       15030 |
| `["findfirst", "n=1000", "foldl"]`                  | 741.610 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 581.227 ms (5%) |         | 327.75 KiB (1%) |        4590 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 498.478 ms (5%) |         | 157.23 KiB (1%) |        2194 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 675.870 ms (5%) |         | 103.53 KiB (1%) |        1454 |
| `["findfirst", "n=400", "foldl"]`                   | 556.669 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 285.541 ms (5%) |         | 371.22 KiB (1%) |        5299 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 291.523 ms (5%) |         | 197.78 KiB (1%) |        2833 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 418.196 ms (5%) |         | 145.17 KiB (1%) |        2079 |
| `["findfirst", "n=500", "foldl"]`                   |  96.374 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 153.466 ms (5%) |         | 186.88 KiB (1%) |        2583 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 276.876 ms (5%) |         | 167.84 KiB (1%) |        2370 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  97.258 ms (5%) |         |  50.78 KiB (1%) |         679 |
| `["overhead", "default"]`                           |  71.500 μs (5%) |         |  32.77 KiB (1%) |         419 |
| `["overhead", "stoppable=false"]`                   |  72.900 μs (5%) |         |  32.69 KiB (1%) |         416 |
| `["overhead", "stoppable=true"]`                    |  81.799 μs (5%) |         |  44.25 KiB (1%) |         610 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   3.746 ms (5%) |         | 728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   4.531 ms (5%) |         |   1.79 MiB (1%) |         216 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   4.137 ms (5%) |         |   1.42 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  16.138 ms (5%) |         |   1.66 MiB (1%) |        5063 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  26.445 ms (5%) |         |   1.46 MiB (1%) |       13961 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  19.894 ms (5%) |         |   1.36 MiB (1%) |        3998 |
| `["parallel_histogram", "seq"]`                     |   6.686 ms (5%) |         | 364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  41.215 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  20.619 ms (5%) |         |  736 bytes (1%) |          11 |
| `["splitby", "count", "foldl"]`                     |   2.323 ms (5%) |         |                 |             |
| `["splitby", "count", "man"]`                       |   1.531 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    |   1.151 ms (5%) |         |   1.09 KiB (1%) |          19 |
| `["sum", "random", "foldl"]`                        |  17.951 ms (5%) |         |                 |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   9.137 ms (5%) |         |  74.14 KiB (1%) |        1103 |
| `["sum", "random", "reduce", "basesize=256"]`       |   9.095 ms (5%) |         |  36.77 KiB (1%) |         547 |
| `["sum", "random", "reduce", "basesize=512"]`       |   9.048 ms (5%) |         |  18.08 KiB (1%) |         269 |
| `["sum", "uniform", "foldl"]`                       |  17.722 ms (5%) |         |                 |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   9.084 ms (5%) |         |  74.14 KiB (1%) |        1103 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   8.991 ms (5%) |         |  36.61 KiB (1%) |         542 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   8.940 ms (5%) |         |  18.03 KiB (1%) |         268 |
| `["sum", "valley", "foldl"]`                        |  18.135 ms (5%) |         |                 |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   9.317 ms (5%) |         |  74.08 KiB (1%) |        1101 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   9.218 ms (5%) |         |  36.70 KiB (1%) |         545 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   9.222 ms (5%) |         |  18.06 KiB (1%) |         269 |
| `["words", "nthreads=1"]`                           |  19.589 ms (5%) |         |  31.80 MiB (1%) |     1036708 |
| `["words", "nthreads=2"]`                           |  12.139 ms (5%) |         |  32.15 MiB (1%) |     1036744 |
| `["words", "nthreads=4"]`                           |  12.816 ms (5%) |         |  33.05 MiB (1%) |     1036895 |

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
      Ubuntu 20.04.5 LTS
  uname: Linux 5.15.0-1022-azure #27~20.04.1-Ubuntu SMP Mon Oct 17 02:03:50 UTC 2022 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8370C CPU @ 2.80GHz: 
              speed         user         nice          sys         idle          irq
       #1  2793 MHz       7545 s          1 s        276 s       4298 s          0 s
       #2  2793 MHz       7519 s          2 s        298 s       4307 s          0 s
       
  Memory: 6.781246185302734 GB (3117.59375 MB free)
  Uptime: 1216.8 sec
  Load Avg:  1.45  1.54  1.08
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, icelake-server)
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
    Model:                           106
    Model name:                      Intel(R) Xeon(R) Platinum 8370C CPU @ 2.80GHz
    Stepping:                        6
    CPU MHz:                         2793.436
    BogoMIPS:                        5586.87
    Hypervisor vendor:               Microsoft
    Virtualization type:             full
    L1d cache:                       96 KiB
    L1i cache:                       64 KiB
    L2 cache:                        2.5 MiB
    L3 cache:                        48 MiB
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
    Flags:                           fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush mmx fxsr sse sse2 ss ht syscall nx pdpe1gb rdtscp lm constant_tsc rep_good nopl xtopology cpuid pni pclmulqdq ssse3 fma cx16 pcid sse4_1 sse4_2 movbe popcnt aes xsave avx f16c rdrand hypervisor lahf_lm abm 3dnowprefetch invpcid_single pti fsgsbase bmi1 hle avx2 smep bmi2 erms invpcid rtm avx512f avx512dq rdseed adx smap clflushopt avx512cd avx512bw avx512vl xsaveopt xsavec xsaves md_clear
    

| Cpu Property       | Value                                                   |
|:------------------ |:------------------------------------------------------- |
| Brand              | Intel(R) Xeon(R) Platinum 8370C CPU @ 2.80GHz           |
| Vendor             | :Intel                                                  |
| Architecture       | :UnknownIntel                                           |
| Model              | Family: 0x06, Model: 0x6a, Stepping: 0x06, Type: 0x00   |
| Cores              | 2 physical cores, 2 logical cores (on executing CPU)    |
|                    | No Hyperthreading hardware capability detected          |
| Clock Frequencies  | Not supported by CPU                                    |
| Data Cache         | Level 1:3 : (48, 1280, 49152) kbytes                    |
|                    | 64 byte cache line size                                 |
| Address Size       | 48 bits virtual, 46 bits physical                       |
| SIMD               | 512 bit = 64 byte max. SIMD vector size                 |
| Time Stamp Counter | TSC is accessible via `rdtsc`                           |
|                    | TSC increased at every clock cycle (non-invariant TSC)  |
| Perf. Monitoring   | Performance Monitoring Counters (PMC) are not supported |
| Hypervisor         | Yes, Microsoft                                          |

