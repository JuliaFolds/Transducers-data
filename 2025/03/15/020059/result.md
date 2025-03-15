# Multi-thread benchmark result

* Pull request commit: [`96a179e0dd23e4dfcf226fdab71f00cbf4262f17`](https://github.com/JuliaFolds/Transducers.jl/commit/96a179e0dd23e4dfcf226fdab71f00cbf4262f17)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/243> (Update */Manifest.toml)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 15 Mar 2025 - 01:55
    - Baseline: 15 Mar 2025 - 02:00
* Package commits:
    - Target: c1a0b2
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
| `["findfirst", "n=1000", "reduce", "basesize=128"]` |                1.44 (5%) :x: |                1.35 (1%) :x: |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 0.57 (5%) :white_check_mark: | 0.68 (1%) :white_check_mark: |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` |                1.75 (5%) :x: |                1.55 (1%) :x: |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 0.92 (5%) :white_check_mark: | 0.91 (1%) :white_check_mark: |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  |                1.16 (5%) :x: |                1.06 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 0.44 (5%) :white_check_mark: | 0.60 (1%) :white_check_mark: |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 0.52 (5%) :white_check_mark: | 0.66 (1%) :white_check_mark: |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 0.91 (5%) :white_check_mark: | 0.95 (1%) :white_check_mark: |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |                   1.03 (5%)  |                1.30 (1%) :x: |
| `["parallel_histogram", "comm", "basesize=16384"]`  |                   1.00 (5%)  | 0.99 (1%) :white_check_mark: |
| `["parallel_histogram", "comm", "basesize=4096"]`   |                   0.99 (5%)  |                1.01 (1%) :x: |
| `["parallel_histogram", "comm", "basesize=8192"]`   |                   1.03 (5%)  |                1.02 (1%) :x: |
| `["partition_length_maximum", "rand", "reduce"]`    |                   1.00 (5%)  |                1.05 (1%) :x: |
| `["splitby", "count", "reduce"]`                    | 0.84 (5%) :white_check_mark: |                1.04 (1%) :x: |

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
      Ubuntu 24.04.2 LTS
  uname: Linux 6.8.0-1021-azure #25-Ubuntu SMP Wed Jan 15 20:45:09 UTC 2025 x86_64 x86_64
  CPU: AMD EPYC 7763 64-Core Processor: 
              speed         user         nice          sys         idle          irq
       #1  3246 MHz       2562 s          0 s        225 s       4013 s          0 s
       #2  3232 MHz       2671 s          0 s        208 s       3946 s          0 s
       #3  3245 MHz       2530 s          0 s        173 s       4116 s          0 s
       #4  3245 MHz       2223 s          0 s        226 s       4349 s          0 s
       
  Memory: 15.61526870727539 GB (8713.25 MB free)
  Uptime: 689.61 sec
  Load Avg:  1.66  1.48  0.88
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
      Ubuntu 24.04.2 LTS
  uname: Linux 6.8.0-1021-azure #25-Ubuntu SMP Wed Jan 15 20:45:09 UTC 2025 x86_64 x86_64
  CPU: AMD EPYC 7763 64-Core Processor: 
              speed         user         nice          sys         idle          irq
       #1  3246 MHz       3743 s          0 s        287 s       5859 s          0 s
       #2  3263 MHz       3756 s          0 s        282 s       5874 s          0 s
       #3  3244 MHz       3939 s          0 s        272 s       5698 s          0 s
       #4  3242 MHz       3344 s          0 s        298 s       6246 s          0 s
       
  Memory: 15.61526870727539 GB (8608.734375 MB free)
  Uptime: 999.05 sec
  Load Avg:  1.74  1.65  1.14
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, znver3)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 15 Mar 2025 - 1:55
* Package commit: c1a0b2
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
| `["collect", "assoc", "basesize=1"]`                | 149.691 ms (5%) |         |   4.36 MiB (1%) |       32800 |
| `["collect", "assoc", "basesize=1024"]`             | 148.168 ms (5%) |         |   1.09 MiB (1%) |          53 |
| `["collect", "assoc", "basesize=32"]`               | 148.351 ms (5%) |         |   1.48 MiB (1%) |        1052 |
| `["collect", "seq"]`                                | 296.135 ms (5%) |         | 256.05 KiB (1%) |           2 |
| `["collect", "unordered", "basesize=1"]`            | 246.322 ms (5%) |         |  23.69 MiB (1%) |      406096 |
| `["collect", "unordered", "basesize=1024"]`         | 158.597 ms (5%) |         |   1.01 MiB (1%) |        1173 |
| `["collect", "unordered", "basesize=32"]`           | 173.480 ms (5%) |         |   1.60 MiB (1%) |       15340 |
| `["findfirst", "n=1000", "foldl"]`                  | 509.814 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 395.285 ms (5%) |         | 314.34 KiB (1%) |        4433 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 341.250 ms (5%) |         | 157.20 KiB (1%) |        2193 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 796.765 ms (5%) |         | 168.31 KiB (1%) |        2376 |
| `["findfirst", "n=400", "foldl"]`                   | 381.079 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 197.550 ms (5%) |         | 384.09 KiB (1%) |        5471 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 197.823 ms (5%) |         | 200.98 KiB (1%) |        2877 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 285.691 ms (5%) |         | 146.14 KiB (1%) |        2101 |
| `["findfirst", "n=500", "foldl"]`                   |  65.593 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |  57.718 ms (5%) |         | 138.83 KiB (1%) |        1867 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |  75.668 ms (5%) |         |  90.27 KiB (1%) |        1218 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  86.344 ms (5%) |         |  56.73 KiB (1%) |         775 |
| `["overhead", "default"]`                           |  52.939 μs (5%) |         |  32.73 KiB (1%) |         418 |
| `["overhead", "stoppable=false"]`                   |  53.560 μs (5%) |         |  32.72 KiB (1%) |         417 |
| `["overhead", "stoppable=true"]`                    |  60.462 μs (5%) |         |  44.25 KiB (1%) |         610 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   2.405 ms (5%) |         | 728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   3.033 ms (5%) |         |   2.32 MiB (1%) |         227 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   2.681 ms (5%) |         |   1.42 MiB (1%) |         118 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |   8.314 ms (5%) |         |   1.55 MiB (1%) |        1302 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  13.480 ms (5%) |         |   1.34 MiB (1%) |       10220 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  11.828 ms (5%) |         |   1.28 MiB (1%) |        8109 |
| `["parallel_histogram", "seq"]`                     |   4.278 ms (5%) |         | 364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  31.328 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  15.698 ms (5%) |         |  736 bytes (1%) |          11 |
| `["splitby", "count", "foldl"]`                     |   1.552 ms (5%) |         |                 |             |
| `["splitby", "count", "man"]`                       |   1.166 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    | 722.318 μs (5%) |         |   1.09 KiB (1%) |          19 |
| `["sum", "random", "foldl"]`                        |  11.069 ms (5%) |         |                 |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   5.684 ms (5%) |         |  74.22 KiB (1%) |        1105 |
| `["sum", "random", "reduce", "basesize=256"]`       |   5.613 ms (5%) |         |  36.81 KiB (1%) |         548 |
| `["sum", "random", "reduce", "basesize=512"]`       |   5.582 ms (5%) |         |  18.08 KiB (1%) |         269 |
| `["sum", "uniform", "foldl"]`                       |  10.924 ms (5%) |         |                 |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   5.623 ms (5%) |         |  74.19 KiB (1%) |        1104 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   5.560 ms (5%) |         |  36.81 KiB (1%) |         548 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   5.516 ms (5%) |         |  18.08 KiB (1%) |         269 |
| `["sum", "valley", "foldl"]`                        |  11.173 ms (5%) |         |                 |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   5.737 ms (5%) |         |  74.09 KiB (1%) |        1101 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   5.668 ms (5%) |         |  36.75 KiB (1%) |         546 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   5.636 ms (5%) |         |  18.08 KiB (1%) |         269 |
| `["words", "nthreads=1"]`                           |  14.235 ms (5%) |         |  31.55 MiB (1%) |     1028137 |
| `["words", "nthreads=2"]`                           |   9.658 ms (5%) |         |  32.27 MiB (1%) |     1028220 |
| `["words", "nthreads=4"]`                           |  10.061 ms (5%) |         |  32.90 MiB (1%) |     1028366 |

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
      Ubuntu 24.04.2 LTS
  uname: Linux 6.8.0-1021-azure #25-Ubuntu SMP Wed Jan 15 20:45:09 UTC 2025 x86_64 x86_64
  CPU: AMD EPYC 7763 64-Core Processor: 
              speed         user         nice          sys         idle          irq
       #1  3246 MHz       2562 s          0 s        225 s       4013 s          0 s
       #2  3232 MHz       2671 s          0 s        208 s       3946 s          0 s
       #3  3245 MHz       2530 s          0 s        173 s       4116 s          0 s
       #4  3245 MHz       2223 s          0 s        226 s       4349 s          0 s
       
  Memory: 15.61526870727539 GB (8713.25 MB free)
  Uptime: 689.61 sec
  Load Avg:  1.66  1.48  0.88
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, znver3)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 15 Mar 2025 - 2:0
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
| `["collect", "assoc", "basesize=1"]`                | 149.882 ms (5%) |         |   4.36 MiB (1%) |       32800 |
| `["collect", "assoc", "basesize=1024"]`             | 148.437 ms (5%) |         |   1.09 MiB (1%) |          53 |
| `["collect", "assoc", "basesize=32"]`               | 148.302 ms (5%) |         |   1.48 MiB (1%) |        1052 |
| `["collect", "seq"]`                                | 296.042 ms (5%) |         | 256.05 KiB (1%) |           2 |
| `["collect", "unordered", "basesize=1"]`            | 250.816 ms (5%) |         |  23.68 MiB (1%) |      405917 |
| `["collect", "unordered", "basesize=1024"]`         | 158.394 ms (5%) |         |   1.01 MiB (1%) |        1150 |
| `["collect", "unordered", "basesize=32"]`           | 170.919 ms (5%) |         |   1.61 MiB (1%) |       15512 |
| `["findfirst", "n=1000", "foldl"]`                  | 506.839 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 275.254 ms (5%) |         | 232.73 KiB (1%) |        3272 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 595.971 ms (5%) |         | 232.36 KiB (1%) |        3306 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 455.878 ms (5%) |         | 108.55 KiB (1%) |        1509 |
| `["findfirst", "n=400", "foldl"]`                   | 379.886 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 214.924 ms (5%) |         | 422.09 KiB (1%) |        5987 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 198.406 ms (5%) |         | 200.86 KiB (1%) |        2873 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 246.284 ms (5%) |         | 137.55 KiB (1%) |        1954 |
| `["findfirst", "n=500", "foldl"]`                   |  65.258 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 132.556 ms (5%) |         | 232.66 KiB (1%) |        3227 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 145.404 ms (5%) |         | 137.16 KiB (1%) |        1919 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  94.803 ms (5%) |         |  59.84 KiB (1%) |         819 |
| `["overhead", "default"]`                           |  51.296 μs (5%) |         |  32.73 KiB (1%) |         418 |
| `["overhead", "stoppable=false"]`                   |  53.119 μs (5%) |         |  32.75 KiB (1%) |         418 |
| `["overhead", "stoppable=true"]`                    |  60.924 μs (5%) |         |  44.25 KiB (1%) |         610 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   2.391 ms (5%) |         | 728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   2.954 ms (5%) |         |   1.79 MiB (1%) |         216 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   2.674 ms (5%) |         |   1.42 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |   8.311 ms (5%) |         |   1.57 MiB (1%) |        2037 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  13.682 ms (5%) |         |   1.32 MiB (1%) |        9582 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  11.437 ms (5%) |         |   1.26 MiB (1%) |        7416 |
| `["parallel_histogram", "seq"]`                     |   4.264 ms (5%) |         | 364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  31.314 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  15.685 ms (5%) |         |  704 bytes (1%) |          10 |
| `["splitby", "count", "foldl"]`                     |   1.498 ms (5%) |         |                 |             |
| `["splitby", "count", "man"]`                       |   1.140 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    | 859.885 μs (5%) |         |   1.05 KiB (1%) |          19 |
| `["sum", "random", "foldl"]`                        |  10.959 ms (5%) |         |                 |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   5.586 ms (5%) |         |  74.25 KiB (1%) |        1106 |
| `["sum", "random", "reduce", "basesize=256"]`       |   5.539 ms (5%) |         |  36.78 KiB (1%) |         547 |
| `["sum", "random", "reduce", "basesize=512"]`       |   5.517 ms (5%) |         |  18.05 KiB (1%) |         268 |
| `["sum", "uniform", "foldl"]`                       |  10.935 ms (5%) |         |                 |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   5.603 ms (5%) |         |  74.16 KiB (1%) |        1103 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   5.538 ms (5%) |         |  36.81 KiB (1%) |         548 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   5.501 ms (5%) |         |  18.08 KiB (1%) |         269 |
| `["sum", "valley", "foldl"]`                        |  11.172 ms (5%) |         |                 |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   5.718 ms (5%) |         |  74.06 KiB (1%) |        1100 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   5.655 ms (5%) |         |  36.75 KiB (1%) |         546 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   5.641 ms (5%) |         |  18.08 KiB (1%) |         269 |
| `["words", "nthreads=1"]`                           |  14.673 ms (5%) |         |  31.71 MiB (1%) |     1032875 |
| `["words", "nthreads=2"]`                           |   9.743 ms (5%) |         |  32.42 MiB (1%) |     1032952 |
| `["words", "nthreads=4"]`                           |   9.882 ms (5%) |         |  32.87 MiB (1%) |     1033019 |

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
      Ubuntu 24.04.2 LTS
  uname: Linux 6.8.0-1021-azure #25-Ubuntu SMP Wed Jan 15 20:45:09 UTC 2025 x86_64 x86_64
  CPU: AMD EPYC 7763 64-Core Processor: 
              speed         user         nice          sys         idle          irq
       #1  3246 MHz       3743 s          0 s        287 s       5859 s          0 s
       #2  3263 MHz       3756 s          0 s        282 s       5874 s          0 s
       #3  3244 MHz       3939 s          0 s        272 s       5698 s          0 s
       #4  3242 MHz       3344 s          0 s        298 s       6246 s          0 s
       
  Memory: 15.61526870727539 GB (8608.734375 MB free)
  Uptime: 999.05 sec
  Load Avg:  1.74  1.65  1.14
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

