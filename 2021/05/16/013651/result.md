# Multi-thread benchmark result

* Pull request commit: [`f960d2921cfade9270cc8f03628edfe4536b5f95`](https://github.com/JuliaFolds/Transducers.jl/commit/f960d2921cfade9270cc8f03628edfe4536b5f95)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/243> (Update */Manifest.toml)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 16 May 2021 - 01:30
    - Baseline: 16 May 2021 - 01:36
* Package commits:
    - Target: 4bfd02
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
| `["collect", "assoc", "basesize=1"]`                |                1.15 (5%) :x: |                   1.00 (1%)  |
| `["collect", "assoc", "basesize=1024"]`             |                1.08 (5%) :x: |                   1.00 (1%)  |
| `["collect", "assoc", "basesize=32"]`               |                1.16 (5%) :x: |                   1.00 (1%)  |
| `["collect", "seq"]`                                | 0.94 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["collect", "unordered", "basesize=1024"]`         |                   0.96 (5%)  | 0.93 (1%) :white_check_mark: |
| `["findfirst", "n=1000", "foldl"]`                  | 0.94 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 0.84 (5%) :white_check_mark: | 0.86 (1%) :white_check_mark: |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` |                1.06 (5%) :x: |                1.02 (1%) :x: |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 0.89 (5%) :white_check_mark: |                   1.01 (1%)  |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 0.90 (5%) :white_check_mark: |                1.03 (1%) :x: |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  |                   1.04 (5%)  |                1.03 (1%) :x: |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  |                   0.96 (5%)  | 0.99 (1%) :white_check_mark: |
| `["findfirst", "n=500", "foldl"]`                   | 0.95 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |                2.05 (5%) :x: |                1.46 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |                   1.02 (5%)  | 0.83 (1%) :white_check_mark: |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |                1.16 (5%) :x: |                1.14 (1%) :x: |
| `["overhead", "stoppable=false"]`                   |                1.08 (5%) :x: |                   1.00 (1%)  |
| `["overhead", "stoppable=true"]`                    |                1.05 (5%) :x: |                   1.00 (1%)  |
| `["parallel_histogram", "comm", "basesize=16384"]`  | 0.85 (5%) :white_check_mark: |                1.02 (1%) :x: |
| `["parallel_histogram", "comm", "basesize=4096"]`   |                1.17 (5%) :x: |                1.02 (1%) :x: |
| `["partition_length_maximum", "rand", "reduce"]`    | 0.94 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["splitby", "count", "man"]`                       |                1.12 (5%) :x: |                   1.00 (1%)  |
| `["splitby", "count", "reduce"]`                    |                   1.01 (5%)  | 0.99 (1%) :white_check_mark: |
| `["sum", "uniform", "reduce", "basesize=256"]`      | 0.95 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["sum", "valley", "reduce", "basesize=128"]`       | 0.95 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["sum", "valley", "reduce", "basesize=512"]`       | 0.94 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["words", "nthreads=2"]`                           | 0.91 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["words", "nthreads=4"]`                           |                1.07 (5%) :x: | 0.99 (1%) :white_check_mark: |

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
  CPU: Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz: 
              speed         user         nice          sys         idle          irq
       #1  2294 MHz      52780 s         17 s       2252 s      21838 s          0 s
       #2  2294 MHz      57237 s          3 s       2728 s      16999 s          0 s
       
  Memory: 6.791339874267578 GB (3726.28125 MB free)
  Uptime: 776.0 sec
  Load Avg:  1.5966796875  1.51513671875  0.9638671875
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
  uname: Linux 5.4.0-1047-azure #49-Ubuntu SMP Thu Apr 22 14:30:37 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz: 
              speed         user         nice          sys         idle          irq
       #1  2294 MHz      75669 s         17 s       2927 s      32585 s          0 s
       #2  2294 MHz      85206 s          3 s       3361 s      22610 s          0 s
       
  Memory: 6.791339874267578 GB (3692.6796875 MB free)
  Uptime: 1120.0 sec
  Load Avg:  1.5927734375  1.53662109375  1.14111328125
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, broadwell)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 16 May 2021 - 1:30
* Package commit: 4bfd02
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
| `["collect", "assoc", "basesize=1"]`                | 234.186 ms (5%) |         |  32.66 MiB (1%) |      286768 |
| `["collect", "assoc", "basesize=1024"]`             | 170.910 ms (5%) |         |   1.79 MiB (1%) |         570 |
| `["collect", "assoc", "basesize=32"]`               | 181.035 ms (5%) |         |   3.97 MiB (1%) |       13306 |
| `["collect", "seq"]`                                | 328.118 ms (5%) |         | 512.72 KiB (1%) |          15 |
| `["collect", "unordered", "basesize=1"]`            | 423.024 ms (5%) |         |  30.01 MiB (1%) |      360642 |
| `["collect", "unordered", "basesize=1024"]`         | 262.463 ms (5%) |         | 824.89 KiB (1%) |        3136 |
| `["collect", "unordered", "basesize=32"]`           | 210.686 ms (5%) |         |   1.47 MiB (1%) |       12554 |
| `["findfirst", "n=1000", "foldl"]`                  | 506.770 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 347.186 ms (5%) |         | 744.73 KiB (1%) |       13039 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 452.370 ms (5%) |         | 485.03 KiB (1%) |        8498 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 449.490 ms (5%) |         | 324.25 KiB (1%) |        5685 |
| `["findfirst", "n=400", "foldl"]`                   | 380.402 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 220.062 ms (5%) |         |   1.10 MiB (1%) |       19807 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 217.618 ms (5%) |         | 597.72 KiB (1%) |       10539 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 219.605 ms (5%) |         | 345.92 KiB (1%) |        6102 |
| `["findfirst", "n=500", "foldl"]`                   |  60.078 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 127.026 ms (5%) |         | 541.66 KiB (1%) |        9442 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 113.256 ms (5%) |         | 297.19 KiB (1%) |        5189 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 113.341 ms (5%) |         | 210.89 KiB (1%) |        3671 |
| `["overhead", "default"]`                           |  60.200 μs (5%) |         |  47.36 KiB (1%) |         382 |
| `["overhead", "stoppable=false"]`                   |  60.700 μs (5%) |         |  47.39 KiB (1%) |         382 |
| `["overhead", "stoppable=true"]`                    | 152.500 μs (5%) |         | 139.67 KiB (1%) |        2464 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   3.049 ms (5%) |         | 730.06 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   3.819 ms (5%) |         |   1.79 MiB (1%) |         213 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   3.321 ms (5%) |         |   1.43 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  12.318 ms (5%) |         |   1.02 MiB (1%) |         157 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  23.150 ms (5%) |         |   1.02 MiB (1%) |        1304 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  17.317 ms (5%) |         |   1.24 MiB (1%) |         907 |
| `["parallel_histogram", "seq"]`                     |   5.473 ms (5%) |         | 364.61 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  31.283 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  14.810 ms (5%) |         |   2.66 KiB (1%) |          48 |
| `["splitby", "count", "foldl"]`                     |   3.490 ms (5%) |         |   96 bytes (1%) |           4 |
| `["splitby", "count", "man"]`                       |   1.547 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    | 754.700 μs (5%) |         |   2.84 KiB (1%) |          54 |
| `["sum", "random", "foldl"]`                        |  11.632 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "random", "reduce", "basesize=128"]`       |   6.114 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "random", "reduce", "basesize=256"]`       |   5.758 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "random", "reduce", "basesize=512"]`       |   5.830 ms (5%) |         |  25.30 KiB (1%) |         252 |
| `["sum", "uniform", "foldl"]`                       |  11.104 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   5.675 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   5.560 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   5.598 ms (5%) |         |  25.25 KiB (1%) |         251 |
| `["sum", "valley", "foldl"]`                        |  11.756 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "valley", "reduce", "basesize=128"]`       |   5.888 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   5.873 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   5.787 ms (5%) |         |  25.25 KiB (1%) |         251 |
| `["words", "nthreads=1"]`                           |  20.486 ms (5%) |         |  31.57 MiB (1%) |     1028929 |
| `["words", "nthreads=2"]`                           |  12.986 ms (5%) |         |  32.29 MiB (1%) |     1029028 |
| `["words", "nthreads=4"]`                           |  15.217 ms (5%) |         |  32.74 MiB (1%) |     1029128 |

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
  CPU: Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz: 
              speed         user         nice          sys         idle          irq
       #1  2294 MHz      52780 s         17 s       2252 s      21838 s          0 s
       #2  2294 MHz      57237 s          3 s       2728 s      16999 s          0 s
       
  Memory: 6.791339874267578 GB (3726.28125 MB free)
  Uptime: 776.0 sec
  Load Avg:  1.5966796875  1.51513671875  0.9638671875
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, broadwell)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 16 May 2021 - 1:36
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
| `["collect", "assoc", "basesize=1"]`                | 203.199 ms (5%) |         |  32.66 MiB (1%) |      286777 |
| `["collect", "assoc", "basesize=1024"]`             | 157.725 ms (5%) |         |   1.79 MiB (1%) |         569 |
| `["collect", "assoc", "basesize=32"]`               | 156.554 ms (5%) |         |   3.97 MiB (1%) |       13306 |
| `["collect", "seq"]`                                | 348.813 ms (5%) |         | 512.72 KiB (1%) |          15 |
| `["collect", "unordered", "basesize=1"]`            | 436.460 ms (5%) |         |  30.01 MiB (1%) |      360690 |
| `["collect", "unordered", "basesize=1024"]`         | 272.904 ms (5%) |         | 890.42 KiB (1%) |        5233 |
| `["collect", "unordered", "basesize=32"]`           | 206.057 ms (5%) |         |   1.47 MiB (1%) |       12611 |
| `["findfirst", "n=1000", "foldl"]`                  | 538.737 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 414.526 ms (5%) |         | 869.22 KiB (1%) |       15191 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 427.353 ms (5%) |         | 473.36 KiB (1%) |        8291 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 502.307 ms (5%) |         | 321.89 KiB (1%) |        5645 |
| `["findfirst", "n=400", "foldl"]`                   | 388.085 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 243.809 ms (5%) |         |   1.07 MiB (1%) |       19260 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 210.061 ms (5%) |         | 581.55 KiB (1%) |       10257 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 229.195 ms (5%) |         | 350.56 KiB (1%) |        6183 |
| `["findfirst", "n=500", "foldl"]`                   |  63.494 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |  61.888 ms (5%) |         | 372.16 KiB (1%) |        6487 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 111.259 ms (5%) |         | 359.48 KiB (1%) |        6275 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  97.977 ms (5%) |         | 185.69 KiB (1%) |        3241 |
| `["overhead", "default"]`                           |  58.700 μs (5%) |         |  47.36 KiB (1%) |         382 |
| `["overhead", "stoppable=false"]`                   |  56.000 μs (5%) |         |  47.39 KiB (1%) |         382 |
| `["overhead", "stoppable=true"]`                    | 144.700 μs (5%) |         | 139.67 KiB (1%) |        2464 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   3.061 ms (5%) |         | 730.06 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   3.829 ms (5%) |         |   1.79 MiB (1%) |         213 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   3.343 ms (5%) |         |   1.43 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  14.525 ms (5%) |         |   1.00 MiB (1%) |         160 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  19.869 ms (5%) |         |   1.00 MiB (1%) |        1116 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  18.192 ms (5%) |         |   1.25 MiB (1%) |         983 |
| `["parallel_histogram", "seq"]`                     |   5.498 ms (5%) |         | 364.61 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  31.329 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  15.739 ms (5%) |         |   2.66 KiB (1%) |          48 |
| `["splitby", "count", "foldl"]`                     |   3.494 ms (5%) |         |   96 bytes (1%) |           4 |
| `["splitby", "count", "man"]`                       |   1.376 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    | 745.400 μs (5%) |         |   2.88 KiB (1%) |          55 |
| `["sum", "random", "foldl"]`                        |  11.422 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "random", "reduce", "basesize=128"]`       |   5.853 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "random", "reduce", "basesize=256"]`       |   5.772 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "random", "reduce", "basesize=512"]`       |   5.647 ms (5%) |         |  25.30 KiB (1%) |         252 |
| `["sum", "uniform", "foldl"]`                       |  11.552 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   5.899 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   5.857 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   5.752 ms (5%) |         |  25.25 KiB (1%) |         251 |
| `["sum", "valley", "foldl"]`                        |  11.840 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "valley", "reduce", "basesize=128"]`       |   6.198 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   6.043 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   6.133 ms (5%) |         |  25.25 KiB (1%) |         251 |
| `["words", "nthreads=1"]`                           |  21.384 ms (5%) |         |  31.87 MiB (1%) |     1038576 |
| `["words", "nthreads=2"]`                           |  14.196 ms (5%) |         |  32.23 MiB (1%) |     1038616 |
| `["words", "nthreads=4"]`                           |  14.206 ms (5%) |         |  33.13 MiB (1%) |     1038790 |

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
  CPU: Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz: 
              speed         user         nice          sys         idle          irq
       #1  2294 MHz      75669 s         17 s       2927 s      32585 s          0 s
       #2  2294 MHz      85206 s          3 s       3361 s      22610 s          0 s
       
  Memory: 6.791339874267578 GB (3692.6796875 MB free)
  Uptime: 1120.0 sec
  Load Avg:  1.5927734375  1.53662109375  1.14111328125
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
    CPU MHz:                         2294.685
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

