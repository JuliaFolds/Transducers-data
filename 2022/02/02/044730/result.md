# Multi-thread benchmark result

* Pull request commit: [`b7a488c44d91b204780861c9e0faab8a96da9408`](https://github.com/JuliaFolds/Transducers.jl/commit/b7a488c44d91b204780861c9e0faab8a96da9408)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/510> (Don't use `@_inline_meta`)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 2 Feb 2022 - 04:41
    - Baseline: 2 Feb 2022 - 04:46
* Package commits:
    - Target: 0b0693
    - Baseline: 332ac4
* Julia commits:
    - Target: ac5cc9
    - Baseline: ac5cc9
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
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 0.78 (5%) :white_check_mark: | 0.79 (1%) :white_check_mark: |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 0.92 (5%) :white_check_mark: | 0.91 (1%) :white_check_mark: |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  |                1.27 (5%) :x: |                1.22 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 0.91 (5%) :white_check_mark: | 0.87 (1%) :white_check_mark: |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 0.85 (5%) :white_check_mark: | 0.95 (1%) :white_check_mark: |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |                   0.97 (5%)  |                1.07 (1%) :x: |
| `["parallel_histogram", "comm", "basesize=16384"]`  |                1.13 (5%) :x: |                   1.00 (1%)  |
| `["parallel_histogram", "comm", "basesize=4096"]`   |                   1.01 (5%)  |                1.02 (1%) :x: |
| `["parallel_histogram", "comm", "basesize=8192"]`   | 0.90 (5%) :white_check_mark: | 0.87 (1%) :white_check_mark: |
| `["splitby", "count", "reduce"]`                    | 0.94 (5%) :white_check_mark: | 0.97 (1%) :white_check_mark: |
| `["words", "nthreads=1"]`                           | 0.90 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["words", "nthreads=2"]`                           | 0.94 (5%) :white_check_mark: |                   1.00 (1%)  |

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
Julia Version 1.7.1
Commit ac5cc99908 (2021-12-22 19:35 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 20.04.3 LTS
  uname: Linux 5.11.0-1027-azure #30~20.04.1-Ubuntu SMP Wed Jan 12 20:56:50 UTC 2022 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz       5435 s          1 s        262 s       1611 s          0 s
       #2  2095 MHz       5280 s          1 s        263 s       1782 s          0 s
       
  Memory: 6.788978576660156 GB (3422.89453125 MB free)
  Uptime: 738.36 sec
  Load Avg:  1.69  1.52  0.91
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, skylake-avx512)
```

### Baseline
```
Julia Version 1.7.1
Commit ac5cc99908 (2021-12-22 19:35 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 20.04.3 LTS
  uname: Linux 5.11.0-1027-azure #30~20.04.1-Ubuntu SMP Wed Jan 12 20:56:50 UTC 2022 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz       8343 s          1 s        303 s       1764 s          0 s
       #2  2095 MHz       7103 s          1 s        307 s       3010 s          0 s
       
  Memory: 6.788978576660156 GB (3416.8359375 MB free)
  Uptime: 1048.73 sec
  Load Avg:  1.65  1.56  1.1
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, skylake-avx512)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 2 Feb 2022 - 4:41
* Package commit: 0b0693
* Julia commit: ac5cc9
* Julia command flags: None
* Environment variables: `JULIA_NUM_THREADS => 2`

## Results
Below is a table of this job's results, obtained by running the benchmarks.
The values listed in the `ID` column have the structure `[parent_group, child_group, ..., key]`, and can be used to
index into the BaseBenchmarks suite to retrieve the corresponding benchmarks.
The percentages accompanying time and memory values in the below table are noise tolerances. The "true"
time/memory value for a given benchmark is expected to fall within this percentage of the reported value.
An empty cell means that the value was zero.

| ID                                                  | time            | GC time | memory           | allocations |
|-----------------------------------------------------|----------------:|--------:|-----------------:|------------:|
| `["collect", "assoc", "basesize=1"]`                | 288.587 ms (5%) |         |   25.97 MiB (1%) |      306825 |
| `["collect", "assoc", "basesize=1024"]`             | 240.833 ms (5%) |         |    2.61 MiB (1%) |         456 |
| `["collect", "assoc", "basesize=32"]`               | 243.467 ms (5%) |         |    4.82 MiB (1%) |       11720 |
| `["collect", "seq"]`                                | 457.673 ms (5%) |         |  812.73 KiB (1%) |          11 |
| `["collect", "unordered", "basesize=1"]`            | 403.241 ms (5%) |         |   23.86 MiB (1%) |      411609 |
| `["collect", "unordered", "basesize=1024"]`         | 256.902 ms (5%) |         | 1003.33 KiB (1%) |         989 |
| `["collect", "unordered", "basesize=32"]`           | 265.950 ms (5%) |         |    1.58 MiB (1%) |       14648 |
| `["findfirst", "n=1000", "foldl"]`                  | 729.937 ms (5%) |         |                  |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 415.064 ms (5%) |         |  231.33 KiB (1%) |        3256 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 490.701 ms (5%) |         |  144.12 KiB (1%) |        2027 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 604.755 ms (5%) |         |   99.20 KiB (1%) |        1382 |
| `["findfirst", "n=400", "foldl"]`                   | 555.689 ms (5%) |         |                  |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 313.530 ms (5%) |         |  413.47 KiB (1%) |        5855 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 300.671 ms (5%) |         |  199.00 KiB (1%) |        2863 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 458.215 ms (5%) |         |  153.27 KiB (1%) |        2198 |
| `["findfirst", "n=500", "foldl"]`                   |  94.668 ms (5%) |         |                  |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 199.541 ms (5%) |         |  229.77 KiB (1%) |        3199 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 163.899 ms (5%) |         |  115.39 KiB (1%) |        1575 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 128.038 ms (5%) |         |   60.59 KiB (1%) |         824 |
| `["overhead", "default"]`                           |  81.202 μs (5%) |         |   32.73 KiB (1%) |         418 |
| `["overhead", "stoppable=false"]`                   |  83.102 μs (5%) |         |   32.72 KiB (1%) |         417 |
| `["overhead", "stoppable=true"]`                    |  94.802 μs (5%) |         |   44.22 KiB (1%) |         609 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   3.630 ms (5%) |         |  728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   4.434 ms (5%) |         |    1.79 MiB (1%) |         216 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   4.076 ms (5%) |         |    1.42 MiB (1%) |         118 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  20.809 ms (5%) |         |    1.58 MiB (1%) |        2324 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  29.041 ms (5%) |         |    1.26 MiB (1%) |        7504 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  23.668 ms (5%) |         |    1.16 MiB (1%) |        4238 |
| `["parallel_histogram", "seq"]`                     |   6.471 ms (5%) |         |  364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  40.360 ms (5%) |         |                  |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  20.402 ms (5%) |         |   736 bytes (1%) |          11 |
| `["splitby", "count", "foldl"]`                     |   2.524 ms (5%) |         |                  |             |
| `["splitby", "count", "man"]`                       |   1.575 ms (5%) |         |                  |             |
| `["splitby", "count", "reduce"]`                    |   1.205 ms (5%) |         |    1.06 KiB (1%) |          18 |
| `["sum", "random", "foldl"]`                        |  18.350 ms (5%) |         |                  |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   9.347 ms (5%) |         |   74.17 KiB (1%) |        1104 |
| `["sum", "random", "reduce", "basesize=256"]`       |   9.276 ms (5%) |         |   36.70 KiB (1%) |         545 |
| `["sum", "random", "reduce", "basesize=512"]`       |   9.203 ms (5%) |         |   18.11 KiB (1%) |         270 |
| `["sum", "uniform", "foldl"]`                       |  17.929 ms (5%) |         |                  |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   9.226 ms (5%) |         |   74.20 KiB (1%) |        1105 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   9.024 ms (5%) |         |   36.67 KiB (1%) |         544 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   8.970 ms (5%) |         |   18.06 KiB (1%) |         269 |
| `["sum", "valley", "foldl"]`                        |  18.584 ms (5%) |         |                  |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   9.533 ms (5%) |         |   74.14 KiB (1%) |        1103 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   9.392 ms (5%) |         |   36.73 KiB (1%) |         546 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   9.775 ms (5%) |         |   18.03 KiB (1%) |         268 |
| `["words", "nthreads=1"]`                           |  25.529 ms (5%) |         |   31.64 MiB (1%) |     1030823 |
| `["words", "nthreads=2"]`                           |  16.762 ms (5%) |         |   32.36 MiB (1%) |     1030950 |
| `["words", "nthreads=4"]`                           |  17.493 ms (5%) |         |   32.98 MiB (1%) |     1031081 |

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
Julia Version 1.7.1
Commit ac5cc99908 (2021-12-22 19:35 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 20.04.3 LTS
  uname: Linux 5.11.0-1027-azure #30~20.04.1-Ubuntu SMP Wed Jan 12 20:56:50 UTC 2022 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz       5435 s          1 s        262 s       1611 s          0 s
       #2  2095 MHz       5280 s          1 s        263 s       1782 s          0 s
       
  Memory: 6.788978576660156 GB (3422.89453125 MB free)
  Uptime: 738.36 sec
  Load Avg:  1.69  1.52  0.91
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, skylake-avx512)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 2 Feb 2022 - 4:46
* Package commit: 332ac4
* Julia commit: ac5cc9
* Julia command flags: None
* Environment variables: `JULIA_NUM_THREADS => 2`

## Results
Below is a table of this job's results, obtained by running the benchmarks.
The values listed in the `ID` column have the structure `[parent_group, child_group, ..., key]`, and can be used to
index into the BaseBenchmarks suite to retrieve the corresponding benchmarks.
The percentages accompanying time and memory values in the below table are noise tolerances. The "true"
time/memory value for a given benchmark is expected to fall within this percentage of the reported value.
An empty cell means that the value was zero.

| ID                                                  | time            | GC time | memory           | allocations |
|-----------------------------------------------------|----------------:|--------:|-----------------:|------------:|
| `["collect", "assoc", "basesize=1"]`                | 302.781 ms (5%) |         |   25.97 MiB (1%) |      306800 |
| `["collect", "assoc", "basesize=1024"]`             | 243.292 ms (5%) |         |    2.61 MiB (1%) |         456 |
| `["collect", "assoc", "basesize=32"]`               | 240.883 ms (5%) |         |    4.82 MiB (1%) |       11716 |
| `["collect", "seq"]`                                | 465.938 ms (5%) |         |  812.73 KiB (1%) |          11 |
| `["collect", "unordered", "basesize=1"]`            | 418.252 ms (5%) |         |   23.86 MiB (1%) |      411692 |
| `["collect", "unordered", "basesize=1024"]`         | 257.925 ms (5%) |         | 1003.45 KiB (1%) |        1044 |
| `["collect", "unordered", "basesize=32"]`           | 266.377 ms (5%) |         |    1.58 MiB (1%) |       14765 |
| `["findfirst", "n=1000", "foldl"]`                  | 721.954 ms (5%) |         |                  |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 407.291 ms (5%) |         |  230.58 KiB (1%) |        3248 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 625.730 ms (5%) |         |  183.22 KiB (1%) |        2561 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 658.829 ms (5%) |         |  108.55 KiB (1%) |        1509 |
| `["findfirst", "n=400", "foldl"]`                   | 545.315 ms (5%) |         |                  |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 308.210 ms (5%) |         |  412.70 KiB (1%) |        5847 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 292.727 ms (5%) |         |  200.64 KiB (1%) |        2866 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 359.412 ms (5%) |         |  125.59 KiB (1%) |        1792 |
| `["findfirst", "n=500", "foldl"]`                   |  93.982 ms (5%) |         |                  |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 219.513 ms (5%) |         |  264.39 KiB (1%) |        3638 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 193.748 ms (5%) |         |  121.30 KiB (1%) |        1670 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 131.801 ms (5%) |         |   56.84 KiB (1%) |         779 |
| `["overhead", "default"]`                           |  83.302 μs (5%) |         |   32.70 KiB (1%) |         417 |
| `["overhead", "stoppable=false"]`                   |  82.802 μs (5%) |         |   32.72 KiB (1%) |         417 |
| `["overhead", "stoppable=true"]`                    |  93.802 μs (5%) |         |   44.25 KiB (1%) |         610 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   3.611 ms (5%) |         |  728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   4.539 ms (5%) |         |    1.79 MiB (1%) |         215 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   4.029 ms (5%) |         |    1.42 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  18.439 ms (5%) |         |    1.58 MiB (1%) |        2361 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  28.778 ms (5%) |         |    1.24 MiB (1%) |        6886 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  26.370 ms (5%) |         |    1.33 MiB (1%) |        5795 |
| `["parallel_histogram", "seq"]`                     |   6.475 ms (5%) |         |  364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  40.239 ms (5%) |         |                  |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  20.977 ms (5%) |         |   736 bytes (1%) |          11 |
| `["splitby", "count", "foldl"]`                     |   2.435 ms (5%) |         |                  |             |
| `["splitby", "count", "man"]`                       |   1.579 ms (5%) |         |                  |             |
| `["splitby", "count", "reduce"]`                    |   1.281 ms (5%) |         |    1.09 KiB (1%) |          19 |
| `["sum", "random", "foldl"]`                        |  18.672 ms (5%) |         |                  |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   9.619 ms (5%) |         |   74.14 KiB (1%) |        1103 |
| `["sum", "random", "reduce", "basesize=256"]`       |   9.309 ms (5%) |         |   36.70 KiB (1%) |         545 |
| `["sum", "random", "reduce", "basesize=512"]`       |   9.294 ms (5%) |         |   18.11 KiB (1%) |         270 |
| `["sum", "uniform", "foldl"]`                       |  18.302 ms (5%) |         |                  |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   9.248 ms (5%) |         |   74.05 KiB (1%) |        1100 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   9.192 ms (5%) |         |   36.77 KiB (1%) |         547 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   9.077 ms (5%) |         |   18.06 KiB (1%) |         269 |
| `["sum", "valley", "foldl"]`                        |  18.508 ms (5%) |         |                  |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   9.550 ms (5%) |         |   74.17 KiB (1%) |        1104 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   9.339 ms (5%) |         |   36.73 KiB (1%) |         546 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   9.431 ms (5%) |         |   18.03 KiB (1%) |         268 |
| `["words", "nthreads=1"]`                           |  28.454 ms (5%) |         |   31.52 MiB (1%) |     1026879 |
| `["words", "nthreads=2"]`                           |  17.782 ms (5%) |         |   32.23 MiB (1%) |     1026962 |
| `["words", "nthreads=4"]`                           |  18.409 ms (5%) |         |   32.86 MiB (1%) |     1027130 |

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
Julia Version 1.7.1
Commit ac5cc99908 (2021-12-22 19:35 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 20.04.3 LTS
  uname: Linux 5.11.0-1027-azure #30~20.04.1-Ubuntu SMP Wed Jan 12 20:56:50 UTC 2022 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz       8343 s          1 s        303 s       1764 s          0 s
       #2  2095 MHz       7103 s          1 s        307 s       3010 s          0 s
       
  Memory: 6.788978576660156 GB (3416.8359375 MB free)
  Uptime: 1048.73 sec
  Load Avg:  1.65  1.56  1.1
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
    CPU MHz:                         2095.078
    BogoMIPS:                        4190.15
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
    Vulnerability Spec store bypass: Vulnerable
    Vulnerability Spectre v1:        Mitigation; usercopy/swapgs barriers and __user pointer sanitization
    Vulnerability Spectre v2:        Mitigation; Full generic retpoline, STIBP disabled, RSB filling
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

