# Multi-thread benchmark result

* Pull request commit: [`e9228bcdbf09286a920ff59c8d057697e15d566b`](https://github.com/JuliaFolds/Transducers.jl/commit/e9228bcdbf09286a920ff59c8d057697e15d566b)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/243> (Update */Manifest.toml)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 18 Aug 2022 - 02:43
    - Baseline: 18 Aug 2022 - 02:48
* Package commits:
    - Target: e61d6d
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
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 0.94 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` |                   1.04 (5%)  |                1.02 (1%) :x: |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` |                1.18 (5%) :x: |                1.10 (1%) :x: |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  |                   0.98 (5%)  | 0.95 (1%) :white_check_mark: |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  |                1.07 (5%) :x: |                   1.00 (1%)  |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  |                1.51 (5%) :x: |                1.37 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 0.57 (5%) :white_check_mark: | 0.65 (1%) :white_check_mark: |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 0.29 (5%) :white_check_mark: | 0.38 (1%) :white_check_mark: |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |                1.50 (5%) :x: |                1.26 (1%) :x: |
| `["overhead", "default"]`                           |                1.09 (5%) :x: |                   1.00 (1%)  |
| `["overhead", "stoppable=false"]`                   |                1.05 (5%) :x: |                   1.00 (1%)  |
| `["overhead", "stoppable=true"]`                    |                1.10 (5%) :x: |                   1.00 (1%)  |
| `["parallel_histogram", "comm", "basesize=16384"]`  |                1.11 (5%) :x: |                1.04 (1%) :x: |
| `["parallel_histogram", "comm", "basesize=8192"]`   | 0.94 (5%) :white_check_mark: | 0.99 (1%) :white_check_mark: |
| `["parallel_histogram", "seq"]`                     | 0.92 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["partition_length_maximum", "rand", "foldl"]`     |                1.10 (5%) :x: |                   1.00 (1%)  |
| `["splitby", "count", "foldl"]`                     |                1.05 (5%) :x: |                   1.00 (1%)  |
| `["sum", "random", "reduce", "basesize=256"]`       | 0.94 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["sum", "uniform", "foldl"]`                       | 0.92 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["sum", "uniform", "reduce", "basesize=512"]`      | 0.90 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["sum", "valley", "foldl"]`                        |                1.05 (5%) :x: |                   1.00 (1%)  |
| `["sum", "valley", "reduce", "basesize=256"]`       |                1.07 (5%) :x: |                   1.00 (1%)  |
| `["words", "nthreads=1"]`                           | 0.89 (5%) :white_check_mark: |                1.01 (1%) :x: |
| `["words", "nthreads=2"]`                           |                   0.97 (5%)  |                1.01 (1%) :x: |
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
  uname: Linux 5.15.0-1017-azure #20~20.04.1-Ubuntu SMP Fri Aug 5 12:16:53 UTC 2022 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz: 
              speed         user         nice          sys         idle          irq
       #1  2294 MHz       5868 s          2 s        235 s       3983 s          0 s
       #2  2294 MHz       4659 s          1 s        261 s       5178 s          0 s
       
  Memory: 6.781246185302734 GB (3708.609375 MB free)
  Uptime: 1015.72 sec
  Load Avg:  1.69  1.48  0.9
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, broadwell)
```

### Baseline
```
Julia Version 1.7.3
Commit 742b9abb4d (2022-05-06 12:58 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 20.04.4 LTS
  uname: Linux 5.15.0-1017-azure #20~20.04.1-Ubuntu SMP Fri Aug 5 12:16:53 UTC 2022 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz: 
              speed         user         nice          sys         idle          irq
       #1  2294 MHz       8396 s          2 s        306 s       4616 s          0 s
       #2  2294 MHz       7023 s          1 s        343 s       5967 s          0 s
       
  Memory: 6.781246185302734 GB (3658.6796875 MB free)
  Uptime: 1339.88 sec
  Load Avg:  1.6  1.56  1.11
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, broadwell)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 18 Aug 2022 - 2:43
* Package commit: e61d6d
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
| `["collect", "assoc", "basesize=1"]`                | 239.368 ms (5%) |         |  25.97 MiB (1%) |      306823 |
| `["collect", "assoc", "basesize=1024"]`             | 175.446 ms (5%) |         |   2.61 MiB (1%) |         456 |
| `["collect", "assoc", "basesize=32"]`               | 180.247 ms (5%) |         |   4.82 MiB (1%) |       11714 |
| `["collect", "seq"]`                                | 339.270 ms (5%) |         | 812.73 KiB (1%) |          11 |
| `["collect", "unordered", "basesize=1"]`            | 362.297 ms (5%) |         |  23.94 MiB (1%) |      414438 |
| `["collect", "unordered", "basesize=1024"]`         | 188.787 ms (5%) |         |   1.03 MiB (1%) |        1611 |
| `["collect", "unordered", "basesize=32"]`           | 207.013 ms (5%) |         |   1.61 MiB (1%) |       15668 |
| `["findfirst", "n=1000", "foldl"]`                  | 542.707 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 314.761 ms (5%) |         | 232.92 KiB (1%) |        3278 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 461.410 ms (5%) |         | 168.36 KiB (1%) |        2370 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 600.454 ms (5%) |         | 119.67 KiB (1%) |        1686 |
| `["findfirst", "n=400", "foldl"]`                   | 421.137 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 222.877 ms (5%) |         | 386.88 KiB (1%) |        5499 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 230.115 ms (5%) |         | 200.98 KiB (1%) |        2877 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 379.378 ms (5%) |         | 154.05 KiB (1%) |        2181 |
| `["findfirst", "n=500", "foldl"]`                   |  68.644 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 116.625 ms (5%) |         | 191.67 KiB (1%) |        2628 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |  73.071 ms (5%) |         |  73.11 KiB (1%) |        1001 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 112.366 ms (5%) |         |  63.84 KiB (1%) |         871 |
| `["overhead", "default"]`                           |  77.201 μs (5%) |         |  32.73 KiB (1%) |         418 |
| `["overhead", "stoppable=false"]`                   |  73.301 μs (5%) |         |  32.75 KiB (1%) |         418 |
| `["overhead", "stoppable=true"]`                    |  88.701 μs (5%) |         |  44.28 KiB (1%) |         611 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   2.667 ms (5%) |         | 728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   3.414 ms (5%) |         |   1.79 MiB (1%) |         215 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   3.098 ms (5%) |         |   1.42 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  18.628 ms (5%) |         |   1.65 MiB (1%) |        4703 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  24.714 ms (5%) |         |   1.33 MiB (1%) |        9756 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  21.334 ms (5%) |         |   1.25 MiB (1%) |        7215 |
| `["parallel_histogram", "seq"]`                     |   4.479 ms (5%) |         | 364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  37.629 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  18.591 ms (5%) |         |  736 bytes (1%) |          11 |
| `["splitby", "count", "foldl"]`                     |   1.696 ms (5%) |         |                 |             |
| `["splitby", "count", "man"]`                       |   1.224 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    | 807.405 μs (5%) |         |   1.09 KiB (1%) |          19 |
| `["sum", "random", "foldl"]`                        |  13.336 ms (5%) |         |                 |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   6.841 ms (5%) |         |  74.20 KiB (1%) |        1105 |
| `["sum", "random", "reduce", "basesize=256"]`       |   6.408 ms (5%) |         |  36.67 KiB (1%) |         544 |
| `["sum", "random", "reduce", "basesize=512"]`       |   6.386 ms (5%) |         |  18.08 KiB (1%) |         269 |
| `["sum", "uniform", "foldl"]`                       |  12.392 ms (5%) |         |                 |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   7.048 ms (5%) |         |  74.14 KiB (1%) |        1103 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   6.395 ms (5%) |         |  36.77 KiB (1%) |         547 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   6.202 ms (5%) |         |  18.03 KiB (1%) |         268 |
| `["sum", "valley", "foldl"]`                        |  13.719 ms (5%) |         |                 |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   6.757 ms (5%) |         |  74.05 KiB (1%) |        1100 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   7.086 ms (5%) |         |  36.73 KiB (1%) |         546 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   6.845 ms (5%) |         |  18.03 KiB (1%) |         268 |
| `["words", "nthreads=1"]`                           |  25.890 ms (5%) |         |  31.69 MiB (1%) |     1031704 |
| `["words", "nthreads=2"]`                           |  16.345 ms (5%) |         |  32.04 MiB (1%) |     1031751 |
| `["words", "nthreads=4"]`                           |  16.663 ms (5%) |         |  32.94 MiB (1%) |     1031920 |

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
  CPU: Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz: 
              speed         user         nice          sys         idle          irq
       #1  2294 MHz       5868 s          2 s        235 s       3983 s          0 s
       #2  2294 MHz       4659 s          1 s        261 s       5178 s          0 s
       
  Memory: 6.781246185302734 GB (3708.609375 MB free)
  Uptime: 1015.72 sec
  Load Avg:  1.69  1.48  0.9
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, broadwell)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 18 Aug 2022 - 2:48
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
| `["collect", "assoc", "basesize=1"]`                | 231.599 ms (5%) |         |  25.97 MiB (1%) |      306836 |
| `["collect", "assoc", "basesize=1024"]`             | 178.174 ms (5%) |         |   2.61 MiB (1%) |         454 |
| `["collect", "assoc", "basesize=32"]`               | 175.382 ms (5%) |         |   4.82 MiB (1%) |       11711 |
| `["collect", "seq"]`                                | 347.461 ms (5%) |         | 812.73 KiB (1%) |          11 |
| `["collect", "unordered", "basesize=1"]`            | 367.488 ms (5%) |         |  23.92 MiB (1%) |      413568 |
| `["collect", "unordered", "basesize=1024"]`         | 195.894 ms (5%) |         |   1.02 MiB (1%) |        1472 |
| `["collect", "unordered", "basesize=32"]`           | 206.240 ms (5%) |         |   1.60 MiB (1%) |       15437 |
| `["findfirst", "n=1000", "foldl"]`                  | 546.198 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 335.684 ms (5%) |         | 232.80 KiB (1%) |        3274 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 442.946 ms (5%) |         | 165.36 KiB (1%) |        2320 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 508.303 ms (5%) |         | 108.55 KiB (1%) |        1509 |
| `["findfirst", "n=400", "foldl"]`                   | 411.364 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 226.802 ms (5%) |         | 405.89 KiB (1%) |        5742 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 216.034 ms (5%) |         | 201.08 KiB (1%) |        2880 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 250.571 ms (5%) |         | 112.62 KiB (1%) |        1623 |
| `["findfirst", "n=500", "foldl"]`                   |  71.044 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 204.405 ms (5%) |         | 296.86 KiB (1%) |        4148 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 250.974 ms (5%) |         | 190.30 KiB (1%) |        2638 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  74.685 ms (5%) |         |  50.72 KiB (1%) |         678 |
| `["overhead", "default"]`                           |  71.000 μs (5%) |         |  32.77 KiB (1%) |         419 |
| `["overhead", "stoppable=false"]`                   |  69.500 μs (5%) |         |  32.75 KiB (1%) |         418 |
| `["overhead", "stoppable=true"]`                    |  80.301 μs (5%) |         |  44.28 KiB (1%) |         611 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   2.763 ms (5%) |         | 728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   3.349 ms (5%) |         |   1.79 MiB (1%) |         215 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   3.120 ms (5%) |         |   1.42 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  16.809 ms (5%) |         |   1.58 MiB (1%) |        2581 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  24.410 ms (5%) |         |   1.34 MiB (1%) |       10189 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  22.682 ms (5%) |         |   1.27 MiB (1%) |        7731 |
| `["parallel_histogram", "seq"]`                     |   4.875 ms (5%) |         | 364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  34.330 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  18.550 ms (5%) |         |  736 bytes (1%) |          11 |
| `["splitby", "count", "foldl"]`                     |   1.609 ms (5%) |         |                 |             |
| `["splitby", "count", "man"]`                       |   1.250 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    | 812.105 μs (5%) |         |   1.09 KiB (1%) |          19 |
| `["sum", "random", "foldl"]`                        |  13.083 ms (5%) |         |                 |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   6.985 ms (5%) |         |  74.14 KiB (1%) |        1103 |
| `["sum", "random", "reduce", "basesize=256"]`       |   6.850 ms (5%) |         |  36.73 KiB (1%) |         546 |
| `["sum", "random", "reduce", "basesize=512"]`       |   6.587 ms (5%) |         |  18.11 KiB (1%) |         270 |
| `["sum", "uniform", "foldl"]`                       |  13.529 ms (5%) |         |                 |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   6.801 ms (5%) |         |  74.14 KiB (1%) |        1103 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   6.730 ms (5%) |         |  36.73 KiB (1%) |         546 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   6.880 ms (5%) |         |  18.03 KiB (1%) |         268 |
| `["sum", "valley", "foldl"]`                        |  13.009 ms (5%) |         |                 |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   6.789 ms (5%) |         |  74.05 KiB (1%) |        1100 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   6.646 ms (5%) |         |  36.73 KiB (1%) |         546 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   6.630 ms (5%) |         |  18.03 KiB (1%) |         268 |
| `["words", "nthreads=1"]`                           |  29.161 ms (5%) |         |  31.31 MiB (1%) |     1020266 |
| `["words", "nthreads=2"]`                           |  16.912 ms (5%) |         |  31.67 MiB (1%) |     1020305 |
| `["words", "nthreads=4"]`                           |  17.014 ms (5%) |         |  32.38 MiB (1%) |     1020389 |

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
  CPU: Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz: 
              speed         user         nice          sys         idle          irq
       #1  2294 MHz       8396 s          2 s        306 s       4616 s          0 s
       #2  2294 MHz       7023 s          1 s        343 s       5967 s          0 s
       
  Memory: 6.781246185302734 GB (3658.6796875 MB free)
  Uptime: 1339.88 sec
  Load Avg:  1.6  1.56  1.11
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
    CPU MHz:                         2294.683
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
    Vulnerability Mmio stale data:   Vulnerable: Clear CPU buffers attempted, no microcode; SMT Host state unknown
    Vulnerability Retbleed:          Not affected
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

