# Multi-thread benchmark result

* Pull request commit: [`c21e2a7d0e0bec0e44045c5e5b53cdb7b24df9d7`](https://github.com/JuliaFolds/Transducers.jl/commit/c21e2a7d0e0bec0e44045c5e5b53cdb7b24df9d7)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/243> (Update */Manifest.toml)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 12 Sep 2022 - 02:50
    - Baseline: 12 Sep 2022 - 02:55
* Package commits:
    - Target: fcb4b5
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
| `["collect", "unordered", "basesize=1"]`            |                   0.98 (5%)  |                1.01 (1%) :x: |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 0.76 (5%) :white_check_mark: | 0.85 (1%) :white_check_mark: |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  |                   1.00 (5%)  |                1.05 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |                1.61 (5%) :x: |                1.35 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |                1.82 (5%) :x: |                1.44 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |                1.06 (5%) :x: |                   1.00 (1%)  |
| `["parallel_histogram", "comm", "basesize=4096"]`   | 0.90 (5%) :white_check_mark: | 0.97 (1%) :white_check_mark: |
| `["parallel_histogram", "comm", "basesize=8192"]`   |                1.55 (5%) :x: |                1.23 (1%) :x: |
| `["splitby", "count", "man"]`                       | 0.81 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["splitby", "count", "reduce"]`                    |                1.08 (5%) :x: |                1.03 (1%) :x: |
| `["words", "nthreads=2"]`                           |                   0.97 (5%)  | 0.98 (1%) :white_check_mark: |
| `["words", "nthreads=4"]`                           |                   1.01 (5%)  | 0.99 (1%) :white_check_mark: |

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
  uname: Linux 5.15.0-1019-azure #24~20.04.1-Ubuntu SMP Tue Aug 23 15:52:52 UTC 2022 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2593 MHz       4721 s          1 s        212 s       3998 s          0 s
       #2  2593 MHz       5726 s          1 s        236 s       2983 s          0 s
       
  Memory: 6.781253814697266 GB (3655.625 MB free)
  Uptime: 898.98 sec
  Load Avg:  1.58  1.43  0.86
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
  uname: Linux 5.15.0-1019-azure #24~20.04.1-Ubuntu SMP Tue Aug 23 15:52:52 UTC 2022 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2593 MHz       7331 s          1 s        309 s       4439 s          0 s
       #2  2593 MHz       7892 s          1 s        312 s       3890 s          0 s
       
  Memory: 6.781253814697266 GB (3473.93359375 MB free)
  Uptime: 1214.44 sec
  Load Avg:  1.56  1.51  1.06
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, skylake-avx512)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 12 Sep 2022 - 2:50
* Package commit: fcb4b5
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
| `["collect", "assoc", "basesize=1"]`                | 247.789 ms (5%) |         |   25.97 MiB (1%) |      306821 |
| `["collect", "assoc", "basesize=1024"]`             | 198.411 ms (5%) |         |    2.61 MiB (1%) |         456 |
| `["collect", "assoc", "basesize=32"]`               | 200.699 ms (5%) |         |    4.82 MiB (1%) |       11709 |
| `["collect", "seq"]`                                | 395.232 ms (5%) |         |  812.73 KiB (1%) |          11 |
| `["collect", "unordered", "basesize=1"]`            | 348.382 ms (5%) |         |   23.88 MiB (1%) |      412239 |
| `["collect", "unordered", "basesize=1024"]`         | 212.999 ms (5%) |         | 1004.89 KiB (1%) |        1052 |
| `["collect", "unordered", "basesize=32"]`           | 223.753 ms (5%) |         |    1.58 MiB (1%) |       14730 |
| `["findfirst", "n=1000", "foldl"]`                  | 631.566 ms (5%) |         |                  |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 347.271 ms (5%) |         |  232.83 KiB (1%) |        3275 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 423.575 ms (5%) |         |  157.20 KiB (1%) |        2193 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 565.819 ms (5%) |         |  108.55 KiB (1%) |        1509 |
| `["findfirst", "n=400", "foldl"]`                   | 473.845 ms (5%) |         |                  |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 245.876 ms (5%) |         |  374.94 KiB (1%) |        5364 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 249.089 ms (5%) |         |  200.91 KiB (1%) |        2875 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 306.038 ms (5%) |         |  137.02 KiB (1%) |        1934 |
| `["findfirst", "n=500", "foldl"]`                   |  82.167 ms (5%) |         |                  |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 150.441 ms (5%) |         |  217.39 KiB (1%) |        2987 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 228.747 ms (5%) |         |  158.59 KiB (1%) |        2228 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 122.940 ms (5%) |         |   63.70 KiB (1%) |         867 |
| `["overhead", "default"]`                           |  75.302 μs (5%) |         |   32.70 KiB (1%) |         417 |
| `["overhead", "stoppable=false"]`                   |  76.501 μs (5%) |         |   32.69 KiB (1%) |         416 |
| `["overhead", "stoppable=true"]`                    |  87.902 μs (5%) |         |   44.22 KiB (1%) |         609 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   3.260 ms (5%) |         |  728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   3.917 ms (5%) |         |    1.79 MiB (1%) |         216 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   3.616 ms (5%) |         |    1.42 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  18.612 ms (5%) |         |    1.59 MiB (1%) |        2678 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  21.856 ms (5%) |         |    1.19 MiB (1%) |        5155 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  22.317 ms (5%) |         |    1.27 MiB (1%) |        5068 |
| `["parallel_histogram", "seq"]`                     |   5.781 ms (5%) |         |  364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  35.208 ms (5%) |         |                  |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  17.615 ms (5%) |         |   736 bytes (1%) |          11 |
| `["splitby", "count", "foldl"]`                     |   2.297 ms (5%) |         |                  |             |
| `["splitby", "count", "man"]`                       |   1.418 ms (5%) |         |                  |             |
| `["splitby", "count", "reduce"]`                    |   1.179 ms (5%) |         |    1.09 KiB (1%) |          19 |
| `["sum", "random", "foldl"]`                        |  16.315 ms (5%) |         |                  |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   8.259 ms (5%) |         |   74.20 KiB (1%) |        1105 |
| `["sum", "random", "reduce", "basesize=256"]`       |   8.161 ms (5%) |         |   36.77 KiB (1%) |         547 |
| `["sum", "random", "reduce", "basesize=512"]`       |   8.097 ms (5%) |         |   18.11 KiB (1%) |         270 |
| `["sum", "uniform", "foldl"]`                       |  15.743 ms (5%) |         |                  |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   8.058 ms (5%) |         |   74.08 KiB (1%) |        1101 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   7.932 ms (5%) |         |   36.77 KiB (1%) |         547 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   7.865 ms (5%) |         |   18.03 KiB (1%) |         268 |
| `["sum", "valley", "foldl"]`                        |  16.166 ms (5%) |         |                  |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   8.269 ms (5%) |         |   74.08 KiB (1%) |        1101 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   8.186 ms (5%) |         |   36.73 KiB (1%) |         546 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   8.131 ms (5%) |         |   18.06 KiB (1%) |         269 |
| `["words", "nthreads=1"]`                           |  24.315 ms (5%) |         |   31.69 MiB (1%) |     1032568 |
| `["words", "nthreads=2"]`                           |  15.157 ms (5%) |         |   32.05 MiB (1%) |     1032604 |
| `["words", "nthreads=4"]`                           |  15.188 ms (5%) |         |   32.76 MiB (1%) |     1032703 |

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
  uname: Linux 5.15.0-1019-azure #24~20.04.1-Ubuntu SMP Tue Aug 23 15:52:52 UTC 2022 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2593 MHz       4721 s          1 s        212 s       3998 s          0 s
       #2  2593 MHz       5726 s          1 s        236 s       2983 s          0 s
       
  Memory: 6.781253814697266 GB (3655.625 MB free)
  Uptime: 898.98 sec
  Load Avg:  1.58  1.43  0.86
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, skylake-avx512)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 12 Sep 2022 - 2:55
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

| ID                                                  | time            | GC time | memory           | allocations |
|-----------------------------------------------------|----------------:|--------:|-----------------:|------------:|
| `["collect", "assoc", "basesize=1"]`                | 247.434 ms (5%) |         |   25.97 MiB (1%) |      306722 |
| `["collect", "assoc", "basesize=1024"]`             | 199.017 ms (5%) |         |    2.61 MiB (1%) |         456 |
| `["collect", "assoc", "basesize=32"]`               | 201.160 ms (5%) |         |    4.82 MiB (1%) |       11707 |
| `["collect", "seq"]`                                | 395.277 ms (5%) |         |  812.73 KiB (1%) |          11 |
| `["collect", "unordered", "basesize=1"]`            | 356.369 ms (5%) |         |   23.62 MiB (1%) |      403667 |
| `["collect", "unordered", "basesize=1024"]`         | 213.815 ms (5%) |         | 1005.17 KiB (1%) |        1019 |
| `["collect", "unordered", "basesize=32"]`           | 226.434 ms (5%) |         |    1.58 MiB (1%) |       14737 |
| `["findfirst", "n=1000", "foldl"]`                  | 625.761 ms (5%) |         |                  |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 341.209 ms (5%) |         |  232.86 KiB (1%) |        3276 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 559.898 ms (5%) |         |  184.47 KiB (1%) |        2624 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 545.613 ms (5%) |         |  108.55 KiB (1%) |        1508 |
| `["findfirst", "n=400", "foldl"]`                   | 469.781 ms (5%) |         |                  |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 241.868 ms (5%) |         |  374.11 KiB (1%) |        5349 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 247.014 ms (5%) |         |  200.95 KiB (1%) |        2876 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 307.172 ms (5%) |         |  130.31 KiB (1%) |        1854 |
| `["findfirst", "n=500", "foldl"]`                   |  81.427 ms (5%) |         |                  |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |  93.175 ms (5%) |         |  161.03 KiB (1%) |        2193 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 125.881 ms (5%) |         |  109.86 KiB (1%) |        1501 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 116.115 ms (5%) |         |   63.66 KiB (1%) |         865 |
| `["overhead", "default"]`                           |  77.401 μs (5%) |         |   32.73 KiB (1%) |         418 |
| `["overhead", "stoppable=false"]`                   |  77.802 μs (5%) |         |   32.72 KiB (1%) |         417 |
| `["overhead", "stoppable=true"]`                    |  86.802 μs (5%) |         |   44.25 KiB (1%) |         610 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   3.218 ms (5%) |         |  728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   3.841 ms (5%) |         |    1.79 MiB (1%) |         215 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   3.566 ms (5%) |         |    1.42 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  17.995 ms (5%) |         |    1.59 MiB (1%) |        2662 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  24.322 ms (5%) |         |    1.23 MiB (1%) |        6525 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  14.397 ms (5%) |         |    1.04 MiB (1%) |         171 |
| `["parallel_histogram", "seq"]`                     |   5.714 ms (5%) |         |  364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  35.315 ms (5%) |         |                  |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  17.658 ms (5%) |         |   736 bytes (1%) |          11 |
| `["splitby", "count", "foldl"]`                     |   2.362 ms (5%) |         |                  |             |
| `["splitby", "count", "man"]`                       |   1.755 ms (5%) |         |                  |             |
| `["splitby", "count", "reduce"]`                    |   1.091 ms (5%) |         |    1.06 KiB (1%) |          18 |
| `["sum", "random", "foldl"]`                        |  16.071 ms (5%) |         |                  |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   8.070 ms (5%) |         |   74.11 KiB (1%) |        1102 |
| `["sum", "random", "reduce", "basesize=256"]`       |   8.012 ms (5%) |         |   36.77 KiB (1%) |         547 |
| `["sum", "random", "reduce", "basesize=512"]`       |   7.944 ms (5%) |         |   18.11 KiB (1%) |         270 |
| `["sum", "uniform", "foldl"]`                       |  15.759 ms (5%) |         |                  |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   7.985 ms (5%) |         |   74.02 KiB (1%) |        1099 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   7.890 ms (5%) |         |   36.77 KiB (1%) |         547 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   7.821 ms (5%) |         |   17.97 KiB (1%) |         266 |
| `["sum", "valley", "foldl"]`                        |  16.078 ms (5%) |         |                  |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   8.225 ms (5%) |         |   74.14 KiB (1%) |        1103 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   8.117 ms (5%) |         |   36.73 KiB (1%) |         546 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   8.101 ms (5%) |         |   18.06 KiB (1%) |         269 |
| `["words", "nthreads=1"]`                           |  25.543 ms (5%) |         |   32.00 MiB (1%) |     1042969 |
| `["words", "nthreads=2"]`                           |  15.570 ms (5%) |         |   32.72 MiB (1%) |     1043042 |
| `["words", "nthreads=4"]`                           |  15.024 ms (5%) |         |   33.16 MiB (1%) |     1043121 |

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
  uname: Linux 5.15.0-1019-azure #24~20.04.1-Ubuntu SMP Tue Aug 23 15:52:52 UTC 2022 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2593 MHz       7331 s          1 s        309 s       4439 s          0 s
       #2  2593 MHz       7892 s          1 s        312 s       3890 s          0 s
       
  Memory: 6.781253814697266 GB (3473.93359375 MB free)
  Uptime: 1214.44 sec
  Load Avg:  1.56  1.51  1.06
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
    Vulnerability Spectre v2:        Mitigation; Retpolines, STIBP disabled, RSB filling
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

