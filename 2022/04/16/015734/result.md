# Multi-thread benchmark result

* Pull request commit: [`cc3273e747921b64cb9dc6a4793cee2855147feb`](https://github.com/JuliaFolds/Transducers.jl/commit/cc3273e747921b64cb9dc6a4793cee2855147feb)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/243> (Update */Manifest.toml)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 16 Apr 2022 - 01:51
    - Baseline: 16 Apr 2022 - 01:57
* Package commits:
    - Target: ca452c
    - Baseline: 6125fe
* Julia commits:
    - Target: bf5349
    - Baseline: bf5349
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
| `["findfirst", "n=1000", "reduce", "basesize=256"]` |                1.35 (5%) :x: |                1.22 (1%) :x: |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` |                   1.02 (5%)  | 0.95 (1%) :white_check_mark: |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 0.94 (5%) :white_check_mark: | 0.94 (1%) :white_check_mark: |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 0.87 (5%) :white_check_mark: | 0.91 (1%) :white_check_mark: |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 0.67 (5%) :white_check_mark: | 0.76 (1%) :white_check_mark: |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 0.80 (5%) :white_check_mark: | 0.77 (1%) :white_check_mark: |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 0.71 (5%) :white_check_mark: | 0.80 (1%) :white_check_mark: |
| `["parallel_histogram", "comm", "basesize=16384"]`  |                1.19 (5%) :x: |                1.27 (1%) :x: |
| `["parallel_histogram", "comm", "basesize=4096"]`   |                1.07 (5%) :x: |                1.05 (1%) :x: |
| `["parallel_histogram", "comm", "basesize=8192"]`   |                   0.98 (5%)  | 0.76 (1%) :white_check_mark: |
| `["splitby", "count", "foldl"]`                     | 0.89 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["splitby", "count", "man"]`                       |                1.14 (5%) :x: |                   1.00 (1%)  |

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
Julia Version 1.7.2
Commit bf53498635 (2022-02-06 15:21 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 20.04.4 LTS
  uname: Linux 5.13.0-1021-azure #24~20.04.1-Ubuntu SMP Tue Mar 29 15:34:22 UTC 2022 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz       5516 s          1 s        251 s       1461 s          0 s
       #2  2095 MHz       5178 s          1 s        241 s       1823 s          0 s
       
  Memory: 6.783611297607422 GB (3523.4921875 MB free)
  Uptime: 729.3 sec
  Load Avg:  1.67  1.54  0.96
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, skylake-avx512)
```

### Baseline
```
Julia Version 1.7.2
Commit bf53498635 (2022-02-06 15:21 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 20.04.4 LTS
  uname: Linux 5.13.0-1021-azure #24~20.04.1-Ubuntu SMP Tue Mar 29 15:34:22 UTC 2022 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz       7619 s          1 s        337 s       2537 s          0 s
       #2  2095 MHz       8010 s          1 s        317 s       2186 s          0 s
       
  Memory: 6.783611297607422 GB (3255.3515625 MB free)
  Uptime: 1056.72 sec
  Load Avg:  1.55  1.57  1.15
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, skylake-avx512)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 16 Apr 2022 - 1:51
* Package commit: ca452c
* Julia commit: bf5349
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
| `["collect", "assoc", "basesize=1"]`                | 291.171 ms (5%) |         |   25.97 MiB (1%) |      306818 |
| `["collect", "assoc", "basesize=1024"]`             | 234.433 ms (5%) |         |    2.61 MiB (1%) |         455 |
| `["collect", "assoc", "basesize=32"]`               | 239.773 ms (5%) |         |    4.82 MiB (1%) |       11700 |
| `["collect", "seq"]`                                | 464.042 ms (5%) |         |  812.73 KiB (1%) |          11 |
| `["collect", "unordered", "basesize=1"]`            | 407.650 ms (5%) |         |   23.89 MiB (1%) |      412549 |
| `["collect", "unordered", "basesize=1024"]`         | 251.194 ms (5%) |         | 1004.42 KiB (1%) |        1026 |
| `["collect", "unordered", "basesize=32"]`           | 263.949 ms (5%) |         |    1.58 MiB (1%) |       14698 |
| `["findfirst", "n=1000", "foldl"]`                  | 733.700 ms (5%) |         |                  |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 409.246 ms (5%) |         |  232.89 KiB (1%) |        3277 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 676.604 ms (5%) |         |  191.11 KiB (1%) |        2694 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 686.163 ms (5%) |         |  103.53 KiB (1%) |        1454 |
| `["findfirst", "n=400", "foldl"]`                   | 561.128 ms (5%) |         |                  |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 295.350 ms (5%) |         |  383.20 KiB (1%) |        5459 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 298.049 ms (5%) |         |  202.56 KiB (1%) |        2901 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 394.884 ms (5%) |         |  139.36 KiB (1%) |        1986 |
| `["findfirst", "n=500", "foldl"]`                   |  93.906 ms (5%) |         |                  |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 189.404 ms (5%) |         |  234.36 KiB (1%) |        3228 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |  87.146 ms (5%) |         |   74.39 KiB (1%) |        1005 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  97.758 ms (5%) |         |   50.72 KiB (1%) |         677 |
| `["overhead", "default"]`                           |  83.301 μs (5%) |         |   32.77 KiB (1%) |         419 |
| `["overhead", "stoppable=false"]`                   |  84.901 μs (5%) |         |   32.75 KiB (1%) |         418 |
| `["overhead", "stoppable=true"]`                    |  96.302 μs (5%) |         |   44.25 KiB (1%) |         610 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   3.597 ms (5%) |         |  728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   4.330 ms (5%) |         |    1.79 MiB (1%) |         215 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   4.000 ms (5%) |         |    1.42 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  21.085 ms (5%) |         |    1.59 MiB (1%) |        2797 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  28.456 ms (5%) |         |    1.26 MiB (1%) |        7541 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  25.238 ms (5%) |         |    1.28 MiB (1%) |        5850 |
| `["parallel_histogram", "seq"]`                     |   6.471 ms (5%) |         |  364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  41.491 ms (5%) |         |                  |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  20.967 ms (5%) |         |   736 bytes (1%) |          11 |
| `["splitby", "count", "foldl"]`                     |   2.110 ms (5%) |         |                  |             |
| `["splitby", "count", "man"]`                       |   1.568 ms (5%) |         |                  |             |
| `["splitby", "count", "reduce"]`                    |   1.158 ms (5%) |         |    1.09 KiB (1%) |          19 |
| `["sum", "random", "foldl"]`                        |  18.671 ms (5%) |         |                  |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   9.409 ms (5%) |         |   74.08 KiB (1%) |        1101 |
| `["sum", "random", "reduce", "basesize=256"]`       |   9.141 ms (5%) |         |   36.73 KiB (1%) |         546 |
| `["sum", "random", "reduce", "basesize=512"]`       |   8.973 ms (5%) |         |   18.08 KiB (1%) |         269 |
| `["sum", "uniform", "foldl"]`                       |  18.192 ms (5%) |         |                  |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   9.007 ms (5%) |         |   74.05 KiB (1%) |        1100 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   9.214 ms (5%) |         |   36.73 KiB (1%) |         546 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   8.779 ms (5%) |         |   18.00 KiB (1%) |         267 |
| `["sum", "valley", "foldl"]`                        |  18.277 ms (5%) |         |                  |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   9.347 ms (5%) |         |   74.11 KiB (1%) |        1102 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   9.216 ms (5%) |         |   36.73 KiB (1%) |         546 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   9.347 ms (5%) |         |   18.03 KiB (1%) |         268 |
| `["words", "nthreads=1"]`                           |  26.034 ms (5%) |         |   31.52 MiB (1%) |     1025917 |
| `["words", "nthreads=2"]`                           |  16.464 ms (5%) |         |   32.23 MiB (1%) |     1025992 |
| `["words", "nthreads=4"]`                           |  17.387 ms (5%) |         |   32.86 MiB (1%) |     1026172 |

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
Julia Version 1.7.2
Commit bf53498635 (2022-02-06 15:21 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 20.04.4 LTS
  uname: Linux 5.13.0-1021-azure #24~20.04.1-Ubuntu SMP Tue Mar 29 15:34:22 UTC 2022 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz       5516 s          1 s        251 s       1461 s          0 s
       #2  2095 MHz       5178 s          1 s        241 s       1823 s          0 s
       
  Memory: 6.783611297607422 GB (3523.4921875 MB free)
  Uptime: 729.3 sec
  Load Avg:  1.67  1.54  0.96
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, skylake-avx512)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 16 Apr 2022 - 1:57
* Package commit: 6125fe
* Julia commit: bf5349
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
| `["collect", "assoc", "basesize=1"]`                | 292.360 ms (5%) |         |   25.97 MiB (1%) |      306804 |
| `["collect", "assoc", "basesize=1024"]`             | 235.968 ms (5%) |         |    2.61 MiB (1%) |         455 |
| `["collect", "assoc", "basesize=32"]`               | 237.178 ms (5%) |         |    4.82 MiB (1%) |       11711 |
| `["collect", "seq"]`                                | 461.458 ms (5%) |         |  812.73 KiB (1%) |          11 |
| `["collect", "unordered", "basesize=1"]`            | 412.591 ms (5%) |         |   23.83 MiB (1%) |      410628 |
| `["collect", "unordered", "basesize=1024"]`         | 254.105 ms (5%) |         | 1005.33 KiB (1%) |        1094 |
| `["collect", "unordered", "basesize=32"]`           | 264.421 ms (5%) |         |    1.58 MiB (1%) |       14750 |
| `["findfirst", "n=1000", "foldl"]`                  | 745.551 ms (5%) |         |                  |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 412.700 ms (5%) |         |  230.61 KiB (1%) |        3249 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 500.833 ms (5%) |         |  157.20 KiB (1%) |        2193 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 674.273 ms (5%) |         |  108.55 KiB (1%) |        1509 |
| `["findfirst", "n=400", "foldl"]`                   | 555.313 ms (5%) |         |                  |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 314.680 ms (5%) |         |  409.31 KiB (1%) |        5821 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 297.814 ms (5%) |         |  200.92 KiB (1%) |        2875 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 455.108 ms (5%) |         |  153.11 KiB (1%) |        2193 |
| `["findfirst", "n=500", "foldl"]`                   |  94.056 ms (5%) |         |                  |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 284.454 ms (5%) |         |  307.67 KiB (1%) |        4324 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 109.285 ms (5%) |         |   96.39 KiB (1%) |        1296 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 138.559 ms (5%) |         |   63.66 KiB (1%) |         865 |
| `["overhead", "default"]`                           |  87.001 μs (5%) |         |   32.77 KiB (1%) |         419 |
| `["overhead", "stoppable=false"]`                   |  83.102 μs (5%) |         |   32.75 KiB (1%) |         418 |
| `["overhead", "stoppable=true"]`                    |  99.102 μs (5%) |         |   44.28 KiB (1%) |         611 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   3.624 ms (5%) |         |  728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   4.470 ms (5%) |         |    1.79 MiB (1%) |         215 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   4.074 ms (5%) |         |    1.42 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  17.790 ms (5%) |         |    1.26 MiB (1%) |         557 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  26.703 ms (5%) |         |    1.21 MiB (1%) |        5683 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  25.833 ms (5%) |         |    1.69 MiB (1%) |        6032 |
| `["parallel_histogram", "seq"]`                     |   6.191 ms (5%) |         |  364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  40.005 ms (5%) |         |                  |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  20.127 ms (5%) |         |   736 bytes (1%) |          11 |
| `["splitby", "count", "foldl"]`                     |   2.380 ms (5%) |         |                  |             |
| `["splitby", "count", "man"]`                       |   1.378 ms (5%) |         |                  |             |
| `["splitby", "count", "reduce"]`                    |   1.213 ms (5%) |         |    1.09 KiB (1%) |          19 |
| `["sum", "random", "foldl"]`                        |  18.968 ms (5%) |         |                  |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   9.420 ms (5%) |         |   74.17 KiB (1%) |        1104 |
| `["sum", "random", "reduce", "basesize=256"]`       |   9.175 ms (5%) |         |   36.70 KiB (1%) |         545 |
| `["sum", "random", "reduce", "basesize=512"]`       |   9.260 ms (5%) |         |   18.11 KiB (1%) |         270 |
| `["sum", "uniform", "foldl"]`                       |  18.464 ms (5%) |         |                  |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   9.102 ms (5%) |         |   74.23 KiB (1%) |        1106 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   9.016 ms (5%) |         |   36.77 KiB (1%) |         547 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   8.864 ms (5%) |         |   18.00 KiB (1%) |         267 |
| `["sum", "valley", "foldl"]`                        |  18.042 ms (5%) |         |                  |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   9.356 ms (5%) |         |   74.05 KiB (1%) |        1100 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   9.381 ms (5%) |         |   36.77 KiB (1%) |         547 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   9.272 ms (5%) |         |   18.06 KiB (1%) |         269 |
| `["words", "nthreads=1"]`                           |  27.227 ms (5%) |         |   31.66 MiB (1%) |     1031492 |
| `["words", "nthreads=2"]`                           |  17.031 ms (5%) |         |   32.02 MiB (1%) |     1031537 |
| `["words", "nthreads=4"]`                           |  17.824 ms (5%) |         |   32.73 MiB (1%) |     1031610 |

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
Julia Version 1.7.2
Commit bf53498635 (2022-02-06 15:21 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 20.04.4 LTS
  uname: Linux 5.13.0-1021-azure #24~20.04.1-Ubuntu SMP Tue Mar 29 15:34:22 UTC 2022 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz       7619 s          1 s        337 s       2537 s          0 s
       #2  2095 MHz       8010 s          1 s        317 s       2186 s          0 s
       
  Memory: 6.783611297607422 GB (3255.3515625 MB free)
  Uptime: 1056.72 sec
  Load Avg:  1.55  1.57  1.15
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
    CPU MHz:                         2095.076
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

