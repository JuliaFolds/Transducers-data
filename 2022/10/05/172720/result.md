# Multi-thread benchmark result

* Pull request commit: [`a793941741ec5e0255e04ed9ff93737c7bc03001`](https://github.com/JuliaFolds/Transducers.jl/commit/a793941741ec5e0255e04ed9ff93737c7bc03001)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/536> (add delimitedfiles as dependency for 1.9 compat)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 5 Oct 2022 - 17:21
    - Baseline: 5 Oct 2022 - 17:26
* Package commits:
    - Target: d9482b
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
| `["findfirst", "n=1000", "reduce", "basesize=128"]` |                1.39 (5%) :x: |                1.32 (1%) :x: |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` |                1.14 (5%) :x: |                1.05 (1%) :x: |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` |                1.18 (5%) :x: |                1.10 (1%) :x: |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  |                1.14 (5%) :x: |                1.09 (1%) :x: |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  |                1.07 (5%) :x: |                1.04 (1%) :x: |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  |                1.08 (5%) :x: |                1.04 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |                1.42 (5%) :x: |                1.20 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |                2.25 (5%) :x: |                1.54 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 0.55 (5%) :white_check_mark: | 0.59 (1%) :white_check_mark: |
| `["parallel_histogram", "assoc", "basesize=16384"]` | 0.93 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["parallel_histogram", "assoc", "basesize=4096"]`  | 0.91 (5%) :white_check_mark: |                1.15 (1%) :x: |
| `["parallel_histogram", "assoc", "basesize=8192"]`  | 0.88 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["parallel_histogram", "comm", "basesize=16384"]`  | 0.91 (5%) :white_check_mark: | 0.98 (1%) :white_check_mark: |
| `["parallel_histogram", "comm", "basesize=4096"]`   |                   0.96 (5%)  | 0.99 (1%) :white_check_mark: |
| `["parallel_histogram", "comm", "basesize=8192"]`   |                   0.97 (5%)  | 0.77 (1%) :white_check_mark: |
| `["parallel_histogram", "seq"]`                     | 0.91 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["splitby", "count", "foldl"]`                     |                1.06 (5%) :x: |                   1.00 (1%)  |
| `["splitby", "count", "reduce"]`                    |                1.15 (5%) :x: |                   1.00 (1%)  |
| `["sum", "random", "reduce", "basesize=128"]`       |                1.15 (5%) :x: |                   1.00 (1%)  |
| `["sum", "random", "reduce", "basesize=256"]`       |                1.11 (5%) :x: |                   1.00 (1%)  |
| `["sum", "uniform", "reduce", "basesize=128"]`      |                1.09 (5%) :x: |                   1.00 (1%)  |
| `["sum", "uniform", "reduce", "basesize=256"]`      |                1.09 (5%) :x: |                   1.00 (1%)  |
| `["sum", "uniform", "reduce", "basesize=512"]`      |                1.12 (5%) :x: |                   1.00 (1%)  |
| `["sum", "valley", "foldl"]`                        |                1.07 (5%) :x: |                   1.00 (1%)  |
| `["sum", "valley", "reduce", "basesize=128"]`       |                1.09 (5%) :x: |                   1.00 (1%)  |
| `["sum", "valley", "reduce", "basesize=256"]`       |                1.06 (5%) :x: |                   1.00 (1%)  |
| `["sum", "valley", "reduce", "basesize=512"]`       |                1.08 (5%) :x: |                   1.00 (1%)  |
| `["words", "nthreads=1"]`                           | 0.94 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["words", "nthreads=2"]`                           | 0.92 (5%) :white_check_mark: |                   1.00 (1%)  |

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
  uname: Linux 5.15.0-1020-azure #25~20.04.1-Ubuntu SMP Thu Sep 1 19:20:56 UTC 2022 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz       4921 s          0 s        249 s       2753 s          0 s
       #2  2095 MHz       5472 s          0 s        277 s       2180 s          0 s
       
  Memory: 6.781253814697266 GB (3702.3671875 MB free)
  Uptime: 798.22 sec
  Load Avg:  1.72  1.51  0.91
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
      Ubuntu 20.04.5 LTS
  uname: Linux 5.15.0-1020-azure #25~20.04.1-Ubuntu SMP Thu Sep 1 19:20:56 UTC 2022 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz       7789 s          0 s        291 s       2822 s          0 s
       #2  2095 MHz       7233 s          0 s        311 s       3358 s          0 s
       
  Memory: 6.781253814697266 GB (3724.4375 MB free)
  Uptime: 1096.3 sec
  Load Avg:  1.66  1.57  1.1
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, skylake-avx512)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 5 Oct 2022 - 17:21
* Package commit: d9482b
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

| ID                                                  | time            | GC time | memory           | allocations |
|-----------------------------------------------------|----------------:|--------:|-----------------:|------------:|
| `["collect", "assoc", "basesize=1"]`                | 267.312 ms (5%) |         |   25.97 MiB (1%) |      306859 |
| `["collect", "assoc", "basesize=1024"]`             | 215.716 ms (5%) |         |    2.61 MiB (1%) |         455 |
| `["collect", "assoc", "basesize=32"]`               | 218.993 ms (5%) |         |    4.82 MiB (1%) |       11718 |
| `["collect", "seq"]`                                | 420.628 ms (5%) |         |  812.73 KiB (1%) |          11 |
| `["collect", "unordered", "basesize=1"]`            | 384.374 ms (5%) |         |   23.88 MiB (1%) |      412317 |
| `["collect", "unordered", "basesize=1024"]`         | 230.716 ms (5%) |         | 1002.20 KiB (1%) |         904 |
| `["collect", "unordered", "basesize=32"]`           | 244.249 ms (5%) |         |    1.58 MiB (1%) |       14770 |
| `["findfirst", "n=1000", "foldl"]`                  | 671.830 ms (5%) |         |                  |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 530.823 ms (5%) |         |  303.48 KiB (1%) |        4271 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 538.040 ms (5%) |         |  164.36 KiB (1%) |        2314 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 670.555 ms (5%) |         |  108.55 KiB (1%) |        1509 |
| `["findfirst", "n=400", "foldl"]`                   | 491.220 ms (5%) |         |                  |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 295.374 ms (5%) |         |  417.19 KiB (1%) |        5920 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 279.717 ms (5%) |         |  208.25 KiB (1%) |        2975 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 410.455 ms (5%) |         |  153.12 KiB (1%) |        2194 |
| `["findfirst", "n=500", "foldl"]`                   |  82.738 ms (5%) |         |                  |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 144.946 ms (5%) |         |  195.77 KiB (1%) |        2684 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 242.219 ms (5%) |         |  146.95 KiB (1%) |        2050 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 121.558 ms (5%) |         |   56.83 KiB (1%) |         778 |
| `["overhead", "default"]`                           |  75.507 μs (5%) |         |   32.73 KiB (1%) |         418 |
| `["overhead", "stoppable=false"]`                   |  76.506 μs (5%) |         |   32.75 KiB (1%) |         418 |
| `["overhead", "stoppable=true"]`                    |  82.907 μs (5%) |         |   44.25 KiB (1%) |         610 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   2.890 ms (5%) |         |  728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   3.655 ms (5%) |         |    2.05 MiB (1%) |         222 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   3.198 ms (5%) |         |    1.42 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  19.499 ms (5%) |         |    1.57 MiB (1%) |        2105 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  28.442 ms (5%) |         |    1.24 MiB (1%) |        6807 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  25.677 ms (5%) |         |    1.30 MiB (1%) |        5867 |
| `["parallel_histogram", "seq"]`                     |   5.088 ms (5%) |         |  364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  33.594 ms (5%) |         |                  |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  17.204 ms (5%) |         |   736 bytes (1%) |          11 |
| `["splitby", "count", "foldl"]`                     |   2.023 ms (5%) |         |                  |             |
| `["splitby", "count", "man"]`                       |   1.461 ms (5%) |         |                  |             |
| `["splitby", "count", "reduce"]`                    |   1.051 ms (5%) |         |    1.09 KiB (1%) |          19 |
| `["sum", "random", "foldl"]`                        |  15.404 ms (5%) |         |                  |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   8.535 ms (5%) |         |   74.14 KiB (1%) |        1103 |
| `["sum", "random", "reduce", "basesize=256"]`       |   8.467 ms (5%) |         |   36.73 KiB (1%) |         546 |
| `["sum", "random", "reduce", "basesize=512"]`       |   7.649 ms (5%) |         |   18.11 KiB (1%) |         270 |
| `["sum", "uniform", "foldl"]`                       |  15.243 ms (5%) |         |                  |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   7.965 ms (5%) |         |   74.17 KiB (1%) |        1104 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   7.872 ms (5%) |         |   36.73 KiB (1%) |         546 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   7.998 ms (5%) |         |   18.00 KiB (1%) |         267 |
| `["sum", "valley", "foldl"]`                        |  16.003 ms (5%) |         |                  |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   8.442 ms (5%) |         |   74.05 KiB (1%) |        1100 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   8.281 ms (5%) |         |   36.77 KiB (1%) |         547 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   8.108 ms (5%) |         |   18.03 KiB (1%) |         268 |
| `["words", "nthreads=1"]`                           |  23.376 ms (5%) |         |   31.63 MiB (1%) |     1030188 |
| `["words", "nthreads=2"]`                           |  14.958 ms (5%) |         |   31.99 MiB (1%) |     1030224 |
| `["words", "nthreads=4"]`                           |  15.480 ms (5%) |         |   32.70 MiB (1%) |     1030322 |

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
  uname: Linux 5.15.0-1020-azure #25~20.04.1-Ubuntu SMP Thu Sep 1 19:20:56 UTC 2022 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz       4921 s          0 s        249 s       2753 s          0 s
       #2  2095 MHz       5472 s          0 s        277 s       2180 s          0 s
       
  Memory: 6.781253814697266 GB (3702.3671875 MB free)
  Uptime: 798.22 sec
  Load Avg:  1.72  1.51  0.91
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, skylake-avx512)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 5 Oct 2022 - 17:26
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

| ID                                                  | time            | GC time | memory           | allocations |
|-----------------------------------------------------|----------------:|--------:|-----------------:|------------:|
| `["collect", "assoc", "basesize=1"]`                | 273.579 ms (5%) |         |   25.97 MiB (1%) |      306816 |
| `["collect", "assoc", "basesize=1024"]`             | 216.962 ms (5%) |         |    2.61 MiB (1%) |         456 |
| `["collect", "assoc", "basesize=32"]`               | 224.308 ms (5%) |         |    4.82 MiB (1%) |       11701 |
| `["collect", "seq"]`                                | 402.080 ms (5%) |         |  812.73 KiB (1%) |          11 |
| `["collect", "unordered", "basesize=1"]`            | 377.226 ms (5%) |         |   23.92 MiB (1%) |      413686 |
| `["collect", "unordered", "basesize=1024"]`         | 227.800 ms (5%) |         | 1002.55 KiB (1%) |        1074 |
| `["collect", "unordered", "basesize=32"]`           | 241.554 ms (5%) |         |    1.59 MiB (1%) |       14870 |
| `["findfirst", "n=1000", "foldl"]`                  | 651.833 ms (5%) |         |                  |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 380.668 ms (5%) |         |  229.64 KiB (1%) |        3233 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 473.411 ms (5%) |         |  157.20 KiB (1%) |        2193 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 569.216 ms (5%) |         |   99.09 KiB (1%) |        1377 |
| `["findfirst", "n=400", "foldl"]`                   | 481.382 ms (5%) |         |                  |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 258.394 ms (5%) |         |  382.64 KiB (1%) |        5454 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 260.866 ms (5%) |         |  200.52 KiB (1%) |        2862 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 379.958 ms (5%) |         |  146.59 KiB (1%) |        2092 |
| `["findfirst", "n=500", "foldl"]`                   |  83.328 ms (5%) |         |                  |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 102.078 ms (5%) |         |  163.61 KiB (1%) |        2227 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 107.585 ms (5%) |         |   95.19 KiB (1%) |        1286 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 220.703 ms (5%) |         |   96.00 KiB (1%) |        1301 |
| `["overhead", "default"]`                           |  76.407 μs (5%) |         |   32.73 KiB (1%) |         418 |
| `["overhead", "stoppable=false"]`                   |  78.907 μs (5%) |         |   32.66 KiB (1%) |         415 |
| `["overhead", "stoppable=true"]`                    |  87.207 μs (5%) |         |   44.22 KiB (1%) |         609 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   3.117 ms (5%) |         |  728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   3.996 ms (5%) |         |    1.79 MiB (1%) |         215 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   3.629 ms (5%) |         |    1.42 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  21.388 ms (5%) |         |    1.61 MiB (1%) |        3412 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  29.484 ms (5%) |         |    1.25 MiB (1%) |        7273 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  26.352 ms (5%) |         |    1.70 MiB (1%) |        6238 |
| `["parallel_histogram", "seq"]`                     |   5.602 ms (5%) |         |  364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  34.547 ms (5%) |         |                  |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  17.254 ms (5%) |         |   736 bytes (1%) |          11 |
| `["splitby", "count", "foldl"]`                     |   1.917 ms (5%) |         |                  |             |
| `["splitby", "count", "man"]`                       |   1.462 ms (5%) |         |                  |             |
| `["splitby", "count", "reduce"]`                    | 913.276 μs (5%) |         |    1.09 KiB (1%) |          19 |
| `["sum", "random", "foldl"]`                        |  15.694 ms (5%) |         |                  |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   7.442 ms (5%) |         |   74.14 KiB (1%) |        1103 |
| `["sum", "random", "reduce", "basesize=256"]`       |   7.628 ms (5%) |         |   36.70 KiB (1%) |         545 |
| `["sum", "random", "reduce", "basesize=512"]`       |   7.795 ms (5%) |         |   18.08 KiB (1%) |         269 |
| `["sum", "uniform", "foldl"]`                       |  14.726 ms (5%) |         |                  |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   7.299 ms (5%) |         |   74.20 KiB (1%) |        1105 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   7.235 ms (5%) |         |   36.70 KiB (1%) |         545 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   7.125 ms (5%) |         |   18.03 KiB (1%) |         268 |
| `["sum", "valley", "foldl"]`                        |  14.996 ms (5%) |         |                  |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   7.741 ms (5%) |         |   74.14 KiB (1%) |        1103 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   7.783 ms (5%) |         |   36.77 KiB (1%) |         547 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   7.532 ms (5%) |         |   18.00 KiB (1%) |         267 |
| `["words", "nthreads=1"]`                           |  25.001 ms (5%) |         |   31.69 MiB (1%) |     1032908 |
| `["words", "nthreads=2"]`                           |  16.314 ms (5%) |         |   32.05 MiB (1%) |     1032944 |
| `["words", "nthreads=4"]`                           |  15.938 ms (5%) |         |   32.76 MiB (1%) |     1033052 |

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
  uname: Linux 5.15.0-1020-azure #25~20.04.1-Ubuntu SMP Thu Sep 1 19:20:56 UTC 2022 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz       7789 s          0 s        291 s       2822 s          0 s
       #2  2095 MHz       7233 s          0 s        311 s       3358 s          0 s
       
  Memory: 6.781253814697266 GB (3724.4375 MB free)
  Uptime: 1096.3 sec
  Load Avg:  1.66  1.57  1.1
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
    CPU MHz:                         2095.224
    BogoMIPS:                        4190.44
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

