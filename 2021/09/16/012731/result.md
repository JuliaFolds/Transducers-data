# Multi-thread benchmark result

* Pull request commit: [`ff4b31c5c8936114a114315560d3c47bed7a8451`](https://github.com/JuliaFolds/Transducers.jl/commit/ff4b31c5c8936114a114315560d3c47bed7a8451)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/243> (Update */Manifest.toml)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 16 Sep 2021 - 01:21
    - Baseline: 16 Sep 2021 - 01:26
* Package commits:
    - Target: 26fe42
    - Baseline: 9ac175
* Julia commits:
    - Target: 69fcb5
    - Baseline: 69fcb5
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
| `["collect", "unordered", "basesize=1024"]`         | 0.91 (5%) :white_check_mark: | 0.93 (1%) :white_check_mark: |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` |                2.33 (5%) :x: |                2.22 (1%) :x: |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` |                   1.04 (5%)  |                1.04 (1%) :x: |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` |                   0.98 (5%)  |                1.05 (1%) :x: |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  |                1.11 (5%) :x: |                1.08 (1%) :x: |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  |                   0.97 (5%)  | 0.96 (1%) :white_check_mark: |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  |                   1.02 (5%)  |                1.06 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |                1.10 (5%) :x: |                1.01 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 0.70 (5%) :white_check_mark: | 0.82 (1%) :white_check_mark: |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |                2.13 (5%) :x: |                1.55 (1%) :x: |
| `["overhead", "default"]`                           |                1.05 (5%) :x: |                   1.00 (1%)  |
| `["parallel_histogram", "comm", "basesize=16384"]`  |                1.07 (5%) :x: | 0.80 (1%) :white_check_mark: |
| `["parallel_histogram", "comm", "basesize=4096"]`   | 0.93 (5%) :white_check_mark: |                1.04 (1%) :x: |
| `["parallel_histogram", "comm", "basesize=8192"]`   |                1.19 (5%) :x: |                1.02 (1%) :x: |
| `["splitby", "count", "reduce"]`                    |                   1.02 (5%)  | 0.97 (1%) :white_check_mark: |
| `["words", "nthreads=1"]`                           | 0.95 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["words", "nthreads=2"]`                           | 0.94 (5%) :white_check_mark: |                   1.00 (1%)  |

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
Julia Version 1.5.4
Commit 69fcb5745b (2021-03-11 19:13 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 20.04.3 LTS
  uname: Linux 5.8.0-1040-azure #43~20.04.1-Ubuntu SMP Mon Aug 2 22:06:11 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz      58378 s         19 s       2503 s      31503 s          0 s
       #2  2095 MHz      53791 s          6 s       2535 s      36214 s          0 s
       
  Memory: 6.790924072265625 GB (3343.49609375 MB free)
  Uptime: 933.0 sec
  Load Avg:  1.75732421875  1.5361328125  0.9208984375
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, skylake-avx512)
```

### Baseline
```
Julia Version 1.5.4
Commit 69fcb5745b (2021-03-11 19:13 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 20.04.3 LTS
  uname: Linux 5.8.0-1040-azure #43~20.04.1-Ubuntu SMP Mon Aug 2 22:06:11 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz      90166 s         19 s       3110 s      34069 s          0 s
       #2  2095 MHz      74425 s          6 s       3121 s      50058 s          0 s
       
  Memory: 6.790924072265625 GB (3316.11328125 MB free)
  Uptime: 1285.0 sec
  Load Avg:  1.798828125  1.6162109375  1.14208984375
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, skylake-avx512)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 16 Sep 2021 - 1:21
* Package commit: 26fe42
* Julia commit: 69fcb5
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
| `["collect", "assoc", "basesize=1"]`                | 296.625 ms (5%) |         |   32.66 MiB (1%) |      286746 |
| `["collect", "assoc", "basesize=1024"]`             | 249.032 ms (5%) |         |    1.79 MiB (1%) |         569 |
| `["collect", "assoc", "basesize=32"]`               | 252.221 ms (5%) |         |    3.97 MiB (1%) |       13306 |
| `["collect", "seq"]`                                | 494.429 ms (5%) |         |  512.72 KiB (1%) |          15 |
| `["collect", "unordered", "basesize=1"]`            | 540.565 ms (5%) |         |   30.01 MiB (1%) |      360577 |
| `["collect", "unordered", "basesize=1024"]`         | 332.337 ms (5%) |         |  882.89 KiB (1%) |        4992 |
| `["collect", "unordered", "basesize=32"]`           | 282.168 ms (5%) |         |    1.48 MiB (1%) |       12666 |
| `["findfirst", "n=1000", "foldl"]`                  | 782.121 ms (5%) |         |                  |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` |    1.017 s (5%) |         |    1.48 MiB (1%) |       26530 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 548.015 ms (5%) |         |  484.92 KiB (1%) |        8491 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 704.277 ms (5%) |         |  347.11 KiB (1%) |        6079 |
| `["findfirst", "n=400", "foldl"]`                   | 586.898 ms (5%) |         |                  |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 349.119 ms (5%) |         |    1.19 MiB (1%) |       21397 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 318.403 ms (5%) |         |  588.61 KiB (1%) |       10386 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 352.677 ms (5%) |         |  366.73 KiB (1%) |        6468 |
| `["findfirst", "n=500", "foldl"]`                   | 101.743 ms (5%) |         |                  |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 229.972 ms (5%) |         |  801.61 KiB (1%) |       13987 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 123.035 ms (5%) |         |  287.64 KiB (1%) |        5008 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 407.207 ms (5%) |         |  386.73 KiB (1%) |        6792 |
| `["overhead", "default"]`                           |  71.700 μs (5%) |         |   47.33 KiB (1%) |         381 |
| `["overhead", "stoppable=false"]`                   |  71.801 μs (5%) |         |   47.36 KiB (1%) |         381 |
| `["overhead", "stoppable=true"]`                    | 189.002 μs (5%) |         |  139.64 KiB (1%) |        2463 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   4.999 ms (5%) |         |  730.06 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   5.772 ms (5%) |         |    1.79 MiB (1%) |         213 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   5.383 ms (5%) |         |    1.43 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  16.264 ms (5%) |         | 1010.52 KiB (1%) |         595 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  25.961 ms (5%) |         |    1.06 MiB (1%) |        2537 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  21.888 ms (5%) |         |    1.26 MiB (1%) |        1536 |
| `["parallel_histogram", "seq"]`                     |   9.089 ms (5%) |         |  364.61 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  42.178 ms (5%) |         |                  |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  21.106 ms (5%) |         |    2.66 KiB (1%) |          48 |
| `["splitby", "count", "foldl"]`                     |   5.851 ms (5%) |         |    96 bytes (1%) |           4 |
| `["splitby", "count", "man"]`                       |   2.101 ms (5%) |         |                  |             |
| `["splitby", "count", "reduce"]`                    |   1.502 ms (5%) |         |    2.75 KiB (1%) |          51 |
| `["sum", "random", "foldl"]`                        |  19.964 ms (5%) |         |    32 bytes (1%) |           2 |
| `["sum", "random", "reduce", "basesize=128"]`       |  10.234 ms (5%) |         |  103.23 KiB (1%) |        1018 |
| `["sum", "random", "reduce", "basesize=256"]`       |  10.133 ms (5%) |         |   51.23 KiB (1%) |         506 |
| `["sum", "random", "reduce", "basesize=512"]`       |  10.059 ms (5%) |         |   25.30 KiB (1%) |         252 |
| `["sum", "uniform", "foldl"]`                       |  19.336 ms (5%) |         |    32 bytes (1%) |           2 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |  10.007 ms (5%) |         |  103.23 KiB (1%) |        1018 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   9.862 ms (5%) |         |   51.23 KiB (1%) |         506 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   9.803 ms (5%) |         |   25.25 KiB (1%) |         251 |
| `["sum", "valley", "foldl"]`                        |  20.029 ms (5%) |         |    32 bytes (1%) |           2 |
| `["sum", "valley", "reduce", "basesize=128"]`       |  10.278 ms (5%) |         |  103.23 KiB (1%) |        1018 |
| `["sum", "valley", "reduce", "basesize=256"]`       |  10.178 ms (5%) |         |   51.23 KiB (1%) |         506 |
| `["sum", "valley", "reduce", "basesize=512"]`       |  10.081 ms (5%) |         |   25.25 KiB (1%) |         251 |
| `["words", "nthreads=1"]`                           |  27.075 ms (5%) |         |   31.54 MiB (1%) |     1027357 |
| `["words", "nthreads=2"]`                           |  17.160 ms (5%) |         |   32.25 MiB (1%) |     1027429 |
| `["words", "nthreads=4"]`                           |  18.157 ms (5%) |         |   32.89 MiB (1%) |     1027580 |

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
Julia Version 1.5.4
Commit 69fcb5745b (2021-03-11 19:13 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 20.04.3 LTS
  uname: Linux 5.8.0-1040-azure #43~20.04.1-Ubuntu SMP Mon Aug 2 22:06:11 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz      58378 s         19 s       2503 s      31503 s          0 s
       #2  2095 MHz      53791 s          6 s       2535 s      36214 s          0 s
       
  Memory: 6.790924072265625 GB (3343.49609375 MB free)
  Uptime: 933.0 sec
  Load Avg:  1.75732421875  1.5361328125  0.9208984375
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, skylake-avx512)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 16 Sep 2021 - 1:26
* Package commit: 9ac175
* Julia commit: 69fcb5
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
| `["collect", "assoc", "basesize=1"]`                | 296.055 ms (5%) |         |  32.66 MiB (1%) |      286754 |
| `["collect", "assoc", "basesize=1024"]`             | 249.002 ms (5%) |         |   1.79 MiB (1%) |         570 |
| `["collect", "assoc", "basesize=32"]`               | 251.629 ms (5%) |         |   3.97 MiB (1%) |       13306 |
| `["collect", "seq"]`                                | 494.328 ms (5%) |         | 512.72 KiB (1%) |          15 |
| `["collect", "unordered", "basesize=1"]`            | 522.892 ms (5%) |         |  30.01 MiB (1%) |      360572 |
| `["collect", "unordered", "basesize=1024"]`         | 367.194 ms (5%) |         | 950.17 KiB (1%) |        7127 |
| `["collect", "unordered", "basesize=32"]`           | 278.941 ms (5%) |         |   1.47 MiB (1%) |       12603 |
| `["findfirst", "n=1000", "foldl"]`                  | 784.172 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 435.841 ms (5%) |         | 682.52 KiB (1%) |       11973 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 526.787 ms (5%) |         | 466.42 KiB (1%) |        8171 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 718.987 ms (5%) |         | 329.02 KiB (1%) |        5775 |
| `["findfirst", "n=400", "foldl"]`                   | 588.201 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 313.967 ms (5%) |         |   1.10 MiB (1%) |       19737 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 329.288 ms (5%) |         | 611.78 KiB (1%) |       10793 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 346.394 ms (5%) |         | 346.08 KiB (1%) |        6109 |
| `["findfirst", "n=500", "foldl"]`                   | 102.038 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 208.486 ms (5%) |         | 793.20 KiB (1%) |       13787 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 174.941 ms (5%) |         | 352.55 KiB (1%) |        6149 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 191.133 ms (5%) |         | 249.94 KiB (1%) |        4352 |
| `["overhead", "default"]`                           |  68.001 μs (5%) |         |  47.33 KiB (1%) |         381 |
| `["overhead", "stoppable=false"]`                   |  72.301 μs (5%) |         |  47.36 KiB (1%) |         381 |
| `["overhead", "stoppable=true"]`                    | 188.101 μs (5%) |         | 139.67 KiB (1%) |        2464 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   4.964 ms (5%) |         | 730.06 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   5.718 ms (5%) |         |   1.79 MiB (1%) |         213 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   5.351 ms (5%) |         |   1.43 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  15.255 ms (5%) |         |   1.23 MiB (1%) |         359 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  27.990 ms (5%) |         |   1.02 MiB (1%) |        1740 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  18.418 ms (5%) |         |   1.24 MiB (1%) |         810 |
| `["parallel_histogram", "seq"]`                     |   9.049 ms (5%) |         | 364.61 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  42.185 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  21.111 ms (5%) |         |   2.66 KiB (1%) |          48 |
| `["splitby", "count", "foldl"]`                     |   5.699 ms (5%) |         |   96 bytes (1%) |           4 |
| `["splitby", "count", "man"]`                       |   2.104 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    |   1.479 ms (5%) |         |   2.84 KiB (1%) |          54 |
| `["sum", "random", "foldl"]`                        |  19.996 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "random", "reduce", "basesize=128"]`       |  10.242 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "random", "reduce", "basesize=256"]`       |  10.127 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "random", "reduce", "basesize=512"]`       |  10.077 ms (5%) |         |  25.30 KiB (1%) |         252 |
| `["sum", "uniform", "foldl"]`                       |  19.350 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   9.938 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   9.847 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   9.765 ms (5%) |         |  25.25 KiB (1%) |         251 |
| `["sum", "valley", "foldl"]`                        |  19.972 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "valley", "reduce", "basesize=128"]`       |  10.288 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "valley", "reduce", "basesize=256"]`       |  10.186 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "valley", "reduce", "basesize=512"]`       |  10.123 ms (5%) |         |  25.25 KiB (1%) |         251 |
| `["words", "nthreads=1"]`                           |  28.516 ms (5%) |         |  31.57 MiB (1%) |     1028547 |
| `["words", "nthreads=2"]`                           |  18.216 ms (5%) |         |  32.28 MiB (1%) |     1028623 |
| `["words", "nthreads=4"]`                           |  18.758 ms (5%) |         |  32.91 MiB (1%) |     1028760 |

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
Julia Version 1.5.4
Commit 69fcb5745b (2021-03-11 19:13 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 20.04.3 LTS
  uname: Linux 5.8.0-1040-azure #43~20.04.1-Ubuntu SMP Mon Aug 2 22:06:11 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz      90166 s         19 s       3110 s      34069 s          0 s
       #2  2095 MHz      74425 s          6 s       3121 s      50058 s          0 s
       
  Memory: 6.790924072265625 GB (3316.11328125 MB free)
  Uptime: 1285.0 sec
  Load Avg:  1.798828125  1.6162109375  1.14208984375
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, skylake-avx512)
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
    CPU MHz:                         2095.076
    BogoMIPS:                        4190.15
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

