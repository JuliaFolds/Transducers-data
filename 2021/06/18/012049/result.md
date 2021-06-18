# Multi-thread benchmark result

* Pull request commit: [`e9f37daadb08f54595077d822448d7cb4956a049`](https://github.com/JuliaFolds/Transducers.jl/commit/e9f37daadb08f54595077d822448d7cb4956a049)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/243> (Update */Manifest.toml)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 18 Jun 2021 - 01:15
    - Baseline: 18 Jun 2021 - 01:20
* Package commits:
    - Target: 7acb74
    - Baseline: 2cfb4c
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
| `["collect", "unordered", "basesize=1024"]`         |                1.23 (5%) :x: |                1.19 (1%) :x: |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` |                1.80 (5%) :x: |                1.68 (1%) :x: |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` |                1.07 (5%) :x: |                1.04 (1%) :x: |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` |                1.24 (5%) :x: |                1.12 (1%) :x: |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 0.92 (5%) :white_check_mark: | 0.88 (1%) :white_check_mark: |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 0.77 (5%) :white_check_mark: | 0.81 (1%) :white_check_mark: |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |                1.21 (5%) :x: |                1.31 (1%) :x: |
| `["parallel_histogram", "comm", "basesize=4096"]`   |                   1.05 (5%)  |                1.03 (1%) :x: |
| `["splitby", "count", "man"]`                       | 0.90 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["splitby", "count", "reduce"]`                    |                   0.96 (5%)  | 0.99 (1%) :white_check_mark: |
| `["words", "nthreads=2"]`                           |                1.06 (5%) :x: |                   1.00 (1%)  |

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
      Ubuntu 20.04.2 LTS
  uname: Linux 5.8.0-1033-azure #35~20.04.1-Ubuntu SMP Wed May 19 06:46:04 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2593 MHz      46812 s         12 s       2093 s      23662 s          0 s
       #2  2593 MHz      57811 s          9 s       2238 s      12777 s          0 s
       
  Memory: 6.790924072265625 GB (3516.984375 MB free)
  Uptime: 733.0 sec
  Load Avg:  1.70556640625  1.52978515625  0.9091796875
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
      Ubuntu 20.04.2 LTS
  uname: Linux 5.8.0-1033-azure #35~20.04.1-Ubuntu SMP Wed May 19 06:46:04 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2593 MHz      66860 s         12 s       2711 s      35212 s          0 s
       #2  2593 MHz      86376 s          9 s       2903 s      15616 s          0 s
       
  Memory: 6.790924072265625 GB (3498.265625 MB free)
  Uptime: 1056.0 sec
  Load Avg:  1.76904296875  1.6025390625  1.1171875
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, skylake-avx512)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 18 Jun 2021 - 1:15
* Package commit: 7acb74
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
| `["collect", "assoc", "basesize=1"]`                | 235.994 ms (5%) |         |  32.66 MiB (1%) |      286727 |
| `["collect", "assoc", "basesize=1024"]`             | 198.165 ms (5%) |         |   1.79 MiB (1%) |         570 |
| `["collect", "assoc", "basesize=32"]`               | 199.934 ms (5%) |         |   3.97 MiB (1%) |       13305 |
| `["collect", "seq"]`                                | 394.929 ms (5%) |         | 512.72 KiB (1%) |          15 |
| `["collect", "unordered", "basesize=1"]`            | 408.301 ms (5%) |         |  30.01 MiB (1%) |      360559 |
| `["collect", "unordered", "basesize=1024"]`         | 288.107 ms (5%) |         | 952.64 KiB (1%) |        7224 |
| `["collect", "unordered", "basesize=32"]`           | 222.420 ms (5%) |         |   1.47 MiB (1%) |       12555 |
| `["findfirst", "n=1000", "foldl"]`                  | 627.457 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 695.497 ms (5%) |         |   1.28 MiB (1%) |       22927 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 444.023 ms (5%) |         | 484.97 KiB (1%) |        8496 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 652.218 ms (5%) |         | 359.17 KiB (1%) |        6307 |
| `["findfirst", "n=400", "foldl"]`                   | 470.604 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 247.550 ms (5%) |         |   1.09 MiB (1%) |       19667 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 254.408 ms (5%) |         | 599.97 KiB (1%) |       10577 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 258.585 ms (5%) |         | 332.13 KiB (1%) |        5864 |
| `["findfirst", "n=500", "foldl"]`                   |  81.643 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 148.422 ms (5%) |         | 696.25 KiB (1%) |       12124 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 128.681 ms (5%) |         | 363.75 KiB (1%) |        6336 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 133.556 ms (5%) |         | 220.02 KiB (1%) |        3829 |
| `["overhead", "default"]`                           |  58.800 μs (5%) |         |  47.36 KiB (1%) |         382 |
| `["overhead", "stoppable=false"]`                   |  58.000 μs (5%) |         |  47.39 KiB (1%) |         382 |
| `["overhead", "stoppable=true"]`                    | 149.901 μs (5%) |         | 139.67 KiB (1%) |        2464 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   3.972 ms (5%) |         | 730.06 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   4.571 ms (5%) |         |   1.79 MiB (1%) |         213 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   4.272 ms (5%) |         |   1.43 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  12.779 ms (5%) |         |   1.23 MiB (1%) |         385 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  22.370 ms (5%) |         |   1.07 MiB (1%) |        2574 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  17.875 ms (5%) |         |   1.26 MiB (1%) |        1383 |
| `["parallel_histogram", "seq"]`                     |   7.258 ms (5%) |         | 364.61 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  33.705 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  16.865 ms (5%) |         |   2.66 KiB (1%) |          48 |
| `["splitby", "count", "foldl"]`                     |   4.694 ms (5%) |         |   96 bytes (1%) |           4 |
| `["splitby", "count", "man"]`                       |   1.735 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    |   1.169 ms (5%) |         |   2.84 KiB (1%) |          54 |
| `["sum", "random", "foldl"]`                        |  15.910 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "random", "reduce", "basesize=128"]`       |   8.141 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "random", "reduce", "basesize=256"]`       |   8.061 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "random", "reduce", "basesize=512"]`       |   8.006 ms (5%) |         |  25.30 KiB (1%) |         252 |
| `["sum", "uniform", "foldl"]`                       |  15.470 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   7.949 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   7.850 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   7.806 ms (5%) |         |  25.25 KiB (1%) |         251 |
| `["sum", "valley", "foldl"]`                        |  15.966 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "valley", "reduce", "basesize=128"]`       |   8.183 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   8.101 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   8.033 ms (5%) |         |  25.25 KiB (1%) |         251 |
| `["words", "nthreads=1"]`                           |  21.870 ms (5%) |         |  31.78 MiB (1%) |     1035470 |
| `["words", "nthreads=2"]`                           |  13.868 ms (5%) |         |  32.14 MiB (1%) |     1035506 |
| `["words", "nthreads=4"]`                           |  14.476 ms (5%) |         |  33.04 MiB (1%) |     1035707 |

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
      Ubuntu 20.04.2 LTS
  uname: Linux 5.8.0-1033-azure #35~20.04.1-Ubuntu SMP Wed May 19 06:46:04 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2593 MHz      46812 s         12 s       2093 s      23662 s          0 s
       #2  2593 MHz      57811 s          9 s       2238 s      12777 s          0 s
       
  Memory: 6.790924072265625 GB (3516.984375 MB free)
  Uptime: 733.0 sec
  Load Avg:  1.70556640625  1.52978515625  0.9091796875
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, skylake-avx512)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 18 Jun 2021 - 1:20
* Package commit: 2cfb4c
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
| `["collect", "assoc", "basesize=1"]`                | 236.079 ms (5%) |         |  32.66 MiB (1%) |      286734 |
| `["collect", "assoc", "basesize=1024"]`             | 198.479 ms (5%) |         |   1.79 MiB (1%) |         570 |
| `["collect", "assoc", "basesize=32"]`               | 199.971 ms (5%) |         |   3.97 MiB (1%) |       13306 |
| `["collect", "seq"]`                                | 395.177 ms (5%) |         | 512.72 KiB (1%) |          15 |
| `["collect", "unordered", "basesize=1"]`            | 404.170 ms (5%) |         |  30.01 MiB (1%) |      360562 |
| `["collect", "unordered", "basesize=1024"]`         | 233.726 ms (5%) |         | 800.58 KiB (1%) |        2340 |
| `["collect", "unordered", "basesize=32"]`           | 223.231 ms (5%) |         |   1.48 MiB (1%) |       12836 |
| `["findfirst", "n=1000", "foldl"]`                  | 624.493 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 386.926 ms (5%) |         | 777.19 KiB (1%) |       13607 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 416.550 ms (5%) |         | 464.14 KiB (1%) |        8130 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 526.069 ms (5%) |         | 319.67 KiB (1%) |        5607 |
| `["findfirst", "n=400", "foldl"]`                   | 468.315 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 250.989 ms (5%) |         |   1.09 MiB (1%) |       19584 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 256.785 ms (5%) |         | 602.63 KiB (1%) |       10635 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 280.442 ms (5%) |         | 376.05 KiB (1%) |        6622 |
| `["findfirst", "n=500", "foldl"]`                   |  81.197 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 192.232 ms (5%) |         | 858.95 KiB (1%) |       14965 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 133.651 ms (5%) |         | 363.75 KiB (1%) |        6336 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 110.513 ms (5%) |         | 167.61 KiB (1%) |        2939 |
| `["overhead", "default"]`                           |  57.200 μs (5%) |         |  47.36 KiB (1%) |         382 |
| `["overhead", "stoppable=false"]`                   |  58.101 μs (5%) |         |  47.39 KiB (1%) |         382 |
| `["overhead", "stoppable=true"]`                    | 149.001 μs (5%) |         | 139.67 KiB (1%) |        2464 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   3.993 ms (5%) |         | 730.06 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   4.608 ms (5%) |         |   1.79 MiB (1%) |         213 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   4.300 ms (5%) |         |   1.43 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  13.346 ms (5%) |         |   1.24 MiB (1%) |         745 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  21.349 ms (5%) |         |   1.05 MiB (1%) |        2115 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  18.076 ms (5%) |         |   1.25 MiB (1%) |        1069 |
| `["parallel_histogram", "seq"]`                     |   7.285 ms (5%) |         | 364.61 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  33.705 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  16.865 ms (5%) |         |   2.66 KiB (1%) |          48 |
| `["splitby", "count", "foldl"]`                     |   4.775 ms (5%) |         |   96 bytes (1%) |           4 |
| `["splitby", "count", "man"]`                       |   1.923 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    |   1.218 ms (5%) |         |   2.88 KiB (1%) |          55 |
| `["sum", "random", "foldl"]`                        |  16.029 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "random", "reduce", "basesize=128"]`       |   8.173 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "random", "reduce", "basesize=256"]`       |   8.121 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "random", "reduce", "basesize=512"]`       |   8.068 ms (5%) |         |  25.30 KiB (1%) |         252 |
| `["sum", "uniform", "foldl"]`                       |  15.359 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   7.897 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   7.841 ms (5%) |         |  51.27 KiB (1%) |         507 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   7.749 ms (5%) |         |  25.25 KiB (1%) |         251 |
| `["sum", "valley", "foldl"]`                        |  15.978 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "valley", "reduce", "basesize=128"]`       |   8.175 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   8.101 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   8.042 ms (5%) |         |  25.25 KiB (1%) |         251 |
| `["words", "nthreads=1"]`                           |  21.515 ms (5%) |         |  31.67 MiB (1%) |     1032308 |
| `["words", "nthreads=2"]`                           |  13.098 ms (5%) |         |  32.03 MiB (1%) |     1032359 |
| `["words", "nthreads=4"]`                           |  13.901 ms (5%) |         |  32.93 MiB (1%) |     1032536 |

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
      Ubuntu 20.04.2 LTS
  uname: Linux 5.8.0-1033-azure #35~20.04.1-Ubuntu SMP Wed May 19 06:46:04 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2593 MHz      66860 s         12 s       2711 s      35212 s          0 s
       #2  2593 MHz      86376 s          9 s       2903 s      15616 s          0 s
       
  Memory: 6.790924072265625 GB (3498.265625 MB free)
  Uptime: 1056.0 sec
  Load Avg:  1.76904296875  1.6025390625  1.1171875
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
    Model name:                      Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz
    Stepping:                        7
    CPU MHz:                         2593.906
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

