# Multi-thread benchmark result

* Pull request commit: [`bd8502e71c76debca8519fc2cdd2999f2cb70a32`](https://github.com/JuliaFolds/Transducers.jl/commit/bd8502e71c76debca8519fc2cdd2999f2cb70a32)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/243> (Update */Manifest.toml)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 7 Dec 2024 - 01:59
    - Baseline: 7 Dec 2024 - 02:04
* Package commits:
    - Target: bcdf76
    - Baseline: 2a51f8
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
| `["findfirst", "n=1000", "reduce", "basesize=256"]` |                1.08 (5%) :x: |                1.08 (1%) :x: |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 0.87 (5%) :white_check_mark: | 0.89 (1%) :white_check_mark: |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  |                1.23 (5%) :x: |                1.27 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 0.58 (5%) :white_check_mark: | 0.64 (1%) :white_check_mark: |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |                   1.02 (5%)  |                1.15 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |                1.40 (5%) :x: |                1.29 (1%) :x: |
| `["parallel_histogram", "comm", "basesize=16384"]`  |                   1.03 (5%)  |                1.01 (1%) :x: |
| `["parallel_histogram", "comm", "basesize=4096"]`   |                1.05 (5%) :x: |                   1.01 (1%)  |
| `["partition_length_maximum", "rand", "reduce"]`    |                   1.00 (5%)  |                1.05 (1%) :x: |
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
Julia Version 1.7.3
Commit 742b9abb4d (2022-05-06 12:58 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 22.04.5 LTS
  uname: Linux 6.5.0-1025-azure #26~22.04.1-Ubuntu SMP Thu Jul 11 22:33:04 UTC 2024 x86_64 x86_64
  CPU: AMD EPYC 7763 64-Core Processor: 
              speed         user         nice          sys         idle          irq
       #1  3219 MHz       2125 s          0 s        157 s       5280 s          0 s
       #2  2591 MHz       2425 s          0 s        162 s       4976 s          0 s
       #3  3241 MHz       2874 s          0 s        163 s       4537 s          0 s
       #4  2445 MHz       2560 s          0 s        174 s       4836 s          0 s
       
  Memory: 15.606491088867188 GB (12454.66015625 MB free)
  Uptime: 760.02 sec
  Load Avg:  1.71  1.55  0.92
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, znver3)
```

### Baseline
```
Julia Version 1.7.3
Commit 742b9abb4d (2022-05-06 12:58 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 22.04.5 LTS
  uname: Linux 6.5.0-1025-azure #26~22.04.1-Ubuntu SMP Thu Jul 11 22:33:04 UTC 2024 x86_64 x86_64
  CPU: AMD EPYC 7763 64-Core Processor: 
              speed         user         nice          sys         idle          irq
       #1  2445 MHz       3278 s          0 s        210 s       6981 s          0 s
       #2  3241 MHz       3926 s          0 s        211 s       6334 s          0 s
       #3  3113 MHz       3833 s          0 s        214 s       6434 s          0 s
       #4  3137 MHz       3537 s          0 s        226 s       6714 s          0 s
       
  Memory: 15.606491088867188 GB (12386.58203125 MB free)
  Uptime: 1051.34 sec
  Load Avg:  1.72  1.63  1.13
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, znver3)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 7 Dec 2024 - 1:59
* Package commit: bcdf76
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
| `["collect", "assoc", "basesize=1"]`                | 148.861 ms (5%) |         |   4.36 MiB (1%) |       32800 |
| `["collect", "assoc", "basesize=1024"]`             | 147.420 ms (5%) |         |   1.09 MiB (1%) |          53 |
| `["collect", "assoc", "basesize=32"]`               | 147.589 ms (5%) |         |   1.48 MiB (1%) |        1052 |
| `["collect", "seq"]`                                | 294.648 ms (5%) |         | 256.05 KiB (1%) |           2 |
| `["collect", "unordered", "basesize=1"]`            | 246.461 ms (5%) |         |  23.83 MiB (1%) |      410597 |
| `["collect", "unordered", "basesize=1024"]`         | 156.159 ms (5%) |         |   1.01 MiB (1%) |        1003 |
| `["collect", "unordered", "basesize=32"]`           | 163.129 ms (5%) |         |   1.60 MiB (1%) |       15207 |
| `["findfirst", "n=1000", "foldl"]`                  | 505.645 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 274.845 ms (5%) |         | 232.64 KiB (1%) |        3269 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 396.317 ms (5%) |         | 173.20 KiB (1%) |        2435 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 394.567 ms (5%) |         |  96.84 KiB (1%) |        1349 |
| `["findfirst", "n=400", "foldl"]`                   | 379.098 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 198.375 ms (5%) |         | 390.67 KiB (1%) |        5546 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 196.750 ms (5%) |         | 199.97 KiB (1%) |        2859 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 270.768 ms (5%) |         | 142.55 KiB (1%) |        2034 |
| `["findfirst", "n=500", "foldl"]`                   |  64.841 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |  81.986 ms (5%) |         | 164.22 KiB (1%) |        2239 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 134.697 ms (5%) |         | 144.06 KiB (1%) |        1967 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  93.718 ms (5%) |         |  63.66 KiB (1%) |         865 |
| `["overhead", "default"]`                           |  52.448 μs (5%) |         |  32.73 KiB (1%) |         418 |
| `["overhead", "stoppable=false"]`                   |  52.829 μs (5%) |         |  32.78 KiB (1%) |         419 |
| `["overhead", "stoppable=true"]`                    |  61.044 μs (5%) |         |  44.25 KiB (1%) |         610 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   2.390 ms (5%) |         | 728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   2.948 ms (5%) |         |   1.79 MiB (1%) |         216 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   2.657 ms (5%) |         |   1.42 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |   8.706 ms (5%) |         |   1.60 MiB (1%) |        2976 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  14.023 ms (5%) |         |   1.37 MiB (1%) |       10923 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  12.288 ms (5%) |         |   1.27 MiB (1%) |        7623 |
| `["parallel_histogram", "seq"]`                     |   4.244 ms (5%) |         | 364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  31.116 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  15.571 ms (5%) |         |  736 bytes (1%) |          11 |
| `["splitby", "count", "foldl"]`                     |   1.502 ms (5%) |         |                 |             |
| `["splitby", "count", "man"]`                       |   1.158 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    | 721.387 μs (5%) |         | 1008 bytes (1%) |          18 |
| `["sum", "random", "foldl"]`                        |  10.994 ms (5%) |         |                 |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   5.636 ms (5%) |         |  74.20 KiB (1%) |        1105 |
| `["sum", "random", "reduce", "basesize=256"]`       |   5.574 ms (5%) |         |  36.70 KiB (1%) |         545 |
| `["sum", "random", "reduce", "basesize=512"]`       |   5.542 ms (5%) |         |  18.14 KiB (1%) |         271 |
| `["sum", "uniform", "foldl"]`                       |  10.880 ms (5%) |         |                 |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   5.571 ms (5%) |         |  74.11 KiB (1%) |        1102 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   5.505 ms (5%) |         |  36.73 KiB (1%) |         546 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   5.466 ms (5%) |         |  18.03 KiB (1%) |         268 |
| `["sum", "valley", "foldl"]`                        |  11.111 ms (5%) |         |                 |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   5.698 ms (5%) |         |  74.08 KiB (1%) |        1101 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   5.638 ms (5%) |         |  36.70 KiB (1%) |         545 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   5.605 ms (5%) |         |  18.06 KiB (1%) |         269 |
| `["words", "nthreads=1"]`                           |  14.413 ms (5%) |         |  31.66 MiB (1%) |     1031607 |
| `["words", "nthreads=2"]`                           |   9.500 ms (5%) |         |  32.38 MiB (1%) |     1031685 |
| `["words", "nthreads=4"]`                           |   9.794 ms (5%) |         |  32.83 MiB (1%) |     1031756 |

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
      Ubuntu 22.04.5 LTS
  uname: Linux 6.5.0-1025-azure #26~22.04.1-Ubuntu SMP Thu Jul 11 22:33:04 UTC 2024 x86_64 x86_64
  CPU: AMD EPYC 7763 64-Core Processor: 
              speed         user         nice          sys         idle          irq
       #1  3219 MHz       2125 s          0 s        157 s       5280 s          0 s
       #2  2591 MHz       2425 s          0 s        162 s       4976 s          0 s
       #3  3241 MHz       2874 s          0 s        163 s       4537 s          0 s
       #4  2445 MHz       2560 s          0 s        174 s       4836 s          0 s
       
  Memory: 15.606491088867188 GB (12454.66015625 MB free)
  Uptime: 760.02 sec
  Load Avg:  1.71  1.55  0.92
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, znver3)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 7 Dec 2024 - 2:4
* Package commit: 2a51f8
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
| `["collect", "assoc", "basesize=1"]`                | 149.099 ms (5%) |         |   4.36 MiB (1%) |       32800 |
| `["collect", "assoc", "basesize=1024"]`             | 147.628 ms (5%) |         |   1.09 MiB (1%) |          53 |
| `["collect", "assoc", "basesize=32"]`               | 147.580 ms (5%) |         |   1.48 MiB (1%) |        1052 |
| `["collect", "seq"]`                                | 294.727 ms (5%) |         | 256.05 KiB (1%) |           2 |
| `["collect", "unordered", "basesize=1"]`            | 244.357 ms (5%) |         |  23.80 MiB (1%) |      409839 |
| `["collect", "unordered", "basesize=1024"]`         | 156.317 ms (5%) |         |   1.01 MiB (1%) |        1026 |
| `["collect", "unordered", "basesize=32"]`           | 163.432 ms (5%) |         |   1.60 MiB (1%) |       15213 |
| `["findfirst", "n=1000", "foldl"]`                  | 506.848 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 276.068 ms (5%) |         | 232.73 KiB (1%) |        3272 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 367.680 ms (5%) |         | 160.23 KiB (1%) |        2255 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 454.560 ms (5%) |         | 108.73 KiB (1%) |        1515 |
| `["findfirst", "n=400", "foldl"]`                   | 379.130 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 200.399 ms (5%) |         | 389.75 KiB (1%) |        5547 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 198.930 ms (5%) |         | 200.86 KiB (1%) |        2873 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 220.236 ms (5%) |         | 112.59 KiB (1%) |        1622 |
| `["findfirst", "n=500", "foldl"]`                   |  65.018 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 141.726 ms (5%) |         | 258.12 KiB (1%) |        3562 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 131.673 ms (5%) |         | 125.00 KiB (1%) |        1735 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  67.179 ms (5%) |         |  49.44 KiB (1%) |         664 |
| `["overhead", "default"]`                           |  53.020 μs (5%) |         |  32.73 KiB (1%) |         418 |
| `["overhead", "stoppable=false"]`                   |  52.579 μs (5%) |         |  32.75 KiB (1%) |         418 |
| `["overhead", "stoppable=true"]`                    |  59.491 μs (5%) |         |  44.28 KiB (1%) |         611 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   2.399 ms (5%) |         | 728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   2.923 ms (5%) |         |   1.79 MiB (1%) |         216 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   2.658 ms (5%) |         |   1.42 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |   8.458 ms (5%) |         |   1.58 MiB (1%) |        2287 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  13.314 ms (5%) |         |   1.36 MiB (1%) |       10698 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  12.148 ms (5%) |         |   1.28 MiB (1%) |        8037 |
| `["parallel_histogram", "seq"]`                     |   4.241 ms (5%) |         | 364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  31.113 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  15.575 ms (5%) |         |  704 bytes (1%) |          10 |
| `["splitby", "count", "foldl"]`                     |   1.480 ms (5%) |         |                 |             |
| `["splitby", "count", "man"]`                       |   1.157 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    | 720.045 μs (5%) |         |   1.06 KiB (1%) |          18 |
| `["sum", "random", "foldl"]`                        |  10.994 ms (5%) |         |                 |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   5.599 ms (5%) |         |  74.14 KiB (1%) |        1103 |
| `["sum", "random", "reduce", "basesize=256"]`       |   5.574 ms (5%) |         |  36.73 KiB (1%) |         546 |
| `["sum", "random", "reduce", "basesize=512"]`       |   5.531 ms (5%) |         |  18.11 KiB (1%) |         270 |
| `["sum", "uniform", "foldl"]`                       |  10.862 ms (5%) |         |                 |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   5.577 ms (5%) |         |  74.17 KiB (1%) |        1104 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   5.517 ms (5%) |         |  36.73 KiB (1%) |         546 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   5.480 ms (5%) |         |  18.00 KiB (1%) |         267 |
| `["sum", "valley", "foldl"]`                        |  11.105 ms (5%) |         |                 |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   5.699 ms (5%) |         |  74.05 KiB (1%) |        1100 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   5.630 ms (5%) |         |  36.70 KiB (1%) |         545 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   5.609 ms (5%) |         |  18.06 KiB (1%) |         269 |
| `["words", "nthreads=1"]`                           |  14.649 ms (5%) |         |  31.83 MiB (1%) |     1037225 |
| `["words", "nthreads=2"]`                           |   9.703 ms (5%) |         |  32.54 MiB (1%) |     1037298 |
| `["words", "nthreads=4"]`                           |   9.674 ms (5%) |         |  32.99 MiB (1%) |     1037378 |

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
      Ubuntu 22.04.5 LTS
  uname: Linux 6.5.0-1025-azure #26~22.04.1-Ubuntu SMP Thu Jul 11 22:33:04 UTC 2024 x86_64 x86_64
  CPU: AMD EPYC 7763 64-Core Processor: 
              speed         user         nice          sys         idle          irq
       #1  2445 MHz       3278 s          0 s        210 s       6981 s          0 s
       #2  3241 MHz       3926 s          0 s        211 s       6334 s          0 s
       #3  3113 MHz       3833 s          0 s        214 s       6434 s          0 s
       #4  3137 MHz       3537 s          0 s        226 s       6714 s          0 s
       
  Memory: 15.606491088867188 GB (12386.58203125 MB free)
  Uptime: 1051.34 sec
  Load Avg:  1.72  1.63  1.13
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, znver3)
```

---
# Runtime information
| Runtime Info | |
|:--|:--|
| BLAS #threads | 4 |
| `BLAS.vendor()` | `openblas64` |
| `Sys.CPU_THREADS` | 4 |

`lscpu` output:

    Architecture:                       x86_64
    CPU op-mode(s):                     32-bit, 64-bit
    Address sizes:                      48 bits physical, 48 bits virtual
    Byte Order:                         Little Endian
    CPU(s):                             4
    On-line CPU(s) list:                0-3
    Vendor ID:                          AuthenticAMD
    Model name:                         AMD EPYC 7763 64-Core Processor
    CPU family:                         25
    Model:                              1
    Thread(s) per core:                 2
    Core(s) per socket:                 2
    Socket(s):                          1
    Stepping:                           1
    BogoMIPS:                           4890.85
    Flags:                              fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush mmx fxsr sse sse2 ht syscall nx mmxext fxsr_opt pdpe1gb rdtscp lm constant_tsc rep_good nopl tsc_reliable nonstop_tsc cpuid extd_apicid aperfmperf pni pclmulqdq ssse3 fma cx16 pcid sse4_1 sse4_2 movbe popcnt aes xsave avx f16c rdrand hypervisor lahf_lm cmp_legacy svm cr8_legacy abm sse4a misalignsse 3dnowprefetch osvw topoext invpcid_single vmmcall fsgsbase bmi1 avx2 smep bmi2 erms invpcid rdseed adx smap clflushopt clwb sha_ni xsaveopt xsavec xgetbv1 xsaves clzero xsaveerptr rdpru arat npt nrip_save tsc_scale vmcb_clean flushbyasid decodeassists pausefilter pfthreshold v_vmsave_vmload umip vaes vpclmulqdq rdpid fsrm
    Virtualization:                     AMD-V
    Hypervisor vendor:                  Microsoft
    Virtualization type:                full
    L1d cache:                          64 KiB (2 instances)
    L1i cache:                          64 KiB (2 instances)
    L2 cache:                           1 MiB (2 instances)
    L3 cache:                           32 MiB (1 instance)
    NUMA node(s):                       1
    NUMA node0 CPU(s):                  0-3
    Vulnerability Gather data sampling: Not affected
    Vulnerability Itlb multihit:        Not affected
    Vulnerability L1tf:                 Not affected
    Vulnerability Mds:                  Not affected
    Vulnerability Meltdown:             Not affected
    Vulnerability Mmio stale data:      Not affected
    Vulnerability Retbleed:             Not affected
    Vulnerability Spec rstack overflow: Vulnerable: Safe RET, no microcode
    Vulnerability Spec store bypass:    Vulnerable
    Vulnerability Spectre v1:           Mitigation; usercopy/swapgs barriers and __user pointer sanitization
    Vulnerability Spectre v2:           Mitigation; Retpolines; STIBP disabled; RSB filling; PBRSB-eIBRS Not affected; BHI Not affected
    Vulnerability Srbds:                Not affected
    Vulnerability Tsx async abort:      Not affected
    

| Cpu Property       | Value                                                      |
|:------------------ |:---------------------------------------------------------- |
| Brand              | AMD EPYC 7763 64-Core Processor                            |
| Vendor             | :AMD                                                       |
| Architecture       | :Unknown                                                   |
| Model              | Family: 0xaf, Model: 0x01, Stepping: 0x01, Type: 0x00      |
| Cores              | 16 physical cores, 16 logical cores (on executing CPU)     |
|                    | No Hyperthreading hardware capability detected             |
| Clock Frequencies  | Not supported by CPU                                       |
| Data Cache         | Level 1:3 : (32, 512, 32768) kbytes                        |
|                    | 64 byte cache line size                                    |
| Address Size       | 48 bits virtual, 48 bits physical                          |
| SIMD               | 256 bit = 32 byte max. SIMD vector size                    |
| Time Stamp Counter | TSC is accessible via `rdtsc`                              |
|                    | TSC runs at constant rate (invariant from clock frequency) |
| Perf. Monitoring   | Performance Monitoring Counters (PMC) are not supported    |
| Hypervisor         | Yes, Microsoft                                             |

