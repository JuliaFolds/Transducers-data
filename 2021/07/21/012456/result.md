# Multi-thread benchmark result

* Pull request commit: [`92885fc1e0f757f79caf17cad04d006744d81210`](https://github.com/JuliaFolds/Transducers.jl/commit/92885fc1e0f757f79caf17cad04d006744d81210)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/243> (Update */Manifest.toml)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 21 Jul 2021 - 01:18
    - Baseline: 21 Jul 2021 - 01:24
* Package commits:
    - Target: 1c8654
    - Baseline: 2cfb4c
* Julia commits:
    - Target: 69fcb5
    - Baseline: 69fcb5
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
| `["collect", "assoc", "basesize=1"]`                |                1.11 (5%) :x: |                   1.00 (1%)  |
| `["collect", "assoc", "basesize=1024"]`             |                1.15 (5%) :x: |                   1.00 (1%)  |
| `["collect", "assoc", "basesize=32"]`               |                1.10 (5%) :x: |                   1.00 (1%)  |
| `["collect", "seq"]`                                |                1.05 (5%) :x: |                   1.00 (1%)  |
| `["collect", "unordered", "basesize=1"]`            |                1.19 (5%) :x: |                   1.00 (1%)  |
| `["collect", "unordered", "basesize=1024"]`         |                1.09 (5%) :x: |                   1.01 (1%)  |
| `["collect", "unordered", "basesize=32"]`           |                1.14 (5%) :x: |                   1.00 (1%)  |
| `["findfirst", "n=1000", "foldl"]`                  |                1.06 (5%) :x: |                   1.00 (1%)  |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` |                1.25 (5%) :x: |                1.21 (1%) :x: |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` |                1.13 (5%) :x: |                1.07 (1%) :x: |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` |                1.26 (5%) :x: |                1.20 (1%) :x: |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  |                   0.99 (5%)  | 0.98 (1%) :white_check_mark: |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 0.92 (5%) :white_check_mark: | 0.95 (1%) :white_check_mark: |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |                   1.04 (5%)  | 0.90 (1%) :white_check_mark: |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |                   0.99 (5%)  |                1.05 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |                1.17 (5%) :x: |                1.06 (1%) :x: |
| `["overhead", "stoppable=false"]`                   |                1.07 (5%) :x: |                   1.00 (1%)  |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |                   0.99 (5%)  |                1.15 (1%) :x: |
| `["parallel_histogram", "comm", "basesize=16384"]`  |                   0.99 (5%)  | 0.96 (1%) :white_check_mark: |
| `["parallel_histogram", "comm", "basesize=4096"]`   |                1.13 (5%) :x: |                   1.00 (1%)  |
| `["parallel_histogram", "comm", "basesize=8192"]`   |                1.08 (5%) :x: |                   1.00 (1%)  |
| `["partition_length_maximum", "rand", "reduce"]`    |                1.38 (5%) :x: |                   1.00 (1%)  |
| `["splitby", "count", "foldl"]`                     | 0.53 (5%) :white_check_mark: | 0.17 (1%) :white_check_mark: |
| `["splitby", "count", "man"]`                       |                1.14 (5%) :x: |                   1.00 (1%)  |
| `["splitby", "count", "reduce"]`                    |                1.10 (5%) :x: |                   1.00 (1%)  |
| `["sum", "random", "reduce", "basesize=128"]`       |                1.10 (5%) :x: |                   1.00 (1%)  |
| `["sum", "random", "reduce", "basesize=512"]`       |                1.05 (5%) :x: |                   1.00 (1%)  |
| `["sum", "uniform", "foldl"]`                       |                1.08 (5%) :x: |                   1.00 (1%)  |
| `["sum", "uniform", "reduce", "basesize=256"]`      | 0.95 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["sum", "uniform", "reduce", "basesize=512"]`      | 0.93 (5%) :white_check_mark: |                   1.00 (1%)  |

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
Julia Version 1.5.4
Commit 69fcb5745b (2021-03-11 19:13 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 20.04.2 LTS
  uname: Linux 5.8.0-1036-azure #38~20.04.1-Ubuntu SMP Thu Jun 17 14:14:18 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz: 
              speed         user         nice          sys         idle          irq
       #1  2294 MHz      58650 s         14 s       2689 s      34770 s          0 s
       #2  2294 MHz      55527 s          8 s       2890 s      37775 s          0 s
       
  Memory: 6.790924072265625 GB (3104.1796875 MB free)
  Uptime: 974.0 sec
  Load Avg:  1.4375  1.47509765625  0.9599609375
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, broadwell)
```

### Baseline
```
Julia Version 1.5.4
Commit 69fcb5745b (2021-03-11 19:13 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 20.04.2 LTS
  uname: Linux 5.8.0-1036-azure #38~20.04.1-Ubuntu SMP Thu Jun 17 14:14:18 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz: 
              speed         user         nice          sys         idle          irq
       #1  2294 MHz      89954 s         14 s       3454 s      39675 s          0 s
       #2  2294 MHz      78569 s          8 s       3741 s      51033 s          0 s
       
  Memory: 6.790924072265625 GB (3072.51171875 MB free)
  Uptime: 1347.0 sec
  Load Avg:  1.52734375  1.509765625  1.14697265625
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, broadwell)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 21 Jul 2021 - 1:18
* Package commit: 1c8654
* Julia commit: 69fcb5
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
| `["collect", "assoc", "basesize=1"]`                | 298.374 ms (5%) |         |  32.66 MiB (1%) |      286769 |
| `["collect", "assoc", "basesize=1024"]`             | 225.771 ms (5%) |         |   1.79 MiB (1%) |         569 |
| `["collect", "assoc", "basesize=32"]`               | 225.921 ms (5%) |         |   3.97 MiB (1%) |       13306 |
| `["collect", "seq"]`                                | 423.200 ms (5%) |         | 512.72 KiB (1%) |          15 |
| `["collect", "unordered", "basesize=1"]`            | 614.624 ms (5%) |         |  30.02 MiB (1%) |      361020 |
| `["collect", "unordered", "basesize=1024"]`         | 359.812 ms (5%) |         | 857.20 KiB (1%) |        4170 |
| `["collect", "unordered", "basesize=32"]`           | 268.723 ms (5%) |         |   1.47 MiB (1%) |       12562 |
| `["findfirst", "n=1000", "foldl"]`                  | 720.843 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` |    1.082 s (5%) |         |   1.72 MiB (1%) |       30773 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 525.848 ms (5%) |         | 517.02 KiB (1%) |        9045 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 711.642 ms (5%) |         | 326.91 KiB (1%) |        5744 |
| `["findfirst", "n=400", "foldl"]`                   | 522.402 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 283.617 ms (5%) |         |   1.08 MiB (1%) |       19423 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 281.226 ms (5%) |         | 595.61 KiB (1%) |       10511 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 294.977 ms (5%) |         | 350.53 KiB (1%) |        6182 |
| `["findfirst", "n=500", "foldl"]`                   |  83.989 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 174.462 ms (5%) |         | 567.33 KiB (1%) |        9907 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 153.934 ms (5%) |         | 389.03 KiB (1%) |        6771 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 149.657 ms (5%) |         | 197.39 KiB (1%) |        3457 |
| `["overhead", "default"]`                           |  63.000 μs (5%) |         |  47.36 KiB (1%) |         382 |
| `["overhead", "stoppable=false"]`                   |  65.400 μs (5%) |         |  47.39 KiB (1%) |         382 |
| `["overhead", "stoppable=true"]`                    | 169.100 μs (5%) |         | 139.67 KiB (1%) |        2464 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   4.075 ms (5%) |         | 730.06 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   4.871 ms (5%) |         |   2.06 MiB (1%) |         219 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   4.383 ms (5%) |         |   1.43 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  14.513 ms (5%) |         | 998.55 KiB (1%) |         159 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  22.615 ms (5%) |         |   1.00 MiB (1%) |         804 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  17.643 ms (5%) |         |   1.23 MiB (1%) |         400 |
| `["parallel_histogram", "seq"]`                     |   7.035 ms (5%) |         | 364.61 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  41.267 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  27.525 ms (5%) |         |   2.66 KiB (1%) |          48 |
| `["splitby", "count", "foldl"]`                     |   2.150 ms (5%) |         |   16 bytes (1%) |           1 |
| `["splitby", "count", "man"]`                       |   1.811 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    | 960.700 μs (5%) |         |   2.78 KiB (1%) |          52 |
| `["sum", "random", "foldl"]`                        |  14.914 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "random", "reduce", "basesize=128"]`       |   8.149 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "random", "reduce", "basesize=256"]`       |   7.610 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "random", "reduce", "basesize=512"]`       |   7.901 ms (5%) |         |  25.30 KiB (1%) |         252 |
| `["sum", "uniform", "foldl"]`                       |  15.201 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   7.618 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   7.204 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   7.050 ms (5%) |         |  25.25 KiB (1%) |         251 |
| `["sum", "valley", "foldl"]`                        |  15.283 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "valley", "reduce", "basesize=128"]`       |   8.197 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   8.201 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   7.769 ms (5%) |         |  25.25 KiB (1%) |         251 |
| `["words", "nthreads=1"]`                           |  28.937 ms (5%) |         |  31.56 MiB (1%) |     1028314 |
| `["words", "nthreads=2"]`                           |  17.934 ms (5%) |         |  31.92 MiB (1%) |     1028353 |
| `["words", "nthreads=4"]`                           |  18.272 ms (5%) |         |  32.64 MiB (1%) |     1028425 |

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
Julia Version 1.5.4
Commit 69fcb5745b (2021-03-11 19:13 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 20.04.2 LTS
  uname: Linux 5.8.0-1036-azure #38~20.04.1-Ubuntu SMP Thu Jun 17 14:14:18 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz: 
              speed         user         nice          sys         idle          irq
       #1  2294 MHz      58650 s         14 s       2689 s      34770 s          0 s
       #2  2294 MHz      55527 s          8 s       2890 s      37775 s          0 s
       
  Memory: 6.790924072265625 GB (3104.1796875 MB free)
  Uptime: 974.0 sec
  Load Avg:  1.4375  1.47509765625  0.9599609375
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, broadwell)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 21 Jul 2021 - 1:24
* Package commit: 2cfb4c
* Julia commit: 69fcb5
* Julia command flags: None
* Environment variables: `JULIA_NUM_THREADS => 2`

## Results
Below is a table of this job's results, obtained by running the benchmarks.
The values listed in the `ID` column have the structure `[parent_group, child_group, ..., key]`, and can be used to
index into the BaseBenchmarks suite to retrieve the corresponding benchmarks.
The percentages accompanying time and memory values in the below table are noise tolerances. The "true"
time/memory value for a given benchmark is expected to fall within this percentage of the reported value.
An empty cell means that the value was zero.

| ID                                                  | time            | GC time  | memory           | allocations |
|-----------------------------------------------------|----------------:|---------:|-----------------:|------------:|
| `["collect", "assoc", "basesize=1"]`                | 268.199 ms (5%) |          |   32.66 MiB (1%) |      286772 |
| `["collect", "assoc", "basesize=1024"]`             | 196.281 ms (5%) |          |    1.79 MiB (1%) |         570 |
| `["collect", "assoc", "basesize=32"]`               | 204.906 ms (5%) |          |    3.97 MiB (1%) |       13306 |
| `["collect", "seq"]`                                | 401.589 ms (5%) |          |  512.72 KiB (1%) |          15 |
| `["collect", "unordered", "basesize=1"]`            | 514.975 ms (5%) | 6.204 ms |   30.01 MiB (1%) |      360756 |
| `["collect", "unordered", "basesize=1024"]`         | 330.540 ms (5%) |          |  851.64 KiB (1%) |        3992 |
| `["collect", "unordered", "basesize=32"]`           | 236.321 ms (5%) |          |    1.48 MiB (1%) |       12701 |
| `["findfirst", "n=1000", "foldl"]`                  | 681.949 ms (5%) |          |                  |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 868.942 ms (5%) |          |    1.41 MiB (1%) |       25345 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 465.430 ms (5%) |          |  484.67 KiB (1%) |        8481 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 566.293 ms (5%) |          |  271.83 KiB (1%) |        4781 |
| `["findfirst", "n=400", "foldl"]`                   | 509.730 ms (5%) |          |                  |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 286.606 ms (5%) |          |    1.11 MiB (1%) |       19905 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 290.345 ms (5%) |          |  595.34 KiB (1%) |       10495 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 320.093 ms (5%) |          |  368.81 KiB (1%) |        6500 |
| `["findfirst", "n=500", "foldl"]`                   |  80.454 ms (5%) |          |                  |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 167.470 ms (5%) |          |  632.52 KiB (1%) |       11052 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 154.936 ms (5%) |          |  370.58 KiB (1%) |        6449 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 128.215 ms (5%) |          |  185.69 KiB (1%) |        3241 |
| `["overhead", "default"]`                           |  63.800 μs (5%) |          |   47.36 KiB (1%) |         382 |
| `["overhead", "stoppable=false"]`                   |  61.400 μs (5%) |          |   47.39 KiB (1%) |         382 |
| `["overhead", "stoppable=true"]`                    | 172.100 μs (5%) |          |  139.67 KiB (1%) |        2464 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   3.893 ms (5%) |          |  730.06 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   4.914 ms (5%) |          |    1.79 MiB (1%) |         213 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   4.296 ms (5%) |          |    1.43 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  14.675 ms (5%) |          |    1.01 MiB (1%) |         160 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  20.090 ms (5%) |          | 1019.69 KiB (1%) |         902 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  16.272 ms (5%) |          |    1.23 MiB (1%) |         406 |
| `["parallel_histogram", "seq"]`                     |   6.769 ms (5%) |          |  364.61 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  39.615 ms (5%) |          |                  |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  19.881 ms (5%) |          |    2.66 KiB (1%) |          48 |
| `["splitby", "count", "foldl"]`                     |   4.039 ms (5%) |          |    96 bytes (1%) |           4 |
| `["splitby", "count", "man"]`                       |   1.590 ms (5%) |          |                  |             |
| `["splitby", "count", "reduce"]`                    | 877.099 μs (5%) |          |    2.78 KiB (1%) |          52 |
| `["sum", "random", "foldl"]`                        |  14.268 ms (5%) |          |    32 bytes (1%) |           2 |
| `["sum", "random", "reduce", "basesize=128"]`       |   7.396 ms (5%) |          |  103.23 KiB (1%) |        1018 |
| `["sum", "random", "reduce", "basesize=256"]`       |   7.398 ms (5%) |          |   51.23 KiB (1%) |         506 |
| `["sum", "random", "reduce", "basesize=512"]`       |   7.492 ms (5%) |          |   25.30 KiB (1%) |         252 |
| `["sum", "uniform", "foldl"]`                       |  14.097 ms (5%) |          |    32 bytes (1%) |           2 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   7.772 ms (5%) |          |  103.23 KiB (1%) |        1018 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   7.615 ms (5%) |          |   51.23 KiB (1%) |         506 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   7.597 ms (5%) |          |   25.25 KiB (1%) |         251 |
| `["sum", "valley", "foldl"]`                        |  15.316 ms (5%) |          |    32 bytes (1%) |           2 |
| `["sum", "valley", "reduce", "basesize=128"]`       |   7.824 ms (5%) |          |  103.23 KiB (1%) |        1018 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   7.820 ms (5%) |          |   51.23 KiB (1%) |         506 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   7.578 ms (5%) |          |   25.25 KiB (1%) |         251 |
| `["words", "nthreads=1"]`                           |  28.012 ms (5%) |          |   31.56 MiB (1%) |     1028038 |
| `["words", "nthreads=2"]`                           |  17.670 ms (5%) |          |   31.92 MiB (1%) |     1028088 |
| `["words", "nthreads=4"]`                           |  18.320 ms (5%) |          |   32.82 MiB (1%) |     1028248 |

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
Julia Version 1.5.4
Commit 69fcb5745b (2021-03-11 19:13 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 20.04.2 LTS
  uname: Linux 5.8.0-1036-azure #38~20.04.1-Ubuntu SMP Thu Jun 17 14:14:18 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz: 
              speed         user         nice          sys         idle          irq
       #1  2294 MHz      89954 s         14 s       3454 s      39675 s          0 s
       #2  2294 MHz      78569 s          8 s       3741 s      51033 s          0 s
       
  Memory: 6.790924072265625 GB (3072.51171875 MB free)
  Uptime: 1347.0 sec
  Load Avg:  1.52734375  1.509765625  1.14697265625
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, broadwell)
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
    Model:                           79
    Model name:                      Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz
    Stepping:                        1
    CPU MHz:                         2294.688
    BogoMIPS:                        4589.37
    Hypervisor vendor:               Microsoft
    Virtualization type:             full
    L1d cache:                       64 KiB
    L1i cache:                       64 KiB
    L2 cache:                        512 KiB
    L3 cache:                        50 MiB
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
    Flags:                           fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush mmx fxsr sse sse2 ss ht syscall nx pdpe1gb rdtscp lm constant_tsc rep_good nopl xtopology cpuid pni pclmulqdq ssse3 fma cx16 pcid sse4_1 sse4_2 movbe popcnt aes xsave avx f16c rdrand hypervisor lahf_lm abm 3dnowprefetch invpcid_single pti fsgsbase bmi1 hle avx2 smep bmi2 erms invpcid rtm rdseed adx smap xsaveopt md_clear
    

| Cpu Property       | Value                                                   |
|:------------------ |:------------------------------------------------------- |
| Brand              | Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz               |
| Vendor             | :Intel                                                  |
| Architecture       | :Broadwell                                              |
| Model              | Family: 0x06, Model: 0x4f, Stepping: 0x01, Type: 0x00   |
| Cores              | 2 physical cores, 2 logical cores (on executing CPU)    |
|                    | No Hyperthreading hardware capability detected          |
| Clock Frequencies  | Not supported by CPU                                    |
| Data Cache         | Level 1:3 : (32, 256, 51200) kbytes                     |
|                    | 64 byte cache line size                                 |
| Address Size       | 48 bits virtual, 46 bits physical                       |
| SIMD               | 256 bit = 32 byte max. SIMD vector size                 |
| Time Stamp Counter | TSC is accessible via `rdtsc`                           |
|                    | TSC increased at every clock cycle (non-invariant TSC)  |
| Perf. Monitoring   | Performance Monitoring Counters (PMC) are not supported |
| Hypervisor         | Yes, Microsoft                                          |

