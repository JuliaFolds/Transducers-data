# Multi-thread benchmark result

* Pull request commit: [`f2083783c026975e258551f405bb44ca8df1cc47`](https://github.com/JuliaFolds/Transducers.jl/commit/f2083783c026975e258551f405bb44ca8df1cc47)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/243> (Update */Manifest.toml)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 19 Aug 2022 - 02:32
    - Baseline: 19 Aug 2022 - 02:37
* Package commits:
    - Target: f25b25
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
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 0.80 (5%) :white_check_mark: | 0.80 (1%) :white_check_mark: |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` |                2.05 (5%) :x: |                1.94 (1%) :x: |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  |                   1.02 (5%)  |                1.01 (1%) :x: |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  |                   0.99 (5%)  | 0.97 (1%) :white_check_mark: |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  |                1.17 (5%) :x: |                1.21 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |                   0.96 (5%)  | 0.94 (1%) :white_check_mark: |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |                1.22 (5%) :x: |                1.15 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 0.90 (5%) :white_check_mark: | 0.88 (1%) :white_check_mark: |
| `["parallel_histogram", "assoc", "basesize=16384"]` |                1.08 (5%) :x: |                   1.00 (1%)  |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |                1.05 (5%) :x: |                   1.00 (1%)  |
| `["parallel_histogram", "comm", "basesize=16384"]`  |                1.05 (5%) :x: |                   1.01 (1%)  |
| `["parallel_histogram", "comm", "basesize=4096"]`   |                   0.99 (5%)  |                1.02 (1%) :x: |
| `["parallel_histogram", "comm", "basesize=8192"]`   |                1.16 (5%) :x: | 0.98 (1%) :white_check_mark: |
| `["partition_length_maximum", "rand", "reduce"]`    |                   1.02 (5%)  | 0.96 (1%) :white_check_mark: |
| `["splitby", "count", "foldl"]`                     | 0.94 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["splitby", "count", "reduce"]`                    | 0.82 (5%) :white_check_mark: | 0.93 (1%) :white_check_mark: |
| `["sum", "random", "reduce", "basesize=128"]`       | 0.93 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["sum", "uniform", "foldl"]`                       | 0.93 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["sum", "valley", "reduce", "basesize=128"]`       | 0.91 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["sum", "valley", "reduce", "basesize=256"]`       | 0.94 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["sum", "valley", "reduce", "basesize=512"]`       | 0.94 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["words", "nthreads=1"]`                           | 0.94 (5%) :white_check_mark: |                   1.01 (1%)  |

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
  uname: Linux 5.15.0-1017-azure #20~20.04.1-Ubuntu SMP Fri Aug 5 12:16:53 UTC 2022 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz       5407 s          1 s        226 s       3179 s          0 s
       #2  2095 MHz       5170 s          1 s        258 s       3412 s          0 s
       
  Memory: 6.781246185302734 GB (3707.1328125 MB free)
  Uptime: 888.77 sec
  Load Avg:  1.56  1.46  0.89
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
  uname: Linux 5.15.0-1017-azure #20~20.04.1-Ubuntu SMP Fri Aug 5 12:16:53 UTC 2022 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz       7639 s          1 s        298 s       4110 s          0 s
       #2  2095 MHz       7861 s          1 s        322 s       3896 s          0 s
       
  Memory: 6.781246185302734 GB (3675.19921875 MB free)
  Uptime: 1213.04 sec
  Load Avg:  1.69  1.62  1.13
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, skylake-avx512)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 19 Aug 2022 - 2:32
* Package commit: f25b25
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
| `["collect", "assoc", "basesize=1"]`                | 298.368 ms (5%) |         |   25.97 MiB (1%) |      306805 |
| `["collect", "assoc", "basesize=1024"]`             | 232.743 ms (5%) |         |    2.61 MiB (1%) |         456 |
| `["collect", "assoc", "basesize=32"]`               | 240.744 ms (5%) |         |    4.82 MiB (1%) |       11713 |
| `["collect", "seq"]`                                | 456.533 ms (5%) |         |  812.73 KiB (1%) |          11 |
| `["collect", "unordered", "basesize=1"]`            | 414.688 ms (5%) |         |   23.87 MiB (1%) |      412156 |
| `["collect", "unordered", "basesize=1024"]`         | 256.091 ms (5%) |         | 1010.61 KiB (1%) |         923 |
| `["collect", "unordered", "basesize=32"]`           | 265.858 ms (5%) |         |    1.58 MiB (1%) |       14574 |
| `["findfirst", "n=1000", "foldl"]`                  | 752.570 ms (5%) |         |                  |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 413.395 ms (5%) |         |  232.98 KiB (1%) |        3280 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 576.243 ms (5%) |         |  162.83 KiB (1%) |        2294 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` |    1.067 s (5%) |         |  157.78 KiB (1%) |        2218 |
| `["findfirst", "n=400", "foldl"]`                   | 558.316 ms (5%) |         |                  |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 309.111 ms (5%) |         |  386.42 KiB (1%) |        5498 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 299.811 ms (5%) |         |  201.14 KiB (1%) |        2882 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 403.075 ms (5%) |         |  145.41 KiB (1%) |        2069 |
| `["findfirst", "n=500", "foldl"]`                   |  93.564 ms (5%) |         |                  |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 210.090 ms (5%) |         |  247.91 KiB (1%) |        3378 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 263.409 ms (5%) |         |  158.38 KiB (1%) |        2220 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 125.659 ms (5%) |         |   55.91 KiB (1%) |         762 |
| `["overhead", "default"]`                           |  86.004 μs (5%) |         |   32.73 KiB (1%) |         418 |
| `["overhead", "stoppable=false"]`                   |  85.604 μs (5%) |         |   32.75 KiB (1%) |         418 |
| `["overhead", "stoppable=true"]`                    | 100.504 μs (5%) |         |   44.25 KiB (1%) |         610 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   3.901 ms (5%) |         |  728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   4.556 ms (5%) |         |    1.79 MiB (1%) |         215 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   4.212 ms (5%) |         |    1.42 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  21.640 ms (5%) |         |    1.61 MiB (1%) |        3332 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  28.463 ms (5%) |         |    1.25 MiB (1%) |        6981 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  26.372 ms (5%) |         |    1.24 MiB (1%) |        5757 |
| `["parallel_histogram", "seq"]`                     |   6.390 ms (5%) |         |  364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  39.138 ms (5%) |         |                  |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  20.467 ms (5%) |         |   704 bytes (1%) |          10 |
| `["splitby", "count", "foldl"]`                     |   2.215 ms (5%) |         |                  |             |
| `["splitby", "count", "man"]`                       |   1.303 ms (5%) |         |                  |             |
| `["splitby", "count", "reduce"]`                    |   1.066 ms (5%) |         |    1.02 KiB (1%) |          18 |
| `["sum", "random", "foldl"]`                        |  18.899 ms (5%) |         |                  |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   8.859 ms (5%) |         |   74.20 KiB (1%) |        1105 |
| `["sum", "random", "reduce", "basesize=256"]`       |   9.493 ms (5%) |         |   36.77 KiB (1%) |         547 |
| `["sum", "random", "reduce", "basesize=512"]`       |   9.294 ms (5%) |         |   18.02 KiB (1%) |         267 |
| `["sum", "uniform", "foldl"]`                       |  17.068 ms (5%) |         |                  |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   9.054 ms (5%) |         |   74.11 KiB (1%) |        1102 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   8.722 ms (5%) |         |   36.70 KiB (1%) |         545 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   8.538 ms (5%) |         |   18.03 KiB (1%) |         268 |
| `["sum", "valley", "foldl"]`                        |  17.647 ms (5%) |         |                  |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   9.035 ms (5%) |         |   74.11 KiB (1%) |        1102 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   9.205 ms (5%) |         |   36.73 KiB (1%) |         546 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   9.230 ms (5%) |         |   18.03 KiB (1%) |         268 |
| `["words", "nthreads=1"]`                           |  27.676 ms (5%) |         |   31.91 MiB (1%) |     1039572 |
| `["words", "nthreads=2"]`                           |  17.543 ms (5%) |         |   32.26 MiB (1%) |     1039608 |
| `["words", "nthreads=4"]`                           |  17.564 ms (5%) |         |   32.98 MiB (1%) |     1039682 |

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
  uname: Linux 5.15.0-1017-azure #20~20.04.1-Ubuntu SMP Fri Aug 5 12:16:53 UTC 2022 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz       5407 s          1 s        226 s       3179 s          0 s
       #2  2095 MHz       5170 s          1 s        258 s       3412 s          0 s
       
  Memory: 6.781246185302734 GB (3707.1328125 MB free)
  Uptime: 888.77 sec
  Load Avg:  1.56  1.46  0.89
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, skylake-avx512)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 19 Aug 2022 - 2:37
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
| `["collect", "assoc", "basesize=1"]`                | 293.454 ms (5%) |         |   25.97 MiB (1%) |      306783 |
| `["collect", "assoc", "basesize=1024"]`             | 238.073 ms (5%) |         |    2.61 MiB (1%) |         457 |
| `["collect", "assoc", "basesize=32"]`               | 236.280 ms (5%) |         |    4.82 MiB (1%) |       11717 |
| `["collect", "seq"]`                                | 468.604 ms (5%) |         |  812.73 KiB (1%) |          11 |
| `["collect", "unordered", "basesize=1"]`            | 416.853 ms (5%) |         |   23.89 MiB (1%) |      412629 |
| `["collect", "unordered", "basesize=1024"]`         | 254.764 ms (5%) |         | 1006.20 KiB (1%) |        1025 |
| `["collect", "unordered", "basesize=32"]`           | 264.203 ms (5%) |         |    1.58 MiB (1%) |       14768 |
| `["findfirst", "n=1000", "foldl"]`                  | 730.784 ms (5%) |         |                  |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 416.379 ms (5%) |         |  232.80 KiB (1%) |        3274 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 720.826 ms (5%) |         |  202.73 KiB (1%) |        2867 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 521.688 ms (5%) |         |   81.30 KiB (1%) |        1145 |
| `["findfirst", "n=400", "foldl"]`                   | 560.681 ms (5%) |         |                  |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 303.423 ms (5%) |         |  381.58 KiB (1%) |        5436 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 303.143 ms (5%) |         |  208.03 KiB (1%) |        2969 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 345.021 ms (5%) |         |  120.28 KiB (1%) |        1722 |
| `["findfirst", "n=500", "foldl"]`                   |  95.292 ms (5%) |         |                  |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 219.481 ms (5%) |         |  262.58 KiB (1%) |        3588 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 216.175 ms (5%) |         |  138.22 KiB (1%) |        1896 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 140.274 ms (5%) |         |   63.59 KiB (1%) |         863 |
| `["overhead", "default"]`                           |  83.615 μs (5%) |         |   32.77 KiB (1%) |         419 |
| `["overhead", "stoppable=false"]`                   |  86.716 μs (5%) |         |   32.75 KiB (1%) |         418 |
| `["overhead", "stoppable=true"]`                    |  97.118 μs (5%) |         |   44.28 KiB (1%) |         611 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   3.610 ms (5%) |         |  728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   4.326 ms (5%) |         |    1.79 MiB (1%) |         216 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   4.135 ms (5%) |         |    1.42 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  20.525 ms (5%) |         |    1.60 MiB (1%) |        2979 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  28.710 ms (5%) |         |    1.22 MiB (1%) |        6117 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  22.712 ms (5%) |         |    1.27 MiB (1%) |        4520 |
| `["parallel_histogram", "seq"]`                     |   6.161 ms (5%) |         |  364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  39.173 ms (5%) |         |                  |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  20.011 ms (5%) |         |   736 bytes (1%) |          11 |
| `["splitby", "count", "foldl"]`                     |   2.368 ms (5%) |         |                  |             |
| `["splitby", "count", "man"]`                       |   1.309 ms (5%) |         |                  |             |
| `["splitby", "count", "reduce"]`                    |   1.293 ms (5%) |         |    1.09 KiB (1%) |          19 |
| `["sum", "random", "foldl"]`                        |  18.435 ms (5%) |         |                  |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   9.560 ms (5%) |         |   74.17 KiB (1%) |        1104 |
| `["sum", "random", "reduce", "basesize=256"]`       |   9.274 ms (5%) |         |   36.70 KiB (1%) |         545 |
| `["sum", "random", "reduce", "basesize=512"]`       |   8.989 ms (5%) |         |   18.05 KiB (1%) |         268 |
| `["sum", "uniform", "foldl"]`                       |  18.345 ms (5%) |         |                  |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   9.098 ms (5%) |         |   74.14 KiB (1%) |        1103 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   8.902 ms (5%) |         |   36.77 KiB (1%) |         547 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   8.967 ms (5%) |         |   18.03 KiB (1%) |         268 |
| `["sum", "valley", "foldl"]`                        |  18.442 ms (5%) |         |                  |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   9.886 ms (5%) |         |   74.08 KiB (1%) |        1101 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   9.743 ms (5%) |         |   36.73 KiB (1%) |         546 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   9.801 ms (5%) |         |   18.03 KiB (1%) |         268 |
| `["words", "nthreads=1"]`                           |  29.531 ms (5%) |         |   31.68 MiB (1%) |     1032362 |
| `["words", "nthreads=2"]`                           |  16.876 ms (5%) |         |   32.04 MiB (1%) |     1032398 |
| `["words", "nthreads=4"]`                           |  17.732 ms (5%) |         |   32.93 MiB (1%) |     1032559 |

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
  uname: Linux 5.15.0-1017-azure #20~20.04.1-Ubuntu SMP Fri Aug 5 12:16:53 UTC 2022 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz       7639 s          1 s        298 s       4110 s          0 s
       #2  2095 MHz       7861 s          1 s        322 s       3896 s          0 s
       
  Memory: 6.781246185302734 GB (3675.19921875 MB free)
  Uptime: 1213.04 sec
  Load Avg:  1.69  1.62  1.13
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
    Model name:                      Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz
    Stepping:                        4
    CPU MHz:                         2095.222
    BogoMIPS:                        4190.44
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

