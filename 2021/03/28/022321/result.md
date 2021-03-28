# Multi-thread benchmark result

* Pull request commit: [`f2ecac9bf5d1f804a15128e91313869429d759ee`](https://github.com/JuliaFolds/Transducers.jl/commit/f2ecac9bf5d1f804a15128e91313869429d759ee)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/466> (Fix stateful transducers with distributed)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 28 Mar 2021 - 02:17
    - Baseline: 28 Mar 2021 - 02:22
* Package commits:
    - Target: b79da5
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
| `["collect", "assoc", "basesize=1"]`                |                1.08 (5%) :x: |                   1.00 (1%)  |
| `["collect", "assoc", "basesize=1024"]`             |                1.11 (5%) :x: |                   1.00 (1%)  |
| `["collect", "assoc", "basesize=32"]`               |                1.08 (5%) :x: |                   1.00 (1%)  |
| `["collect", "unordered", "basesize=1"]`            |                1.06 (5%) :x: |                   1.00 (1%)  |
| `["collect", "unordered", "basesize=1024"]`         |                1.18 (5%) :x: |                1.07 (1%) :x: |
| `["collect", "unordered", "basesize=32"]`           |                1.06 (5%) :x: |                   0.99 (1%)  |
| `["findfirst", "n=1000", "foldl"]`                  | 0.93 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` |                   1.04 (5%)  |                1.04 (1%) :x: |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 0.90 (5%) :white_check_mark: | 0.91 (1%) :white_check_mark: |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 0.93 (5%) :white_check_mark: | 0.93 (1%) :white_check_mark: |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  |                   1.05 (5%)  | 0.98 (1%) :white_check_mark: |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  |                   1.00 (5%)  | 0.94 (1%) :white_check_mark: |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 0.61 (5%) :white_check_mark: | 0.64 (1%) :white_check_mark: |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 0.79 (5%) :white_check_mark: | 0.84 (1%) :white_check_mark: |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |                2.05 (5%) :x: |                1.63 (1%) :x: |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |                1.09 (5%) :x: |                1.15 (1%) :x: |
| `["parallel_histogram", "comm", "basesize=4096"]`   |                1.22 (5%) :x: |                   1.00 (1%)  |
| `["parallel_histogram", "comm", "basesize=8192"]`   | 0.90 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["splitby", "count", "man"]`                       | 0.91 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["splitby", "count", "reduce"]`                    |                   1.03 (5%)  | 0.98 (1%) :white_check_mark: |
| `["sum", "uniform", "reduce", "basesize=128"]`      |                1.07 (5%) :x: |                   1.00 (1%)  |
| `["sum", "valley", "reduce", "basesize=256"]`       |                1.07 (5%) :x: |                   1.00 (1%)  |
| `["sum", "valley", "reduce", "basesize=512"]`       |                1.06 (5%) :x: |                   1.00 (1%)  |
| `["words", "nthreads=1"]`                           |                   1.02 (5%)  | 0.99 (1%) :white_check_mark: |
| `["words", "nthreads=2"]`                           |                   0.97 (5%)  | 0.98 (1%) :white_check_mark: |
| `["words", "nthreads=4"]`                           |                   0.97 (5%)  | 0.99 (1%) :white_check_mark: |

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
  CPU: Intel(R) Xeon(R) CPU E5-2673 v3 @ 2.40GHz: 
              speed         user         nice          sys         idle          irq
       #1  2397 MHz      55886 s         17 s       2234 s      24354 s          0 s
       #2  2397 MHz      54813 s          7 s       2321 s      25276 s          0 s
       
  Memory: 6.791343688964844 GB (3800.12890625 MB free)
  Uptime: 838.0 sec
  Load Avg:  1.68017578125  1.49658203125  0.9208984375
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, haswell)
```

### Baseline
```
Julia Version 1.5.4
Commit 69fcb5745b (2021-03-11 19:13 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 20.04.2 LTS
  uname: Linux 5.4.0-1041-azure #43-Ubuntu SMP Fri Feb 26 10:21:20 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v3 @ 2.40GHz: 
              speed         user         nice          sys         idle          irq
       #1  2397 MHz      77488 s         17 s       2687 s      34101 s          0 s
       #2  2397 MHz      82179 s          7 s       2753 s      29327 s          0 s
       
  Memory: 6.791343688964844 GB (3807.74609375 MB free)
  Uptime: 1157.0 sec
  Load Avg:  1.7607421875  1.59765625  1.12939453125
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, haswell)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 28 Mar 2021 - 2:17
* Package commit: b79da5
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
| `["collect", "assoc", "basesize=1"]`                | 287.030 ms (5%) |         |  32.66 MiB (1%) |      286760 |
| `["collect", "assoc", "basesize=1024"]`             | 245.819 ms (5%) |         |   1.79 MiB (1%) |         569 |
| `["collect", "assoc", "basesize=32"]`               | 241.073 ms (5%) |         |   3.97 MiB (1%) |       13306 |
| `["collect", "seq"]`                                | 455.191 ms (5%) |         | 512.72 KiB (1%) |          15 |
| `["collect", "unordered", "basesize=1"]`            | 501.544 ms (5%) |         |  30.01 MiB (1%) |      360622 |
| `["collect", "unordered", "basesize=1024"]`         | 320.935 ms (5%) |         | 870.86 KiB (1%) |        4607 |
| `["collect", "unordered", "basesize=32"]`           | 263.414 ms (5%) |         |   1.48 MiB (1%) |       12714 |
| `["findfirst", "n=1000", "foldl"]`                  | 658.509 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 498.510 ms (5%) |         | 862.88 KiB (1%) |       15097 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 469.611 ms (5%) |         | 441.31 KiB (1%) |        7738 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 729.409 ms (5%) |         | 345.50 KiB (1%) |        6077 |
| `["findfirst", "n=400", "foldl"]`                   | 498.597 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 277.788 ms (5%) |         |   1.08 MiB (1%) |       19377 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 290.461 ms (5%) |         | 586.33 KiB (1%) |       10348 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 320.994 ms (5%) |         | 329.92 KiB (1%) |        5828 |
| `["findfirst", "n=500", "foldl"]`                   |  85.463 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 125.787 ms (5%) |         | 522.97 KiB (1%) |        9111 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 162.558 ms (5%) |         | 370.91 KiB (1%) |        6468 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 239.913 ms (5%) |         | 295.95 KiB (1%) |        5162 |
| `["overhead", "default"]`                           |  56.902 μs (5%) |         |  47.36 KiB (1%) |         382 |
| `["overhead", "stoppable=false"]`                   |  56.602 μs (5%) |         |  47.39 KiB (1%) |         382 |
| `["overhead", "stoppable=true"]`                    | 154.105 μs (5%) |         | 139.67 KiB (1%) |        2464 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   4.326 ms (5%) |         | 730.06 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   5.259 ms (5%) |         |   2.06 MiB (1%) |         219 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   4.642 ms (5%) |         |   1.43 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  11.789 ms (5%) |         |   1.22 MiB (1%) |         160 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  20.857 ms (5%) |         |   1.01 MiB (1%) |        1413 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  13.365 ms (5%) |         |   1.23 MiB (1%) |         388 |
| `["parallel_histogram", "seq"]`                     |   7.593 ms (5%) |         | 364.61 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  57.142 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  29.737 ms (5%) |         |   2.66 KiB (1%) |          48 |
| `["splitby", "count", "foldl"]`                     |   4.154 ms (5%) |         |   96 bytes (1%) |           4 |
| `["splitby", "count", "man"]`                       |   1.583 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    | 915.032 μs (5%) |         |   2.78 KiB (1%) |          52 |
| `["sum", "random", "foldl"]`                        |  16.329 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "random", "reduce", "basesize=128"]`       |   8.657 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "random", "reduce", "basesize=256"]`       |   8.829 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "random", "reduce", "basesize=512"]`       |   8.759 ms (5%) |         |  25.30 KiB (1%) |         252 |
| `["sum", "uniform", "foldl"]`                       |  15.958 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   8.617 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   8.348 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   8.338 ms (5%) |         |  25.25 KiB (1%) |         251 |
| `["sum", "valley", "foldl"]`                        |  16.435 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "valley", "reduce", "basesize=128"]`       |   8.695 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   8.842 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   8.660 ms (5%) |         |  25.25 KiB (1%) |         251 |
| `["words", "nthreads=1"]`                           |  23.576 ms (5%) |         |  31.28 MiB (1%) |     1018622 |
| `["words", "nthreads=2"]`                           |  14.663 ms (5%) |         |  31.64 MiB (1%) |     1018673 |
| `["words", "nthreads=4"]`                           |  15.524 ms (5%) |         |  32.54 MiB (1%) |     1018816 |

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
  CPU: Intel(R) Xeon(R) CPU E5-2673 v3 @ 2.40GHz: 
              speed         user         nice          sys         idle          irq
       #1  2397 MHz      55886 s         17 s       2234 s      24354 s          0 s
       #2  2397 MHz      54813 s          7 s       2321 s      25276 s          0 s
       
  Memory: 6.791343688964844 GB (3800.12890625 MB free)
  Uptime: 838.0 sec
  Load Avg:  1.68017578125  1.49658203125  0.9208984375
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, haswell)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 28 Mar 2021 - 2:22
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
| `["collect", "assoc", "basesize=1"]`                | 265.916 ms (5%) |         |  32.66 MiB (1%) |      286749 |
| `["collect", "assoc", "basesize=1024"]`             | 222.311 ms (5%) |         |   1.79 MiB (1%) |         570 |
| `["collect", "assoc", "basesize=32"]`               | 223.974 ms (5%) |         |   3.97 MiB (1%) |       13306 |
| `["collect", "seq"]`                                | 438.453 ms (5%) |         | 512.72 KiB (1%) |          15 |
| `["collect", "unordered", "basesize=1"]`            | 472.403 ms (5%) |         |  30.01 MiB (1%) |      360585 |
| `["collect", "unordered", "basesize=1024"]`         | 271.897 ms (5%) |         | 817.48 KiB (1%) |        2899 |
| `["collect", "unordered", "basesize=32"]`           | 247.904 ms (5%) |         |   1.49 MiB (1%) |       12999 |
| `["findfirst", "n=1000", "foldl"]`                  | 711.857 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 481.139 ms (5%) |         | 830.52 KiB (1%) |       14534 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 522.871 ms (5%) |         | 485.03 KiB (1%) |        8498 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 698.891 ms (5%) |         | 343.06 KiB (1%) |        6030 |
| `["findfirst", "n=400", "foldl"]`                   | 491.501 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 299.415 ms (5%) |         |   1.16 MiB (1%) |       20786 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 277.741 ms (5%) |         | 595.44 KiB (1%) |       10501 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 320.964 ms (5%) |         | 350.56 KiB (1%) |        6183 |
| `["findfirst", "n=500", "foldl"]`                   |  86.337 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 206.554 ms (5%) |         | 817.19 KiB (1%) |       14242 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 204.686 ms (5%) |         | 443.88 KiB (1%) |        7795 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 117.291 ms (5%) |         | 181.11 KiB (1%) |        3162 |
| `["overhead", "default"]`                           |  55.902 μs (5%) |         |  47.36 KiB (1%) |         382 |
| `["overhead", "stoppable=false"]`                   |  55.302 μs (5%) |         |  47.39 KiB (1%) |         382 |
| `["overhead", "stoppable=true"]`                    | 159.506 μs (5%) |         | 139.67 KiB (1%) |        2464 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   4.137 ms (5%) |         | 730.06 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   4.814 ms (5%) |         |   1.79 MiB (1%) |         213 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   4.469 ms (5%) |         |   1.43 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  11.337 ms (5%) |         |   1.22 MiB (1%) |         203 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  17.166 ms (5%) |         |   1.01 MiB (1%) |        1106 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  14.801 ms (5%) |         |   1.23 MiB (1%) |         371 |
| `["parallel_histogram", "seq"]`                     |   7.547 ms (5%) |         | 364.61 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  56.853 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  29.202 ms (5%) |         |   2.66 KiB (1%) |          48 |
| `["splitby", "count", "foldl"]`                     |   4.118 ms (5%) |         |   96 bytes (1%) |           4 |
| `["splitby", "count", "man"]`                       |   1.736 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    | 891.432 μs (5%) |         |   2.84 KiB (1%) |          54 |
| `["sum", "random", "foldl"]`                        |  16.622 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "random", "reduce", "basesize=128"]`       |   8.818 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "random", "reduce", "basesize=256"]`       |   8.813 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "random", "reduce", "basesize=512"]`       |   8.811 ms (5%) |         |  25.30 KiB (1%) |         252 |
| `["sum", "uniform", "foldl"]`                       |  15.932 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   8.074 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   8.659 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   8.512 ms (5%) |         |  25.25 KiB (1%) |         251 |
| `["sum", "valley", "foldl"]`                        |  16.293 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "valley", "reduce", "basesize=128"]`       |   8.305 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   8.239 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   8.165 ms (5%) |         |  25.25 KiB (1%) |         251 |
| `["words", "nthreads=1"]`                           |  23.217 ms (5%) |         |  31.71 MiB (1%) |     1032923 |
| `["words", "nthreads=2"]`                           |  15.069 ms (5%) |         |  32.42 MiB (1%) |     1032995 |
| `["words", "nthreads=4"]`                           |  16.015 ms (5%) |         |  32.87 MiB (1%) |     1033074 |

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
  CPU: Intel(R) Xeon(R) CPU E5-2673 v3 @ 2.40GHz: 
              speed         user         nice          sys         idle          irq
       #1  2397 MHz      77488 s         17 s       2687 s      34101 s          0 s
       #2  2397 MHz      82179 s          7 s       2753 s      29327 s          0 s
       
  Memory: 6.791343688964844 GB (3807.74609375 MB free)
  Uptime: 1157.0 sec
  Load Avg:  1.7607421875  1.59765625  1.12939453125
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, haswell)
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
    Model:                           63
    Model name:                      Intel(R) Xeon(R) CPU E5-2673 v3 @ 2.40GHz
    Stepping:                        2
    CPU MHz:                         2397.220
    BogoMIPS:                        4794.44
    Hypervisor vendor:               Microsoft
    Virtualization type:             full
    L1d cache:                       64 KiB
    L1i cache:                       64 KiB
    L2 cache:                        512 KiB
    L3 cache:                        30 MiB
    NUMA node0 CPU(s):               0,1
    Vulnerability Itlb multihit:     KVM: Vulnerable
    Vulnerability L1tf:              Mitigation; PTE Inversion
    Vulnerability Mds:               Mitigation; Clear CPU buffers; SMT Host state unknown
    Vulnerability Meltdown:          Mitigation; PTI
    Vulnerability Spec store bypass: Vulnerable
    Vulnerability Spectre v1:        Mitigation; usercopy/swapgs barriers and __user pointer sanitization
    Vulnerability Spectre v2:        Mitigation; Full generic retpoline, STIBP disabled, RSB filling
    Vulnerability Srbds:             Not affected
    Vulnerability Tsx async abort:   Not affected
    Flags:                           fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush mmx fxsr sse sse2 ss ht syscall nx pdpe1gb rdtscp lm constant_tsc rep_good nopl xtopology cpuid pni pclmulqdq ssse3 fma cx16 pcid sse4_1 sse4_2 movbe popcnt aes xsave avx f16c rdrand hypervisor lahf_lm abm invpcid_single pti fsgsbase bmi1 avx2 smep bmi2 erms invpcid xsaveopt md_clear
    

| Cpu Property       | Value                                                   |
|:------------------ |:------------------------------------------------------- |
| Brand              | Intel(R) Xeon(R) CPU E5-2673 v3 @ 2.40GHz               |
| Vendor             | :Intel                                                  |
| Architecture       | :Haswell                                                |
| Model              | Family: 0x06, Model: 0x3f, Stepping: 0x02, Type: 0x00   |
| Cores              | 2 physical cores, 2 logical cores (on executing CPU)    |
|                    | No Hyperthreading hardware capability detected          |
| Clock Frequencies  | Not supported by CPU                                    |
| Data Cache         | Level 1:3 : (32, 256, 30720) kbytes                     |
|                    | 64 byte cache line size                                 |
| Address Size       | 48 bits virtual, 46 bits physical                       |
| SIMD               | 256 bit = 32 byte max. SIMD vector size                 |
| Time Stamp Counter | TSC is accessible via `rdtsc`                           |
|                    | TSC increased at every clock cycle (non-invariant TSC)  |
| Perf. Monitoring   | Performance Monitoring Counters (PMC) are not supported |
| Hypervisor         | Yes, Microsoft                                          |

