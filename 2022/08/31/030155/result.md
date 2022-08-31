# Multi-thread benchmark result

* Pull request commit: [`0b5eb9d796856e05d18a02bec84c29c360db245f`](https://github.com/JuliaFolds/Transducers.jl/commit/0b5eb9d796856e05d18a02bec84c29c360db245f)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/243> (Update */Manifest.toml)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 31 Aug 2022 - 02:56
    - Baseline: 31 Aug 2022 - 03:01
* Package commits:
    - Target: 6df954
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
| `["collect", "unordered", "basesize=1"]`            |                   0.98 (5%)  | 0.99 (1%) :white_check_mark: |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 0.69 (5%) :white_check_mark: | 0.69 (1%) :white_check_mark: |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` |                1.13 (5%) :x: |                1.12 (1%) :x: |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` |                1.10 (5%) :x: |                1.09 (1%) :x: |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  |                   0.99 (5%)  | 0.98 (1%) :white_check_mark: |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 0.94 (5%) :white_check_mark: | 0.98 (1%) :white_check_mark: |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |                1.10 (5%) :x: |                1.06 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 0.45 (5%) :white_check_mark: | 0.55 (1%) :white_check_mark: |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |                1.91 (5%) :x: |                1.82 (1%) :x: |
| `["parallel_histogram", "comm", "basesize=16384"]`  | 0.85 (5%) :white_check_mark: | 0.96 (1%) :white_check_mark: |
| `["parallel_histogram", "comm", "basesize=4096"]`   | 0.92 (5%) :white_check_mark: | 0.93 (1%) :white_check_mark: |
| `["parallel_histogram", "comm", "basesize=8192"]`   |                   1.01 (5%)  | 0.76 (1%) :white_check_mark: |
| `["splitby", "count", "reduce"]`                    |                   1.01 (5%)  |                1.03 (1%) :x: |
| `["words", "nthreads=1"]`                           | 0.85 (5%) :white_check_mark: |                   1.01 (1%)  |
| `["words", "nthreads=2"]`                           | 0.87 (5%) :white_check_mark: |                1.02 (1%) :x: |
| `["words", "nthreads=4"]`                           |                   0.95 (5%)  |                1.01 (1%) :x: |

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
       #1  2593 MHz       5026 s          1 s        257 s       3053 s          0 s
       #2  2593 MHz       5206 s          1 s        260 s       2890 s          0 s
       
  Memory: 6.781246185302734 GB (3482.9453125 MB free)
  Uptime: 841.0 sec
  Load Avg:  1.75  1.51  0.9
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
       #1  2593 MHz       7433 s          1 s        325 s       3681 s          0 s
       #2  2593 MHz       7565 s          1 s        316 s       3582 s          0 s
       
  Memory: 6.781246185302734 GB (3435.3203125 MB free)
  Uptime: 1151.94 sec
  Load Avg:  1.61  1.57  1.11
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, skylake-avx512)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 31 Aug 2022 - 2:56
* Package commit: 6df954
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
| `["collect", "assoc", "basesize=1"]`                | 245.493 ms (5%) |         |   25.97 MiB (1%) |      306766 |
| `["collect", "assoc", "basesize=1024"]`             | 198.431 ms (5%) |         |    2.61 MiB (1%) |         456 |
| `["collect", "assoc", "basesize=32"]`               | 200.553 ms (5%) |         |    4.82 MiB (1%) |       11706 |
| `["collect", "seq"]`                                | 395.469 ms (5%) |         |  812.73 KiB (1%) |          11 |
| `["collect", "unordered", "basesize=1"]`            | 349.394 ms (5%) |         |   23.57 MiB (1%) |      402068 |
| `["collect", "unordered", "basesize=1024"]`         | 213.999 ms (5%) |         | 1003.64 KiB (1%) |         871 |
| `["collect", "unordered", "basesize=32"]`           | 225.887 ms (5%) |         |    1.58 MiB (1%) |       14686 |
| `["findfirst", "n=1000", "foldl"]`                  | 631.328 ms (5%) |         |                  |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 348.257 ms (5%) |         |  232.86 KiB (1%) |        3276 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 424.376 ms (5%) |         |  157.20 KiB (1%) |        2193 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 567.368 ms (5%) |         |  108.55 KiB (1%) |        1509 |
| `["findfirst", "n=400", "foldl"]`                   | 473.108 ms (5%) |         |                  |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 243.132 ms (5%) |         |  371.09 KiB (1%) |        5296 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 248.966 ms (5%) |         |  199.22 KiB (1%) |        2851 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 367.564 ms (5%) |         |  156.50 KiB (1%) |        2214 |
| `["findfirst", "n=500", "foldl"]`                   |  82.037 ms (5%) |         |                  |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 164.834 ms (5%) |         |  215.08 KiB (1%) |        3025 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |  72.091 ms (5%) |         |   72.12 KiB (1%) |         978 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 211.661 ms (5%) |         |  103.62 KiB (1%) |        1407 |
| `["overhead", "default"]`                           |  75.301 μs (5%) |         |   32.73 KiB (1%) |         418 |
| `["overhead", "stoppable=false"]`                   |  75.101 μs (5%) |         |   32.75 KiB (1%) |         418 |
| `["overhead", "stoppable=true"]`                    |  85.201 μs (5%) |         |   44.25 KiB (1%) |         610 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   3.244 ms (5%) |         |  728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   3.897 ms (5%) |         |    1.79 MiB (1%) |         216 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   3.581 ms (5%) |         |    1.42 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  15.946 ms (5%) |         |    1.55 MiB (1%) |        1297 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  22.732 ms (5%) |         |    1.16 MiB (1%) |        4192 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  22.742 ms (5%) |         |    1.28 MiB (1%) |        5731 |
| `["parallel_histogram", "seq"]`                     |   5.761 ms (5%) |         |  364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  35.203 ms (5%) |         |                  |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  17.579 ms (5%) |         |   736 bytes (1%) |          11 |
| `["splitby", "count", "foldl"]`                     |   2.334 ms (5%) |         |                  |             |
| `["splitby", "count", "man"]`                       |   1.752 ms (5%) |         |                  |             |
| `["splitby", "count", "reduce"]`                    |   1.095 ms (5%) |         |    1.09 KiB (1%) |          19 |
| `["sum", "random", "foldl"]`                        |  16.247 ms (5%) |         |                  |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   8.185 ms (5%) |         |   74.17 KiB (1%) |        1104 |
| `["sum", "random", "reduce", "basesize=256"]`       |   8.085 ms (5%) |         |   36.64 KiB (1%) |         543 |
| `["sum", "random", "reduce", "basesize=512"]`       |   8.057 ms (5%) |         |   18.14 KiB (1%) |         271 |
| `["sum", "uniform", "foldl"]`                       |  15.779 ms (5%) |         |                  |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   8.006 ms (5%) |         |   74.02 KiB (1%) |        1099 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   7.913 ms (5%) |         |   36.73 KiB (1%) |         546 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   7.840 ms (5%) |         |   17.97 KiB (1%) |         266 |
| `["sum", "valley", "foldl"]`                        |  16.166 ms (5%) |         |                  |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   8.245 ms (5%) |         |   74.14 KiB (1%) |        1103 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   8.157 ms (5%) |         |   36.73 KiB (1%) |         546 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   8.109 ms (5%) |         |   18.03 KiB (1%) |         268 |
| `["words", "nthreads=1"]`                           |  22.327 ms (5%) |         |   31.94 MiB (1%) |     1040705 |
| `["words", "nthreads=2"]`                           |  14.348 ms (5%) |         |   32.66 MiB (1%) |     1040816 |
| `["words", "nthreads=4"]`                           |  14.885 ms (5%) |         |   33.29 MiB (1%) |     1041009 |

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
       #1  2593 MHz       5026 s          1 s        257 s       3053 s          0 s
       #2  2593 MHz       5206 s          1 s        260 s       2890 s          0 s
       
  Memory: 6.781246185302734 GB (3482.9453125 MB free)
  Uptime: 841.0 sec
  Load Avg:  1.75  1.51  0.9
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, skylake-avx512)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 31 Aug 2022 - 3:1
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

| ID                                                  | time            | GC time | memory           | allocations |
|-----------------------------------------------------|----------------:|--------:|-----------------:|------------:|
| `["collect", "assoc", "basesize=1"]`                | 249.281 ms (5%) |         |   25.97 MiB (1%) |      306848 |
| `["collect", "assoc", "basesize=1024"]`             | 199.121 ms (5%) |         |    2.61 MiB (1%) |         455 |
| `["collect", "assoc", "basesize=32"]`               | 201.592 ms (5%) |         |    4.82 MiB (1%) |       11709 |
| `["collect", "seq"]`                                | 395.284 ms (5%) |         |  812.73 KiB (1%) |          11 |
| `["collect", "unordered", "basesize=1"]`            | 356.503 ms (5%) |         |   23.89 MiB (1%) |      412539 |
| `["collect", "unordered", "basesize=1024"]`         | 213.905 ms (5%) |         | 1009.20 KiB (1%) |        1205 |
| `["collect", "unordered", "basesize=32"]`           | 225.310 ms (5%) |         |    1.59 MiB (1%) |       15022 |
| `["findfirst", "n=1000", "foldl"]`                  | 631.821 ms (5%) |         |                  |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 502.630 ms (5%) |         |  335.52 KiB (1%) |        4683 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 374.464 ms (5%) |         |  140.19 KiB (1%) |        1956 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 516.806 ms (5%) |         |   99.95 KiB (1%) |        1392 |
| `["findfirst", "n=400", "foldl"]`                   | 472.736 ms (5%) |         |                  |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 245.841 ms (5%) |         |  378.50 KiB (1%) |        5399 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 246.282 ms (5%) |         |  198.53 KiB (1%) |        2842 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 392.225 ms (5%) |         |  160.41 KiB (1%) |        2300 |
| `["findfirst", "n=500", "foldl"]`                   |  82.034 ms (5%) |         |                  |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 149.268 ms (5%) |         |  202.83 KiB (1%) |        2821 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 160.713 ms (5%) |         |  130.53 KiB (1%) |        1782 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 110.914 ms (5%) |         |   56.84 KiB (1%) |         779 |
| `["overhead", "default"]`                           |  75.301 μs (5%) |         |   32.67 KiB (1%) |         416 |
| `["overhead", "stoppable=false"]`                   |  75.301 μs (5%) |         |   32.75 KiB (1%) |         418 |
| `["overhead", "stoppable=true"]`                    |  85.901 μs (5%) |         |   44.25 KiB (1%) |         610 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   3.255 ms (5%) |         |  728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   3.896 ms (5%) |         |    1.79 MiB (1%) |         216 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   3.586 ms (5%) |         |    1.42 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  18.768 ms (5%) |         |    1.62 MiB (1%) |        3603 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  24.825 ms (5%) |         |    1.25 MiB (1%) |        7003 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  22.477 ms (5%) |         |    1.68 MiB (1%) |        5795 |
| `["parallel_histogram", "seq"]`                     |   5.801 ms (5%) |         |  364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  35.231 ms (5%) |         |                  |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  17.634 ms (5%) |         |   736 bytes (1%) |          11 |
| `["splitby", "count", "foldl"]`                     |   2.331 ms (5%) |         |                  |             |
| `["splitby", "count", "man"]`                       |   1.754 ms (5%) |         |                  |             |
| `["splitby", "count", "reduce"]`                    |   1.088 ms (5%) |         |    1.06 KiB (1%) |          19 |
| `["sum", "random", "foldl"]`                        |  16.270 ms (5%) |         |                  |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   8.138 ms (5%) |         |   74.17 KiB (1%) |        1104 |
| `["sum", "random", "reduce", "basesize=256"]`       |   8.097 ms (5%) |         |   36.73 KiB (1%) |         546 |
| `["sum", "random", "reduce", "basesize=512"]`       |   8.118 ms (5%) |         |   18.05 KiB (1%) |         268 |
| `["sum", "uniform", "foldl"]`                       |  15.717 ms (5%) |         |                  |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   7.989 ms (5%) |         |   74.08 KiB (1%) |        1101 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   7.897 ms (5%) |         |   36.77 KiB (1%) |         547 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   7.838 ms (5%) |         |   18.03 KiB (1%) |         268 |
| `["sum", "valley", "foldl"]`                        |  16.137 ms (5%) |         |                  |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   8.236 ms (5%) |         |   74.02 KiB (1%) |        1099 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   8.137 ms (5%) |         |   36.67 KiB (1%) |         544 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   8.147 ms (5%) |         |   18.06 KiB (1%) |         269 |
| `["words", "nthreads=1"]`                           |  26.340 ms (5%) |         |   31.70 MiB (1%) |     1032358 |
| `["words", "nthreads=2"]`                           |  16.459 ms (5%) |         |   32.05 MiB (1%) |     1032402 |
| `["words", "nthreads=4"]`                           |  15.649 ms (5%) |         |   32.95 MiB (1%) |     1032570 |

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
       #1  2593 MHz       7433 s          1 s        325 s       3681 s          0 s
       #2  2593 MHz       7565 s          1 s        316 s       3582 s          0 s
       
  Memory: 6.781246185302734 GB (3435.3203125 MB free)
  Uptime: 1151.94 sec
  Load Avg:  1.61  1.57  1.11
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
    CPU MHz:                         2593.904
    BogoMIPS:                        5187.80
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
    Flags:                           fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush mmx fxsr sse sse2 ss ht syscall nx pdpe1gb rdtscp lm constant_tsc rep_good nopl xtopology cpuid pni pclmulqdq ssse3 fma cx16 pcid sse4_1 sse4_2 movbe popcnt aes xsave avx f16c rdrand hypervisor lahf_lm abm 3dnowprefetch invpcid_single pti fsgsbase bmi1 hle avx2 smep bmi2 erms invpcid rtm avx512f avx512dq rdseed adx smap clflushopt avx512cd avx512bw avx512vl xsaveopt xsavec xsaves md_clear
    

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

