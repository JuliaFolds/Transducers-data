# Multi-thread benchmark result

* Pull request commit: [`bbdc24dfa19b27704f726200f6a3b1dbd807fa35`](https://github.com/JuliaFolds/Transducers.jl/commit/bbdc24dfa19b27704f726200f6a3b1dbd807fa35)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/243> (Update */Manifest.toml)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 18 Jan 2025 - 01:46
    - Baseline: 18 Jan 2025 - 01:51
* Package commits:
    - Target: a299d8
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
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 0.85 (5%) :white_check_mark: | 0.91 (1%) :white_check_mark: |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 0.79 (5%) :white_check_mark: | 0.77 (1%) :white_check_mark: |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  |                   1.04 (5%)  |                1.08 (1%) :x: |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  |                   1.04 (5%)  |                1.06 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |                1.56 (5%) :x: |                1.55 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |                1.06 (5%) :x: |                1.17 (1%) :x: |
| `["overhead", "stoppable=false"]`                   |                1.06 (5%) :x: |                   1.00 (1%)  |
| `["parallel_histogram", "comm", "basesize=4096"]`   |                   0.99 (5%)  | 0.98 (1%) :white_check_mark: |
| `["parallel_histogram", "comm", "basesize=8192"]`   |                   1.00 (5%)  | 0.98 (1%) :white_check_mark: |
| `["splitby", "count", "reduce"]`                    | 0.84 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["words", "nthreads=2"]`                           | 0.95 (5%) :white_check_mark: |                1.02 (1%) :x: |
| `["words", "nthreads=4"]`                           | 0.89 (5%) :white_check_mark: |                   1.00 (1%)  |

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
      Ubuntu 24.04.1 LTS
  uname: Linux 6.8.0-1017-azure #20-Ubuntu SMP Tue Oct 22 03:43:13 UTC 2024 x86_64 x86_64
  CPU: AMD EPYC 7763 64-Core Processor: 
              speed         user         nice          sys         idle          irq
       #1  3240 MHz       2651 s          0 s        186 s       4201 s          0 s
       #2  3185 MHz       2798 s          0 s        228 s       3981 s          0 s
       #3  3250 MHz       2164 s          0 s        196 s       4640 s          0 s
       #4  3245 MHz       2482 s          0 s        207 s       4302 s          0 s
       
  Memory: 15.615280151367188 GB (8621.11328125 MB free)
  Uptime: 709.6 sec
  Load Avg:  1.68  1.56  0.97
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
      Ubuntu 24.04.1 LTS
  uname: Linux 6.8.0-1017-azure #20-Ubuntu SMP Tue Oct 22 03:43:13 UTC 2024 x86_64 x86_64
  CPU: AMD EPYC 7763 64-Core Processor: 
              speed         user         nice          sys         idle          irq
       #1  3245 MHz       3621 s          0 s        261 s       6221 s          0 s
       #2  3245 MHz       4283 s          0 s        322 s       5469 s          0 s
       #3  3242 MHz       3349 s          0 s        255 s       6462 s          0 s
       #4  3241 MHz       3600 s          0 s        274 s       6184 s          0 s
       
  Memory: 15.615280151367188 GB (8581.71875 MB free)
  Uptime: 1016.77 sec
  Load Avg:  1.67  1.68  1.2
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, znver3)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 18 Jan 2025 - 1:46
* Package commit: a299d8
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
| `["collect", "assoc", "basesize=1"]`                | 149.391 ms (5%) |         |   4.36 MiB (1%) |       32800 |
| `["collect", "assoc", "basesize=1024"]`             | 148.203 ms (5%) |         |   1.09 MiB (1%) |          53 |
| `["collect", "assoc", "basesize=32"]`               | 148.342 ms (5%) |         |   1.48 MiB (1%) |        1052 |
| `["collect", "seq"]`                                | 296.057 ms (5%) |         | 256.05 KiB (1%) |           2 |
| `["collect", "unordered", "basesize=1"]`            | 246.445 ms (5%) |         |  23.69 MiB (1%) |      406143 |
| `["collect", "unordered", "basesize=1024"]`         | 158.283 ms (5%) |         |   1.01 MiB (1%) |        1048 |
| `["collect", "unordered", "basesize=32"]`           | 170.676 ms (5%) |         |   1.61 MiB (1%) |       15496 |
| `["findfirst", "n=1000", "foldl"]`                  | 508.667 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 277.381 ms (5%) |         | 232.70 KiB (1%) |        3271 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 340.146 ms (5%) |         | 157.20 KiB (1%) |        2193 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 360.239 ms (5%) |         |  83.05 KiB (1%) |        1172 |
| `["findfirst", "n=400", "foldl"]`                   | 380.449 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 201.539 ms (5%) |         | 404.48 KiB (1%) |        5722 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 206.794 ms (5%) |         | 213.47 KiB (1%) |        3041 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 220.772 ms (5%) |         | 112.59 KiB (1%) |        1622 |
| `["findfirst", "n=500", "foldl"]`                   |  65.855 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 116.102 ms (5%) |         | 211.09 KiB (1%) |        2902 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |  98.932 ms (5%) |         | 114.02 KiB (1%) |        1547 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  85.482 ms (5%) |         |  56.83 KiB (1%) |         778 |
| `["overhead", "default"]`                           |  51.025 μs (5%) |         |  32.73 KiB (1%) |         418 |
| `["overhead", "stoppable=false"]`                   |  53.981 μs (5%) |         |  32.75 KiB (1%) |         418 |
| `["overhead", "stoppable=true"]`                    |  59.000 μs (5%) |         |  44.22 KiB (1%) |         609 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   2.401 ms (5%) |         | 728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   2.952 ms (5%) |         |   1.79 MiB (1%) |         216 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   2.680 ms (5%) |         |   1.42 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |   7.928 ms (5%) |         |   1.56 MiB (1%) |        1634 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  12.301 ms (5%) |         |   1.30 MiB (1%) |        8635 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  11.808 ms (5%) |         |   1.26 MiB (1%) |        7223 |
| `["parallel_histogram", "seq"]`                     |   4.268 ms (5%) |         | 364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  31.310 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  15.692 ms (5%) |         |  736 bytes (1%) |          11 |
| `["splitby", "count", "foldl"]`                     |   1.511 ms (5%) |         |                 |             |
| `["splitby", "count", "man"]`                       |   1.166 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    | 720.368 μs (5%) |         |   1.06 KiB (1%) |          18 |
| `["sum", "random", "foldl"]`                        |  11.020 ms (5%) |         |                 |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   5.648 ms (5%) |         |  74.22 KiB (1%) |        1105 |
| `["sum", "random", "reduce", "basesize=256"]`       |   5.593 ms (5%) |         |  36.78 KiB (1%) |         547 |
| `["sum", "random", "reduce", "basesize=512"]`       |   5.551 ms (5%) |         |  18.11 KiB (1%) |         270 |
| `["sum", "uniform", "foldl"]`                       |  10.937 ms (5%) |         |                 |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   5.594 ms (5%) |         |  74.19 KiB (1%) |        1104 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   5.533 ms (5%) |         |  36.78 KiB (1%) |         547 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   5.493 ms (5%) |         |  18.08 KiB (1%) |         269 |
| `["sum", "valley", "foldl"]`                        |  11.170 ms (5%) |         |                 |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   5.722 ms (5%) |         |  74.16 KiB (1%) |        1103 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   5.667 ms (5%) |         |  36.75 KiB (1%) |         546 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   5.627 ms (5%) |         |  18.08 KiB (1%) |         269 |
| `["words", "nthreads=1"]`                           |  14.954 ms (5%) |         |  31.74 MiB (1%) |     1034077 |
| `["words", "nthreads=2"]`                           |   9.540 ms (5%) |         |  32.45 MiB (1%) |     1034150 |
| `["words", "nthreads=4"]`                           |   9.672 ms (5%) |         |  32.90 MiB (1%) |     1034216 |

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
      Ubuntu 24.04.1 LTS
  uname: Linux 6.8.0-1017-azure #20-Ubuntu SMP Tue Oct 22 03:43:13 UTC 2024 x86_64 x86_64
  CPU: AMD EPYC 7763 64-Core Processor: 
              speed         user         nice          sys         idle          irq
       #1  3240 MHz       2651 s          0 s        186 s       4201 s          0 s
       #2  3185 MHz       2798 s          0 s        228 s       3981 s          0 s
       #3  3250 MHz       2164 s          0 s        196 s       4640 s          0 s
       #4  3245 MHz       2482 s          0 s        207 s       4302 s          0 s
       
  Memory: 15.615280151367188 GB (8621.11328125 MB free)
  Uptime: 709.6 sec
  Load Avg:  1.68  1.56  0.97
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, znver3)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 18 Jan 2025 - 1:51
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
| `["collect", "assoc", "basesize=1"]`                | 149.841 ms (5%) |         |   4.36 MiB (1%) |       32800 |
| `["collect", "assoc", "basesize=1024"]`             | 148.424 ms (5%) |         |   1.09 MiB (1%) |          53 |
| `["collect", "assoc", "basesize=32"]`               | 148.380 ms (5%) |         |   1.48 MiB (1%) |        1052 |
| `["collect", "seq"]`                                | 296.128 ms (5%) |         | 256.05 KiB (1%) |           2 |
| `["collect", "unordered", "basesize=1"]`            | 245.293 ms (5%) |         |  23.69 MiB (1%) |      406266 |
| `["collect", "unordered", "basesize=1024"]`         | 158.616 ms (5%) |         |   1.01 MiB (1%) |        1070 |
| `["collect", "unordered", "basesize=32"]`           | 170.578 ms (5%) |         |   1.60 MiB (1%) |       15236 |
| `["findfirst", "n=1000", "foldl"]`                  | 509.481 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 278.005 ms (5%) |         | 232.83 KiB (1%) |        3275 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 399.774 ms (5%) |         | 173.20 KiB (1%) |        2435 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 457.222 ms (5%) |         | 108.55 KiB (1%) |        1509 |
| `["findfirst", "n=400", "foldl"]`                   | 381.097 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 194.183 ms (5%) |         | 373.95 KiB (1%) |        5341 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 199.186 ms (5%) |         | 200.89 KiB (1%) |        2874 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 221.673 ms (5%) |         | 112.59 KiB (1%) |        1622 |
| `["findfirst", "n=500", "foldl"]`                   |  65.513 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |  74.643 ms (5%) |         | 135.95 KiB (1%) |        1891 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |  93.668 ms (5%) |         |  97.86 KiB (1%) |        1337 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  88.471 ms (5%) |         |  56.84 KiB (1%) |         779 |
| `["overhead", "default"]`                           |  52.027 μs (5%) |         |  32.73 KiB (1%) |         418 |
| `["overhead", "stoppable=false"]`                   |  51.055 μs (5%) |         |  32.75 KiB (1%) |         418 |
| `["overhead", "stoppable=true"]`                    |  58.830 μs (5%) |         |  44.25 KiB (1%) |         610 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   2.405 ms (5%) |         | 728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   2.962 ms (5%) |         |   1.79 MiB (1%) |         216 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   2.686 ms (5%) |         |   1.42 MiB (1%) |         118 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |   8.010 ms (5%) |         |   1.57 MiB (1%) |        2073 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  12.457 ms (5%) |         |   1.32 MiB (1%) |        9397 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  11.796 ms (5%) |         |   1.29 MiB (1%) |        7217 |
| `["parallel_histogram", "seq"]`                     |   4.272 ms (5%) |         | 364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  31.311 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  15.714 ms (5%) |         |  736 bytes (1%) |          11 |
| `["splitby", "count", "foldl"]`                     |   1.542 ms (5%) |         |                 |             |
| `["splitby", "count", "man"]`                       |   1.166 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    | 857.375 μs (5%) |         |   1.06 KiB (1%) |          18 |
| `["sum", "random", "foldl"]`                        |  11.022 ms (5%) |         |                 |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   5.615 ms (5%) |         |  74.22 KiB (1%) |        1105 |
| `["sum", "random", "reduce", "basesize=256"]`       |   5.568 ms (5%) |         |  36.78 KiB (1%) |         547 |
| `["sum", "random", "reduce", "basesize=512"]`       |   5.552 ms (5%) |         |  18.08 KiB (1%) |         269 |
| `["sum", "uniform", "foldl"]`                       |  10.919 ms (5%) |         |                 |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   5.587 ms (5%) |         |  74.12 KiB (1%) |        1102 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   5.529 ms (5%) |         |  36.78 KiB (1%) |         547 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   5.496 ms (5%) |         |  18.08 KiB (1%) |         269 |
| `["sum", "valley", "foldl"]`                        |  11.165 ms (5%) |         |                 |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   5.728 ms (5%) |         |  74.12 KiB (1%) |        1102 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   5.664 ms (5%) |         |  36.75 KiB (1%) |         546 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   5.634 ms (5%) |         |  18.11 KiB (1%) |         270 |
| `["words", "nthreads=1"]`                           |  14.785 ms (5%) |         |  31.56 MiB (1%) |     1028422 |
| `["words", "nthreads=2"]`                           |  10.062 ms (5%) |         |  31.92 MiB (1%) |     1028470 |
| `["words", "nthreads=4"]`                           |  10.847 ms (5%) |         |  32.82 MiB (1%) |     1028635 |

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
      Ubuntu 24.04.1 LTS
  uname: Linux 6.8.0-1017-azure #20-Ubuntu SMP Tue Oct 22 03:43:13 UTC 2024 x86_64 x86_64
  CPU: AMD EPYC 7763 64-Core Processor: 
              speed         user         nice          sys         idle          irq
       #1  3245 MHz       3621 s          0 s        261 s       6221 s          0 s
       #2  3245 MHz       4283 s          0 s        322 s       5469 s          0 s
       #3  3242 MHz       3349 s          0 s        255 s       6462 s          0 s
       #4  3241 MHz       3600 s          0 s        274 s       6184 s          0 s
       
  Memory: 15.615280151367188 GB (8581.71875 MB free)
  Uptime: 1016.77 sec
  Load Avg:  1.67  1.68  1.2
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

    Architecture:                         x86_64
    CPU op-mode(s):                       32-bit, 64-bit
    Address sizes:                        48 bits physical, 48 bits virtual
    Byte Order:                           Little Endian
    CPU(s):                               4
    On-line CPU(s) list:                  0-3
    Vendor ID:                            AuthenticAMD
    Model name:                           AMD EPYC 7763 64-Core Processor
    CPU family:                           25
    Model:                                1
    Thread(s) per core:                   2
    Core(s) per socket:                   2
    Socket(s):                            1
    Stepping:                             1
    BogoMIPS:                             4890.86
    Flags:                                fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush mmx fxsr sse sse2 ht syscall nx mmxext fxsr_opt pdpe1gb rdtscp lm constant_tsc rep_good nopl tsc_reliable nonstop_tsc cpuid extd_apicid aperfmperf pni pclmulqdq ssse3 fma cx16 pcid sse4_1 sse4_2 movbe popcnt aes xsave avx f16c rdrand hypervisor lahf_lm cmp_legacy svm cr8_legacy abm sse4a misalignsse 3dnowprefetch osvw topoext vmmcall fsgsbase bmi1 avx2 smep bmi2 erms invpcid rdseed adx smap clflushopt clwb sha_ni xsaveopt xsavec xgetbv1 xsaves user_shstk clzero xsaveerptr rdpru arat npt nrip_save tsc_scale vmcb_clean flushbyasid decodeassists pausefilter pfthreshold v_vmsave_vmload umip vaes vpclmulqdq rdpid fsrm
    Virtualization:                       AMD-V
    Hypervisor vendor:                    Microsoft
    Virtualization type:                  full
    L1d cache:                            64 KiB (2 instances)
    L1i cache:                            64 KiB (2 instances)
    L2 cache:                             1 MiB (2 instances)
    L3 cache:                             32 MiB (1 instance)
    NUMA node(s):                         1
    NUMA node0 CPU(s):                    0-3
    Vulnerability Gather data sampling:   Not affected
    Vulnerability Itlb multihit:          Not affected
    Vulnerability L1tf:                   Not affected
    Vulnerability Mds:                    Not affected
    Vulnerability Meltdown:               Not affected
    Vulnerability Mmio stale data:        Not affected
    Vulnerability Reg file data sampling: Not affected
    Vulnerability Retbleed:               Not affected
    Vulnerability Spec rstack overflow:   Vulnerable: Safe RET, no microcode
    Vulnerability Spec store bypass:      Vulnerable
    Vulnerability Spectre v1:             Mitigation; usercopy/swapgs barriers and __user pointer sanitization
    Vulnerability Spectre v2:             Mitigation; Retpolines; STIBP disabled; RSB filling; PBRSB-eIBRS Not affected; BHI Not affected
    Vulnerability Srbds:                  Not affected
    Vulnerability Tsx async abort:        Not affected
    

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

