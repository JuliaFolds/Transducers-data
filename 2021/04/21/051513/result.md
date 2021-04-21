# Multi-thread benchmark result

* Pull request commit: [`bbf0eb045178a9bdc2ef1198f8c3ed9c64b5a4fd`](https://github.com/JuliaFolds/Transducers.jl/commit/bbf0eb045178a9bdc2ef1198f8c3ed9c64b5a4fd)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/476> (Fix a bug in NondeterministicThreading)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 21 Apr 2021 - 05:09
    - Baseline: 21 Apr 2021 - 05:14
* Package commits:
    - Target: 47fd0e
    - Baseline: 2cc4af
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
| `["collect", "unordered", "basesize=1024"]`         |                1.13 (5%) :x: |                1.11 (1%) :x: |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 0.90 (5%) :white_check_mark: | 0.89 (1%) :white_check_mark: |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` |                   1.00 (5%)  | 0.98 (1%) :white_check_mark: |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` |                1.47 (5%) :x: |                1.39 (1%) :x: |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  |                   1.00 (5%)  | 0.98 (1%) :white_check_mark: |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 0.95 (5%) :white_check_mark: | 0.98 (1%) :white_check_mark: |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  |                   0.99 (5%)  | 0.97 (1%) :white_check_mark: |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |                1.11 (5%) :x: |                1.07 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |                1.16 (5%) :x: |                1.10 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |                1.11 (5%) :x: |                1.06 (1%) :x: |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |                   1.00 (5%)  |                1.15 (1%) :x: |
| `["parallel_histogram", "comm", "basesize=16384"]`  |                   0.98 (5%)  | 0.71 (1%) :white_check_mark: |
| `["parallel_histogram", "comm", "basesize=4096"]`   |                1.10 (5%) :x: |                   0.99 (1%)  |
| `["parallel_histogram", "comm", "basesize=8192"]`   | 0.91 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["splitby", "count", "man"]`                       | 0.91 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["splitby", "count", "reduce"]`                    |                   1.00 (5%)  | 0.96 (1%) :white_check_mark: |
| `["words", "nthreads=2"]`                           | 0.93 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["words", "nthreads=4"]`                           | 0.92 (5%) :white_check_mark: |                   0.99 (1%)  |

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
  CPU: Intel(R) Xeon(R) CPU E5-2673 v3 @ 2.40GHz: 
              speed         user         nice          sys         idle          irq
       #1  2394 MHz      52270 s         18 s       2065 s      49209 s          0 s
       #2  2394 MHz      58835 s          7 s       2399 s      42541 s          0 s
       
  Memory: 6.791343688964844 GB (3678.3828125 MB free)
  Uptime: 1044.0 sec
  Load Avg:  1.84326171875  1.513671875  0.91845703125
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
  uname: Linux 5.4.0-1043-azure #45-Ubuntu SMP Fri Mar 19 17:33:38 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v3 @ 2.40GHz: 
              speed         user         nice          sys         idle          irq
       #1  2394 MHz      71814 s         18 s       2474 s      61159 s          0 s
       #2  2394 MHz      88296 s          7 s       2810 s      44603 s          0 s
       
  Memory: 6.791343688964844 GB (3672.39453125 MB free)
  Uptime: 1365.0 sec
  Load Avg:  1.68603515625  1.5615234375  1.111328125
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, haswell)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 21 Apr 2021 - 5:9
* Package commit: 47fd0e
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
| `["collect", "assoc", "basesize=1"]`                | 293.025 ms (5%) |         |  32.66 MiB (1%) |      286753 |
| `["collect", "assoc", "basesize=1024"]`             | 249.048 ms (5%) |         |   1.79 MiB (1%) |         570 |
| `["collect", "assoc", "basesize=32"]`               | 252.431 ms (5%) |         |   3.97 MiB (1%) |       13306 |
| `["collect", "seq"]`                                | 494.908 ms (5%) |         | 512.72 KiB (1%) |          15 |
| `["collect", "unordered", "basesize=1"]`            | 505.855 ms (5%) |         |  30.01 MiB (1%) |      360578 |
| `["collect", "unordered", "basesize=1024"]`         | 341.607 ms (5%) |         | 933.92 KiB (1%) |        6607 |
| `["collect", "unordered", "basesize=32"]`           | 275.842 ms (5%) |         |   1.47 MiB (1%) |       12616 |
| `["findfirst", "n=1000", "foldl"]`                  | 731.113 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 418.537 ms (5%) |         | 712.42 KiB (1%) |       12483 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 516.460 ms (5%) |         | 487.17 KiB (1%) |        8531 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 773.263 ms (5%) |         | 359.36 KiB (1%) |        6320 |
| `["findfirst", "n=400", "foldl"]`                   | 542.443 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 287.922 ms (5%) |         |   1.06 MiB (1%) |       19079 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 285.929 ms (5%) |         | 581.53 KiB (1%) |       10257 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 308.670 ms (5%) |         | 345.92 KiB (1%) |        6103 |
| `["findfirst", "n=500", "foldl"]`                   |  93.045 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 305.553 ms (5%) |         |   1.01 MiB (1%) |       18162 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 191.735 ms (5%) |         | 409.97 KiB (1%) |        7141 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 170.569 ms (5%) |         | 213.17 KiB (1%) |        3712 |
| `["overhead", "default"]`                           |  60.700 μs (5%) |         |  47.36 KiB (1%) |         382 |
| `["overhead", "stoppable=false"]`                   |  59.800 μs (5%) |         |  47.39 KiB (1%) |         382 |
| `["overhead", "stoppable=true"]`                    | 175.602 μs (5%) |         | 139.67 KiB (1%) |        2464 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   4.741 ms (5%) |         | 730.06 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   5.542 ms (5%) |         |   2.06 MiB (1%) |         219 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   5.103 ms (5%) |         |   1.43 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  12.111 ms (5%) |         | 890.66 KiB (1%) |         131 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  23.175 ms (5%) |         |   1.01 MiB (1%) |        1426 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  13.756 ms (5%) |         |   1.23 MiB (1%) |         307 |
| `["parallel_histogram", "seq"]`                     |   8.654 ms (5%) |         | 364.61 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  63.428 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  31.698 ms (5%) |         |   2.66 KiB (1%) |          48 |
| `["splitby", "count", "foldl"]`                     |   4.722 ms (5%) |         |   96 bytes (1%) |           4 |
| `["splitby", "count", "man"]`                       |   1.813 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    |   1.023 ms (5%) |         |   2.75 KiB (1%) |          51 |
| `["sum", "random", "foldl"]`                        |  18.589 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "random", "reduce", "basesize=128"]`       |   9.511 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "random", "reduce", "basesize=256"]`       |   9.409 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "random", "reduce", "basesize=512"]`       |   9.377 ms (5%) |         |  25.30 KiB (1%) |         252 |
| `["sum", "uniform", "foldl"]`                       |  18.141 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   9.280 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   9.181 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   9.126 ms (5%) |         |  25.25 KiB (1%) |         251 |
| `["sum", "valley", "foldl"]`                        |  18.668 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "valley", "reduce", "basesize=128"]`       |   9.561 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   9.479 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   9.445 ms (5%) |         |  25.25 KiB (1%) |         251 |
| `["words", "nthreads=1"]`                           |  24.678 ms (5%) |         |  31.65 MiB (1%) |     1031239 |
| `["words", "nthreads=2"]`                           |  15.106 ms (5%) |         |  32.37 MiB (1%) |     1031314 |
| `["words", "nthreads=4"]`                           |  15.495 ms (5%) |         |  32.81 MiB (1%) |     1031385 |

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
  CPU: Intel(R) Xeon(R) CPU E5-2673 v3 @ 2.40GHz: 
              speed         user         nice          sys         idle          irq
       #1  2394 MHz      52270 s         18 s       2065 s      49209 s          0 s
       #2  2394 MHz      58835 s          7 s       2399 s      42541 s          0 s
       
  Memory: 6.791343688964844 GB (3678.3828125 MB free)
  Uptime: 1044.0 sec
  Load Avg:  1.84326171875  1.513671875  0.91845703125
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, haswell)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 21 Apr 2021 - 5:14
* Package commit: 2cc4af
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

| ID                                                  | time            | GC time   | memory          | allocations |
|-----------------------------------------------------|----------------:|----------:|----------------:|------------:|
| `["collect", "assoc", "basesize=1"]`                | 292.551 ms (5%) |           |  32.66 MiB (1%) |      286750 |
| `["collect", "assoc", "basesize=1024"]`             | 248.222 ms (5%) |           |   1.79 MiB (1%) |         570 |
| `["collect", "assoc", "basesize=32"]`               | 251.374 ms (5%) |           |   3.97 MiB (1%) |       13306 |
| `["collect", "seq"]`                                | 494.509 ms (5%) |           | 512.72 KiB (1%) |          15 |
| `["collect", "unordered", "basesize=1"]`            | 508.862 ms (5%) | 13.157 ms |  30.01 MiB (1%) |      360602 |
| `["collect", "unordered", "basesize=1024"]`         | 303.036 ms (5%) |           | 843.80 KiB (1%) |        3741 |
| `["collect", "unordered", "basesize=32"]`           | 273.615 ms (5%) |           |   1.47 MiB (1%) |       12501 |
| `["findfirst", "n=1000", "foldl"]`                  | 719.525 ms (5%) |           |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 464.642 ms (5%) |           | 804.77 KiB (1%) |       14077 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 517.444 ms (5%) |           | 498.80 KiB (1%) |        8739 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 524.684 ms (5%) |           | 257.94 KiB (1%) |        4537 |
| `["findfirst", "n=400", "foldl"]`                   | 542.394 ms (5%) |           |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 287.884 ms (5%) |           |   1.08 MiB (1%) |       19477 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 301.237 ms (5%) |           | 595.67 KiB (1%) |       10513 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 311.635 ms (5%) |           | 357.36 KiB (1%) |        6299 |
| `["findfirst", "n=500", "foldl"]`                   |  92.786 ms (5%) |           |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 274.816 ms (5%) |           | 970.47 KiB (1%) |       16904 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 164.888 ms (5%) |           | 373.23 KiB (1%) |        6506 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 153.200 ms (5%) |           | 201.98 KiB (1%) |        3536 |
| `["overhead", "default"]`                           |  61.700 μs (5%) |           |  47.36 KiB (1%) |         382 |
| `["overhead", "stoppable=false"]`                   |  59.700 μs (5%) |           |  47.39 KiB (1%) |         382 |
| `["overhead", "stoppable=true"]`                    | 170.001 μs (5%) |           | 139.67 KiB (1%) |        2464 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   4.798 ms (5%) |           | 730.06 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   5.525 ms (5%) |           |   1.79 MiB (1%) |         213 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   5.153 ms (5%) |           |   1.43 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  12.421 ms (5%) |           |   1.22 MiB (1%) |         186 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  21.040 ms (5%) |           |   1.02 MiB (1%) |        1630 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  15.057 ms (5%) |           |   1.23 MiB (1%) |         304 |
| `["parallel_histogram", "seq"]`                     |   8.741 ms (5%) |           | 364.61 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  63.418 ms (5%) |           |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  31.765 ms (5%) |           |   2.66 KiB (1%) |          48 |
| `["splitby", "count", "foldl"]`                     |   4.744 ms (5%) |           |   96 bytes (1%) |           4 |
| `["splitby", "count", "man"]`                       |   1.991 ms (5%) |           |                 |             |
| `["splitby", "count", "reduce"]`                    |   1.022 ms (5%) |           |   2.88 KiB (1%) |          55 |
| `["sum", "random", "foldl"]`                        |  18.525 ms (5%) |           |   32 bytes (1%) |           2 |
| `["sum", "random", "reduce", "basesize=128"]`       |   9.443 ms (5%) |           | 103.23 KiB (1%) |        1018 |
| `["sum", "random", "reduce", "basesize=256"]`       |   9.385 ms (5%) |           |  51.23 KiB (1%) |         506 |
| `["sum", "random", "reduce", "basesize=512"]`       |   9.310 ms (5%) |           |  25.30 KiB (1%) |         252 |
| `["sum", "uniform", "foldl"]`                       |  18.127 ms (5%) |           |   32 bytes (1%) |           2 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   9.266 ms (5%) |           | 103.23 KiB (1%) |        1018 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   9.173 ms (5%) |           |  51.23 KiB (1%) |         506 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   9.114 ms (5%) |           |  25.25 KiB (1%) |         251 |
| `["sum", "valley", "foldl"]`                        |  18.652 ms (5%) |           |   32 bytes (1%) |           2 |
| `["sum", "valley", "reduce", "basesize=128"]`       |   9.536 ms (5%) |           | 103.23 KiB (1%) |        1018 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   9.436 ms (5%) |           |  51.23 KiB (1%) |         506 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   9.377 ms (5%) |           |  25.25 KiB (1%) |         251 |
| `["words", "nthreads=1"]`                           |  25.440 ms (5%) |           |  31.71 MiB (1%) |     1032883 |
| `["words", "nthreads=2"]`                           |  16.288 ms (5%) |           |  32.42 MiB (1%) |     1032981 |
| `["words", "nthreads=4"]`                           |  16.766 ms (5%) |           |  33.06 MiB (1%) |     1033114 |

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
  CPU: Intel(R) Xeon(R) CPU E5-2673 v3 @ 2.40GHz: 
              speed         user         nice          sys         idle          irq
       #1  2394 MHz      71814 s         18 s       2474 s      61159 s          0 s
       #2  2394 MHz      88296 s          7 s       2810 s      44603 s          0 s
       
  Memory: 6.791343688964844 GB (3672.39453125 MB free)
  Uptime: 1365.0 sec
  Load Avg:  1.68603515625  1.5615234375  1.111328125
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
    CPU MHz:                         2394.457
    BogoMIPS:                        4788.91
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

