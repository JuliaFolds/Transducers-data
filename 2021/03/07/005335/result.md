# Multi-thread benchmark result

* Pull request commit: [`d04176a94fa92eaf4461feabae61d59c5e42fc19`](https://github.com/JuliaFolds/Transducers.jl/commit/d04176a94fa92eaf4461feabae61d59c5e42fc19)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/460> (Better executor support with Referenceables)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 7 Mar 2021 - 00:48
    - Baseline: 7 Mar 2021 - 00:53
* Package commits:
    - Target: 835795
    - Baseline: 2e58c7
* Julia commits:
    - Target: 788b2c
    - Baseline: 788b2c
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
| `["findfirst", "n=1000", "reduce", "basesize=128"]` |                1.09 (5%) :x: |                1.11 (1%) :x: |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 0.84 (5%) :white_check_mark: | 0.87 (1%) :white_check_mark: |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` |                1.08 (5%) :x: |                1.16 (1%) :x: |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  |                   1.01 (5%)  |                1.02 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 0.76 (5%) :white_check_mark: | 0.86 (1%) :white_check_mark: |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |                2.75 (5%) :x: |                2.60 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 0.56 (5%) :white_check_mark: | 0.72 (1%) :white_check_mark: |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |                   1.02 (5%)  | 0.87 (1%) :white_check_mark: |
| `["parallel_histogram", "comm", "basesize=16384"]`  |                1.06 (5%) :x: |                   1.00 (1%)  |
| `["parallel_histogram", "comm", "basesize=8192"]`   |                1.25 (5%) :x: |                1.01 (1%) :x: |

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
Julia Version 1.5.3
Commit 788b2c77c1 (2020-11-09 13:37 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 20.04.2 LTS
  uname: Linux 5.4.0-1040-azure #42-Ubuntu SMP Fri Feb 5 15:39:06 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz      54963 s         16 s       2212 s      15913 s          0 s
       #2  2095 MHz      50201 s          6 s       2509 s      20122 s          0 s
       
  Memory: 6.7913818359375 GB (3726.375 MB free)
  Uptime: 743.0 sec
  Load Avg:  1.61669921875  1.50634765625  0.93212890625
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, skylake-avx512)
```

### Baseline
```
Julia Version 1.5.3
Commit 788b2c77c1 (2020-11-09 13:37 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 20.04.2 LTS
  uname: Linux 5.4.0-1040-azure #42-Ubuntu SMP Fri Feb 5 15:39:06 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz      75484 s         16 s       2687 s      24414 s          0 s
       #2  2095 MHz      75454 s          6 s       3032 s      23780 s          0 s
       
  Memory: 6.7913818359375 GB (3752.3359375 MB free)
  Uptime: 1039.0 sec
  Load Avg:  1.642578125  1.53271484375  1.099609375
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, skylake-avx512)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 7 Mar 2021 - 0:48
* Package commit: 835795
* Julia commit: 788b2c
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
| `["collect", "assoc", "basesize=1"]`                | 262.017 ms (5%) |         |  32.66 MiB (1%) |      286742 |
| `["collect", "assoc", "basesize=1024"]`             | 219.058 ms (5%) |         |   1.79 MiB (1%) |         570 |
| `["collect", "assoc", "basesize=32"]`               | 219.691 ms (5%) |         |   3.97 MiB (1%) |       13305 |
| `["collect", "seq"]`                                | 434.163 ms (5%) |         | 512.72 KiB (1%) |          15 |
| `["collect", "unordered", "basesize=1"]`            | 467.308 ms (5%) |         |  30.01 MiB (1%) |      360572 |
| `["collect", "unordered", "basesize=1024"]`         | 286.160 ms (5%) |         | 821.33 KiB (1%) |        3004 |
| `["collect", "unordered", "basesize=32"]`           | 246.513 ms (5%) |         |   1.47 MiB (1%) |       12479 |
| `["findfirst", "n=1000", "foldl"]`                  | 694.171 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 468.118 ms (5%) |         | 828.03 KiB (1%) |       14482 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 488.929 ms (5%) |         | 466.42 KiB (1%) |        8171 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 710.227 ms (5%) |         | 381.64 KiB (1%) |        6683 |
| `["findfirst", "n=400", "foldl"]`                   | 516.870 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 280.460 ms (5%) |         |   1.06 MiB (1%) |       19101 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 300.004 ms (5%) |         | 607.13 KiB (1%) |       10711 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 313.780 ms (5%) |         | 368.81 KiB (1%) |        6500 |
| `["findfirst", "n=500", "foldl"]`                   |  84.546 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 159.645 ms (5%) |         | 691.28 KiB (1%) |       12019 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 369.745 ms (5%) |         | 744.75 KiB (1%) |       12987 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 258.826 ms (5%) |         | 312.02 KiB (1%) |        5441 |
| `["overhead", "default"]`                           |  58.303 μs (5%) |         |  47.33 KiB (1%) |         381 |
| `["overhead", "stoppable=false"]`                   |  61.803 μs (5%) |         |  47.36 KiB (1%) |         381 |
| `["overhead", "stoppable=true"]`                    | 147.809 μs (5%) |         | 139.67 KiB (1%) |        2464 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   3.892 ms (5%) |         | 730.06 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   4.630 ms (5%) |         |   1.79 MiB (1%) |         213 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   4.187 ms (5%) |         |   1.43 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  15.332 ms (5%) |         |   1.22 MiB (1%) |         320 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  23.776 ms (5%) |         |   1.05 MiB (1%) |        1771 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  19.727 ms (5%) |         |   1.25 MiB (1%) |         964 |
| `["parallel_histogram", "seq"]`                     |   7.094 ms (5%) |         | 364.61 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  34.633 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  17.561 ms (5%) |         |   2.66 KiB (1%) |          48 |
| `["sum", "random", "foldl"]`                        |  16.114 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "random", "reduce", "basesize=128"]`       |   8.295 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "random", "reduce", "basesize=256"]`       |   8.099 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "random", "reduce", "basesize=512"]`       |   8.104 ms (5%) |         |  25.30 KiB (1%) |         252 |
| `["sum", "uniform", "foldl"]`                       |  15.512 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   8.139 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   7.808 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   7.932 ms (5%) |         |  25.25 KiB (1%) |         251 |
| `["sum", "valley", "foldl"]`                        |  16.335 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "valley", "reduce", "basesize=128"]`       |   8.324 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   8.156 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   8.362 ms (5%) |         |  25.25 KiB (1%) |         251 |
| `["words", "nthreads=1"]`                           |  22.477 ms (5%) |         |  31.53 MiB (1%) |     1027320 |
| `["words", "nthreads=2"]`                           |  14.303 ms (5%) |         |  31.89 MiB (1%) |     1027379 |
| `["words", "nthreads=4"]`                           |  14.216 ms (5%) |         |  32.60 MiB (1%) |     1027451 |

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
- `["sum", "random"]`
- `["sum", "random", "reduce"]`
- `["sum", "uniform"]`
- `["sum", "uniform", "reduce"]`
- `["sum", "valley"]`
- `["sum", "valley", "reduce"]`
- `["words"]`

## Julia versioninfo
```
Julia Version 1.5.3
Commit 788b2c77c1 (2020-11-09 13:37 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 20.04.2 LTS
  uname: Linux 5.4.0-1040-azure #42-Ubuntu SMP Fri Feb 5 15:39:06 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz      54963 s         16 s       2212 s      15913 s          0 s
       #2  2095 MHz      50201 s          6 s       2509 s      20122 s          0 s
       
  Memory: 6.7913818359375 GB (3726.375 MB free)
  Uptime: 743.0 sec
  Load Avg:  1.61669921875  1.50634765625  0.93212890625
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, skylake-avx512)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 7 Mar 2021 - 0:53
* Package commit: 2e58c7
* Julia commit: 788b2c
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
| `["collect", "assoc", "basesize=1"]`                | 262.233 ms (5%) |         |  32.66 MiB (1%) |      286742 |
| `["collect", "assoc", "basesize=1024"]`             | 226.061 ms (5%) |         |   1.79 MiB (1%) |         570 |
| `["collect", "assoc", "basesize=32"]`               | 224.205 ms (5%) |         |   3.97 MiB (1%) |       13306 |
| `["collect", "seq"]`                                | 433.048 ms (5%) |         | 512.72 KiB (1%) |          15 |
| `["collect", "unordered", "basesize=1"]`            | 477.326 ms (5%) |         |  30.01 MiB (1%) |      360615 |
| `["collect", "unordered", "basesize=1024"]`         | 290.463 ms (5%) |         | 824.98 KiB (1%) |        3139 |
| `["collect", "unordered", "basesize=32"]`           | 249.649 ms (5%) |         |   1.47 MiB (1%) |       12439 |
| `["findfirst", "n=1000", "foldl"]`                  | 694.282 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 429.071 ms (5%) |         | 746.97 KiB (1%) |       13077 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 584.177 ms (5%) |         | 536.23 KiB (1%) |        9410 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 654.825 ms (5%) |         | 329.00 KiB (1%) |        5774 |
| `["findfirst", "n=400", "foldl"]`                   | 520.782 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 289.008 ms (5%) |         |   1.07 MiB (1%) |       19259 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 296.821 ms (5%) |         | 597.73 KiB (1%) |       10539 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 327.408 ms (5%) |         | 366.59 KiB (1%) |        6466 |
| `["findfirst", "n=500", "foldl"]`                   |  87.216 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 210.636 ms (5%) |         | 803.22 KiB (1%) |       13992 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 134.272 ms (5%) |         | 285.94 KiB (1%) |        5003 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 462.380 ms (5%) |         | 430.64 KiB (1%) |        7564 |
| `["overhead", "default"]`                           |  59.003 μs (5%) |         |  47.33 KiB (1%) |         381 |
| `["overhead", "stoppable=false"]`                   |  59.803 μs (5%) |         |  47.36 KiB (1%) |         381 |
| `["overhead", "stoppable=true"]`                    | 145.407 μs (5%) |         | 139.67 KiB (1%) |        2464 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   3.852 ms (5%) |         | 730.06 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   4.528 ms (5%) |         |   2.06 MiB (1%) |         219 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   4.150 ms (5%) |         |   1.43 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  14.443 ms (5%) |         |   1.22 MiB (1%) |         160 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  24.993 ms (5%) |         |   1.05 MiB (1%) |        1608 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  15.743 ms (5%) |         |   1.23 MiB (1%) |         424 |
| `["parallel_histogram", "seq"]`                     |   7.048 ms (5%) |         | 364.61 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  35.324 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  17.767 ms (5%) |         |   2.66 KiB (1%) |          48 |
| `["sum", "random", "foldl"]`                        |  16.214 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "random", "reduce", "basesize=128"]`       |   8.347 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "random", "reduce", "basesize=256"]`       |   8.462 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "random", "reduce", "basesize=512"]`       |   8.345 ms (5%) |         |  25.30 KiB (1%) |         252 |
| `["sum", "uniform", "foldl"]`                       |  15.918 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   8.221 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   8.101 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   8.099 ms (5%) |         |  25.25 KiB (1%) |         251 |
| `["sum", "valley", "foldl"]`                        |  16.275 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "valley", "reduce", "basesize=128"]`       |   8.480 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   8.179 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   8.264 ms (5%) |         |  25.25 KiB (1%) |         251 |
| `["words", "nthreads=1"]`                           |  22.212 ms (5%) |         |  31.82 MiB (1%) |     1036862 |
| `["words", "nthreads=2"]`                           |  14.610 ms (5%) |         |  32.18 MiB (1%) |     1036898 |
| `["words", "nthreads=4"]`                           |  14.618 ms (5%) |         |  32.89 MiB (1%) |     1036988 |

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
- `["sum", "random"]`
- `["sum", "random", "reduce"]`
- `["sum", "uniform"]`
- `["sum", "uniform", "reduce"]`
- `["sum", "valley"]`
- `["sum", "valley", "reduce"]`
- `["words"]`

## Julia versioninfo
```
Julia Version 1.5.3
Commit 788b2c77c1 (2020-11-09 13:37 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 20.04.2 LTS
  uname: Linux 5.4.0-1040-azure #42-Ubuntu SMP Fri Feb 5 15:39:06 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz      75484 s         16 s       2687 s      24414 s          0 s
       #2  2095 MHz      75454 s          6 s       3032 s      23780 s          0 s
       
  Memory: 6.7913818359375 GB (3752.3359375 MB free)
  Uptime: 1039.0 sec
  Load Avg:  1.642578125  1.53271484375  1.099609375
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
    CPU MHz:                         2095.175
    BogoMIPS:                        4190.35
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
|                    | No Hyperthreading detected                              |
| Clock Frequencies  | Not supported by CPU                                    |
| Data Cache         | Level 1:3 : (32, 1024, 36608) kbytes                    |
|                    | 64 byte cache line size                                 |
| Address Size       | 48 bits virtual, 46 bits physical                       |
| SIMD               | 512 bit = 64 byte max. SIMD vector size                 |
| Time Stamp Counter | TSC is accessible via `rdtsc`                           |
|                    | TSC increased at every clock cycle (non-invariant TSC)  |
| Perf. Monitoring   | Performance Monitoring Counters (PMC) are not supported |
| Hypervisor         | Yes, Microsoft                                          |

