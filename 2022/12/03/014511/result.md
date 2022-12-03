# Multi-thread benchmark result

* Pull request commit: [`4890e74de845d934029fc262d04879ff1072b364`](https://github.com/JuliaFolds/Transducers.jl/commit/4890e74de845d934029fc262d04879ff1072b364)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/243> (Update */Manifest.toml)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 3 Dec 2022 - 01:39
    - Baseline: 3 Dec 2022 - 01:44
* Package commits:
    - Target: 0e7521
    - Baseline: f8d0df
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
| `["findfirst", "n=1000", "reduce", "basesize=128"]` |                1.12 (5%) :x: |                1.11 (1%) :x: |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 0.90 (5%) :white_check_mark: | 0.95 (1%) :white_check_mark: |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` |                1.08 (5%) :x: |                1.05 (1%) :x: |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  |                   1.01 (5%)  |                1.02 (1%) :x: |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 0.90 (5%) :white_check_mark: | 0.88 (1%) :white_check_mark: |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 0.73 (5%) :white_check_mark: | 0.88 (1%) :white_check_mark: |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |                1.06 (5%) :x: |                1.02 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 0.95 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["overhead", "default"]`                           |                1.05 (5%) :x: |                   1.00 (1%)  |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |                1.08 (5%) :x: |                   1.00 (1%)  |
| `["parallel_histogram", "comm", "basesize=16384"]`  | 0.74 (5%) :white_check_mark: | 0.72 (1%) :white_check_mark: |
| `["parallel_histogram", "comm", "basesize=4096"]`   |                   0.96 (5%)  | 0.98 (1%) :white_check_mark: |
| `["parallel_histogram", "comm", "basesize=8192"]`   | 0.90 (5%) :white_check_mark: | 0.84 (1%) :white_check_mark: |
| `["partition_length_maximum", "rand", "reduce"]`    |                   1.02 (5%)  | 0.96 (1%) :white_check_mark: |
| `["splitby", "count", "foldl"]`                     | 0.88 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["splitby", "count", "reduce"]`                    | 0.87 (5%) :white_check_mark: | 0.99 (1%) :white_check_mark: |
| `["sum", "random", "reduce", "basesize=128"]`       |                1.07 (5%) :x: |                   1.00 (1%)  |
| `["sum", "uniform", "foldl"]`                       |                1.05 (5%) :x: |                   1.00 (1%)  |
| `["sum", "uniform", "reduce", "basesize=512"]`      |                1.12 (5%) :x: |                   1.00 (1%)  |
| `["sum", "valley", "reduce", "basesize=128"]`       | 0.93 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["sum", "valley", "reduce", "basesize=512"]`       | 0.95 (5%) :white_check_mark: |                   1.00 (1%)  |

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
      Ubuntu 22.04.1 LTS
  uname: Linux 5.15.0-1023-azure #29-Ubuntu SMP Wed Oct 19 22:37:08 UTC 2022 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz       5441 s          0 s        262 s       3217 s          0 s
       #2  2095 MHz       5284 s          0 s        285 s       3306 s          0 s
       
  Memory: 6.781219482421875 GB (3855.6875 MB free)
  Uptime: 897.54 sec
  Load Avg:  1.59  1.5  0.94
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
      Ubuntu 22.04.1 LTS
  uname: Linux 5.15.0-1023-azure #29-Ubuntu SMP Wed Oct 19 22:37:08 UTC 2022 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz       7674 s          0 s        341 s       4123 s          0 s
       #2  2095 MHz       7921 s          0 s        376 s       3796 s          0 s
       
  Memory: 6.781219482421875 GB (3785.17578125 MB free)
  Uptime: 1220.11 sec
  Load Avg:  1.76  1.62  1.16
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, skylake-avx512)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 3 Dec 2022 - 1:39
* Package commit: 0e7521
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
| `["collect", "assoc", "basesize=1"]`                | 289.116 ms (5%) |         |  25.97 MiB (1%) |      306805 |
| `["collect", "assoc", "basesize=1024"]`             | 234.396 ms (5%) |         |   2.61 MiB (1%) |         455 |
| `["collect", "assoc", "basesize=32"]`               | 238.957 ms (5%) |         |   4.82 MiB (1%) |       11703 |
| `["collect", "seq"]`                                | 464.045 ms (5%) |         | 812.73 KiB (1%) |          11 |
| `["collect", "unordered", "basesize=1"]`            | 402.408 ms (5%) |         |  23.91 MiB (1%) |      413353 |
| `["collect", "unordered", "basesize=1024"]`         | 244.139 ms (5%) |         |   1.01 MiB (1%) |        1008 |
| `["collect", "unordered", "basesize=32"]`           | 263.799 ms (5%) |         |   1.56 MiB (1%) |       14089 |
| `["findfirst", "n=1000", "foldl"]`                  | 741.962 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 559.895 ms (5%) |         | 302.69 KiB (1%) |        4268 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 507.063 ms (5%) |         | 155.70 KiB (1%) |        2175 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 721.826 ms (5%) |         | 114.30 KiB (1%) |        1591 |
| `["findfirst", "n=400", "foldl"]`                   | 543.068 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 298.597 ms (5%) |         | 388.92 KiB (1%) |        5519 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 295.455 ms (5%) |         | 201.02 KiB (1%) |        2878 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 417.581 ms (5%) |         | 144.33 KiB (1%) |        2066 |
| `["findfirst", "n=500", "foldl"]`                   |  94.795 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 179.217 ms (5%) |         | 246.78 KiB (1%) |        3353 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |  86.058 ms (5%) |         |  72.84 KiB (1%) |         986 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 139.379 ms (5%) |         |  63.59 KiB (1%) |         863 |
| `["overhead", "default"]`                           |  83.302 μs (5%) |         |  32.70 KiB (1%) |         417 |
| `["overhead", "stoppable=false"]`                   |  75.802 μs (5%) |         |  32.75 KiB (1%) |         418 |
| `["overhead", "stoppable=true"]`                    |  92.402 μs (5%) |         |  44.25 KiB (1%) |         610 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   3.413 ms (5%) |         | 728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   4.451 ms (5%) |         |   1.79 MiB (1%) |         215 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   3.953 ms (5%) |         |   1.42 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  14.845 ms (5%) |         |   1.16 MiB (1%) |         137 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  25.561 ms (5%) |         |   1.20 MiB (1%) |        5553 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  21.774 ms (5%) |         |   1.04 MiB (1%) |         184 |
| `["parallel_histogram", "seq"]`                     |   6.364 ms (5%) |         | 364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  39.420 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  20.163 ms (5%) |         |  704 bytes (1%) |          10 |
| `["splitby", "count", "foldl"]`                     |   2.211 ms (5%) |         |                 |             |
| `["splitby", "count", "man"]`                       |   1.209 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    |   1.134 ms (5%) |         |   1.05 KiB (1%) |          19 |
| `["sum", "random", "foldl"]`                        |  18.492 ms (5%) |         |                 |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   9.379 ms (5%) |         |  74.20 KiB (1%) |        1105 |
| `["sum", "random", "reduce", "basesize=256"]`       |   9.311 ms (5%) |         |  36.70 KiB (1%) |         545 |
| `["sum", "random", "reduce", "basesize=512"]`       |   9.196 ms (5%) |         |  18.11 KiB (1%) |         270 |
| `["sum", "uniform", "foldl"]`                       |  17.921 ms (5%) |         |                 |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   9.429 ms (5%) |         |  74.17 KiB (1%) |        1104 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   9.104 ms (5%) |         |  36.77 KiB (1%) |         547 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   9.120 ms (5%) |         |  18.00 KiB (1%) |         267 |
| `["sum", "valley", "foldl"]`                        |  18.542 ms (5%) |         |                 |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   8.957 ms (5%) |         |  74.11 KiB (1%) |        1102 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   9.052 ms (5%) |         |  36.70 KiB (1%) |         545 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   9.024 ms (5%) |         |  18.06 KiB (1%) |         269 |
| `["words", "nthreads=1"]`                           |  26.286 ms (5%) |         |  31.70 MiB (1%) |     1032740 |
| `["words", "nthreads=2"]`                           |  16.572 ms (5%) |         |  32.06 MiB (1%) |     1032776 |
| `["words", "nthreads=4"]`                           |  16.964 ms (5%) |         |  32.96 MiB (1%) |     1032944 |

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
      Ubuntu 22.04.1 LTS
  uname: Linux 5.15.0-1023-azure #29-Ubuntu SMP Wed Oct 19 22:37:08 UTC 2022 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz       5441 s          0 s        262 s       3217 s          0 s
       #2  2095 MHz       5284 s          0 s        285 s       3306 s          0 s
       
  Memory: 6.781219482421875 GB (3855.6875 MB free)
  Uptime: 897.54 sec
  Load Avg:  1.59  1.5  0.94
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, skylake-avx512)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 3 Dec 2022 - 1:44
* Package commit: f8d0df
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
| `["collect", "assoc", "basesize=1"]`                | 287.854 ms (5%) |         |  25.97 MiB (1%) |      306854 |
| `["collect", "assoc", "basesize=1024"]`             | 232.072 ms (5%) |         |   2.61 MiB (1%) |         454 |
| `["collect", "assoc", "basesize=32"]`               | 238.083 ms (5%) |         |   4.82 MiB (1%) |       11718 |
| `["collect", "seq"]`                                | 468.713 ms (5%) |         | 812.73 KiB (1%) |          11 |
| `["collect", "unordered", "basesize=1"]`            | 403.436 ms (5%) |         |  23.80 MiB (1%) |      409882 |
| `["collect", "unordered", "basesize=1024"]`         | 256.963 ms (5%) |         |   1.00 MiB (1%) |         913 |
| `["collect", "unordered", "basesize=32"]`           | 268.837 ms (5%) |         |   1.57 MiB (1%) |       14484 |
| `["findfirst", "n=1000", "foldl"]`                  | 725.665 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 501.482 ms (5%) |         | 272.67 KiB (1%) |        3826 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 564.194 ms (5%) |         | 164.75 KiB (1%) |        2307 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 671.205 ms (5%) |         | 108.55 KiB (1%) |        1509 |
| `["findfirst", "n=400", "foldl"]`                   | 551.570 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 295.159 ms (5%) |         | 380.81 KiB (1%) |        5427 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 293.873 ms (5%) |         | 200.86 KiB (1%) |        2873 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 463.471 ms (5%) |         | 164.11 KiB (1%) |        2338 |
| `["findfirst", "n=500", "foldl"]`                   |  93.801 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 244.496 ms (5%) |         | 279.09 KiB (1%) |        3878 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |  81.115 ms (5%) |         |  71.25 KiB (1%) |         964 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 146.723 ms (5%) |         |  63.70 KiB (1%) |         867 |
| `["overhead", "default"]`                           |  79.202 μs (5%) |         |  32.70 KiB (1%) |         417 |
| `["overhead", "stoppable=false"]`                   |  78.702 μs (5%) |         |  32.78 KiB (1%) |         419 |
| `["overhead", "stoppable=true"]`                    |  88.202 μs (5%) |         |  44.25 KiB (1%) |         610 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   3.539 ms (5%) |         | 728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   4.116 ms (5%) |         |   1.79 MiB (1%) |         215 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   4.036 ms (5%) |         |   1.42 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  19.953 ms (5%) |         |   1.60 MiB (1%) |        2963 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  26.558 ms (5%) |         |   1.22 MiB (1%) |        6186 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  24.060 ms (5%) |         |   1.23 MiB (1%) |        5328 |
| `["parallel_histogram", "seq"]`                     |   6.391 ms (5%) |         | 364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  40.037 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  19.862 ms (5%) |         |  736 bytes (1%) |          11 |
| `["splitby", "count", "foldl"]`                     |   2.512 ms (5%) |         |                 |             |
| `["splitby", "count", "man"]`                       |   1.255 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    |   1.305 ms (5%) |         |   1.06 KiB (1%) |          18 |
| `["sum", "random", "foldl"]`                        |  18.536 ms (5%) |         |                 |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   8.757 ms (5%) |         |  74.17 KiB (1%) |        1104 |
| `["sum", "random", "reduce", "basesize=256"]`       |   9.036 ms (5%) |         |  36.64 KiB (1%) |         543 |
| `["sum", "random", "reduce", "basesize=512"]`       |   9.125 ms (5%) |         |  18.08 KiB (1%) |         269 |
| `["sum", "uniform", "foldl"]`                       |  16.998 ms (5%) |         |                 |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   9.221 ms (5%) |         |  74.17 KiB (1%) |        1104 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   9.069 ms (5%) |         |  36.70 KiB (1%) |         545 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   8.153 ms (5%) |         |  18.03 KiB (1%) |         268 |
| `["sum", "valley", "foldl"]`                        |  18.493 ms (5%) |         |                 |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   9.595 ms (5%) |         |  74.02 KiB (1%) |        1099 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   9.423 ms (5%) |         |  36.73 KiB (1%) |         546 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   9.502 ms (5%) |         |  18.03 KiB (1%) |         268 |
| `["words", "nthreads=1"]`                           |  25.754 ms (5%) |         |  31.62 MiB (1%) |     1029736 |
| `["words", "nthreads=2"]`                           |  16.902 ms (5%) |         |  31.97 MiB (1%) |     1029778 |
| `["words", "nthreads=4"]`                           |  16.726 ms (5%) |         |  32.87 MiB (1%) |     1029957 |

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
      Ubuntu 22.04.1 LTS
  uname: Linux 5.15.0-1023-azure #29-Ubuntu SMP Wed Oct 19 22:37:08 UTC 2022 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz       7674 s          0 s        341 s       4123 s          0 s
       #2  2095 MHz       7921 s          0 s        376 s       3796 s          0 s
       
  Memory: 6.781219482421875 GB (3785.17578125 MB free)
  Uptime: 1220.11 sec
  Load Avg:  1.76  1.62  1.16
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
    Address sizes:                   46 bits physical, 48 bits virtual
    Byte Order:                      Little Endian
    CPU(s):                          2
    On-line CPU(s) list:             0,1
    Vendor ID:                       GenuineIntel
    Model name:                      Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz
    CPU family:                      6
    Model:                           85
    Thread(s) per core:              1
    Core(s) per socket:              2
    Socket(s):                       1
    Stepping:                        4
    BogoMIPS:                        4190.15
    Flags:                           fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush mmx fxsr sse sse2 ss ht syscall nx pdpe1gb rdtscp lm constant_tsc rep_good nopl xtopology cpuid pni pclmulqdq ssse3 fma cx16 pcid sse4_1 sse4_2 movbe popcnt aes xsave avx f16c rdrand hypervisor lahf_lm abm 3dnowprefetch invpcid_single pti fsgsbase bmi1 hle avx2 smep bmi2 erms invpcid rtm avx512f avx512dq rdseed adx smap clflushopt avx512cd avx512bw avx512vl xsaveopt xsavec xsaves md_clear
    Hypervisor vendor:               Microsoft
    Virtualization type:             full
    L1d cache:                       64 KiB (2 instances)
    L1i cache:                       64 KiB (2 instances)
    L2 cache:                        2 MiB (2 instances)
    L3 cache:                        35.8 MiB (1 instance)
    NUMA node(s):                    1
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

