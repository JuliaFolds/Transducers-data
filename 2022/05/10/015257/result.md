# Multi-thread benchmark result

* Pull request commit: [`6a5ab2e66c797f552c3ecc1037389c2b0961bdbd`](https://github.com/JuliaFolds/Transducers.jl/commit/6a5ab2e66c797f552c3ecc1037389c2b0961bdbd)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/243> (Update */Manifest.toml)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 10 May 2022 - 01:47
    - Baseline: 10 May 2022 - 01:52
* Package commits:
    - Target: 92ef45
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
| `["findfirst", "n=1000", "reduce", "basesize=128"]` |                1.22 (5%) :x: |                1.31 (1%) :x: |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` |                1.08 (5%) :x: |                1.04 (1%) :x: |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 0.84 (5%) :white_check_mark: | 0.90 (1%) :white_check_mark: |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  |                   1.00 (5%)  | 0.95 (1%) :white_check_mark: |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  |                1.14 (5%) :x: |                1.32 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 0.80 (5%) :white_check_mark: | 0.81 (1%) :white_check_mark: |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 0.67 (5%) :white_check_mark: | 0.65 (1%) :white_check_mark: |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |                1.19 (5%) :x: |                1.15 (1%) :x: |
| `["overhead", "default"]`                           |                1.09 (5%) :x: |                   1.00 (1%)  |
| `["overhead", "stoppable=true"]`                    |                1.08 (5%) :x: |                   1.00 (1%)  |
| `["parallel_histogram", "comm", "basesize=16384"]`  | 0.83 (5%) :white_check_mark: | 0.94 (1%) :white_check_mark: |
| `["parallel_histogram", "comm", "basesize=4096"]`   | 0.92 (5%) :white_check_mark: | 0.94 (1%) :white_check_mark: |
| `["parallel_histogram", "comm", "basesize=8192"]`   |                   0.98 (5%)  | 0.96 (1%) :white_check_mark: |
| `["partition_length_maximum", "rand", "foldl"]`     | 0.90 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["splitby", "count", "reduce"]`                    |                   1.00 (5%)  | 0.93 (1%) :white_check_mark: |

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
  uname: Linux 5.13.0-1022-azure #26~20.04.1-Ubuntu SMP Thu Apr 7 19:42:45 UTC 2022 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz: 
              speed         user         nice          sys         idle          irq
       #1  2294 MHz       5015 s          2 s        235 s       2057 s          0 s
       #2  2294 MHz       5361 s          0 s        248 s       1705 s          0 s
       
  Memory: 6.783607482910156 GB (3708.19921875 MB free)
  Uptime: 738.58 sec
  Load Avg:  1.75  1.54  0.95
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, broadwell)
```

### Baseline
```
Julia Version 1.7.2
Commit bf53498635 (2022-02-06 15:21 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 20.04.4 LTS
  uname: Linux 5.13.0-1022-azure #26~20.04.1-Ubuntu SMP Thu Apr 7 19:42:45 UTC 2022 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz: 
              speed         user         nice          sys         idle          irq
       #1  2294 MHz       7030 s          2 s        295 s       3152 s          0 s
       #2  2294 MHz       8148 s          0 s        324 s       2010 s          0 s
       
  Memory: 6.783607482910156 GB (3758.09375 MB free)
  Uptime: 1055.83 sec
  Load Avg:  1.62  1.56  1.12
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, broadwell)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 10 May 2022 - 1:47
* Package commit: 92ef45
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

| ID                                                  | time            | GC time | memory          | allocations |
|-----------------------------------------------------|----------------:|--------:|----------------:|------------:|
| `["collect", "assoc", "basesize=1"]`                | 200.332 ms (5%) |         |  25.97 MiB (1%) |      306854 |
| `["collect", "assoc", "basesize=1024"]`             | 149.580 ms (5%) |         |   2.61 MiB (1%) |         456 |
| `["collect", "assoc", "basesize=32"]`               | 151.875 ms (5%) |         |   4.82 MiB (1%) |       11711 |
| `["collect", "seq"]`                                | 288.348 ms (5%) |         | 812.73 KiB (1%) |          11 |
| `["collect", "unordered", "basesize=1"]`            | 308.959 ms (5%) |         |  23.92 MiB (1%) |      413573 |
| `["collect", "unordered", "basesize=1024"]`         | 163.165 ms (5%) |         |   1.02 MiB (1%) |        1560 |
| `["collect", "unordered", "basesize=32"]`           | 174.357 ms (5%) |         |   1.62 MiB (1%) |       15846 |
| `["findfirst", "n=1000", "foldl"]`                  | 474.114 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 370.547 ms (5%) |         | 298.09 KiB (1%) |        4136 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 386.224 ms (5%) |         | 160.52 KiB (1%) |        2238 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 481.857 ms (5%) |         | 108.55 KiB (1%) |        1509 |
| `["findfirst", "n=400", "foldl"]`                   | 356.511 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 202.820 ms (5%) |         | 373.62 KiB (1%) |        5331 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 205.057 ms (5%) |         | 200.83 KiB (1%) |        2873 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 272.781 ms (5%) |         | 151.03 KiB (1%) |        2117 |
| `["findfirst", "n=500", "foldl"]`                   |  62.034 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 104.185 ms (5%) |         | 180.86 KiB (1%) |        2518 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |  63.678 ms (5%) |         |  74.61 KiB (1%) |        1014 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  83.425 ms (5%) |         |  56.83 KiB (1%) |         778 |
| `["overhead", "default"]`                           |  71.400 μs (5%) |         |  32.70 KiB (1%) |         417 |
| `["overhead", "stoppable=false"]`                   |  69.000 μs (5%) |         |  32.75 KiB (1%) |         418 |
| `["overhead", "stoppable=true"]`                    |  83.800 μs (5%) |         |  44.25 KiB (1%) |         610 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   2.371 ms (5%) |         | 728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   2.914 ms (5%) |         |   1.79 MiB (1%) |         215 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   2.687 ms (5%) |         |   1.42 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  14.431 ms (5%) |         |   1.56 MiB (1%) |        1934 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  21.460 ms (5%) |         |   1.25 MiB (1%) |        7063 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  19.794 ms (5%) |         |   1.22 MiB (1%) |        6228 |
| `["parallel_histogram", "seq"]`                     |   4.196 ms (5%) |         | 364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  30.927 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  15.682 ms (5%) |         |  736 bytes (1%) |          11 |
| `["splitby", "count", "foldl"]`                     |   1.592 ms (5%) |         |                 |             |
| `["splitby", "count", "man"]`                       |   1.223 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    | 750.501 μs (5%) |         |   1.02 KiB (1%) |          18 |
| `["sum", "random", "foldl"]`                        |  11.555 ms (5%) |         |                 |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   5.826 ms (5%) |         |  74.20 KiB (1%) |        1105 |
| `["sum", "random", "reduce", "basesize=256"]`       |   5.681 ms (5%) |         |  36.70 KiB (1%) |         545 |
| `["sum", "random", "reduce", "basesize=512"]`       |   5.635 ms (5%) |         |  18.08 KiB (1%) |         269 |
| `["sum", "uniform", "foldl"]`                       |  11.221 ms (5%) |         |                 |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   5.710 ms (5%) |         |  74.20 KiB (1%) |        1105 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   5.598 ms (5%) |         |  36.77 KiB (1%) |         547 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   5.506 ms (5%) |         |  18.00 KiB (1%) |         267 |
| `["sum", "valley", "foldl"]`                        |  11.596 ms (5%) |         |                 |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   5.912 ms (5%) |         |  74.02 KiB (1%) |        1099 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   5.750 ms (5%) |         |  36.61 KiB (1%) |         542 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   5.752 ms (5%) |         |  18.03 KiB (1%) |         268 |
| `["words", "nthreads=1"]`                           |  21.270 ms (5%) |         |  31.51 MiB (1%) |     1026717 |
| `["words", "nthreads=2"]`                           |  13.910 ms (5%) |         |  32.22 MiB (1%) |     1026792 |
| `["words", "nthreads=4"]`                           |  14.003 ms (5%) |         |  32.85 MiB (1%) |     1026965 |

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
  uname: Linux 5.13.0-1022-azure #26~20.04.1-Ubuntu SMP Thu Apr 7 19:42:45 UTC 2022 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz: 
              speed         user         nice          sys         idle          irq
       #1  2294 MHz       5015 s          2 s        235 s       2057 s          0 s
       #2  2294 MHz       5361 s          0 s        248 s       1705 s          0 s
       
  Memory: 6.783607482910156 GB (3708.19921875 MB free)
  Uptime: 738.58 sec
  Load Avg:  1.75  1.54  0.95
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, broadwell)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 10 May 2022 - 1:52
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

| ID                                                  | time            | GC time | memory          | allocations |
|-----------------------------------------------------|----------------:|--------:|----------------:|------------:|
| `["collect", "assoc", "basesize=1"]`                | 198.325 ms (5%) |         |  25.97 MiB (1%) |      306902 |
| `["collect", "assoc", "basesize=1024"]`             | 148.639 ms (5%) |         |   2.61 MiB (1%) |         457 |
| `["collect", "assoc", "basesize=32"]`               | 151.408 ms (5%) |         |   4.82 MiB (1%) |       11710 |
| `["collect", "seq"]`                                | 289.684 ms (5%) |         | 812.73 KiB (1%) |          11 |
| `["collect", "unordered", "basesize=1"]`            | 322.250 ms (5%) |         |  23.91 MiB (1%) |      413207 |
| `["collect", "unordered", "basesize=1024"]`         | 162.740 ms (5%) |         |   1.02 MiB (1%) |        1468 |
| `["collect", "unordered", "basesize=32"]`           | 175.735 ms (5%) |         |   1.60 MiB (1%) |       15462 |
| `["findfirst", "n=1000", "foldl"]`                  | 495.843 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 303.935 ms (5%) |         | 227.38 KiB (1%) |        3210 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 355.998 ms (5%) |         | 154.47 KiB (1%) |        2171 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 573.765 ms (5%) |         | 120.97 KiB (1%) |        1698 |
| `["findfirst", "n=400", "foldl"]`                   | 375.102 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 202.986 ms (5%) |         | 394.23 KiB (1%) |        5595 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 205.651 ms (5%) |         | 200.86 KiB (1%) |        2873 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 239.996 ms (5%) |         | 114.27 KiB (1%) |        1647 |
| `["findfirst", "n=500", "foldl"]`                   |  60.571 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 130.780 ms (5%) |         | 224.14 KiB (1%) |        3126 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |  95.348 ms (5%) |         | 114.94 KiB (1%) |        1554 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  70.057 ms (5%) |         |  49.62 KiB (1%) |         672 |
| `["overhead", "default"]`                           |  65.800 μs (5%) |         |  32.70 KiB (1%) |         417 |
| `["overhead", "stoppable=false"]`                   |  69.000 μs (5%) |         |  32.75 KiB (1%) |         418 |
| `["overhead", "stoppable=true"]`                    |  77.700 μs (5%) |         |  44.25 KiB (1%) |         610 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   2.362 ms (5%) |         | 728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   2.903 ms (5%) |         |   1.79 MiB (1%) |         215 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   2.661 ms (5%) |         |   1.42 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  17.360 ms (5%) |         |   1.67 MiB (1%) |        5382 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  23.434 ms (5%) |         |   1.32 MiB (1%) |        9582 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  20.273 ms (5%) |         |   1.27 MiB (1%) |        7712 |
| `["parallel_histogram", "seq"]`                     |   4.175 ms (5%) |         | 364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  34.298 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  15.849 ms (5%) |         |  736 bytes (1%) |          11 |
| `["splitby", "count", "foldl"]`                     |   1.594 ms (5%) |         |                 |             |
| `["splitby", "count", "man"]`                       |   1.223 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    | 748.700 μs (5%) |         |   1.09 KiB (1%) |          19 |
| `["sum", "random", "foldl"]`                        |  11.819 ms (5%) |         |                 |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   6.044 ms (5%) |         |  74.20 KiB (1%) |        1105 |
| `["sum", "random", "reduce", "basesize=256"]`       |   5.800 ms (5%) |         |  36.67 KiB (1%) |         544 |
| `["sum", "random", "reduce", "basesize=512"]`       |   5.729 ms (5%) |         |  18.05 KiB (1%) |         268 |
| `["sum", "uniform", "foldl"]`                       |  11.210 ms (5%) |         |                 |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   5.893 ms (5%) |         |  74.08 KiB (1%) |        1101 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   5.663 ms (5%) |         |  36.70 KiB (1%) |         545 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   5.537 ms (5%) |         |  17.97 KiB (1%) |         266 |
| `["sum", "valley", "foldl"]`                        |  11.611 ms (5%) |         |                 |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   6.010 ms (5%) |         |  74.11 KiB (1%) |        1102 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   5.825 ms (5%) |         |  36.73 KiB (1%) |         546 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   5.723 ms (5%) |         |  18.00 KiB (1%) |         267 |
| `["words", "nthreads=1"]`                           |  21.819 ms (5%) |         |  31.57 MiB (1%) |     1028279 |
| `["words", "nthreads=2"]`                           |  13.647 ms (5%) |         |  32.28 MiB (1%) |     1028359 |
| `["words", "nthreads=4"]`                           |  14.212 ms (5%) |         |  32.73 MiB (1%) |     1028425 |

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
  uname: Linux 5.13.0-1022-azure #26~20.04.1-Ubuntu SMP Thu Apr 7 19:42:45 UTC 2022 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz: 
              speed         user         nice          sys         idle          irq
       #1  2294 MHz       7030 s          2 s        295 s       3152 s          0 s
       #2  2294 MHz       8148 s          0 s        324 s       2010 s          0 s
       
  Memory: 6.783607482910156 GB (3758.09375 MB free)
  Uptime: 1055.83 sec
  Load Avg:  1.62  1.56  1.12
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, broadwell)
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
    CPU MHz:                         2294.684
    BogoMIPS:                        4589.36
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
    Vulnerability Spectre v2:        Mitigation; Retpolines, STIBP disabled, RSB filling
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

