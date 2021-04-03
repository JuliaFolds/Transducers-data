# Multi-thread benchmark result

* Pull request commit: [`a68e7974603fac81c2306dd116969ad44dfcf4ef`](https://github.com/JuliaFolds/Transducers.jl/commit/a68e7974603fac81c2306dd116969ad44dfcf4ef)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/243> (Update */Manifest.toml)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 3 Apr 2021 - 01:18
    - Baseline: 3 Apr 2021 - 01:23
* Package commits:
    - Target: 8e42a3
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
| `["collect", "unordered", "basesize=1"]`            |                1.06 (5%) :x: |                   1.00 (1%)  |
| `["collect", "unordered", "basesize=1024"]`         | 0.88 (5%) :white_check_mark: | 0.87 (1%) :white_check_mark: |
| `["collect", "unordered", "basesize=32"]`           | 0.93 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` |                   1.04 (5%)  |                1.06 (1%) :x: |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` |                   1.01 (5%)  |                1.05 (1%) :x: |
| `["findfirst", "n=400", "foldl"]`                   | 0.92 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 0.86 (5%) :white_check_mark: | 0.94 (1%) :white_check_mark: |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 0.90 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  |                1.05 (5%) :x: |                   1.00 (1%)  |
| `["findfirst", "n=500", "foldl"]`                   | 0.95 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |                1.55 (5%) :x: |                1.49 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 0.81 (5%) :white_check_mark: | 0.95 (1%) :white_check_mark: |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 0.89 (5%) :white_check_mark: | 0.88 (1%) :white_check_mark: |
| `["overhead", "default"]`                           | 0.92 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["overhead", "stoppable=false"]`                   | 0.90 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["parallel_histogram", "comm", "basesize=4096"]`   |                   1.02 (5%)  | 0.98 (1%) :white_check_mark: |
| `["parallel_histogram", "comm", "basesize=8192"]`   |                1.09 (5%) :x: |                1.03 (1%) :x: |
| `["parallel_histogram", "seq"]`                     |                1.11 (5%) :x: |                   1.00 (1%)  |
| `["partition_length_maximum", "rand", "foldl"]`     | 0.87 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["partition_length_maximum", "rand", "reduce"]`    | 0.93 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["splitby", "count", "reduce"]`                    |                   0.99 (5%)  | 0.99 (1%) :white_check_mark: |
| `["sum", "random", "foldl"]`                        | 0.89 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["sum", "random", "reduce", "basesize=128"]`       | 0.91 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["sum", "random", "reduce", "basesize=256"]`       | 0.89 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["sum", "random", "reduce", "basesize=512"]`       | 0.91 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["sum", "uniform", "reduce", "basesize=128"]`      | 0.91 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["sum", "uniform", "reduce", "basesize=256"]`      | 0.88 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["sum", "valley", "reduce", "basesize=128"]`       | 0.89 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["sum", "valley", "reduce", "basesize=256"]`       | 0.92 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["sum", "valley", "reduce", "basesize=512"]`       | 0.84 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["words", "nthreads=1"]`                           |                1.10 (5%) :x: |                   1.00 (1%)  |
| `["words", "nthreads=2"]`                           |                   0.97 (5%)  | 0.99 (1%) :white_check_mark: |

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
  uname: Linux 5.4.0-1043-azure #45-Ubuntu SMP Fri Mar 19 17:33:38 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz      55762 s         16 s       2118 s      19312 s          0 s
       #2  2095 MHz      52327 s          9 s       2258 s      22580 s          0 s
       
  Memory: 6.791343688964844 GB (3776.3359375 MB free)
  Uptime: 778.0 sec
  Load Avg:  1.63525390625  1.52197265625  0.939453125
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, skylake-avx512)
```

### Baseline
```
Julia Version 1.5.4
Commit 69fcb5745b (2021-03-11 19:13 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 20.04.2 LTS
  uname: Linux 5.4.0-1043-azure #45-Ubuntu SMP Fri Mar 19 17:33:38 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz      84186 s         16 s       2794 s      23459 s          0 s
       #2  2095 MHz      73777 s          9 s       2875 s      33733 s          0 s
       
  Memory: 6.791343688964844 GB (3672.8984375 MB free)
  Uptime: 1111.0 sec
  Load Avg:  1.560546875  1.560546875  1.13427734375
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, skylake-avx512)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 3 Apr 2021 - 1:18
* Package commit: 8e42a3
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
| `["collect", "assoc", "basesize=1"]`                | 267.082 ms (5%) |         |  32.66 MiB (1%) |      286736 |
| `["collect", "assoc", "basesize=1024"]`             | 208.900 ms (5%) |         |   1.79 MiB (1%) |         570 |
| `["collect", "assoc", "basesize=32"]`               | 205.016 ms (5%) |         |   3.97 MiB (1%) |       13305 |
| `["collect", "seq"]`                                | 401.672 ms (5%) |         | 512.72 KiB (1%) |          15 |
| `["collect", "unordered", "basesize=1"]`            | 457.625 ms (5%) |         |  30.01 MiB (1%) |      360591 |
| `["collect", "unordered", "basesize=1024"]`         | 232.771 ms (5%) |         | 767.86 KiB (1%) |        1293 |
| `["collect", "unordered", "basesize=32"]`           | 234.015 ms (5%) |         |   1.48 MiB (1%) |       12693 |
| `["findfirst", "n=1000", "foldl"]`                  | 709.362 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 725.884 ms (5%) |         |   1.24 MiB (1%) |       22296 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 505.088 ms (5%) |         | 496.70 KiB (1%) |        8707 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 673.346 ms (5%) |         | 345.09 KiB (1%) |        6051 |
| `["findfirst", "n=400", "foldl"]`                   | 475.060 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 268.446 ms (5%) |         |   1.16 MiB (1%) |       20789 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 266.836 ms (5%) |         | 607.31 KiB (1%) |       10721 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 309.475 ms (5%) |         | 366.38 KiB (1%) |        6457 |
| `["findfirst", "n=500", "foldl"]`                   |  78.978 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 186.696 ms (5%) |         | 719.89 KiB (1%) |       12536 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 139.218 ms (5%) |         | 354.58 KiB (1%) |        6175 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 212.361 ms (5%) |         | 259.56 KiB (1%) |        4538 |
| `["overhead", "default"]`                           |  56.701 μs (5%) |         |  47.33 KiB (1%) |         381 |
| `["overhead", "stoppable=false"]`                   |  53.501 μs (5%) |         |  47.36 KiB (1%) |         381 |
| `["overhead", "stoppable=true"]`                    | 136.001 μs (5%) |         | 139.67 KiB (1%) |        2464 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   3.333 ms (5%) |         | 730.06 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   4.138 ms (5%) |         |   1.79 MiB (1%) |         213 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   3.768 ms (5%) |         |   1.43 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  14.615 ms (5%) |         |   1.23 MiB (1%) |         341 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  25.165 ms (5%) |         |   1.05 MiB (1%) |        2671 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  20.662 ms (5%) |         |   1.28 MiB (1%) |        2092 |
| `["parallel_histogram", "seq"]`                     |   7.090 ms (5%) |         | 364.61 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  32.102 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  16.215 ms (5%) |         |   2.66 KiB (1%) |          48 |
| `["splitby", "count", "foldl"]`                     |   3.917 ms (5%) |         |   96 bytes (1%) |           4 |
| `["splitby", "count", "man"]`                       |   1.412 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    | 978.212 μs (5%) |         |   2.81 KiB (1%) |          54 |
| `["sum", "random", "foldl"]`                        |  15.333 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "random", "reduce", "basesize=128"]`       |   7.369 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "random", "reduce", "basesize=256"]`       |   7.123 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "random", "reduce", "basesize=512"]`       |   7.251 ms (5%) |         |  25.30 KiB (1%) |         252 |
| `["sum", "uniform", "foldl"]`                       |  14.205 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   7.190 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   6.904 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   7.500 ms (5%) |         |  25.25 KiB (1%) |         251 |
| `["sum", "valley", "foldl"]`                        |  14.932 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "valley", "reduce", "basesize=128"]`       |   7.251 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   7.384 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   7.300 ms (5%) |         |  25.25 KiB (1%) |         251 |
| `["words", "nthreads=1"]`                           |  23.183 ms (5%) |         |  31.65 MiB (1%) |     1031852 |
| `["words", "nthreads=2"]`                           |  13.035 ms (5%) |         |  32.01 MiB (1%) |     1031888 |
| `["words", "nthreads=4"]`                           |  13.850 ms (5%) |         |  32.91 MiB (1%) |     1032055 |

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
  uname: Linux 5.4.0-1043-azure #45-Ubuntu SMP Fri Mar 19 17:33:38 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz      55762 s         16 s       2118 s      19312 s          0 s
       #2  2095 MHz      52327 s          9 s       2258 s      22580 s          0 s
       
  Memory: 6.791343688964844 GB (3776.3359375 MB free)
  Uptime: 778.0 sec
  Load Avg:  1.63525390625  1.52197265625  0.939453125
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, skylake-avx512)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 3 Apr 2021 - 1:23
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

| ID                                                  | time            | GC time  | memory          | allocations |
|-----------------------------------------------------|----------------:|---------:|----------------:|------------:|
| `["collect", "assoc", "basesize=1"]`                | 259.838 ms (5%) |          |  32.66 MiB (1%) |      286742 |
| `["collect", "assoc", "basesize=1024"]`             | 200.431 ms (5%) |          |   1.79 MiB (1%) |         570 |
| `["collect", "assoc", "basesize=32"]`               | 203.279 ms (5%) |          |   3.97 MiB (1%) |       13306 |
| `["collect", "seq"]`                                | 392.455 ms (5%) |          | 512.72 KiB (1%) |          15 |
| `["collect", "unordered", "basesize=1"]`            | 432.123 ms (5%) |          |  30.01 MiB (1%) |      360577 |
| `["collect", "unordered", "basesize=1024"]`         | 266.017 ms (5%) |          | 886.27 KiB (1%) |        5100 |
| `["collect", "unordered", "basesize=32"]`           | 250.598 ms (5%) |          |   1.48 MiB (1%) |       12660 |
| `["findfirst", "n=1000", "foldl"]`                  | 716.056 ms (5%) |          |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 759.240 ms (5%) |          |   1.24 MiB (1%) |       22297 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 487.056 ms (5%) |          | 466.42 KiB (1%) |        8171 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 665.741 ms (5%) |          | 329.00 KiB (1%) |        5774 |
| `["findfirst", "n=400", "foldl"]`                   | 518.460 ms (5%) |          |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 311.751 ms (5%) |          |   1.23 MiB (1%) |       22060 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 296.703 ms (5%) |          | 604.72 KiB (1%) |       10664 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 294.067 ms (5%) |          | 366.34 KiB (1%) |        6456 |
| `["findfirst", "n=500", "foldl"]`                   |  83.285 ms (5%) |          |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 120.324 ms (5%) |          | 481.58 KiB (1%) |        8407 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 172.650 ms (5%) |          | 373.23 KiB (1%) |        6506 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 239.510 ms (5%) |          | 295.97 KiB (1%) |        5163 |
| `["overhead", "default"]`                           |  61.300 μs (5%) |          |  47.33 KiB (1%) |         381 |
| `["overhead", "stoppable=false"]`                   |  59.701 μs (5%) |          |  47.36 KiB (1%) |         381 |
| `["overhead", "stoppable=true"]`                    | 131.800 μs (5%) |          | 139.64 KiB (1%) |        2463 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   3.348 ms (5%) |          | 730.06 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   4.132 ms (5%) |          |   1.79 MiB (1%) |         213 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   3.954 ms (5%) |          |   1.43 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  14.969 ms (5%) |          |   1.23 MiB (1%) |         520 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  24.566 ms (5%) |          |   1.07 MiB (1%) |        2798 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  18.891 ms (5%) | 2.126 ms |   1.24 MiB (1%) |         770 |
| `["parallel_histogram", "seq"]`                     |   6.379 ms (5%) |          | 364.61 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  36.888 ms (5%) |          |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  17.383 ms (5%) |          |   2.66 KiB (1%) |          48 |
| `["splitby", "count", "foldl"]`                     |   3.913 ms (5%) |          |   96 bytes (1%) |           4 |
| `["splitby", "count", "man"]`                       |   1.405 ms (5%) |          |                 |             |
| `["splitby", "count", "reduce"]`                    | 989.312 μs (5%) |          |   2.84 KiB (1%) |          54 |
| `["sum", "random", "foldl"]`                        |  17.235 ms (5%) |          |   32 bytes (1%) |           2 |
| `["sum", "random", "reduce", "basesize=128"]`       |   8.096 ms (5%) |          | 103.23 KiB (1%) |        1018 |
| `["sum", "random", "reduce", "basesize=256"]`       |   8.024 ms (5%) |          |  51.23 KiB (1%) |         506 |
| `["sum", "random", "reduce", "basesize=512"]`       |   7.953 ms (5%) |          |  25.30 KiB (1%) |         252 |
| `["sum", "uniform", "foldl"]`                       |  14.816 ms (5%) |          |   32 bytes (1%) |           2 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   7.907 ms (5%) |          | 103.23 KiB (1%) |        1018 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   7.806 ms (5%) |          |  51.23 KiB (1%) |         506 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   7.775 ms (5%) |          |  25.25 KiB (1%) |         251 |
| `["sum", "valley", "foldl"]`                        |  15.062 ms (5%) |          |   32 bytes (1%) |           2 |
| `["sum", "valley", "reduce", "basesize=128"]`       |   8.131 ms (5%) |          | 103.23 KiB (1%) |        1018 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   7.992 ms (5%) |          |  51.23 KiB (1%) |         506 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   8.693 ms (5%) |          |  25.25 KiB (1%) |         251 |
| `["words", "nthreads=1"]`                           |  20.984 ms (5%) |          |  31.74 MiB (1%) |     1034087 |
| `["words", "nthreads=2"]`                           |  13.455 ms (5%) |          |  32.45 MiB (1%) |     1034188 |
| `["words", "nthreads=4"]`                           |  13.492 ms (5%) |          |  33.08 MiB (1%) |     1034318 |

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
  uname: Linux 5.4.0-1043-azure #45-Ubuntu SMP Fri Mar 19 17:33:38 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz      84186 s         16 s       2794 s      23459 s          0 s
       #2  2095 MHz      73777 s          9 s       2875 s      33733 s          0 s
       
  Memory: 6.791343688964844 GB (3672.8984375 MB free)
  Uptime: 1111.0 sec
  Load Avg:  1.560546875  1.560546875  1.13427734375
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, skylake-avx512)
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
    Model:                           85
    Model name:                      Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz
    Stepping:                        4
    CPU MHz:                         2095.074
    BogoMIPS:                        4190.14
    Hypervisor vendor:               Microsoft
    Virtualization type:             full
    L1d cache:                       64 KiB
    L1i cache:                       64 KiB
    L2 cache:                        2 MiB
    L3 cache:                        35.8 MiB
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
    Flags:                           fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush mmx fxsr sse sse2 ss ht syscall nx pdpe1gb rdtscp lm constant_tsc rep_good nopl xtopology cpuid pni pclmulqdq ssse3 fma cx16 pcid sse4_1 sse4_2 movbe popcnt aes xsave avx f16c rdrand hypervisor lahf_lm abm 3dnowprefetch invpcid_single pti fsgsbase bmi1 hle avx2 smep bmi2 erms invpcid rtm mpx avx512f avx512dq rdseed adx smap clflushopt avx512cd avx512bw avx512vl xsaveopt xsavec xsaves md_clear
    

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

