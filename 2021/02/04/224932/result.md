# Multi-thread benchmark result

* Pull request commit: [`d2d9583e6fc4feaaf85ad57c0a7242e8a0759519`](https://github.com/JuliaFolds/Transducers.jl/commit/d2d9583e6fc4feaaf85ad57c0a7242e8a0759519)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/455> (Remove depth-first scheduling)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 4 Feb 2021 - 22:44
    - Baseline: 4 Feb 2021 - 22:49
* Package commits:
    - Target: eb008e
    - Baseline: 6901d5
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
| `["collect", "assoc", "basesize=1"]`                | 0.84 (5%) :white_check_mark: | 0.40 (1%) :white_check_mark: |
| `["collect", "assoc", "basesize=1024"]`             |                   1.02 (5%)  | 0.98 (1%) :white_check_mark: |
| `["collect", "assoc", "basesize=32"]`               |                   1.01 (5%)  | 0.72 (1%) :white_check_mark: |
| `["collect", "seq"]`                                | 0.94 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["collect", "unordered", "basesize=1024"]`         | 0.94 (5%) :white_check_mark: | 0.98 (1%) :white_check_mark: |
| `["findfirst", "n=1000", "foldl"]`                  |                1.09 (5%) :x: |                   1.00 (1%)  |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` |                1.26 (5%) :x: |                1.39 (1%) :x: |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` |                1.51 (5%) :x: |                1.74 (1%) :x: |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` |                1.99 (5%) :x: |                2.23 (1%) :x: |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  |                1.27 (5%) :x: |                1.13 (1%) :x: |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  |                1.19 (5%) :x: |                1.18 (1%) :x: |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  |                1.20 (5%) :x: |                1.41 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |                4.46 (5%) :x: |                4.88 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |                4.60 (5%) :x: |                5.53 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |                2.90 (5%) :x: |                4.16 (1%) :x: |
| `["overhead", "default"]`                           | 0.42 (5%) :white_check_mark: | 0.34 (1%) :white_check_mark: |
| `["overhead", "stoppable=false"]`                   | 0.41 (5%) :white_check_mark: | 0.34 (1%) :white_check_mark: |
| `["overhead", "stoppable=true"]`                    | 0.50 (5%) :white_check_mark: |                   0.99 (1%)  |
| `["parallel_histogram", "comm", "basesize=4096"]`   | 0.91 (5%) :white_check_mark: | 0.88 (1%) :white_check_mark: |
| `["sum", "random", "reduce", "basesize=128"]`       | 0.93 (5%) :white_check_mark: | 0.35 (1%) :white_check_mark: |
| `["sum", "random", "reduce", "basesize=256"]`       |                   1.01 (5%)  | 0.35 (1%) :white_check_mark: |
| `["sum", "random", "reduce", "basesize=512"]`       |                   0.99 (5%)  | 0.36 (1%) :white_check_mark: |
| `["sum", "uniform", "reduce", "basesize=128"]`      |                   0.98 (5%)  | 0.35 (1%) :white_check_mark: |
| `["sum", "uniform", "reduce", "basesize=256"]`      |                   0.98 (5%)  | 0.35 (1%) :white_check_mark: |
| `["sum", "uniform", "reduce", "basesize=512"]`      |                   0.96 (5%)  | 0.36 (1%) :white_check_mark: |
| `["sum", "valley", "reduce", "basesize=128"]`       |                   0.99 (5%)  | 0.35 (1%) :white_check_mark: |
| `["sum", "valley", "reduce", "basesize=256"]`       |                   0.98 (5%)  | 0.35 (1%) :white_check_mark: |
| `["sum", "valley", "reduce", "basesize=512"]`       |                   1.01 (5%)  | 0.36 (1%) :white_check_mark: |
| `["words", "nthreads=1"]`                           | 0.94 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["words", "nthreads=2"]`                           |                1.09 (5%) :x: |                   1.01 (1%)  |
| `["words", "nthreads=4"]`                           |                1.06 (5%) :x: |                   1.00 (1%)  |

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
       #1  2095 MHz      46471 s          0 s       2443 s      30806 s          0 s
       #2  2095 MHz      51021 s          0 s       2528 s      26299 s          0 s
       
  Memory: 6.791393280029297 GB (3781.6015625 MB free)
  Uptime: 812.0 sec
  Load Avg:  1.65234375  1.5166015625  0.93115234375
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
       #1  2095 MHz      67603 s          0 s       2969 s      36924 s          0 s
       #2  2095 MHz      73309 s          0 s       3062 s      31194 s          0 s
       
  Memory: 6.791393280029297 GB (3710.359375 MB free)
  Uptime: 1090.0 sec
  Load Avg:  1.7197265625  1.57421875  1.103515625
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, skylake-avx512)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 4 Feb 2021 - 22:44
* Package commit: eb008e
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
| `["collect", "assoc", "basesize=1"]`                | 245.496 ms (5%) |         |   32.66 MiB (1%) |      286737 |
| `["collect", "assoc", "basesize=1024"]`             | 194.276 ms (5%) |         |    1.79 MiB (1%) |         570 |
| `["collect", "assoc", "basesize=32"]`               | 202.692 ms (5%) |         |    3.97 MiB (1%) |       13305 |
| `["collect", "seq"]`                                | 368.935 ms (5%) |         |  512.72 KiB (1%) |          15 |
| `["collect", "unordered", "basesize=1"]`            | 406.367 ms (5%) |         |   30.01 MiB (1%) |      360558 |
| `["collect", "unordered", "basesize=1024"]`         | 222.711 ms (5%) |         |  759.55 KiB (1%) |        1027 |
| `["collect", "unordered", "basesize=32"]`           | 218.233 ms (5%) |         |    1.47 MiB (1%) |       12575 |
| `["findfirst", "n=1000", "foldl"]`                  | 640.641 ms (5%) |         |                  |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 404.517 ms (5%) |         |  758.61 KiB (1%) |       13282 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 474.799 ms (5%) |         |  485.00 KiB (1%) |        8497 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 614.498 ms (5%) |         |  322.11 KiB (1%) |        5654 |
| `["findfirst", "n=400", "foldl"]`                   | 468.450 ms (5%) |         |                  |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 286.138 ms (5%) |         |    1.11 MiB (1%) |       20044 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 282.593 ms (5%) |         |  600.08 KiB (1%) |       10583 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 294.923 ms (5%) |         |  364.36 KiB (1%) |        6421 |
| `["findfirst", "n=500", "foldl"]`                   |  75.190 ms (5%) |         |                  |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 175.499 ms (5%) |         |  744.59 KiB (1%) |       12942 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 174.576 ms (5%) |         |  453.50 KiB (1%) |        7881 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 118.621 ms (5%) |         |  194.80 KiB (1%) |        3395 |
| `["overhead", "default"]`                           |  54.200 μs (5%) |         |   47.33 KiB (1%) |         381 |
| `["overhead", "stoppable=false"]`                   |  52.300 μs (5%) |         |   47.36 KiB (1%) |         381 |
| `["overhead", "stoppable=true"]`                    | 129.201 μs (5%) |         |  139.64 KiB (1%) |        2463 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   3.717 ms (5%) |         |  730.06 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   4.222 ms (5%) |         |    1.79 MiB (1%) |         213 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   3.976 ms (5%) |         |    1.43 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  14.123 ms (5%) |         |    1.22 MiB (1%) |         238 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  22.259 ms (5%) |         | 1018.84 KiB (1%) |         875 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  21.315 ms (5%) |         |    1.26 MiB (1%) |        1282 |
| `["parallel_histogram", "seq"]`                     |   6.828 ms (5%) |         |  364.61 KiB (1%) |          24 |
| `["sum", "random", "foldl"]`                        |  14.175 ms (5%) |         |    32 bytes (1%) |           2 |
| `["sum", "random", "reduce", "basesize=128"]`       |   6.886 ms (5%) |         |  103.23 KiB (1%) |        1018 |
| `["sum", "random", "reduce", "basesize=256"]`       |   6.956 ms (5%) |         |   51.23 KiB (1%) |         506 |
| `["sum", "random", "reduce", "basesize=512"]`       |   6.727 ms (5%) |         |   25.30 KiB (1%) |         252 |
| `["sum", "uniform", "foldl"]`                       |  13.701 ms (5%) |         |    32 bytes (1%) |           2 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   6.642 ms (5%) |         |  103.23 KiB (1%) |        1018 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   6.547 ms (5%) |         |   51.23 KiB (1%) |         506 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   6.640 ms (5%) |         |   25.25 KiB (1%) |         251 |
| `["sum", "valley", "foldl"]`                        |  13.635 ms (5%) |         |    32 bytes (1%) |           2 |
| `["sum", "valley", "reduce", "basesize=128"]`       |   6.885 ms (5%) |         |  103.23 KiB (1%) |        1018 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   6.837 ms (5%) |         |   51.23 KiB (1%) |         506 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   6.944 ms (5%) |         |   25.25 KiB (1%) |         251 |
| `["words", "nthreads=1"]`                           |  18.461 ms (5%) |         |   31.59 MiB (1%) |     1029149 |
| `["words", "nthreads=2"]`                           |  13.096 ms (5%) |         |   32.30 MiB (1%) |     1029221 |
| `["words", "nthreads=4"]`                           |  13.475 ms (5%) |         |   32.93 MiB (1%) |     1029348 |

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
       #1  2095 MHz      46471 s          0 s       2443 s      30806 s          0 s
       #2  2095 MHz      51021 s          0 s       2528 s      26299 s          0 s
       
  Memory: 6.791393280029297 GB (3781.6015625 MB free)
  Uptime: 812.0 sec
  Load Avg:  1.65234375  1.5166015625  0.93115234375
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, skylake-avx512)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 4 Feb 2021 - 22:49
* Package commit: 6901d5
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

| ID                                                  | time            | GC time  | memory           | allocations |
|-----------------------------------------------------|----------------:|---------:|-----------------:|------------:|
| `["collect", "assoc", "basesize=1"]`                | 293.177 ms (5%) | 9.522 ms |   82.15 MiB (1%) |     1368048 |
| `["collect", "assoc", "basesize=1024"]`             | 189.921 ms (5%) |          |    1.83 MiB (1%) |        1597 |
| `["collect", "assoc", "basesize=32"]`               | 201.527 ms (5%) |          |    5.47 MiB (1%) |       47069 |
| `["collect", "seq"]`                                | 390.891 ms (5%) |          |  512.72 KiB (1%) |          15 |
| `["collect", "unordered", "basesize=1"]`            | 419.097 ms (5%) |          |   30.01 MiB (1%) |      360561 |
| `["collect", "unordered", "basesize=1024"]`         | 235.857 ms (5%) |          |  775.58 KiB (1%) |        1558 |
| `["collect", "unordered", "basesize=32"]`           | 220.861 ms (5%) |          |    1.47 MiB (1%) |       12491 |
| `["findfirst", "n=1000", "foldl"]`                  | 585.979 ms (5%) |          |                  |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 322.033 ms (5%) |          |  546.38 KiB (1%) |        9563 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 314.184 ms (5%) |          |  278.25 KiB (1%) |        4888 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 308.164 ms (5%) |          |  144.66 KiB (1%) |        2550 |
| `["findfirst", "n=400", "foldl"]`                   | 457.285 ms (5%) |          |                  |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 225.891 ms (5%) |          | 1012.91 KiB (1%) |       17727 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 237.742 ms (5%) |          |  509.63 KiB (1%) |        8952 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 245.736 ms (5%) |          |  258.84 KiB (1%) |        4564 |
| `["findfirst", "n=500", "foldl"]`                   |  76.034 ms (5%) |          |                  |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |  39.385 ms (5%) |          |  152.59 KiB (1%) |        2677 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |  37.957 ms (5%) |          |   82.00 KiB (1%) |        1444 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  40.854 ms (5%) |          |   46.84 KiB (1%) |         828 |
| `["overhead", "default"]`                           | 128.601 μs (5%) |          |  140.72 KiB (1%) |        2464 |
| `["overhead", "stoppable=false"]`                   | 129.001 μs (5%) |          |  140.78 KiB (1%) |        2464 |
| `["overhead", "stoppable=true"]`                    | 260.202 μs (5%) |          |  140.81 KiB (1%) |        2466 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   3.708 ms (5%) |          |  731.81 KiB (1%) |          94 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   4.218 ms (5%) |          |    1.80 MiB (1%) |         448 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   3.974 ms (5%) |          |    1.43 MiB (1%) |         220 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  14.071 ms (5%) |          |    1.22 MiB (1%) |         254 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  24.366 ms (5%) |          |    1.13 MiB (1%) |        2185 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  20.626 ms (5%) |          |    1.26 MiB (1%) |        1258 |
| `["parallel_histogram", "seq"]`                     |   6.889 ms (5%) |          |  364.61 KiB (1%) |          24 |
| `["sum", "random", "foldl"]`                        |  13.724 ms (5%) |          |    32 bytes (1%) |           2 |
| `["sum", "random", "reduce", "basesize=128"]`       |   7.387 ms (5%) |          |  292.02 KiB (1%) |        5213 |
| `["sum", "random", "reduce", "basesize=256"]`       |   6.918 ms (5%) |          |  144.53 KiB (1%) |        2589 |
| `["sum", "random", "reduce", "basesize=512"]`       |   6.812 ms (5%) |          |   71.11 KiB (1%) |        1279 |
| `["sum", "uniform", "foldl"]`                       |  13.489 ms (5%) |          |    32 bytes (1%) |           2 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   6.790 ms (5%) |          |  292.02 KiB (1%) |        5213 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   6.676 ms (5%) |          |  144.53 KiB (1%) |        2589 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   6.940 ms (5%) |          |   71.06 KiB (1%) |        1278 |
| `["sum", "valley", "foldl"]`                        |  13.698 ms (5%) |          |    32 bytes (1%) |           2 |
| `["sum", "valley", "reduce", "basesize=128"]`       |   6.964 ms (5%) |          |  292.02 KiB (1%) |        5213 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   6.952 ms (5%) |          |  144.53 KiB (1%) |        2589 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   6.859 ms (5%) |          |   71.06 KiB (1%) |        1278 |
| `["words", "nthreads=1"]`                           |  19.553 ms (5%) |          |   31.65 MiB (1%) |     1030752 |
| `["words", "nthreads=2"]`                           |  12.029 ms (5%) |          |   32.01 MiB (1%) |     1030821 |
| `["words", "nthreads=4"]`                           |  12.746 ms (5%) |          |   32.91 MiB (1%) |     1031092 |

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
       #1  2095 MHz      67603 s          0 s       2969 s      36924 s          0 s
       #2  2095 MHz      73309 s          0 s       3062 s      31194 s          0 s
       
  Memory: 6.791393280029297 GB (3710.359375 MB free)
  Uptime: 1090.0 sec
  Load Avg:  1.7197265625  1.57421875  1.103515625
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
    CPU MHz:             2095.077
    BogoMIPS:            4190.15
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

