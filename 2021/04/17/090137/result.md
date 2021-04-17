# Multi-thread benchmark result

* Pull request commit: [`280a3e8d3a5e8a3ceb0e947a7f5a0a51c322e94c`](https://github.com/JuliaFolds/Transducers.jl/commit/280a3e8d3a5e8a3ceb0e947a7f5a0a51c322e94c)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/469> (Make transducer listing work again)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 17 Apr 2021 - 08:55
    - Baseline: 17 Apr 2021 - 09:01
* Package commits:
    - Target: c087ab
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
| `["collect", "unordered", "basesize=1"]`            | 0.94 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["collect", "unordered", "basesize=1024"]`         |                1.24 (5%) :x: |                1.15 (1%) :x: |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` |                1.53 (5%) :x: |                1.52 (1%) :x: |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 0.86 (5%) :white_check_mark: | 0.88 (1%) :white_check_mark: |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  |                   1.00 (5%)  | 0.98 (1%) :white_check_mark: |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  |                   1.01 (5%)  |                1.04 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 0.83 (5%) :white_check_mark: | 0.89 (1%) :white_check_mark: |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |                1.41 (5%) :x: |                1.37 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |                1.37 (5%) :x: |                1.23 (1%) :x: |
| `["parallel_histogram", "comm", "basesize=16384"]`  |                1.08 (5%) :x: |                   1.00 (1%)  |
| `["splitby", "count", "foldl"]`                     | 0.88 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["splitby", "count", "man"]`                       | 0.77 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["splitby", "count", "reduce"]`                    | 0.84 (5%) :white_check_mark: |                   0.99 (1%)  |
| `["sum", "random", "reduce", "basesize=512"]`       | 0.94 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["sum", "uniform", "reduce", "basesize=512"]`      | 0.95 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["sum", "valley", "reduce", "basesize=512"]`       | 0.95 (5%) :white_check_mark: |                   1.00 (1%)  |

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
       #1  2095 MHz      55634 s         24 s       2360 s      25062 s          0 s
       #2  2095 MHz      54583 s          2 s       2465 s      26280 s          0 s
       
  Memory: 6.791343688964844 GB (3709.359375 MB free)
  Uptime: 840.0 sec
  Load Avg:  1.7421875  1.5078125  0.9287109375
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
       #1  2095 MHz      75922 s         24 s       2848 s      36020 s          0 s
       #2  2095 MHz      82887 s          2 s       2916 s      29187 s          0 s
       
  Memory: 6.791343688964844 GB (3653.16796875 MB free)
  Uptime: 1159.0 sec
  Load Avg:  1.76708984375  1.5869140625  1.12841796875
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, skylake-avx512)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 17 Apr 2021 - 8:55
* Package commit: c087ab
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
| `["collect", "assoc", "basesize=1"]`                | 282.614 ms (5%) |         |  32.66 MiB (1%) |      286746 |
| `["collect", "assoc", "basesize=1024"]`             | 233.981 ms (5%) |         |   1.79 MiB (1%) |         569 |
| `["collect", "assoc", "basesize=32"]`               | 240.475 ms (5%) |         |   3.97 MiB (1%) |       13306 |
| `["collect", "seq"]`                                | 466.104 ms (5%) |         | 512.72 KiB (1%) |          15 |
| `["collect", "unordered", "basesize=1"]`            | 475.434 ms (5%) |         |  30.01 MiB (1%) |      360569 |
| `["collect", "unordered", "basesize=1024"]`         | 405.787 ms (5%) |         |   1.02 MiB (1%) |       10318 |
| `["collect", "unordered", "basesize=32"]`           | 266.468 ms (5%) |         |   1.47 MiB (1%) |       12542 |
| `["findfirst", "n=1000", "foldl"]`                  | 751.013 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 880.496 ms (5%) |         |   1.34 MiB (1%) |       23964 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 503.315 ms (5%) |         | 466.45 KiB (1%) |        8172 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 674.018 ms (5%) |         | 319.91 KiB (1%) |        5616 |
| `["findfirst", "n=400", "foldl"]`                   | 554.230 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 302.029 ms (5%) |         |   1.05 MiB (1%) |       18951 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 311.755 ms (5%) |         | 595.41 KiB (1%) |       10500 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 341.668 ms (5%) |         | 368.84 KiB (1%) |        6499 |
| `["findfirst", "n=500", "foldl"]`                   |  94.557 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 220.968 ms (5%) |         | 844.48 KiB (1%) |       14688 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 188.121 ms (5%) |         | 416.81 KiB (1%) |        7253 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 383.458 ms (5%) |         | 365.73 KiB (1%) |        6412 |
| `["overhead", "default"]`                           |  64.900 μs (5%) |         |  47.33 KiB (1%) |         381 |
| `["overhead", "stoppable=false"]`                   |  65.600 μs (5%) |         |  47.36 KiB (1%) |         381 |
| `["overhead", "stoppable=true"]`                    | 170.701 μs (5%) |         | 139.67 KiB (1%) |        2464 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   4.586 ms (5%) |         | 730.06 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   5.351 ms (5%) |         |   1.79 MiB (1%) |         213 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   5.021 ms (5%) |         |   1.43 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  16.433 ms (5%) |         |   1.23 MiB (1%) |         588 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  25.048 ms (5%) |         |   1.04 MiB (1%) |        1041 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  20.390 ms (5%) |         |   1.26 MiB (1%) |        1537 |
| `["parallel_histogram", "seq"]`                     |   8.386 ms (5%) |         | 364.61 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  38.284 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  19.471 ms (5%) |         |   2.66 KiB (1%) |          48 |
| `["splitby", "count", "foldl"]`                     |   4.739 ms (5%) |         |   96 bytes (1%) |           4 |
| `["splitby", "count", "man"]`                       |   1.653 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    |   1.142 ms (5%) |         |   2.83 KiB (1%) |          55 |
| `["sum", "random", "foldl"]`                        |  17.924 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "random", "reduce", "basesize=128"]`       |   9.384 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "random", "reduce", "basesize=256"]`       |   9.084 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "random", "reduce", "basesize=512"]`       |   8.894 ms (5%) |         |  25.30 KiB (1%) |         252 |
| `["sum", "uniform", "foldl"]`                       |  17.450 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   9.062 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   8.873 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   8.823 ms (5%) |         |  25.25 KiB (1%) |         251 |
| `["sum", "valley", "foldl"]`                        |  18.254 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "valley", "reduce", "basesize=128"]`       |   9.346 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   9.346 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   9.197 ms (5%) |         |  25.25 KiB (1%) |         251 |
| `["words", "nthreads=1"]`                           |  25.728 ms (5%) |         |  31.66 MiB (1%) |     1031520 |
| `["words", "nthreads=2"]`                           |  15.439 ms (5%) |         |  32.01 MiB (1%) |     1031556 |
| `["words", "nthreads=4"]`                           |  16.058 ms (5%) |         |  32.73 MiB (1%) |     1031638 |

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
       #1  2095 MHz      55634 s         24 s       2360 s      25062 s          0 s
       #2  2095 MHz      54583 s          2 s       2465 s      26280 s          0 s
       
  Memory: 6.791343688964844 GB (3709.359375 MB free)
  Uptime: 840.0 sec
  Load Avg:  1.7421875  1.5078125  0.9287109375
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, skylake-avx512)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 17 Apr 2021 - 9:1
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
| `["collect", "assoc", "basesize=1"]`                | 285.344 ms (5%) |         |  32.66 MiB (1%) |      286745 |
| `["collect", "assoc", "basesize=1024"]`             | 240.001 ms (5%) |         |   1.79 MiB (1%) |         570 |
| `["collect", "assoc", "basesize=32"]`               | 243.055 ms (5%) |         |   3.97 MiB (1%) |       13305 |
| `["collect", "seq"]`                                | 472.303 ms (5%) |         | 512.72 KiB (1%) |          15 |
| `["collect", "unordered", "basesize=1"]`            | 508.481 ms (5%) |         |  30.01 MiB (1%) |      360606 |
| `["collect", "unordered", "basesize=1024"]`         | 326.160 ms (5%) |         | 912.30 KiB (1%) |        5933 |
| `["collect", "unordered", "basesize=32"]`           | 269.028 ms (5%) |         |   1.47 MiB (1%) |       12501 |
| `["findfirst", "n=1000", "foldl"]`                  | 760.220 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 574.315 ms (5%) |         | 898.88 KiB (1%) |       15778 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 508.960 ms (5%) |         | 466.42 KiB (1%) |        8171 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 786.163 ms (5%) |         | 363.73 KiB (1%) |        6386 |
| `["findfirst", "n=400", "foldl"]`                   | 563.425 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 302.868 ms (5%) |         |   1.07 MiB (1%) |       19259 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 310.293 ms (5%) |         | 597.81 KiB (1%) |       10543 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 339.830 ms (5%) |         | 355.16 KiB (1%) |        6262 |
| `["findfirst", "n=500", "foldl"]`                   |  97.502 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 266.279 ms (5%) |         | 951.94 KiB (1%) |       16589 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 133.547 ms (5%) |         | 304.28 KiB (1%) |        5314 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 279.991 ms (5%) |         | 296.34 KiB (1%) |        5187 |
| `["overhead", "default"]`                           |  68.300 μs (5%) |         |  47.33 KiB (1%) |         381 |
| `["overhead", "stoppable=false"]`                   |  68.001 μs (5%) |         |  47.36 KiB (1%) |         381 |
| `["overhead", "stoppable=true"]`                    | 167.801 μs (5%) |         | 139.67 KiB (1%) |        2464 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   4.660 ms (5%) |         | 730.06 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   5.504 ms (5%) |         |   1.79 MiB (1%) |         213 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   5.075 ms (5%) |         |   1.43 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  15.221 ms (5%) |         |   1.23 MiB (1%) |         522 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  25.556 ms (5%) |         |   1.04 MiB (1%) |        1483 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  20.377 ms (5%) |         |   1.27 MiB (1%) |        1666 |
| `["parallel_histogram", "seq"]`                     |   8.453 ms (5%) |         | 364.61 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  40.211 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  20.288 ms (5%) |         |   2.66 KiB (1%) |          48 |
| `["splitby", "count", "foldl"]`                     |   5.406 ms (5%) |         |   96 bytes (1%) |           4 |
| `["splitby", "count", "man"]`                       |   2.154 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    |   1.365 ms (5%) |         |   2.84 KiB (1%) |          54 |
| `["sum", "random", "foldl"]`                        |  18.675 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "random", "reduce", "basesize=128"]`       |   9.680 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "random", "reduce", "basesize=256"]`       |   9.515 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "random", "reduce", "basesize=512"]`       |   9.466 ms (5%) |         |  25.30 KiB (1%) |         252 |
| `["sum", "uniform", "foldl"]`                       |  18.151 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   9.426 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   9.232 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   9.308 ms (5%) |         |  25.25 KiB (1%) |         251 |
| `["sum", "valley", "foldl"]`                        |  18.876 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "valley", "reduce", "basesize=128"]`       |   9.712 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   9.754 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   9.701 ms (5%) |         |  25.25 KiB (1%) |         251 |
| `["words", "nthreads=1"]`                           |  25.871 ms (5%) |         |  31.46 MiB (1%) |     1024686 |
| `["words", "nthreads=2"]`                           |  16.010 ms (5%) |         |  31.82 MiB (1%) |     1024722 |
| `["words", "nthreads=4"]`                           |  16.392 ms (5%) |         |  32.53 MiB (1%) |     1024814 |

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
       #1  2095 MHz      75922 s         24 s       2848 s      36020 s          0 s
       #2  2095 MHz      82887 s          2 s       2916 s      29187 s          0 s
       
  Memory: 6.791343688964844 GB (3653.16796875 MB free)
  Uptime: 1159.0 sec
  Load Avg:  1.76708984375  1.5869140625  1.12841796875
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
    CPU MHz:                         2095.075
    BogoMIPS:                        4190.15
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

