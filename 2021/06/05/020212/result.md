# Multi-thread benchmark result

* Pull request commit: [`72496c02f3d189f3fcaff620c407bd8e10b85fcd`](https://github.com/JuliaFolds/Transducers.jl/commit/72496c02f3d189f3fcaff620c407bd8e10b85fcd)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/243> (Update */Manifest.toml)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 5 Jun 2021 - 01:56
    - Baseline: 5 Jun 2021 - 02:01
* Package commits:
    - Target: f4d8c5
    - Baseline: 2cfb4c
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
| `["collect", "unordered", "basesize=1024"]`         | 0.81 (5%) :white_check_mark: | 0.85 (1%) :white_check_mark: |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 0.74 (5%) :white_check_mark: | 0.74 (1%) :white_check_mark: |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 0.93 (5%) :white_check_mark: | 0.95 (1%) :white_check_mark: |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 0.88 (5%) :white_check_mark: | 0.91 (1%) :white_check_mark: |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  |                   1.00 (5%)  |                1.02 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |                1.64 (5%) :x: |                1.47 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |                1.37 (5%) :x: |                1.19 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |                1.50 (5%) :x: |                1.28 (1%) :x: |
| `["overhead", "default"]`                           | 0.92 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |                   1.01 (5%)  |                1.15 (1%) :x: |
| `["parallel_histogram", "comm", "basesize=16384"]`  |                1.08 (5%) :x: |                   1.00 (1%)  |
| `["parallel_histogram", "comm", "basesize=4096"]`   |                   0.98 (5%)  |                1.01 (1%) :x: |
| `["parallel_histogram", "comm", "basesize=8192"]`   | 0.88 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["splitby", "count", "man"]`                       | 0.86 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["splitby", "count", "reduce"]`                    |                   0.98 (5%)  |                1.01 (1%) :x: |
| `["words", "nthreads=1"]`                           |                   1.01 (5%)  | 0.99 (1%) :white_check_mark: |
| `["words", "nthreads=2"]`                           |                   1.02 (5%)  | 0.99 (1%) :white_check_mark: |
| `["words", "nthreads=4"]`                           |                   1.01 (5%)  | 0.98 (1%) :white_check_mark: |

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
  uname: Linux 5.4.0-1047-azure #49-Ubuntu SMP Thu Apr 22 14:30:37 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2593 MHz      49513 s         16 s       2243 s      25557 s          0 s
       #2  2593 MHz      56469 s          8 s       2347 s      19022 s          0 s
       
  Memory: 6.791339874267578 GB (3732.0703125 MB free)
  Uptime: 790.0 sec
  Load Avg:  1.73974609375  1.525390625  0.921875
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
  uname: Linux 5.4.0-1047-azure #49-Ubuntu SMP Thu Apr 22 14:30:37 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2593 MHz      72023 s         16 s       2940 s      35122 s          0 s
       #2  2593 MHz      83158 s          8 s       2986 s      24353 s          0 s
       
  Memory: 6.791339874267578 GB (3751.609375 MB free)
  Uptime: 1118.0 sec
  Load Avg:  1.787109375  1.6064453125  1.13037109375
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, skylake-avx512)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 5 Jun 2021 - 1:56
* Package commit: f4d8c5
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
| `["collect", "assoc", "basesize=1"]`                | 238.332 ms (5%) |         |  32.66 MiB (1%) |      286745 |
| `["collect", "assoc", "basesize=1024"]`             | 198.176 ms (5%) |         |   1.79 MiB (1%) |         569 |
| `["collect", "assoc", "basesize=32"]`               | 200.100 ms (5%) |         |   3.97 MiB (1%) |       13306 |
| `["collect", "seq"]`                                | 395.044 ms (5%) |         | 512.72 KiB (1%) |          15 |
| `["collect", "unordered", "basesize=1"]`            | 417.777 ms (5%) |         |  30.01 MiB (1%) |      360559 |
| `["collect", "unordered", "basesize=1024"]`         | 218.135 ms (5%) |         | 775.39 KiB (1%) |        1534 |
| `["collect", "unordered", "basesize=32"]`           | 222.407 ms (5%) |         |   1.48 MiB (1%) |       12683 |
| `["findfirst", "n=1000", "foldl"]`                  | 624.492 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 338.712 ms (5%) |         | 668.58 KiB (1%) |       11728 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 417.543 ms (5%) |         | 466.45 KiB (1%) |        8173 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 537.774 ms (5%) |         | 319.72 KiB (1%) |        5606 |
| `["findfirst", "n=400", "foldl"]`                   | 468.687 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 247.067 ms (5%) |         |   1.11 MiB (1%) |       19932 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 254.214 ms (5%) |         | 597.67 KiB (1%) |       10537 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 269.568 ms (5%) |         | 366.38 KiB (1%) |        6457 |
| `["findfirst", "n=500", "foldl"]`                   |  81.257 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 147.781 ms (5%) |         | 669.19 KiB (1%) |       11673 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 155.168 ms (5%) |         | 412.16 KiB (1%) |        7172 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 200.246 ms (5%) |         | 273.38 KiB (1%) |        4781 |
| `["overhead", "default"]`                           |  56.401 μs (5%) |         |  47.36 KiB (1%) |         382 |
| `["overhead", "stoppable=false"]`                   |  59.201 μs (5%) |         |  47.39 KiB (1%) |         382 |
| `["overhead", "stoppable=true"]`                    | 156.603 μs (5%) |         | 139.67 KiB (1%) |        2464 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   4.005 ms (5%) |         | 730.06 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   4.674 ms (5%) |         |   2.06 MiB (1%) |         219 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   4.317 ms (5%) |         |   1.43 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  13.946 ms (5%) |         |   1.23 MiB (1%) |         567 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  22.106 ms (5%) |         |   1.07 MiB (1%) |        3208 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  17.619 ms (5%) |         |   1.26 MiB (1%) |        1577 |
| `["parallel_histogram", "seq"]`                     |   7.291 ms (5%) |         | 364.61 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  33.719 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  16.876 ms (5%) |         |   2.66 KiB (1%) |          48 |
| `["splitby", "count", "foldl"]`                     |   4.703 ms (5%) |         |   96 bytes (1%) |           4 |
| `["splitby", "count", "man"]`                       |   1.661 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    |   1.176 ms (5%) |         |   2.88 KiB (1%) |          55 |
| `["sum", "random", "foldl"]`                        |  15.916 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "random", "reduce", "basesize=128"]`       |   8.133 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "random", "reduce", "basesize=256"]`       |   8.031 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "random", "reduce", "basesize=512"]`       |   7.986 ms (5%) |         |  25.30 KiB (1%) |         252 |
| `["sum", "uniform", "foldl"]`                       |  15.401 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   7.897 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   7.802 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   7.746 ms (5%) |         |  25.25 KiB (1%) |         251 |
| `["sum", "valley", "foldl"]`                        |  16.087 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "valley", "reduce", "basesize=128"]`       |   8.192 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   8.105 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   8.051 ms (5%) |         |  25.25 KiB (1%) |         251 |
| `["words", "nthreads=1"]`                           |  22.030 ms (5%) |         |  31.60 MiB (1%) |     1029840 |
| `["words", "nthreads=2"]`                           |  13.987 ms (5%) |         |  31.95 MiB (1%) |     1029878 |
| `["words", "nthreads=4"]`                           |  14.411 ms (5%) |         |  32.67 MiB (1%) |     1029967 |

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
  uname: Linux 5.4.0-1047-azure #49-Ubuntu SMP Thu Apr 22 14:30:37 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2593 MHz      49513 s         16 s       2243 s      25557 s          0 s
       #2  2593 MHz      56469 s          8 s       2347 s      19022 s          0 s
       
  Memory: 6.791339874267578 GB (3732.0703125 MB free)
  Uptime: 790.0 sec
  Load Avg:  1.73974609375  1.525390625  0.921875
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, skylake-avx512)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 5 Jun 2021 - 2:1
* Package commit: 2cfb4c
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
| `["collect", "assoc", "basesize=1"]`                | 238.842 ms (5%) |         |  32.66 MiB (1%) |      286740 |
| `["collect", "assoc", "basesize=1024"]`             | 198.518 ms (5%) |         |   1.79 MiB (1%) |         570 |
| `["collect", "assoc", "basesize=32"]`               | 199.848 ms (5%) |         |   3.97 MiB (1%) |       13306 |
| `["collect", "seq"]`                                | 395.166 ms (5%) |         | 512.72 KiB (1%) |          15 |
| `["collect", "unordered", "basesize=1"]`            | 410.110 ms (5%) |         |  30.01 MiB (1%) |      360562 |
| `["collect", "unordered", "basesize=1024"]`         | 268.069 ms (5%) |         | 907.17 KiB (1%) |        5769 |
| `["collect", "unordered", "basesize=32"]`           | 222.486 ms (5%) |         |   1.47 MiB (1%) |       12601 |
| `["findfirst", "n=1000", "foldl"]`                  | 625.964 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 458.936 ms (5%) |         | 898.30 KiB (1%) |       15744 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 451.117 ms (5%) |         | 492.00 KiB (1%) |        8619 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 613.206 ms (5%) |         | 352.30 KiB (1%) |        6188 |
| `["findfirst", "n=400", "foldl"]`                   | 469.634 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 247.716 ms (5%) |         |   1.09 MiB (1%) |       19556 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 259.840 ms (5%) |         | 600.09 KiB (1%) |       10583 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 270.460 ms (5%) |         | 366.38 KiB (1%) |        6457 |
| `["findfirst", "n=500", "foldl"]`                   |  81.449 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |  89.887 ms (5%) |         | 455.50 KiB (1%) |        7938 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 113.061 ms (5%) |         | 347.22 KiB (1%) |        6035 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 133.345 ms (5%) |         | 213.17 KiB (1%) |        3711 |
| `["overhead", "default"]`                           |  61.401 μs (5%) |         |  47.36 KiB (1%) |         382 |
| `["overhead", "stoppable=false"]`                   |  60.401 μs (5%) |         |  47.39 KiB (1%) |         382 |
| `["overhead", "stoppable=true"]`                    | 152.302 μs (5%) |         | 139.67 KiB (1%) |        2464 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   4.008 ms (5%) |         | 730.06 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   4.623 ms (5%) |         |   1.79 MiB (1%) |         213 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   4.323 ms (5%) |         |   1.43 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  12.967 ms (5%) |         |   1.23 MiB (1%) |         400 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  22.501 ms (5%) |         |   1.05 MiB (1%) |        2568 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  19.924 ms (5%) |         |   1.26 MiB (1%) |        1437 |
| `["parallel_histogram", "seq"]`                     |   7.283 ms (5%) |         | 364.61 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  33.723 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  16.868 ms (5%) |         |   2.66 KiB (1%) |          48 |
| `["splitby", "count", "foldl"]`                     |   4.728 ms (5%) |         |   96 bytes (1%) |           4 |
| `["splitby", "count", "man"]`                       |   1.937 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    |   1.202 ms (5%) |         |   2.84 KiB (1%) |          54 |
| `["sum", "random", "foldl"]`                        |  16.051 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "random", "reduce", "basesize=128"]`       |   8.229 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "random", "reduce", "basesize=256"]`       |   8.119 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "random", "reduce", "basesize=512"]`       |   8.080 ms (5%) |         |  25.30 KiB (1%) |         252 |
| `["sum", "uniform", "foldl"]`                       |  15.384 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   7.871 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   7.792 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   7.746 ms (5%) |         |  25.25 KiB (1%) |         251 |
| `["sum", "valley", "foldl"]`                        |  16.068 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "valley", "reduce", "basesize=128"]`       |   8.211 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   8.132 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   8.093 ms (5%) |         |  25.25 KiB (1%) |         251 |
| `["words", "nthreads=1"]`                           |  21.827 ms (5%) |         |  31.96 MiB (1%) |     1041486 |
| `["words", "nthreads=2"]`                           |  13.746 ms (5%) |         |  32.31 MiB (1%) |     1041522 |
| `["words", "nthreads=4"]`                           |  14.209 ms (5%) |         |  33.21 MiB (1%) |     1041672 |

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
  uname: Linux 5.4.0-1047-azure #49-Ubuntu SMP Thu Apr 22 14:30:37 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2593 MHz      72023 s         16 s       2940 s      35122 s          0 s
       #2  2593 MHz      83158 s          8 s       2986 s      24353 s          0 s
       
  Memory: 6.791339874267578 GB (3751.609375 MB free)
  Uptime: 1118.0 sec
  Load Avg:  1.787109375  1.6064453125  1.13037109375
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
    Model name:                      Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz
    Stepping:                        7
    CPU MHz:                         2593.905
    BogoMIPS:                        5187.81
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
| Brand              | Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz          |
| Vendor             | :Intel                                                  |
| Architecture       | :Skylake                                                |
| Model              | Family: 0x06, Model: 0x55, Stepping: 0x07, Type: 0x00   |
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

