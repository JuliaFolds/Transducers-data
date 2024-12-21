# Multi-thread benchmark result

* Pull request commit: [`514251352760906ea47d728e74e2b3523b572dad`](https://github.com/JuliaFolds/Transducers.jl/commit/514251352760906ea47d728e74e2b3523b572dad)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/243> (Update */Manifest.toml)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 21 Dec 2024 - 01:50
    - Baseline: 21 Dec 2024 - 01:55
* Package commits:
    - Target: 8abba5
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
| `["findfirst", "n=1000", "reduce", "basesize=128"]` |                   1.03 (5%)  |                1.03 (1%) :x: |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` |                1.64 (5%) :x: |                1.47 (1%) :x: |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` |                1.31 (5%) :x: |                1.31 (1%) :x: |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  |                1.06 (5%) :x: |                1.07 (1%) :x: |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  |                1.08 (5%) :x: |                1.11 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |                1.17 (5%) :x: |                1.02 (1%) :x: |
| `["overhead", "stoppable=false"]`                   | 0.94 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["parallel_histogram", "comm", "basesize=16384"]`  |                   0.99 (5%)  | 0.99 (1%) :white_check_mark: |
| `["splitby", "count", "reduce"]`                    |                   1.00 (5%)  | 0.94 (1%) :white_check_mark: |
| `["words", "nthreads=2"]`                           |                1.12 (5%) :x: |                1.01 (1%) :x: |
| `["words", "nthreads=4"]`                           |                1.08 (5%) :x: |                   1.00 (1%)  |

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
       #1  3289 MHz       2044 s          0 s        157 s       4419 s          0 s
       #2  3240 MHz       2642 s          0 s        191 s       3812 s          0 s
       #3  3237 MHz       2284 s          0 s        198 s       4194 s          0 s
       #4  3238 MHz       2991 s          0 s        244 s       3401 s          0 s
       
  Memory: 15.615280151367188 GB (8585.3125 MB free)
  Uptime: 672.9 sec
  Load Avg:  1.76  1.55  0.91
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
       #1  3243 MHz       3053 s          0 s        217 s       6297 s          0 s
       #2  3277 MHz       3563 s          0 s        286 s       5743 s          0 s
       #3  3243 MHz       3657 s          0 s        256 s       5712 s          0 s
       #4  3243 MHz       4296 s          0 s        303 s       4984 s          0 s
       
  Memory: 15.615280151367188 GB (8619.5078125 MB free)
  Uptime: 968.21 sec
  Load Avg:  1.8  1.7  1.16
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, znver3)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 21 Dec 2024 - 1:50
* Package commit: 8abba5
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
| `["collect", "assoc", "basesize=1"]`                | 149.422 ms (5%) |         |   4.36 MiB (1%) |       32800 |
| `["collect", "assoc", "basesize=1024"]`             | 148.142 ms (5%) |         |   1.09 MiB (1%) |          53 |
| `["collect", "assoc", "basesize=32"]`               | 148.305 ms (5%) |         |   1.48 MiB (1%) |        1052 |
| `["collect", "seq"]`                                | 296.045 ms (5%) |         | 256.05 KiB (1%) |           2 |
| `["collect", "unordered", "basesize=1"]`            | 250.580 ms (5%) |         |  23.71 MiB (1%) |      406897 |
| `["collect", "unordered", "basesize=1024"]`         | 157.834 ms (5%) |         |   1.01 MiB (1%) |        1049 |
| `["collect", "unordered", "basesize=32"]`           | 169.875 ms (5%) |         |   1.60 MiB (1%) |       15424 |
| `["findfirst", "n=1000", "foldl"]`                  | 508.341 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 277.291 ms (5%) |         | 232.73 KiB (1%) |        3272 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 558.991 ms (5%) |         | 231.83 KiB (1%) |        3265 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 456.071 ms (5%) |         | 106.97 KiB (1%) |        1509 |
| `["findfirst", "n=400", "foldl"]`                   | 380.050 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 209.981 ms (5%) |         | 410.17 KiB (1%) |        5811 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 198.777 ms (5%) |         | 200.86 KiB (1%) |        2873 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 254.676 ms (5%) |         | 138.98 KiB (1%) |        1971 |
| `["findfirst", "n=500", "foldl"]`                   |  65.386 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 139.737 ms (5%) |         | 236.80 KiB (1%) |        3275 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 123.825 ms (5%) |         | 118.89 KiB (1%) |        1639 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  94.287 ms (5%) |         |  63.69 KiB (1%) |         866 |
| `["overhead", "default"]`                           |  52.418 μs (5%) |         |  32.70 KiB (1%) |         417 |
| `["overhead", "stoppable=false"]`                   |  49.703 μs (5%) |         |  32.72 KiB (1%) |         417 |
| `["overhead", "stoppable=true"]`                    |  58.098 μs (5%) |         |  44.25 KiB (1%) |         610 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   2.395 ms (5%) |         | 728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   2.945 ms (5%) |         |   1.79 MiB (1%) |         216 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   2.675 ms (5%) |         |   1.42 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |   8.365 ms (5%) |         |   1.56 MiB (1%) |        1807 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  12.635 ms (5%) |         |   1.33 MiB (1%) |        9767 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  11.649 ms (5%) |         |   1.27 MiB (1%) |        7807 |
| `["parallel_histogram", "seq"]`                     |   4.255 ms (5%) |         | 364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  31.303 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  15.705 ms (5%) |         |  736 bytes (1%) |          11 |
| `["splitby", "count", "foldl"]`                     |   1.745 ms (5%) |         |                 |             |
| `["splitby", "count", "man"]`                       |   1.141 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    | 719.842 μs (5%) |         |   1.03 KiB (1%) |          18 |
| `["sum", "random", "foldl"]`                        |  11.101 ms (5%) |         |                 |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   5.669 ms (5%) |         |  74.14 KiB (1%) |        1103 |
| `["sum", "random", "reduce", "basesize=256"]`       |   5.620 ms (5%) |         |  36.73 KiB (1%) |         546 |
| `["sum", "random", "reduce", "basesize=512"]`       |   5.584 ms (5%) |         |  18.08 KiB (1%) |         269 |
| `["sum", "uniform", "foldl"]`                       |  10.937 ms (5%) |         |                 |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   5.590 ms (5%) |         |  74.14 KiB (1%) |        1103 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   5.541 ms (5%) |         |  36.70 KiB (1%) |         545 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   5.506 ms (5%) |         |  18.03 KiB (1%) |         268 |
| `["sum", "valley", "foldl"]`                        |  11.167 ms (5%) |         |                 |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   5.717 ms (5%) |         |  74.08 KiB (1%) |        1101 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   5.662 ms (5%) |         |  36.77 KiB (1%) |         547 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   5.644 ms (5%) |         |  18.06 KiB (1%) |         269 |
| `["words", "nthreads=1"]`                           |  14.449 ms (5%) |         |  31.95 MiB (1%) |     1041519 |
| `["words", "nthreads=2"]`                           |  10.481 ms (5%) |         |  32.66 MiB (1%) |     1041592 |
| `["words", "nthreads=4"]`                           |  10.871 ms (5%) |         |  33.11 MiB (1%) |     1041665 |

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
       #1  3289 MHz       2044 s          0 s        157 s       4419 s          0 s
       #2  3240 MHz       2642 s          0 s        191 s       3812 s          0 s
       #3  3237 MHz       2284 s          0 s        198 s       4194 s          0 s
       #4  3238 MHz       2991 s          0 s        244 s       3401 s          0 s
       
  Memory: 15.615280151367188 GB (8585.3125 MB free)
  Uptime: 672.9 sec
  Load Avg:  1.76  1.55  0.91
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, znver3)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 21 Dec 2024 - 1:55
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
| `["collect", "assoc", "basesize=1"]`                | 149.825 ms (5%) |         |   4.36 MiB (1%) |       32800 |
| `["collect", "assoc", "basesize=1024"]`             | 148.374 ms (5%) |         |   1.09 MiB (1%) |          53 |
| `["collect", "assoc", "basesize=32"]`               | 148.318 ms (5%) |         |   1.48 MiB (1%) |        1052 |
| `["collect", "seq"]`                                | 296.007 ms (5%) |         | 256.05 KiB (1%) |           2 |
| `["collect", "unordered", "basesize=1"]`            | 247.019 ms (5%) |         |  23.72 MiB (1%) |      407023 |
| `["collect", "unordered", "basesize=1024"]`         | 158.074 ms (5%) |         |   1.01 MiB (1%) |        1097 |
| `["collect", "unordered", "basesize=32"]`           | 170.081 ms (5%) |         |   1.60 MiB (1%) |       15357 |
| `["findfirst", "n=1000", "foldl"]`                  | 508.191 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 269.961 ms (5%) |         | 224.89 KiB (1%) |        3172 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 340.519 ms (5%) |         | 157.20 KiB (1%) |        2193 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 347.588 ms (5%) |         |  81.42 KiB (1%) |        1149 |
| `["findfirst", "n=400", "foldl"]`                   | 380.703 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 198.923 ms (5%) |         | 383.84 KiB (1%) |        5465 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 198.799 ms (5%) |         | 200.86 KiB (1%) |        2873 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 234.753 ms (5%) |         | 124.98 KiB (1%) |        1787 |
| `["findfirst", "n=500", "foldl"]`                   |  65.395 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 119.058 ms (5%) |         | 231.78 KiB (1%) |        3159 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 120.296 ms (5%) |         | 118.86 KiB (1%) |        1638 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  94.251 ms (5%) |         |  63.66 KiB (1%) |         865 |
| `["overhead", "default"]`                           |  53.380 μs (5%) |         |  32.73 KiB (1%) |         418 |
| `["overhead", "stoppable=false"]`                   |  52.799 μs (5%) |         |  32.75 KiB (1%) |         418 |
| `["overhead", "stoppable=true"]`                    |  59.200 μs (5%) |         |  44.25 KiB (1%) |         610 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   2.415 ms (5%) |         | 728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   2.954 ms (5%) |         |   1.79 MiB (1%) |         216 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   2.689 ms (5%) |         |   1.42 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |   8.422 ms (5%) |         |   1.58 MiB (1%) |        2437 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  12.770 ms (5%) |         |   1.32 MiB (1%) |        9452 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  11.741 ms (5%) |         |   1.27 MiB (1%) |        7198 |
| `["parallel_histogram", "seq"]`                     |   4.256 ms (5%) |         | 364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  31.305 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  15.696 ms (5%) |         |  736 bytes (1%) |          11 |
| `["splitby", "count", "foldl"]`                     |   1.744 ms (5%) |         |                 |             |
| `["splitby", "count", "man"]`                       |   1.140 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    | 723.138 μs (5%) |         |   1.09 KiB (1%) |          19 |
| `["sum", "random", "foldl"]`                        |  11.033 ms (5%) |         |                 |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   5.621 ms (5%) |         |  74.14 KiB (1%) |        1103 |
| `["sum", "random", "reduce", "basesize=256"]`       |   5.593 ms (5%) |         |  36.64 KiB (1%) |         543 |
| `["sum", "random", "reduce", "basesize=512"]`       |   5.550 ms (5%) |         |  18.05 KiB (1%) |         268 |
| `["sum", "uniform", "foldl"]`                       |  10.956 ms (5%) |         |                 |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   5.589 ms (5%) |         |  73.98 KiB (1%) |        1098 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   5.542 ms (5%) |         |  36.77 KiB (1%) |         547 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   5.506 ms (5%) |         |  18.03 KiB (1%) |         268 |
| `["sum", "valley", "foldl"]`                        |  11.166 ms (5%) |         |                 |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   5.728 ms (5%) |         |  74.02 KiB (1%) |        1099 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   5.658 ms (5%) |         |  36.77 KiB (1%) |         547 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   5.641 ms (5%) |         |  18.03 KiB (1%) |         268 |
| `["words", "nthreads=1"]`                           |  14.300 ms (5%) |         |  31.88 MiB (1%) |     1038504 |
| `["words", "nthreads=2"]`                           |   9.349 ms (5%) |         |  32.24 MiB (1%) |     1038540 |
| `["words", "nthreads=4"]`                           |  10.034 ms (5%) |         |  33.14 MiB (1%) |     1038705 |

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
       #1  3243 MHz       3053 s          0 s        217 s       6297 s          0 s
       #2  3277 MHz       3563 s          0 s        286 s       5743 s          0 s
       #3  3243 MHz       3657 s          0 s        256 s       5712 s          0 s
       #4  3243 MHz       4296 s          0 s        303 s       4984 s          0 s
       
  Memory: 15.615280151367188 GB (8619.5078125 MB free)
  Uptime: 968.21 sec
  Load Avg:  1.8  1.7  1.16
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
    BogoMIPS:                             4890.85
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

