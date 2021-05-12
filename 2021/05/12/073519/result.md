# Multi-thread benchmark result

* Pull request commit: [`d1e38cfe4b90b24b9d0612c05ed838b50151cede`](https://github.com/JuliaFolds/Transducers.jl/commit/d1e38cfe4b90b24b9d0612c05ed838b50151cede)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/485> (Update Maybe and ConstructionBase for CI)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 12 May 2021 - 07:29
    - Baseline: 12 May 2021 - 07:34
* Package commits:
    - Target: 858dea
    - Baseline: 31d6da
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
| `["collect", "seq"]`                                | 0.94 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["collect", "unordered", "basesize=1"]`            |                1.06 (5%) :x: |                   1.00 (1%)  |
| `["collect", "unordered", "basesize=1024"]`         | 0.66 (5%) :white_check_mark: | 0.81 (1%) :white_check_mark: |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 0.57 (5%) :white_check_mark: | 0.62 (1%) :white_check_mark: |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 0.93 (5%) :white_check_mark: | 0.95 (1%) :white_check_mark: |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` |                1.17 (5%) :x: |                1.13 (1%) :x: |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  |                   1.01 (5%)  | 0.99 (1%) :white_check_mark: |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  |                   1.05 (5%)  | 0.99 (1%) :white_check_mark: |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  |                   1.00 (5%)  | 0.97 (1%) :white_check_mark: |
| `["findfirst", "n=500", "foldl"]`                   | 0.95 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |                1.50 (5%) :x: |                1.64 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |                   1.02 (5%)  |                1.20 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 0.67 (5%) :white_check_mark: | 0.75 (1%) :white_check_mark: |
| `["parallel_histogram", "comm", "basesize=8192"]`   |                   0.99 (5%)  |                1.02 (1%) :x: |
| `["splitby", "count", "foldl"]`                     | 0.93 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["splitby", "count", "man"]`                       |                1.10 (5%) :x: |                   1.00 (1%)  |
| `["splitby", "count", "reduce"]`                    | 0.92 (5%) :white_check_mark: | 0.97 (1%) :white_check_mark: |
| `["sum", "random", "reduce", "basesize=512"]`       | 0.95 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["words", "nthreads=1"]`                           | 0.94 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["words", "nthreads=2"]`                           |                1.11 (5%) :x: |                   1.00 (1%)  |
| `["words", "nthreads=4"]`                           |                1.15 (5%) :x: |                   1.00 (1%)  |

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
  uname: Linux 5.4.0-1046-azure #48-Ubuntu SMP Tue Apr 13 07:18:42 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz: 
              speed         user         nice          sys         idle          irq
       #1  2294 MHz      53717 s          5 s       2496 s      21666 s          0 s
       #2  2294 MHz      56844 s         21 s       2681 s      18706 s          0 s
       
  Memory: 6.791343688964844 GB (3634.265625 MB free)
  Uptime: 789.0 sec
  Load Avg:  1.7626953125  1.54150390625  0.9375
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
  uname: Linux 5.4.0-1046-azure #48-Ubuntu SMP Tue Apr 13 07:18:42 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz: 
              speed         user         nice          sys         idle          irq
       #1  2294 MHz      79115 s          5 s       3042 s      27238 s          0 s
       #2  2294 MHz      79690 s         21 s       3212 s      26791 s          0 s
       
  Memory: 6.791343688964844 GB (3630.1484375 MB free)
  Uptime: 1105.0 sec
  Load Avg:  1.6494140625  1.60546875  1.1416015625
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, broadwell)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 12 May 2021 - 7:29
* Package commit: 858dea
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
| `["collect", "assoc", "basesize=1"]`                | 225.727 ms (5%) |         |  32.66 MiB (1%) |      286771 |
| `["collect", "assoc", "basesize=1024"]`             | 176.218 ms (5%) |         |   1.79 MiB (1%) |         570 |
| `["collect", "assoc", "basesize=32"]`               | 177.981 ms (5%) |         |   3.97 MiB (1%) |       13305 |
| `["collect", "seq"]`                                | 339.448 ms (5%) |         | 512.72 KiB (1%) |          15 |
| `["collect", "unordered", "basesize=1"]`            | 424.000 ms (5%) |         |  30.01 MiB (1%) |      360598 |
| `["collect", "unordered", "basesize=1024"]`         | 201.381 ms (5%) |         | 785.80 KiB (1%) |        1885 |
| `["collect", "unordered", "basesize=32"]`           | 209.547 ms (5%) |         |   1.47 MiB (1%) |       12608 |
| `["findfirst", "n=1000", "foldl"]`                  | 575.175 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 372.707 ms (5%) |         | 781.83 KiB (1%) |       13686 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 402.427 ms (5%) |         | 461.77 KiB (1%) |        8089 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 615.852 ms (5%) |         | 361.52 KiB (1%) |        6353 |
| `["findfirst", "n=400", "foldl"]`                   | 436.008 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 241.144 ms (5%) |         |   1.06 MiB (1%) |       19148 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 246.078 ms (5%) |         | 602.53 KiB (1%) |       10630 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 268.544 ms (5%) |         | 357.33 KiB (1%) |        6299 |
| `["findfirst", "n=500", "foldl"]`                   |  70.982 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 233.477 ms (5%) |         |   1.03 MiB (1%) |       18410 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 109.005 ms (5%) |         | 349.89 KiB (1%) |        6094 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 107.315 ms (5%) |         | 172.11 KiB (1%) |        3014 |
| `["overhead", "default"]`                           |  58.800 μs (5%) |         |  47.36 KiB (1%) |         382 |
| `["overhead", "stoppable=false"]`                   |  57.399 μs (5%) |         |  47.39 KiB (1%) |         382 |
| `["overhead", "stoppable=true"]`                    | 157.101 μs (5%) |         | 139.67 KiB (1%) |        2464 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   3.382 ms (5%) |         | 730.06 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   4.190 ms (5%) |         |   1.79 MiB (1%) |         213 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   3.692 ms (5%) |         |   1.43 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  13.444 ms (5%) |         |   1.04 MiB (1%) |         289 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  22.358 ms (5%) |         |   1.04 MiB (1%) |        1799 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  18.392 ms (5%) |         |   1.26 MiB (1%) |        1361 |
| `["parallel_histogram", "seq"]`                     |   6.018 ms (5%) |         | 364.61 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  35.375 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  17.813 ms (5%) |         |   2.66 KiB (1%) |          48 |
| `["splitby", "count", "foldl"]`                     |   3.620 ms (5%) |         |   96 bytes (1%) |           4 |
| `["splitby", "count", "man"]`                       |   1.522 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    | 764.605 μs (5%) |         |   2.78 KiB (1%) |          52 |
| `["sum", "random", "foldl"]`                        |  13.541 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "random", "reduce", "basesize=128"]`       |   6.830 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "random", "reduce", "basesize=256"]`       |   6.769 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "random", "reduce", "basesize=512"]`       |   6.653 ms (5%) |         |  25.30 KiB (1%) |         252 |
| `["sum", "uniform", "foldl"]`                       |  12.630 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   6.595 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   6.478 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   6.432 ms (5%) |         |  25.25 KiB (1%) |         251 |
| `["sum", "valley", "foldl"]`                        |  13.687 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "valley", "reduce", "basesize=128"]`       |   6.699 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   6.771 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   6.831 ms (5%) |         |  25.25 KiB (1%) |         251 |
| `["words", "nthreads=1"]`                           |  23.437 ms (5%) |         |  31.25 MiB (1%) |     1018151 |
| `["words", "nthreads=2"]`                           |  17.210 ms (5%) |         |  31.97 MiB (1%) |     1018243 |
| `["words", "nthreads=4"]`                           |  17.843 ms (5%) |         |  32.60 MiB (1%) |     1018395 |

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
  uname: Linux 5.4.0-1046-azure #48-Ubuntu SMP Tue Apr 13 07:18:42 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz: 
              speed         user         nice          sys         idle          irq
       #1  2294 MHz      53717 s          5 s       2496 s      21666 s          0 s
       #2  2294 MHz      56844 s         21 s       2681 s      18706 s          0 s
       
  Memory: 6.791343688964844 GB (3634.265625 MB free)
  Uptime: 789.0 sec
  Load Avg:  1.7626953125  1.54150390625  0.9375
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, broadwell)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 12 May 2021 - 7:34
* Package commit: 31d6da
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
| `["collect", "assoc", "basesize=1"]`                | 229.191 ms (5%) |         |  32.66 MiB (1%) |      286760 |
| `["collect", "assoc", "basesize=1024"]`             | 175.718 ms (5%) |         |   1.79 MiB (1%) |         569 |
| `["collect", "assoc", "basesize=32"]`               | 176.934 ms (5%) |         |   3.97 MiB (1%) |       13306 |
| `["collect", "seq"]`                                | 359.974 ms (5%) |         | 512.72 KiB (1%) |          15 |
| `["collect", "unordered", "basesize=1"]`            | 399.415 ms (5%) |         |  30.01 MiB (1%) |      360592 |
| `["collect", "unordered", "basesize=1024"]`         | 304.399 ms (5%) |         | 975.17 KiB (1%) |        7945 |
| `["collect", "unordered", "basesize=32"]`           | 210.912 ms (5%) |         |   1.48 MiB (1%) |       12670 |
| `["findfirst", "n=1000", "foldl"]`                  | 570.839 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 652.092 ms (5%) |         |   1.24 MiB (1%) |       22262 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 434.400 ms (5%) |         | 484.88 KiB (1%) |        8487 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 528.595 ms (5%) |         | 319.81 KiB (1%) |        5614 |
| `["findfirst", "n=400", "foldl"]`                   | 430.122 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 238.720 ms (5%) |         |   1.07 MiB (1%) |       19337 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 234.400 ms (5%) |         | 609.25 KiB (1%) |       10739 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 269.716 ms (5%) |         | 369.02 KiB (1%) |        6507 |
| `["findfirst", "n=500", "foldl"]`                   |  74.860 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 155.474 ms (5%) |         | 644.33 KiB (1%) |       11258 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 106.550 ms (5%) |         | 292.28 KiB (1%) |        5098 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 159.206 ms (5%) |         | 229.58 KiB (1%) |        4011 |
| `["overhead", "default"]`                           |  60.000 μs (5%) |         |  47.36 KiB (1%) |         382 |
| `["overhead", "stoppable=false"]`                   |  56.701 μs (5%) |         |  47.36 KiB (1%) |         381 |
| `["overhead", "stoppable=true"]`                    | 149.901 μs (5%) |         | 139.67 KiB (1%) |        2464 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   3.367 ms (5%) |         | 730.06 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   4.188 ms (5%) |         |   1.79 MiB (1%) |         213 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   3.731 ms (5%) |         |   1.43 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  13.958 ms (5%) |         |   1.03 MiB (1%) |         160 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  23.339 ms (5%) |         |   1.03 MiB (1%) |        1841 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  18.600 ms (5%) |         |   1.24 MiB (1%) |         673 |
| `["parallel_histogram", "seq"]`                     |   5.836 ms (5%) |         | 364.61 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  35.021 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  17.368 ms (5%) |         |   2.66 KiB (1%) |          48 |
| `["splitby", "count", "foldl"]`                     |   3.881 ms (5%) |         |   96 bytes (1%) |           4 |
| `["splitby", "count", "man"]`                       |   1.381 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    | 834.405 μs (5%) |         |   2.88 KiB (1%) |          55 |
| `["sum", "random", "foldl"]`                        |  13.340 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "random", "reduce", "basesize=128"]`       |   6.834 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "random", "reduce", "basesize=256"]`       |   6.916 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "random", "reduce", "basesize=512"]`       |   7.007 ms (5%) |         |  25.30 KiB (1%) |         252 |
| `["sum", "uniform", "foldl"]`                       |  12.884 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   6.433 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   6.700 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   6.399 ms (5%) |         |  25.25 KiB (1%) |         251 |
| `["sum", "valley", "foldl"]`                        |  13.153 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "valley", "reduce", "basesize=128"]`       |   6.733 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   6.707 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   6.807 ms (5%) |         |  25.25 KiB (1%) |         251 |
| `["words", "nthreads=1"]`                           |  24.899 ms (5%) |         |  31.40 MiB (1%) |     1023139 |
| `["words", "nthreads=2"]`                           |  15.458 ms (5%) |         |  32.12 MiB (1%) |     1023235 |
| `["words", "nthreads=4"]`                           |  15.471 ms (5%) |         |  32.57 MiB (1%) |     1023310 |

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
  uname: Linux 5.4.0-1046-azure #48-Ubuntu SMP Tue Apr 13 07:18:42 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz: 
              speed         user         nice          sys         idle          irq
       #1  2294 MHz      79115 s          5 s       3042 s      27238 s          0 s
       #2  2294 MHz      79690 s         21 s       3212 s      26791 s          0 s
       
  Memory: 6.791343688964844 GB (3630.1484375 MB free)
  Uptime: 1105.0 sec
  Load Avg:  1.6494140625  1.60546875  1.1416015625
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
    CPU MHz:                         2294.681
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

