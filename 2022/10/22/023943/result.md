# Multi-thread benchmark result

* Pull request commit: [`9fc7be81a327d02ac8a15fa342ae6608b47a0d7c`](https://github.com/JuliaFolds/Transducers.jl/commit/9fc7be81a327d02ac8a15fa342ae6608b47a0d7c)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/243> (Update */Manifest.toml)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 22 Oct 2022 - 02:34
    - Baseline: 22 Oct 2022 - 02:39
* Package commits:
    - Target: 2c5f49
    - Baseline: 958213
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
| `["collect", "unordered", "basesize=1024"]`         |                   1.00 (5%)  | 0.97 (1%) :white_check_mark: |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 0.63 (5%) :white_check_mark: | 0.64 (1%) :white_check_mark: |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 0.88 (5%) :white_check_mark: | 0.86 (1%) :white_check_mark: |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  |                   0.99 (5%)  | 0.97 (1%) :white_check_mark: |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  |                1.07 (5%) :x: |                1.10 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |                1.43 (5%) :x: |                1.24 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |                1.30 (5%) :x: |                1.21 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |                   0.96 (5%)  | 0.97 (1%) :white_check_mark: |
| `["parallel_histogram", "comm", "basesize=16384"]`  |                1.35 (5%) :x: |                1.35 (1%) :x: |
| `["parallel_histogram", "comm", "basesize=8192"]`   | 0.93 (5%) :white_check_mark: |                1.05 (1%) :x: |
| `["splitby", "count", "man"]`                       | 0.81 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["splitby", "count", "reduce"]`                    | 0.92 (5%) :white_check_mark: |                   1.00 (1%)  |

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
      Ubuntu 20.04.5 LTS
  uname: Linux 5.15.0-1022-azure #27~20.04.1-Ubuntu SMP Mon Oct 17 02:03:50 UTC 2022 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2593 MHz       5978 s          2 s        215 s       1719 s          0 s
       #2  2593 MHz       4395 s          1 s        231 s       3290 s          0 s
       
  Memory: 6.78125 GB (3734.1015625 MB free)
  Uptime: 795.22 sec
  Load Avg:  1.52  1.45  0.88
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
      Ubuntu 20.04.5 LTS
  uname: Linux 5.15.0-1022-azure #27~20.04.1-Ubuntu SMP Mon Oct 17 02:03:50 UTC 2022 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2593 MHz       8149 s          2 s        280 s       2593 s          0 s
       #2  2593 MHz       7028 s          1 s        285 s       3718 s          0 s
       
  Memory: 6.78125 GB (3697.83984375 MB free)
  Uptime: 1106.87 sec
  Load Avg:  1.47  1.53  1.09
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, skylake-avx512)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 22 Oct 2022 - 2:34
* Package commit: 2c5f49
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
| `["collect", "assoc", "basesize=1"]`                | 246.373 ms (5%) |         |   25.97 MiB (1%) |      306804 |
| `["collect", "assoc", "basesize=1024"]`             | 198.401 ms (5%) |         |    2.61 MiB (1%) |         456 |
| `["collect", "assoc", "basesize=32"]`               | 200.355 ms (5%) |         |    4.82 MiB (1%) |       11720 |
| `["collect", "seq"]`                                | 395.174 ms (5%) |         |  812.73 KiB (1%) |          11 |
| `["collect", "unordered", "basesize=1"]`            | 346.861 ms (5%) |         |   23.90 MiB (1%) |      413146 |
| `["collect", "unordered", "basesize=1024"]`         | 213.208 ms (5%) |         | 1002.23 KiB (1%) |        1080 |
| `["collect", "unordered", "basesize=32"]`           | 224.003 ms (5%) |         |    1.58 MiB (1%) |       14716 |
| `["findfirst", "n=1000", "foldl"]`                  | 625.248 ms (5%) |         |                  |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 348.849 ms (5%) |         |  232.98 KiB (1%) |        3280 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 371.919 ms (5%) |         |  135.39 KiB (1%) |        1910 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 562.616 ms (5%) |         |  108.55 KiB (1%) |        1509 |
| `["findfirst", "n=400", "foldl"]`                   | 469.371 ms (5%) |         |                  |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 244.680 ms (5%) |         |  379.16 KiB (1%) |        5408 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 244.288 ms (5%) |         |  200.86 KiB (1%) |        2873 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 299.007 ms (5%) |         |  127.39 KiB (1%) |        1822 |
| `["findfirst", "n=500", "foldl"]`                   |  81.339 ms (5%) |         |                  |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 192.705 ms (5%) |         |  267.92 KiB (1%) |        3694 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 200.214 ms (5%) |         |  143.70 KiB (1%) |        2034 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 116.587 ms (5%) |         |   61.48 KiB (1%) |         839 |
| `["overhead", "default"]`                           |  76.300 μs (5%) |         |   32.77 KiB (1%) |         419 |
| `["overhead", "stoppable=false"]`                   |  75.201 μs (5%) |         |   32.75 KiB (1%) |         418 |
| `["overhead", "stoppable=true"]`                    |  87.301 μs (5%) |         |   44.25 KiB (1%) |         610 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   3.218 ms (5%) |         |  728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   3.862 ms (5%) |         |    1.79 MiB (1%) |         215 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   3.597 ms (5%) |         |    1.42 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  17.701 ms (5%) |         |    1.56 MiB (1%) |        1628 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  25.484 ms (5%) |         |    1.25 MiB (1%) |        7205 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  21.304 ms (5%) |         |    1.33 MiB (1%) |        2944 |
| `["parallel_histogram", "seq"]`                     |   5.733 ms (5%) |         |  364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  35.226 ms (5%) |         |                  |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  17.629 ms (5%) |         |   736 bytes (1%) |          11 |
| `["splitby", "count", "foldl"]`                     |   2.294 ms (5%) |         |                  |             |
| `["splitby", "count", "man"]`                       |   1.418 ms (5%) |         |                  |             |
| `["splitby", "count", "reduce"]`                    |   1.091 ms (5%) |         |    1.09 KiB (1%) |          19 |
| `["sum", "random", "foldl"]`                        |  16.194 ms (5%) |         |                  |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   8.198 ms (5%) |         |   74.11 KiB (1%) |        1102 |
| `["sum", "random", "reduce", "basesize=256"]`       |   8.106 ms (5%) |         |   36.77 KiB (1%) |         547 |
| `["sum", "random", "reduce", "basesize=512"]`       |   8.029 ms (5%) |         |   18.08 KiB (1%) |         269 |
| `["sum", "uniform", "foldl"]`                       |  15.757 ms (5%) |         |                  |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   8.024 ms (5%) |         |   74.20 KiB (1%) |        1105 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   7.916 ms (5%) |         |   36.77 KiB (1%) |         547 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   7.837 ms (5%) |         |   18.03 KiB (1%) |         268 |
| `["sum", "valley", "foldl"]`                        |  16.055 ms (5%) |         |                  |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   8.202 ms (5%) |         |   74.14 KiB (1%) |        1103 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   8.117 ms (5%) |         |   36.70 KiB (1%) |         545 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   8.114 ms (5%) |         |   18.03 KiB (1%) |         268 |
| `["words", "nthreads=1"]`                           |  23.418 ms (5%) |         |   31.57 MiB (1%) |     1028643 |
| `["words", "nthreads=2"]`                           |  14.427 ms (5%) |         |   32.28 MiB (1%) |     1028729 |
| `["words", "nthreads=4"]`                           |  14.659 ms (5%) |         |   32.91 MiB (1%) |     1028860 |

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
      Ubuntu 20.04.5 LTS
  uname: Linux 5.15.0-1022-azure #27~20.04.1-Ubuntu SMP Mon Oct 17 02:03:50 UTC 2022 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2593 MHz       5978 s          2 s        215 s       1719 s          0 s
       #2  2593 MHz       4395 s          1 s        231 s       3290 s          0 s
       
  Memory: 6.78125 GB (3734.1015625 MB free)
  Uptime: 795.22 sec
  Load Avg:  1.52  1.45  0.88
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, skylake-avx512)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 22 Oct 2022 - 2:39
* Package commit: 958213
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
| `["collect", "assoc", "basesize=1"]`                | 245.713 ms (5%) |         |  25.97 MiB (1%) |      306761 |
| `["collect", "assoc", "basesize=1024"]`             | 198.816 ms (5%) |         |   2.61 MiB (1%) |         456 |
| `["collect", "assoc", "basesize=32"]`               | 200.606 ms (5%) |         |   4.82 MiB (1%) |       11705 |
| `["collect", "seq"]`                                | 395.233 ms (5%) |         | 812.73 KiB (1%) |          11 |
| `["collect", "unordered", "basesize=1"]`            | 348.465 ms (5%) |         |  23.91 MiB (1%) |      413258 |
| `["collect", "unordered", "basesize=1024"]`         | 212.160 ms (5%) |         |   1.01 MiB (1%) |        1042 |
| `["collect", "unordered", "basesize=32"]`           | 223.885 ms (5%) |         |   1.59 MiB (1%) |       14841 |
| `["findfirst", "n=1000", "foldl"]`                  | 625.238 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 555.570 ms (5%) |         | 364.14 KiB (1%) |        5102 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 421.797 ms (5%) |         | 157.20 KiB (1%) |        2193 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 561.532 ms (5%) |         | 108.55 KiB (1%) |        1509 |
| `["findfirst", "n=400", "foldl"]`                   | 469.206 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 246.971 ms (5%) |         | 391.94 KiB (1%) |        5570 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 249.229 ms (5%) |         | 200.95 KiB (1%) |        2876 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 279.430 ms (5%) |         | 115.67 KiB (1%) |        1664 |
| `["findfirst", "n=500", "foldl"]`                   |  81.324 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 134.594 ms (5%) |         | 215.86 KiB (1%) |        2944 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 154.232 ms (5%) |         | 118.80 KiB (1%) |        1636 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 122.049 ms (5%) |         |  63.70 KiB (1%) |         867 |
| `["overhead", "default"]`                           |  76.201 μs (5%) |         |  32.73 KiB (1%) |         418 |
| `["overhead", "stoppable=false"]`                   |  76.600 μs (5%) |         |  32.75 KiB (1%) |         418 |
| `["overhead", "stoppable=true"]`                    |  87.600 μs (5%) |         |  44.28 KiB (1%) |         611 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   3.230 ms (5%) |         | 728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   3.885 ms (5%) |         |   1.79 MiB (1%) |         216 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   3.587 ms (5%) |         |   1.42 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  13.086 ms (5%) |         |   1.16 MiB (1%) |         136 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  25.163 ms (5%) |         |   1.24 MiB (1%) |        6883 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  22.953 ms (5%) |         |   1.27 MiB (1%) |        6037 |
| `["parallel_histogram", "seq"]`                     |   5.738 ms (5%) |         | 364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  35.225 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  17.601 ms (5%) |         |  736 bytes (1%) |          11 |
| `["splitby", "count", "foldl"]`                     |   2.330 ms (5%) |         |                 |             |
| `["splitby", "count", "man"]`                       |   1.754 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    |   1.184 ms (5%) |         |   1.09 KiB (1%) |          19 |
| `["sum", "random", "foldl"]`                        |  16.256 ms (5%) |         |                 |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   8.173 ms (5%) |         |  74.08 KiB (1%) |        1101 |
| `["sum", "random", "reduce", "basesize=256"]`       |   8.119 ms (5%) |         |  36.67 KiB (1%) |         544 |
| `["sum", "random", "reduce", "basesize=512"]`       |   8.029 ms (5%) |         |  18.11 KiB (1%) |         270 |
| `["sum", "uniform", "foldl"]`                       |  15.738 ms (5%) |         |                 |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   7.994 ms (5%) |         |  74.08 KiB (1%) |        1101 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   7.905 ms (5%) |         |  36.77 KiB (1%) |         547 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   7.848 ms (5%) |         |  18.03 KiB (1%) |         268 |
| `["sum", "valley", "foldl"]`                        |  16.071 ms (5%) |         |                 |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   8.219 ms (5%) |         |  74.11 KiB (1%) |        1102 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   8.130 ms (5%) |         |  36.70 KiB (1%) |         545 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   8.108 ms (5%) |         |  18.03 KiB (1%) |         268 |
| `["words", "nthreads=1"]`                           |  23.868 ms (5%) |         |  31.62 MiB (1%) |     1029657 |
| `["words", "nthreads=2"]`                           |  14.361 ms (5%) |         |  32.33 MiB (1%) |     1029730 |
| `["words", "nthreads=4"]`                           |  14.541 ms (5%) |         |  32.96 MiB (1%) |     1029902 |

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
      Ubuntu 20.04.5 LTS
  uname: Linux 5.15.0-1022-azure #27~20.04.1-Ubuntu SMP Mon Oct 17 02:03:50 UTC 2022 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2593 MHz       8149 s          2 s        280 s       2593 s          0 s
       #2  2593 MHz       7028 s          1 s        285 s       3718 s          0 s
       
  Memory: 6.78125 GB (3697.83984375 MB free)
  Uptime: 1106.87 sec
  Load Avg:  1.47  1.53  1.09
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
    Vulnerability Mmio stale data:   Vulnerable: Clear CPU buffers attempted, no microcode; SMT Host state unknown
    Vulnerability Retbleed:          Vulnerable
    Vulnerability Spec store bypass: Vulnerable
    Vulnerability Spectre v1:        Mitigation; usercopy/swapgs barriers and __user pointer sanitization
    Vulnerability Spectre v2:        Mitigation; Retpolines, STIBP disabled, RSB filling, PBRSB-eIBRS Not affected
    Vulnerability Srbds:             Not affected
    Vulnerability Tsx async abort:   Mitigation; Clear CPU buffers; SMT Host state unknown
    Flags:                           fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush mmx fxsr sse sse2 ss ht syscall nx pdpe1gb rdtscp lm constant_tsc rep_good nopl xtopology cpuid pni pclmulqdq ssse3 fma cx16 pcid sse4_1 sse4_2 movbe popcnt aes xsave avx f16c rdrand hypervisor lahf_lm abm 3dnowprefetch invpcid_single pti fsgsbase bmi1 hle avx2 smep bmi2 erms invpcid rtm avx512f avx512dq rdseed adx smap clflushopt avx512cd avx512bw avx512vl xsaveopt xsavec xsaves md_clear
    

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

