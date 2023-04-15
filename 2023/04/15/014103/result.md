# Multi-thread benchmark result

* Pull request commit: [`c848a770aa8a51541f28c723acb9b2bd8ee1c009`](https://github.com/JuliaFolds/Transducers.jl/commit/c848a770aa8a51541f28c723acb9b2bd8ee1c009)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/243> (Update */Manifest.toml)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 15 Apr 2023 - 01:35
    - Baseline: 15 Apr 2023 - 01:40
* Package commits:
    - Target: da6383
    - Baseline: f8d0df
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
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 0.77 (5%) :white_check_mark: | 0.81 (1%) :white_check_mark: |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  |                   1.05 (5%)  |                1.06 (1%) :x: |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  |                1.22 (5%) :x: |                1.18 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |                1.14 (5%) :x: |                1.05 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 0.61 (5%) :white_check_mark: | 0.68 (1%) :white_check_mark: |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 0.95 (5%) :white_check_mark: |                1.09 (1%) :x: |
| `["parallel_histogram", "comm", "basesize=16384"]`  | 0.94 (5%) :white_check_mark: | 0.99 (1%) :white_check_mark: |
| `["parallel_histogram", "comm", "basesize=4096"]`   | 0.95 (5%) :white_check_mark: |                1.08 (1%) :x: |
| `["parallel_histogram", "comm", "basesize=8192"]`   | 0.94 (5%) :white_check_mark: | 0.97 (1%) :white_check_mark: |
| `["words", "nthreads=4"]`                           | 0.94 (5%) :white_check_mark: |                   1.00 (1%)  |

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
      Ubuntu 22.04.2 LTS
  uname: Linux 5.15.0-1035-azure #42-Ubuntu SMP Tue Feb 28 19:41:23 UTC 2023 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8370C CPU @ 2.80GHz: 
              speed         user         nice          sys         idle          irq
       #1  2793 MHz       5503 s          0 s        228 s       2538 s          0 s
       #2  2793 MHz       4941 s          0 s        228 s       3091 s          0 s
       
  Memory: 6.781211853027344 GB (3623.8125 MB free)
  Uptime: 831.22 sec
  Load Avg:  1.62  1.5  0.91
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
      Ubuntu 22.04.2 LTS
  uname: Linux 5.15.0-1035-azure #42-Ubuntu SMP Tue Feb 28 19:41:23 UTC 2023 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8370C CPU @ 2.80GHz: 
              speed         user         nice          sys         idle          irq
       #1  2793 MHz       7867 s          0 s        289 s       3174 s          0 s
       #2  2793 MHz       7335 s          0 s        287 s       3701 s          0 s
       
  Memory: 6.781211853027344 GB (3574.73046875 MB free)
  Uptime: 1137.67 sec
  Load Avg:  1.59  1.57  1.11
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, icelake-server)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 15 Apr 2023 - 1:35
* Package commit: da6383
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
| `["collect", "assoc", "basesize=1"]`                | 279.417 ms (5%) |         |  25.97 MiB (1%) |      306809 |
| `["collect", "assoc", "basesize=1024"]`             | 239.233 ms (5%) |         |   2.61 MiB (1%) |         456 |
| `["collect", "assoc", "basesize=32"]`               | 241.416 ms (5%) |         |   4.82 MiB (1%) |       11700 |
| `["collect", "seq"]`                                | 477.746 ms (5%) |         | 812.73 KiB (1%) |          11 |
| `["collect", "unordered", "basesize=1"]`            | 366.817 ms (5%) |         |  23.91 MiB (1%) |      413370 |
| `["collect", "unordered", "basesize=1024"]`         | 250.237 ms (5%) |         |   1.01 MiB (1%) |         975 |
| `["collect", "unordered", "basesize=32"]`           | 260.694 ms (5%) |         |   1.59 MiB (1%) |       15065 |
| `["findfirst", "n=1000", "foldl"]`                  | 735.202 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 403.757 ms (5%) |         | 232.86 KiB (1%) |        3276 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 501.500 ms (5%) |         | 157.23 KiB (1%) |        2194 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 676.581 ms (5%) |         | 103.56 KiB (1%) |        1455 |
| `["findfirst", "n=400", "foldl"]`                   | 551.299 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 303.108 ms (5%) |         | 404.03 KiB (1%) |        5735 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 290.515 ms (5%) |         | 200.86 KiB (1%) |        2873 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 404.483 ms (5%) |         | 145.50 KiB (1%) |        2067 |
| `["findfirst", "n=500", "foldl"]`                   |  95.500 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 191.123 ms (5%) |         | 226.44 KiB (1%) |        3126 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 163.963 ms (5%) |         | 116.34 KiB (1%) |        1596 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 143.128 ms (5%) |         |  63.67 KiB (1%) |         866 |
| `["overhead", "default"]`                           |  71.899 μs (5%) |         |  32.70 KiB (1%) |         417 |
| `["overhead", "stoppable=false"]`                   |  69.300 μs (5%) |         |  32.72 KiB (1%) |         417 |
| `["overhead", "stoppable=true"]`                    |  79.699 μs (5%) |         |  44.25 KiB (1%) |         610 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   3.762 ms (5%) |         | 728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   4.485 ms (5%) |         |   1.79 MiB (1%) |         216 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   4.097 ms (5%) |         |   1.42 MiB (1%) |         118 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  14.164 ms (5%) |         |   1.65 MiB (1%) |        4762 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  23.247 ms (5%) |         |   1.34 MiB (1%) |        9950 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  19.767 ms (5%) |         |   1.30 MiB (1%) |        3813 |
| `["parallel_histogram", "seq"]`                     |   6.631 ms (5%) |         | 364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  41.193 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  20.595 ms (5%) |         |  736 bytes (1%) |          11 |
| `["splitby", "count", "foldl"]`                     |   2.304 ms (5%) |         |                 |             |
| `["splitby", "count", "man"]`                       |   1.527 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    |   1.128 ms (5%) |         |   1.06 KiB (1%) |          18 |
| `["sum", "random", "foldl"]`                        |  18.099 ms (5%) |         |                 |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   9.242 ms (5%) |         |  74.14 KiB (1%) |        1103 |
| `["sum", "random", "reduce", "basesize=256"]`       |   9.158 ms (5%) |         |  36.73 KiB (1%) |         546 |
| `["sum", "random", "reduce", "basesize=512"]`       |   9.106 ms (5%) |         |  18.08 KiB (1%) |         269 |
| `["sum", "uniform", "foldl"]`                       |  17.725 ms (5%) |         |                 |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   9.056 ms (5%) |         |  74.14 KiB (1%) |        1103 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   8.953 ms (5%) |         |  36.73 KiB (1%) |         546 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   8.911 ms (5%) |         |  18.00 KiB (1%) |         267 |
| `["sum", "valley", "foldl"]`                        |  18.139 ms (5%) |         |                 |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   9.252 ms (5%) |         |  74.11 KiB (1%) |        1102 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   9.193 ms (5%) |         |  36.70 KiB (1%) |         545 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   9.184 ms (5%) |         |  18.00 KiB (1%) |         267 |
| `["words", "nthreads=1"]`                           |  18.091 ms (5%) |         |  31.59 MiB (1%) |     1029319 |
| `["words", "nthreads=2"]`                           |  12.293 ms (5%) |         |  32.31 MiB (1%) |     1029392 |
| `["words", "nthreads=4"]`                           |  12.527 ms (5%) |         |  32.75 MiB (1%) |     1029459 |

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
      Ubuntu 22.04.2 LTS
  uname: Linux 5.15.0-1035-azure #42-Ubuntu SMP Tue Feb 28 19:41:23 UTC 2023 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8370C CPU @ 2.80GHz: 
              speed         user         nice          sys         idle          irq
       #1  2793 MHz       5503 s          0 s        228 s       2538 s          0 s
       #2  2793 MHz       4941 s          0 s        228 s       3091 s          0 s
       
  Memory: 6.781211853027344 GB (3623.8125 MB free)
  Uptime: 831.22 sec
  Load Avg:  1.62  1.5  0.91
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, icelake-server)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 15 Apr 2023 - 1:40
* Package commit: f8d0df
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
| `["collect", "assoc", "basesize=1"]`                | 278.729 ms (5%) |         |  25.97 MiB (1%) |      306790 |
| `["collect", "assoc", "basesize=1024"]`             | 239.303 ms (5%) |         |   2.61 MiB (1%) |         455 |
| `["collect", "assoc", "basesize=32"]`               | 240.468 ms (5%) |         |   4.82 MiB (1%) |       11709 |
| `["collect", "seq"]`                                | 476.532 ms (5%) |         | 812.73 KiB (1%) |          11 |
| `["collect", "unordered", "basesize=1"]`            | 370.204 ms (5%) |         |  23.94 MiB (1%) |      414173 |
| `["collect", "unordered", "basesize=1024"]`         | 250.260 ms (5%) |         |   1.01 MiB (1%) |         960 |
| `["collect", "unordered", "basesize=32"]`           | 260.687 ms (5%) |         |   1.59 MiB (1%) |       14868 |
| `["findfirst", "n=1000", "foldl"]`                  | 738.635 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 404.611 ms (5%) |         | 232.89 KiB (1%) |        3277 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 497.508 ms (5%) |         | 157.20 KiB (1%) |        2193 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 877.686 ms (5%) |         | 127.69 KiB (1%) |        1809 |
| `["findfirst", "n=400", "foldl"]`                   | 553.092 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 288.756 ms (5%) |         | 382.61 KiB (1%) |        5435 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 289.243 ms (5%) |         | 199.97 KiB (1%) |        2859 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 332.591 ms (5%) |         | 122.98 KiB (1%) |        1753 |
| `["findfirst", "n=500", "foldl"]`                   |  95.825 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 167.766 ms (5%) |         | 216.48 KiB (1%) |        2952 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 269.167 ms (5%) |         | 169.88 KiB (1%) |        2359 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 150.987 ms (5%) |         |  58.44 KiB (1%) |         801 |
| `["overhead", "default"]`                           |  72.999 μs (5%) |         |  32.77 KiB (1%) |         419 |
| `["overhead", "stoppable=false"]`                   |  68.899 μs (5%) |         |  32.75 KiB (1%) |         418 |
| `["overhead", "stoppable=true"]`                    |  82.199 μs (5%) |         |  44.22 KiB (1%) |         609 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   3.713 ms (5%) |         | 728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   4.484 ms (5%) |         |   1.79 MiB (1%) |         216 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   4.102 ms (5%) |         |   1.42 MiB (1%) |         118 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  15.072 ms (5%) |         |   1.67 MiB (1%) |        5310 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  24.553 ms (5%) |         |   1.24 MiB (1%) |        6804 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  21.023 ms (5%) |         |   1.34 MiB (1%) |        9032 |
| `["parallel_histogram", "seq"]`                     |   6.652 ms (5%) |         | 364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  41.188 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  20.595 ms (5%) |         |  736 bytes (1%) |          11 |
| `["splitby", "count", "foldl"]`                     |   2.300 ms (5%) |         |                 |             |
| `["splitby", "count", "man"]`                       |   1.529 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    |   1.148 ms (5%) |         |   1.06 KiB (1%) |          18 |
| `["sum", "random", "foldl"]`                        |  17.869 ms (5%) |         |                 |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   9.131 ms (5%) |         |  74.14 KiB (1%) |        1103 |
| `["sum", "random", "reduce", "basesize=256"]`       |   9.035 ms (5%) |         |  36.73 KiB (1%) |         546 |
| `["sum", "random", "reduce", "basesize=512"]`       |   8.987 ms (5%) |         |  18.11 KiB (1%) |         270 |
| `["sum", "uniform", "foldl"]`                       |  17.731 ms (5%) |         |                 |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   9.055 ms (5%) |         |  74.20 KiB (1%) |        1105 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   8.962 ms (5%) |         |  36.73 KiB (1%) |         546 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   8.910 ms (5%) |         |  18.03 KiB (1%) |         268 |
| `["sum", "valley", "foldl"]`                        |  18.144 ms (5%) |         |                 |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   9.270 ms (5%) |         |  74.11 KiB (1%) |        1102 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   9.173 ms (5%) |         |  36.70 KiB (1%) |         545 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   9.161 ms (5%) |         |  18.00 KiB (1%) |         267 |
| `["words", "nthreads=1"]`                           |  18.384 ms (5%) |         |  31.67 MiB (1%) |     1031576 |
| `["words", "nthreads=2"]`                           |  12.297 ms (5%) |         |  32.02 MiB (1%) |     1031645 |
| `["words", "nthreads=4"]`                           |  13.323 ms (5%) |         |  32.74 MiB (1%) |     1031751 |

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
      Ubuntu 22.04.2 LTS
  uname: Linux 5.15.0-1035-azure #42-Ubuntu SMP Tue Feb 28 19:41:23 UTC 2023 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8370C CPU @ 2.80GHz: 
              speed         user         nice          sys         idle          irq
       #1  2793 MHz       7867 s          0 s        289 s       3174 s          0 s
       #2  2793 MHz       7335 s          0 s        287 s       3701 s          0 s
       
  Memory: 6.781211853027344 GB (3574.73046875 MB free)
  Uptime: 1137.67 sec
  Load Avg:  1.59  1.57  1.11
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
    Address sizes:                   46 bits physical, 48 bits virtual
    Byte Order:                      Little Endian
    CPU(s):                          2
    On-line CPU(s) list:             0,1
    Vendor ID:                       GenuineIntel
    Model name:                      Intel(R) Xeon(R) Platinum 8370C CPU @ 2.80GHz
    CPU family:                      6
    Model:                           106
    Thread(s) per core:              1
    Core(s) per socket:              2
    Socket(s):                       1
    Stepping:                        6
    BogoMIPS:                        5586.87
    Flags:                           fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush mmx fxsr sse sse2 ss ht syscall nx pdpe1gb rdtscp lm constant_tsc rep_good nopl xtopology cpuid pni pclmulqdq ssse3 fma cx16 pcid sse4_1 sse4_2 movbe popcnt aes xsave avx f16c rdrand hypervisor lahf_lm abm 3dnowprefetch invpcid_single pti fsgsbase bmi1 hle avx2 smep bmi2 erms invpcid rtm avx512f avx512dq rdseed adx smap clflushopt avx512cd avx512bw avx512vl xsaveopt xsavec xsaves md_clear
    Hypervisor vendor:               Microsoft
    Virtualization type:             full
    L1d cache:                       96 KiB (2 instances)
    L1i cache:                       64 KiB (2 instances)
    L2 cache:                        2.5 MiB (2 instances)
    L3 cache:                        48 MiB (1 instance)
    NUMA node(s):                    1
    NUMA node0 CPU(s):               0,1
    Vulnerability Itlb multihit:     KVM: Mitigation: VMX unsupported
    Vulnerability L1tf:              Mitigation; PTE Inversion
    Vulnerability Mds:               Mitigation; Clear CPU buffers; SMT Host state unknown
    Vulnerability Meltdown:          Mitigation; PTI
    Vulnerability Mmio stale data:   Vulnerable: Clear CPU buffers attempted, no microcode; SMT Host state unknown
    Vulnerability Retbleed:          Not affected
    Vulnerability Spec store bypass: Vulnerable
    Vulnerability Spectre v1:        Mitigation; usercopy/swapgs barriers and __user pointer sanitization
    Vulnerability Spectre v2:        Mitigation; Retpolines, STIBP disabled, RSB filling, PBRSB-eIBRS Not affected
    Vulnerability Srbds:             Not affected
    Vulnerability Tsx async abort:   Mitigation; Clear CPU buffers; SMT Host state unknown
    

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

