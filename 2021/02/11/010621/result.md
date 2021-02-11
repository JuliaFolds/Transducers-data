# Multi-thread benchmark result

* Pull request commit: [`b52f3e3587cfef77fb4a2470087ea21b42cf81d6`](https://github.com/JuliaFolds/Transducers.jl/commit/b52f3e3587cfef77fb4a2470087ea21b42cf81d6)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/243> (Update */Manifest.toml)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 11 Feb 2021 - 01:00
    - Baseline: 11 Feb 2021 - 01:05
* Package commits:
    - Target: 9f6232
    - Baseline: 6b0f22
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
| `["collect", "assoc", "basesize=1024"]`             | 0.93 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["collect", "unordered", "basesize=1"]`            | 0.94 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["collect", "unordered", "basesize=1024"]`         | 0.83 (5%) :white_check_mark: | 0.90 (1%) :white_check_mark: |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` |                1.24 (5%) :x: |                1.26 (1%) :x: |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 0.94 (5%) :white_check_mark: |                1.04 (1%) :x: |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` |                   1.02 (5%)  |                1.11 (1%) :x: |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 0.87 (5%) :white_check_mark: |                   0.99 (1%)  |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 0.94 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 0.91 (5%) :white_check_mark: |                1.04 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 0.52 (5%) :white_check_mark: | 0.53 (1%) :white_check_mark: |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |                1.06 (5%) :x: |                1.06 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |                1.21 (5%) :x: |                1.14 (1%) :x: |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |                   0.98 (5%)  |                1.15 (1%) :x: |
| `["parallel_histogram", "comm", "basesize=16384"]`  | 0.92 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["parallel_histogram", "comm", "basesize=4096"]`   |                   1.02 (5%)  | 0.98 (1%) :white_check_mark: |
| `["sum", "random", "foldl"]`                        | 0.92 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["sum", "random", "reduce", "basesize=128"]`       | 0.93 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["sum", "random", "reduce", "basesize=256"]`       | 0.93 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["sum", "uniform", "foldl"]`                       | 0.91 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["sum", "uniform", "reduce", "basesize=128"]`      | 0.93 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["sum", "uniform", "reduce", "basesize=256"]`      | 0.95 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["sum", "valley", "reduce", "basesize=256"]`       |                1.14 (5%) :x: |                   1.00 (1%)  |
| `["words", "nthreads=2"]`                           | 0.85 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["words", "nthreads=4"]`                           | 0.94 (5%) :white_check_mark: |                   0.99 (1%)  |

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
  CPU: Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz: 
              speed         user         nice          sys         idle          irq
       #1  2294 MHz      56657 s          0 s       2394 s      35325 s          0 s
       #2  2294 MHz      45628 s          0 s       2661 s      46374 s          0 s
       
  Memory: 6.791393280029297 GB (3740.01171875 MB free)
  Uptime: 961.0 sec
  Load Avg:  1.759765625  1.4921875  0.86328125
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, broadwell)
```

### Baseline
```
Julia Version 1.5.3
Commit 788b2c77c1 (2020-11-09 13:37 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 18.04.5 LTS
  uname: Linux 5.4.0-1039-azure #41~18.04.1-Ubuntu SMP Mon Jan 18 14:00:01 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz: 
              speed         user         nice          sys         idle          irq
       #1  2294 MHz      79804 s          0 s       3013 s      43037 s          0 s
       #2  2294 MHz      69818 s          0 s       3289 s      53033 s          0 s
       
  Memory: 6.791393280029297 GB (3731.671875 MB free)
  Uptime: 1277.0 sec
  Load Avg:  1.693359375  1.5654296875  1.078125
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, broadwell)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 11 Feb 2021 - 1:0
* Package commit: 9f6232
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

| ID                                                  | time            | GC time | memory           | allocations |
|-----------------------------------------------------|----------------:|--------:|-----------------:|------------:|
| `["collect", "assoc", "basesize=1"]`                | 231.181 ms (5%) |         |   32.66 MiB (1%) |      286768 |
| `["collect", "assoc", "basesize=1024"]`             | 174.287 ms (5%) |         |    1.79 MiB (1%) |         570 |
| `["collect", "assoc", "basesize=32"]`               | 173.569 ms (5%) |         |    3.97 MiB (1%) |       13306 |
| `["collect", "seq"]`                                | 351.958 ms (5%) |         |  512.72 KiB (1%) |          15 |
| `["collect", "unordered", "basesize=1"]`            | 432.389 ms (5%) |         |   30.01 MiB (1%) |      360597 |
| `["collect", "unordered", "basesize=1024"]`         | 238.514 ms (5%) |         |  822.92 KiB (1%) |        3073 |
| `["collect", "unordered", "basesize=32"]`           | 213.188 ms (5%) |         |    1.48 MiB (1%) |       12679 |
| `["findfirst", "n=1000", "foldl"]`                  | 544.779 ms (5%) |         |                  |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 469.418 ms (5%) |         |  982.14 KiB (1%) |       17225 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 390.164 ms (5%) |         |  484.97 KiB (1%) |        8496 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 586.103 ms (5%) |         |  352.30 KiB (1%) |        6188 |
| `["findfirst", "n=400", "foldl"]`                   | 426.804 ms (5%) |         |                  |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 216.026 ms (5%) |         |    1.12 MiB (1%) |       20217 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 226.091 ms (5%) |         |  595.61 KiB (1%) |       10510 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 261.166 ms (5%) |         |  377.86 KiB (1%) |        6660 |
| `["findfirst", "n=500", "foldl"]`                   |  68.069 ms (5%) |         |                  |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |  69.435 ms (5%) |         |  344.38 KiB (1%) |        6006 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 159.800 ms (5%) |         |  426.09 KiB (1%) |        7421 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 158.563 ms (5%) |         |  241.19 KiB (1%) |        4223 |
| `["overhead", "default"]`                           |  59.200 μs (5%) |         |   47.36 KiB (1%) |         382 |
| `["overhead", "stoppable=false"]`                   |  59.600 μs (5%) |         |   47.39 KiB (1%) |         382 |
| `["overhead", "stoppable=true"]`                    | 150.600 μs (5%) |         |  139.67 KiB (1%) |        2464 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   3.864 ms (5%) |         |  730.06 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   4.815 ms (5%) |         |    2.06 MiB (1%) |         219 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   4.296 ms (5%) |         |    1.43 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  11.873 ms (5%) |         |    1.22 MiB (1%) |         260 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  18.992 ms (5%) |         | 1023.00 KiB (1%) |         990 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  15.875 ms (5%) |         |    1.23 MiB (1%) |         583 |
| `["parallel_histogram", "seq"]`                     |   6.743 ms (5%) |         |  364.61 KiB (1%) |          24 |
| `["sum", "random", "foldl"]`                        |  12.632 ms (5%) |         |    32 bytes (1%) |           2 |
| `["sum", "random", "reduce", "basesize=128"]`       |   6.387 ms (5%) |         |  103.23 KiB (1%) |        1018 |
| `["sum", "random", "reduce", "basesize=256"]`       |   6.283 ms (5%) |         |   51.23 KiB (1%) |         506 |
| `["sum", "random", "reduce", "basesize=512"]`       |   6.448 ms (5%) |         |   25.30 KiB (1%) |         252 |
| `["sum", "uniform", "foldl"]`                       |  12.097 ms (5%) |         |    32 bytes (1%) |           2 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   6.192 ms (5%) |         |  103.23 KiB (1%) |        1018 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   6.386 ms (5%) |         |   51.23 KiB (1%) |         506 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   6.538 ms (5%) |         |   25.25 KiB (1%) |         251 |
| `["sum", "valley", "foldl"]`                        |  12.944 ms (5%) |         |    32 bytes (1%) |           2 |
| `["sum", "valley", "reduce", "basesize=128"]`       |   7.033 ms (5%) |         |  103.23 KiB (1%) |        1018 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   7.787 ms (5%) |         |   51.23 KiB (1%) |         506 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   6.514 ms (5%) |         |   25.25 KiB (1%) |         251 |
| `["words", "nthreads=1"]`                           |  23.102 ms (5%) |         |   31.65 MiB (1%) |     1030941 |
| `["words", "nthreads=2"]`                           |  14.593 ms (5%) |         |   32.36 MiB (1%) |     1031013 |
| `["words", "nthreads=4"]`                           |  14.398 ms (5%) |         |   32.81 MiB (1%) |     1031097 |

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
  CPU: Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz: 
              speed         user         nice          sys         idle          irq
       #1  2294 MHz      56657 s          0 s       2394 s      35325 s          0 s
       #2  2294 MHz      45628 s          0 s       2661 s      46374 s          0 s
       
  Memory: 6.791393280029297 GB (3740.01171875 MB free)
  Uptime: 961.0 sec
  Load Avg:  1.759765625  1.4921875  0.86328125
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, broadwell)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 11 Feb 2021 - 1:5
* Package commit: 6b0f22
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
| `["collect", "assoc", "basesize=1"]`                | 235.960 ms (5%) |         |  32.66 MiB (1%) |      286771 |
| `["collect", "assoc", "basesize=1024"]`             | 187.616 ms (5%) |         |   1.79 MiB (1%) |         570 |
| `["collect", "assoc", "basesize=32"]`               | 175.220 ms (5%) |         |   3.97 MiB (1%) |       13306 |
| `["collect", "seq"]`                                | 345.663 ms (5%) |         | 512.72 KiB (1%) |          15 |
| `["collect", "unordered", "basesize=1"]`            | 457.825 ms (5%) |         |  30.01 MiB (1%) |      360644 |
| `["collect", "unordered", "basesize=1024"]`         | 285.726 ms (5%) |         | 915.52 KiB (1%) |        6036 |
| `["collect", "unordered", "basesize=32"]`           | 209.894 ms (5%) |         |   1.47 MiB (1%) |       12628 |
| `["findfirst", "n=1000", "foldl"]`                  | 564.785 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 378.498 ms (5%) |         | 781.55 KiB (1%) |       13674 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 413.308 ms (5%) |         | 466.42 KiB (1%) |        8171 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 575.588 ms (5%) |         | 317.50 KiB (1%) |        5573 |
| `["findfirst", "n=400", "foldl"]`                   | 420.652 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 249.064 ms (5%) |         |   1.13 MiB (1%) |       20348 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 239.745 ms (5%) |         | 593.19 KiB (1%) |       10463 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 286.056 ms (5%) |         | 364.25 KiB (1%) |        6424 |
| `["findfirst", "n=500", "foldl"]`                   |  71.562 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 133.634 ms (5%) |         | 654.42 KiB (1%) |       11386 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 151.275 ms (5%) |         | 402.91 KiB (1%) |        7013 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 131.524 ms (5%) |         | 210.89 KiB (1%) |        3672 |
| `["overhead", "default"]`                           |  60.800 μs (5%) |         |  47.36 KiB (1%) |         382 |
| `["overhead", "stoppable=false"]`                   |  60.500 μs (5%) |         |  47.39 KiB (1%) |         382 |
| `["overhead", "stoppable=true"]`                    | 157.300 μs (5%) |         | 139.67 KiB (1%) |        2464 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   3.968 ms (5%) |         | 730.06 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   4.917 ms (5%) |         |   1.79 MiB (1%) |         213 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   4.173 ms (5%) |         |   1.43 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  12.841 ms (5%) |         |   1.22 MiB (1%) |         160 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  18.693 ms (5%) |         |   1.02 MiB (1%) |        1473 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  15.286 ms (5%) |         |   1.24 MiB (1%) |         732 |
| `["parallel_histogram", "seq"]`                     |   6.900 ms (5%) |         | 364.61 KiB (1%) |          24 |
| `["sum", "random", "foldl"]`                        |  13.703 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "random", "reduce", "basesize=128"]`       |   6.893 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "random", "reduce", "basesize=256"]`       |   6.763 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "random", "reduce", "basesize=512"]`       |   6.779 ms (5%) |         |  25.30 KiB (1%) |         252 |
| `["sum", "uniform", "foldl"]`                       |  13.283 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   6.653 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   6.744 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   6.415 ms (5%) |         |  25.25 KiB (1%) |         251 |
| `["sum", "valley", "foldl"]`                        |  12.956 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "valley", "reduce", "basesize=128"]`       |   7.025 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   6.816 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   6.491 ms (5%) |         |  25.25 KiB (1%) |         251 |
| `["words", "nthreads=1"]`                           |  23.843 ms (5%) |         |  31.63 MiB (1%) |     1030637 |
| `["words", "nthreads=2"]`                           |  17.097 ms (5%) |         |  32.34 MiB (1%) |     1030709 |
| `["words", "nthreads=4"]`                           |  15.389 ms (5%) |         |  32.98 MiB (1%) |     1030858 |

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
  CPU: Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz: 
              speed         user         nice          sys         idle          irq
       #1  2294 MHz      79804 s          0 s       3013 s      43037 s          0 s
       #2  2294 MHz      69818 s          0 s       3289 s      53033 s          0 s
       
  Memory: 6.791393280029297 GB (3731.671875 MB free)
  Uptime: 1277.0 sec
  Load Avg:  1.693359375  1.5654296875  1.078125
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
    Model:               79
    Model name:          Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz
    Stepping:            1
    CPU MHz:             2294.688
    BogoMIPS:            4589.37
    Hypervisor vendor:   Microsoft
    Virtualization type: full
    L1d cache:           32K
    L1i cache:           32K
    L2 cache:            256K
    L3 cache:            51200K
    NUMA node0 CPU(s):   0,1
    Flags:               fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush mmx fxsr sse sse2 ss ht syscall nx pdpe1gb rdtscp lm constant_tsc rep_good nopl xtopology cpuid pni pclmulqdq ssse3 fma cx16 pcid sse4_1 sse4_2 movbe popcnt aes xsave avx f16c rdrand hypervisor lahf_lm abm 3dnowprefetch invpcid_single pti fsgsbase bmi1 hle avx2 smep bmi2 erms invpcid rtm rdseed adx smap xsaveopt md_clear
    

| Cpu Property       | Value                                                   |
|:------------------ |:------------------------------------------------------- |
| Brand              | Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz               |
| Vendor             | :Intel                                                  |
| Architecture       | :Broadwell                                              |
| Model              | Family: 0x06, Model: 0x4f, Stepping: 0x01, Type: 0x00   |
| Cores              | 2 physical cores, 2 logical cores (on executing CPU)    |
|                    | No Hyperthreading detected                              |
| Clock Frequencies  | Not supported by CPU                                    |
| Data Cache         | Level 1:3 : (32, 256, 51200) kbytes                     |
|                    | 64 byte cache line size                                 |
| Address Size       | 48 bits virtual, 46 bits physical                       |
| SIMD               | 256 bit = 32 byte max. SIMD vector size                 |
| Time Stamp Counter | TSC is accessible via `rdtsc`                           |
|                    | TSC increased at every clock cycle (non-invariant TSC)  |
| Perf. Monitoring   | Performance Monitoring Counters (PMC) are not supported |
| Hypervisor         | Yes, Microsoft                                          |

