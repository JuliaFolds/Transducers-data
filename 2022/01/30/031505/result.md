# Multi-thread benchmark result

* Pull request commit: [`a2aeaccd14148164272c29c3511a568669025e95`](https://github.com/JuliaFolds/Transducers.jl/commit/a2aeaccd14148164272c29c3511a568669025e95)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/509> (Add `completebasecase` protocol)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 30 Jan 2022 - 03:09
    - Baseline: 30 Jan 2022 - 03:14
* Package commits:
    - Target: 1bb228
    - Baseline: 354150
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
| `["collect", "assoc", "basesize=1"]`                |                1.07 (5%) :x: |                   1.00 (1%)  |
| `["collect", "assoc", "basesize=1024"]`             |                1.07 (5%) :x: |                   1.00 (1%)  |
| `["collect", "assoc", "basesize=32"]`               |                1.07 (5%) :x: |                   1.00 (1%)  |
| `["collect", "unordered", "basesize=1"]`            |                   1.01 (5%)  | 0.98 (1%) :white_check_mark: |
| `["collect", "unordered", "basesize=1024"]`         |                1.07 (5%) :x: |                1.02 (1%) :x: |
| `["collect", "unordered", "basesize=32"]`           |                1.07 (5%) :x: |                   0.99 (1%)  |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` |                1.12 (5%) :x: |                1.04 (1%) :x: |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  |                   1.03 (5%)  |                1.05 (1%) :x: |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  |                1.26 (5%) :x: |                1.30 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 0.92 (5%) :white_check_mark: | 0.97 (1%) :white_check_mark: |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 0.66 (5%) :white_check_mark: | 0.70 (1%) :white_check_mark: |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |                1.15 (5%) :x: |                1.10 (1%) :x: |
| `["overhead", "default"]`                           |                1.09 (5%) :x: |                   1.00 (1%)  |
| `["overhead", "stoppable=false"]`                   |                1.07 (5%) :x: |                   1.00 (1%)  |
| `["parallel_histogram", "comm", "basesize=16384"]`  |                   1.04 (5%)  | 0.98 (1%) :white_check_mark: |
| `["parallel_histogram", "comm", "basesize=4096"]`   |                1.07 (5%) :x: |                   0.99 (1%)  |
| `["parallel_histogram", "comm", "basesize=8192"]`   |                   1.03 (5%)  |                1.02 (1%) :x: |

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
  CPU: Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2593 MHz       5115 s          1 s        254 s       3808 s          0 s
       #2  2593 MHz       5310 s          2 s        277 s       3587 s          0 s
       
  Memory: 6.788978576660156 GB (3391.93359375 MB free)
  Uptime: 923.2 sec
  Load Avg:  1.74  1.51  0.92
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
  CPU: Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2593 MHz       7550 s          1 s        291 s       4331 s          0 s
       #2  2593 MHz       7480 s          2 s        321 s       4374 s          0 s
       
  Memory: 6.788978576660156 GB (3424.01171875 MB free)
  Uptime: 1223.76 sec
  Load Avg:  1.58  1.55  1.1
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, skylake-avx512)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 30 Jan 2022 - 3:9
* Package commit: 1bb228
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

| ID                                                  | time            | GC time  | memory          | allocations |
|-----------------------------------------------------|----------------:|---------:|----------------:|------------:|
| `["collect", "assoc", "basesize=1"]`                | 245.386 ms (5%) |          |  25.97 MiB (1%) |      306872 |
| `["collect", "assoc", "basesize=1024"]`             | 198.566 ms (5%) |          |   2.61 MiB (1%) |         455 |
| `["collect", "assoc", "basesize=32"]`               | 200.600 ms (5%) |          |   4.82 MiB (1%) |       11707 |
| `["collect", "seq"]`                                | 395.502 ms (5%) |          | 812.73 KiB (1%) |          11 |
| `["collect", "unordered", "basesize=1"]`            | 348.355 ms (5%) |          |  23.61 MiB (1%) |      403347 |
| `["collect", "unordered", "basesize=1024"]`         | 213.501 ms (5%) |          |   1.01 MiB (1%) |         939 |
| `["collect", "unordered", "basesize=32"]`           | 225.163 ms (5%) |          |   1.58 MiB (1%) |       14687 |
| `["findfirst", "n=1000", "foldl"]`                  | 629.952 ms (5%) |          |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 347.314 ms (5%) |          | 230.58 KiB (1%) |        3248 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 431.962 ms (5%) |          | 157.08 KiB (1%) |        2189 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 565.576 ms (5%) |          | 103.53 KiB (1%) |        1454 |
| `["findfirst", "n=400", "foldl"]`                   | 472.553 ms (5%) |          |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 247.239 ms (5%) |          | 387.25 KiB (1%) |        5511 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 249.258 ms (5%) |          | 200.67 KiB (1%) |        2867 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 346.503 ms (5%) |          | 146.16 KiB (1%) |        2075 |
| `["findfirst", "n=500", "foldl"]`                   |  81.945 ms (5%) |          |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 118.318 ms (5%) |          | 178.66 KiB (1%) |        2464 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |  79.317 ms (5%) |          |  79.38 KiB (1%) |        1083 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 100.650 ms (5%) |          |  54.47 KiB (1%) |         747 |
| `["overhead", "default"]`                           |  75.100 μs (5%) |          |  32.70 KiB (1%) |         417 |
| `["overhead", "stoppable=false"]`                   |  75.601 μs (5%) |          |  32.72 KiB (1%) |         417 |
| `["overhead", "stoppable=true"]`                    |  83.401 μs (5%) |          |  44.25 KiB (1%) |         610 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   3.245 ms (5%) |          | 728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   3.863 ms (5%) |          |   1.79 MiB (1%) |         215 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   3.578 ms (5%) |          |   1.42 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  17.000 ms (5%) | 2.080 ms |   1.53 MiB (1%) |         722 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  25.440 ms (5%) |          |   1.22 MiB (1%) |        6111 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  22.920 ms (5%) |          |   1.68 MiB (1%) |        5665 |
| `["parallel_histogram", "seq"]`                     |   5.748 ms (5%) |          | 364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  35.190 ms (5%) |          |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  17.579 ms (5%) |          |  704 bytes (1%) |          10 |
| `["splitby", "count", "foldl"]`                     |   2.288 ms (5%) |          |                 |             |
| `["splitby", "count", "man"]`                       |   1.752 ms (5%) |          |                 |             |
| `["splitby", "count", "reduce"]`                    |   1.087 ms (5%) |          |   1.06 KiB (1%) |          18 |
| `["sum", "random", "foldl"]`                        |  16.311 ms (5%) |          |                 |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   8.234 ms (5%) |          |  74.20 KiB (1%) |        1105 |
| `["sum", "random", "reduce", "basesize=256"]`       |   8.119 ms (5%) |          |  36.77 KiB (1%) |         547 |
| `["sum", "random", "reduce", "basesize=512"]`       |   8.066 ms (5%) |          |  18.11 KiB (1%) |         270 |
| `["sum", "uniform", "foldl"]`                       |  15.727 ms (5%) |          |                 |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   7.981 ms (5%) |          |  73.92 KiB (1%) |        1096 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   7.885 ms (5%) |          |  36.77 KiB (1%) |         547 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   7.838 ms (5%) |          |  18.03 KiB (1%) |         268 |
| `["sum", "valley", "foldl"]`                        |  16.144 ms (5%) |          |                 |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   8.236 ms (5%) |          |  74.11 KiB (1%) |        1102 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   8.162 ms (5%) |          |  36.73 KiB (1%) |         546 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   8.106 ms (5%) |          |  18.03 KiB (1%) |         268 |
| `["words", "nthreads=1"]`                           |  22.641 ms (5%) |          |  31.72 MiB (1%) |     1033333 |
| `["words", "nthreads=2"]`                           |  14.470 ms (5%) |          |  32.43 MiB (1%) |     1033406 |
| `["words", "nthreads=4"]`                           |  14.993 ms (5%) |          |  33.06 MiB (1%) |     1033538 |

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
  CPU: Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2593 MHz       5115 s          1 s        254 s       3808 s          0 s
       #2  2593 MHz       5310 s          2 s        277 s       3587 s          0 s
       
  Memory: 6.788978576660156 GB (3391.93359375 MB free)
  Uptime: 923.2 sec
  Load Avg:  1.74  1.51  0.92
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, skylake-avx512)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 30 Jan 2022 - 3:14
* Package commit: 354150
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
| `["collect", "assoc", "basesize=1"]`                | 229.535 ms (5%) |         |   25.97 MiB (1%) |      306743 |
| `["collect", "assoc", "basesize=1024"]`             | 186.133 ms (5%) |         |    2.61 MiB (1%) |         457 |
| `["collect", "assoc", "basesize=32"]`               | 187.759 ms (5%) |         |    4.82 MiB (1%) |       11709 |
| `["collect", "seq"]`                                | 395.105 ms (5%) |         |  812.73 KiB (1%) |          11 |
| `["collect", "unordered", "basesize=1"]`            | 345.615 ms (5%) |         |   24.07 MiB (1%) |      418614 |
| `["collect", "unordered", "basesize=1024"]`         | 199.338 ms (5%) |         | 1007.61 KiB (1%) |        1258 |
| `["collect", "unordered", "basesize=32"]`           | 210.342 ms (5%) |         |    1.60 MiB (1%) |       15187 |
| `["findfirst", "n=1000", "foldl"]`                  | 624.347 ms (5%) |         |                  |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 341.761 ms (5%) |         |  232.75 KiB (1%) |        3272 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 420.969 ms (5%) |         |  157.20 KiB (1%) |        2193 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 502.994 ms (5%) |         |   99.31 KiB (1%) |        1385 |
| `["findfirst", "n=400", "foldl"]`                   | 468.591 ms (5%) |         |                  |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 239.642 ms (5%) |         |  370.55 KiB (1%) |        5294 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 246.519 ms (5%) |         |  200.86 KiB (1%) |        2873 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 274.273 ms (5%) |         |  112.56 KiB (1%) |        1621 |
| `["findfirst", "n=500", "foldl"]`                   |  81.221 ms (5%) |         |                  |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 128.861 ms (5%) |         |  184.84 KiB (1%) |        2542 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 120.947 ms (5%) |         |  112.75 KiB (1%) |        1534 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  87.375 ms (5%) |         |   49.50 KiB (1%) |         667 |
| `["overhead", "default"]`                           |  69.201 μs (5%) |         |   32.73 KiB (1%) |         418 |
| `["overhead", "stoppable=false"]`                   |  70.400 μs (5%) |         |   32.69 KiB (1%) |         416 |
| `["overhead", "stoppable=true"]`                    |  79.900 μs (5%) |         |   44.25 KiB (1%) |         610 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   3.206 ms (5%) |         |  728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   3.711 ms (5%) |         |    1.79 MiB (1%) |         216 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   3.538 ms (5%) |         |    1.42 MiB (1%) |         119 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  16.327 ms (5%) |         |    1.57 MiB (1%) |        1960 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  23.877 ms (5%) |         |    1.23 MiB (1%) |        6471 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  22.209 ms (5%) |         |    1.64 MiB (1%) |        4414 |
| `["parallel_histogram", "seq"]`                     |   5.734 ms (5%) |         |  364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  35.125 ms (5%) |         |                  |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  17.569 ms (5%) |         |   704 bytes (1%) |          10 |
| `["splitby", "count", "foldl"]`                     |   2.290 ms (5%) |         |                  |             |
| `["splitby", "count", "man"]`                       |   1.752 ms (5%) |         |                  |             |
| `["splitby", "count", "reduce"]`                    |   1.142 ms (5%) |         |    1.06 KiB (1%) |          18 |
| `["sum", "random", "foldl"]`                        |  16.257 ms (5%) |         |                  |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   8.145 ms (5%) |         |   74.14 KiB (1%) |        1103 |
| `["sum", "random", "reduce", "basesize=256"]`       |   8.085 ms (5%) |         |   36.77 KiB (1%) |         547 |
| `["sum", "random", "reduce", "basesize=512"]`       |   8.019 ms (5%) |         |   18.11 KiB (1%) |         270 |
| `["sum", "uniform", "foldl"]`                       |  15.741 ms (5%) |         |                  |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   7.958 ms (5%) |         |   74.20 KiB (1%) |        1105 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   7.867 ms (5%) |         |   36.77 KiB (1%) |         547 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   7.829 ms (5%) |         |   18.06 KiB (1%) |         269 |
| `["sum", "valley", "foldl"]`                        |  16.082 ms (5%) |         |                  |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   8.204 ms (5%) |         |   74.14 KiB (1%) |        1103 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   8.099 ms (5%) |         |   36.70 KiB (1%) |         545 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   8.091 ms (5%) |         |   18.06 KiB (1%) |         269 |
| `["words", "nthreads=1"]`                           |  23.439 ms (5%) |         |   31.67 MiB (1%) |     1032337 |
| `["words", "nthreads=2"]`                           |  14.208 ms (5%) |         |   32.39 MiB (1%) |     1032419 |
| `["words", "nthreads=4"]`                           |  15.099 ms (5%) |         |   32.84 MiB (1%) |     1032553 |

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
  CPU: Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2593 MHz       7550 s          1 s        291 s       4331 s          0 s
       #2  2593 MHz       7480 s          2 s        321 s       4374 s          0 s
       
  Memory: 6.788978576660156 GB (3424.01171875 MB free)
  Uptime: 1223.76 sec
  Load Avg:  1.58  1.55  1.1
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
    CPU MHz:                         2593.907
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
    Vulnerability Spec store bypass: Vulnerable
    Vulnerability Spectre v1:        Mitigation; usercopy/swapgs barriers and __user pointer sanitization
    Vulnerability Spectre v2:        Mitigation; Full generic retpoline, STIBP disabled, RSB filling
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

