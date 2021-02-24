# Multi-thread benchmark result

* Pull request commit: [`c5076ce754b624934b89ee877b68097403516f05`](https://github.com/JuliaFolds/Transducers.jl/commit/c5076ce754b624934b89ee877b68097403516f05)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/243> (Update */Manifest.toml)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 24 Feb 2021 - 01:02
    - Baseline: 24 Feb 2021 - 01:07
* Package commits:
    - Target: 91e321
    - Baseline: eb0a9e
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
| `["collect", "unordered", "basesize=1"]`            | 0.95 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["collect", "unordered", "basesize=1024"]`         |                   1.01 (5%)  | 0.94 (1%) :white_check_mark: |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` |                1.11 (5%) :x: |                1.15 (1%) :x: |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` |                   0.97 (5%)  |                1.02 (1%) :x: |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 0.92 (5%) :white_check_mark: |                   0.99 (1%)  |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  |                   0.98 (5%)  |                1.02 (1%) :x: |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  |                   1.00 (5%)  | 0.97 (1%) :white_check_mark: |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 0.82 (5%) :white_check_mark: | 0.93 (1%) :white_check_mark: |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 0.88 (5%) :white_check_mark: | 0.87 (1%) :white_check_mark: |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |                1.86 (5%) :x: |                1.59 (1%) :x: |
| `["parallel_histogram", "comm", "basesize=4096"]`   |                   1.03 (5%)  |                1.01 (1%) :x: |
| `["words", "nthreads=2"]`                           |                1.10 (5%) :x: |                   1.01 (1%)  |
| `["words", "nthreads=4"]`                           |                1.13 (5%) :x: |                   1.01 (1%)  |

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
      Ubuntu 18.04.5 LTS
  uname: Linux 5.4.0-1039-azure #41~18.04.1-Ubuntu SMP Mon Jan 18 14:00:01 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz      53367 s          0 s       2294 s      14317 s          0 s
       #2  2095 MHz      47815 s          0 s       2695 s      20320 s          0 s
       
  Memory: 6.791389465332031 GB (3791.3125 MB free)
  Uptime: 721.0 sec
  Load Avg:  1.66796875  1.47802734375  0.892578125
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
      Ubuntu 18.04.5 LTS
  uname: Linux 5.4.0-1039-azure #41~18.04.1-Ubuntu SMP Mon Jan 18 14:00:01 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz      78608 s          0 s       2842 s      19798 s          0 s
       #2  2095 MHz      69607 s          0 s       3301 s      29218 s          0 s
       
  Memory: 6.791389465332031 GB (3774.99609375 MB free)
  Uptime: 1035.0 sec
  Load Avg:  1.68798828125  1.576171875  1.10302734375
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, skylake-avx512)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 24 Feb 2021 - 1:2
* Package commit: 91e321
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

| ID                                                  | time            | GC time   | memory          | allocations |
|-----------------------------------------------------|----------------:|----------:|----------------:|------------:|
| `["collect", "assoc", "basesize=1"]`                | 286.290 ms (5%) |           |  32.66 MiB (1%) |      286749 |
| `["collect", "assoc", "basesize=1024"]`             | 252.910 ms (5%) |           |   1.79 MiB (1%) |         570 |
| `["collect", "assoc", "basesize=32"]`               | 243.400 ms (5%) |           |   3.97 MiB (1%) |       13306 |
| `["collect", "seq"]`                                | 474.764 ms (5%) |           | 512.72 KiB (1%) |          15 |
| `["collect", "unordered", "basesize=1"]`            | 470.410 ms (5%) | 16.607 ms |  30.02 MiB (1%) |      360817 |
| `["collect", "unordered", "basesize=1024"]`         | 302.724 ms (5%) |           | 780.64 KiB (1%) |        1720 |
| `["collect", "unordered", "basesize=32"]`           | 266.707 ms (5%) |           |   1.47 MiB (1%) |       12419 |
| `["findfirst", "n=1000", "foldl"]`                  | 750.332 ms (5%) |           |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 854.755 ms (5%) |           |   1.25 MiB (1%) |       22497 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 510.755 ms (5%) |           | 466.42 KiB (1%) |        8171 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 716.097 ms (5%) |           | 329.00 KiB (1%) |        5775 |
| `["findfirst", "n=400", "foldl"]`                   | 575.019 ms (5%) |           |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 296.555 ms (5%) |           |   1.07 MiB (1%) |       19350 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 307.777 ms (5%) |           | 602.45 KiB (1%) |       10627 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 342.688 ms (5%) |           | 364.36 KiB (1%) |        6421 |
| `["findfirst", "n=500", "foldl"]`                   |  97.576 ms (5%) |           |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 202.063 ms (5%) |           | 800.52 KiB (1%) |       13926 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 182.802 ms (5%) |           | 366.27 KiB (1%) |        6385 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 254.556 ms (5%) |           | 295.98 KiB (1%) |        5164 |
| `["overhead", "default"]`                           |  67.104 μs (5%) |           |  47.33 KiB (1%) |         381 |
| `["overhead", "stoppable=false"]`                   |  68.504 μs (5%) |           |  47.36 KiB (1%) |         381 |
| `["overhead", "stoppable=true"]`                    | 174.211 μs (5%) |           | 139.67 KiB (1%) |        2464 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   5.391 ms (5%) |           | 730.06 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   6.094 ms (5%) |           |   1.79 MiB (1%) |         213 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   5.742 ms (5%) |           |   1.43 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  16.374 ms (5%) |           |   1.23 MiB (1%) |         400 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  24.889 ms (5%) |           |   1.04 MiB (1%) |        1395 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  21.424 ms (5%) |           |   1.25 MiB (1%) |        1186 |
| `["parallel_histogram", "seq"]`                     |   9.835 ms (5%) |           | 364.61 KiB (1%) |          24 |
| `["sum", "random", "foldl"]`                        |  19.123 ms (5%) |           |   32 bytes (1%) |           2 |
| `["sum", "random", "reduce", "basesize=128"]`       |   9.600 ms (5%) |           | 103.23 KiB (1%) |        1018 |
| `["sum", "random", "reduce", "basesize=256"]`       |   9.668 ms (5%) |           |  51.23 KiB (1%) |         506 |
| `["sum", "random", "reduce", "basesize=512"]`       |   9.654 ms (5%) |           |  25.30 KiB (1%) |         252 |
| `["sum", "uniform", "foldl"]`                       |  18.495 ms (5%) |           |   32 bytes (1%) |           2 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   9.504 ms (5%) |           | 103.23 KiB (1%) |        1018 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   9.413 ms (5%) |           |  51.23 KiB (1%) |         506 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   9.323 ms (5%) |           |  25.25 KiB (1%) |         251 |
| `["sum", "valley", "foldl"]`                        |  19.238 ms (5%) |           |   32 bytes (1%) |           2 |
| `["sum", "valley", "reduce", "basesize=128"]`       |   9.950 ms (5%) |           | 103.23 KiB (1%) |        1018 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   9.846 ms (5%) |           |  51.23 KiB (1%) |         506 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   9.757 ms (5%) |           |  25.25 KiB (1%) |         251 |
| `["words", "nthreads=1"]`                           |  26.088 ms (5%) |           |  31.83 MiB (1%) |     1037178 |
| `["words", "nthreads=2"]`                           |  18.339 ms (5%) |           |  32.18 MiB (1%) |     1037214 |
| `["words", "nthreads=4"]`                           |  18.889 ms (5%) |           |  33.08 MiB (1%) |     1037366 |

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
      Ubuntu 18.04.5 LTS
  uname: Linux 5.4.0-1039-azure #41~18.04.1-Ubuntu SMP Mon Jan 18 14:00:01 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz      53367 s          0 s       2294 s      14317 s          0 s
       #2  2095 MHz      47815 s          0 s       2695 s      20320 s          0 s
       
  Memory: 6.791389465332031 GB (3791.3125 MB free)
  Uptime: 721.0 sec
  Load Avg:  1.66796875  1.47802734375  0.892578125
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, skylake-avx512)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 24 Feb 2021 - 1:7
* Package commit: eb0a9e
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
| `["collect", "assoc", "basesize=1"]`                | 286.976 ms (5%) |         |  32.66 MiB (1%) |      286741 |
| `["collect", "assoc", "basesize=1024"]`             | 246.181 ms (5%) |         |   1.79 MiB (1%) |         570 |
| `["collect", "assoc", "basesize=32"]`               | 244.990 ms (5%) |         |   3.97 MiB (1%) |       13306 |
| `["collect", "seq"]`                                | 474.397 ms (5%) |         | 512.72 KiB (1%) |          15 |
| `["collect", "unordered", "basesize=1"]`            | 496.752 ms (5%) |         |  30.01 MiB (1%) |      360642 |
| `["collect", "unordered", "basesize=1024"]`         | 298.885 ms (5%) |         | 827.64 KiB (1%) |        3224 |
| `["collect", "unordered", "basesize=32"]`           | 275.540 ms (5%) |         |   1.46 MiB (1%) |       12124 |
| `["findfirst", "n=1000", "foldl"]`                  | 750.800 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 768.226 ms (5%) |         |   1.08 MiB (1%) |       19492 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 527.871 ms (5%) |         | 457.25 KiB (1%) |        8012 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 719.683 ms (5%) |         | 329.02 KiB (1%) |        5775 |
| `["findfirst", "n=400", "foldl"]`                   | 563.066 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 321.103 ms (5%) |         |   1.08 MiB (1%) |       19506 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 315.379 ms (5%) |         | 588.58 KiB (1%) |       10383 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 341.425 ms (5%) |         | 375.63 KiB (1%) |        6616 |
| `["findfirst", "n=500", "foldl"]`                   |  97.475 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 246.379 ms (5%) |         | 864.64 KiB (1%) |       15106 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 208.529 ms (5%) |         | 421.70 KiB (1%) |        7356 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 137.162 ms (5%) |         | 185.73 KiB (1%) |        3242 |
| `["overhead", "default"]`                           |  66.703 μs (5%) |         |  47.33 KiB (1%) |         381 |
| `["overhead", "stoppable=false"]`                   |  67.103 μs (5%) |         |  47.36 KiB (1%) |         381 |
| `["overhead", "stoppable=true"]`                    | 173.708 μs (5%) |         | 139.67 KiB (1%) |        2464 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   5.384 ms (5%) |         | 730.06 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   6.126 ms (5%) |         |   1.79 MiB (1%) |         213 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   5.733 ms (5%) |         |   1.43 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  16.183 ms (5%) |         |   1.22 MiB (1%) |         234 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  24.153 ms (5%) |         |   1.02 MiB (1%) |        1411 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  21.242 ms (5%) |         |   1.25 MiB (1%) |        1066 |
| `["parallel_histogram", "seq"]`                     |   9.852 ms (5%) |         | 364.61 KiB (1%) |          24 |
| `["sum", "random", "foldl"]`                        |  19.060 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "random", "reduce", "basesize=128"]`       |   9.834 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "random", "reduce", "basesize=256"]`       |   9.721 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "random", "reduce", "basesize=512"]`       |   9.631 ms (5%) |         |  25.30 KiB (1%) |         252 |
| `["sum", "uniform", "foldl"]`                       |  18.490 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   9.512 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   9.413 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   9.346 ms (5%) |         |  25.25 KiB (1%) |         251 |
| `["sum", "valley", "foldl"]`                        |  19.290 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "valley", "reduce", "basesize=128"]`       |   9.909 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   9.785 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   9.762 ms (5%) |         |  25.25 KiB (1%) |         251 |
| `["words", "nthreads=1"]`                           |  26.539 ms (5%) |         |  31.62 MiB (1%) |     1029830 |
| `["words", "nthreads=2"]`                           |  16.603 ms (5%) |         |  31.97 MiB (1%) |     1029866 |
| `["words", "nthreads=4"]`                           |  16.775 ms (5%) |         |  32.87 MiB (1%) |     1030027 |

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
      Ubuntu 18.04.5 LTS
  uname: Linux 5.4.0-1039-azure #41~18.04.1-Ubuntu SMP Mon Jan 18 14:00:01 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz      78608 s          0 s       2842 s      19798 s          0 s
       #2  2095 MHz      69607 s          0 s       3301 s      29218 s          0 s
       
  Memory: 6.791389465332031 GB (3774.99609375 MB free)
  Uptime: 1035.0 sec
  Load Avg:  1.68798828125  1.576171875  1.10302734375
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

    Architecture:        x86_64
    CPU op-mode(s):      32-bit, 64-bit
    Byte Order:          Little Endian
    CPU(s):              2
    On-line CPU(s) list: 0,1
    Thread(s) per core:  1
    Core(s) per socket:  2
    Socket(s):           1
    NUMA node(s):        1
    Vendor ID:           GenuineIntel
    CPU family:          6
    Model:               85
    Model name:          Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz
    Stepping:            4
    CPU MHz:             2095.209
    BogoMIPS:            4190.41
    Hypervisor vendor:   Microsoft
    Virtualization type: full
    L1d cache:           32K
    L1i cache:           32K
    L2 cache:            1024K
    L3 cache:            36608K
    NUMA node0 CPU(s):   0,1
    Flags:               fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush mmx fxsr sse sse2 ss ht syscall nx pdpe1gb rdtscp lm constant_tsc rep_good nopl xtopology cpuid pni pclmulqdq ssse3 fma cx16 pcid sse4_1 sse4_2 movbe popcnt aes xsave avx f16c rdrand hypervisor lahf_lm abm 3dnowprefetch invpcid_single pti fsgsbase bmi1 hle avx2 smep bmi2 erms invpcid rtm mpx avx512f avx512dq rdseed adx smap clflushopt avx512cd avx512bw avx512vl xsaveopt xsavec xsaves md_clear
    

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

