# Multi-thread benchmark result

* Pull request commit: [`3c7d80d5d8a29b25d6c8b5872338fcb8d421d7df`](https://github.com/JuliaFolds/Transducers.jl/commit/3c7d80d5d8a29b25d6c8b5872338fcb8d421d7df)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/243> (Update */Manifest.toml)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 28 Sep 2022 - 02:42
    - Baseline: 28 Sep 2022 - 02:47
* Package commits:
    - Target: b74e93
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
| `["findfirst", "n=1000", "reduce", "basesize=128"]` |                1.51 (5%) :x: |                1.48 (1%) :x: |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` |                   1.05 (5%)  | 0.96 (1%) :white_check_mark: |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 0.94 (5%) :white_check_mark: |                1.03 (1%) :x: |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  |                   0.98 (5%)  | 0.97 (1%) :white_check_mark: |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  |                1.07 (5%) :x: |                1.08 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |                1.19 (5%) :x: |                1.25 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |                3.36 (5%) :x: |                2.36 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 0.79 (5%) :white_check_mark: | 0.87 (1%) :white_check_mark: |
| `["parallel_histogram", "comm", "basesize=4096"]`   |                   1.04 (5%)  |                1.13 (1%) :x: |
| `["parallel_histogram", "comm", "basesize=8192"]`   |                   1.03 (5%)  |                1.03 (1%) :x: |
| `["partition_length_maximum", "rand", "reduce"]`    |                   0.99 (5%)  | 0.96 (1%) :white_check_mark: |
| `["splitby", "count", "man"]`                       | 0.81 (5%) :white_check_mark: |                   1.00 (1%)  |

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
  uname: Linux 5.15.0-1020-azure #25~20.04.1-Ubuntu SMP Thu Sep 1 19:20:56 UTC 2022 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz       5327 s          2 s        254 s       2888 s          0 s
       #2  2095 MHz       5478 s          1 s        272 s       2739 s          0 s
       
  Memory: 6.781253814697266 GB (3654.44921875 MB free)
  Uptime: 854.02 sec
  Load Avg:  1.59  1.48  0.93
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
  uname: Linux 5.15.0-1020-azure #25~20.04.1-Ubuntu SMP Thu Sep 1 19:20:56 UTC 2022 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz       7733 s          2 s        335 s       3666 s          0 s
       #2  2095 MHz       8021 s          1 s        351 s       3381 s          0 s
       
  Memory: 6.781253814697266 GB (3644.83984375 MB free)
  Uptime: 1181.13 sec
  Load Avg:  1.43  1.55  1.14
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, skylake-avx512)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 28 Sep 2022 - 2:42
* Package commit: b74e93
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
| `["collect", "assoc", "basesize=1"]`                | 303.476 ms (5%) |         |  25.97 MiB (1%) |      306827 |
| `["collect", "assoc", "basesize=1024"]`             | 248.014 ms (5%) |         |   2.61 MiB (1%) |         456 |
| `["collect", "assoc", "basesize=32"]`               | 250.365 ms (5%) |         |   4.82 MiB (1%) |       11715 |
| `["collect", "seq"]`                                | 494.119 ms (5%) |         | 812.73 KiB (1%) |          11 |
| `["collect", "unordered", "basesize=1"]`            | 431.464 ms (5%) |         |  23.85 MiB (1%) |      411367 |
| `["collect", "unordered", "basesize=1024"]`         | 265.940 ms (5%) |         |   1.01 MiB (1%) |        1041 |
| `["collect", "unordered", "basesize=32"]`           | 280.010 ms (5%) |         |   1.58 MiB (1%) |       14715 |
| `["findfirst", "n=1000", "foldl"]`                  | 787.724 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 663.689 ms (5%) |         | 343.88 KiB (1%) |        4827 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 530.088 ms (5%) |         | 157.20 KiB (1%) |        2193 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 725.305 ms (5%) |         | 103.53 KiB (1%) |        1454 |
| `["findfirst", "n=400", "foldl"]`                   | 590.794 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 309.087 ms (5%) |         | 388.36 KiB (1%) |        5515 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 316.580 ms (5%) |         | 202.73 KiB (1%) |        2905 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 441.490 ms (5%) |         | 144.89 KiB (1%) |        2062 |
| `["findfirst", "n=500", "foldl"]`                   | 102.359 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 255.258 ms (5%) |         | 279.12 KiB (1%) |        3879 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 292.820 ms (5%) |         | 170.94 KiB (1%) |        2383 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 265.277 ms (5%) |         |  93.66 KiB (1%) |        1274 |
| `["overhead", "default"]`                           |  92.607 μs (5%) |         |  32.70 KiB (1%) |         417 |
| `["overhead", "stoppable=false"]`                   |  90.706 μs (5%) |         |  32.75 KiB (1%) |         418 |
| `["overhead", "stoppable=true"]`                    |  99.707 μs (5%) |         |  44.25 KiB (1%) |         610 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   4.070 ms (5%) |         | 728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   4.877 ms (5%) |         |   1.79 MiB (1%) |         215 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   4.497 ms (5%) |         |   1.42 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  20.221 ms (5%) |         |   1.57 MiB (1%) |        2170 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  28.036 ms (5%) |         |   1.23 MiB (1%) |        6557 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  25.761 ms (5%) |         |   1.31 MiB (1%) |        5887 |
| `["parallel_histogram", "seq"]`                     |   7.209 ms (5%) |         | 364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  44.030 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  21.990 ms (5%) |         |  704 bytes (1%) |          10 |
| `["splitby", "count", "foldl"]`                     |   2.870 ms (5%) |         |                 |             |
| `["splitby", "count", "man"]`                       |   1.767 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    |   1.475 ms (5%) |         |   1.09 KiB (1%) |          19 |
| `["sum", "random", "foldl"]`                        |  20.479 ms (5%) |         |                 |             |
| `["sum", "random", "reduce", "basesize=128"]`       |  10.342 ms (5%) |         |  74.08 KiB (1%) |        1101 |
| `["sum", "random", "reduce", "basesize=256"]`       |  10.224 ms (5%) |         |  36.80 KiB (1%) |         548 |
| `["sum", "random", "reduce", "basesize=512"]`       |  10.170 ms (5%) |         |  18.05 KiB (1%) |         268 |
| `["sum", "uniform", "foldl"]`                       |  19.501 ms (5%) |         |                 |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |  10.004 ms (5%) |         |  74.17 KiB (1%) |        1104 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   9.882 ms (5%) |         |  36.77 KiB (1%) |         547 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   9.776 ms (5%) |         |  18.03 KiB (1%) |         268 |
| `["sum", "valley", "foldl"]`                        |  20.198 ms (5%) |         |                 |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |  10.366 ms (5%) |         |  74.17 KiB (1%) |        1104 |
| `["sum", "valley", "reduce", "basesize=256"]`       |  10.202 ms (5%) |         |  36.73 KiB (1%) |         546 |
| `["sum", "valley", "reduce", "basesize=512"]`       |  10.201 ms (5%) |         |  18.00 KiB (1%) |         267 |
| `["words", "nthreads=1"]`                           |  27.168 ms (5%) |         |  31.50 MiB (1%) |     1025993 |
| `["words", "nthreads=2"]`                           |  17.457 ms (5%) |         |  32.21 MiB (1%) |     1026078 |
| `["words", "nthreads=4"]`                           |  17.559 ms (5%) |         |  32.66 MiB (1%) |     1026148 |

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
  uname: Linux 5.15.0-1020-azure #25~20.04.1-Ubuntu SMP Thu Sep 1 19:20:56 UTC 2022 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz       5327 s          2 s        254 s       2888 s          0 s
       #2  2095 MHz       5478 s          1 s        272 s       2739 s          0 s
       
  Memory: 6.781253814697266 GB (3654.44921875 MB free)
  Uptime: 854.02 sec
  Load Avg:  1.59  1.48  0.93
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, skylake-avx512)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 28 Sep 2022 - 2:47
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
| `["collect", "assoc", "basesize=1"]`                | 304.132 ms (5%) |         |  25.97 MiB (1%) |      306768 |
| `["collect", "assoc", "basesize=1024"]`             | 248.609 ms (5%) |         |   2.61 MiB (1%) |         456 |
| `["collect", "assoc", "basesize=32"]`               | 252.734 ms (5%) |         |   4.82 MiB (1%) |       11724 |
| `["collect", "seq"]`                                | 494.209 ms (5%) |         | 812.73 KiB (1%) |          11 |
| `["collect", "unordered", "basesize=1"]`            | 433.452 ms (5%) |         |  23.81 MiB (1%) |      409894 |
| `["collect", "unordered", "basesize=1024"]`         | 269.569 ms (5%) |         |   1.01 MiB (1%) |         950 |
| `["collect", "unordered", "basesize=32"]`           | 279.592 ms (5%) |         |   1.58 MiB (1%) |       14769 |
| `["findfirst", "n=1000", "foldl"]`                  | 787.816 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 438.278 ms (5%) |         | 232.83 KiB (1%) |        3275 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 532.039 ms (5%) |         | 157.20 KiB (1%) |        2193 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 693.129 ms (5%) |         | 107.95 KiB (1%) |        1502 |
| `["findfirst", "n=400", "foldl"]`                   | 591.010 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 328.532 ms (5%) |         | 376.53 KiB (1%) |        5363 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 322.143 ms (5%) |         | 209.94 KiB (1%) |        3004 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 412.427 ms (5%) |         | 134.25 KiB (1%) |        1912 |
| `["findfirst", "n=500", "foldl"]`                   | 102.348 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 213.810 ms (5%) |         | 224.19 KiB (1%) |        3137 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |  87.257 ms (5%) |         |  72.28 KiB (1%) |         981 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 337.678 ms (5%) |         | 107.53 KiB (1%) |        1485 |
| `["overhead", "default"]`                           |  89.007 μs (5%) |         |  32.73 KiB (1%) |         418 |
| `["overhead", "stoppable=false"]`                   |  89.107 μs (5%) |         |  32.75 KiB (1%) |         418 |
| `["overhead", "stoppable=true"]`                    | 103.407 μs (5%) |         |  44.25 KiB (1%) |         610 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   4.064 ms (5%) |         | 728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   4.866 ms (5%) |         |   1.79 MiB (1%) |         215 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   4.479 ms (5%) |         |   1.42 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  19.830 ms (5%) |         |   1.58 MiB (1%) |        2492 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  27.000 ms (5%) |         |   1.09 MiB (1%) |        4473 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  25.120 ms (5%) |         |   1.28 MiB (1%) |        3237 |
| `["parallel_histogram", "seq"]`                     |   7.234 ms (5%) |         | 364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  44.076 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  22.243 ms (5%) |         |  736 bytes (1%) |          11 |
| `["splitby", "count", "foldl"]`                     |   2.917 ms (5%) |         |                 |             |
| `["splitby", "count", "man"]`                       |   2.193 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    |   1.434 ms (5%) |         |   1.09 KiB (1%) |          19 |
| `["sum", "random", "foldl"]`                        |  20.176 ms (5%) |         |                 |             |
| `["sum", "random", "reduce", "basesize=128"]`       |  10.203 ms (5%) |         |  74.20 KiB (1%) |        1105 |
| `["sum", "random", "reduce", "basesize=256"]`       |  10.023 ms (5%) |         |  36.70 KiB (1%) |         545 |
| `["sum", "random", "reduce", "basesize=512"]`       |  10.014 ms (5%) |         |  18.11 KiB (1%) |         270 |
| `["sum", "uniform", "foldl"]`                       |  19.643 ms (5%) |         |                 |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |  10.014 ms (5%) |         |  74.20 KiB (1%) |        1105 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   9.866 ms (5%) |         |  36.77 KiB (1%) |         547 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   9.770 ms (5%) |         |  18.03 KiB (1%) |         268 |
| `["sum", "valley", "foldl"]`                        |  20.189 ms (5%) |         |                 |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |  10.312 ms (5%) |         |  74.14 KiB (1%) |        1103 |
| `["sum", "valley", "reduce", "basesize=256"]`       |  10.208 ms (5%) |         |  36.70 KiB (1%) |         545 |
| `["sum", "valley", "reduce", "basesize=512"]`       |  10.153 ms (5%) |         |  18.03 KiB (1%) |         268 |
| `["words", "nthreads=1"]`                           |  28.318 ms (5%) |         |  31.75 MiB (1%) |     1034354 |
| `["words", "nthreads=2"]`                           |  17.600 ms (5%) |         |  32.10 MiB (1%) |     1034399 |
| `["words", "nthreads=4"]`                           |  17.620 ms (5%) |         |  32.82 MiB (1%) |     1034479 |

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
  uname: Linux 5.15.0-1020-azure #25~20.04.1-Ubuntu SMP Thu Sep 1 19:20:56 UTC 2022 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz       7733 s          2 s        335 s       3666 s          0 s
       #2  2095 MHz       8021 s          1 s        351 s       3381 s          0 s
       
  Memory: 6.781253814697266 GB (3644.83984375 MB free)
  Uptime: 1181.13 sec
  Load Avg:  1.43  1.55  1.14
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
    CPU MHz:                         2095.196
    BogoMIPS:                        4190.39
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
    Flags:                           fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush mmx fxsr sse sse2 ss ht syscall nx pdpe1gb rdtscp lm constant_tsc rep_good nopl xtopology cpuid pni pclmulqdq ssse3 fma cx16 pcid sse4_1 sse4_2 movbe popcnt aes xsave avx f16c rdrand hypervisor lahf_lm abm 3dnowprefetch invpcid_single pti fsgsbase bmi1 hle avx2 smep bmi2 erms invpcid rtm mpx avx512f avx512dq rdseed adx smap clflushopt avx512cd avx512bw avx512vl xsaveopt xsavec xsaves md_clear
    

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

