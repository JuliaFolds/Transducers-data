# Multi-thread benchmark result

* Pull request commit: [`c3af82f0c72de4dc7bea18177cad24a219f21db0`](https://github.com/JuliaFolds/Transducers.jl/commit/c3af82f0c72de4dc7bea18177cad24a219f21db0)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/243> (Update */Manifest.toml)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 26 Jun 2024 - 01:31
    - Baseline: 26 Jun 2024 - 01:35
* Package commits:
    - Target: 7123f4
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
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 0.70 (5%) :white_check_mark: | 0.74 (1%) :white_check_mark: |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` |                1.27 (5%) :x: |                1.13 (1%) :x: |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 0.76 (5%) :white_check_mark: | 0.75 (1%) :white_check_mark: |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  |                   1.02 (5%)  |                1.03 (1%) :x: |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  |                   1.00 (5%)  |                1.03 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 0.70 (5%) :white_check_mark: | 0.75 (1%) :white_check_mark: |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 0.44 (5%) :white_check_mark: | 0.54 (1%) :white_check_mark: |
| `["parallel_histogram", "comm", "basesize=16384"]`  | 0.94 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["parallel_histogram", "comm", "basesize=4096"]`   | 0.92 (5%) :white_check_mark: | 0.99 (1%) :white_check_mark: |
| `["splitby", "count", "foldl"]`                     |                1.13 (5%) :x: |                   1.00 (1%)  |
| `["splitby", "count", "reduce"]`                    |                   1.01 (5%)  | 0.97 (1%) :white_check_mark: |
| `["words", "nthreads=1"]`                           |                   0.99 (5%)  | 0.99 (1%) :white_check_mark: |
| `["words", "nthreads=2"]`                           |                   0.98 (5%)  | 0.99 (1%) :white_check_mark: |
| `["words", "nthreads=4"]`                           |                1.06 (5%) :x: |                   0.99 (1%)  |

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
      Ubuntu 22.04.4 LTS
  uname: Linux 6.5.0-1022-azure #23~22.04.1-Ubuntu SMP Thu May  9 17:59:24 UTC 2024 x86_64 x86_64
  CPU: AMD EPYC 7763 64-Core Processor: 
              speed         user         nice          sys         idle          irq
       #1  2445 MHz       2483 s          0 s        149 s       5166 s          0 s
       #2  2564 MHz       2544 s          0 s        160 s       5087 s          0 s
       #3  2445 MHz       2944 s          0 s        180 s       4678 s          0 s
       #4  3243 MHz       2154 s          0 s        168 s       5475 s          0 s
       
  Memory: 15.606491088867188 GB (12464.5546875 MB free)
  Uptime: 783.27 sec
  Load Avg:  1.88  1.58  0.92
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
      Ubuntu 22.04.4 LTS
  uname: Linux 6.5.0-1022-azure #23~22.04.1-Ubuntu SMP Thu May  9 17:59:24 UTC 2024 x86_64 x86_64
  CPU: AMD EPYC 7763 64-Core Processor: 
              speed         user         nice          sys         idle          irq
       #1  3230 MHz       3480 s          0 s        196 s       7047 s          0 s
       #2  3187 MHz       4143 s          0 s        212 s       6364 s          0 s
       #3  3241 MHz       3970 s          0 s        234 s       6523 s          0 s
       #4  3235 MHz       3143 s          0 s        218 s       7363 s          0 s
       
  Memory: 15.606491088867188 GB (12411.08984375 MB free)
  Uptime: 1076.53 sec
  Load Avg:  1.78  1.68  1.15
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, znver3)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 26 Jun 2024 - 1:31
* Package commit: 7123f4
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
| `["collect", "assoc", "basesize=1"]`                | 149.007 ms (5%) |         |   4.36 MiB (1%) |       32800 |
| `["collect", "assoc", "basesize=1024"]`             | 147.406 ms (5%) |         |   1.09 MiB (1%) |          53 |
| `["collect", "assoc", "basesize=32"]`               | 147.548 ms (5%) |         |   1.48 MiB (1%) |        1052 |
| `["collect", "seq"]`                                | 294.503 ms (5%) |         | 256.05 KiB (1%) |           2 |
| `["collect", "unordered", "basesize=1"]`            | 247.957 ms (5%) |         |  23.78 MiB (1%) |      409120 |
| `["collect", "unordered", "basesize=1024"]`         | 156.001 ms (5%) |         |   1.01 MiB (1%) |        1081 |
| `["collect", "unordered", "basesize=32"]`           | 163.779 ms (5%) |         |   1.60 MiB (1%) |       15189 |
| `["findfirst", "n=1000", "foldl"]`                  | 503.899 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 275.185 ms (5%) |         | 232.73 KiB (1%) |        3272 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 428.798 ms (5%) |         | 176.88 KiB (1%) |        2510 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 343.856 ms (5%) |         |  81.33 KiB (1%) |        1146 |
| `["findfirst", "n=400", "foldl"]`                   | 376.771 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 197.383 ms (5%) |         | 386.19 KiB (1%) |        5495 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 195.693 ms (5%) |         | 202.42 KiB (1%) |        2891 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 277.513 ms (5%) |         | 144.55 KiB (1%) |        2074 |
| `["findfirst", "n=500", "foldl"]`                   |  64.655 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |  93.606 ms (5%) |         | 175.73 KiB (1%) |        2403 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |  62.337 ms (5%) |         |  74.56 KiB (1%) |        1016 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  93.570 ms (5%) |         |  63.69 KiB (1%) |         866 |
| `["overhead", "default"]`                           |  51.285 μs (5%) |         |  32.73 KiB (1%) |         418 |
| `["overhead", "stoppable=false"]`                   |  53.740 μs (5%) |         |  32.78 KiB (1%) |         419 |
| `["overhead", "stoppable=true"]`                    |  57.766 μs (5%) |         |  44.25 KiB (1%) |         610 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   2.386 ms (5%) |         | 728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   2.914 ms (5%) |         |   1.79 MiB (1%) |         216 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   2.644 ms (5%) |         |   1.42 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |   7.934 ms (5%) |         |   1.56 MiB (1%) |        1881 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  13.817 ms (5%) |         |   1.35 MiB (1%) |       10407 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  12.203 ms (5%) |         |   1.28 MiB (1%) |        7377 |
| `["parallel_histogram", "seq"]`                     |   4.222 ms (5%) |         | 364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  31.129 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  15.613 ms (5%) |         |  736 bytes (1%) |          11 |
| `["splitby", "count", "foldl"]`                     |   1.744 ms (5%) |         |                 |             |
| `["splitby", "count", "man"]`                       |   1.132 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    | 729.278 μs (5%) |         |   1.06 KiB (1%) |          18 |
| `["sum", "random", "foldl"]`                        |  11.013 ms (5%) |         |                 |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   5.647 ms (5%) |         |  74.17 KiB (1%) |        1104 |
| `["sum", "random", "reduce", "basesize=256"]`       |   5.584 ms (5%) |         |  36.77 KiB (1%) |         547 |
| `["sum", "random", "reduce", "basesize=512"]`       |   5.552 ms (5%) |         |  18.11 KiB (1%) |         270 |
| `["sum", "uniform", "foldl"]`                       |  10.885 ms (5%) |         |                 |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   5.580 ms (5%) |         |  74.14 KiB (1%) |        1103 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   5.514 ms (5%) |         |  36.70 KiB (1%) |         545 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   5.473 ms (5%) |         |  18.00 KiB (1%) |         267 |
| `["sum", "valley", "foldl"]`                        |  11.106 ms (5%) |         |                 |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   5.700 ms (5%) |         |  74.14 KiB (1%) |        1103 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   5.643 ms (5%) |         |  36.73 KiB (1%) |         546 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   5.611 ms (5%) |         |  18.06 KiB (1%) |         269 |
| `["words", "nthreads=1"]`                           |  14.228 ms (5%) |         |  31.50 MiB (1%) |     1026547 |
| `["words", "nthreads=2"]`                           |   9.373 ms (5%) |         |  32.21 MiB (1%) |     1026652 |
| `["words", "nthreads=4"]`                           |  10.119 ms (5%) |         |  32.84 MiB (1%) |     1026824 |

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
      Ubuntu 22.04.4 LTS
  uname: Linux 6.5.0-1022-azure #23~22.04.1-Ubuntu SMP Thu May  9 17:59:24 UTC 2024 x86_64 x86_64
  CPU: AMD EPYC 7763 64-Core Processor: 
              speed         user         nice          sys         idle          irq
       #1  2445 MHz       2483 s          0 s        149 s       5166 s          0 s
       #2  2564 MHz       2544 s          0 s        160 s       5087 s          0 s
       #3  2445 MHz       2944 s          0 s        180 s       4678 s          0 s
       #4  3243 MHz       2154 s          0 s        168 s       5475 s          0 s
       
  Memory: 15.606491088867188 GB (12464.5546875 MB free)
  Uptime: 783.27 sec
  Load Avg:  1.88  1.58  0.92
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, znver3)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 26 Jun 2024 - 1:35
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
| `["collect", "assoc", "basesize=1"]`                | 148.676 ms (5%) |         |   4.36 MiB (1%) |       32800 |
| `["collect", "assoc", "basesize=1024"]`             | 147.595 ms (5%) |         |   1.09 MiB (1%) |          53 |
| `["collect", "assoc", "basesize=32"]`               | 147.521 ms (5%) |         |   1.48 MiB (1%) |        1052 |
| `["collect", "seq"]`                                | 294.600 ms (5%) |         | 256.05 KiB (1%) |           2 |
| `["collect", "unordered", "basesize=1"]`            | 244.754 ms (5%) |         |  23.81 MiB (1%) |      409889 |
| `["collect", "unordered", "basesize=1024"]`         | 156.680 ms (5%) |         |   1.01 MiB (1%) |        1177 |
| `["collect", "unordered", "basesize=32"]`           | 163.765 ms (5%) |         |   1.60 MiB (1%) |       15233 |
| `["findfirst", "n=1000", "foldl"]`                  | 505.981 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 392.772 ms (5%) |         | 313.84 KiB (1%) |        4417 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 338.567 ms (5%) |         | 157.20 KiB (1%) |        2193 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 452.934 ms (5%) |         | 108.55 KiB (1%) |        1509 |
| `["findfirst", "n=400", "foldl"]`                   | 378.427 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 194.273 ms (5%) |         | 374.11 KiB (1%) |        5349 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 198.116 ms (5%) |         | 200.67 KiB (1%) |        2867 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 276.884 ms (5%) |         | 140.66 KiB (1%) |        2022 |
| `["findfirst", "n=500", "foldl"]`                   |  64.961 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 134.672 ms (5%) |         | 233.77 KiB (1%) |        3252 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 140.887 ms (5%) |         | 137.28 KiB (1%) |        1885 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  93.884 ms (5%) |         |  63.66 KiB (1%) |         865 |
| `["overhead", "default"]`                           |  52.827 μs (5%) |         |  32.77 KiB (1%) |         419 |
| `["overhead", "stoppable=false"]`                   |  52.197 μs (5%) |         |  32.75 KiB (1%) |         418 |
| `["overhead", "stoppable=true"]`                    |  59.390 μs (5%) |         |  44.28 KiB (1%) |         611 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   2.404 ms (5%) |         | 728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   2.948 ms (5%) |         |   1.79 MiB (1%) |         216 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   2.658 ms (5%) |         |   1.42 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |   8.481 ms (5%) |         |   1.57 MiB (1%) |        2034 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  15.044 ms (5%) |         |   1.37 MiB (1%) |       10949 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  12.530 ms (5%) |         |   1.26 MiB (1%) |        7542 |
| `["parallel_histogram", "seq"]`                     |   4.246 ms (5%) |         | 364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  31.115 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  15.569 ms (5%) |         |  736 bytes (1%) |          11 |
| `["splitby", "count", "foldl"]`                     |   1.547 ms (5%) |         |                 |             |
| `["splitby", "count", "man"]`                       |   1.158 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    | 721.002 μs (5%) |         |   1.09 KiB (1%) |          19 |
| `["sum", "random", "foldl"]`                        |  11.055 ms (5%) |         |                 |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   5.636 ms (5%) |         |  74.14 KiB (1%) |        1103 |
| `["sum", "random", "reduce", "basesize=256"]`       |   5.603 ms (5%) |         |  36.70 KiB (1%) |         545 |
| `["sum", "random", "reduce", "basesize=512"]`       |   5.573 ms (5%) |         |  18.08 KiB (1%) |         269 |
| `["sum", "uniform", "foldl"]`                       |  10.878 ms (5%) |         |                 |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   5.580 ms (5%) |         |  74.14 KiB (1%) |        1103 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   5.524 ms (5%) |         |  36.67 KiB (1%) |         544 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   5.478 ms (5%) |         |  18.03 KiB (1%) |         268 |
| `["sum", "valley", "foldl"]`                        |  11.107 ms (5%) |         |                 |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   5.705 ms (5%) |         |  74.08 KiB (1%) |        1101 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   5.644 ms (5%) |         |  36.70 KiB (1%) |         545 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   5.597 ms (5%) |         |  18.06 KiB (1%) |         269 |
| `["words", "nthreads=1"]`                           |  14.306 ms (5%) |         |  31.85 MiB (1%) |     1037797 |
| `["words", "nthreads=2"]`                           |   9.555 ms (5%) |         |  32.57 MiB (1%) |     1037909 |
| `["words", "nthreads=4"]`                           |   9.581 ms (5%) |         |  33.02 MiB (1%) |     1038013 |

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
      Ubuntu 22.04.4 LTS
  uname: Linux 6.5.0-1022-azure #23~22.04.1-Ubuntu SMP Thu May  9 17:59:24 UTC 2024 x86_64 x86_64
  CPU: AMD EPYC 7763 64-Core Processor: 
              speed         user         nice          sys         idle          irq
       #1  3230 MHz       3480 s          0 s        196 s       7047 s          0 s
       #2  3187 MHz       4143 s          0 s        212 s       6364 s          0 s
       #3  3241 MHz       3970 s          0 s        234 s       6523 s          0 s
       #4  3235 MHz       3143 s          0 s        218 s       7363 s          0 s
       
  Memory: 15.606491088867188 GB (12411.08984375 MB free)
  Uptime: 1076.53 sec
  Load Avg:  1.78  1.68  1.15
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
    BogoMIPS:                           4890.86
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

