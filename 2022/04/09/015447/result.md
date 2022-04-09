# Multi-thread benchmark result

* Pull request commit: [`4735a2746345b6ecaf79e69217e780fde5bc2dc3`](https://github.com/JuliaFolds/Transducers.jl/commit/4735a2746345b6ecaf79e69217e780fde5bc2dc3)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/243> (Update */Manifest.toml)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 9 Apr 2022 - 01:49
    - Baseline: 9 Apr 2022 - 01:54
* Package commits:
    - Target: 09cd80
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
| `["findfirst", "n=1000", "reduce", "basesize=128"]` |                1.62 (5%) :x: |                1.52 (1%) :x: |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 0.91 (5%) :white_check_mark: | 0.95 (1%) :white_check_mark: |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 0.77 (5%) :white_check_mark: | 0.75 (1%) :white_check_mark: |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  |                   1.02 (5%)  |                1.01 (1%) :x: |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 0.92 (5%) :white_check_mark: | 0.93 (1%) :white_check_mark: |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |                1.36 (5%) :x: |                1.19 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |                1.96 (5%) :x: |                1.59 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 0.84 (5%) :white_check_mark: | 0.94 (1%) :white_check_mark: |
| `["parallel_histogram", "comm", "basesize=16384"]`  | 0.87 (5%) :white_check_mark: | 0.98 (1%) :white_check_mark: |
| `["parallel_histogram", "comm", "basesize=8192"]`   | 0.88 (5%) :white_check_mark: | 0.99 (1%) :white_check_mark: |
| `["splitby", "count", "man"]`                       |                1.23 (5%) :x: |                   1.00 (1%)  |
| `["splitby", "count", "reduce"]`                    |                1.05 (5%) :x: |                1.04 (1%) :x: |

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
       #1  2593 MHz       4849 s          1 s        254 s       3357 s          0 s
       #2  2593 MHz       5489 s          1 s        234 s       2754 s          0 s
       
  Memory: 6.783611297607422 GB (3378.91796875 MB free)
  Uptime: 851.99 sec
  Load Avg:  1.6  1.51  0.93
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
       #1  2593 MHz       6949 s          1 s        336 s       4348 s          0 s
       #2  2593 MHz       8191 s          1 s        301 s       3162 s          0 s
       
  Memory: 6.783611297607422 GB (3333.2265625 MB free)
  Uptime: 1170.04 sec
  Load Avg:  1.63  1.56  1.12
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, skylake-avx512)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 9 Apr 2022 - 1:49
* Package commit: 09cd80
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
| `["collect", "assoc", "basesize=1"]`                | 245.503 ms (5%) |         |   25.97 MiB (1%) |      306784 |
| `["collect", "assoc", "basesize=1024"]`             | 198.053 ms (5%) |         |    2.61 MiB (1%) |         456 |
| `["collect", "assoc", "basesize=32"]`               | 199.913 ms (5%) |         |    4.82 MiB (1%) |       11711 |
| `["collect", "seq"]`                                | 394.965 ms (5%) |         |  812.73 KiB (1%) |          11 |
| `["collect", "unordered", "basesize=1"]`            | 339.512 ms (5%) |         |   23.73 MiB (1%) |      407526 |
| `["collect", "unordered", "basesize=1024"]`         | 214.628 ms (5%) |         | 1001.89 KiB (1%) |         965 |
| `["collect", "unordered", "basesize=32"]`           | 222.624 ms (5%) |         |    1.58 MiB (1%) |       14793 |
| `["findfirst", "n=1000", "foldl"]`                  | 628.742 ms (5%) |         |                  |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 553.942 ms (5%) |         |  353.95 KiB (1%) |        4982 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 421.614 ms (5%) |         |  157.20 KiB (1%) |        2193 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 431.167 ms (5%) |         |   81.42 KiB (1%) |        1149 |
| `["findfirst", "n=400", "foldl"]`                   | 471.866 ms (5%) |         |                  |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 250.411 ms (5%) |         |  387.89 KiB (1%) |        5517 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 247.857 ms (5%) |         |  200.89 KiB (1%) |        2874 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 355.437 ms (5%) |         |  150.17 KiB (1%) |        2159 |
| `["findfirst", "n=500", "foldl"]`                   |  81.858 ms (5%) |         |                  |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 199.082 ms (5%) |         |  257.55 KiB (1%) |        3593 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 150.764 ms (5%) |         |  118.75 KiB (1%) |        1632 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  83.439 ms (5%) |         |   49.62 KiB (1%) |         672 |
| `["overhead", "default"]`                           |  77.701 μs (5%) |         |   32.70 KiB (1%) |         417 |
| `["overhead", "stoppable=false"]`                   |  76.201 μs (5%) |         |   32.75 KiB (1%) |         418 |
| `["overhead", "stoppable=true"]`                    |  86.201 μs (5%) |         |   44.25 KiB (1%) |         610 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   3.255 ms (5%) |         |  728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   3.908 ms (5%) |         |    1.79 MiB (1%) |         216 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   3.606 ms (5%) |         |    1.42 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  15.738 ms (5%) |         |    1.54 MiB (1%) |        1266 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  24.554 ms (5%) |         |    1.26 MiB (1%) |        7356 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  20.199 ms (5%) |         |    1.27 MiB (1%) |        2827 |
| `["parallel_histogram", "seq"]`                     |   5.805 ms (5%) |         |  364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  35.198 ms (5%) |         |                  |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  17.593 ms (5%) |         |   704 bytes (1%) |          10 |
| `["splitby", "count", "foldl"]`                     |   2.295 ms (5%) |         |                  |             |
| `["splitby", "count", "man"]`                       |   1.752 ms (5%) |         |                  |             |
| `["splitby", "count", "reduce"]`                    |   1.142 ms (5%) |         |    1.09 KiB (1%) |          19 |
| `["sum", "random", "foldl"]`                        |  16.252 ms (5%) |         |                  |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   8.180 ms (5%) |         |   74.20 KiB (1%) |        1105 |
| `["sum", "random", "reduce", "basesize=256"]`       |   8.088 ms (5%) |         |   36.73 KiB (1%) |         546 |
| `["sum", "random", "reduce", "basesize=512"]`       |   8.027 ms (5%) |         |   18.05 KiB (1%) |         268 |
| `["sum", "uniform", "foldl"]`                       |  15.677 ms (5%) |         |                  |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   7.971 ms (5%) |         |   74.02 KiB (1%) |        1099 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   7.865 ms (5%) |         |   36.77 KiB (1%) |         547 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   7.826 ms (5%) |         |   18.00 KiB (1%) |         267 |
| `["sum", "valley", "foldl"]`                        |  16.143 ms (5%) |         |                  |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   8.216 ms (5%) |         |   74.11 KiB (1%) |        1102 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   8.126 ms (5%) |         |   36.70 KiB (1%) |         545 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   8.105 ms (5%) |         |   18.03 KiB (1%) |         268 |
| `["words", "nthreads=1"]`                           |  22.760 ms (5%) |         |   31.69 MiB (1%) |     1032878 |
| `["words", "nthreads=2"]`                           |  14.226 ms (5%) |         |   32.05 MiB (1%) |     1032914 |
| `["words", "nthreads=4"]`                           |  14.464 ms (5%) |         |   32.94 MiB (1%) |     1033072 |

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
       #1  2593 MHz       4849 s          1 s        254 s       3357 s          0 s
       #2  2593 MHz       5489 s          1 s        234 s       2754 s          0 s
       
  Memory: 6.783611297607422 GB (3378.91796875 MB free)
  Uptime: 851.99 sec
  Load Avg:  1.6  1.51  0.93
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, skylake-avx512)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 9 Apr 2022 - 1:54
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
| `["collect", "assoc", "basesize=1"]`                | 244.973 ms (5%) |         |   25.97 MiB (1%) |      306857 |
| `["collect", "assoc", "basesize=1024"]`             | 198.548 ms (5%) |         |    2.61 MiB (1%) |         456 |
| `["collect", "assoc", "basesize=32"]`               | 199.975 ms (5%) |         |    4.82 MiB (1%) |       11714 |
| `["collect", "seq"]`                                | 394.993 ms (5%) |         |  812.73 KiB (1%) |          11 |
| `["collect", "unordered", "basesize=1"]`            | 341.551 ms (5%) |         |   23.85 MiB (1%) |      411254 |
| `["collect", "unordered", "basesize=1024"]`         | 213.527 ms (5%) |         | 1004.52 KiB (1%) |        1016 |
| `["collect", "unordered", "basesize=32"]`           | 223.682 ms (5%) |         |    1.59 MiB (1%) |       14848 |
| `["findfirst", "n=1000", "foldl"]`                  | 624.170 ms (5%) |         |                  |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 342.341 ms (5%) |         |  232.86 KiB (1%) |        3276 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 464.634 ms (5%) |         |  166.30 KiB (1%) |        2323 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 560.606 ms (5%) |         |  108.55 KiB (1%) |        1509 |
| `["findfirst", "n=400", "foldl"]`                   | 468.507 ms (5%) |         |                  |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 246.386 ms (5%) |         |  382.70 KiB (1%) |        5459 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 246.428 ms (5%) |         |  200.86 KiB (1%) |        2873 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 387.245 ms (5%) |         |  160.92 KiB (1%) |        2327 |
| `["findfirst", "n=500", "foldl"]`                   |  81.218 ms (5%) |         |                  |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 146.398 ms (5%) |         |  216.34 KiB (1%) |        2968 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |  76.802 ms (5%) |         |   74.61 KiB (1%) |        1014 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  99.734 ms (5%) |         |   52.86 KiB (1%) |         722 |
| `["overhead", "default"]`                           |  78.901 μs (5%) |         |   32.73 KiB (1%) |         418 |
| `["overhead", "stoppable=false"]`                   |  76.601 μs (5%) |         |   32.72 KiB (1%) |         417 |
| `["overhead", "stoppable=true"]`                    |  85.601 μs (5%) |         |   44.25 KiB (1%) |         610 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   3.213 ms (5%) |         |  728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   3.859 ms (5%) |         |    1.79 MiB (1%) |         215 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   3.554 ms (5%) |         |    1.42 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  18.054 ms (5%) |         |    1.57 MiB (1%) |        2268 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  25.219 ms (5%) |         |    1.25 MiB (1%) |        7171 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  22.957 ms (5%) |         |    1.29 MiB (1%) |        4721 |
| `["parallel_histogram", "seq"]`                     |   5.741 ms (5%) |         |  364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  35.210 ms (5%) |         |                  |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  17.564 ms (5%) |         |   704 bytes (1%) |          10 |
| `["splitby", "count", "foldl"]`                     |   2.286 ms (5%) |         |                  |             |
| `["splitby", "count", "man"]`                       |   1.419 ms (5%) |         |                  |             |
| `["splitby", "count", "reduce"]`                    |   1.087 ms (5%) |         |    1.05 KiB (1%) |          19 |
| `["sum", "random", "foldl"]`                        |  16.076 ms (5%) |         |                  |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   8.135 ms (5%) |         |   73.98 KiB (1%) |        1098 |
| `["sum", "random", "reduce", "basesize=256"]`       |   8.033 ms (5%) |         |   36.70 KiB (1%) |         545 |
| `["sum", "random", "reduce", "basesize=512"]`       |   7.977 ms (5%) |         |   18.08 KiB (1%) |         269 |
| `["sum", "uniform", "foldl"]`                       |  15.731 ms (5%) |         |                  |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   7.961 ms (5%) |         |   74.17 KiB (1%) |        1104 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   7.874 ms (5%) |         |   36.67 KiB (1%) |         544 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   7.803 ms (5%) |         |   18.00 KiB (1%) |         267 |
| `["sum", "valley", "foldl"]`                        |  16.069 ms (5%) |         |                  |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   8.199 ms (5%) |         |   74.11 KiB (1%) |        1102 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   8.104 ms (5%) |         |   36.77 KiB (1%) |         547 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   8.055 ms (5%) |         |   18.03 KiB (1%) |         268 |
| `["words", "nthreads=1"]`                           |  22.849 ms (5%) |         |   31.59 MiB (1%) |     1028954 |
| `["words", "nthreads=2"]`                           |  14.535 ms (5%) |         |   31.94 MiB (1%) |     1028990 |
| `["words", "nthreads=4"]`                           |  15.100 ms (5%) |         |   32.66 MiB (1%) |     1029095 |

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
       #1  2593 MHz       6949 s          1 s        336 s       4348 s          0 s
       #2  2593 MHz       8191 s          1 s        301 s       3162 s          0 s
       
  Memory: 6.783611297607422 GB (3333.2265625 MB free)
  Uptime: 1170.04 sec
  Load Avg:  1.63  1.56  1.12
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

