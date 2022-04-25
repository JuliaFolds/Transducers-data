# Multi-thread benchmark result

* Pull request commit: [`76ef3dbb187d50152ae9a50acd68d355d634f50f`](https://github.com/JuliaFolds/Transducers.jl/commit/76ef3dbb187d50152ae9a50acd68d355d634f50f)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/243> (Update */Manifest.toml)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 25 Apr 2022 - 02:00
    - Baseline: 25 Apr 2022 - 02:05
* Package commits:
    - Target: dd78f8
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
| `["findfirst", "n=1000", "reduce", "basesize=128"]` |                1.59 (5%) :x: |                1.55 (1%) :x: |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 0.89 (5%) :white_check_mark: | 0.86 (1%) :white_check_mark: |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` |                1.35 (5%) :x: |                1.34 (1%) :x: |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  |                   0.99 (5%)  | 0.96 (1%) :white_check_mark: |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  |                   1.02 (5%)  | 0.97 (1%) :white_check_mark: |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |                1.40 (5%) :x: |                1.25 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 0.86 (5%) :white_check_mark: | 0.86 (1%) :white_check_mark: |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |                   1.05 (5%)  |                1.15 (1%) :x: |
| `["parallel_histogram", "comm", "basesize=16384"]`  |                1.07 (5%) :x: |                   1.00 (1%)  |
| `["parallel_histogram", "comm", "basesize=4096"]`   |                   0.98 (5%)  |                1.02 (1%) :x: |
| `["parallel_histogram", "comm", "basesize=8192"]`   |                   1.02 (5%)  |                1.05 (1%) :x: |
| `["partition_length_maximum", "rand", "reduce"]`    |                   1.00 (5%)  | 0.96 (1%) :white_check_mark: |
| `["splitby", "count", "man"]`                       |                1.24 (5%) :x: |                   1.00 (1%)  |
| `["splitby", "count", "reduce"]`                    |                1.06 (5%) :x: |                1.03 (1%) :x: |
| `["words", "nthreads=4"]`                           | 0.94 (5%) :white_check_mark: | 0.99 (1%) :white_check_mark: |

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
  uname: Linux 5.13.0-1021-azure #24~20.04.1-Ubuntu SMP Tue Mar 29 15:34:22 UTC 2022 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2593 MHz       4800 s          2 s        218 s       2838 s          0 s
       #2  2593 MHz       5481 s          0 s        212 s       2187 s          0 s
       
  Memory: 6.783611297607422 GB (3826.72265625 MB free)
  Uptime: 791.79 sec
  Load Avg:  1.65  1.5  0.91
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
  uname: Linux 5.13.0-1021-azure #24~20.04.1-Ubuntu SMP Tue Mar 29 15:34:22 UTC 2022 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2593 MHz       7116 s          2 s        271 s       3533 s          0 s
       #2  2593 MHz       7912 s          0 s        276 s       2761 s          0 s
       
  Memory: 6.783611297607422 GB (3771.765625 MB free)
  Uptime: 1098.9 sec
  Load Avg:  1.73  1.61  1.13
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, skylake-avx512)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 25 Apr 2022 - 2:0
* Package commit: dd78f8
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
| `["collect", "assoc", "basesize=1"]`                | 242.804 ms (5%) |         |  25.97 MiB (1%) |      306780 |
| `["collect", "assoc", "basesize=1024"]`             | 197.956 ms (5%) |         |   2.61 MiB (1%) |         456 |
| `["collect", "assoc", "basesize=32"]`               | 199.785 ms (5%) |         |   4.82 MiB (1%) |       11705 |
| `["collect", "seq"]`                                | 394.923 ms (5%) |         | 812.73 KiB (1%) |          11 |
| `["collect", "unordered", "basesize=1"]`            | 340.812 ms (5%) |         |  23.88 MiB (1%) |      412436 |
| `["collect", "unordered", "basesize=1024"]`         | 212.271 ms (5%) |         | 999.61 KiB (1%) |         895 |
| `["collect", "unordered", "basesize=32"]`           | 222.982 ms (5%) |         |   1.58 MiB (1%) |       14718 |
| `["findfirst", "n=1000", "foldl"]`                  | 630.813 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 550.431 ms (5%) |         | 360.22 KiB (1%) |        5070 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 373.621 ms (5%) |         | 135.20 KiB (1%) |        1904 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 579.974 ms (5%) |         | 108.64 KiB (1%) |        1512 |
| `["findfirst", "n=400", "foldl"]`                   | 473.143 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 250.052 ms (5%) |         | 381.56 KiB (1%) |        5454 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 247.602 ms (5%) |         | 200.89 KiB (1%) |        2874 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 277.564 ms (5%) |         | 112.48 KiB (1%) |        1619 |
| `["findfirst", "n=500", "foldl"]`                   |  82.032 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 167.753 ms (5%) |         | 238.62 KiB (1%) |        3284 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 203.059 ms (5%) |         | 147.31 KiB (1%) |        2044 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 100.334 ms (5%) |         |  54.45 KiB (1%) |         747 |
| `["overhead", "default"]`                           |  73.701 μs (5%) |         |  32.73 KiB (1%) |         418 |
| `["overhead", "stoppable=false"]`                   |  73.601 μs (5%) |         |  32.72 KiB (1%) |         417 |
| `["overhead", "stoppable=true"]`                    |  83.001 μs (5%) |         |  44.19 KiB (1%) |         608 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   3.234 ms (5%) |         | 728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   3.993 ms (5%) |         |   2.05 MiB (1%) |         221 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   3.571 ms (5%) |         |   1.42 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  18.520 ms (5%) |         |   1.58 MiB (1%) |        2420 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  25.127 ms (5%) |         |   1.27 MiB (1%) |        7721 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  22.895 ms (5%) |         |   1.31 MiB (1%) |        5941 |
| `["parallel_histogram", "seq"]`                     |   5.766 ms (5%) |         | 364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  35.160 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  17.579 ms (5%) |         |  704 bytes (1%) |          10 |
| `["splitby", "count", "foldl"]`                     |   2.291 ms (5%) |         |                 |             |
| `["splitby", "count", "man"]`                       |   1.752 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    |   1.157 ms (5%) |         |   1.09 KiB (1%) |          19 |
| `["sum", "random", "foldl"]`                        |  16.391 ms (5%) |         |                 |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   8.232 ms (5%) |         |  74.17 KiB (1%) |        1104 |
| `["sum", "random", "reduce", "basesize=256"]`       |   8.133 ms (5%) |         |  36.70 KiB (1%) |         545 |
| `["sum", "random", "reduce", "basesize=512"]`       |   8.088 ms (5%) |         |  18.08 KiB (1%) |         269 |
| `["sum", "uniform", "foldl"]`                       |  15.684 ms (5%) |         |                 |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   7.964 ms (5%) |         |  74.17 KiB (1%) |        1104 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   7.875 ms (5%) |         |  36.70 KiB (1%) |         545 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   7.813 ms (5%) |         |  18.03 KiB (1%) |         268 |
| `["sum", "valley", "foldl"]`                        |  16.163 ms (5%) |         |                 |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   8.221 ms (5%) |         |  74.11 KiB (1%) |        1102 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   8.141 ms (5%) |         |  36.70 KiB (1%) |         545 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   8.097 ms (5%) |         |  18.00 KiB (1%) |         267 |
| `["words", "nthreads=1"]`                           |  21.409 ms (5%) |         |  31.64 MiB (1%) |     1030730 |
| `["words", "nthreads=2"]`                           |  14.057 ms (5%) |         |  32.00 MiB (1%) |     1030804 |
| `["words", "nthreads=4"]`                           |  14.360 ms (5%) |         |  32.71 MiB (1%) |     1030916 |

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
  uname: Linux 5.13.0-1021-azure #24~20.04.1-Ubuntu SMP Tue Mar 29 15:34:22 UTC 2022 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2593 MHz       4800 s          2 s        218 s       2838 s          0 s
       #2  2593 MHz       5481 s          0 s        212 s       2187 s          0 s
       
  Memory: 6.783611297607422 GB (3826.72265625 MB free)
  Uptime: 791.79 sec
  Load Avg:  1.65  1.5  0.91
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, skylake-avx512)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 25 Apr 2022 - 2:5
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
| `["collect", "assoc", "basesize=1"]`                | 244.926 ms (5%) |         |   25.97 MiB (1%) |      306818 |
| `["collect", "assoc", "basesize=1024"]`             | 198.316 ms (5%) |         |    2.61 MiB (1%) |         456 |
| `["collect", "assoc", "basesize=32"]`               | 200.233 ms (5%) |         |    4.82 MiB (1%) |       11704 |
| `["collect", "seq"]`                                | 395.013 ms (5%) |         |  812.73 KiB (1%) |          11 |
| `["collect", "unordered", "basesize=1"]`            | 338.814 ms (5%) |         |   23.92 MiB (1%) |      413795 |
| `["collect", "unordered", "basesize=1024"]`         | 211.077 ms (5%) |         | 1004.73 KiB (1%) |        1033 |
| `["collect", "unordered", "basesize=32"]`           | 222.487 ms (5%) |         |    1.59 MiB (1%) |       15080 |
| `["findfirst", "n=1000", "foldl"]`                  | 624.515 ms (5%) |         |                  |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 346.650 ms (5%) |         |  232.86 KiB (1%) |        3276 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 421.273 ms (5%) |         |  157.20 KiB (1%) |        2193 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 428.349 ms (5%) |         |   81.36 KiB (1%) |        1147 |
| `["findfirst", "n=400", "foldl"]`                   | 468.667 ms (5%) |         |                  |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 253.707 ms (5%) |         |  399.44 KiB (1%) |        5678 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 250.364 ms (5%) |         |  201.05 KiB (1%) |        2879 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 272.742 ms (5%) |         |  115.62 KiB (1%) |        1660 |
| `["findfirst", "n=500", "foldl"]`                   |  81.302 ms (5%) |         |                  |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 119.938 ms (5%) |         |  190.86 KiB (1%) |        2604 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 197.661 ms (5%) |         |  148.31 KiB (1%) |        2065 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 116.302 ms (5%) |         |   63.66 KiB (1%) |         865 |
| `["overhead", "default"]`                           |  75.701 μs (5%) |         |   32.73 KiB (1%) |         418 |
| `["overhead", "stoppable=false"]`                   |  73.301 μs (5%) |         |   32.75 KiB (1%) |         418 |
| `["overhead", "stoppable=true"]`                    |  84.501 μs (5%) |         |   44.25 KiB (1%) |         610 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   3.201 ms (5%) |         |  728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   3.818 ms (5%) |         |    1.79 MiB (1%) |         215 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   3.534 ms (5%) |         |    1.42 MiB (1%) |         118 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  17.234 ms (5%) |         |    1.58 MiB (1%) |        2464 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  25.609 ms (5%) |         |    1.24 MiB (1%) |        6818 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  22.378 ms (5%) |         |    1.25 MiB (1%) |        5713 |
| `["parallel_histogram", "seq"]`                     |   5.723 ms (5%) |         |  364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  35.141 ms (5%) |         |                  |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  17.571 ms (5%) |         |   736 bytes (1%) |          11 |
| `["splitby", "count", "foldl"]`                     |   2.251 ms (5%) |         |                  |             |
| `["splitby", "count", "man"]`                       |   1.417 ms (5%) |         |                  |             |
| `["splitby", "count", "reduce"]`                    |   1.088 ms (5%) |         |    1.06 KiB (1%) |          18 |
| `["sum", "random", "foldl"]`                        |  16.120 ms (5%) |         |                  |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   8.060 ms (5%) |         |   74.08 KiB (1%) |        1101 |
| `["sum", "random", "reduce", "basesize=256"]`       |   8.027 ms (5%) |         |   36.70 KiB (1%) |         545 |
| `["sum", "random", "reduce", "basesize=512"]`       |   7.961 ms (5%) |         |   18.11 KiB (1%) |         270 |
| `["sum", "uniform", "foldl"]`                       |  15.634 ms (5%) |         |                  |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   7.921 ms (5%) |         |   74.08 KiB (1%) |        1101 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   7.853 ms (5%) |         |   36.70 KiB (1%) |         545 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   7.794 ms (5%) |         |   18.03 KiB (1%) |         268 |
| `["sum", "valley", "foldl"]`                        |  16.073 ms (5%) |         |                  |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   8.198 ms (5%) |         |   74.14 KiB (1%) |        1103 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   8.069 ms (5%) |         |   36.70 KiB (1%) |         545 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   8.059 ms (5%) |         |   18.03 KiB (1%) |         268 |
| `["words", "nthreads=1"]`                           |  22.323 ms (5%) |         |   31.90 MiB (1%) |     1039394 |
| `["words", "nthreads=2"]`                           |  14.677 ms (5%) |         |   32.25 MiB (1%) |     1039434 |
| `["words", "nthreads=4"]`                           |  15.247 ms (5%) |         |   33.15 MiB (1%) |     1039609 |

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
  uname: Linux 5.13.0-1021-azure #24~20.04.1-Ubuntu SMP Tue Mar 29 15:34:22 UTC 2022 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2593 MHz       7116 s          2 s        271 s       3533 s          0 s
       #2  2593 MHz       7912 s          0 s        276 s       2761 s          0 s
       
  Memory: 6.783611297607422 GB (3771.765625 MB free)
  Uptime: 1098.9 sec
  Load Avg:  1.73  1.61  1.13
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
    Vulnerability Spectre v2:        Mitigation; Retpolines, STIBP disabled, RSB filling
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

