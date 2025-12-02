# Multi-thread benchmark result

* Pull request commit: [`f0251a3d3e68d53954de68638f19aa1322cc6652`](https://github.com/JuliaFolds/Transducers.jl/commit/f0251a3d3e68d53954de68638f19aa1322cc6652)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/243> (Update */Manifest.toml)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 2 Dec 2025 - 02:10
    - Baseline: 2 Dec 2025 - 02:15
* Package commits:
    - Target: bfeee39
    - Baseline: 2a51f8d
* Julia commits:
    - Target: 742b9ab
    - Baseline: 742b9ab
* Julia command flags:
    - Target: None
    - Baseline: None
* Environment variables:
    - Target: `JULIA_NUM_THREADS => 2`
    - Baseline: `JULIA_NUM_THREADS => 2`

## Results
A ratio greater than `1.0` denotes a possible regression (marked with :x:), while a ratio less
than `1.0` denotes a possible improvement (marked with :white_check_mark:). Brackets display [tolerances](https://juliaci.github.io/BenchmarkTools.jl/stable/manual/#Benchmark-Parameters) for the benchmark estimates. Only significant results - results
that indicate possible regressions or improvements - are shown below (thus, an empty table means that all
benchmark results remained invariant between builds).

| ID                                                  | time ratio                   | memory ratio                 |
|-----------------------------------------------------|------------------------------|------------------------------|
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 0.91 (5%) :white_check_mark: | 0.85 (1%) :white_check_mark: |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  |                   1.02 (5%)  |                1.04 (1%) :x: |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  |                1.30 (5%) :x: |                1.34 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 0.68 (5%) :white_check_mark: | 0.79 (1%) :white_check_mark: |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |                2.88 (5%) :x: |                2.22 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 0.94 (5%) :white_check_mark: | 0.96 (1%) :white_check_mark: |
| `["splitby", "count", "foldl"]`                     | 0.91 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["splitby", "count", "man"]`                       | 0.94 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["splitby", "count", "reduce"]`                    |                1.05 (5%) :x: |                   1.00 (1%)  |
| `["words", "nthreads=2"]`                           |                   0.98 (5%)  |                1.02 (1%) :x: |

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
      Ubuntu 24.04.3 LTS
  uname: Linux 6.11.0-1018-azure #18~24.04.1-Ubuntu SMP Sat Jun 28 04:46:03 UTC 2025 x86_64 x86_64
  CPU: AMD EPYC 7763 64-Core Processor: 
              speed         user         nice          sys         idle          irq
       #1  3226 MHz       2564 s          0 s        190 s       3704 s          0 s
       #2  3243 MHz       2787 s          0 s        182 s       3479 s          0 s
       #3  3242 MHz       2434 s          0 s        157 s       3870 s          0 s
       #4  3251 MHz       2118 s          0 s        154 s       4197 s          0 s
       
  Memory: 15.620681762695312 GB (8290.41796875 MB free)
  Uptime: 657.38 sec
  Load Avg:  1.7  1.51  0.89
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
      Ubuntu 24.04.3 LTS
  uname: Linux 6.11.0-1018-azure #18~24.04.1-Ubuntu SMP Sat Jun 28 04:46:03 UTC 2025 x86_64 x86_64
  CPU: AMD EPYC 7763 64-Core Processor: 
              speed         user         nice          sys         idle          irq
       #1  3240 MHz       3845 s          0 s        231 s       5440 s          0 s
       #2  3240 MHz       4049 s          0 s        256 s       5202 s          0 s
       #3  3238 MHz       3668 s          0 s        231 s       5623 s          0 s
       #4  3246 MHz       3114 s          0 s        208 s       6207 s          0 s
       
  Memory: 15.620681762695312 GB (8309.21875 MB free)
  Uptime: 963.7 sec
  Load Avg:  1.7  1.63  1.12
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, znver3)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 2 Dec 2025 - 02:10
* Package commit: bfeee39
* Julia commit: 742b9ab
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
| `["collect", "assoc", "basesize=1"]`                | 149.410 ms (5%) |         |   4.36 MiB (1%) |       32800 |
| `["collect", "assoc", "basesize=1024"]`             | 148.433 ms (5%) |         |   1.09 MiB (1%) |          53 |
| `["collect", "assoc", "basesize=32"]`               | 148.389 ms (5%) |         |   1.48 MiB (1%) |        1053 |
| `["collect", "seq"]`                                | 293.790 ms (5%) |         | 256.05 KiB (1%) |           2 |
| `["collect", "unordered", "basesize=1"]`            | 243.524 ms (5%) |         |  23.69 MiB (1%) |      406041 |
| `["collect", "unordered", "basesize=1024"]`         | 158.015 ms (5%) |         |   1.01 MiB (1%) |        1038 |
| `["collect", "unordered", "basesize=32"]`           | 170.049 ms (5%) |         |   1.60 MiB (1%) |       15305 |
| `["findfirst", "n=1000", "foldl"]`                  | 509.470 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 279.599 ms (5%) |         | 233.02 KiB (1%) |        3281 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 309.388 ms (5%) |         | 133.61 KiB (1%) |        1886 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 348.380 ms (5%) |         |  81.33 KiB (1%) |        1146 |
| `["findfirst", "n=400", "foldl"]`                   | 380.356 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 199.810 ms (5%) |         | 389.52 KiB (1%) |        5538 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 199.453 ms (5%) |         | 200.86 KiB (1%) |        2873 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 285.740 ms (5%) |         | 147.50 KiB (1%) |        2110 |
| `["findfirst", "n=500", "foldl"]`                   |  66.189 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |  76.928 ms (5%) |         | 170.64 KiB (1%) |        2306 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 191.774 ms (5%) |         | 170.98 KiB (1%) |        2385 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  80.832 ms (5%) |         |  54.41 KiB (1%) |         745 |
| `["overhead", "default"]`                           |  52.087 μs (5%) |         |  32.73 KiB (1%) |         418 |
| `["overhead", "stoppable=false"]`                   |  52.038 μs (5%) |         |  32.75 KiB (1%) |         418 |
| `["overhead", "stoppable=true"]`                    |  57.978 μs (5%) |         |  44.25 KiB (1%) |         610 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   2.327 ms (5%) |         | 728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   2.941 ms (5%) |         |   1.79 MiB (1%) |         216 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   2.629 ms (5%) |         |   1.42 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |   8.667 ms (5%) |         |   1.59 MiB (1%) |        2833 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  12.872 ms (5%) |         |   1.33 MiB (1%) |        9752 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  11.462 ms (5%) |         |   1.29 MiB (1%) |        7950 |
| `["parallel_histogram", "seq"]`                     |   4.277 ms (5%) |         | 364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  31.160 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  15.640 ms (5%) |         |  736 bytes (1%) |          11 |
| `["splitby", "count", "foldl"]`                     |   1.380 ms (5%) |         |                 |             |
| `["splitby", "count", "man"]`                       |   1.090 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    | 758.605 μs (5%) |         |   1.09 KiB (1%) |          19 |
| `["sum", "random", "foldl"]`                        |  10.992 ms (5%) |         |                 |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   5.640 ms (5%) |         |  74.19 KiB (1%) |        1104 |
| `["sum", "random", "reduce", "basesize=256"]`       |   5.434 ms (5%) |         |  36.75 KiB (1%) |         546 |
| `["sum", "random", "reduce", "basesize=512"]`       |   5.401 ms (5%) |         |  18.11 KiB (1%) |         270 |
| `["sum", "uniform", "foldl"]`                       |  10.944 ms (5%) |         |                 |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   5.611 ms (5%) |         |  74.19 KiB (1%) |        1104 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   5.321 ms (5%) |         |  36.78 KiB (1%) |         547 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   5.512 ms (5%) |         |  18.05 KiB (1%) |         268 |
| `["sum", "valley", "foldl"]`                        |  11.167 ms (5%) |         |                 |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   5.726 ms (5%) |         |  74.09 KiB (1%) |        1101 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   5.666 ms (5%) |         |  36.75 KiB (1%) |         546 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   5.650 ms (5%) |         |  18.08 KiB (1%) |         269 |
| `["words", "nthreads=1"]`                           |  14.173 ms (5%) |         |  31.71 MiB (1%) |     1033623 |
| `["words", "nthreads=2"]`                           |   9.835 ms (5%) |         |  32.42 MiB (1%) |     1033696 |
| `["words", "nthreads=4"]`                           |  10.084 ms (5%) |         |  32.87 MiB (1%) |     1033783 |

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
      Ubuntu 24.04.3 LTS
  uname: Linux 6.11.0-1018-azure #18~24.04.1-Ubuntu SMP Sat Jun 28 04:46:03 UTC 2025 x86_64 x86_64
  CPU: AMD EPYC 7763 64-Core Processor: 
              speed         user         nice          sys         idle          irq
       #1  3226 MHz       2564 s          0 s        190 s       3704 s          0 s
       #2  3243 MHz       2787 s          0 s        182 s       3479 s          0 s
       #3  3242 MHz       2434 s          0 s        157 s       3870 s          0 s
       #4  3251 MHz       2118 s          0 s        154 s       4197 s          0 s
       
  Memory: 15.620681762695312 GB (8290.41796875 MB free)
  Uptime: 657.38 sec
  Load Avg:  1.7  1.51  0.89
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, znver3)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 2 Dec 2025 - 02:15
* Package commit: 2a51f8d
* Julia commit: 742b9ab
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
| `["collect", "assoc", "basesize=1"]`                | 149.783 ms (5%) |         |   4.36 MiB (1%) |       32800 |
| `["collect", "assoc", "basesize=1024"]`             | 148.356 ms (5%) |         |   1.09 MiB (1%) |          53 |
| `["collect", "assoc", "basesize=32"]`               | 148.359 ms (5%) |         |   1.48 MiB (1%) |        1052 |
| `["collect", "seq"]`                                | 296.054 ms (5%) |         | 256.05 KiB (1%) |           2 |
| `["collect", "unordered", "basesize=1"]`            | 243.076 ms (5%) |         |  23.69 MiB (1%) |      406056 |
| `["collect", "unordered", "basesize=1024"]`         | 157.823 ms (5%) |         |   1.01 MiB (1%) |        1061 |
| `["collect", "unordered", "basesize=32"]`           | 169.081 ms (5%) |         |   1.60 MiB (1%) |       15320 |
| `["findfirst", "n=1000", "foldl"]`                  | 510.128 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 279.843 ms (5%) |         | 233.08 KiB (1%) |        3283 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 340.861 ms (5%) |         | 157.20 KiB (1%) |        2193 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 348.668 ms (5%) |         |  81.42 KiB (1%) |        1149 |
| `["findfirst", "n=400", "foldl"]`                   | 381.738 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 194.970 ms (5%) |         | 374.06 KiB (1%) |        5345 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 198.049 ms (5%) |         | 199.95 KiB (1%) |        2863 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 219.062 ms (5%) |         | 109.73 KiB (1%) |        1595 |
| `["findfirst", "n=500", "foldl"]`                   |  66.277 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 113.875 ms (5%) |         | 216.73 KiB (1%) |        2963 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |  66.488 ms (5%) |         |  76.92 KiB (1%) |        1051 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  85.670 ms (5%) |         |  56.86 KiB (1%) |         779 |
| `["overhead", "default"]`                           |  51.326 μs (5%) |         |  32.67 KiB (1%) |         416 |
| `["overhead", "stoppable=false"]`                   |  52.097 μs (5%) |         |  32.75 KiB (1%) |         418 |
| `["overhead", "stoppable=true"]`                    |  57.097 μs (5%) |         |  44.25 KiB (1%) |         610 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   2.403 ms (5%) |         | 728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   2.949 ms (5%) |         |   1.79 MiB (1%) |         216 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   2.679 ms (5%) |         |   1.42 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |   8.735 ms (5%) |         |   1.60 MiB (1%) |        2985 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  12.670 ms (5%) |         |   1.33 MiB (1%) |        9897 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  11.442 ms (5%) |         |   1.29 MiB (1%) |        7805 |
| `["parallel_histogram", "seq"]`                     |   4.077 ms (5%) |         | 364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  31.310 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  15.680 ms (5%) |         |  736 bytes (1%) |          11 |
| `["splitby", "count", "foldl"]`                     |   1.511 ms (5%) |         |                 |             |
| `["splitby", "count", "man"]`                       |   1.166 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    | 720.295 μs (5%) |         |   1.09 KiB (1%) |          19 |
| `["sum", "random", "foldl"]`                        |  11.024 ms (5%) |         |                 |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   5.623 ms (5%) |         |  74.12 KiB (1%) |        1102 |
| `["sum", "random", "reduce", "basesize=256"]`       |   5.589 ms (5%) |         |  36.75 KiB (1%) |         546 |
| `["sum", "random", "reduce", "basesize=512"]`       |   5.551 ms (5%) |         |  18.11 KiB (1%) |         270 |
| `["sum", "uniform", "foldl"]`                       |  10.915 ms (5%) |         |                 |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   5.594 ms (5%) |         |  74.19 KiB (1%) |        1104 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   5.194 ms (5%) |         |  36.78 KiB (1%) |         547 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   5.483 ms (5%) |         |  18.05 KiB (1%) |         268 |
| `["sum", "valley", "foldl"]`                        |  11.165 ms (5%) |         |                 |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   5.729 ms (5%) |         |  74.19 KiB (1%) |        1104 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   5.657 ms (5%) |         |  36.75 KiB (1%) |         546 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   5.629 ms (5%) |         |  18.08 KiB (1%) |         269 |
| `["words", "nthreads=1"]`                           |  14.526 ms (5%) |         |  31.58 MiB (1%) |     1029340 |
| `["words", "nthreads=2"]`                           |  10.086 ms (5%) |         |  31.94 MiB (1%) |     1029376 |
| `["words", "nthreads=4"]`                           |  10.528 ms (5%) |         |  32.65 MiB (1%) |     1029449 |

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
      Ubuntu 24.04.3 LTS
  uname: Linux 6.11.0-1018-azure #18~24.04.1-Ubuntu SMP Sat Jun 28 04:46:03 UTC 2025 x86_64 x86_64
  CPU: AMD EPYC 7763 64-Core Processor: 
              speed         user         nice          sys         idle          irq
       #1  3240 MHz       3845 s          0 s        231 s       5440 s          0 s
       #2  3240 MHz       4049 s          0 s        256 s       5202 s          0 s
       #3  3238 MHz       3668 s          0 s        231 s       5623 s          0 s
       #4  3246 MHz       3114 s          0 s        208 s       6207 s          0 s
       
  Memory: 15.620681762695312 GB (8309.21875 MB free)
  Uptime: 963.7 sec
  Load Avg:  1.7  1.63  1.12
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
    BogoMIPS:                             4890.84
    Flags:                                fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush mmx fxsr sse sse2 ht syscall nx mmxext fxsr_opt pdpe1gb rdtscp lm constant_tsc rep_good nopl tsc_reliable nonstop_tsc cpuid extd_apicid aperfmperf tsc_known_freq pni pclmulqdq ssse3 fma cx16 pcid sse4_1 sse4_2 movbe popcnt aes xsave avx f16c rdrand hypervisor lahf_lm cmp_legacy svm cr8_legacy abm sse4a misalignsse 3dnowprefetch osvw topoext vmmcall fsgsbase bmi1 avx2 smep bmi2 erms invpcid rdseed adx smap clflushopt clwb sha_ni xsaveopt xsavec xgetbv1 xsaves user_shstk clzero xsaveerptr rdpru arat npt nrip_save tsc_scale vmcb_clean flushbyasid decodeassists pausefilter pfthreshold v_vmsave_vmload umip vaes vpclmulqdq rdpid fsrm
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

