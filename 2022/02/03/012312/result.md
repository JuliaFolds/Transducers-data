# Multi-thread benchmark result

* Pull request commit: [`77e3d33b3ba80c26c32c877ac61e7432a0e228e5`](https://github.com/JuliaFolds/Transducers.jl/commit/77e3d33b3ba80c26c32c877ac61e7432a0e228e5)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/243> (Update */Manifest.toml)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 3 Feb 2022 - 01:17
    - Baseline: 3 Feb 2022 - 01:22
* Package commits:
    - Target: 401e1f
    - Baseline: 673f9b
* Julia commits:
    - Target: ac5cc9
    - Baseline: ac5cc9
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
| `["collect", "unordered", "basesize=1"]`            |                   1.01 (5%)  | 0.99 (1%) :white_check_mark: |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` |                2.56 (5%) :x: |                2.48 (1%) :x: |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` |                   1.01 (5%)  |                1.02 (1%) :x: |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 0.94 (5%) :white_check_mark: | 0.96 (1%) :white_check_mark: |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 0.80 (5%) :white_check_mark: | 0.81 (1%) :white_check_mark: |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 0.67 (5%) :white_check_mark: | 0.69 (1%) :white_check_mark: |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |                   0.99 (5%)  |                1.09 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |                1.17 (5%) :x: |                1.13 (1%) :x: |
| `["parallel_histogram", "comm", "basesize=4096"]`   | 0.92 (5%) :white_check_mark: | 0.96 (1%) :white_check_mark: |
| `["parallel_histogram", "comm", "basesize=8192"]`   | 0.87 (5%) :white_check_mark: | 0.74 (1%) :white_check_mark: |
| `["splitby", "count", "foldl"]`                     | 0.95 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["splitby", "count", "man"]`                       | 0.81 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["splitby", "count", "reduce"]`                    | 0.92 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["words", "nthreads=2"]`                           |                   1.03 (5%)  |                1.01 (1%) :x: |

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
Julia Version 1.7.1
Commit ac5cc99908 (2021-12-22 19:35 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 20.04.3 LTS
  uname: Linux 5.11.0-1027-azure #30~20.04.1-Ubuntu SMP Wed Jan 12 20:56:50 UTC 2022 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2593 MHz       5228 s          1 s        302 s       1814 s          0 s
       #2  2593 MHz       5110 s          1 s        269 s       1964 s          0 s
       
  Memory: 6.788978576660156 GB (3662.27734375 MB free)
  Uptime: 739.58 sec
  Load Avg:  1.68  1.5  0.9
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, skylake-avx512)
```

### Baseline
```
Julia Version 1.7.1
Commit ac5cc99908 (2021-12-22 19:35 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 20.04.3 LTS
  uname: Linux 5.11.0-1027-azure #30~20.04.1-Ubuntu SMP Wed Jan 12 20:56:50 UTC 2022 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2593 MHz       7605 s          1 s        373 s       2565 s          0 s
       #2  2593 MHz       7604 s          1 s        331 s       2607 s          0 s
       
  Memory: 6.788978576660156 GB (3425.9765625 MB free)
  Uptime: 1060.12 sec
  Load Avg:  1.53  1.53  1.09
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, skylake-avx512)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 3 Feb 2022 - 1:17
* Package commit: 401e1f
* Julia commit: ac5cc9
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
| `["collect", "assoc", "basesize=1"]`                | 246.359 ms (5%) |         |   25.97 MiB (1%) |      306833 |
| `["collect", "assoc", "basesize=1024"]`             | 198.295 ms (5%) |         |    2.61 MiB (1%) |         455 |
| `["collect", "assoc", "basesize=32"]`               | 200.494 ms (5%) |         |    4.82 MiB (1%) |       11710 |
| `["collect", "seq"]`                                | 394.971 ms (5%) |         |  812.73 KiB (1%) |          11 |
| `["collect", "unordered", "basesize=1"]`            | 353.241 ms (5%) |         |   23.56 MiB (1%) |      401823 |
| `["collect", "unordered", "basesize=1024"]`         | 213.912 ms (5%) |         | 1000.52 KiB (1%) |         921 |
| `["collect", "unordered", "basesize=32"]`           | 232.464 ms (5%) |         |    1.58 MiB (1%) |       14749 |
| `["findfirst", "n=1000", "foldl"]`                  | 626.719 ms (5%) |         |                  |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 883.432 ms (5%) |         |  577.33 KiB (1%) |        8049 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 498.716 ms (5%) |         |  178.25 KiB (1%) |        2483 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 561.303 ms (5%) |         |  108.58 KiB (1%) |        1510 |
| `["findfirst", "n=400", "foldl"]`                   | 470.340 ms (5%) |         |                  |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 244.159 ms (5%) |         |  380.83 KiB (1%) |        5428 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 246.271 ms (5%) |         |  200.77 KiB (1%) |        2870 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 263.818 ms (5%) |         |  112.58 KiB (1%) |        1624 |
| `["findfirst", "n=500", "foldl"]`                   |  81.553 ms (5%) |         |                  |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 124.686 ms (5%) |         |  183.41 KiB (1%) |        2562 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 195.586 ms (5%) |         |  164.39 KiB (1%) |        2230 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 117.266 ms (5%) |         |   61.52 KiB (1%) |         842 |
| `["overhead", "default"]`                           |  73.901 μs (5%) |         |   32.73 KiB (1%) |         418 |
| `["overhead", "stoppable=false"]`                   |  74.601 μs (5%) |         |   32.75 KiB (1%) |         418 |
| `["overhead", "stoppable=true"]`                    |  86.601 μs (5%) |         |   44.22 KiB (1%) |         609 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   3.210 ms (5%) |         |  728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   3.860 ms (5%) |         |    1.79 MiB (1%) |         215 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   3.549 ms (5%) |         |    1.42 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  18.325 ms (5%) |         |    1.58 MiB (1%) |        2341 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  22.790 ms (5%) |         |    1.20 MiB (1%) |        5505 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  19.165 ms (5%) |         |    1.24 MiB (1%) |        3885 |
| `["parallel_histogram", "seq"]`                     |   5.729 ms (5%) |         |  364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  35.253 ms (5%) |         |                  |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  17.613 ms (5%) |         |   736 bytes (1%) |          11 |
| `["splitby", "count", "foldl"]`                     |   2.175 ms (5%) |         |                  |             |
| `["splitby", "count", "man"]`                       |   1.417 ms (5%) |         |                  |             |
| `["splitby", "count", "reduce"]`                    |   1.086 ms (5%) |         |    1.06 KiB (1%) |          18 |
| `["sum", "random", "foldl"]`                        |  16.241 ms (5%) |         |                  |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   8.155 ms (5%) |         |   74.17 KiB (1%) |        1104 |
| `["sum", "random", "reduce", "basesize=256"]`       |   8.047 ms (5%) |         |   36.70 KiB (1%) |         545 |
| `["sum", "random", "reduce", "basesize=512"]`       |   7.987 ms (5%) |         |   18.08 KiB (1%) |         269 |
| `["sum", "uniform", "foldl"]`                       |  15.755 ms (5%) |         |                  |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   7.967 ms (5%) |         |   74.17 KiB (1%) |        1104 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   7.865 ms (5%) |         |   36.67 KiB (1%) |         544 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   7.809 ms (5%) |         |   18.03 KiB (1%) |         268 |
| `["sum", "valley", "foldl"]`                        |  16.081 ms (5%) |         |                  |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   8.213 ms (5%) |         |   74.05 KiB (1%) |        1100 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   8.116 ms (5%) |         |   36.73 KiB (1%) |         546 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   8.084 ms (5%) |         |   18.03 KiB (1%) |         268 |
| `["words", "nthreads=1"]`                           |  23.237 ms (5%) |         |   31.72 MiB (1%) |     1033355 |
| `["words", "nthreads=2"]`                           |  15.154 ms (5%) |         |   32.44 MiB (1%) |     1033428 |
| `["words", "nthreads=4"]`                           |  15.140 ms (5%) |         |   32.88 MiB (1%) |     1033494 |

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
Julia Version 1.7.1
Commit ac5cc99908 (2021-12-22 19:35 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 20.04.3 LTS
  uname: Linux 5.11.0-1027-azure #30~20.04.1-Ubuntu SMP Wed Jan 12 20:56:50 UTC 2022 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2593 MHz       5228 s          1 s        302 s       1814 s          0 s
       #2  2593 MHz       5110 s          1 s        269 s       1964 s          0 s
       
  Memory: 6.788978576660156 GB (3662.27734375 MB free)
  Uptime: 739.58 sec
  Load Avg:  1.68  1.5  0.9
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, skylake-avx512)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 3 Feb 2022 - 1:22
* Package commit: 673f9b
* Julia commit: ac5cc9
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
| `["collect", "assoc", "basesize=1"]`                | 245.892 ms (5%) |         |   25.97 MiB (1%) |      306829 |
| `["collect", "assoc", "basesize=1024"]`             | 198.316 ms (5%) |         |    2.61 MiB (1%) |         456 |
| `["collect", "assoc", "basesize=32"]`               | 200.427 ms (5%) |         |    4.82 MiB (1%) |       11712 |
| `["collect", "seq"]`                                | 395.124 ms (5%) |         |  812.73 KiB (1%) |          11 |
| `["collect", "unordered", "basesize=1"]`            | 351.466 ms (5%) |         |   23.89 MiB (1%) |      412550 |
| `["collect", "unordered", "basesize=1024"]`         | 211.849 ms (5%) |         | 1002.64 KiB (1%) |         986 |
| `["collect", "unordered", "basesize=32"]`           | 223.897 ms (5%) |         |    1.58 MiB (1%) |       14671 |
| `["findfirst", "n=1000", "foldl"]`                  | 630.206 ms (5%) |         |                  |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 344.767 ms (5%) |         |  232.98 KiB (1%) |        3280 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 491.923 ms (5%) |         |  174.95 KiB (1%) |        2436 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 565.257 ms (5%) |         |  108.55 KiB (1%) |        1509 |
| `["findfirst", "n=400", "foldl"]`                   | 473.192 ms (5%) |         |                  |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 259.110 ms (5%) |         |  395.58 KiB (1%) |        5612 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 248.424 ms (5%) |         |  200.62 KiB (1%) |        2866 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 330.548 ms (5%) |         |  138.52 KiB (1%) |        1978 |
| `["findfirst", "n=500", "foldl"]`                   |  82.007 ms (5%) |         |                  |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 185.043 ms (5%) |         |  267.67 KiB (1%) |        3708 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 197.547 ms (5%) |         |  150.31 KiB (1%) |        2074 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 100.362 ms (5%) |         |   54.38 KiB (1%) |         744 |
| `["overhead", "default"]`                           |  77.301 μs (5%) |         |   32.77 KiB (1%) |         419 |
| `["overhead", "stoppable=false"]`                   |  75.201 μs (5%) |         |   32.72 KiB (1%) |         417 |
| `["overhead", "stoppable=true"]`                    |  85.802 μs (5%) |         |   44.25 KiB (1%) |         610 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   3.252 ms (5%) |         |  728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   3.926 ms (5%) |         |    1.79 MiB (1%) |         216 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   3.597 ms (5%) |         |    1.42 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  18.177 ms (5%) |         |    1.58 MiB (1%) |        2428 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  24.848 ms (5%) |         |    1.25 MiB (1%) |        7037 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  22.126 ms (5%) |         |    1.67 MiB (1%) |        5474 |
| `["parallel_histogram", "seq"]`                     |   5.805 ms (5%) |         |  364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  35.301 ms (5%) |         |                  |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  17.607 ms (5%) |         |   736 bytes (1%) |          11 |
| `["splitby", "count", "foldl"]`                     |   2.294 ms (5%) |         |                  |             |
| `["splitby", "count", "man"]`                       |   1.754 ms (5%) |         |                  |             |
| `["splitby", "count", "reduce"]`                    |   1.176 ms (5%) |         |    1.06 KiB (1%) |          18 |
| `["sum", "random", "foldl"]`                        |  16.237 ms (5%) |         |                  |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   8.227 ms (5%) |         |   74.17 KiB (1%) |        1104 |
| `["sum", "random", "reduce", "basesize=256"]`       |   8.116 ms (5%) |         |   36.73 KiB (1%) |         546 |
| `["sum", "random", "reduce", "basesize=512"]`       |   8.056 ms (5%) |         |   18.11 KiB (1%) |         270 |
| `["sum", "uniform", "foldl"]`                       |  15.797 ms (5%) |         |                  |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   7.961 ms (5%) |         |   74.17 KiB (1%) |        1104 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   7.852 ms (5%) |         |   36.77 KiB (1%) |         547 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   7.774 ms (5%) |         |   18.00 KiB (1%) |         267 |
| `["sum", "valley", "foldl"]`                        |  16.138 ms (5%) |         |                  |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   8.253 ms (5%) |         |   74.11 KiB (1%) |        1102 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   8.162 ms (5%) |         |   36.73 KiB (1%) |         546 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   8.118 ms (5%) |         |   18.03 KiB (1%) |         268 |
| `["words", "nthreads=1"]`                           |  22.986 ms (5%) |         |   31.62 MiB (1%) |     1030198 |
| `["words", "nthreads=2"]`                           |  14.690 ms (5%) |         |   31.97 MiB (1%) |     1030234 |
| `["words", "nthreads=4"]`                           |  14.929 ms (5%) |         |   32.69 MiB (1%) |     1030307 |

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
Julia Version 1.7.1
Commit ac5cc99908 (2021-12-22 19:35 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 20.04.3 LTS
  uname: Linux 5.11.0-1027-azure #30~20.04.1-Ubuntu SMP Wed Jan 12 20:56:50 UTC 2022 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2593 MHz       7605 s          1 s        373 s       2565 s          0 s
       #2  2593 MHz       7604 s          1 s        331 s       2607 s          0 s
       
  Memory: 6.788978576660156 GB (3425.9765625 MB free)
  Uptime: 1060.12 sec
  Load Avg:  1.53  1.53  1.09
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
    CPU MHz:                         2593.905
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

