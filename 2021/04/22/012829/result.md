# Multi-thread benchmark result

* Pull request commit: [`fa793cbbbda5bb48807ab18028d3cc95d8af9fe2`](https://github.com/JuliaFolds/Transducers.jl/commit/fa793cbbbda5bb48807ab18028d3cc95d8af9fe2)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/243> (Update */Manifest.toml)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 22 Apr 2021 - 01:22
    - Baseline: 22 Apr 2021 - 01:27
* Package commits:
    - Target: 62dfcf
    - Baseline: df8f12
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
| `["collect", "unordered", "basesize=1024"]`         |                1.14 (5%) :x: |                1.08 (1%) :x: |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` |                1.74 (5%) :x: |                1.67 (1%) :x: |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` |                1.14 (5%) :x: |                1.03 (1%) :x: |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 0.92 (5%) :white_check_mark: | 0.88 (1%) :white_check_mark: |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  |                   0.95 (5%)  | 0.97 (1%) :white_check_mark: |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  |                   1.02 (5%)  |                1.04 (1%) :x: |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  |                   1.00 (5%)  |                1.03 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |                1.45 (5%) :x: |                1.32 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 0.78 (5%) :white_check_mark: | 0.78 (1%) :white_check_mark: |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |                1.52 (5%) :x: |                1.52 (1%) :x: |
| `["parallel_histogram", "comm", "basesize=8192"]`   |                1.06 (5%) :x: |                   1.00 (1%)  |
| `["splitby", "count", "man"]`                       |                1.13 (5%) :x: |                   1.00 (1%)  |
| `["words", "nthreads=2"]`                           | 0.94 (5%) :white_check_mark: |                   0.99 (1%)  |
| `["words", "nthreads=4"]`                           | 0.89 (5%) :white_check_mark: |                   1.00 (1%)  |

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
       #1  2397 MHz      54024 s         11 s       2020 s      23762 s          0 s
       #2  2397 MHz      56810 s         10 s       2446 s      20721 s          0 s
       
  Memory: 6.791343688964844 GB (3744.8828125 MB free)
  Uptime: 805.0 sec
  Load Avg:  1.5751953125  1.4833984375  0.904296875
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
       #1  2397 MHz      79577 s         11 s       2615 s      31698 s          0 s
       #2  2397 MHz      82285 s         10 s       3003 s      28828 s          0 s
       
  Memory: 6.791343688964844 GB (3688.73828125 MB free)
  Uptime: 1147.0 sec
  Load Avg:  1.5869140625  1.537109375  1.11083984375
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, haswell)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 22 Apr 2021 - 1:22
* Package commit: 62dfcf
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
| `["collect", "assoc", "basesize=1"]`                | 270.791 ms (5%) |         |  32.66 MiB (1%) |      286757 |
| `["collect", "assoc", "basesize=1024"]`             | 224.769 ms (5%) |         |   1.79 MiB (1%) |         570 |
| `["collect", "assoc", "basesize=32"]`               | 226.408 ms (5%) |         |   3.97 MiB (1%) |       13305 |
| `["collect", "seq"]`                                | 448.684 ms (5%) |         | 512.72 KiB (1%) |          15 |
| `["collect", "unordered", "basesize=1"]`            | 482.527 ms (5%) |         |  30.01 MiB (1%) |      360576 |
| `["collect", "unordered", "basesize=1024"]`         | 328.636 ms (5%) |         | 907.92 KiB (1%) |        5793 |
| `["collect", "unordered", "basesize=32"]`           | 250.395 ms (5%) |         |   1.48 MiB (1%) |       12711 |
| `["findfirst", "n=1000", "foldl"]`                  | 653.998 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 681.805 ms (5%) |         |   1.16 MiB (1%) |       20685 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 528.306 ms (5%) |         | 499.06 KiB (1%) |        8751 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 558.063 ms (5%) |         | 280.98 KiB (1%) |        4940 |
| `["findfirst", "n=400", "foldl"]`                   | 491.259 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 263.592 ms (5%) |         |   1.10 MiB (1%) |       19857 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 269.009 ms (5%) |         | 606.70 KiB (1%) |       10688 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 282.459 ms (5%) |         | 350.47 KiB (1%) |        6179 |
| `["findfirst", "n=500", "foldl"]`                   |  82.911 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 265.668 ms (5%) |         | 998.36 KiB (1%) |       17398 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 131.820 ms (5%) |         | 347.19 KiB (1%) |        6034 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 272.993 ms (5%) |         | 348.81 KiB (1%) |        6085 |
| `["overhead", "default"]`                           |  56.903 μs (5%) |         |  47.36 KiB (1%) |         382 |
| `["overhead", "stoppable=false"]`                   |  55.903 μs (5%) |         |  47.39 KiB (1%) |         382 |
| `["overhead", "stoppable=true"]`                    | 155.007 μs (5%) |         | 139.67 KiB (1%) |        2464 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   4.167 ms (5%) |         | 730.06 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   4.843 ms (5%) |         |   1.79 MiB (1%) |         213 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   4.496 ms (5%) |         |   1.43 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  11.995 ms (5%) |         |   1.22 MiB (1%) |         160 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  19.267 ms (5%) |         |   1.02 MiB (1%) |         576 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  14.382 ms (5%) |         |   1.23 MiB (1%) |         541 |
| `["parallel_histogram", "seq"]`                     |   7.630 ms (5%) |         | 364.61 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  56.908 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  28.127 ms (5%) |         |   2.66 KiB (1%) |          48 |
| `["splitby", "count", "foldl"]`                     |   4.095 ms (5%) |         |   96 bytes (1%) |           4 |
| `["splitby", "count", "man"]`                       |   1.795 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    | 877.538 μs (5%) |         |   2.83 KiB (1%) |          55 |
| `["sum", "random", "foldl"]`                        |  16.514 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "random", "reduce", "basesize=128"]`       |   8.369 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "random", "reduce", "basesize=256"]`       |   8.314 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "random", "reduce", "basesize=512"]`       |   8.233 ms (5%) |         |  25.30 KiB (1%) |         252 |
| `["sum", "uniform", "foldl"]`                       |  15.936 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   8.084 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   7.992 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   7.941 ms (5%) |         |  25.25 KiB (1%) |         251 |
| `["sum", "valley", "foldl"]`                        |  16.411 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "valley", "reduce", "basesize=128"]`       |   8.460 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   8.258 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   8.192 ms (5%) |         |  25.25 KiB (1%) |         251 |
| `["words", "nthreads=1"]`                           |  23.745 ms (5%) |         |  31.77 MiB (1%) |     1034878 |
| `["words", "nthreads=2"]`                           |  14.039 ms (5%) |         |  32.13 MiB (1%) |     1034922 |
| `["words", "nthreads=4"]`                           |  14.267 ms (5%) |         |  32.84 MiB (1%) |     1035004 |

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
       #1  2397 MHz      54024 s         11 s       2020 s      23762 s          0 s
       #2  2397 MHz      56810 s         10 s       2446 s      20721 s          0 s
       
  Memory: 6.791343688964844 GB (3744.8828125 MB free)
  Uptime: 805.0 sec
  Load Avg:  1.5751953125  1.4833984375  0.904296875
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, haswell)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 22 Apr 2021 - 1:27
* Package commit: df8f12
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
| `["collect", "assoc", "basesize=1"]`                | 268.453 ms (5%) |         |  32.66 MiB (1%) |      286758 |
| `["collect", "assoc", "basesize=1024"]`             | 228.795 ms (5%) |         |   1.79 MiB (1%) |         570 |
| `["collect", "assoc", "basesize=32"]`               | 227.007 ms (5%) |         |   3.97 MiB (1%) |       13305 |
| `["collect", "seq"]`                                | 446.221 ms (5%) |         | 512.72 KiB (1%) |          15 |
| `["collect", "unordered", "basesize=1"]`            | 470.394 ms (5%) |         |  30.01 MiB (1%) |      360596 |
| `["collect", "unordered", "basesize=1024"]`         | 288.477 ms (5%) |         | 839.80 KiB (1%) |        3595 |
| `["collect", "unordered", "basesize=32"]`           | 249.776 ms (5%) |         |   1.47 MiB (1%) |       12382 |
| `["findfirst", "n=1000", "foldl"]`                  | 649.821 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 391.388 ms (5%) |         | 710.06 KiB (1%) |       12443 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 463.025 ms (5%) |         | 484.94 KiB (1%) |        8495 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 603.593 ms (5%) |         | 317.56 KiB (1%) |        5575 |
| `["findfirst", "n=400", "foldl"]`                   | 486.987 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 276.505 ms (5%) |         |   1.13 MiB (1%) |       20378 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 262.959 ms (5%) |         | 581.45 KiB (1%) |       10254 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 283.479 ms (5%) |         | 341.36 KiB (1%) |        6024 |
| `["findfirst", "n=500", "foldl"]`                   |  82.603 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 182.888 ms (5%) |         | 754.66 KiB (1%) |       13168 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 169.513 ms (5%) |         | 444.00 KiB (1%) |        7708 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 180.147 ms (5%) |         | 229.59 KiB (1%) |        4013 |
| `["overhead", "default"]`                           |  54.802 μs (5%) |         |  47.36 KiB (1%) |         382 |
| `["overhead", "stoppable=false"]`                   |  56.802 μs (5%) |         |  47.39 KiB (1%) |         382 |
| `["overhead", "stoppable=true"]`                    | 161.807 μs (5%) |         | 139.67 KiB (1%) |        2464 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   4.166 ms (5%) |         | 730.06 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   4.809 ms (5%) |         |   1.79 MiB (1%) |         213 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   4.505 ms (5%) |         |   1.43 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  11.626 ms (5%) |         |   1.22 MiB (1%) |         225 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  18.446 ms (5%) |         |   1.01 MiB (1%) |         952 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  13.559 ms (5%) |         |   1.23 MiB (1%) |         550 |
| `["parallel_histogram", "seq"]`                     |   7.633 ms (5%) |         | 364.61 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  56.653 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  28.107 ms (5%) |         |   2.66 KiB (1%) |          48 |
| `["splitby", "count", "foldl"]`                     |   4.089 ms (5%) |         |   96 bytes (1%) |           4 |
| `["splitby", "count", "man"]`                       |   1.582 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    | 876.339 μs (5%) |         |   2.83 KiB (1%) |          55 |
| `["sum", "random", "foldl"]`                        |  16.313 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "random", "reduce", "basesize=128"]`       |   8.300 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "random", "reduce", "basesize=256"]`       |   8.207 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "random", "reduce", "basesize=512"]`       |   8.147 ms (5%) |         |  25.30 KiB (1%) |         252 |
| `["sum", "uniform", "foldl"]`                       |  15.970 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   8.081 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   7.987 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   7.930 ms (5%) |         |  25.25 KiB (1%) |         251 |
| `["sum", "valley", "foldl"]`                        |  16.377 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "valley", "reduce", "basesize=128"]`       |   8.375 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   8.238 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   8.182 ms (5%) |         |  25.25 KiB (1%) |         251 |
| `["words", "nthreads=1"]`                           |  23.945 ms (5%) |         |  31.72 MiB (1%) |     1033767 |
| `["words", "nthreads=2"]`                           |  14.869 ms (5%) |         |  32.44 MiB (1%) |     1033842 |
| `["words", "nthreads=4"]`                           |  15.979 ms (5%) |         |  32.89 MiB (1%) |     1033924 |

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
       #1  2397 MHz      79577 s         11 s       2615 s      31698 s          0 s
       #2  2397 MHz      82285 s         10 s       3003 s      28828 s          0 s
       
  Memory: 6.791343688964844 GB (3688.73828125 MB free)
  Uptime: 1147.0 sec
  Load Avg:  1.5869140625  1.537109375  1.11083984375
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
    CPU MHz:                         2397.223
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

