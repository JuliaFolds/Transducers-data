# Multi-thread benchmark result

* Pull request commit: [`e11ef25aef5ec9ea996e5c54efd796bc91066900`](https://github.com/JuliaFolds/Transducers.jl/commit/e11ef25aef5ec9ea996e5c54efd796bc91066900)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/243> (Update */Manifest.toml)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 23 Jul 2022 - 02:22
    - Baseline: 23 Jul 2022 - 02:27
* Package commits:
    - Target: 2e3bce
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
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 0.45 (5%) :white_check_mark: | 0.46 (1%) :white_check_mark: |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 0.77 (5%) :white_check_mark: | 0.85 (1%) :white_check_mark: |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 0.92 (5%) :white_check_mark: | 0.98 (1%) :white_check_mark: |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  |                   1.03 (5%)  | 0.98 (1%) :white_check_mark: |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  |                1.16 (5%) :x: |                1.08 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 0.82 (5%) :white_check_mark: | 0.90 (1%) :white_check_mark: |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |                1.10 (5%) :x: |                1.04 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |                2.47 (5%) :x: |                1.97 (1%) :x: |
| `["parallel_histogram", "assoc", "basesize=4096"]`  | 0.90 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["parallel_histogram", "assoc", "basesize=8192"]`  | 0.91 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["parallel_histogram", "comm", "basesize=16384"]`  | 0.92 (5%) :white_check_mark: |                1.20 (1%) :x: |
| `["parallel_histogram", "comm", "basesize=4096"]`   |                   1.00 (5%)  |                1.11 (1%) :x: |
| `["parallel_histogram", "comm", "basesize=8192"]`   |                   1.02 (5%)  |                1.02 (1%) :x: |
| `["splitby", "count", "foldl"]`                     | 0.86 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["splitby", "count", "man"]`                       | 0.81 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["splitby", "count", "reduce"]`                    |                   0.98 (5%)  |                1.06 (1%) :x: |
| `["sum", "uniform", "reduce", "basesize=128"]`      | 0.91 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["sum", "uniform", "reduce", "basesize=256"]`      | 0.91 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["sum", "uniform", "reduce", "basesize=512"]`      | 0.95 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["sum", "valley", "foldl"]`                        | 0.93 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["words", "nthreads=1"]`                           |                   0.98 (5%)  |                1.01 (1%) :x: |
| `["words", "nthreads=2"]`                           | 0.92 (5%) :white_check_mark: |                1.01 (1%) :x: |
| `["words", "nthreads=4"]`                           |                   0.98 (5%)  |                1.02 (1%) :x: |

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
  uname: Linux 5.15.0-1014-azure #17~20.04.1-Ubuntu SMP Thu Jun 23 20:01:51 UTC 2022 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz       5217 s        453 s        301 s       1222 s          0 s
       #2  2095 MHz       5137 s        518 s        294 s       1288 s          0 s
       
  Memory: 6.780967712402344 GB (1460.96484375 MB free)
  Uptime: 726.42 sec
  Load Avg:  2.35  2.23  1.35
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
  uname: Linux 5.15.0-1014-azure #17~20.04.1-Ubuntu SMP Thu Jun 23 20:01:51 UTC 2022 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz       7537 s        694 s        393 s       1776 s          0 s
       #2  2095 MHz       7507 s        757 s        387 s       1796 s          0 s
       
  Memory: 6.780967712402344 GB (1231.21875 MB free)
  Uptime: 1046.71 sec
  Load Avg:  2.25  2.3  1.65
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, skylake-avx512)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 23 Jul 2022 - 2:22
* Package commit: 2e3bce
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
| `["collect", "assoc", "basesize=1"]`                | 288.704 ms (5%) |         |  25.97 MiB (1%) |      306780 |
| `["collect", "assoc", "basesize=1024"]`             | 226.683 ms (5%) |         |   2.61 MiB (1%) |         456 |
| `["collect", "assoc", "basesize=32"]`               | 230.617 ms (5%) |         |   4.82 MiB (1%) |       11714 |
| `["collect", "seq"]`                                | 436.800 ms (5%) |         | 812.73 KiB (1%) |          11 |
| `["collect", "unordered", "basesize=1"]`            | 450.888 ms (5%) |         |  24.00 MiB (1%) |      416377 |
| `["collect", "unordered", "basesize=1024"]`         | 248.197 ms (5%) |         |   1.01 MiB (1%) |        1055 |
| `["collect", "unordered", "basesize=32"]`           | 287.773 ms (5%) |         |   1.59 MiB (1%) |       14884 |
| `["findfirst", "n=1000", "foldl"]`                  | 700.640 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 406.342 ms (5%) |         | 230.39 KiB (1%) |        3242 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 487.534 ms (5%) |         | 157.23 KiB (1%) |        2194 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 562.907 ms (5%) |         |  96.75 KiB (1%) |        1346 |
| `["findfirst", "n=400", "foldl"]`                   | 516.475 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 286.877 ms (5%) |         | 376.72 KiB (1%) |        5371 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 289.898 ms (5%) |         | 204.81 KiB (1%) |        2927 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 436.227 ms (5%) |         | 150.16 KiB (1%) |        2156 |
| `["findfirst", "n=500", "foldl"]`                   |  88.028 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 150.652 ms (5%) |         | 190.66 KiB (1%) |        2630 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |  96.482 ms (5%) |         |  82.22 KiB (1%) |        1108 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 312.796 ms (5%) |         | 110.19 KiB (1%) |        1524 |
| `["overhead", "default"]`                           |  73.205 μs (5%) |         |  32.73 KiB (1%) |         418 |
| `["overhead", "stoppable=false"]`                   |  77.105 μs (5%) |         |  32.75 KiB (1%) |         418 |
| `["overhead", "stoppable=true"]`                    |  81.605 μs (5%) |         |  44.25 KiB (1%) |         610 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   2.866 ms (5%) |         | 728.88 KiB (1%) |          56 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   3.476 ms (5%) |         |   1.79 MiB (1%) |         215 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   3.266 ms (5%) |         |   1.42 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  14.040 ms (5%) |         |   1.51 MiB (1%) |         144 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  23.137 ms (5%) |         |   1.15 MiB (1%) |        3899 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  21.467 ms (5%) |         |   1.18 MiB (1%) |         816 |
| `["parallel_histogram", "seq"]`                     |   5.173 ms (5%) |         | 364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  35.720 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  18.734 ms (5%) |         |  736 bytes (1%) |          11 |
| `["splitby", "count", "foldl"]`                     |   1.819 ms (5%) |         |                 |             |
| `["splitby", "count", "man"]`                       |   1.182 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    | 932.161 μs (5%) |         |   1.09 KiB (1%) |          19 |
| `["sum", "random", "foldl"]`                        |  16.127 ms (5%) |         |                 |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   8.586 ms (5%) |         |  73.95 KiB (1%) |        1097 |
| `["sum", "random", "reduce", "basesize=256"]`       |   8.364 ms (5%) |         |  36.70 KiB (1%) |         545 |
| `["sum", "random", "reduce", "basesize=512"]`       |   8.273 ms (5%) |         |  18.02 KiB (1%) |         267 |
| `["sum", "uniform", "foldl"]`                       |  15.805 ms (5%) |         |                 |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   7.878 ms (5%) |         |  74.14 KiB (1%) |        1103 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   7.574 ms (5%) |         |  36.70 KiB (1%) |         545 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   7.755 ms (5%) |         |  18.03 KiB (1%) |         268 |
| `["sum", "valley", "foldl"]`                        |  15.749 ms (5%) |         |                 |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   8.296 ms (5%) |         |  74.11 KiB (1%) |        1102 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   8.470 ms (5%) |         |  36.70 KiB (1%) |         545 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   8.582 ms (5%) |         |  18.00 KiB (1%) |         267 |
| `["words", "nthreads=1"]`                           |  24.488 ms (5%) |         |  31.87 MiB (1%) |     1038461 |
| `["words", "nthreads=2"]`                           |  15.443 ms (5%) |         |  32.59 MiB (1%) |     1038563 |
| `["words", "nthreads=4"]`                           |  16.173 ms (5%) |         |  33.22 MiB (1%) |     1038723 |

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
  uname: Linux 5.15.0-1014-azure #17~20.04.1-Ubuntu SMP Thu Jun 23 20:01:51 UTC 2022 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz       5217 s        453 s        301 s       1222 s          0 s
       #2  2095 MHz       5137 s        518 s        294 s       1288 s          0 s
       
  Memory: 6.780967712402344 GB (1460.96484375 MB free)
  Uptime: 726.42 sec
  Load Avg:  2.35  2.23  1.35
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, skylake-avx512)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 23 Jul 2022 - 2:27
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
| `["collect", "assoc", "basesize=1"]`                | 286.864 ms (5%) |         |  25.97 MiB (1%) |      306869 |
| `["collect", "assoc", "basesize=1024"]`             | 232.964 ms (5%) |         |   2.61 MiB (1%) |         457 |
| `["collect", "assoc", "basesize=32"]`               | 233.294 ms (5%) |         |   4.82 MiB (1%) |       11711 |
| `["collect", "seq"]`                                | 427.403 ms (5%) |         | 812.73 KiB (1%) |          11 |
| `["collect", "unordered", "basesize=1"]`            | 462.347 ms (5%) |         |  23.99 MiB (1%) |      415923 |
| `["collect", "unordered", "basesize=1024"]`         | 242.722 ms (5%) |         |   1.01 MiB (1%) |        1000 |
| `["collect", "unordered", "basesize=32"]`           | 278.311 ms (5%) |         |   1.58 MiB (1%) |       14711 |
| `["findfirst", "n=1000", "foldl"]`                  | 706.154 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 909.932 ms (5%) |         | 505.27 KiB (1%) |        7141 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 633.143 ms (5%) |         | 184.94 KiB (1%) |        2585 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 615.123 ms (5%) |         |  98.38 KiB (1%) |        1370 |
| `["findfirst", "n=400", "foldl"]`                   | 506.750 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 279.192 ms (5%) |         | 379.91 KiB (1%) |        5410 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 282.368 ms (5%) |         | 209.77 KiB (1%) |        2994 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 375.903 ms (5%) |         | 138.97 KiB (1%) |        1972 |
| `["findfirst", "n=500", "foldl"]`                   |  86.771 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 184.280 ms (5%) |         | 212.67 KiB (1%) |        2939 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |  87.449 ms (5%) |         |  79.00 KiB (1%) |        1064 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 126.668 ms (5%) |         |  55.95 KiB (1%) |         765 |
| `["overhead", "default"]`                           |  76.105 μs (5%) |         |  32.73 KiB (1%) |         418 |
| `["overhead", "stoppable=false"]`                   |  74.305 μs (5%) |         |  32.75 KiB (1%) |         418 |
| `["overhead", "stoppable=true"]`                    |  85.106 μs (5%) |         |  44.25 KiB (1%) |         610 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   2.947 ms (5%) |         | 728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   3.878 ms (5%) |         |   1.79 MiB (1%) |         216 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   3.584 ms (5%) |         |   1.42 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  15.244 ms (5%) |         |   1.26 MiB (1%) |         144 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  23.065 ms (5%) |         |   1.04 MiB (1%) |         225 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  21.130 ms (5%) |         |   1.16 MiB (1%) |        2638 |
| `["parallel_histogram", "seq"]`                     |   4.962 ms (5%) |         | 364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  36.277 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  18.873 ms (5%) |         |  736 bytes (1%) |          11 |
| `["splitby", "count", "foldl"]`                     |   2.122 ms (5%) |         |                 |             |
| `["splitby", "count", "man"]`                       |   1.461 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    | 950.162 μs (5%) |         |   1.03 KiB (1%) |          18 |
| `["sum", "random", "foldl"]`                        |  15.830 ms (5%) |         |                 |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   8.260 ms (5%) |         |  74.11 KiB (1%) |        1102 |
| `["sum", "random", "reduce", "basesize=256"]`       |   8.094 ms (5%) |         |  36.70 KiB (1%) |         545 |
| `["sum", "random", "reduce", "basesize=512"]`       |   8.095 ms (5%) |         |  18.08 KiB (1%) |         269 |
| `["sum", "uniform", "foldl"]`                       |  15.933 ms (5%) |         |                 |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   8.632 ms (5%) |         |  74.17 KiB (1%) |        1104 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   8.311 ms (5%) |         |  36.73 KiB (1%) |         546 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   8.198 ms (5%) |         |  18.03 KiB (1%) |         268 |
| `["sum", "valley", "foldl"]`                        |  16.886 ms (5%) |         |                 |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   8.670 ms (5%) |         |  74.14 KiB (1%) |        1103 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   8.395 ms (5%) |         |  36.73 KiB (1%) |         546 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   8.256 ms (5%) |         |  18.03 KiB (1%) |         268 |
| `["words", "nthreads=1"]`                           |  24.975 ms (5%) |         |  31.53 MiB (1%) |     1026953 |
| `["words", "nthreads=2"]`                           |  16.770 ms (5%) |         |  32.24 MiB (1%) |     1027035 |
| `["words", "nthreads=4"]`                           |  16.495 ms (5%) |         |  32.69 MiB (1%) |     1027132 |

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
  uname: Linux 5.15.0-1014-azure #17~20.04.1-Ubuntu SMP Thu Jun 23 20:01:51 UTC 2022 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz       7537 s        694 s        393 s       1776 s          0 s
       #2  2095 MHz       7507 s        757 s        387 s       1796 s          0 s
       
  Memory: 6.780967712402344 GB (1231.21875 MB free)
  Uptime: 1046.71 sec
  Load Avg:  2.25  2.3  1.65
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
    Model name:                      Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz
    Stepping:                        4
    CPU MHz:                         2095.196
    BogoMIPS:                        4190.39
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
    Vulnerability Spec store bypass: Vulnerable
    Vulnerability Spectre v1:        Mitigation; usercopy/swapgs barriers and __user pointer sanitization
    Vulnerability Spectre v2:        Mitigation; Retpolines, STIBP disabled, RSB filling
    Vulnerability Srbds:             Not affected
    Vulnerability Tsx async abort:   Mitigation; Clear CPU buffers; SMT Host state unknown
    Flags:                           fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush mmx fxsr sse sse2 ss ht syscall nx pdpe1gb rdtscp lm constant_tsc rep_good nopl xtopology cpuid pni pclmulqdq ssse3 fma cx16 pcid sse4_1 sse4_2 movbe popcnt aes xsave avx f16c rdrand hypervisor lahf_lm abm 3dnowprefetch invpcid_single pti fsgsbase bmi1 hle avx2 smep bmi2 erms invpcid rtm mpx avx512f avx512dq rdseed adx smap clflushopt avx512cd avx512bw avx512vl xsaveopt xsavec xsaves md_clear
    

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

