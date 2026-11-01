# Multi-thread benchmark result

* Pull request commit: [`38a157ac898df244b3091bb156129043926b9787`](https://github.com/JuliaFolds/Transducers.jl/commit/38a157ac898df244b3091bb156129043926b9787)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/243> (Update */Manifest.toml)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 1 Nov 2026 - 05:37
    - Baseline: 1 Nov 2026 - 05:42
* Package commits:
    - Target: 61429ef
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
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 0.78 (5%) :white_check_mark: | 0.78 (1%) :white_check_mark: |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 0.78 (5%) :white_check_mark: | 0.86 (1%) :white_check_mark: |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 0.81 (5%) :white_check_mark: | 0.79 (1%) :white_check_mark: |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  |                   0.97 (5%)  | 0.96 (1%) :white_check_mark: |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  |                   1.00 (5%)  |                1.01 (1%) :x: |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  |                   0.99 (5%)  | 0.96 (1%) :white_check_mark: |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |                2.28 (5%) :x: |                1.82 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |                1.69 (5%) :x: |                1.41 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 0.78 (5%) :white_check_mark: | 0.89 (1%) :white_check_mark: |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |                   1.02 (5%)  | 0.87 (1%) :white_check_mark: |
| `["parallel_histogram", "comm", "basesize=16384"]`  |                2.21 (5%) :x: | 0.89 (1%) :white_check_mark: |
| `["parallel_histogram", "comm", "basesize=4096"]`   |                2.14 (5%) :x: |                1.02 (1%) :x: |
| `["parallel_histogram", "comm", "basesize=8192"]`   |                2.30 (5%) :x: |                1.42 (1%) :x: |
| `["parallel_histogram", "seq"]`                     |                1.07 (5%) :x: |                   1.00 (1%)  |
| `["splitby", "count", "reduce"]`                    |                   1.00 (5%)  | 0.98 (1%) :white_check_mark: |
| `["words", "nthreads=2"]`                           |                1.05 (5%) :x: |                   1.00 (1%)  |

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
  CPU: INTEL(R) XEON(R) PLATINUM 8573C: 
              speed         user         nice          sys         idle          irq
       #1  3099 MHz       2165 s          0 s        114 s       4118 s          0 s
       #2  3100 MHz       2636 s          0 s        109 s       3702 s          0 s
       #3  3097 MHz       2277 s          0 s        134 s       4001 s          0 s
       #4  3097 MHz       3026 s          0 s        103 s       3310 s          0 s
       
  Memory: 15.608318328857422 GB (13164.56640625 MB free)
  Uptime: 649.03 sec
  Load Avg:  1.88  1.65  0.97
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, icelake-client)
```

### Baseline
```
Julia Version 1.7.3
Commit 742b9abb4d (2022-05-06 12:58 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 24.04.5 LTS
  uname: Linux 7.0.0-1017-azure #17~24.04.1-Ubuntu SMP PREEMPT Thu Sep 24 18:46:57 UTC 2026 x86_64 x86_64
  CPU: INTEL(R) XEON(R) PLATINUM 8573C: 
              speed         user         nice          sys         idle          irq
       #1  3091 MHz       3390 s          0 s        156 s       5918 s          0 s
       #2  3100 MHz       4167 s          0 s        151 s       5196 s          0 s
       #3  3093 MHz       3125 s          0 s        172 s       6185 s          0 s
       #4  3097 MHz       4242 s          0 s        154 s       5113 s          0 s
       
  Memory: 15.608318328857422 GB (13115.50390625 MB free)
  Uptime: 956.38 sec
  Load Avg:  1.78  1.71  1.19
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, icelake-client)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 1 Nov 2026 - 05:37
* Package commit: 61429ef
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

| ID                                                  | time            | GC time | memory           | allocations |
|-----------------------------------------------------|----------------:|--------:|-----------------:|------------:|
| `["collect", "assoc", "basesize=1"]`                | 179.834 ms (5%) |         |    4.36 MiB (1%) |       32801 |
| `["collect", "assoc", "basesize=1024"]`             | 178.093 ms (5%) |         |    1.09 MiB (1%) |          54 |
| `["collect", "assoc", "basesize=32"]`               | 178.458 ms (5%) |         |    1.48 MiB (1%) |        1052 |
| `["collect", "seq"]`                                | 354.459 ms (5%) |         |  256.05 KiB (1%) |           2 |
| `["collect", "unordered", "basesize=1"]`            | 283.329 ms (5%) |         |   23.87 MiB (1%) |      411964 |
| `["collect", "unordered", "basesize=1024"]`         | 189.273 ms (5%) |         | 1011.30 KiB (1%) |        1303 |
| `["collect", "unordered", "basesize=32"]`           | 198.441 ms (5%) |         |    1.60 MiB (1%) |       15163 |
| `["findfirst", "n=1000", "foldl"]`                  | 518.526 ms (5%) |         |                  |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 281.765 ms (5%) |         |  227.91 KiB (1%) |        3209 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 330.711 ms (5%) |         |  148.62 KiB (1%) |        2080 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 354.628 ms (5%) |         |   81.33 KiB (1%) |        1146 |
| `["findfirst", "n=400", "foldl"]`                   | 388.759 ms (5%) |         |                  |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 200.023 ms (5%) |         |  382.50 KiB (1%) |        5449 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 203.973 ms (5%) |         |  203.53 KiB (1%) |        2904 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 250.361 ms (5%) |         |  131.98 KiB (1%) |        1881 |
| `["findfirst", "n=500", "foldl"]`                   |  67.297 ms (5%) |         |                  |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 151.124 ms (5%) |         |  254.33 KiB (1%) |        3514 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |  97.260 ms (5%) |         |   97.25 KiB (1%) |        1337 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  67.875 ms (5%) |         |   50.69 KiB (1%) |         676 |
| `["overhead", "default"]`                           |  66.707 μs (5%) |         |   32.67 KiB (1%) |         416 |
| `["overhead", "stoppable=false"]`                   |  68.224 μs (5%) |         |   32.75 KiB (1%) |         418 |
| `["overhead", "stoppable=true"]`                    |  73.747 μs (5%) |         |   44.25 KiB (1%) |         610 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   2.716 ms (5%) |         |  728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   3.355 ms (5%) |         |    1.79 MiB (1%) |         216 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   3.036 ms (5%) |         |    1.42 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  17.040 ms (5%) |         |    1.38 MiB (1%) |        4603 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  27.492 ms (5%) |         |    1.44 MiB (1%) |       13253 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  24.542 ms (5%) |         |    1.81 MiB (1%) |        9801 |
| `["parallel_histogram", "seq"]`                     |   4.867 ms (5%) |         |  364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  32.815 ms (5%) |         |                  |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  16.465 ms (5%) |         |   736 bytes (1%) |          11 |
| `["splitby", "count", "foldl"]`                     |   1.805 ms (5%) |         |                  |             |
| `["splitby", "count", "man"]`                       |   1.031 ms (5%) |         |                  |             |
| `["splitby", "count", "reduce"]`                    | 896.081 μs (5%) |         |    1.02 KiB (1%) |          18 |
| `["sum", "random", "foldl"]`                        |  12.282 ms (5%) |         |                  |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   6.332 ms (5%) |         |   74.12 KiB (1%) |        1102 |
| `["sum", "random", "reduce", "basesize=256"]`       |   6.252 ms (5%) |         |   36.78 KiB (1%) |         547 |
| `["sum", "random", "reduce", "basesize=512"]`       |   6.202 ms (5%) |         |   18.08 KiB (1%) |         269 |
| `["sum", "uniform", "foldl"]`                       |  12.053 ms (5%) |         |                  |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   6.229 ms (5%) |         |   74.22 KiB (1%) |        1105 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   6.133 ms (5%) |         |   36.78 KiB (1%) |         547 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   6.091 ms (5%) |         |   18.08 KiB (1%) |         269 |
| `["sum", "valley", "foldl"]`                        |  12.375 ms (5%) |         |                  |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   6.396 ms (5%) |         |   74.16 KiB (1%) |        1103 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   6.286 ms (5%) |         |   36.78 KiB (1%) |         547 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   6.271 ms (5%) |         |   18.14 KiB (1%) |         271 |
| `["words", "nthreads=1"]`                           |  14.330 ms (5%) |         |   31.56 MiB (1%) |     1028043 |
| `["words", "nthreads=2"]`                           |   9.996 ms (5%) |         |   32.27 MiB (1%) |     1028138 |
| `["words", "nthreads=4"]`                           |  10.082 ms (5%) |         |   32.72 MiB (1%) |     1028236 |

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
  CPU: INTEL(R) XEON(R) PLATINUM 8573C: 
              speed         user         nice          sys         idle          irq
       #1  3099 MHz       2165 s          0 s        114 s       4118 s          0 s
       #2  3100 MHz       2636 s          0 s        109 s       3702 s          0 s
       #3  3097 MHz       2277 s          0 s        134 s       4001 s          0 s
       #4  3097 MHz       3026 s          0 s        103 s       3310 s          0 s
       
  Memory: 15.608318328857422 GB (13164.56640625 MB free)
  Uptime: 649.03 sec
  Load Avg:  1.88  1.65  0.97
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, icelake-client)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 1 Nov 2026 - 05:42
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

| ID                                                  | time            | GC time | memory           | allocations |
|-----------------------------------------------------|----------------:|--------:|-----------------:|------------:|
| `["collect", "assoc", "basesize=1"]`                | 179.580 ms (5%) |         |    4.36 MiB (1%) |       32800 |
| `["collect", "assoc", "basesize=1024"]`             | 178.140 ms (5%) |         |    1.09 MiB (1%) |          53 |
| `["collect", "assoc", "basesize=32"]`               | 177.936 ms (5%) |         |    1.48 MiB (1%) |        1052 |
| `["collect", "seq"]`                                | 354.294 ms (5%) |         |  256.05 KiB (1%) |           2 |
| `["collect", "unordered", "basesize=1"]`            | 278.898 ms (5%) |         |   23.86 MiB (1%) |      411587 |
| `["collect", "unordered", "basesize=1024"]`         | 189.793 ms (5%) |         | 1013.86 KiB (1%) |        1274 |
| `["collect", "unordered", "basesize=32"]`           | 198.448 ms (5%) |         |    1.60 MiB (1%) |       15225 |
| `["findfirst", "n=1000", "foldl"]`                  | 516.633 ms (5%) |         |                  |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 363.340 ms (5%) |         |  293.88 KiB (1%) |        4127 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 423.386 ms (5%) |         |  172.25 KiB (1%) |        2446 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 436.664 ms (5%) |         |  102.83 KiB (1%) |        1448 |
| `["findfirst", "n=400", "foldl"]`                   | 387.500 ms (5%) |         |                  |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 206.549 ms (5%) |         |  397.50 KiB (1%) |        5644 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 203.441 ms (5%) |         |  200.77 KiB (1%) |        2870 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 252.938 ms (5%) |         |  137.92 KiB (1%) |        1945 |
| `["findfirst", "n=500", "foldl"]`                   |  67.095 ms (5%) |         |                  |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |  66.199 ms (5%) |         |  139.73 KiB (1%) |        1901 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |  57.523 ms (5%) |         |   68.94 KiB (1%) |         939 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  86.948 ms (5%) |         |   56.86 KiB (1%) |         779 |
| `["overhead", "default"]`                           |  67.489 μs (5%) |         |   32.77 KiB (1%) |         419 |
| `["overhead", "stoppable=false"]`                   |  66.782 μs (5%) |         |   32.72 KiB (1%) |         417 |
| `["overhead", "stoppable=true"]`                    |  76.853 μs (5%) |         |   44.25 KiB (1%) |         610 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   2.587 ms (5%) |         |  728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   3.295 ms (5%) |         |    2.05 MiB (1%) |         222 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   2.919 ms (5%) |         |    1.42 MiB (1%) |         118 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |   7.727 ms (5%) |         |    1.55 MiB (1%) |        1313 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  12.823 ms (5%) |         |    1.41 MiB (1%) |       12483 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  10.660 ms (5%) |         |    1.27 MiB (1%) |        7854 |
| `["parallel_histogram", "seq"]`                     |   4.532 ms (5%) |         |  364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  32.816 ms (5%) |         |                  |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  16.434 ms (5%) |         |   736 bytes (1%) |          11 |
| `["splitby", "count", "foldl"]`                     |   1.831 ms (5%) |         |                  |             |
| `["splitby", "count", "man"]`                       |   1.032 ms (5%) |         |                  |             |
| `["splitby", "count", "reduce"]`                    | 897.588 μs (5%) |         |    1.03 KiB (1%) |          18 |
| `["sum", "random", "foldl"]`                        |  12.306 ms (5%) |         |                  |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   6.345 ms (5%) |         |   74.22 KiB (1%) |        1105 |
| `["sum", "random", "reduce", "basesize=256"]`       |   6.253 ms (5%) |         |   36.78 KiB (1%) |         547 |
| `["sum", "random", "reduce", "basesize=512"]`       |   6.220 ms (5%) |         |   18.08 KiB (1%) |         269 |
| `["sum", "uniform", "foldl"]`                       |  12.053 ms (5%) |         |                  |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   6.219 ms (5%) |         |   74.19 KiB (1%) |        1104 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   6.131 ms (5%) |         |   36.75 KiB (1%) |         546 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   6.081 ms (5%) |         |   18.05 KiB (1%) |         268 |
| `["sum", "valley", "foldl"]`                        |  12.378 ms (5%) |         |                  |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   6.382 ms (5%) |         |   74.12 KiB (1%) |        1102 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   6.305 ms (5%) |         |   36.75 KiB (1%) |         546 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   6.253 ms (5%) |         |   18.14 KiB (1%) |         271 |
| `["words", "nthreads=1"]`                           |  14.706 ms (5%) |         |   31.78 MiB (1%) |     1035238 |
| `["words", "nthreads=2"]`                           |   9.495 ms (5%) |         |   32.14 MiB (1%) |     1035274 |
| `["words", "nthreads=4"]`                           |  10.394 ms (5%) |         |   33.03 MiB (1%) |     1035446 |

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
  CPU: INTEL(R) XEON(R) PLATINUM 8573C: 
              speed         user         nice          sys         idle          irq
       #1  3091 MHz       3390 s          0 s        156 s       5918 s          0 s
       #2  3100 MHz       4167 s          0 s        151 s       5196 s          0 s
       #3  3093 MHz       3125 s          0 s        172 s       6185 s          0 s
       #4  3097 MHz       4242 s          0 s        154 s       5113 s          0 s
       
  Memory: 15.608318328857422 GB (13115.50390625 MB free)
  Uptime: 956.38 sec
  Load Avg:  1.78  1.71  1.19
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, icelake-client)
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
    Address sizes:                           48 bits physical, 57 bits virtual
    Byte Order:                              Little Endian
    CPU(s):                                  4
    On-line CPU(s) list:                     0-3
    Vendor ID:                               GenuineIntel
    Model name:                              INTEL(R) XEON(R) PLATINUM 8573C
    CPU family:                              6
    Model:                                   207
    Thread(s) per core:                      2
    Core(s) per socket:                      2
    Socket(s):                               1
    Stepping:                                2
    CPU(s) scaling MHz:                      130%
    CPU max MHz:                             2300.0000
    CPU min MHz:                             800.0000
    BogoMIPS:                                4600.00
    Flags:                                   fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush mmx fxsr sse sse2 ss ht syscall nx pdpe1gb rdtscp lm constant_tsc rep_good nopl xtopology tsc_reliable nonstop_tsc cpuid aperfmperf tsc_known_freq pni pclmulqdq vmx ssse3 fma cx16 pcid sse4_1 sse4_2 x2apic movbe popcnt tsc_deadline_timer aes xsave avx f16c rdrand hypervisor lahf_lm abm 3dnowprefetch tpr_shadow ept vpid fsgsbase tsc_adjust bmi1 hle avx2 smep bmi2 erms invpcid rtm avx512f avx512dq rdseed adx smap avx512ifma clflushopt clwb avx512cd sha_ni avx512bw avx512vl xsaveopt xsavec xgetbv1 xsaves vnmi avx512vbmi umip avx512_vbmi2 gfni vaes vpclmulqdq avx512_vnni avx512_bitalg avx512_vpopcntdq la57 rdpid fsrm arch_capabilities
    Virtualization:                          VT-x
    Hypervisor vendor:                       Microsoft
    Virtualization type:                     full
    L1d cache:                               96 KiB (2 instances)
    L1i cache:                               64 KiB (2 instances)
    L2 cache:                                4 MiB (2 instances)
    L3 cache:                                260 MiB (1 instance)
    NUMA node(s):                            1
    NUMA node0 CPU(s):                       0-3
    Vulnerability Gather data sampling:      Not affected
    Vulnerability Ghostwrite:                Not affected
    Vulnerability Indirect target selection: Mitigation; Aligned branch/return thunks
    Vulnerability Itlb multihit:             Not affected
    Vulnerability L1tf:                      Not affected
    Vulnerability Mds:                       Not affected
    Vulnerability Meltdown:                  Not affected
    Vulnerability Mmio stale data:           Not affected
    Vulnerability Old microcode:             Not affected
    Vulnerability Reg file data sampling:    Not affected
    Vulnerability Retbleed:                  Vulnerable
    Vulnerability Spec rstack overflow:      Not affected
    Vulnerability Spec store bypass:         Vulnerable
    Vulnerability Spectre v1:                Mitigation; usercopy/swapgs barriers and __user pointer sanitization
    Vulnerability Spectre v2:                Mitigation; Retpolines; STIBP disabled; RSB filling; PBRSB-eIBRS Not affected; BHI Retpoline
    Vulnerability Srbds:                     Not affected
    Vulnerability Tsa:                       Not affected
    Vulnerability Tsx async abort:           Vulnerable: Clear CPU buffers attempted, no microcode; SMT Host state unknown
    Vulnerability Vmscape:                   Not affected
    

| Cpu Property       | Value                                                      |
|:------------------ |:---------------------------------------------------------- |
| Brand              | INTEL(R) XEON(R) PLATINUM 8573C                            |
| Vendor             | :Intel                                                     |
| Architecture       | :UnknownIntel                                              |
| Model              | Family: 0x06, Model: 0xcf, Stepping: 0x02, Type: 0x00      |
| Cores              | 2 physical cores, 4 logical cores (on executing CPU)       |
|                    | Hyperthreading hardware capability detected                |
| Clock Frequencies  | Not supported by CPU                                       |
| Data Cache         | Level 1:3 : (48, 2048, 266240) kbytes                      |
|                    | 64 byte cache line size                                    |
| Address Size       | 57 bits virtual, 48 bits physical                          |
| SIMD               | 512 bit = 64 byte max. SIMD vector size                    |
| Time Stamp Counter | TSC is accessible via `rdtsc`                              |
|                    | TSC runs at constant rate (invariant from clock frequency) |
| Perf. Monitoring   | Performance Monitoring Counters (PMC) are not supported    |
| Hypervisor         | Yes, Microsoft                                             |

