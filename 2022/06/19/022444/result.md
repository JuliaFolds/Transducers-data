# Multi-thread benchmark result

* Pull request commit: [`6cb8b71b42bf8a3582f9cb8f1af7fd235eb28a74`](https://github.com/JuliaFolds/Transducers.jl/commit/6cb8b71b42bf8a3582f9cb8f1af7fd235eb28a74)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/243> (Update */Manifest.toml)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 19 Jun 2022 - 02:19
    - Baseline: 19 Jun 2022 - 02:24
* Package commits:
    - Target: 5c9a4a
    - Baseline: 6125fe
* Julia commits:
    - Target: 742b9a
    - Baseline: 742b9a
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
| `["collect", "unordered", "basesize=1"]`            |                   1.02 (5%)  |                1.01 (1%) :x: |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 0.73 (5%) :white_check_mark: | 0.79 (1%) :white_check_mark: |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  |                   1.01 (5%)  |                1.03 (1%) :x: |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  |                1.24 (5%) :x: |                1.04 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |                1.16 (5%) :x: |                1.03 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 0.94 (5%) :white_check_mark: | 0.92 (1%) :white_check_mark: |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |                1.34 (5%) :x: |                1.12 (1%) :x: |
| `["parallel_histogram", "comm", "basesize=16384"]`  | 0.92 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["parallel_histogram", "comm", "basesize=8192"]`   |                   0.95 (5%)  | 0.76 (1%) :white_check_mark: |
| `["splitby", "count", "reduce"]`                    |                   1.00 (5%)  | 0.99 (1%) :white_check_mark: |
| `["words", "nthreads=1"]`                           |                   0.97 (5%)  | 0.99 (1%) :white_check_mark: |
| `["words", "nthreads=2"]`                           |                   0.99 (5%)  | 0.99 (1%) :white_check_mark: |
| `["words", "nthreads=4"]`                           |                   1.03 (5%)  | 0.99 (1%) :white_check_mark: |

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
      Ubuntu 20.04.4 LTS
  uname: Linux 5.13.0-1029-azure #34~20.04.1-Ubuntu SMP Thu Jun 9 12:37:07 UTC 2022 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2593 MHz       5111 s          1 s        190 s       2358 s          0 s
       #2  2593 MHz       4938 s          1 s        197 s       2546 s          0 s
       
  Memory: 6.783603668212891 GB (3729.046875 MB free)
  Uptime: 771.64 sec
  Load Avg:  1.62  1.47  0.87
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, skylake-avx512)
```

### Baseline
```
Julia Version 1.7.3
Commit 742b9abb4d (2022-05-06 12:58 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 20.04.4 LTS
  uname: Linux 5.13.0-1029-azure #34~20.04.1-Ubuntu SMP Thu Jun 9 12:37:07 UTC 2022 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2593 MHz       7592 s          1 s        291 s       2812 s          0 s
       #2  2593 MHz       7097 s          1 s        275 s       3348 s          0 s
       
  Memory: 6.783603668212891 GB (3779.26171875 MB free)
  Uptime: 1075.92 sec
  Load Avg:  1.64  1.55  1.08
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, skylake-avx512)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 19 Jun 2022 - 2:19
* Package commit: 5c9a4a
* Julia commit: 742b9a
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
| `["collect", "assoc", "basesize=1"]`                | 218.669 ms (5%) |         |   25.97 MiB (1%) |      306821 |
| `["collect", "assoc", "basesize=1024"]`             | 174.961 ms (5%) |         |    2.61 MiB (1%) |         455 |
| `["collect", "assoc", "basesize=32"]`               | 176.853 ms (5%) |         |    4.82 MiB (1%) |       11705 |
| `["collect", "seq"]`                                | 348.446 ms (5%) |         |  812.73 KiB (1%) |          11 |
| `["collect", "unordered", "basesize=1"]`            | 312.456 ms (5%) |         |   23.92 MiB (1%) |      413657 |
| `["collect", "unordered", "basesize=1024"]`         | 186.816 ms (5%) |         | 1001.45 KiB (1%) |        1011 |
| `["collect", "unordered", "basesize=32"]`           | 197.661 ms (5%) |         |    1.59 MiB (1%) |       14937 |
| `["findfirst", "n=1000", "foldl"]`                  | 551.005 ms (5%) |         |                  |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 299.390 ms (5%) |         |  231.58 KiB (1%) |        3263 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 371.193 ms (5%) |         |  157.20 KiB (1%) |        2193 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 495.993 ms (5%) |         |  108.55 KiB (1%) |        1509 |
| `["findfirst", "n=400", "foldl"]`                   | 413.386 ms (5%) |         |                  |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 218.857 ms (5%) |         |  388.70 KiB (1%) |        5526 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 218.017 ms (5%) |         |  200.83 KiB (1%) |        2872 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 309.163 ms (5%) |         |  144.55 KiB (1%) |        2074 |
| `["findfirst", "n=500", "foldl"]`                   |  71.600 ms (5%) |         |                  |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 176.711 ms (5%) |         |  257.52 KiB (1%) |        3592 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |  65.424 ms (5%) |         |   72.80 KiB (1%) |         993 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  97.575 ms (5%) |         |   56.84 KiB (1%) |         779 |
| `["overhead", "default"]`                           |  70.101 μs (5%) |         |   32.70 KiB (1%) |         417 |
| `["overhead", "stoppable=false"]`                   |  69.901 μs (5%) |         |   32.75 KiB (1%) |         418 |
| `["overhead", "stoppable=true"]`                    |  81.601 μs (5%) |         |   44.19 KiB (1%) |         608 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   2.844 ms (5%) |         |  728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   3.427 ms (5%) |         |    1.79 MiB (1%) |         216 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   3.146 ms (5%) |         |    1.42 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  16.826 ms (5%) |         |    1.59 MiB (1%) |        2666 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  23.970 ms (5%) |         |    1.24 MiB (1%) |        6778 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  21.442 ms (5%) |         |    1.28 MiB (1%) |        4974 |
| `["parallel_histogram", "seq"]`                     |   5.064 ms (5%) |         |  364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  31.062 ms (5%) |         |                  |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  15.556 ms (5%) |         |   736 bytes (1%) |          11 |
| `["splitby", "count", "foldl"]`                     |   1.927 ms (5%) |         |                  |             |
| `["splitby", "count", "man"]`                       |   1.251 ms (5%) |         |                  |             |
| `["splitby", "count", "reduce"]`                    | 957.912 μs (5%) |         |    1.03 KiB (1%) |          18 |
| `["sum", "random", "foldl"]`                        |  14.283 ms (5%) |         |                  |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   7.205 ms (5%) |         |   74.14 KiB (1%) |        1103 |
| `["sum", "random", "reduce", "basesize=256"]`       |   7.103 ms (5%) |         |   36.70 KiB (1%) |         545 |
| `["sum", "random", "reduce", "basesize=512"]`       |   7.073 ms (5%) |         |   18.05 KiB (1%) |         268 |
| `["sum", "uniform", "foldl"]`                       |  13.852 ms (5%) |         |                  |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   7.046 ms (5%) |         |   74.14 KiB (1%) |        1103 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   6.945 ms (5%) |         |   36.70 KiB (1%) |         545 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   6.891 ms (5%) |         |   18.00 KiB (1%) |         267 |
| `["sum", "valley", "foldl"]`                        |  14.170 ms (5%) |         |                  |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   7.257 ms (5%) |         |   74.08 KiB (1%) |        1101 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   7.121 ms (5%) |         |   36.70 KiB (1%) |         545 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   7.124 ms (5%) |         |   18.03 KiB (1%) |         268 |
| `["words", "nthreads=1"]`                           |  21.262 ms (5%) |         |   31.37 MiB (1%) |     1021780 |
| `["words", "nthreads=2"]`                           |  12.953 ms (5%) |         |   31.73 MiB (1%) |     1021826 |
| `["words", "nthreads=4"]`                           |  13.443 ms (5%) |         |   32.44 MiB (1%) |     1021902 |

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
      Ubuntu 20.04.4 LTS
  uname: Linux 5.13.0-1029-azure #34~20.04.1-Ubuntu SMP Thu Jun 9 12:37:07 UTC 2022 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2593 MHz       5111 s          1 s        190 s       2358 s          0 s
       #2  2593 MHz       4938 s          1 s        197 s       2546 s          0 s
       
  Memory: 6.783603668212891 GB (3729.046875 MB free)
  Uptime: 771.64 sec
  Load Avg:  1.62  1.47  0.87
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, skylake-avx512)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 19 Jun 2022 - 2:24
* Package commit: 6125fe
* Julia commit: 742b9a
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
| `["collect", "assoc", "basesize=1"]`                | 217.120 ms (5%) |         |  25.97 MiB (1%) |      306789 |
| `["collect", "assoc", "basesize=1024"]`             | 175.248 ms (5%) |         |   2.61 MiB (1%) |         456 |
| `["collect", "assoc", "basesize=32"]`               | 177.023 ms (5%) |         |   4.82 MiB (1%) |       11715 |
| `["collect", "seq"]`                                | 348.677 ms (5%) |         | 812.73 KiB (1%) |          11 |
| `["collect", "unordered", "basesize=1"]`            | 307.658 ms (5%) |         |  23.59 MiB (1%) |      402781 |
| `["collect", "unordered", "basesize=1024"]`         | 187.916 ms (5%) |         | 999.61 KiB (1%) |         982 |
| `["collect", "unordered", "basesize=32"]`           | 203.643 ms (5%) |         |   1.59 MiB (1%) |       14852 |
| `["findfirst", "n=1000", "foldl"]`                  | 555.402 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 303.534 ms (5%) |         | 230.61 KiB (1%) |        3249 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 505.277 ms (5%) |         | 197.83 KiB (1%) |        2761 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 498.216 ms (5%) |         | 108.55 KiB (1%) |        1509 |
| `["findfirst", "n=400", "foldl"]`                   | 416.764 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 217.203 ms (5%) |         | 378.92 KiB (1%) |        5414 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 215.285 ms (5%) |         | 199.92 KiB (1%) |        2857 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 250.152 ms (5%) |         | 139.06 KiB (1%) |        1953 |
| `["findfirst", "n=500", "foldl"]`                   |  72.282 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 152.530 ms (5%) |         | 250.42 KiB (1%) |        3442 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |  69.290 ms (5%) |         |  78.97 KiB (1%) |        1065 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  72.753 ms (5%) |         |  50.72 KiB (1%) |         677 |
| `["overhead", "default"]`                           |  69.301 μs (5%) |         |  32.73 KiB (1%) |         418 |
| `["overhead", "stoppable=false"]`                   |  68.201 μs (5%) |         |  32.75 KiB (1%) |         418 |
| `["overhead", "stoppable=true"]`                    |  78.801 μs (5%) |         |  44.28 KiB (1%) |         611 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   2.850 ms (5%) |         | 728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   3.404 ms (5%) |         |   1.79 MiB (1%) |         216 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   3.149 ms (5%) |         |   1.42 MiB (1%) |         118 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  18.263 ms (5%) |         |   1.59 MiB (1%) |        2865 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  24.552 ms (5%) |         |   1.24 MiB (1%) |        6948 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  22.520 ms (5%) |         |   1.68 MiB (1%) |        5677 |
| `["parallel_histogram", "seq"]`                     |   5.078 ms (5%) |         | 364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  31.009 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  15.500 ms (5%) |         |  736 bytes (1%) |          11 |
| `["splitby", "count", "foldl"]`                     |   1.984 ms (5%) |         |                 |             |
| `["splitby", "count", "man"]`                       |   1.252 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    | 959.017 μs (5%) |         |   1.05 KiB (1%) |          19 |
| `["sum", "random", "foldl"]`                        |  14.358 ms (5%) |         |                 |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   7.249 ms (5%) |         |  74.11 KiB (1%) |        1102 |
| `["sum", "random", "reduce", "basesize=256"]`       |   7.161 ms (5%) |         |  36.77 KiB (1%) |         547 |
| `["sum", "random", "reduce", "basesize=512"]`       |   7.116 ms (5%) |         |  18.08 KiB (1%) |         269 |
| `["sum", "uniform", "foldl"]`                       |  13.876 ms (5%) |         |                 |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   7.043 ms (5%) |         |  74.14 KiB (1%) |        1103 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   6.962 ms (5%) |         |  36.73 KiB (1%) |         546 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   6.890 ms (5%) |         |  18.03 KiB (1%) |         268 |
| `["sum", "valley", "foldl"]`                        |  14.226 ms (5%) |         |                 |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   7.256 ms (5%) |         |  74.08 KiB (1%) |        1101 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   7.188 ms (5%) |         |  36.73 KiB (1%) |         546 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   7.159 ms (5%) |         |  18.03 KiB (1%) |         268 |
| `["words", "nthreads=1"]`                           |  21.935 ms (5%) |         |  31.75 MiB (1%) |     1034294 |
| `["words", "nthreads=2"]`                           |  13.114 ms (5%) |         |  32.11 MiB (1%) |     1034366 |
| `["words", "nthreads=4"]`                           |  13.081 ms (5%) |         |  32.82 MiB (1%) |     1034454 |

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
      Ubuntu 20.04.4 LTS
  uname: Linux 5.13.0-1029-azure #34~20.04.1-Ubuntu SMP Thu Jun 9 12:37:07 UTC 2022 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2593 MHz       7592 s          1 s        291 s       2812 s          0 s
       #2  2593 MHz       7097 s          1 s        275 s       3348 s          0 s
       
  Memory: 6.783603668212891 GB (3779.26171875 MB free)
  Uptime: 1075.92 sec
  Load Avg:  1.64  1.55  1.08
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

