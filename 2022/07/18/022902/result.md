# Multi-thread benchmark result

* Pull request commit: [`3dfeb492edb1ed14e68d1274e1799e27ef6934f0`](https://github.com/JuliaFolds/Transducers.jl/commit/3dfeb492edb1ed14e68d1274e1799e27ef6934f0)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/243> (Update */Manifest.toml)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 18 Jul 2022 - 02:22
    - Baseline: 18 Jul 2022 - 02:28
* Package commits:
    - Target: 7c3ef5
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
| `["findfirst", "n=1000", "reduce", "basesize=128"]` |                   1.04 (5%)  | 0.99 (1%) :white_check_mark: |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` |                   1.04 (5%)  |                1.01 (1%) :x: |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 0.88 (5%) :white_check_mark: | 0.84 (1%) :white_check_mark: |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  |                   1.04 (5%)  |                1.02 (1%) :x: |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  |                1.08 (5%) :x: |                1.09 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |                   0.97 (5%)  | 0.96 (1%) :white_check_mark: |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |                2.34 (5%) :x: |                1.81 (1%) :x: |
| `["parallel_histogram", "seq"]`                     |                1.08 (5%) :x: |                   1.00 (1%)  |
| `["splitby", "count", "reduce"]`                    |                   0.98 (5%)  | 0.99 (1%) :white_check_mark: |
| `["sum", "random", "foldl"]`                        |                1.09 (5%) :x: |                   1.00 (1%)  |
| `["sum", "random", "reduce", "basesize=128"]`       |                1.10 (5%) :x: |                   1.00 (1%)  |
| `["sum", "random", "reduce", "basesize=256"]`       |                1.10 (5%) :x: |                   1.00 (1%)  |
| `["sum", "random", "reduce", "basesize=512"]`       |                1.11 (5%) :x: |                   1.00 (1%)  |
| `["sum", "uniform", "foldl"]`                       |                1.07 (5%) :x: |                   1.00 (1%)  |
| `["sum", "uniform", "reduce", "basesize=128"]`      |                1.10 (5%) :x: |                   1.00 (1%)  |
| `["sum", "uniform", "reduce", "basesize=512"]`      |                1.05 (5%) :x: |                   1.00 (1%)  |
| `["sum", "valley", "foldl"]`                        |                1.08 (5%) :x: |                   1.00 (1%)  |
| `["sum", "valley", "reduce", "basesize=128"]`       |                1.07 (5%) :x: |                   1.00 (1%)  |
| `["sum", "valley", "reduce", "basesize=256"]`       |                1.06 (5%) :x: |                   1.00 (1%)  |

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
  uname: Linux 5.13.0-1031-azure #37~20.04.1-Ubuntu SMP Mon Jun 13 22:51:01 UTC 2022 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v3 @ 2.40GHz: 
              speed         user         nice          sys         idle          irq
       #1  2394 MHz       5376 s          1 s        238 s       1572 s          0 s
       #2  2394 MHz       5210 s          2 s        248 s       1747 s          0 s
       
  Memory: 6.783607482910156 GB (3826.81640625 MB free)
  Uptime: 727.11 sec
  Load Avg:  1.59  1.46  0.9
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, haswell)
```

### Baseline
```
Julia Version 1.7.3
Commit 742b9abb4d (2022-05-06 12:58 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 20.04.4 LTS
  uname: Linux 5.13.0-1031-azure #37~20.04.1-Ubuntu SMP Mon Jun 13 22:51:01 UTC 2022 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v3 @ 2.40GHz: 
              speed         user         nice          sys         idle          irq
       #1  2394 MHz       7705 s          1 s        305 s       2442 s          0 s
       #2  2394 MHz       7782 s          2 s        327 s       2364 s          0 s
       
  Memory: 6.783607482910156 GB (3793.5859375 MB free)
  Uptime: 1054.85 sec
  Load Avg:  1.91  1.65  1.15
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, haswell)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 18 Jul 2022 - 2:22
* Package commit: 7c3ef5
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
| `["collect", "assoc", "basesize=1"]`                | 304.583 ms (5%) |         |  25.97 MiB (1%) |      306760 |
| `["collect", "assoc", "basesize=1024"]`             | 250.982 ms (5%) |         |   2.61 MiB (1%) |         456 |
| `["collect", "assoc", "basesize=32"]`               | 253.236 ms (5%) |         |   4.82 MiB (1%) |       11711 |
| `["collect", "seq"]`                                | 488.747 ms (5%) |         | 812.73 KiB (1%) |          11 |
| `["collect", "unordered", "basesize=1"]`            | 424.127 ms (5%) |         |  23.88 MiB (1%) |      412196 |
| `["collect", "unordered", "basesize=1024"]`         | 269.141 ms (5%) |         |   1.02 MiB (1%) |        1267 |
| `["collect", "unordered", "basesize=32"]`           | 280.810 ms (5%) |         |   1.60 MiB (1%) |       15167 |
| `["findfirst", "n=1000", "foldl"]`                  | 727.989 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 408.397 ms (5%) |         | 230.33 KiB (1%) |        3240 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 513.552 ms (5%) |         | 159.41 KiB (1%) |        2236 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 500.828 ms (5%) |         |  81.33 KiB (1%) |        1146 |
| `["findfirst", "n=400", "foldl"]`                   | 531.401 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 282.834 ms (5%) |         | 379.30 KiB (1%) |        5411 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 286.281 ms (5%) |         | 200.94 KiB (1%) |        2876 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 423.341 ms (5%) |         | 149.88 KiB (1%) |        2148 |
| `["findfirst", "n=500", "foldl"]`                   |  89.359 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 177.342 ms (5%) |         | 213.00 KiB (1%) |        2955 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 178.576 ms (5%) |         | 118.77 KiB (1%) |        1635 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 230.377 ms (5%) |         |  92.05 KiB (1%) |        1246 |
| `["overhead", "default"]`                           |  75.700 μs (5%) |         |  32.70 KiB (1%) |         417 |
| `["overhead", "stoppable=false"]`                   |  76.000 μs (5%) |         |  32.69 KiB (1%) |         416 |
| `["overhead", "stoppable=true"]`                    |  90.300 μs (5%) |         |  44.22 KiB (1%) |         609 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   3.725 ms (5%) |         | 728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   4.237 ms (5%) |         |   1.79 MiB (1%) |         215 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   3.728 ms (5%) |         |   1.42 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  12.966 ms (5%) |         |   1.51 MiB (1%) |         235 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  16.912 ms (5%) |         |   1.07 MiB (1%) |        1605 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  17.186 ms (5%) |         |   1.09 MiB (1%) |        1957 |
| `["parallel_histogram", "seq"]`                     |   6.589 ms (5%) |         | 364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  61.760 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  31.662 ms (5%) |         |  736 bytes (1%) |          11 |
| `["splitby", "count", "foldl"]`                     |   1.862 ms (5%) |         |                 |             |
| `["splitby", "count", "man"]`                       |   1.514 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    | 898.920 μs (5%) |         |   1.03 KiB (1%) |          18 |
| `["sum", "random", "foldl"]`                        |  18.577 ms (5%) |         |                 |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   9.486 ms (5%) |         |  74.08 KiB (1%) |        1101 |
| `["sum", "random", "reduce", "basesize=256"]`       |   9.492 ms (5%) |         |  36.70 KiB (1%) |         545 |
| `["sum", "random", "reduce", "basesize=512"]`       |   9.443 ms (5%) |         |  18.05 KiB (1%) |         268 |
| `["sum", "uniform", "foldl"]`                       |  17.489 ms (5%) |         |                 |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   9.315 ms (5%) |         |  74.11 KiB (1%) |        1102 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   8.766 ms (5%) |         |  36.73 KiB (1%) |         546 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   8.833 ms (5%) |         |  17.97 KiB (1%) |         266 |
| `["sum", "valley", "foldl"]`                        |  18.088 ms (5%) |         |                 |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   9.663 ms (5%) |         |  74.14 KiB (1%) |        1103 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   9.561 ms (5%) |         |  36.70 KiB (1%) |         545 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   8.964 ms (5%) |         |  18.00 KiB (1%) |         267 |
| `["words", "nthreads=1"]`                           |  27.538 ms (5%) |         |  31.61 MiB (1%) |     1029747 |
| `["words", "nthreads=2"]`                           |  16.869 ms (5%) |         |  32.33 MiB (1%) |     1029847 |
| `["words", "nthreads=4"]`                           |  16.988 ms (5%) |         |  32.96 MiB (1%) |     1029995 |

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
  uname: Linux 5.13.0-1031-azure #37~20.04.1-Ubuntu SMP Mon Jun 13 22:51:01 UTC 2022 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v3 @ 2.40GHz: 
              speed         user         nice          sys         idle          irq
       #1  2394 MHz       5376 s          1 s        238 s       1572 s          0 s
       #2  2394 MHz       5210 s          2 s        248 s       1747 s          0 s
       
  Memory: 6.783607482910156 GB (3826.81640625 MB free)
  Uptime: 727.11 sec
  Load Avg:  1.59  1.46  0.9
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, haswell)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 18 Jul 2022 - 2:28
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
| `["collect", "assoc", "basesize=1"]`                | 307.998 ms (5%) |         |  25.97 MiB (1%) |      306740 |
| `["collect", "assoc", "basesize=1024"]`             | 248.697 ms (5%) |         |   2.61 MiB (1%) |         457 |
| `["collect", "assoc", "basesize=32"]`               | 255.571 ms (5%) |         |   4.82 MiB (1%) |       11711 |
| `["collect", "seq"]`                                | 494.662 ms (5%) |         | 812.73 KiB (1%) |          11 |
| `["collect", "unordered", "basesize=1"]`            | 415.021 ms (5%) |         |  23.81 MiB (1%) |      410116 |
| `["collect", "unordered", "basesize=1024"]`         | 271.071 ms (5%) |         |   1.01 MiB (1%) |        1143 |
| `["collect", "unordered", "basesize=32"]`           | 277.721 ms (5%) |         |   1.60 MiB (1%) |       15233 |
| `["findfirst", "n=1000", "foldl"]`                  | 710.890 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 393.817 ms (5%) |         | 232.92 KiB (1%) |        3278 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 491.722 ms (5%) |         | 157.42 KiB (1%) |        2200 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 571.893 ms (5%) |         |  96.67 KiB (1%) |        1343 |
| `["findfirst", "n=400", "foldl"]`                   | 529.330 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 270.939 ms (5%) |         | 371.22 KiB (1%) |        5299 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 288.901 ms (5%) |         | 200.83 KiB (1%) |        2872 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 390.302 ms (5%) |         | 137.97 KiB (1%) |        1980 |
| `["findfirst", "n=500", "foldl"]`                   |  86.001 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 183.441 ms (5%) |         | 221.61 KiB (1%) |        3056 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 176.708 ms (5%) |         | 118.86 KiB (1%) |        1638 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  98.490 ms (5%) |         |  50.78 KiB (1%) |         679 |
| `["overhead", "default"]`                           |  74.800 μs (5%) |         |  32.73 KiB (1%) |         418 |
| `["overhead", "stoppable=false"]`                   |  79.000 μs (5%) |         |  32.75 KiB (1%) |         418 |
| `["overhead", "stoppable=true"]`                    |  92.200 μs (5%) |         |  44.25 KiB (1%) |         610 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   3.577 ms (5%) |         | 728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   4.222 ms (5%) |         |   1.79 MiB (1%) |         215 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   3.848 ms (5%) |         |   1.42 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  12.685 ms (5%) |         |   1.51 MiB (1%) |         243 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  16.327 ms (5%) |         |   1.07 MiB (1%) |        2723 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  17.202 ms (5%) |         |   1.10 MiB (1%) |        2284 |
| `["parallel_histogram", "seq"]`                     |   6.079 ms (5%) |         | 364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  59.106 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  30.711 ms (5%) |         |  736 bytes (1%) |          11 |
| `["splitby", "count", "foldl"]`                     |   1.889 ms (5%) |         |                 |             |
| `["splitby", "count", "man"]`                       |   1.515 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    | 914.001 μs (5%) |         |   1.05 KiB (1%) |          19 |
| `["sum", "random", "foldl"]`                        |  16.985 ms (5%) |         |                 |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   8.632 ms (5%) |         |  74.17 KiB (1%) |        1104 |
| `["sum", "random", "reduce", "basesize=256"]`       |   8.650 ms (5%) |         |  36.70 KiB (1%) |         545 |
| `["sum", "random", "reduce", "basesize=512"]`       |   8.511 ms (5%) |         |  18.08 KiB (1%) |         269 |
| `["sum", "uniform", "foldl"]`                       |  16.363 ms (5%) |         |                 |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   8.476 ms (5%) |         |  74.17 KiB (1%) |        1104 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   8.379 ms (5%) |         |  36.70 KiB (1%) |         545 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   8.401 ms (5%) |         |  18.00 KiB (1%) |         267 |
| `["sum", "valley", "foldl"]`                        |  16.789 ms (5%) |         |                 |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   9.034 ms (5%) |         |  73.95 KiB (1%) |        1097 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   9.043 ms (5%) |         |  36.73 KiB (1%) |         546 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   8.780 ms (5%) |         |  18.00 KiB (1%) |         267 |
| `["words", "nthreads=1"]`                           |  28.468 ms (5%) |         |  31.57 MiB (1%) |     1027979 |
| `["words", "nthreads=2"]`                           |  16.820 ms (5%) |         |  32.28 MiB (1%) |     1028056 |
| `["words", "nthreads=4"]`                           |  17.156 ms (5%) |         |  32.91 MiB (1%) |     1028267 |

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
  uname: Linux 5.13.0-1031-azure #37~20.04.1-Ubuntu SMP Mon Jun 13 22:51:01 UTC 2022 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v3 @ 2.40GHz: 
              speed         user         nice          sys         idle          irq
       #1  2394 MHz       7705 s          1 s        305 s       2442 s          0 s
       #2  2394 MHz       7782 s          2 s        327 s       2364 s          0 s
       
  Memory: 6.783607482910156 GB (3793.5859375 MB free)
  Uptime: 1054.85 sec
  Load Avg:  1.91  1.65  1.15
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, haswell)
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
    Model:                           63
    Model name:                      Intel(R) Xeon(R) CPU E5-2673 v3 @ 2.40GHz
    Stepping:                        2
    CPU MHz:                         2394.451
    BogoMIPS:                        4788.90
    Hypervisor vendor:               Microsoft
    Virtualization type:             full
    L1d cache:                       64 KiB
    L1i cache:                       64 KiB
    L2 cache:                        512 KiB
    L3 cache:                        30 MiB
    NUMA node0 CPU(s):               0,1
    Vulnerability Itlb multihit:     KVM: Mitigation: VMX unsupported
    Vulnerability L1tf:              Mitigation; PTE Inversion
    Vulnerability Mds:               Mitigation; Clear CPU buffers; SMT Host state unknown
    Vulnerability Meltdown:          Mitigation; PTI
    Vulnerability Mmio stale data:   Vulnerable: Clear CPU buffers attempted, no microcode; SMT Host state unknown
    Vulnerability Spec store bypass: Vulnerable
    Vulnerability Spectre v1:        Mitigation; usercopy/swapgs barriers and __user pointer sanitization
    Vulnerability Spectre v2:        Mitigation; Retpolines, STIBP disabled, RSB filling
    Vulnerability Srbds:             Not affected
    Vulnerability Tsx async abort:   Not affected
    Flags:                           fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush mmx fxsr sse sse2 ss ht syscall nx pdpe1gb rdtscp lm constant_tsc rep_good nopl xtopology cpuid pni pclmulqdq ssse3 fma cx16 pcid sse4_1 sse4_2 movbe popcnt aes xsave avx f16c rdrand hypervisor lahf_lm abm invpcid_single pti fsgsbase bmi1 avx2 smep bmi2 erms invpcid xsaveopt md_clear
    

| Cpu Property       | Value                                                   |
|:------------------ |:------------------------------------------------------- |
| Brand              | Intel(R) Xeon(R) CPU E5-2673 v3 @ 2.40GHz               |
| Vendor             | :Intel                                                  |
| Architecture       | :Haswell                                                |
| Model              | Family: 0x06, Model: 0x3f, Stepping: 0x02, Type: 0x00   |
| Cores              | 2 physical cores, 2 logical cores (on executing CPU)    |
|                    | No Hyperthreading hardware capability detected          |
| Clock Frequencies  | Not supported by CPU                                    |
| Data Cache         | Level 1:3 : (32, 256, 30720) kbytes                     |
|                    | 64 byte cache line size                                 |
| Address Size       | 48 bits virtual, 46 bits physical                       |
| SIMD               | 256 bit = 32 byte max. SIMD vector size                 |
| Time Stamp Counter | TSC is accessible via `rdtsc`                           |
|                    | TSC increased at every clock cycle (non-invariant TSC)  |
| Perf. Monitoring   | Performance Monitoring Counters (PMC) are not supported |
| Hypervisor         | Yes, Microsoft                                          |

