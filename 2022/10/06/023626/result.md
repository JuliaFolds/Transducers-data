# Multi-thread benchmark result

* Pull request commit: [`7757ae90e5d7eff25cc6950172abd67230985b6d`](https://github.com/JuliaFolds/Transducers.jl/commit/7757ae90e5d7eff25cc6950172abd67230985b6d)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/243> (Update */Manifest.toml)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 6 Oct 2022 - 02:30
    - Baseline: 6 Oct 2022 - 02:36
* Package commits:
    - Target: 24d2fb
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
| `["collect", "unordered", "basesize=1"]`            |                   1.00 (5%)  |                1.01 (1%) :x: |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` |                1.44 (5%) :x: |                1.38 (1%) :x: |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` |                1.16 (5%) :x: |                1.11 (1%) :x: |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` |                1.91 (5%) :x: |                1.81 (1%) :x: |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  |                   0.99 (5%)  | 0.99 (1%) :white_check_mark: |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 0.91 (5%) :white_check_mark: | 0.96 (1%) :white_check_mark: |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |                1.38 (5%) :x: |                1.30 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |                2.76 (5%) :x: |                1.99 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |                1.31 (5%) :x: |                1.12 (1%) :x: |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |                   1.02 (5%)  |                1.30 (1%) :x: |
| `["parallel_histogram", "comm", "basesize=4096"]`   |                   0.98 (5%)  | 0.98 (1%) :white_check_mark: |
| `["splitby", "count", "reduce"]`                    |                   1.02 (5%)  |                1.03 (1%) :x: |

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
  CPU: Intel(R) Xeon(R) Platinum 8370C CPU @ 2.80GHz: 
              speed         user         nice          sys         idle          irq
       #1  2793 MHz       5998 s          1 s        189 s       1242 s          0 s
       #2  2793 MHz       4308 s          2 s        234 s       2890 s          0 s
       
  Memory: 6.78125 GB (3543.96484375 MB free)
  Uptime: 746.85 sec
  Load Avg:  1.55  1.47  0.88
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
  uname: Linux 5.15.0-1020-azure #25~20.04.1-Ubuntu SMP Thu Sep 1 19:20:56 UTC 2022 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8370C CPU @ 2.80GHz: 
              speed         user         nice          sys         idle          irq
       #1  2793 MHz       8186 s          1 s        249 s       2041 s          0 s
       #2  2793 MHz       6862 s          2 s        284 s       3338 s          0 s
       
  Memory: 6.78125 GB (3295.09765625 MB free)
  Uptime: 1052.21 sec
  Load Avg:  1.65  1.58  1.1
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, icelake-server)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 6 Oct 2022 - 2:30
* Package commit: 24d2fb
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
| `["collect", "assoc", "basesize=1"]`                | 279.178 ms (5%) |         |  25.97 MiB (1%) |      306862 |
| `["collect", "assoc", "basesize=1024"]`             | 238.542 ms (5%) |         |   2.61 MiB (1%) |         456 |
| `["collect", "assoc", "basesize=32"]`               | 240.032 ms (5%) |         |   4.82 MiB (1%) |       11708 |
| `["collect", "seq"]`                                | 476.678 ms (5%) |         | 812.73 KiB (1%) |          11 |
| `["collect", "unordered", "basesize=1"]`            | 377.103 ms (5%) |         |  23.91 MiB (1%) |      413318 |
| `["collect", "unordered", "basesize=1024"]`         | 250.585 ms (5%) |         |   1.01 MiB (1%) |        1049 |
| `["collect", "unordered", "basesize=32"]`           | 261.373 ms (5%) |         |   1.59 MiB (1%) |       14925 |
| `["findfirst", "n=1000", "foldl"]`                  | 736.740 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 580.914 ms (5%) |         | 320.83 KiB (1%) |        4502 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 572.672 ms (5%) |         | 173.72 KiB (1%) |        2432 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 958.370 ms (5%) |         | 147.30 KiB (1%) |        2067 |
| `["findfirst", "n=400", "foldl"]`                   | 554.225 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 287.114 ms (5%) |         | 381.11 KiB (1%) |        5436 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 296.270 ms (5%) |         | 201.12 KiB (1%) |        2882 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 346.815 ms (5%) |         | 129.55 KiB (1%) |        1843 |
| `["findfirst", "n=500", "foldl"]`                   |  95.756 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 180.844 ms (5%) |         | 225.80 KiB (1%) |        3116 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 242.032 ms (5%) |         | 154.17 KiB (1%) |        2126 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 137.117 ms (5%) |         |  61.48 KiB (1%) |         839 |
| `["overhead", "default"]`                           |  72.500 μs (5%) |         |  32.70 KiB (1%) |         417 |
| `["overhead", "stoppable=false"]`                   |  71.200 μs (5%) |         |  32.75 KiB (1%) |         418 |
| `["overhead", "stoppable=true"]`                    |  80.000 μs (5%) |         |  44.28 KiB (1%) |         611 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   3.708 ms (5%) |         | 728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   4.598 ms (5%) |         |   2.32 MiB (1%) |         227 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   4.103 ms (5%) |         |   1.42 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  16.629 ms (5%) |         |   1.69 MiB (1%) |        6081 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  25.167 ms (5%) |         |   1.40 MiB (1%) |       12048 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  22.919 ms (5%) |         |   1.42 MiB (1%) |       11145 |
| `["parallel_histogram", "seq"]`                     |   6.691 ms (5%) |         | 364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  41.200 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  20.619 ms (5%) |         |  736 bytes (1%) |          11 |
| `["splitby", "count", "foldl"]`                     |   2.365 ms (5%) |         |                 |             |
| `["splitby", "count", "man"]`                       |   1.528 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    |   1.101 ms (5%) |         |   1.09 KiB (1%) |          19 |
| `["sum", "random", "foldl"]`                        |  18.034 ms (5%) |         |                 |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   9.238 ms (5%) |         |  74.17 KiB (1%) |        1104 |
| `["sum", "random", "reduce", "basesize=256"]`       |   9.144 ms (5%) |         |  36.73 KiB (1%) |         546 |
| `["sum", "random", "reduce", "basesize=512"]`       |   9.081 ms (5%) |         |  18.05 KiB (1%) |         268 |
| `["sum", "uniform", "foldl"]`                       |  17.730 ms (5%) |         |                 |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   9.059 ms (5%) |         |  74.20 KiB (1%) |        1105 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   8.973 ms (5%) |         |  36.70 KiB (1%) |         545 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   8.911 ms (5%) |         |  18.00 KiB (1%) |         267 |
| `["sum", "valley", "foldl"]`                        |  18.143 ms (5%) |         |                 |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   9.267 ms (5%) |         |  74.14 KiB (1%) |        1103 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   9.168 ms (5%) |         |  36.70 KiB (1%) |         545 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   9.192 ms (5%) |         |  18.03 KiB (1%) |         268 |
| `["words", "nthreads=1"]`                           |  18.587 ms (5%) |         |  31.57 MiB (1%) |     1028458 |
| `["words", "nthreads=2"]`                           |  11.670 ms (5%) |         |  31.93 MiB (1%) |     1028494 |
| `["words", "nthreads=4"]`                           |  12.696 ms (5%) |         |  32.82 MiB (1%) |     1028650 |

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
  CPU: Intel(R) Xeon(R) Platinum 8370C CPU @ 2.80GHz: 
              speed         user         nice          sys         idle          irq
       #1  2793 MHz       5998 s          1 s        189 s       1242 s          0 s
       #2  2793 MHz       4308 s          2 s        234 s       2890 s          0 s
       
  Memory: 6.78125 GB (3543.96484375 MB free)
  Uptime: 746.85 sec
  Load Avg:  1.55  1.47  0.88
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, icelake-server)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 6 Oct 2022 - 2:36
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
| `["collect", "assoc", "basesize=1"]`                | 279.926 ms (5%) |         |  25.97 MiB (1%) |      306795 |
| `["collect", "assoc", "basesize=1024"]`             | 239.178 ms (5%) |         |   2.61 MiB (1%) |         455 |
| `["collect", "assoc", "basesize=32"]`               | 240.893 ms (5%) |         |   4.82 MiB (1%) |       11704 |
| `["collect", "seq"]`                                | 477.798 ms (5%) |         | 812.73 KiB (1%) |          11 |
| `["collect", "unordered", "basesize=1"]`            | 376.626 ms (5%) |         |  23.67 MiB (1%) |      405505 |
| `["collect", "unordered", "basesize=1024"]`         | 250.474 ms (5%) |         |   1.01 MiB (1%) |        1081 |
| `["collect", "unordered", "basesize=32"]`           | 261.409 ms (5%) |         |   1.59 MiB (1%) |       14957 |
| `["findfirst", "n=1000", "foldl"]`                  | 734.716 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 402.422 ms (5%) |         | 232.83 KiB (1%) |        3275 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 491.922 ms (5%) |         | 157.20 KiB (1%) |        2193 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 502.903 ms (5%) |         |  81.42 KiB (1%) |        1149 |
| `["findfirst", "n=400", "foldl"]`                   | 551.455 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 289.758 ms (5%) |         | 386.39 KiB (1%) |        5498 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 288.410 ms (5%) |         | 200.72 KiB (1%) |        2869 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 381.103 ms (5%) |         | 135.27 KiB (1%) |        1928 |
| `["findfirst", "n=500", "foldl"]`                   |  95.507 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 130.832 ms (5%) |         | 173.42 KiB (1%) |        2388 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |  87.847 ms (5%) |         |  77.50 KiB (1%) |        1052 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 104.612 ms (5%) |         |  54.72 KiB (1%) |         734 |
| `["overhead", "default"]`                           |  72.300 μs (5%) |         |  32.70 KiB (1%) |         417 |
| `["overhead", "stoppable=false"]`                   |  70.800 μs (5%) |         |  32.69 KiB (1%) |         416 |
| `["overhead", "stoppable=true"]`                    |  81.600 μs (5%) |         |  44.25 KiB (1%) |         610 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   3.711 ms (5%) |         | 728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   4.488 ms (5%) |         |   1.79 MiB (1%) |         216 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   4.091 ms (5%) |         |   1.42 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  15.922 ms (5%) |         |   1.69 MiB (1%) |        6177 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  25.570 ms (5%) |         |   1.43 MiB (1%) |       12985 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  22.632 ms (5%) |         |   1.42 MiB (1%) |       10514 |
| `["parallel_histogram", "seq"]`                     |   6.650 ms (5%) |         | 364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  41.259 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  20.560 ms (5%) |         |  736 bytes (1%) |          11 |
| `["splitby", "count", "foldl"]`                     |   2.306 ms (5%) |         |                 |             |
| `["splitby", "count", "man"]`                       |   1.528 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    |   1.084 ms (5%) |         |   1.06 KiB (1%) |          18 |
| `["sum", "random", "foldl"]`                        |  18.092 ms (5%) |         |                 |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   9.190 ms (5%) |         |  74.20 KiB (1%) |        1105 |
| `["sum", "random", "reduce", "basesize=256"]`       |   9.144 ms (5%) |         |  36.77 KiB (1%) |         547 |
| `["sum", "random", "reduce", "basesize=512"]`       |   9.092 ms (5%) |         |  18.11 KiB (1%) |         270 |
| `["sum", "uniform", "foldl"]`                       |  17.724 ms (5%) |         |                 |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   9.030 ms (5%) |         |  74.08 KiB (1%) |        1101 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   8.960 ms (5%) |         |  36.73 KiB (1%) |         546 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   8.901 ms (5%) |         |  18.00 KiB (1%) |         267 |
| `["sum", "valley", "foldl"]`                        |  18.135 ms (5%) |         |                 |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   9.269 ms (5%) |         |  74.05 KiB (1%) |        1100 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   9.177 ms (5%) |         |  36.67 KiB (1%) |         544 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   9.148 ms (5%) |         |  18.03 KiB (1%) |         268 |
| `["words", "nthreads=1"]`                           |  18.527 ms (5%) |         |  31.69 MiB (1%) |     1032282 |
| `["words", "nthreads=2"]`                           |  12.273 ms (5%) |         |  32.05 MiB (1%) |     1032355 |
| `["words", "nthreads=4"]`                           |  12.556 ms (5%) |         |  32.94 MiB (1%) |     1032529 |

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
  CPU: Intel(R) Xeon(R) Platinum 8370C CPU @ 2.80GHz: 
              speed         user         nice          sys         idle          irq
       #1  2793 MHz       8186 s          1 s        249 s       2041 s          0 s
       #2  2793 MHz       6862 s          2 s        284 s       3338 s          0 s
       
  Memory: 6.78125 GB (3295.09765625 MB free)
  Uptime: 1052.21 sec
  Load Avg:  1.65  1.58  1.1
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
    CPU MHz:                         2793.438
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
    Vulnerability Spectre v2:        Mitigation; Retpolines, STIBP disabled, RSB filling
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

