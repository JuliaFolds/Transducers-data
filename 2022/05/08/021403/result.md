# Multi-thread benchmark result

* Pull request commit: [`77a83c2ecce0600db55f5ccd6956d14b97bc4260`](https://github.com/JuliaFolds/Transducers.jl/commit/77a83c2ecce0600db55f5ccd6956d14b97bc4260)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/243> (Update */Manifest.toml)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 8 May 2022 - 02:08
    - Baseline: 8 May 2022 - 02:13
* Package commits:
    - Target: 7f3ffe
    - Baseline: 6125fe
* Julia commits:
    - Target: bf5349
    - Baseline: bf5349
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
| `["collect", "unordered", "basesize=1024"]`         |                   1.00 (5%)  |                1.03 (1%) :x: |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 0.91 (5%) :white_check_mark: | 0.87 (1%) :white_check_mark: |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 0.85 (5%) :white_check_mark: | 0.88 (1%) :white_check_mark: |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 0.91 (5%) :white_check_mark: | 0.97 (1%) :white_check_mark: |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 0.92 (5%) :white_check_mark: | 0.92 (1%) :white_check_mark: |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |                1.39 (5%) :x: |                1.37 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |                1.54 (5%) :x: |                1.40 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 0.45 (5%) :white_check_mark: | 0.63 (1%) :white_check_mark: |
| `["overhead", "stoppable=false"]`                   |                1.06 (5%) :x: |                   1.00 (1%)  |
| `["overhead", "stoppable=true"]`                    |                1.06 (5%) :x: |                   1.00 (1%)  |
| `["parallel_histogram", "comm", "basesize=16384"]`  |                1.05 (5%) :x: |                1.01 (1%) :x: |
| `["parallel_histogram", "comm", "basesize=4096"]`   |                   1.02 (5%)  |                1.04 (1%) :x: |
| `["parallel_histogram", "comm", "basesize=8192"]`   |                1.05 (5%) :x: |                   1.00 (1%)  |
| `["splitby", "count", "man"]`                       |                1.07 (5%) :x: |                   1.00 (1%)  |
| `["splitby", "count", "reduce"]`                    |                1.07 (5%) :x: |                   1.00 (1%)  |
| `["words", "nthreads=4"]`                           |                1.06 (5%) :x: |                   1.01 (1%)  |

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
Julia Version 1.7.2
Commit bf53498635 (2022-02-06 15:21 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 20.04.4 LTS
  uname: Linux 5.13.0-1022-azure #26~20.04.1-Ubuntu SMP Thu Apr 7 19:42:45 UTC 2022 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz       4856 s          2 s        237 s       3134 s          0 s
       #2  2095 MHz       5736 s          1 s        258 s       2249 s          0 s
       
  Memory: 6.783607482910156 GB (3844.88671875 MB free)
  Uptime: 829.87 sec
  Load Avg:  1.63  1.47  0.89
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, skylake-avx512)
```

### Baseline
```
Julia Version 1.7.2
Commit bf53498635 (2022-02-06 15:21 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 20.04.4 LTS
  uname: Linux 5.13.0-1022-azure #26~20.04.1-Ubuntu SMP Thu Apr 7 19:42:45 UTC 2022 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz       7192 s          2 s        307 s       3959 s          0 s
       #2  2095 MHz       8311 s          1 s        326 s       2840 s          0 s
       
  Memory: 6.783607482910156 GB (3830.4375 MB free)
  Uptime: 1154.01 sec
  Load Avg:  1.72  1.61  1.12
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, skylake-avx512)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 8 May 2022 - 2:8
* Package commit: 7f3ffe
* Julia commit: bf5349
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
| `["collect", "assoc", "basesize=1"]`                | 300.067 ms (5%) |         |  25.97 MiB (1%) |      306793 |
| `["collect", "assoc", "basesize=1024"]`             | 242.590 ms (5%) |         |   2.61 MiB (1%) |         455 |
| `["collect", "assoc", "basesize=32"]`               | 246.459 ms (5%) |         |   4.82 MiB (1%) |       11706 |
| `["collect", "seq"]`                                | 482.742 ms (5%) |         | 812.73 KiB (1%) |          11 |
| `["collect", "unordered", "basesize=1"]`            | 424.474 ms (5%) |         |  23.87 MiB (1%) |      412022 |
| `["collect", "unordered", "basesize=1024"]`         | 261.850 ms (5%) |         |   1.01 MiB (1%) |         983 |
| `["collect", "unordered", "basesize=32"]`           | 273.232 ms (5%) |         |   1.58 MiB (1%) |       14656 |
| `["findfirst", "n=1000", "foldl"]`                  | 770.073 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 429.973 ms (5%) |         | 230.67 KiB (1%) |        3251 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 499.494 ms (5%) |         | 149.38 KiB (1%) |        2091 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 614.709 ms (5%) |         | 105.27 KiB (1%) |        1454 |
| `["findfirst", "n=400", "foldl"]`                   | 578.726 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 304.227 ms (5%) |         | 374.77 KiB (1%) |        5353 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 307.078 ms (5%) |         | 200.70 KiB (1%) |        2868 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 363.164 ms (5%) |         | 126.36 KiB (1%) |        1805 |
| `["findfirst", "n=500", "foldl"]`                   |  97.496 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 204.782 ms (5%) |         | 240.69 KiB (1%) |        3312 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 294.347 ms (5%) |         | 168.97 KiB (1%) |        2374 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 138.553 ms (5%) |         |  59.88 KiB (1%) |         815 |
| `["overhead", "default"]`                           |  86.005 μs (5%) |         |  32.73 KiB (1%) |         418 |
| `["overhead", "stoppable=false"]`                   |  87.205 μs (5%) |         |  32.75 KiB (1%) |         418 |
| `["overhead", "stoppable=true"]`                    |  97.807 μs (5%) |         |  44.22 KiB (1%) |         609 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   3.654 ms (5%) |         | 728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   4.359 ms (5%) |         |   1.79 MiB (1%) |         216 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   4.086 ms (5%) |         |   1.42 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  21.184 ms (5%) |         |   1.60 MiB (1%) |        3008 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  29.020 ms (5%) |         |   1.26 MiB (1%) |        7336 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  26.495 ms (5%) |         |   1.29 MiB (1%) |        6296 |
| `["parallel_histogram", "seq"]`                     |   6.469 ms (5%) |         | 364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  41.560 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  20.757 ms (5%) |         |  736 bytes (1%) |          11 |
| `["splitby", "count", "foldl"]`                     |   2.429 ms (5%) |         |                 |             |
| `["splitby", "count", "man"]`                       |   1.577 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    |   1.278 ms (5%) |         |   1.09 KiB (1%) |          19 |
| `["sum", "random", "foldl"]`                        |  19.556 ms (5%) |         |                 |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   9.829 ms (5%) |         |  74.05 KiB (1%) |        1100 |
| `["sum", "random", "reduce", "basesize=256"]`       |   9.765 ms (5%) |         |  36.73 KiB (1%) |         546 |
| `["sum", "random", "reduce", "basesize=512"]`       |   9.695 ms (5%) |         |  18.02 KiB (1%) |         267 |
| `["sum", "uniform", "foldl"]`                       |  18.924 ms (5%) |         |                 |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   9.632 ms (5%) |         |  74.05 KiB (1%) |        1100 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   9.519 ms (5%) |         |  36.70 KiB (1%) |         545 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   9.429 ms (5%) |         |  18.03 KiB (1%) |         268 |
| `["sum", "valley", "foldl"]`                        |  19.116 ms (5%) |         |                 |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   9.948 ms (5%) |         |  74.11 KiB (1%) |        1102 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   9.842 ms (5%) |         |  36.70 KiB (1%) |         545 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   9.823 ms (5%) |         |  18.00 KiB (1%) |         267 |
| `["words", "nthreads=1"]`                           |  26.220 ms (5%) |         |  31.78 MiB (1%) |     1035347 |
| `["words", "nthreads=2"]`                           |  17.728 ms (5%) |         |  32.49 MiB (1%) |     1035442 |
| `["words", "nthreads=4"]`                           |  18.887 ms (5%) |         |  33.13 MiB (1%) |     1035640 |

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
Julia Version 1.7.2
Commit bf53498635 (2022-02-06 15:21 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 20.04.4 LTS
  uname: Linux 5.13.0-1022-azure #26~20.04.1-Ubuntu SMP Thu Apr 7 19:42:45 UTC 2022 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz       4856 s          2 s        237 s       3134 s          0 s
       #2  2095 MHz       5736 s          1 s        258 s       2249 s          0 s
       
  Memory: 6.783607482910156 GB (3844.88671875 MB free)
  Uptime: 829.87 sec
  Load Avg:  1.63  1.47  0.89
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, skylake-avx512)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 8 May 2022 - 2:13
* Package commit: 6125fe
* Julia commit: bf5349
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
| `["collect", "assoc", "basesize=1"]`                | 293.765 ms (5%) |         |   25.97 MiB (1%) |      306838 |
| `["collect", "assoc", "basesize=1024"]`             | 241.213 ms (5%) |         |    2.61 MiB (1%) |         455 |
| `["collect", "assoc", "basesize=32"]`               | 241.688 ms (5%) |         |    4.82 MiB (1%) |       11712 |
| `["collect", "seq"]`                                | 472.447 ms (5%) |         |  812.73 KiB (1%) |          11 |
| `["collect", "unordered", "basesize=1"]`            | 427.911 ms (5%) |         |   23.91 MiB (1%) |      413317 |
| `["collect", "unordered", "basesize=1024"]`         | 260.860 ms (5%) |         | 1005.67 KiB (1%) |        1114 |
| `["collect", "unordered", "basesize=32"]`           | 273.530 ms (5%) |         |    1.58 MiB (1%) |       14657 |
| `["findfirst", "n=1000", "foldl"]`                  | 749.010 ms (5%) |         |                  |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 474.471 ms (5%) |         |  264.16 KiB (1%) |        3697 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 585.735 ms (5%) |         |  170.47 KiB (1%) |        2384 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 672.867 ms (5%) |         |  108.55 KiB (1%) |        1509 |
| `["findfirst", "n=400", "foldl"]`                   | 558.101 ms (5%) |         |                  |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 295.721 ms (5%) |         |  373.14 KiB (1%) |        5331 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 302.616 ms (5%) |         |  201.08 KiB (1%) |        2880 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 396.542 ms (5%) |         |  137.06 KiB (1%) |        1958 |
| `["findfirst", "n=500", "foldl"]`                   |  97.330 ms (5%) |         |                  |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 147.407 ms (5%) |         |  175.38 KiB (1%) |        2453 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 191.680 ms (5%) |         |  120.61 KiB (1%) |        1664 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 308.715 ms (5%) |         |   94.80 KiB (1%) |        1329 |
| `["overhead", "default"]`                           |  84.805 μs (5%) |         |   32.73 KiB (1%) |         418 |
| `["overhead", "stoppable=false"]`                   |  82.405 μs (5%) |         |   32.75 KiB (1%) |         418 |
| `["overhead", "stoppable=true"]`                    |  92.506 μs (5%) |         |   44.19 KiB (1%) |         608 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   3.557 ms (5%) |         |  728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   4.374 ms (5%) |         |    1.79 MiB (1%) |         215 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   3.931 ms (5%) |         |    1.42 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  20.167 ms (5%) |         |    1.58 MiB (1%) |        2377 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  28.458 ms (5%) |         |    1.21 MiB (1%) |        5885 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  25.142 ms (5%) |         |    1.28 MiB (1%) |        5959 |
| `["parallel_histogram", "seq"]`                     |   6.365 ms (5%) |         |  364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  41.043 ms (5%) |         |                  |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  20.562 ms (5%) |         |   736 bytes (1%) |          11 |
| `["splitby", "count", "foldl"]`                     |   2.394 ms (5%) |         |                  |             |
| `["splitby", "count", "man"]`                       |   1.473 ms (5%) |         |                  |             |
| `["splitby", "count", "reduce"]`                    |   1.198 ms (5%) |         |    1.09 KiB (1%) |          19 |
| `["sum", "random", "foldl"]`                        |  18.724 ms (5%) |         |                  |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   9.439 ms (5%) |         |   74.17 KiB (1%) |        1104 |
| `["sum", "random", "reduce", "basesize=256"]`       |   9.465 ms (5%) |         |   36.73 KiB (1%) |         546 |
| `["sum", "random", "reduce", "basesize=512"]`       |   9.331 ms (5%) |         |   18.05 KiB (1%) |         268 |
| `["sum", "uniform", "foldl"]`                       |  18.112 ms (5%) |         |                  |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   9.261 ms (5%) |         |   74.17 KiB (1%) |        1104 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   9.287 ms (5%) |         |   36.77 KiB (1%) |         547 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   9.075 ms (5%) |         |   18.03 KiB (1%) |         268 |
| `["sum", "valley", "foldl"]`                        |  18.826 ms (5%) |         |                  |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   9.644 ms (5%) |         |   74.08 KiB (1%) |        1101 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   9.552 ms (5%) |         |   36.70 KiB (1%) |         545 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   9.593 ms (5%) |         |   18.00 KiB (1%) |         267 |
| `["words", "nthreads=1"]`                           |  27.359 ms (5%) |         |   31.67 MiB (1%) |     1031319 |
| `["words", "nthreads=2"]`                           |  17.719 ms (5%) |         |   32.38 MiB (1%) |     1031392 |
| `["words", "nthreads=4"]`                           |  17.737 ms (5%) |         |   32.83 MiB (1%) |     1031458 |

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
Julia Version 1.7.2
Commit bf53498635 (2022-02-06 15:21 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 20.04.4 LTS
  uname: Linux 5.13.0-1022-azure #26~20.04.1-Ubuntu SMP Thu Apr 7 19:42:45 UTC 2022 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz       7192 s          2 s        307 s       3959 s          0 s
       #2  2095 MHz       8311 s          1 s        326 s       2840 s          0 s
       
  Memory: 6.783607482910156 GB (3830.4375 MB free)
  Uptime: 1154.01 sec
  Load Avg:  1.72  1.61  1.12
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, skylake-avx512)
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
    CPU MHz:                         2095.174
    BogoMIPS:                        4190.34
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
    Vulnerability Spectre v2:        Mitigation; Retpolines, STIBP disabled, RSB filling
    Vulnerability Srbds:             Not affected
    Vulnerability Tsx async abort:   Mitigation; Clear CPU buffers; SMT Host state unknown
    Flags:                           fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush mmx fxsr sse sse2 ss ht syscall nx pdpe1gb rdtscp lm constant_tsc rep_good nopl xtopology cpuid pni pclmulqdq ssse3 fma cx16 pcid sse4_1 sse4_2 movbe popcnt aes xsave avx f16c rdrand hypervisor lahf_lm abm 3dnowprefetch invpcid_single pti fsgsbase bmi1 hle avx2 smep bmi2 erms invpcid rtm avx512f avx512dq rdseed adx smap clflushopt avx512cd avx512bw avx512vl xsaveopt xsavec xsaves md_clear
    

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

