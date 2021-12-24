# Multi-thread benchmark result

* Pull request commit: [`316f3131b3d537421a2a63b1818a6a385e3c9f65`](https://github.com/JuliaFolds/Transducers.jl/commit/316f3131b3d537421a2a63b1818a6a385e3c9f65)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/501> (Test with Julia 1.7)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 24 Dec 2021 - 04:10
    - Baseline: 24 Dec 2021 - 04:15
* Package commits:
    - Target: e45d48
    - Baseline: ed4189
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
| `["collect", "unordered", "basesize=1024"]`         |                1.07 (5%) :x: |                1.01 (1%) :x: |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` |                   0.96 (5%)  |                1.08 (1%) :x: |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` |                   0.98 (5%)  | 0.98 (1%) :white_check_mark: |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  |                1.07 (5%) :x: |                1.06 (1%) :x: |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  |                   1.05 (5%)  |                1.04 (1%) :x: |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  |                   1.00 (5%)  |                1.03 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |                1.25 (5%) :x: |                1.18 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 0.94 (5%) :white_check_mark: | 0.93 (1%) :white_check_mark: |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 0.33 (5%) :white_check_mark: | 0.52 (1%) :white_check_mark: |
| `["parallel_histogram", "comm", "basesize=16384"]`  |                   1.03 (5%)  | 0.85 (1%) :white_check_mark: |
| `["parallel_histogram", "comm", "basesize=4096"]`   |                1.07 (5%) :x: | 0.99 (1%) :white_check_mark: |
| `["parallel_histogram", "comm", "basesize=8192"]`   |                1.07 (5%) :x: |                   1.00 (1%)  |
| `["partition_length_maximum", "rand", "reduce"]`    |                   1.00 (5%)  | 0.99 (1%) :white_check_mark: |
| `["splitby", "count", "reduce"]`                    |                1.05 (5%) :x: |                1.03 (1%) :x: |
| `["words", "nthreads=1"]`                           |                   0.99 (5%)  |                1.01 (1%) :x: |
| `["words", "nthreads=2"]`                           | 0.92 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["words", "nthreads=4"]`                           | 0.91 (5%) :white_check_mark: |                   1.00 (1%)  |

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
      Ubuntu 20.04.3 LTS
  uname: Linux 5.11.0-1022-azure #23~20.04.1-Ubuntu SMP Fri Nov 19 10:20:52 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2593 MHz      56170 s          9 s       2413 s      23360 s          0 s
       #2  2593 MHz      52734 s         16 s       2528 s      26588 s          0 s
       
  Memory: 6.788982391357422 GB (3229.671875 MB free)
  Uptime: 826.0 sec
  Load Avg:  1.59423828125  1.5107421875  0.94677734375
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
      Ubuntu 20.04.3 LTS
  uname: Linux 5.11.0-1022-azure #23~20.04.1-Ubuntu SMP Fri Nov 19 10:20:52 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2593 MHz      76352 s          9 s       2932 s      33918 s          0 s
       #2  2593 MHz      80448 s         16 s       3030 s      29704 s          0 s
       
  Memory: 6.788982391357422 GB (3200.81640625 MB free)
  Uptime: 1140.0 sec
  Load Avg:  1.60302734375  1.54296875  1.12109375
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, skylake-avx512)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 24 Dec 2021 - 4:10
* Package commit: e45d48
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
| `["collect", "assoc", "basesize=1"]`                | 239.106 ms (5%) |         |  32.66 MiB (1%) |      286743 |
| `["collect", "assoc", "basesize=1024"]`             | 198.290 ms (5%) |         |   1.79 MiB (1%) |         570 |
| `["collect", "assoc", "basesize=32"]`               | 200.378 ms (5%) |         |   3.97 MiB (1%) |       13306 |
| `["collect", "seq"]`                                | 394.965 ms (5%) |         | 512.72 KiB (1%) |          15 |
| `["collect", "unordered", "basesize=1"]`            | 428.213 ms (5%) |         |  30.01 MiB (1%) |      360582 |
| `["collect", "unordered", "basesize=1024"]`         | 249.602 ms (5%) |         | 820.30 KiB (1%) |        2989 |
| `["collect", "unordered", "basesize=32"]`           | 223.847 ms (5%) |         |   1.47 MiB (1%) |       12530 |
| `["findfirst", "n=1000", "foldl"]`                  | 626.559 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 431.160 ms (5%) |         | 924.58 KiB (1%) |       16156 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 443.527 ms (5%) |         | 485.00 KiB (1%) |        8497 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 565.659 ms (5%) |         | 322.09 KiB (1%) |        5651 |
| `["findfirst", "n=400", "foldl"]`                   | 470.138 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 265.542 ms (5%) |         |   1.15 MiB (1%) |       20768 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 259.925 ms (5%) |         | 604.66 KiB (1%) |       10660 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 277.243 ms (5%) |         | 359.64 KiB (1%) |        6340 |
| `["findfirst", "n=500", "foldl"]`                   |  81.509 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 127.430 ms (5%) |         | 610.63 KiB (1%) |       10635 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 154.500 ms (5%) |         | 377.95 KiB (1%) |        6591 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 106.505 ms (5%) |         | 199.42 KiB (1%) |        3475 |
| `["overhead", "default"]`                           |  60.501 μs (5%) |         |  47.36 KiB (1%) |         382 |
| `["overhead", "stoppable=false"]`                   |  60.801 μs (5%) |         |  47.39 KiB (1%) |         382 |
| `["overhead", "stoppable=true"]`                    | 157.102 μs (5%) |         | 139.67 KiB (1%) |        2464 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   4.007 ms (5%) |         | 730.06 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   4.627 ms (5%) |         |   1.79 MiB (1%) |         213 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   4.321 ms (5%) |         |   1.43 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  13.527 ms (5%) |         |   1.03 MiB (1%) |         439 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  21.317 ms (5%) |         |   1.04 MiB (1%) |        2223 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  17.951 ms (5%) |         |   1.25 MiB (1%) |        1180 |
| `["parallel_histogram", "seq"]`                     |   7.287 ms (5%) |         | 364.61 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  33.748 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  16.892 ms (5%) |         |   2.63 KiB (1%) |          47 |
| `["splitby", "count", "foldl"]`                     |   4.688 ms (5%) |         |   96 bytes (1%) |           4 |
| `["splitby", "count", "man"]`                       |   1.687 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    |   1.186 ms (5%) |         |   2.88 KiB (1%) |          55 |
| `["sum", "random", "foldl"]`                        |  16.058 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "random", "reduce", "basesize=128"]`       |   8.260 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "random", "reduce", "basesize=256"]`       |   8.145 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "random", "reduce", "basesize=512"]`       |   8.107 ms (5%) |         |  25.30 KiB (1%) |         252 |
| `["sum", "uniform", "foldl"]`                       |  15.560 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   7.891 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   7.803 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   7.758 ms (5%) |         |  25.25 KiB (1%) |         251 |
| `["sum", "valley", "foldl"]`                        |  15.994 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "valley", "reduce", "basesize=128"]`       |   8.223 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   8.130 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   8.082 ms (5%) |         |  25.25 KiB (1%) |         251 |
| `["words", "nthreads=1"]`                           |  22.524 ms (5%) |         |  31.97 MiB (1%) |     1041632 |
| `["words", "nthreads=2"]`                           |  14.223 ms (5%) |         |  32.32 MiB (1%) |     1041670 |
| `["words", "nthreads=4"]`                           |  14.431 ms (5%) |         |  33.04 MiB (1%) |     1041754 |

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
      Ubuntu 20.04.3 LTS
  uname: Linux 5.11.0-1022-azure #23~20.04.1-Ubuntu SMP Fri Nov 19 10:20:52 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2593 MHz      56170 s          9 s       2413 s      23360 s          0 s
       #2  2593 MHz      52734 s         16 s       2528 s      26588 s          0 s
       
  Memory: 6.788982391357422 GB (3229.671875 MB free)
  Uptime: 826.0 sec
  Load Avg:  1.59423828125  1.5107421875  0.94677734375
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, skylake-avx512)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 24 Dec 2021 - 4:15
* Package commit: ed4189
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
| `["collect", "assoc", "basesize=1"]`                | 239.363 ms (5%) |         |  32.66 MiB (1%) |      286740 |
| `["collect", "assoc", "basesize=1024"]`             | 198.367 ms (5%) |         |   1.79 MiB (1%) |         570 |
| `["collect", "assoc", "basesize=32"]`               | 200.128 ms (5%) |         |   3.97 MiB (1%) |       13306 |
| `["collect", "seq"]`                                | 395.132 ms (5%) |         | 512.72 KiB (1%) |          15 |
| `["collect", "unordered", "basesize=1"]`            | 428.548 ms (5%) |         |  30.01 MiB (1%) |      360574 |
| `["collect", "unordered", "basesize=1024"]`         | 232.862 ms (5%) |         | 809.92 KiB (1%) |        2657 |
| `["collect", "unordered", "basesize=32"]`           | 224.297 ms (5%) |         |   1.48 MiB (1%) |       12709 |
| `["findfirst", "n=1000", "foldl"]`                  | 627.668 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 447.384 ms (5%) |         | 856.64 KiB (1%) |       15024 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 444.146 ms (5%) |         | 484.97 KiB (1%) |        8496 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 574.452 ms (5%) |         | 329.02 KiB (1%) |        5775 |
| `["findfirst", "n=400", "foldl"]`                   | 470.958 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 247.176 ms (5%) |         |   1.09 MiB (1%) |       19654 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 248.566 ms (5%) |         | 583.77 KiB (1%) |       10294 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 276.720 ms (5%) |         | 348.31 KiB (1%) |        6145 |
| `["findfirst", "n=500", "foldl"]`                   |  81.640 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 102.142 ms (5%) |         | 517.83 KiB (1%) |        9006 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 163.974 ms (5%) |         | 405.52 KiB (1%) |        7070 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 323.297 ms (5%) |         | 381.77 KiB (1%) |        6690 |
| `["overhead", "default"]`                           |  60.401 μs (5%) |         |  47.36 KiB (1%) |         382 |
| `["overhead", "stoppable=false"]`                   |  61.401 μs (5%) |         |  47.39 KiB (1%) |         382 |
| `["overhead", "stoppable=true"]`                    | 160.403 μs (5%) |         | 139.67 KiB (1%) |        2464 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   3.982 ms (5%) |         | 730.06 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   4.612 ms (5%) |         |   1.79 MiB (1%) |         213 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   4.297 ms (5%) |         |   1.43 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  13.151 ms (5%) |         |   1.22 MiB (1%) |         160 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  19.925 ms (5%) |         |   1.06 MiB (1%) |        2151 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  16.748 ms (5%) |         |   1.25 MiB (1%) |        1150 |
| `["parallel_histogram", "seq"]`                     |   7.274 ms (5%) |         | 364.61 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  33.746 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  16.880 ms (5%) |         |   2.66 KiB (1%) |          48 |
| `["splitby", "count", "foldl"]`                     |   4.470 ms (5%) |         |   96 bytes (1%) |           4 |
| `["splitby", "count", "man"]`                       |   1.700 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    |   1.127 ms (5%) |         |   2.78 KiB (1%) |          52 |
| `["sum", "random", "foldl"]`                        |  15.915 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "random", "reduce", "basesize=128"]`       |   8.161 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "random", "reduce", "basesize=256"]`       |   8.069 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "random", "reduce", "basesize=512"]`       |   8.023 ms (5%) |         |  25.30 KiB (1%) |         252 |
| `["sum", "uniform", "foldl"]`                       |  15.401 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   7.967 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   7.863 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   7.808 ms (5%) |         |  25.25 KiB (1%) |         251 |
| `["sum", "valley", "foldl"]`                        |  15.966 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "valley", "reduce", "basesize=128"]`       |   8.189 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   8.104 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   8.044 ms (5%) |         |  25.25 KiB (1%) |         251 |
| `["words", "nthreads=1"]`                           |  22.829 ms (5%) |         |  31.55 MiB (1%) |     1028151 |
| `["words", "nthreads=2"]`                           |  15.380 ms (5%) |         |  32.27 MiB (1%) |     1028223 |
| `["words", "nthreads=4"]`                           |  15.806 ms (5%) |         |  32.90 MiB (1%) |     1028392 |

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
      Ubuntu 20.04.3 LTS
  uname: Linux 5.11.0-1022-azure #23~20.04.1-Ubuntu SMP Fri Nov 19 10:20:52 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2593 MHz      76352 s          9 s       2932 s      33918 s          0 s
       #2  2593 MHz      80448 s         16 s       3030 s      29704 s          0 s
       
  Memory: 6.788982391357422 GB (3200.81640625 MB free)
  Uptime: 1140.0 sec
  Load Avg:  1.60302734375  1.54296875  1.12109375
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
    CPU MHz:                         2593.906
    BogoMIPS:                        5187.81
    Hypervisor vendor:               Microsoft
    Virtualization type:             full
    L1d cache:                       64 KiB
    L1i cache:                       64 KiB
    L2 cache:                        2 MiB
    L3 cache:                        35.8 MiB
    NUMA node0 CPU(s):               0,1
    Vulnerability Itlb multihit:     KVM: Mitigation: VMX unsupported
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

