# Multi-thread benchmark result

* Pull request commit: [`cd9d9f57db80c67bc2f6cdaa688e322e22dbc97d`](https://github.com/JuliaFolds/Transducers.jl/commit/cd9d9f57db80c67bc2f6cdaa688e322e22dbc97d)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/243> (Update */Manifest.toml)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 28 Mar 2021 - 01:19
    - Baseline: 28 Mar 2021 - 01:25
* Package commits:
    - Target: 6f49e7
    - Baseline: b7b120
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
| `["collect", "unordered", "basesize=1024"]`         |                   1.00 (5%)  |                1.02 (1%) :x: |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` |                1.34 (5%) :x: |                1.33 (1%) :x: |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 0.91 (5%) :white_check_mark: | 0.96 (1%) :white_check_mark: |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 0.81 (5%) :white_check_mark: | 0.91 (1%) :white_check_mark: |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  |                1.08 (5%) :x: |                1.14 (1%) :x: |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  |                1.06 (5%) :x: |                   1.00 (1%)  |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  |                   0.95 (5%)  | 0.91 (1%) :white_check_mark: |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |                1.45 (5%) :x: |                1.26 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |                1.16 (5%) :x: |                1.01 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |                1.63 (5%) :x: |                1.43 (1%) :x: |
| `["overhead", "stoppable=true"]`                    |                1.06 (5%) :x: |                   1.00 (1%)  |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |                   0.98 (5%)  | 0.87 (1%) :white_check_mark: |
| `["parallel_histogram", "comm", "basesize=16384"]`  |                1.05 (5%) :x: | 0.84 (1%) :white_check_mark: |
| `["parallel_histogram", "comm", "basesize=4096"]`   |                1.34 (5%) :x: |                1.01 (1%) :x: |
| `["parallel_histogram", "comm", "basesize=8192"]`   | 0.91 (5%) :white_check_mark: | 0.99 (1%) :white_check_mark: |
| `["partition_length_maximum", "rand", "foldl"]`     | 0.94 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["splitby", "count", "man"]`                       |                1.08 (5%) :x: |                   1.00 (1%)  |
| `["sum", "random", "foldl"]`                        | 0.92 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["sum", "random", "reduce", "basesize=512"]`       | 0.90 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["sum", "uniform", "foldl"]`                       | 0.92 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["sum", "valley", "foldl"]`                        | 0.94 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["sum", "valley", "reduce", "basesize=128"]`       |                1.07 (5%) :x: |                   1.00 (1%)  |
| `["words", "nthreads=2"]`                           |                   1.03 (5%)  |                1.02 (1%) :x: |
| `["words", "nthreads=4"]`                           |                   0.97 (5%)  |                1.01 (1%) :x: |

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
       #1  2294 MHz      54230 s         18 s       2424 s      27544 s          0 s
       #2  2294 MHz      57832 s          7 s       2559 s      23970 s          0 s
       
  Memory: 6.791339874267578 GB (3736.75390625 MB free)
  Uptime: 858.0 sec
  Load Avg:  1.63671875  1.51220703125  0.9658203125
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
       #1  2294 MHz      81219 s         18 s       3048 s      35180 s          0 s
       #2  2294 MHz      83040 s          7 s       3190 s      33459 s          0 s
       
  Memory: 6.791339874267578 GB (3648.72265625 MB free)
  Uptime: 1212.0 sec
  Load Avg:  1.69873046875  1.568359375  1.15966796875
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, broadwell)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 28 Mar 2021 - 1:19
* Package commit: 6f49e7
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
| `["collect", "assoc", "basesize=1"]`                | 246.296 ms (5%) |         |  32.66 MiB (1%) |      286778 |
| `["collect", "assoc", "basesize=1024"]`             | 192.574 ms (5%) |         |   1.79 MiB (1%) |         569 |
| `["collect", "assoc", "basesize=32"]`               | 199.401 ms (5%) |         |   3.97 MiB (1%) |       13305 |
| `["collect", "seq"]`                                | 387.207 ms (5%) |         | 512.72 KiB (1%) |          15 |
| `["collect", "unordered", "basesize=1"]`            | 465.775 ms (5%) |         |  30.01 MiB (1%) |      360649 |
| `["collect", "unordered", "basesize=1024"]`         | 317.064 ms (5%) |         | 904.58 KiB (1%) |        5686 |
| `["collect", "unordered", "basesize=32"]`           | 238.038 ms (5%) |         |   1.47 MiB (1%) |       12592 |
| `["findfirst", "n=1000", "foldl"]`                  | 599.179 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 679.778 ms (5%) |         |   1.26 MiB (1%) |       22556 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 424.663 ms (5%) |         | 466.42 KiB (1%) |        8171 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 526.122 ms (5%) |         | 312.86 KiB (1%) |        5490 |
| `["findfirst", "n=400", "foldl"]`                   | 464.416 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 275.733 ms (5%) |         |   1.22 MiB (1%) |       21978 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 269.940 ms (5%) |         | 593.39 KiB (1%) |       10475 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 273.000 ms (5%) |         | 343.61 KiB (1%) |        6060 |
| `["findfirst", "n=500", "foldl"]`                   |  75.739 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 103.703 ms (5%) |         | 479.02 KiB (1%) |        8354 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 147.364 ms (5%) |         | 359.36 KiB (1%) |        6265 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 203.666 ms (5%) |         | 295.94 KiB (1%) |        5161 |
| `["overhead", "default"]`                           |  62.501 μs (5%) |         |  47.36 KiB (1%) |         382 |
| `["overhead", "stoppable=false"]`                   |  65.001 μs (5%) |         |  47.39 KiB (1%) |         382 |
| `["overhead", "stoppable=true"]`                    | 180.303 μs (5%) |         | 139.67 KiB (1%) |        2464 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   3.841 ms (5%) |         | 730.06 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   4.903 ms (5%) |         |   1.79 MiB (1%) |         213 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   4.305 ms (5%) |         |   1.43 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  14.517 ms (5%) |         |   1.03 MiB (1%) |         160 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  25.189 ms (5%) |         |   1.03 MiB (1%) |        1437 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  16.232 ms (5%) |         |   1.23 MiB (1%) |         420 |
| `["parallel_histogram", "seq"]`                     |   6.897 ms (5%) |         | 364.61 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  35.424 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  18.062 ms (5%) |         |   2.66 KiB (1%) |          48 |
| `["splitby", "count", "foldl"]`                     |   4.350 ms (5%) |         |   96 bytes (1%) |           4 |
| `["splitby", "count", "man"]`                       |   1.777 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    | 875.011 μs (5%) |         |   2.88 KiB (1%) |          55 |
| `["sum", "random", "foldl"]`                        |  13.346 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "random", "reduce", "basesize=128"]`       |   7.592 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "random", "reduce", "basesize=256"]`       |   7.107 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "random", "reduce", "basesize=512"]`       |   6.865 ms (5%) |         |  25.30 KiB (1%) |         252 |
| `["sum", "uniform", "foldl"]`                       |  13.766 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   7.572 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   7.419 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   7.125 ms (5%) |         |  25.25 KiB (1%) |         251 |
| `["sum", "valley", "foldl"]`                        |  14.526 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "valley", "reduce", "basesize=128"]`       |   7.933 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   7.601 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   7.592 ms (5%) |         |  25.25 KiB (1%) |         251 |
| `["words", "nthreads=1"]`                           |  27.560 ms (5%) |         |  31.78 MiB (1%) |     1035387 |
| `["words", "nthreads=2"]`                           |  17.090 ms (5%) |         |  32.49 MiB (1%) |     1035467 |
| `["words", "nthreads=4"]`                           |  17.555 ms (5%) |         |  33.13 MiB (1%) |     1035619 |

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
       #1  2294 MHz      54230 s         18 s       2424 s      27544 s          0 s
       #2  2294 MHz      57832 s          7 s       2559 s      23970 s          0 s
       
  Memory: 6.791339874267578 GB (3736.75390625 MB free)
  Uptime: 858.0 sec
  Load Avg:  1.63671875  1.51220703125  0.9658203125
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, broadwell)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 28 Mar 2021 - 1:25
* Package commit: b7b120
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
| `["collect", "assoc", "basesize=1"]`                | 243.213 ms (5%) |         |  32.66 MiB (1%) |      286772 |
| `["collect", "assoc", "basesize=1024"]`             | 195.270 ms (5%) |         |   1.79 MiB (1%) |         570 |
| `["collect", "assoc", "basesize=32"]`               | 196.069 ms (5%) |         |   3.97 MiB (1%) |       13306 |
| `["collect", "seq"]`                                | 385.764 ms (5%) |         | 512.72 KiB (1%) |          15 |
| `["collect", "unordered", "basesize=1"]`            | 487.551 ms (5%) |         |  30.01 MiB (1%) |      360669 |
| `["collect", "unordered", "basesize=1024"]`         | 317.126 ms (5%) |         | 884.55 KiB (1%) |        5045 |
| `["collect", "unordered", "basesize=32"]`           | 232.477 ms (5%) |         |   1.47 MiB (1%) |       12523 |
| `["findfirst", "n=1000", "foldl"]`                  | 624.488 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 508.890 ms (5%) |         | 970.02 KiB (1%) |       16992 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 465.177 ms (5%) |         | 485.00 KiB (1%) |        8497 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 647.790 ms (5%) |         | 343.16 KiB (1%) |        6035 |
| `["findfirst", "n=400", "foldl"]`                   | 464.169 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 256.165 ms (5%) |         |   1.07 MiB (1%) |       19340 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 254.027 ms (5%) |         | 590.70 KiB (1%) |       10414 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 286.870 ms (5%) |         | 377.97 KiB (1%) |        6658 |
| `["findfirst", "n=500", "foldl"]`                   |  79.198 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |  71.492 ms (5%) |         | 378.88 KiB (1%) |        6596 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 127.429 ms (5%) |         | 354.69 KiB (1%) |        6186 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 124.860 ms (5%) |         | 206.70 KiB (1%) |        3621 |
| `["overhead", "default"]`                           |  64.901 μs (5%) |         |  47.36 KiB (1%) |         382 |
| `["overhead", "stoppable=false"]`                   |  65.700 μs (5%) |         |  47.39 KiB (1%) |         382 |
| `["overhead", "stoppable=true"]`                    | 169.809 μs (5%) |         | 139.67 KiB (1%) |        2464 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   3.811 ms (5%) |         | 730.06 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   5.003 ms (5%) |         |   2.06 MiB (1%) |         219 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   4.166 ms (5%) |         |   1.43 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  13.776 ms (5%) |         |   1.22 MiB (1%) |         255 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  18.849 ms (5%) |         |   1.01 MiB (1%) |        1446 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  17.867 ms (5%) |         |   1.24 MiB (1%) |         927 |
| `["parallel_histogram", "seq"]`                     |   6.694 ms (5%) |         | 364.61 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  37.633 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  18.925 ms (5%) |         |   2.66 KiB (1%) |          48 |
| `["splitby", "count", "foldl"]`                     |   4.473 ms (5%) |         |   96 bytes (1%) |           4 |
| `["splitby", "count", "man"]`                       |   1.646 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    | 873.212 μs (5%) |         |   2.88 KiB (1%) |          55 |
| `["sum", "random", "foldl"]`                        |  14.430 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "random", "reduce", "basesize=128"]`       |   7.828 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "random", "reduce", "basesize=256"]`       |   7.379 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "random", "reduce", "basesize=512"]`       |   7.669 ms (5%) |         |  25.30 KiB (1%) |         252 |
| `["sum", "uniform", "foldl"]`                       |  14.943 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   7.624 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   7.476 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   7.253 ms (5%) |         |  25.25 KiB (1%) |         251 |
| `["sum", "valley", "foldl"]`                        |  15.417 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "valley", "reduce", "basesize=128"]`       |   7.425 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   7.860 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   7.699 ms (5%) |         |  25.25 KiB (1%) |         251 |
| `["words", "nthreads=1"]`                           |  27.962 ms (5%) |         |  31.63 MiB (1%) |     1030180 |
| `["words", "nthreads=2"]`                           |  16.518 ms (5%) |         |  31.98 MiB (1%) |     1030222 |
| `["words", "nthreads=4"]`                           |  18.126 ms (5%) |         |  32.70 MiB (1%) |     1030311 |

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
       #1  2294 MHz      81219 s         18 s       3048 s      35180 s          0 s
       #2  2294 MHz      83040 s          7 s       3190 s      33459 s          0 s
       
  Memory: 6.791339874267578 GB (3648.72265625 MB free)
  Uptime: 1212.0 sec
  Load Avg:  1.69873046875  1.568359375  1.15966796875
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
    CPU MHz:                         2294.687
    BogoMIPS:                        4589.37
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

