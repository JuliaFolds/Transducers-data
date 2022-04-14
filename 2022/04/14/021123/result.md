# Multi-thread benchmark result

* Pull request commit: [`0009e307a796cbd09fb12cd4937fc66e34751b65`](https://github.com/JuliaFolds/Transducers.jl/commit/0009e307a796cbd09fb12cd4937fc66e34751b65)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/243> (Update */Manifest.toml)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 14 Apr 2022 - 02:05
    - Baseline: 14 Apr 2022 - 02:10
* Package commits:
    - Target: 3aa676
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
| `["collect", "assoc", "basesize=1"]`                |                1.06 (5%) :x: |                   1.00 (1%)  |
| `["collect", "assoc", "basesize=1024"]`             |                1.08 (5%) :x: |                   1.00 (1%)  |
| `["collect", "assoc", "basesize=32"]`               |                1.14 (5%) :x: |                   1.00 (1%)  |
| `["collect", "unordered", "basesize=1"]`            |                1.11 (5%) :x: |                   1.00 (1%)  |
| `["collect", "unordered", "basesize=1024"]`         |                1.05 (5%) :x: |                   1.00 (1%)  |
| `["collect", "unordered", "basesize=32"]`           |                1.11 (5%) :x: |                   1.00 (1%)  |
| `["findfirst", "n=1000", "foldl"]`                  |                1.13 (5%) :x: |                   1.00 (1%)  |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` |                1.13 (5%) :x: |                   0.99 (1%)  |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 0.88 (5%) :white_check_mark: | 0.87 (1%) :white_check_mark: |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 0.95 (5%) :white_check_mark: | 0.90 (1%) :white_check_mark: |
| `["findfirst", "n=400", "foldl"]`                   |                1.14 (5%) :x: |                   1.00 (1%)  |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  |                1.18 (5%) :x: |                1.04 (1%) :x: |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  |                1.15 (5%) :x: |                1.03 (1%) :x: |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  |                1.17 (5%) :x: |                1.07 (1%) :x: |
| `["findfirst", "n=500", "foldl"]`                   |                1.10 (5%) :x: |                   1.00 (1%)  |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |                1.11 (5%) :x: |                1.08 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 0.71 (5%) :white_check_mark: | 0.81 (1%) :white_check_mark: |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 0.78 (5%) :white_check_mark: | 0.83 (1%) :white_check_mark: |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |                   0.97 (5%)  | 0.87 (1%) :white_check_mark: |
| `["parallel_histogram", "comm", "basesize=16384"]`  |                1.20 (5%) :x: |                1.24 (1%) :x: |
| `["parallel_histogram", "comm", "basesize=4096"]`   |                   0.96 (5%)  | 0.99 (1%) :white_check_mark: |
| `["parallel_histogram", "comm", "basesize=8192"]`   | 0.82 (5%) :white_check_mark: | 0.89 (1%) :white_check_mark: |
| `["partition_length_maximum", "rand", "foldl"]`     |                1.21 (5%) :x: |                   1.00 (1%)  |
| `["partition_length_maximum", "rand", "reduce"]`    |                1.24 (5%) :x: |                   1.00 (1%)  |
| `["splitby", "count", "reduce"]`                    |                   1.03 (5%)  | 0.97 (1%) :white_check_mark: |
| `["sum", "random", "foldl"]`                        |                1.05 (5%) :x: |                   1.00 (1%)  |
| `["sum", "random", "reduce", "basesize=128"]`       |                1.12 (5%) :x: |                   1.00 (1%)  |
| `["sum", "random", "reduce", "basesize=256"]`       |                1.18 (5%) :x: |                   1.00 (1%)  |
| `["sum", "random", "reduce", "basesize=512"]`       |                1.12 (5%) :x: |                   1.00 (1%)  |
| `["sum", "uniform", "foldl"]`                       |                1.06 (5%) :x: |                   1.00 (1%)  |
| `["sum", "uniform", "reduce", "basesize=128"]`      |                1.10 (5%) :x: |                   1.00 (1%)  |
| `["sum", "uniform", "reduce", "basesize=256"]`      |                1.08 (5%) :x: |                   1.00 (1%)  |
| `["sum", "uniform", "reduce", "basesize=512"]`      | 0.94 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["sum", "valley", "foldl"]`                        |                1.08 (5%) :x: |                   1.00 (1%)  |
| `["sum", "valley", "reduce", "basesize=128"]`       |                1.10 (5%) :x: |                   1.00 (1%)  |
| `["sum", "valley", "reduce", "basesize=256"]`       |                1.07 (5%) :x: |                   1.00 (1%)  |
| `["words", "nthreads=1"]`                           |                1.09 (5%) :x: |                   1.00 (1%)  |
| `["words", "nthreads=2"]`                           |                1.11 (5%) :x: |                   0.99 (1%)  |
| `["words", "nthreads=4"]`                           |                1.12 (5%) :x: |                   1.00 (1%)  |

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
  CPU: Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz: 
              speed         user         nice          sys         idle          irq
       #1  2294 MHz       5142 s          1 s        242 s       2828 s          0 s
       #2  2294 MHz       5474 s          2 s        268 s       2472 s          0 s
       
  Memory: 6.783611297607422 GB (3512.4375 MB free)
  Uptime: 828.61 sec
  Load Avg:  1.62  1.46  0.9
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, broadwell)
```

### Baseline
```
Julia Version 1.7.2
Commit bf53498635 (2022-02-06 15:21 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 20.04.4 LTS
  uname: Linux 5.13.0-1021-azure #24~20.04.1-Ubuntu SMP Tue Mar 29 15:34:22 UTC 2022 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz: 
              speed         user         nice          sys         idle          irq
       #1  2294 MHz       7563 s          1 s        323 s       3546 s          0 s
       #2  2294 MHz       7923 s          2 s        328 s       3185 s          0 s
       
  Memory: 6.783611297607422 GB (3473.296875 MB free)
  Uptime: 1151.5 sec
  Load Avg:  1.68  1.59  1.13
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, broadwell)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 14 Apr 2022 - 2:5
* Package commit: 3aa676
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
| `["collect", "assoc", "basesize=1"]`                | 223.471 ms (5%) |         |  25.97 MiB (1%) |      306831 |
| `["collect", "assoc", "basesize=1024"]`             | 163.737 ms (5%) |         |   2.61 MiB (1%) |         456 |
| `["collect", "assoc", "basesize=32"]`               | 179.476 ms (5%) |         |   4.82 MiB (1%) |       11708 |
| `["collect", "seq"]`                                | 331.819 ms (5%) |         | 812.73 KiB (1%) |          11 |
| `["collect", "unordered", "basesize=1"]`            | 361.590 ms (5%) |         |  23.93 MiB (1%) |      414058 |
| `["collect", "unordered", "basesize=1024"]`         | 182.678 ms (5%) |         |   1.03 MiB (1%) |        1578 |
| `["collect", "unordered", "basesize=32"]`           | 199.777 ms (5%) |         |   1.61 MiB (1%) |       15689 |
| `["findfirst", "n=1000", "foldl"]`                  | 587.932 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 333.145 ms (5%) |         | 230.62 KiB (1%) |        3249 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 385.326 ms (5%) |         | 150.97 KiB (1%) |        2116 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 475.075 ms (5%) |         |  96.78 KiB (1%) |        1347 |
| `["findfirst", "n=400", "foldl"]`                   | 442.845 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 249.288 ms (5%) |         | 397.88 KiB (1%) |        5658 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 242.154 ms (5%) |         | 207.34 KiB (1%) |        2961 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 274.769 ms (5%) |         | 120.77 KiB (1%) |        1720 |
| `["findfirst", "n=500", "foldl"]`                   |  66.634 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 164.245 ms (5%) |         | 250.52 KiB (1%) |        3473 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |  85.277 ms (5%) |         |  90.17 KiB (1%) |        1216 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  80.164 ms (5%) |         |  53.03 KiB (1%) |         707 |
| `["overhead", "default"]`                           |  67.701 μs (5%) |         |  32.73 KiB (1%) |         418 |
| `["overhead", "stoppable=false"]`                   |  70.501 μs (5%) |         |  32.75 KiB (1%) |         418 |
| `["overhead", "stoppable=true"]`                    |  81.600 μs (5%) |         |  44.28 KiB (1%) |         611 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   2.389 ms (5%) |         | 728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   2.957 ms (5%) |         |   1.79 MiB (1%) |         216 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   2.812 ms (5%) |         |   1.42 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  16.445 ms (5%) |         |   1.56 MiB (1%) |        1651 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  23.357 ms (5%) |         |   1.24 MiB (1%) |        6823 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  18.503 ms (5%) |         |   1.12 MiB (1%) |        2834 |
| `["parallel_histogram", "seq"]`                     |   4.219 ms (5%) |         | 364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  37.947 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  19.819 ms (5%) |         |  736 bytes (1%) |          11 |
| `["splitby", "count", "foldl"]`                     |   1.615 ms (5%) |         |                 |             |
| `["splitby", "count", "man"]`                       |   1.223 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    | 763.206 μs (5%) |         |   1.03 KiB (1%) |          18 |
| `["sum", "random", "foldl"]`                        |  12.309 ms (5%) |         |                 |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   6.469 ms (5%) |         |  74.20 KiB (1%) |        1105 |
| `["sum", "random", "reduce", "basesize=256"]`       |   6.841 ms (5%) |         |  36.73 KiB (1%) |         546 |
| `["sum", "random", "reduce", "basesize=512"]`       |   6.383 ms (5%) |         |  18.08 KiB (1%) |         269 |
| `["sum", "uniform", "foldl"]`                       |  12.135 ms (5%) |         |                 |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   6.397 ms (5%) |         |  74.17 KiB (1%) |        1104 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   6.100 ms (5%) |         |  36.73 KiB (1%) |         546 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   6.101 ms (5%) |         |  18.03 KiB (1%) |         268 |
| `["sum", "valley", "foldl"]`                        |  12.582 ms (5%) |         |                 |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   6.497 ms (5%) |         |  74.11 KiB (1%) |        1102 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   6.257 ms (5%) |         |  36.70 KiB (1%) |         545 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   6.010 ms (5%) |         |  18.00 KiB (1%) |         267 |
| `["words", "nthreads=1"]`                           |  22.516 ms (5%) |         |  31.74 MiB (1%) |     1033756 |
| `["words", "nthreads=2"]`                           |  15.154 ms (5%) |         |  32.10 MiB (1%) |     1033792 |
| `["words", "nthreads=4"]`                           |  15.449 ms (5%) |         |  32.81 MiB (1%) |     1033894 |

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
  CPU: Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz: 
              speed         user         nice          sys         idle          irq
       #1  2294 MHz       5142 s          1 s        242 s       2828 s          0 s
       #2  2294 MHz       5474 s          2 s        268 s       2472 s          0 s
       
  Memory: 6.783611297607422 GB (3512.4375 MB free)
  Uptime: 828.61 sec
  Load Avg:  1.62  1.46  0.9
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, broadwell)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 14 Apr 2022 - 2:10
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

| ID                                                  | time            | GC time | memory          | allocations |
|-----------------------------------------------------|----------------:|--------:|----------------:|------------:|
| `["collect", "assoc", "basesize=1"]`                | 211.820 ms (5%) |         |  25.97 MiB (1%) |      306801 |
| `["collect", "assoc", "basesize=1024"]`             | 151.887 ms (5%) |         |   2.61 MiB (1%) |         456 |
| `["collect", "assoc", "basesize=32"]`               | 157.398 ms (5%) |         |   4.82 MiB (1%) |       11704 |
| `["collect", "seq"]`                                | 317.389 ms (5%) |         | 812.73 KiB (1%) |          11 |
| `["collect", "unordered", "basesize=1"]`            | 325.620 ms (5%) |         |  23.91 MiB (1%) |      413457 |
| `["collect", "unordered", "basesize=1024"]`         | 173.665 ms (5%) |         |   1.02 MiB (1%) |        1535 |
| `["collect", "unordered", "basesize=32"]`           | 180.332 ms (5%) |         |   1.61 MiB (1%) |       15664 |
| `["findfirst", "n=1000", "foldl"]`                  | 522.073 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 294.509 ms (5%) |         | 232.92 KiB (1%) |        3276 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 436.417 ms (5%) |         | 173.70 KiB (1%) |        2437 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 502.338 ms (5%) |         | 108.02 KiB (1%) |        1504 |
| `["findfirst", "n=400", "foldl"]`                   | 387.095 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 212.082 ms (5%) |         | 383.58 KiB (1%) |        5472 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 210.145 ms (5%) |         | 200.98 KiB (1%) |        2877 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 234.755 ms (5%) |         | 112.59 KiB (1%) |        1622 |
| `["findfirst", "n=500", "foldl"]`                   |  60.471 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 147.670 ms (5%) |         | 232.67 KiB (1%) |        3262 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 119.954 ms (5%) |         | 110.77 KiB (1%) |        1521 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 102.124 ms (5%) |         |  63.70 KiB (1%) |         867 |
| `["overhead", "default"]`                           |  68.800 μs (5%) |         |  32.73 KiB (1%) |         418 |
| `["overhead", "stoppable=false"]`                   |  68.801 μs (5%) |         |  32.72 KiB (1%) |         417 |
| `["overhead", "stoppable=true"]`                    |  79.600 μs (5%) |         |  44.22 KiB (1%) |         609 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   2.377 ms (5%) |         | 728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   3.052 ms (5%) |         |   2.05 MiB (1%) |         221 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   2.713 ms (5%) |         |   1.42 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  13.663 ms (5%) |         |   1.26 MiB (1%) |         607 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  24.315 ms (5%) |         |   1.26 MiB (1%) |        7401 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  22.534 ms (5%) |         |   1.25 MiB (1%) |        6203 |
| `["parallel_histogram", "seq"]`                     |   4.183 ms (5%) |         | 364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  31.490 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  15.930 ms (5%) |         |  736 bytes (1%) |          11 |
| `["splitby", "count", "foldl"]`                     |   1.587 ms (5%) |         |                 |             |
| `["splitby", "count", "man"]`                       |   1.223 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    | 741.005 μs (5%) |         |   1.06 KiB (1%) |          18 |
| `["sum", "random", "foldl"]`                        |  11.699 ms (5%) |         |                 |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   5.793 ms (5%) |         |  74.17 KiB (1%) |        1104 |
| `["sum", "random", "reduce", "basesize=256"]`       |   5.778 ms (5%) |         |  36.70 KiB (1%) |         545 |
| `["sum", "random", "reduce", "basesize=512"]`       |   5.698 ms (5%) |         |  18.08 KiB (1%) |         269 |
| `["sum", "uniform", "foldl"]`                       |  11.431 ms (5%) |         |                 |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   5.805 ms (5%) |         |  74.20 KiB (1%) |        1105 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   5.658 ms (5%) |         |  36.77 KiB (1%) |         547 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   6.470 ms (5%) |         |  18.03 KiB (1%) |         268 |
| `["sum", "valley", "foldl"]`                        |  11.691 ms (5%) |         |                 |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   5.889 ms (5%) |         |  74.08 KiB (1%) |        1101 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   5.851 ms (5%) |         |  36.70 KiB (1%) |         545 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   5.768 ms (5%) |         |  18.03 KiB (1%) |         268 |
| `["words", "nthreads=1"]`                           |  20.707 ms (5%) |         |  31.67 MiB (1%) |     1031825 |
| `["words", "nthreads=2"]`                           |  13.706 ms (5%) |         |  32.39 MiB (1%) |     1031930 |
| `["words", "nthreads=4"]`                           |  13.846 ms (5%) |         |  32.83 MiB (1%) |     1032044 |

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
  CPU: Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz: 
              speed         user         nice          sys         idle          irq
       #1  2294 MHz       7563 s          1 s        323 s       3546 s          0 s
       #2  2294 MHz       7923 s          2 s        328 s       3185 s          0 s
       
  Memory: 6.783611297607422 GB (3473.296875 MB free)
  Uptime: 1151.5 sec
  Load Avg:  1.68  1.59  1.13
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, broadwell)
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
    Model:                           79
    Model name:                      Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz
    Stepping:                        1
    CPU MHz:                         2294.684
    BogoMIPS:                        4589.36
    Hypervisor vendor:               Microsoft
    Virtualization type:             full
    L1d cache:                       64 KiB
    L1i cache:                       64 KiB
    L2 cache:                        512 KiB
    L3 cache:                        50 MiB
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
    Flags:                           fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush mmx fxsr sse sse2 ss ht syscall nx pdpe1gb rdtscp lm constant_tsc rep_good nopl xtopology cpuid pni pclmulqdq ssse3 fma cx16 pcid sse4_1 sse4_2 movbe popcnt aes xsave avx f16c rdrand hypervisor lahf_lm abm 3dnowprefetch invpcid_single pti fsgsbase bmi1 hle avx2 smep bmi2 erms invpcid rtm rdseed adx smap xsaveopt md_clear
    

| Cpu Property       | Value                                                   |
|:------------------ |:------------------------------------------------------- |
| Brand              | Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz               |
| Vendor             | :Intel                                                  |
| Architecture       | :Broadwell                                              |
| Model              | Family: 0x06, Model: 0x4f, Stepping: 0x01, Type: 0x00   |
| Cores              | 2 physical cores, 2 logical cores (on executing CPU)    |
|                    | No Hyperthreading hardware capability detected          |
| Clock Frequencies  | Not supported by CPU                                    |
| Data Cache         | Level 1:3 : (32, 256, 51200) kbytes                     |
|                    | 64 byte cache line size                                 |
| Address Size       | 48 bits virtual, 46 bits physical                       |
| SIMD               | 256 bit = 32 byte max. SIMD vector size                 |
| Time Stamp Counter | TSC is accessible via `rdtsc`                           |
|                    | TSC increased at every clock cycle (non-invariant TSC)  |
| Perf. Monitoring   | Performance Monitoring Counters (PMC) are not supported |
| Hypervisor         | Yes, Microsoft                                          |

