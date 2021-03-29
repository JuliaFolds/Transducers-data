# Multi-thread benchmark result

* Pull request commit: [`5d31eca53bb480de3fda2736c1379db7048f29ef`](https://github.com/JuliaFolds/Transducers.jl/commit/5d31eca53bb480de3fda2736c1379db7048f29ef)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/243> (Update */Manifest.toml)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 29 Mar 2021 - 01:21
    - Baseline: 29 Mar 2021 - 01:26
* Package commits:
    - Target: acd58d
    - Baseline: 0e46ec
* Julia commits:
    - Target: 69fcb5
    - Baseline: 69fcb5
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
| `["collect", "assoc", "basesize=1"]`                |                1.08 (5%) :x: |                   1.00 (1%)  |
| `["collect", "unordered", "basesize=1024"]`         | 0.94 (5%) :white_check_mark: | 0.90 (1%) :white_check_mark: |
| `["findfirst", "n=1000", "foldl"]`                  |                1.10 (5%) :x: |                   1.00 (1%)  |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` |                2.03 (5%) :x: |                2.00 (1%) :x: |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` |                   1.02 (5%)  | 0.96 (1%) :white_check_mark: |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 0.90 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["findfirst", "n=400", "foldl"]`                   | 0.92 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  |                   1.01 (5%)  |                1.02 (1%) :x: |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  |                1.06 (5%) :x: | 0.97 (1%) :white_check_mark: |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |                1.16 (5%) :x: |                1.17 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |                   1.01 (5%)  | 0.89 (1%) :white_check_mark: |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |                   1.00 (5%)  |                1.05 (1%) :x: |
| `["overhead", "stoppable=true"]`                    |                1.10 (5%) :x: |                   1.00 (1%)  |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |                1.11 (5%) :x: |                1.30 (1%) :x: |
| `["parallel_histogram", "comm", "basesize=16384"]`  | 0.94 (5%) :white_check_mark: | 0.95 (1%) :white_check_mark: |
| `["parallel_histogram", "comm", "basesize=8192"]`   | 0.95 (5%) :white_check_mark: |                1.14 (1%) :x: |
| `["parallel_histogram", "seq"]`                     |                1.05 (5%) :x: |                   1.00 (1%)  |
| `["partition_length_maximum", "rand", "reduce"]`    | 0.91 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["splitby", "count", "man"]`                       |                1.12 (5%) :x: |                   1.00 (1%)  |
| `["splitby", "count", "reduce"]`                    |                   0.98 (5%)  | 0.99 (1%) :white_check_mark: |
| `["sum", "uniform", "foldl"]`                       | 0.92 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["sum", "valley", "foldl"]`                        |                1.06 (5%) :x: |                   1.00 (1%)  |
| `["sum", "valley", "reduce", "basesize=256"]`       |                1.19 (5%) :x: |                   1.00 (1%)  |
| `["words", "nthreads=1"]`                           |                1.07 (5%) :x: |                   0.99 (1%)  |
| `["words", "nthreads=2"]`                           | 0.85 (5%) :white_check_mark: | 0.98 (1%) :white_check_mark: |
| `["words", "nthreads=4"]`                           | 0.89 (5%) :white_check_mark: |                   0.99 (1%)  |

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
Julia Version 1.5.4
Commit 69fcb5745b (2021-03-11 19:13 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 20.04.2 LTS
  uname: Linux 5.4.0-1041-azure #43-Ubuntu SMP Fri Feb 26 10:21:20 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz: 
              speed         user         nice          sys         idle          irq
       #1  2294 MHz      52958 s          9 s       2616 s      22459 s          0 s
       #2  2294 MHz      55888 s          9 s       2772 s      19266 s          0 s
       
  Memory: 6.791343688964844 GB (3783.08203125 MB free)
  Uptime: 794.0 sec
  Load Avg:  1.70703125  1.62646484375  1.07275390625
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, broadwell)
```

### Baseline
```
Julia Version 1.5.4
Commit 69fcb5745b (2021-03-11 19:13 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 20.04.2 LTS
  uname: Linux 5.4.0-1041-azure #43-Ubuntu SMP Fri Feb 26 10:21:20 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz: 
              speed         user         nice          sys         idle          irq
       #1  2294 MHz      77105 s          9 s       3304 s      31510 s          0 s
       #2  2294 MHz      82177 s          9 s       3428 s      26206 s          0 s
       
  Memory: 6.791343688964844 GB (3753.1640625 MB free)
  Uptime: 1134.0 sec
  Load Avg:  1.6552734375  1.576171875  1.21044921875
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, broadwell)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 29 Mar 2021 - 1:21
* Package commit: acd58d
* Julia commit: 69fcb5
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
| `["collect", "assoc", "basesize=1"]`                | 226.622 ms (5%) |         |  32.66 MiB (1%) |      286776 |
| `["collect", "assoc", "basesize=1024"]`             | 171.329 ms (5%) |         |   1.79 MiB (1%) |         569 |
| `["collect", "assoc", "basesize=32"]`               | 174.449 ms (5%) |         |   3.97 MiB (1%) |       13306 |
| `["collect", "seq"]`                                | 329.619 ms (5%) |         | 512.72 KiB (1%) |          15 |
| `["collect", "unordered", "basesize=1"]`            | 418.533 ms (5%) |         |  30.01 MiB (1%) |      360584 |
| `["collect", "unordered", "basesize=1024"]`         | 279.460 ms (5%) |         | 861.61 KiB (1%) |        4311 |
| `["collect", "unordered", "basesize=32"]`           | 204.890 ms (5%) |         |   1.48 MiB (1%) |       12716 |
| `["findfirst", "n=1000", "foldl"]`                  | 562.033 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 627.247 ms (5%) |         |   1.33 MiB (1%) |       23872 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 415.374 ms (5%) |         | 466.45 KiB (1%) |        8172 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 505.795 ms (5%) |         | 317.59 KiB (1%) |        5578 |
| `["findfirst", "n=400", "foldl"]`                   | 385.636 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 240.801 ms (5%) |         |   1.13 MiB (1%) |       20313 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 239.228 ms (5%) |         | 588.52 KiB (1%) |       10379 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 254.413 ms (5%) |         | 352.84 KiB (1%) |        6230 |
| `["findfirst", "n=500", "foldl"]`                   |  63.449 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 186.238 ms (5%) |         | 856.41 KiB (1%) |       14908 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 137.417 ms (5%) |         | 371.20 KiB (1%) |        6483 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  96.388 ms (5%) |         | 176.56 KiB (1%) |        3085 |
| `["overhead", "default"]`                           |  60.200 μs (5%) |         |  47.36 KiB (1%) |         382 |
| `["overhead", "stoppable=false"]`                   |  61.700 μs (5%) |         |  47.39 KiB (1%) |         382 |
| `["overhead", "stoppable=true"]`                    | 158.601 μs (5%) |         | 139.67 KiB (1%) |        2464 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   3.222 ms (5%) |         | 730.06 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   4.272 ms (5%) |         |   2.32 MiB (1%) |         225 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   3.422 ms (5%) |         |   1.43 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  13.785 ms (5%) |         | 999.20 KiB (1%) |         146 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  23.899 ms (5%) |         |   1.02 MiB (1%) |        1649 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  20.493 ms (5%) |         |   1.25 MiB (1%) |        1166 |
| `["parallel_histogram", "seq"]`                     |   5.795 ms (5%) |         | 364.61 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  32.108 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  15.934 ms (5%) |         |   2.66 KiB (1%) |          48 |
| `["splitby", "count", "foldl"]`                     |   3.504 ms (5%) |         |   96 bytes (1%) |           4 |
| `["splitby", "count", "man"]`                       |   1.541 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    | 743.303 μs (5%) |         |   2.84 KiB (1%) |          54 |
| `["sum", "random", "foldl"]`                        |  12.661 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "random", "reduce", "basesize=128"]`       |   6.365 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "random", "reduce", "basesize=256"]`       |   6.344 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "random", "reduce", "basesize=512"]`       |   5.927 ms (5%) |         |  25.30 KiB (1%) |         252 |
| `["sum", "uniform", "foldl"]`                       |  11.360 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   6.327 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   6.198 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   6.274 ms (5%) |         |  25.25 KiB (1%) |         251 |
| `["sum", "valley", "foldl"]`                        |  12.663 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "valley", "reduce", "basesize=128"]`       |   6.368 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   6.945 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   6.172 ms (5%) |         |  25.25 KiB (1%) |         251 |
| `["words", "nthreads=1"]`                           |  23.958 ms (5%) |         |  31.55 MiB (1%) |     1027680 |
| `["words", "nthreads=2"]`                           |  14.141 ms (5%) |         |  31.90 MiB (1%) |     1027716 |
| `["words", "nthreads=4"]`                           |  15.390 ms (5%) |         |  32.80 MiB (1%) |     1027913 |

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
Julia Version 1.5.4
Commit 69fcb5745b (2021-03-11 19:13 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 20.04.2 LTS
  uname: Linux 5.4.0-1041-azure #43-Ubuntu SMP Fri Feb 26 10:21:20 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz: 
              speed         user         nice          sys         idle          irq
       #1  2294 MHz      52958 s          9 s       2616 s      22459 s          0 s
       #2  2294 MHz      55888 s          9 s       2772 s      19266 s          0 s
       
  Memory: 6.791343688964844 GB (3783.08203125 MB free)
  Uptime: 794.0 sec
  Load Avg:  1.70703125  1.62646484375  1.07275390625
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, broadwell)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 29 Mar 2021 - 1:26
* Package commit: 0e46ec
* Julia commit: 69fcb5
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
| `["collect", "assoc", "basesize=1"]`                | 209.161 ms (5%) |         |  32.66 MiB (1%) |      286762 |
| `["collect", "assoc", "basesize=1024"]`             | 166.429 ms (5%) |         |   1.79 MiB (1%) |         569 |
| `["collect", "assoc", "basesize=32"]`               | 172.545 ms (5%) |         |   3.97 MiB (1%) |       13305 |
| `["collect", "seq"]`                                | 314.333 ms (5%) |         | 512.72 KiB (1%) |          15 |
| `["collect", "unordered", "basesize=1"]`            | 426.783 ms (5%) |         |  30.01 MiB (1%) |      360596 |
| `["collect", "unordered", "basesize=1024"]`         | 297.773 ms (5%) |         | 958.11 KiB (1%) |        7399 |
| `["collect", "unordered", "basesize=32"]`           | 205.405 ms (5%) |         |   1.48 MiB (1%) |       12821 |
| `["findfirst", "n=1000", "foldl"]`                  | 509.469 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 309.424 ms (5%) |         | 682.48 KiB (1%) |       11972 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 406.658 ms (5%) |         | 485.03 KiB (1%) |        8498 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 562.584 ms (5%) |         | 317.53 KiB (1%) |        5574 |
| `["findfirst", "n=400", "foldl"]`                   | 420.777 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 238.061 ms (5%) |         |   1.11 MiB (1%) |       19983 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 226.583 ms (5%) |         | 604.52 KiB (1%) |       10652 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 250.926 ms (5%) |         | 352.86 KiB (1%) |        6222 |
| `["findfirst", "n=500", "foldl"]`                   |  65.297 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 160.585 ms (5%) |         | 729.02 KiB (1%) |       12701 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 136.608 ms (5%) |         | 415.02 KiB (1%) |        7241 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  96.152 ms (5%) |         | 167.50 KiB (1%) |        2934 |
| `["overhead", "default"]`                           |  57.900 μs (5%) |         |  47.36 KiB (1%) |         382 |
| `["overhead", "stoppable=false"]`                   |  60.500 μs (5%) |         |  47.39 KiB (1%) |         382 |
| `["overhead", "stoppable=true"]`                    | 144.100 μs (5%) |         | 139.67 KiB (1%) |        2464 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   3.141 ms (5%) |         | 730.06 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   3.851 ms (5%) |         |   1.79 MiB (1%) |         213 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   3.423 ms (5%) |         |   1.43 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  14.612 ms (5%) |         |   1.03 MiB (1%) |         385 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  23.188 ms (5%) |         |   1.02 MiB (1%) |        1805 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  21.668 ms (5%) |         |   1.10 MiB (1%) |        1290 |
| `["parallel_histogram", "seq"]`                     |   5.517 ms (5%) |         | 364.61 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  33.335 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  17.487 ms (5%) |         |   2.66 KiB (1%) |          48 |
| `["splitby", "count", "foldl"]`                     |   3.551 ms (5%) |         |   96 bytes (1%) |           4 |
| `["splitby", "count", "man"]`                       |   1.372 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    | 756.204 μs (5%) |         |   2.88 KiB (1%) |          55 |
| `["sum", "random", "foldl"]`                        |  12.808 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "random", "reduce", "basesize=128"]`       |   6.310 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "random", "reduce", "basesize=256"]`       |   6.140 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "random", "reduce", "basesize=512"]`       |   6.069 ms (5%) |         |  25.30 KiB (1%) |         252 |
| `["sum", "uniform", "foldl"]`                       |  12.335 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   6.332 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   6.159 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   6.199 ms (5%) |         |  25.25 KiB (1%) |         251 |
| `["sum", "valley", "foldl"]`                        |  11.991 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "valley", "reduce", "basesize=128"]`       |   6.185 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   5.858 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   6.170 ms (5%) |         |  25.25 KiB (1%) |         251 |
| `["words", "nthreads=1"]`                           |  22.362 ms (5%) |         |  31.82 MiB (1%) |     1036841 |
| `["words", "nthreads=2"]`                           |  16.578 ms (5%) |         |  32.54 MiB (1%) |     1036921 |
| `["words", "nthreads=4"]`                           |  17.212 ms (5%) |         |  32.99 MiB (1%) |     1036990 |

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
Julia Version 1.5.4
Commit 69fcb5745b (2021-03-11 19:13 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 20.04.2 LTS
  uname: Linux 5.4.0-1041-azure #43-Ubuntu SMP Fri Feb 26 10:21:20 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz: 
              speed         user         nice          sys         idle          irq
       #1  2294 MHz      77105 s          9 s       3304 s      31510 s          0 s
       #2  2294 MHz      82177 s          9 s       3428 s      26206 s          0 s
       
  Memory: 6.791343688964844 GB (3753.1640625 MB free)
  Uptime: 1134.0 sec
  Load Avg:  1.6552734375  1.576171875  1.21044921875
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, broadwell)
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
    CPU MHz:                         2294.682
    BogoMIPS:                        4589.36
    Hypervisor vendor:               Microsoft
    Virtualization type:             full
    L1d cache:                       64 KiB
    L1i cache:                       64 KiB
    L2 cache:                        512 KiB
    L3 cache:                        50 MiB
    NUMA node0 CPU(s):               0,1
    Vulnerability Itlb multihit:     KVM: Vulnerable
    Vulnerability L1tf:              Mitigation; PTE Inversion
    Vulnerability Mds:               Mitigation; Clear CPU buffers; SMT Host state unknown
    Vulnerability Meltdown:          Mitigation; PTI
    Vulnerability Spec store bypass: Vulnerable
    Vulnerability Spectre v1:        Mitigation; usercopy/swapgs barriers and __user pointer sanitization
    Vulnerability Spectre v2:        Mitigation; Full generic retpoline, STIBP disabled, RSB filling
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

