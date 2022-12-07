# Multi-thread benchmark result

* Pull request commit: [`2e725426deafc4705b76074cdf2d175d10094bbf`](https://github.com/JuliaFolds/Transducers.jl/commit/2e725426deafc4705b76074cdf2d175d10094bbf)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/243> (Update */Manifest.toml)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 7 Dec 2022 - 01:54
    - Baseline: 7 Dec 2022 - 01:59
* Package commits:
    - Target: 873aa0
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
| `["findfirst", "n=1000", "reduce", "basesize=128"]` |                1.60 (5%) :x: |                1.57 (1%) :x: |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 0.86 (5%) :white_check_mark: | 0.92 (1%) :white_check_mark: |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  |                   0.96 (5%)  |                1.02 (1%) :x: |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 0.93 (5%) :white_check_mark: | 0.97 (1%) :white_check_mark: |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 0.79 (5%) :white_check_mark: | 0.90 (1%) :white_check_mark: |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 0.67 (5%) :white_check_mark: | 0.83 (1%) :white_check_mark: |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 0.31 (5%) :white_check_mark: | 0.43 (1%) :white_check_mark: |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 0.45 (5%) :white_check_mark: | 0.59 (1%) :white_check_mark: |
| `["parallel_histogram", "assoc", "basesize=16384"]` | 0.91 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["parallel_histogram", "assoc", "basesize=4096"]`  | 0.93 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["parallel_histogram", "assoc", "basesize=8192"]`  | 0.94 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["parallel_histogram", "comm", "basesize=16384"]`  |                   0.99 (5%)  |                1.03 (1%) :x: |
| `["parallel_histogram", "comm", "basesize=8192"]`   | 0.84 (5%) :white_check_mark: |                1.24 (1%) :x: |
| `["parallel_histogram", "seq"]`                     | 0.91 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["splitby", "count", "foldl"]`                     | 0.85 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["splitby", "count", "man"]`                       | 0.70 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["splitby", "count", "reduce"]`                    | 0.88 (5%) :white_check_mark: |                1.03 (1%) :x: |
| `["sum", "valley", "reduce", "basesize=128"]`       | 0.91 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["words", "nthreads=1"]`                           | 0.94 (5%) :white_check_mark: |                   1.01 (1%)  |
| `["words", "nthreads=2"]`                           |                   1.00 (5%)  |                1.02 (1%) :x: |

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
      Ubuntu 22.04.1 LTS
  uname: Linux 5.15.0-1023-azure #29-Ubuntu SMP Wed Oct 19 22:37:08 UTC 2022 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz       5333 s          0 s        243 s       2783 s          0 s
       #2  2095 MHz       5388 s          0 s        246 s       2704 s          0 s
       
  Memory: 6.781219482421875 GB (3810.06640625 MB free)
  Uptime: 842.47 sec
  Load Avg:  1.5  1.49  0.93
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, skylake-avx512)
```

### Baseline
```
Julia Version 1.7.3
Commit 742b9abb4d (2022-05-06 12:58 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 22.04.1 LTS
  uname: Linux 5.15.0-1023-azure #29-Ubuntu SMP Wed Oct 19 22:37:08 UTC 2022 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz       7533 s          0 s        322 s       3717 s          0 s
       #2  2095 MHz       8085 s          0 s        314 s       3154 s          0 s
       
  Memory: 6.781219482421875 GB (3739.01171875 MB free)
  Uptime: 1164.56 sec
  Load Avg:  1.71  1.69  1.19
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, skylake-avx512)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 7 Dec 2022 - 1:54
* Package commit: 873aa0
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
| `["collect", "assoc", "basesize=1"]`                | 292.822 ms (5%) |         |  25.97 MiB (1%) |      306790 |
| `["collect", "assoc", "basesize=1024"]`             | 234.827 ms (5%) |         |   2.61 MiB (1%) |         456 |
| `["collect", "assoc", "basesize=32"]`               | 237.618 ms (5%) |         |   4.82 MiB (1%) |       11709 |
| `["collect", "seq"]`                                | 452.500 ms (5%) |         | 812.73 KiB (1%) |          11 |
| `["collect", "unordered", "basesize=1"]`            | 397.583 ms (5%) |         |  23.88 MiB (1%) |      412387 |
| `["collect", "unordered", "basesize=1024"]`         | 245.885 ms (5%) |         |   1.00 MiB (1%) |         892 |
| `["collect", "unordered", "basesize=32"]`           | 257.172 ms (5%) |         |   1.58 MiB (1%) |       14572 |
| `["findfirst", "n=1000", "foldl"]`                  | 729.658 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 661.386 ms (5%) |         | 365.77 KiB (1%) |        5115 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 494.670 ms (5%) |         | 157.20 KiB (1%) |        2193 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 661.898 ms (5%) |         | 108.55 KiB (1%) |        1509 |
| `["findfirst", "n=400", "foldl"]`                   | 546.989 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 295.702 ms (5%) |         | 383.88 KiB (1%) |        5465 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 291.492 ms (5%) |         | 200.86 KiB (1%) |        2873 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 365.583 ms (5%) |         | 137.36 KiB (1%) |        1948 |
| `["findfirst", "n=500", "foldl"]`                   |  92.830 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 122.923 ms (5%) |         | 172.02 KiB (1%) |        2343 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |  87.565 ms (5%) |         |  71.38 KiB (1%) |         970 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 125.042 ms (5%) |         |  56.89 KiB (1%) |         780 |
| `["overhead", "default"]`                           |  82.506 μs (5%) |         |  32.77 KiB (1%) |         419 |
| `["overhead", "stoppable=false"]`                   |  84.306 μs (5%) |         |  32.75 KiB (1%) |         418 |
| `["overhead", "stoppable=true"]`                    |  95.907 μs (5%) |         |  44.25 KiB (1%) |         610 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   3.481 ms (5%) |         | 728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   4.443 ms (5%) |         |   2.05 MiB (1%) |         221 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   3.999 ms (5%) |         |   1.42 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  20.759 ms (5%) |         |   1.61 MiB (1%) |        3531 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  27.714 ms (5%) |         |   1.25 MiB (1%) |        7115 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  20.448 ms (5%) |         |   1.58 MiB (1%) |        2303 |
| `["parallel_histogram", "seq"]`                     |   6.221 ms (5%) |         | 364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  39.851 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  20.189 ms (5%) |         |  736 bytes (1%) |          11 |
| `["splitby", "count", "foldl"]`                     |   2.214 ms (5%) |         |                 |             |
| `["splitby", "count", "man"]`                       |   1.374 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    |   1.066 ms (5%) |         |   1.09 KiB (1%) |          19 |
| `["sum", "random", "foldl"]`                        |  17.942 ms (5%) |         |                 |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   9.697 ms (5%) |         |  74.11 KiB (1%) |        1102 |
| `["sum", "random", "reduce", "basesize=256"]`       |   9.344 ms (5%) |         |  36.73 KiB (1%) |         546 |
| `["sum", "random", "reduce", "basesize=512"]`       |   8.975 ms (5%) |         |  18.11 KiB (1%) |         270 |
| `["sum", "uniform", "foldl"]`                       |  18.783 ms (5%) |         |                 |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   9.147 ms (5%) |         |  74.20 KiB (1%) |        1105 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   9.475 ms (5%) |         |  36.77 KiB (1%) |         547 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   9.387 ms (5%) |         |  18.00 KiB (1%) |         267 |
| `["sum", "valley", "foldl"]`                        |  18.336 ms (5%) |         |                 |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   9.077 ms (5%) |         |  74.17 KiB (1%) |        1104 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   9.304 ms (5%) |         |  36.77 KiB (1%) |         547 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   9.160 ms (5%) |         |  18.06 KiB (1%) |         269 |
| `["words", "nthreads=1"]`                           |  26.364 ms (5%) |         |  31.74 MiB (1%) |     1034125 |
| `["words", "nthreads=2"]`                           |  17.275 ms (5%) |         |  32.45 MiB (1%) |     1034205 |
| `["words", "nthreads=4"]`                           |  17.230 ms (5%) |         |  32.90 MiB (1%) |     1034292 |

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
      Ubuntu 22.04.1 LTS
  uname: Linux 5.15.0-1023-azure #29-Ubuntu SMP Wed Oct 19 22:37:08 UTC 2022 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz       5333 s          0 s        243 s       2783 s          0 s
       #2  2095 MHz       5388 s          0 s        246 s       2704 s          0 s
       
  Memory: 6.781219482421875 GB (3810.06640625 MB free)
  Uptime: 842.47 sec
  Load Avg:  1.5  1.49  0.93
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, skylake-avx512)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 7 Dec 2022 - 1:59
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
| `["collect", "assoc", "basesize=1"]`                | 295.025 ms (5%) |         |  25.97 MiB (1%) |      306850 |
| `["collect", "assoc", "basesize=1024"]`             | 239.259 ms (5%) |         |   2.61 MiB (1%) |         455 |
| `["collect", "assoc", "basesize=32"]`               | 243.421 ms (5%) |         |   4.82 MiB (1%) |       11710 |
| `["collect", "seq"]`                                | 468.431 ms (5%) |         | 812.73 KiB (1%) |          11 |
| `["collect", "unordered", "basesize=1"]`            | 415.407 ms (5%) |         |  23.88 MiB (1%) |      412201 |
| `["collect", "unordered", "basesize=1024"]`         | 254.688 ms (5%) |         |   1.00 MiB (1%) |         862 |
| `["collect", "unordered", "basesize=32"]`           | 269.439 ms (5%) |         |   1.58 MiB (1%) |       14578 |
| `["findfirst", "n=1000", "foldl"]`                  | 746.401 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 412.287 ms (5%) |         | 232.52 KiB (1%) |        3265 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 577.703 ms (5%) |         | 170.17 KiB (1%) |        2372 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 676.217 ms (5%) |         | 108.55 KiB (1%) |        1509 |
| `["findfirst", "n=400", "foldl"]`                   | 554.135 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 308.675 ms (5%) |         | 376.98 KiB (1%) |        5379 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 313.755 ms (5%) |         | 207.41 KiB (1%) |        2967 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 460.418 ms (5%) |         | 153.31 KiB (1%) |        2200 |
| `["findfirst", "n=500", "foldl"]`                   |  95.480 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 183.748 ms (5%) |         | 206.97 KiB (1%) |        2885 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 280.364 ms (5%) |         | 167.20 KiB (1%) |        2347 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 277.672 ms (5%) |         |  96.55 KiB (1%) |        1336 |
| `["overhead", "default"]`                           |  83.006 μs (5%) |         |  32.70 KiB (1%) |         417 |
| `["overhead", "stoppable=false"]`                   |  84.706 μs (5%) |         |  32.72 KiB (1%) |         417 |
| `["overhead", "stoppable=true"]`                    |  97.207 μs (5%) |         |  44.22 KiB (1%) |         609 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   3.817 ms (5%) |         | 728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   4.782 ms (5%) |         |   2.05 MiB (1%) |         222 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   4.272 ms (5%) |         |   1.42 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  21.071 ms (5%) |         |   1.57 MiB (1%) |        2163 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  28.362 ms (5%) |         |   1.26 MiB (1%) |        7351 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  24.283 ms (5%) |         |   1.27 MiB (1%) |        5565 |
| `["parallel_histogram", "seq"]`                     |   6.811 ms (5%) |         | 364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  40.069 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  20.147 ms (5%) |         |  736 bytes (1%) |          11 |
| `["splitby", "count", "foldl"]`                     |   2.610 ms (5%) |         |                 |             |
| `["splitby", "count", "man"]`                       |   1.952 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    |   1.213 ms (5%) |         |   1.06 KiB (1%) |          18 |
| `["sum", "random", "foldl"]`                        |  18.557 ms (5%) |         |                 |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   9.521 ms (5%) |         |  74.20 KiB (1%) |        1105 |
| `["sum", "random", "reduce", "basesize=256"]`       |   9.473 ms (5%) |         |  36.77 KiB (1%) |         547 |
| `["sum", "random", "reduce", "basesize=512"]`       |   9.337 ms (5%) |         |  18.11 KiB (1%) |         270 |
| `["sum", "uniform", "foldl"]`                       |  18.850 ms (5%) |         |                 |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   9.184 ms (5%) |         |  74.17 KiB (1%) |        1104 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   9.031 ms (5%) |         |  36.80 KiB (1%) |         548 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   8.985 ms (5%) |         |  18.03 KiB (1%) |         268 |
| `["sum", "valley", "foldl"]`                        |  18.330 ms (5%) |         |                 |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   9.931 ms (5%) |         |  74.02 KiB (1%) |        1099 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   9.625 ms (5%) |         |  36.77 KiB (1%) |         547 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   9.466 ms (5%) |         |  18.03 KiB (1%) |         268 |
| `["words", "nthreads=1"]`                           |  28.163 ms (5%) |         |  31.47 MiB (1%) |     1025176 |
| `["words", "nthreads=2"]`                           |  17.303 ms (5%) |         |  31.83 MiB (1%) |     1025245 |
| `["words", "nthreads=4"]`                           |  17.025 ms (5%) |         |  32.72 MiB (1%) |     1025411 |

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
      Ubuntu 22.04.1 LTS
  uname: Linux 5.15.0-1023-azure #29-Ubuntu SMP Wed Oct 19 22:37:08 UTC 2022 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz       7533 s          0 s        322 s       3717 s          0 s
       #2  2095 MHz       8085 s          0 s        314 s       3154 s          0 s
       
  Memory: 6.781219482421875 GB (3739.01171875 MB free)
  Uptime: 1164.56 sec
  Load Avg:  1.71  1.69  1.19
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, skylake-avx512)
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
    Model name:                      Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz
    CPU family:                      6
    Model:                           85
    Thread(s) per core:              1
    Core(s) per socket:              2
    Socket(s):                       1
    Stepping:                        4
    BogoMIPS:                        4190.44
    Flags:                           fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush mmx fxsr sse sse2 ss ht syscall nx pdpe1gb rdtscp lm constant_tsc rep_good nopl xtopology cpuid pni pclmulqdq ssse3 fma cx16 pcid sse4_1 sse4_2 movbe popcnt aes xsave avx f16c rdrand hypervisor lahf_lm abm 3dnowprefetch invpcid_single pti fsgsbase bmi1 hle avx2 smep bmi2 erms invpcid rtm avx512f avx512dq rdseed adx smap clflushopt avx512cd avx512bw avx512vl xsaveopt xsavec xsaves md_clear
    Hypervisor vendor:               Microsoft
    Virtualization type:             full
    L1d cache:                       64 KiB (2 instances)
    L1i cache:                       64 KiB (2 instances)
    L2 cache:                        2 MiB (2 instances)
    L3 cache:                        35.8 MiB (1 instance)
    NUMA node(s):                    1
    NUMA node0 CPU(s):               0,1
    Vulnerability Itlb multihit:     KVM: Mitigation: VMX unsupported
    Vulnerability L1tf:              Mitigation; PTE Inversion
    Vulnerability Mds:               Mitigation; Clear CPU buffers; SMT Host state unknown
    Vulnerability Meltdown:          Mitigation; PTI
    Vulnerability Mmio stale data:   Vulnerable: Clear CPU buffers attempted, no microcode; SMT Host state unknown
    Vulnerability Retbleed:          Vulnerable
    Vulnerability Spec store bypass: Vulnerable
    Vulnerability Spectre v1:        Mitigation; usercopy/swapgs barriers and __user pointer sanitization
    Vulnerability Spectre v2:        Mitigation; Retpolines, STIBP disabled, RSB filling, PBRSB-eIBRS Not affected
    Vulnerability Srbds:             Not affected
    Vulnerability Tsx async abort:   Mitigation; Clear CPU buffers; SMT Host state unknown
    

| Cpu Property       | Value                                                   |
|:------------------ |:------------------------------------------------------- |
| Brand              | Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz           |
| Vendor             | :Intel                                                  |
| Architecture       | :Skylake                                                |
| Model              | Family: 0x06, Model: 0x55, Stepping: 0x04, Type: 0x00   |
| Cores              | 2 physical cores, 2 logical cores (on executing CPU)    |
|                    | No Hyperthreading hardware capability detected          |
| Clock Frequencies  | Not supported by CPU                                    |
| Data Cache         | Level 1:3 : (32, 1024, 36608) kbytes                    |
|                    | 64 byte cache line size                                 |
| Address Size       | 48 bits virtual, 46 bits physical                       |
| SIMD               | 512 bit = 64 byte max. SIMD vector size                 |
| Time Stamp Counter | TSC is accessible via `rdtsc`                           |
|                    | TSC increased at every clock cycle (non-invariant TSC)  |
| Perf. Monitoring   | Performance Monitoring Counters (PMC) are not supported |
| Hypervisor         | Yes, Microsoft                                          |

