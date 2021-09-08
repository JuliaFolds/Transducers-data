# Multi-thread benchmark result

* Pull request commit: [`f03860ac7c7c0a0c60ed5a52b2544cf2e376b5bd`](https://github.com/JuliaFolds/Transducers.jl/commit/f03860ac7c7c0a0c60ed5a52b2544cf2e376b5bd)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/243> (Update */Manifest.toml)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 8 Sep 2021 - 01:15
    - Baseline: 8 Sep 2021 - 01:20
* Package commits:
    - Target: cd708d
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
| `["collect", "assoc", "basesize=1"]`                |                1.10 (5%) :x: |                   1.00 (1%)  |
| `["collect", "assoc", "basesize=1024"]`             |                1.07 (5%) :x: |                   1.00 (1%)  |
| `["collect", "assoc", "basesize=32"]`               |                1.14 (5%) :x: |                   1.00 (1%)  |
| `["collect", "seq"]`                                | 0.93 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["collect", "unordered", "basesize=1"]`            |                1.12 (5%) :x: |                   1.00 (1%)  |
| `["collect", "unordered", "basesize=1024"]`         | 0.88 (5%) :white_check_mark: | 0.95 (1%) :white_check_mark: |
| `["findfirst", "n=1000", "foldl"]`                  |                1.09 (5%) :x: |                   1.00 (1%)  |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 0.67 (5%) :white_check_mark: | 0.70 (1%) :white_check_mark: |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` |                1.07 (5%) :x: |                   1.00 (1%)  |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 0.83 (5%) :white_check_mark: | 0.84 (1%) :white_check_mark: |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  |                   1.05 (5%)  | 0.98 (1%) :white_check_mark: |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  |                   0.99 (5%)  | 0.96 (1%) :white_check_mark: |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 0.91 (5%) :white_check_mark: | 0.95 (1%) :white_check_mark: |
| `["findfirst", "n=500", "foldl"]`                   | 0.92 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |                1.17 (5%) :x: |                1.16 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 0.77 (5%) :white_check_mark: | 0.76 (1%) :white_check_mark: |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 0.73 (5%) :white_check_mark: | 0.94 (1%) :white_check_mark: |
| `["overhead", "default"]`                           |                1.22 (5%) :x: |                   1.00 (1%)  |
| `["overhead", "stoppable=false"]`                   |                1.19 (5%) :x: |                   1.00 (1%)  |
| `["overhead", "stoppable=true"]`                    |                1.24 (5%) :x: |                   1.00 (1%)  |
| `["parallel_histogram", "assoc", "basesize=16384"]` | 0.78 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["parallel_histogram", "assoc", "basesize=4096"]`  | 0.83 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["parallel_histogram", "assoc", "basesize=8192"]`  | 0.83 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["parallel_histogram", "comm", "basesize=4096"]`   |                   0.98 (5%)  |                1.09 (1%) :x: |
| `["parallel_histogram", "comm", "basesize=8192"]`   |                   1.03 (5%)  |                1.01 (1%) :x: |
| `["parallel_histogram", "seq"]`                     | 0.85 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["splitby", "count", "foldl"]`                     | 0.90 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["splitby", "count", "man"]`                       |                1.13 (5%) :x: |                   1.00 (1%)  |
| `["splitby", "count", "reduce"]`                    | 0.87 (5%) :white_check_mark: |                1.01 (1%) :x: |
| `["sum", "random", "reduce", "basesize=128"]`       | 0.87 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["sum", "random", "reduce", "basesize=256"]`       | 0.87 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["sum", "random", "reduce", "basesize=512"]`       |                1.07 (5%) :x: |                   1.00 (1%)  |
| `["sum", "uniform", "foldl"]`                       | 0.93 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["sum", "uniform", "reduce", "basesize=128"]`      | 0.94 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["sum", "uniform", "reduce", "basesize=256"]`      | 0.91 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["sum", "uniform", "reduce", "basesize=512"]`      | 0.85 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["sum", "valley", "reduce", "basesize=128"]`       | 0.86 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["words", "nthreads=2"]`                           |                1.17 (5%) :x: | 0.99 (1%) :white_check_mark: |

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
       #1  2095 MHz      46379 s          9 s       2399 s      33812 s          0 s
       #2  2095 MHz      63300 s         12 s       2516 s      17167 s          0 s
       
  Memory: 6.790924072265625 GB (3530.05078125 MB free)
  Uptime: 836.0 sec
  Load Avg:  1.62548828125  1.48681640625  0.9111328125
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
       #1  2095 MHz      74612 s          9 s       3040 s      39185 s          0 s
       #2  2095 MHz      85942 s         12 s       3190 s      27995 s          0 s
       
  Memory: 6.790924072265625 GB (3460.54296875 MB free)
  Uptime: 1180.0 sec
  Load Avg:  1.60107421875  1.54345703125  1.10986328125
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, skylake-avx512)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 8 Sep 2021 - 1:15
* Package commit: cd708d
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
| `["collect", "assoc", "basesize=1"]`                | 282.404 ms (5%) |         |  32.66 MiB (1%) |      286734 |
| `["collect", "assoc", "basesize=1024"]`             | 232.274 ms (5%) |         |   1.79 MiB (1%) |         570 |
| `["collect", "assoc", "basesize=32"]`               | 241.661 ms (5%) |         |   3.97 MiB (1%) |       13306 |
| `["collect", "seq"]`                                | 430.026 ms (5%) |         | 512.72 KiB (1%) |          15 |
| `["collect", "unordered", "basesize=1"]`            | 501.136 ms (5%) |         |  30.01 MiB (1%) |      360604 |
| `["collect", "unordered", "basesize=1024"]`         | 275.128 ms (5%) |         | 820.80 KiB (1%) |        3005 |
| `["collect", "unordered", "basesize=32"]`           | 258.396 ms (5%) |         |   1.48 MiB (1%) |       12725 |
| `["findfirst", "n=1000", "foldl"]`                  | 687.353 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 488.139 ms (5%) |         | 858.19 KiB (1%) |       15032 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 516.626 ms (5%) |         | 484.97 KiB (1%) |        8496 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 665.565 ms (5%) |         | 328.98 KiB (1%) |        5774 |
| `["findfirst", "n=400", "foldl"]`                   | 518.536 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 289.581 ms (5%) |         |   1.10 MiB (1%) |       19777 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 290.270 ms (5%) |         | 597.77 KiB (1%) |       10540 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 292.233 ms (5%) |         | 338.92 KiB (1%) |        5975 |
| `["findfirst", "n=500", "foldl"]`                   |  78.677 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 164.397 ms (5%) |         | 722.08 KiB (1%) |       12575 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 150.523 ms (5%) |         | 352.30 KiB (1%) |        6137 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 147.057 ms (5%) |         | 235.94 KiB (1%) |        4102 |
| `["overhead", "default"]`                           |  67.802 μs (5%) |         |  47.33 KiB (1%) |         381 |
| `["overhead", "stoppable=false"]`                   |  67.502 μs (5%) |         |  47.36 KiB (1%) |         381 |
| `["overhead", "stoppable=true"]`                    | 175.605 μs (5%) |         | 139.64 KiB (1%) |        2463 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   3.437 ms (5%) |         | 730.06 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   4.085 ms (5%) |         |   1.79 MiB (1%) |         213 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   3.654 ms (5%) |         |   1.43 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  14.379 ms (5%) |         |   1.22 MiB (1%) |         160 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  23.505 ms (5%) |         |   1.07 MiB (1%) |        2707 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  20.598 ms (5%) |         |   1.27 MiB (1%) |        1712 |
| `["parallel_histogram", "seq"]`                     |   6.201 ms (5%) |         | 364.61 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  34.700 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  17.572 ms (5%) |         |   2.66 KiB (1%) |          48 |
| `["splitby", "count", "foldl"]`                     |   3.715 ms (5%) |         |   96 bytes (1%) |           4 |
| `["splitby", "count", "man"]`                       |   1.658 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    | 946.727 μs (5%) |         |   2.88 KiB (1%) |          55 |
| `["sum", "random", "foldl"]`                        |  14.673 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "random", "reduce", "basesize=128"]`       |   7.321 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "random", "reduce", "basesize=256"]`       |   7.254 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "random", "reduce", "basesize=512"]`       |   7.206 ms (5%) |         |  25.30 KiB (1%) |         252 |
| `["sum", "uniform", "foldl"]`                       |  15.800 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   7.775 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   7.462 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   7.424 ms (5%) |         |  25.25 KiB (1%) |         251 |
| `["sum", "valley", "foldl"]`                        |  15.192 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "valley", "reduce", "basesize=128"]`       |   7.124 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   7.904 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   8.039 ms (5%) |         |  25.25 KiB (1%) |         251 |
| `["words", "nthreads=1"]`                           |  25.302 ms (5%) |         |  31.62 MiB (1%) |     1030190 |
| `["words", "nthreads=2"]`                           |  16.100 ms (5%) |         |  31.98 MiB (1%) |     1030228 |
| `["words", "nthreads=4"]`                           |  16.416 ms (5%) |         |  32.69 MiB (1%) |     1030306 |

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
       #1  2095 MHz      46379 s          9 s       2399 s      33812 s          0 s
       #2  2095 MHz      63300 s         12 s       2516 s      17167 s          0 s
       
  Memory: 6.790924072265625 GB (3530.05078125 MB free)
  Uptime: 836.0 sec
  Load Avg:  1.62548828125  1.48681640625  0.9111328125
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, skylake-avx512)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 8 Sep 2021 - 1:20
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

| ID                                                  | time            | GC time | memory           | allocations |
|-----------------------------------------------------|----------------:|--------:|-----------------:|------------:|
| `["collect", "assoc", "basesize=1"]`                | 257.146 ms (5%) |         |   32.66 MiB (1%) |      286743 |
| `["collect", "assoc", "basesize=1024"]`             | 217.390 ms (5%) |         |    1.79 MiB (1%) |         570 |
| `["collect", "assoc", "basesize=32"]`               | 211.536 ms (5%) |         |    3.97 MiB (1%) |       13306 |
| `["collect", "seq"]`                                | 461.504 ms (5%) |         |  512.72 KiB (1%) |          15 |
| `["collect", "unordered", "basesize=1"]`            | 449.190 ms (5%) |         |   30.01 MiB (1%) |      360578 |
| `["collect", "unordered", "basesize=1024"]`         | 313.770 ms (5%) |         |  859.80 KiB (1%) |        4253 |
| `["collect", "unordered", "basesize=32"]`           | 264.191 ms (5%) |         |    1.47 MiB (1%) |       12553 |
| `["findfirst", "n=1000", "foldl"]`                  | 632.218 ms (5%) |         |                  |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 731.181 ms (5%) |         |    1.20 MiB (1%) |       21490 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 481.695 ms (5%) |         |  485.03 KiB (1%) |        8498 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 803.906 ms (5%) |         |  393.55 KiB (1%) |        6908 |
| `["findfirst", "n=400", "foldl"]`                   | 525.600 ms (5%) |         |                  |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 276.182 ms (5%) |         |    1.12 MiB (1%) |       20216 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 292.733 ms (5%) |         |  621.13 KiB (1%) |       10960 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 322.709 ms (5%) |         |  357.53 KiB (1%) |        6310 |
| `["findfirst", "n=500", "foldl"]`                   |  85.688 ms (5%) |         |                  |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 140.785 ms (5%) |         |  622.52 KiB (1%) |       10859 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 194.851 ms (5%) |         |  463.06 KiB (1%) |        8060 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 202.468 ms (5%) |         |  250.20 KiB (1%) |        4369 |
| `["overhead", "default"]`                           |  55.401 μs (5%) |         |   47.33 KiB (1%) |         381 |
| `["overhead", "stoppable=false"]`                   |  56.802 μs (5%) |         |   47.36 KiB (1%) |         381 |
| `["overhead", "stoppable=true"]`                    | 141.104 μs (5%) |         |  139.67 KiB (1%) |        2464 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   4.425 ms (5%) |         |  730.06 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   4.916 ms (5%) |         |    1.79 MiB (1%) |         213 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   4.422 ms (5%) |         |    1.43 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  15.080 ms (5%) |         |    1.22 MiB (1%) |         160 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  24.000 ms (5%) |         | 1009.63 KiB (1%) |         562 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  19.992 ms (5%) |         |    1.25 MiB (1%) |        1184 |
| `["parallel_histogram", "seq"]`                     |   7.331 ms (5%) |         |  364.61 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  33.212 ms (5%) |         |                  |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  18.490 ms (5%) |         |    2.66 KiB (1%) |          48 |
| `["splitby", "count", "foldl"]`                     |   4.136 ms (5%) |         |    96 bytes (1%) |           4 |
| `["splitby", "count", "man"]`                       |   1.472 ms (5%) |         |                  |             |
| `["splitby", "count", "reduce"]`                    |   1.094 ms (5%) |         |    2.84 KiB (1%) |          54 |
| `["sum", "random", "foldl"]`                        |  14.247 ms (5%) |         |    32 bytes (1%) |           2 |
| `["sum", "random", "reduce", "basesize=128"]`       |   8.430 ms (5%) |         |  103.23 KiB (1%) |        1018 |
| `["sum", "random", "reduce", "basesize=256"]`       |   8.359 ms (5%) |         |   51.23 KiB (1%) |         506 |
| `["sum", "random", "reduce", "basesize=512"]`       |   6.734 ms (5%) |         |   25.30 KiB (1%) |         252 |
| `["sum", "uniform", "foldl"]`                       |  16.912 ms (5%) |         |    32 bytes (1%) |           2 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   8.310 ms (5%) |         |  103.23 KiB (1%) |        1018 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   8.159 ms (5%) |         |   51.23 KiB (1%) |         506 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   8.768 ms (5%) |         |   25.25 KiB (1%) |         251 |
| `["sum", "valley", "foldl"]`                        |  15.562 ms (5%) |         |    32 bytes (1%) |           2 |
| `["sum", "valley", "reduce", "basesize=128"]`       |   8.257 ms (5%) |         |  103.23 KiB (1%) |        1018 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   8.266 ms (5%) |         |   51.23 KiB (1%) |         506 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   8.339 ms (5%) |         |   25.25 KiB (1%) |         251 |
| `["words", "nthreads=1"]`                           |  24.348 ms (5%) |         |   31.73 MiB (1%) |     1033931 |
| `["words", "nthreads=2"]`                           |  13.784 ms (5%) |         |   32.44 MiB (1%) |     1034020 |
| `["words", "nthreads=4"]`                           |  15.870 ms (5%) |         |   32.89 MiB (1%) |     1034086 |

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
       #1  2095 MHz      74612 s          9 s       3040 s      39185 s          0 s
       #2  2095 MHz      85942 s         12 s       3190 s      27995 s          0 s
       
  Memory: 6.790924072265625 GB (3460.54296875 MB free)
  Uptime: 1180.0 sec
  Load Avg:  1.60107421875  1.54345703125  1.10986328125
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
    CPU MHz:                         2095.109
    BogoMIPS:                        4190.21
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

