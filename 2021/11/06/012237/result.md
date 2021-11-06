# Multi-thread benchmark result

* Pull request commit: [`18a10373f35bf2995afe1890e435de585a9aeb33`](https://github.com/JuliaFolds/Transducers.jl/commit/18a10373f35bf2995afe1890e435de585a9aeb33)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/243> (Update */Manifest.toml)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 6 Nov 2021 - 01:16
    - Baseline: 6 Nov 2021 - 01:22
* Package commits:
    - Target: b6b5f1
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
| `["collect", "unordered", "basesize=1024"]`         |                   0.97 (5%)  | 0.96 (1%) :white_check_mark: |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 0.91 (5%) :white_check_mark: | 0.85 (1%) :white_check_mark: |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` |                1.31 (5%) :x: |                1.27 (1%) :x: |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  |                   1.02 (5%)  |                1.03 (1%) :x: |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  |                1.33 (5%) :x: | 0.97 (1%) :white_check_mark: |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 0.95 (5%) :white_check_mark: | 0.95 (1%) :white_check_mark: |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |                1.45 (5%) :x: |                1.50 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 0.82 (5%) :white_check_mark: | 0.85 (1%) :white_check_mark: |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |                1.12 (5%) :x: |                   1.00 (1%)  |
| `["parallel_histogram", "comm", "basesize=4096"]`   | 0.92 (5%) :white_check_mark: |                1.02 (1%) :x: |
| `["parallel_histogram", "comm", "basesize=8192"]`   |                   1.05 (5%)  |                1.01 (1%) :x: |
| `["partition_length_maximum", "rand", "reduce"]`    |                   1.00 (5%)  |                1.01 (1%) :x: |
| `["splitby", "count", "man"]`                       | 0.86 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["words", "nthreads=4"]`                           | 0.85 (5%) :white_check_mark: |                   1.00 (1%)  |

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
  uname: Linux 5.11.0-1020-azure #21~20.04.1-Ubuntu SMP Mon Oct 11 18:54:28 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2593 MHz      52693 s         13 s       2510 s      47158 s          0 s
       #2  2593 MHz      55215 s          6 s       2340 s      45246 s          0 s
       
  Memory: 6.788990020751953 GB (3384.78125 MB free)
  Uptime: 1032.0 sec
  Load Avg:  1.6005859375  1.47412109375  0.90380859375
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
  uname: Linux 5.11.0-1020-azure #21~20.04.1-Ubuntu SMP Mon Oct 11 18:54:28 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2593 MHz      80401 s         13 s       3189 s      53008 s          0 s
       #2  2593 MHz      78717 s          6 s       2968 s      55446 s          0 s
       
  Memory: 6.788990020751953 GB (3166.7578125 MB free)
  Uptime: 1377.0 sec
  Load Avg:  1.6171875  1.5693359375  1.1259765625
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, skylake-avx512)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 6 Nov 2021 - 1:16
* Package commit: b6b5f1
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

| ID                                                  | time            | GC time | memory           | allocations |
|-----------------------------------------------------|----------------:|--------:|-----------------:|------------:|
| `["collect", "assoc", "basesize=1"]`                | 241.350 ms (5%) |         |   32.66 MiB (1%) |      286743 |
| `["collect", "assoc", "basesize=1024"]`             | 198.322 ms (5%) |         |    1.79 MiB (1%) |         570 |
| `["collect", "assoc", "basesize=32"]`               | 200.727 ms (5%) |         |    3.97 MiB (1%) |       13306 |
| `["collect", "seq"]`                                | 394.972 ms (5%) |         |  512.72 KiB (1%) |          15 |
| `["collect", "unordered", "basesize=1"]`            | 428.947 ms (5%) |         |   30.01 MiB (1%) |      360569 |
| `["collect", "unordered", "basesize=1024"]`         | 253.828 ms (5%) |         |  830.20 KiB (1%) |        3288 |
| `["collect", "unordered", "basesize=32"]`           | 225.852 ms (5%) |         |    1.48 MiB (1%) |       12762 |
| `["findfirst", "n=1000", "foldl"]`                  | 624.293 ms (5%) |         |                  |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 477.217 ms (5%) |         |  887.77 KiB (1%) |       15595 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 442.925 ms (5%) |         |  484.97 KiB (1%) |        8496 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 693.166 ms (5%) |         |  393.55 KiB (1%) |        6908 |
| `["findfirst", "n=400", "foldl"]`                   | 469.351 ms (5%) |         |                  |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 250.694 ms (5%) |         |    1.09 MiB (1%) |       19631 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 343.299 ms (5%) |         |  581.38 KiB (1%) |       10248 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 270.287 ms (5%) |         |  357.45 KiB (1%) |        6302 |
| `["findfirst", "n=500", "foldl"]`                   |  81.187 ms (5%) |         |                  |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 211.444 ms (5%) |         | 1001.39 KiB (1%) |       17414 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 134.633 ms (5%) |         |  345.47 KiB (1%) |        6022 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 231.906 ms (5%) |         |  296.34 KiB (1%) |        5187 |
| `["overhead", "default"]`                           |  61.101 μs (5%) |         |   47.36 KiB (1%) |         382 |
| `["overhead", "stoppable=false"]`                   |  61.801 μs (5%) |         |   47.39 KiB (1%) |         382 |
| `["overhead", "stoppable=true"]`                    | 158.403 μs (5%) |         |  139.67 KiB (1%) |        2464 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   4.003 ms (5%) |         |  730.06 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   4.620 ms (5%) |         |    1.79 MiB (1%) |         213 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   4.314 ms (5%) |         |    1.43 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  13.285 ms (5%) |         |    1.23 MiB (1%) |         413 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  21.082 ms (5%) |         |    1.06 MiB (1%) |        2784 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  19.396 ms (5%) |         |    1.26 MiB (1%) |        1502 |
| `["parallel_histogram", "seq"]`                     |   7.286 ms (5%) |         |  364.61 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  33.768 ms (5%) |         |                  |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  16.916 ms (5%) |         |    2.66 KiB (1%) |          48 |
| `["splitby", "count", "foldl"]`                     |   4.698 ms (5%) |         |    96 bytes (1%) |           4 |
| `["splitby", "count", "man"]`                       |   1.660 ms (5%) |         |                  |             |
| `["splitby", "count", "reduce"]`                    |   1.187 ms (5%) |         |    2.80 KiB (1%) |          54 |
| `["sum", "random", "foldl"]`                        |  15.968 ms (5%) |         |    32 bytes (1%) |           2 |
| `["sum", "random", "reduce", "basesize=128"]`       |   8.179 ms (5%) |         |  103.23 KiB (1%) |        1018 |
| `["sum", "random", "reduce", "basesize=256"]`       |   8.100 ms (5%) |         |   51.23 KiB (1%) |         506 |
| `["sum", "random", "reduce", "basesize=512"]`       |   8.020 ms (5%) |         |   25.30 KiB (1%) |         252 |
| `["sum", "uniform", "foldl"]`                       |  15.413 ms (5%) |         |    32 bytes (1%) |           2 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   7.923 ms (5%) |         |  103.23 KiB (1%) |        1018 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   7.810 ms (5%) |         |   51.23 KiB (1%) |         506 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   7.759 ms (5%) |         |   25.25 KiB (1%) |         251 |
| `["sum", "valley", "foldl"]`                        |  16.054 ms (5%) |         |    32 bytes (1%) |           2 |
| `["sum", "valley", "reduce", "basesize=128"]`       |   8.236 ms (5%) |         |  103.23 KiB (1%) |        1018 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   8.132 ms (5%) |         |   51.23 KiB (1%) |         506 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   8.107 ms (5%) |         |   25.25 KiB (1%) |         251 |
| `["words", "nthreads=1"]`                           |  23.723 ms (5%) |         |   31.46 MiB (1%) |     1024837 |
| `["words", "nthreads=2"]`                           |  14.979 ms (5%) |         |   32.18 MiB (1%) |     1024919 |
| `["words", "nthreads=4"]`                           |  15.003 ms (5%) |         |   32.81 MiB (1%) |     1025059 |

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
  uname: Linux 5.11.0-1020-azure #21~20.04.1-Ubuntu SMP Mon Oct 11 18:54:28 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2593 MHz      52693 s         13 s       2510 s      47158 s          0 s
       #2  2593 MHz      55215 s          6 s       2340 s      45246 s          0 s
       
  Memory: 6.788990020751953 GB (3384.78125 MB free)
  Uptime: 1032.0 sec
  Load Avg:  1.6005859375  1.47412109375  0.90380859375
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, skylake-avx512)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 6 Nov 2021 - 1:22
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

| ID                                                  | time            | GC time  | memory          | allocations |
|-----------------------------------------------------|----------------:|---------:|----------------:|------------:|
| `["collect", "assoc", "basesize=1"]`                | 240.646 ms (5%) |          |  32.66 MiB (1%) |      286744 |
| `["collect", "assoc", "basesize=1024"]`             | 199.081 ms (5%) |          |   1.79 MiB (1%) |         570 |
| `["collect", "assoc", "basesize=32"]`               | 200.966 ms (5%) |          |   3.97 MiB (1%) |       13305 |
| `["collect", "seq"]`                                | 394.992 ms (5%) |          | 512.72 KiB (1%) |          15 |
| `["collect", "unordered", "basesize=1"]`            | 427.069 ms (5%) |          |  30.01 MiB (1%) |      360588 |
| `["collect", "unordered", "basesize=1024"]`         | 262.856 ms (5%) |          | 861.42 KiB (1%) |        4305 |
| `["collect", "unordered", "basesize=32"]`           | 224.748 ms (5%) |          |   1.47 MiB (1%) |       12642 |
| `["findfirst", "n=1000", "foldl"]`                  | 628.333 ms (5%) |          |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 523.387 ms (5%) |          |   1.02 MiB (1%) |       18246 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 444.573 ms (5%) |          | 484.97 KiB (1%) |        8496 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 527.969 ms (5%) |          | 310.50 KiB (1%) |        5448 |
| `["findfirst", "n=400", "foldl"]`                   | 471.427 ms (5%) |          |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 246.292 ms (5%) |          |   1.06 MiB (1%) |       19032 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 258.943 ms (5%) |          | 597.81 KiB (1%) |       10543 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 285.641 ms (5%) |          | 375.63 KiB (1%) |        6616 |
| `["findfirst", "n=500", "foldl"]`                   |  81.736 ms (5%) |          |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 145.875 ms (5%) |          | 668.88 KiB (1%) |       11649 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 164.586 ms (5%) |          | 405.48 KiB (1%) |        7069 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 207.865 ms (5%) |          | 295.94 KiB (1%) |        5161 |
| `["overhead", "default"]`                           |  61.100 μs (5%) |          |  47.36 KiB (1%) |         382 |
| `["overhead", "stoppable=false"]`                   |  61.101 μs (5%) |          |  47.39 KiB (1%) |         382 |
| `["overhead", "stoppable=true"]`                    | 159.102 μs (5%) |          | 139.67 KiB (1%) |        2464 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   3.982 ms (5%) |          | 730.06 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   4.596 ms (5%) |          |   1.79 MiB (1%) |         213 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   4.300 ms (5%) |          |   1.43 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  13.330 ms (5%) |          |   1.22 MiB (1%) |         160 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  22.942 ms (5%) |          |   1.04 MiB (1%) |        2310 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  18.543 ms (5%) | 3.082 ms |   1.25 MiB (1%) |         956 |
| `["parallel_histogram", "seq"]`                     |   7.248 ms (5%) |          | 364.61 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  33.759 ms (5%) |          |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  16.900 ms (5%) |          |   2.63 KiB (1%) |          47 |
| `["splitby", "count", "foldl"]`                     |   4.783 ms (5%) |          |   96 bytes (1%) |           4 |
| `["splitby", "count", "man"]`                       |   1.928 ms (5%) |          |                 |             |
| `["splitby", "count", "reduce"]`                    |   1.219 ms (5%) |          |   2.81 KiB (1%) |          54 |
| `["sum", "random", "foldl"]`                        |  15.919 ms (5%) |          |   32 bytes (1%) |           2 |
| `["sum", "random", "reduce", "basesize=128"]`       |   8.201 ms (5%) |          | 103.23 KiB (1%) |        1018 |
| `["sum", "random", "reduce", "basesize=256"]`       |   8.077 ms (5%) |          |  51.23 KiB (1%) |         506 |
| `["sum", "random", "reduce", "basesize=512"]`       |   8.013 ms (5%) |          |  25.30 KiB (1%) |         252 |
| `["sum", "uniform", "foldl"]`                       |  15.481 ms (5%) |          |   32 bytes (1%) |           2 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   7.966 ms (5%) |          | 103.23 KiB (1%) |        1018 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   7.866 ms (5%) |          |  51.23 KiB (1%) |         506 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   7.809 ms (5%) |          |  25.25 KiB (1%) |         251 |
| `["sum", "valley", "foldl"]`                        |  15.973 ms (5%) |          |   32 bytes (1%) |           2 |
| `["sum", "valley", "reduce", "basesize=128"]`       |   8.199 ms (5%) |          | 103.23 KiB (1%) |        1018 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   8.116 ms (5%) |          |  51.23 KiB (1%) |         506 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   8.060 ms (5%) |          |  25.25 KiB (1%) |         251 |
| `["words", "nthreads=1"]`                           |  24.000 ms (5%) |          |  31.56 MiB (1%) |     1028263 |
| `["words", "nthreads=2"]`                           |  14.839 ms (5%) |          |  32.27 MiB (1%) |     1028345 |
| `["words", "nthreads=4"]`                           |  17.710 ms (5%) |          |  32.72 MiB (1%) |     1028420 |

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
  uname: Linux 5.11.0-1020-azure #21~20.04.1-Ubuntu SMP Mon Oct 11 18:54:28 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2593 MHz      80401 s         13 s       3189 s      53008 s          0 s
       #2  2593 MHz      78717 s          6 s       2968 s      55446 s          0 s
       
  Memory: 6.788990020751953 GB (3166.7578125 MB free)
  Uptime: 1377.0 sec
  Load Avg:  1.6171875  1.5693359375  1.1259765625
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
    CPU MHz:                         2593.908
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

