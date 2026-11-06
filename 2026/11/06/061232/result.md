# Multi-thread benchmark result

* Pull request commit: [`cc0b5ccd74c064013b581eff5818a79cd256c07b`](https://github.com/JuliaFolds/Transducers.jl/commit/cc0b5ccd74c064013b581eff5818a79cd256c07b)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/243> (Update */Manifest.toml)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 6 Nov 2026 - 06:07
    - Baseline: 6 Nov 2026 - 06:12
* Package commits:
    - Target: a2e1391
    - Baseline: 2a51f8d
* Julia commits:
    - Target: 742b9ab
    - Baseline: 742b9ab
* Julia command flags:
    - Target: None
    - Baseline: None
* Environment variables:
    - Target: `JULIA_NUM_THREADS => 2`
    - Baseline: `JULIA_NUM_THREADS => 2`

## Results
A ratio greater than `1.0` denotes a possible regression (marked with :x:), while a ratio less
than `1.0` denotes a possible improvement (marked with :white_check_mark:). Brackets display [tolerances](https://juliaci.github.io/BenchmarkTools.jl/stable/manual/#Benchmark-Parameters) for the benchmark estimates. Only significant results - results
that indicate possible regressions or improvements - are shown below (thus, an empty table means that all
benchmark results remained invariant between builds).

| ID                                                  | time ratio                   | memory ratio                 |
|-----------------------------------------------------|------------------------------|------------------------------|
| `["findfirst", "n=1000", "reduce", "basesize=128"]` |                1.47 (5%) :x: |                1.42 (1%) :x: |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` |                1.09 (5%) :x: |                1.07 (1%) :x: |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 0.93 (5%) :white_check_mark: | 0.95 (1%) :white_check_mark: |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  |                   0.98 (5%)  | 0.96 (1%) :white_check_mark: |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  |                   1.01 (5%)  |                1.03 (1%) :x: |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  |                   1.00 (5%)  |                1.09 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 0.81 (5%) :white_check_mark: | 0.87 (1%) :white_check_mark: |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |                1.84 (5%) :x: |                1.47 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 0.83 (5%) :white_check_mark: | 0.94 (1%) :white_check_mark: |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |                   0.97 (5%)  | 0.87 (1%) :white_check_mark: |
| `["parallel_histogram", "comm", "basesize=16384"]`  | 0.95 (5%) :white_check_mark: | 0.96 (1%) :white_check_mark: |
| `["parallel_histogram", "comm", "basesize=4096"]`   |                   0.95 (5%)  |                1.05 (1%) :x: |
| `["parallel_histogram", "comm", "basesize=8192"]`   | 0.94 (5%) :white_check_mark: | 0.92 (1%) :white_check_mark: |
| `["splitby", "count", "foldl"]`                     |                1.12 (5%) :x: |                   1.00 (1%)  |
| `["splitby", "count", "reduce"]`                    |                1.09 (5%) :x: |                1.03 (1%) :x: |

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
Julia Version 1.7.3
Commit 742b9abb4d (2022-05-06 12:58 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 24.04.5 LTS
  uname: Linux 7.0.0-1017-azure #17~24.04.1-Ubuntu SMP PREEMPT Thu Sep 24 18:46:57 UTC 2026 x86_64 x86_64
  CPU: AMD EPYC 9V45 96-Core Processor: 
              speed         user         nice          sys         idle          irq
       #1  4530 MHz       2351 s          0 s        124 s       3892 s          0 s
       #2  4527 MHz       2190 s          0 s        116 s       4039 s          0 s
       #3  4518 MHz       2418 s          0 s        117 s       3803 s          0 s
       #4  4532 MHz       2516 s          0 s        128 s       3647 s          0 s
       
  Memory: 15.60928726196289 GB (13177.43359375 MB free)
  Uptime: 639.23 sec
  Load Avg:  1.88  1.59  0.89
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, generic)
```

### Baseline
```
Julia Version 1.7.3
Commit 742b9abb4d (2022-05-06 12:58 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 24.04.5 LTS
  uname: Linux 7.0.0-1017-azure #17~24.04.1-Ubuntu SMP PREEMPT Thu Sep 24 18:46:57 UTC 2026 x86_64 x86_64
  CPU: AMD EPYC 9V45 96-Core Processor: 
              speed         user         nice          sys         idle          irq
       #1  4628 MHz       3254 s          0 s        150 s       5802 s          0 s
       #2  4541 MHz       3122 s          0 s        154 s       5907 s          0 s
       #3  4540 MHz       3492 s          0 s        158 s       5529 s          0 s
       #4  4541 MHz       4124 s          0 s        183 s       4826 s          0 s
       
  Memory: 15.60928726196289 GB (13165.37109375 MB free)
  Uptime: 923.6 sec
  Load Avg:  1.75  1.68  1.12
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, generic)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 6 Nov 2026 - 06:07
* Package commit: a2e1391
* Julia commit: 742b9ab
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
| `["collect", "assoc", "basesize=1"]`                | 101.414 ms (5%) |         |   4.36 MiB (1%) |       32800 |
| `["collect", "assoc", "basesize=1024"]`             | 100.766 ms (5%) |         |   1.09 MiB (1%) |          53 |
| `["collect", "assoc", "basesize=32"]`               | 100.819 ms (5%) |         |   1.48 MiB (1%) |        1052 |
| `["collect", "seq"]`                                | 201.288 ms (5%) |         | 256.05 KiB (1%) |           2 |
| `["collect", "unordered", "basesize=1"]`            | 166.187 ms (5%) |         |  23.89 MiB (1%) |      412773 |
| `["collect", "unordered", "basesize=1024"]`         | 104.438 ms (5%) |         |   1.01 MiB (1%) |        1111 |
| `["collect", "unordered", "basesize=32"]`           | 109.040 ms (5%) |         |   1.59 MiB (1%) |       15081 |
| `["findfirst", "n=1000", "foldl"]`                  | 341.980 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 275.052 ms (5%) |         | 329.75 KiB (1%) |        4624 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 269.817 ms (5%) |         | 173.20 KiB (1%) |        2435 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 217.942 ms (5%) |         |  77.47 KiB (1%) |        1094 |
| `["findfirst", "n=400", "foldl"]`                   | 256.237 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 132.490 ms (5%) |         | 382.39 KiB (1%) |        5428 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 135.554 ms (5%) |         | 206.42 KiB (1%) |        2946 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 156.361 ms (5%) |         | 137.80 KiB (1%) |        1946 |
| `["findfirst", "n=500", "foldl"]`                   |  44.434 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |  68.367 ms (5%) |         | 199.48 KiB (1%) |        2718 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |  79.105 ms (5%) |         | 121.28 KiB (1%) |        1664 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  45.246 ms (5%) |         |  49.44 KiB (1%) |         664 |
| `["overhead", "default"]`                           |  35.753 μs (5%) |         |  32.70 KiB (1%) |         417 |
| `["overhead", "stoppable=false"]`                   |  36.454 μs (5%) |         |  32.75 KiB (1%) |         418 |
| `["overhead", "stoppable=true"]`                    |  41.021 μs (5%) |         |  44.25 KiB (1%) |         610 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   1.508 ms (5%) |         | 728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   1.969 ms (5%) |         |   1.79 MiB (1%) |         216 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   1.723 ms (5%) |         |   1.42 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |   7.278 ms (5%) |         |   1.66 MiB (1%) |        4981 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |   9.423 ms (5%) |         |   1.41 MiB (1%) |       12368 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |   8.586 ms (5%) |         |   1.71 MiB (1%) |        6657 |
| `["parallel_histogram", "seq"]`                     |   2.659 ms (5%) |         | 364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  29.741 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  14.887 ms (5%) |         |  736 bytes (1%) |          11 |
| `["splitby", "count", "foldl"]`                     |   1.317 ms (5%) |         |                 |             |
| `["splitby", "count", "man"]`                       | 694.121 μs (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    | 613.731 μs (5%) |         |   1.09 KiB (1%) |          19 |
| `["sum", "random", "foldl"]`                        |   7.711 ms (5%) |         |                 |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   3.947 ms (5%) |         |  74.16 KiB (1%) |        1103 |
| `["sum", "random", "reduce", "basesize=256"]`       |   3.906 ms (5%) |         |  36.69 KiB (1%) |         544 |
| `["sum", "random", "reduce", "basesize=512"]`       |   3.880 ms (5%) |         |  18.08 KiB (1%) |         269 |
| `["sum", "uniform", "foldl"]`                       |   7.503 ms (5%) |         |                 |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   3.846 ms (5%) |         |  74.22 KiB (1%) |        1105 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   3.806 ms (5%) |         |  36.75 KiB (1%) |         546 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   3.780 ms (5%) |         |  18.08 KiB (1%) |         269 |
| `["sum", "valley", "foldl"]`                        |   7.791 ms (5%) |         |                 |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   3.985 ms (5%) |         |  74.06 KiB (1%) |        1100 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   3.942 ms (5%) |         |  36.78 KiB (1%) |         547 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   3.936 ms (5%) |         |  18.05 KiB (1%) |         268 |
| `["words", "nthreads=1"]`                           |   8.263 ms (5%) |         |  31.39 MiB (1%) |     1022844 |
| `["words", "nthreads=2"]`                           |   5.806 ms (5%) |         |  31.75 MiB (1%) |     1022888 |
| `["words", "nthreads=4"]`                           |   6.011 ms (5%) |         |  32.46 MiB (1%) |     1022961 |

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
Julia Version 1.7.3
Commit 742b9abb4d (2022-05-06 12:58 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 24.04.5 LTS
  uname: Linux 7.0.0-1017-azure #17~24.04.1-Ubuntu SMP PREEMPT Thu Sep 24 18:46:57 UTC 2026 x86_64 x86_64
  CPU: AMD EPYC 9V45 96-Core Processor: 
              speed         user         nice          sys         idle          irq
       #1  4530 MHz       2351 s          0 s        124 s       3892 s          0 s
       #2  4527 MHz       2190 s          0 s        116 s       4039 s          0 s
       #3  4518 MHz       2418 s          0 s        117 s       3803 s          0 s
       #4  4532 MHz       2516 s          0 s        128 s       3647 s          0 s
       
  Memory: 15.60928726196289 GB (13177.43359375 MB free)
  Uptime: 639.23 sec
  Load Avg:  1.88  1.59  0.89
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, generic)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 6 Nov 2026 - 06:12
* Package commit: 2a51f8d
* Julia commit: 742b9ab
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
| `["collect", "assoc", "basesize=1"]`                | 101.545 ms (5%) |         |   4.36 MiB (1%) |       32800 |
| `["collect", "assoc", "basesize=1024"]`             | 101.035 ms (5%) |         |   1.09 MiB (1%) |          54 |
| `["collect", "assoc", "basesize=32"]`               | 100.955 ms (5%) |         |   1.48 MiB (1%) |        1052 |
| `["collect", "seq"]`                                | 201.388 ms (5%) |         | 256.05 KiB (1%) |           2 |
| `["collect", "unordered", "basesize=1"]`            | 166.583 ms (5%) |         |  23.89 MiB (1%) |      412529 |
| `["collect", "unordered", "basesize=1024"]`         | 104.977 ms (5%) |         |   1.01 MiB (1%) |        1142 |
| `["collect", "unordered", "basesize=32"]`           | 109.762 ms (5%) |         |   1.60 MiB (1%) |       15303 |
| `["findfirst", "n=1000", "foldl"]`                  | 342.153 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 186.484 ms (5%) |         | 232.86 KiB (1%) |        3276 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 248.640 ms (5%) |         | 161.72 KiB (1%) |        2279 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 233.759 ms (5%) |         |  81.33 KiB (1%) |        1146 |
| `["findfirst", "n=400", "foldl"]`                   | 256.229 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 135.259 ms (5%) |         | 397.38 KiB (1%) |        5640 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 134.052 ms (5%) |         | 200.86 KiB (1%) |        2873 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 156.649 ms (5%) |         | 126.17 KiB (1%) |        1791 |
| `["findfirst", "n=500", "foldl"]`                   |  44.454 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |  84.448 ms (5%) |         | 229.66 KiB (1%) |        3195 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |  42.880 ms (5%) |         |  82.31 KiB (1%) |        1116 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  54.222 ms (5%) |         |  52.80 KiB (1%) |         723 |
| `["overhead", "default"]`                           |  36.085 μs (5%) |         |  32.73 KiB (1%) |         418 |
| `["overhead", "stoppable=false"]`                   |  36.435 μs (5%) |         |  32.75 KiB (1%) |         418 |
| `["overhead", "stoppable=true"]`                    |  41.002 μs (5%) |         |  44.25 KiB (1%) |         610 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   1.512 ms (5%) |         | 728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   2.025 ms (5%) |         |   2.05 MiB (1%) |         222 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   1.746 ms (5%) |         |   1.42 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |   7.676 ms (5%) |         |   1.72 MiB (1%) |        7002 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |   9.895 ms (5%) |         |   1.35 MiB (1%) |       10327 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |   9.135 ms (5%) |         |   1.86 MiB (1%) |       11700 |
| `["parallel_histogram", "seq"]`                     |   2.671 ms (5%) |         | 364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  29.723 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  14.889 ms (5%) |         |  736 bytes (1%) |          11 |
| `["splitby", "count", "foldl"]`                     |   1.172 ms (5%) |         |                 |             |
| `["splitby", "count", "man"]`                       | 671.747 μs (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    | 561.501 μs (5%) |         |   1.06 KiB (1%) |          18 |
| `["sum", "random", "foldl"]`                        |   7.691 ms (5%) |         |                 |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   3.938 ms (5%) |         |  74.12 KiB (1%) |        1102 |
| `["sum", "random", "reduce", "basesize=256"]`       |   3.897 ms (5%) |         |  36.72 KiB (1%) |         545 |
| `["sum", "random", "reduce", "basesize=512"]`       |   3.870 ms (5%) |         |  18.11 KiB (1%) |         270 |
| `["sum", "uniform", "foldl"]`                       |   7.510 ms (5%) |         |                 |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   3.839 ms (5%) |         |  74.06 KiB (1%) |        1100 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   3.804 ms (5%) |         |  36.75 KiB (1%) |         546 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   3.779 ms (5%) |         |  18.05 KiB (1%) |         268 |
| `["sum", "valley", "foldl"]`                        |   7.796 ms (5%) |         |                 |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   3.985 ms (5%) |         |  74.09 KiB (1%) |        1101 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   3.950 ms (5%) |         |  36.78 KiB (1%) |         547 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   3.926 ms (5%) |         |  18.08 KiB (1%) |         269 |
| `["words", "nthreads=1"]`                           |   8.579 ms (5%) |         |  31.44 MiB (1%) |     1023454 |
| `["words", "nthreads=2"]`                           |   5.859 ms (5%) |         |  31.80 MiB (1%) |     1023497 |
| `["words", "nthreads=4"]`                           |   6.231 ms (5%) |         |  32.51 MiB (1%) |     1023607 |

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
Julia Version 1.7.3
Commit 742b9abb4d (2022-05-06 12:58 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 24.04.5 LTS
  uname: Linux 7.0.0-1017-azure #17~24.04.1-Ubuntu SMP PREEMPT Thu Sep 24 18:46:57 UTC 2026 x86_64 x86_64
  CPU: AMD EPYC 9V45 96-Core Processor: 
              speed         user         nice          sys         idle          irq
       #1  4628 MHz       3254 s          0 s        150 s       5802 s          0 s
       #2  4541 MHz       3122 s          0 s        154 s       5907 s          0 s
       #3  4540 MHz       3492 s          0 s        158 s       5529 s          0 s
       #4  4541 MHz       4124 s          0 s        183 s       4826 s          0 s
       
  Memory: 15.60928726196289 GB (13165.37109375 MB free)
  Uptime: 923.6 sec
  Load Avg:  1.75  1.68  1.12
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, generic)
```

---
# Runtime information
| Runtime Info | |
|:--|:--|
| BLAS #threads | 4 |
| `BLAS.vendor()` | `openblas64` |
| `Sys.CPU_THREADS` | 4 |

`lscpu` output:

    Architecture:                            x86_64
    CPU op-mode(s):                          32-bit, 64-bit
    Address sizes:                           48 bits physical, 48 bits virtual
    Byte Order:                              Little Endian
    CPU(s):                                  4
    On-line CPU(s) list:                     0-3
    Vendor ID:                               AuthenticAMD
    Model name:                              AMD EPYC 9V45 96-Core Processor
    CPU family:                              26
    Model:                                   2
    Thread(s) per core:                      2
    Core(s) per socket:                      2
    Socket(s):                               1
    Stepping:                                1
    BogoMIPS:                                5192.24
    Flags:                                   fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush mmx fxsr sse sse2 ht syscall nx mmxext fxsr_opt pdpe1gb rdtscp lm constant_tsc rep_good nopl xtopology tsc_reliable nonstop_tsc cpuid extd_apicid aperfmperf tsc_known_freq pni pclmulqdq ssse3 fma cx16 pcid sse4_1 sse4_2 x2apic movbe popcnt aes xsave avx f16c rdrand hypervisor lahf_lm cmp_legacy svm cr8_legacy abm sse4a misalignsse 3dnowprefetch osvw topoext vmmcall fsgsbase bmi1 avx2 smep bmi2 erms invpcid avx512f avx512dq rdseed adx smap avx512ifma clflushopt clwb avx512cd sha_ni avx512bw avx512vl xsaveopt xsavec xgetbv1 xsaves user_shstk avx_vnni avx512_bf16 clzero xsaveerptr rdpru arat npt nrip_save tsc_scale vmcb_clean flushbyasid decodeassists pausefilter pfthreshold v_vmsave_vmload avx512vbmi umip avx512_vbmi2 gfni vaes vpclmulqdq avx512_vnni avx512_bitalg avx512_vpopcntdq rdpid fsrm avx512_vp2intersect
    Virtualization:                          AMD-V
    Hypervisor vendor:                       Microsoft
    Virtualization type:                     full
    L1d cache:                               96 KiB (2 instances)
    L1i cache:                               64 KiB (2 instances)
    L2 cache:                                2 MiB (2 instances)
    L3 cache:                                32 MiB (1 instance)
    NUMA node(s):                            1
    NUMA node0 CPU(s):                       0-3
    Vulnerability Gather data sampling:      Not affected
    Vulnerability Ghostwrite:                Not affected
    Vulnerability Indirect target selection: Not affected
    Vulnerability Itlb multihit:             Not affected
    Vulnerability L1tf:                      Not affected
    Vulnerability Mds:                       Not affected
    Vulnerability Meltdown:                  Not affected
    Vulnerability Mmio stale data:           Not affected
    Vulnerability Old microcode:             Not affected
    Vulnerability Reg file data sampling:    Not affected
    Vulnerability Retbleed:                  Not affected
    Vulnerability Spec rstack overflow:      Vulnerable: Safe RET, no microcode
    Vulnerability Spec store bypass:         Vulnerable
    Vulnerability Spectre v1:                Mitigation; usercopy/swapgs barriers and __user pointer sanitization
    Vulnerability Spectre v2:                Mitigation; Retpolines; STIBP disabled; RSB filling; PBRSB-eIBRS Not affected; BHI Not affected
    Vulnerability Srbds:                     Not affected
    Vulnerability Tsa:                       Not affected
    Vulnerability Tsx async abort:           Not affected
    Vulnerability Vmscape:                   Not affected
    

| Cpu Property       | Value                                                      |
|:------------------ |:---------------------------------------------------------- |
| Brand              | AMD EPYC 9V45 96-Core Processor                            |
| Vendor             | :AMD                                                       |
| Architecture       | :Unknown                                                   |
| Model              | Family: 0xbf, Model: 0x02, Stepping: 0x01, Type: 0x00      |
| Cores              | 8 physical cores, 16 logical cores (on executing CPU)      |
|                    | Hyperthreading hardware capability detected                |
| Clock Frequencies  | Not supported by CPU                                       |
| Data Cache         | Level 1:3 : (48, 1024, 32768) kbytes                       |
|                    | 64 byte cache line size                                    |
| Address Size       | 48 bits virtual, 48 bits physical                          |
| SIMD               | 512 bit = 64 byte max. SIMD vector size                    |
| Time Stamp Counter | TSC is accessible via `rdtsc`                              |
|                    | TSC runs at constant rate (invariant from clock frequency) |
| Perf. Monitoring   | Performance Monitoring Counters (PMC) are not supported    |
| Hypervisor         | Yes, Microsoft                                             |

