# Multi-thread benchmark result

* Pull request commit: [`f2d7c7c92abff5130bb0553294f86e5ba6438fba`](https://github.com/JuliaFolds/Transducers.jl/commit/f2d7c7c92abff5130bb0553294f86e5ba6438fba)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/243> (Update */Manifest.toml)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 9 Sep 2021 - 01:19
    - Baseline: 9 Sep 2021 - 01:24
* Package commits:
    - Target: 43452a
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
| `["collect", "unordered", "basesize=1024"]`         |                   0.96 (5%)  | 0.96 (1%) :white_check_mark: |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` |                1.06 (5%) :x: |                1.04 (1%) :x: |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` |                   1.05 (5%)  |                1.03 (1%) :x: |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` |                1.19 (5%) :x: |                1.25 (1%) :x: |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  |                   1.01 (5%)  |                1.03 (1%) :x: |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  |                   1.03 (5%)  |                1.01 (1%) :x: |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  |                   0.96 (5%)  | 0.93 (1%) :white_check_mark: |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 0.71 (5%) :white_check_mark: | 0.71 (1%) :white_check_mark: |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |                1.10 (5%) :x: |                1.04 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |                1.08 (5%) :x: |                1.02 (1%) :x: |
| `["parallel_histogram", "comm", "basesize=4096"]`   |                1.06 (5%) :x: |                   1.00 (1%)  |
| `["parallel_histogram", "comm", "basesize=8192"]`   |                1.09 (5%) :x: |                   1.00 (1%)  |
| `["splitby", "count", "man"]`                       |                1.14 (5%) :x: |                   1.00 (1%)  |
| `["splitby", "count", "reduce"]`                    |                   0.99 (5%)  | 0.98 (1%) :white_check_mark: |
| `["words", "nthreads=2"]`                           |                1.22 (5%) :x: |                   1.00 (1%)  |
| `["words", "nthreads=4"]`                           |                1.24 (5%) :x: |                   1.00 (1%)  |

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
  CPU: Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2593 MHz      57859 s         19 s       2228 s      13550 s          0 s
       #2  2593 MHz      48281 s          3 s       2086 s      23708 s          0 s
       
  Memory: 6.790924072265625 GB (3452.984375 MB free)
  Uptime: 744.0 sec
  Load Avg:  1.70263671875  1.49169921875  0.89013671875
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
  CPU: Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2593 MHz      87544 s         19 s       2896 s      15691 s          0 s
       #2  2593 MHz      67667 s          3 s       2663 s      36386 s          0 s
       
  Memory: 6.790924072265625 GB (3430.74609375 MB free)
  Uptime: 1071.0 sec
  Load Avg:  1.64501953125  1.56689453125  1.10498046875
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, skylake-avx512)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 9 Sep 2021 - 1:19
* Package commit: 43452a
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
| `["collect", "assoc", "basesize=1"]`                | 236.082 ms (5%) |         |  32.66 MiB (1%) |      286737 |
| `["collect", "assoc", "basesize=1024"]`             | 197.987 ms (5%) |         |   1.79 MiB (1%) |         570 |
| `["collect", "assoc", "basesize=32"]`               | 200.180 ms (5%) |         |   3.97 MiB (1%) |       13306 |
| `["collect", "seq"]`                                | 394.853 ms (5%) |         | 512.72 KiB (1%) |          15 |
| `["collect", "unordered", "basesize=1"]`            | 414.365 ms (5%) |         |  30.01 MiB (1%) |      360558 |
| `["collect", "unordered", "basesize=1024"]`         | 234.058 ms (5%) |         | 801.27 KiB (1%) |        2362 |
| `["collect", "unordered", "basesize=32"]`           | 222.818 ms (5%) |         |   1.48 MiB (1%) |       12797 |
| `["findfirst", "n=1000", "foldl"]`                  | 627.451 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 428.032 ms (5%) |         | 881.03 KiB (1%) |       15391 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 466.351 ms (5%) |         | 499.03 KiB (1%) |        8750 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 613.874 ms (5%) |         | 352.30 KiB (1%) |        6188 |
| `["findfirst", "n=400", "foldl"]`                   | 470.329 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 249.536 ms (5%) |         |   1.12 MiB (1%) |       20135 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 260.344 ms (5%) |         | 600.08 KiB (1%) |       10583 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 273.416 ms (5%) |         | 350.50 KiB (1%) |        6187 |
| `["findfirst", "n=500", "foldl"]`                   |  81.592 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 166.148 ms (5%) |         | 697.67 KiB (1%) |       12182 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 147.377 ms (5%) |         | 375.47 KiB (1%) |        6543 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 144.373 ms (5%) |         | 224.67 KiB (1%) |        3912 |
| `["overhead", "default"]`                           |  57.201 μs (5%) |         |  47.36 KiB (1%) |         382 |
| `["overhead", "stoppable=false"]`                   |  58.600 μs (5%) |         |  47.39 KiB (1%) |         382 |
| `["overhead", "stoppable=true"]`                    | 154.902 μs (5%) |         | 139.67 KiB (1%) |        2464 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   3.968 ms (5%) |         | 730.06 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   4.580 ms (5%) |         |   1.79 MiB (1%) |         213 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   4.276 ms (5%) |         |   1.43 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  13.149 ms (5%) |         |   1.23 MiB (1%) |         432 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  23.071 ms (5%) |         |   1.04 MiB (1%) |        2376 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  19.549 ms (5%) |         |   1.26 MiB (1%) |        1316 |
| `["parallel_histogram", "seq"]`                     |   7.247 ms (5%) |         | 364.61 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  33.710 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  16.862 ms (5%) |         |   2.66 KiB (1%) |          48 |
| `["splitby", "count", "foldl"]`                     |   4.417 ms (5%) |         |   96 bytes (1%) |           4 |
| `["splitby", "count", "man"]`                       |   1.933 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    |   1.127 ms (5%) |         |   2.75 KiB (1%) |          51 |
| `["sum", "random", "foldl"]`                        |  15.868 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "random", "reduce", "basesize=128"]`       |   8.107 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "random", "reduce", "basesize=256"]`       |   7.994 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "random", "reduce", "basesize=512"]`       |   7.943 ms (5%) |         |  25.30 KiB (1%) |         252 |
| `["sum", "uniform", "foldl"]`                       |  15.501 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   7.962 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   7.862 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   7.820 ms (5%) |         |  25.25 KiB (1%) |         251 |
| `["sum", "valley", "foldl"]`                        |  16.020 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "valley", "reduce", "basesize=128"]`       |   8.170 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   8.099 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   8.034 ms (5%) |         |  25.25 KiB (1%) |         251 |
| `["words", "nthreads=1"]`                           |  20.977 ms (5%) |         |  31.60 MiB (1%) |     1029289 |
| `["words", "nthreads=2"]`                           |  16.575 ms (5%) |         |  32.31 MiB (1%) |     1029384 |
| `["words", "nthreads=4"]`                           |  17.128 ms (5%) |         |  32.94 MiB (1%) |     1029556 |

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
  CPU: Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2593 MHz      57859 s         19 s       2228 s      13550 s          0 s
       #2  2593 MHz      48281 s          3 s       2086 s      23708 s          0 s
       
  Memory: 6.790924072265625 GB (3452.984375 MB free)
  Uptime: 744.0 sec
  Load Avg:  1.70263671875  1.49169921875  0.89013671875
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, skylake-avx512)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 9 Sep 2021 - 1:24
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
| `["collect", "assoc", "basesize=1"]`                | 235.797 ms (5%) |         |  32.66 MiB (1%) |      286738 |
| `["collect", "assoc", "basesize=1024"]`             | 198.586 ms (5%) |         |   1.79 MiB (1%) |         570 |
| `["collect", "assoc", "basesize=32"]`               | 200.231 ms (5%) |         |   3.97 MiB (1%) |       13307 |
| `["collect", "seq"]`                                | 394.941 ms (5%) |         | 512.72 KiB (1%) |          15 |
| `["collect", "unordered", "basesize=1"]`            | 418.929 ms (5%) |         |  30.01 MiB (1%) |      360644 |
| `["collect", "unordered", "basesize=1024"]`         | 244.918 ms (5%) |         | 832.77 KiB (1%) |        3388 |
| `["collect", "unordered", "basesize=32"]`           | 223.239 ms (5%) |         |   1.48 MiB (1%) |       12685 |
| `["findfirst", "n=1000", "foldl"]`                  | 627.412 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 404.561 ms (5%) |         | 848.55 KiB (1%) |       14827 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 444.289 ms (5%) |         | 485.00 KiB (1%) |        8497 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 515.637 ms (5%) |         | 281.05 KiB (1%) |        4943 |
| `["findfirst", "n=400", "foldl"]`                   | 470.589 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 246.740 ms (5%) |         |   1.09 MiB (1%) |       19623 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 252.223 ms (5%) |         | 593.09 KiB (1%) |       10457 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 284.852 ms (5%) |         | 375.66 KiB (1%) |        6617 |
| `["findfirst", "n=500", "foldl"]`                   |  81.599 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 235.229 ms (5%) |         | 980.67 KiB (1%) |       17128 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 134.492 ms (5%) |         | 361.53 KiB (1%) |        6296 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 133.392 ms (5%) |         | 220.08 KiB (1%) |        3831 |
| `["overhead", "default"]`                           |  59.201 μs (5%) |         |  47.36 KiB (1%) |         382 |
| `["overhead", "stoppable=false"]`                   |  57.901 μs (5%) |         |  47.39 KiB (1%) |         382 |
| `["overhead", "stoppable=true"]`                    | 153.502 μs (5%) |         | 139.67 KiB (1%) |        2464 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   3.976 ms (5%) |         | 730.06 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   4.577 ms (5%) |         |   1.79 MiB (1%) |         213 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   4.280 ms (5%) |         |   1.43 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  13.110 ms (5%) |         |   1.23 MiB (1%) |         400 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  21.663 ms (5%) |         |   1.04 MiB (1%) |        2380 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  17.906 ms (5%) |         |   1.26 MiB (1%) |        1322 |
| `["parallel_histogram", "seq"]`                     |   7.222 ms (5%) |         | 364.61 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  33.710 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  16.865 ms (5%) |         |   2.66 KiB (1%) |          48 |
| `["splitby", "count", "foldl"]`                     |   4.445 ms (5%) |         |   96 bytes (1%) |           4 |
| `["splitby", "count", "man"]`                       |   1.692 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    |   1.134 ms (5%) |         |   2.81 KiB (1%) |          54 |
| `["sum", "random", "foldl"]`                        |  15.837 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "random", "reduce", "basesize=128"]`       |   8.108 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "random", "reduce", "basesize=256"]`       |   8.021 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "random", "reduce", "basesize=512"]`       |   7.973 ms (5%) |         |  25.30 KiB (1%) |         252 |
| `["sum", "uniform", "foldl"]`                       |  15.487 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   7.949 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   7.865 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   7.817 ms (5%) |         |  25.25 KiB (1%) |         251 |
| `["sum", "valley", "foldl"]`                        |  15.979 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "valley", "reduce", "basesize=128"]`       |   8.166 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   8.088 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   8.052 ms (5%) |         |  25.25 KiB (1%) |         251 |
| `["words", "nthreads=1"]`                           |  21.427 ms (5%) |         |  31.76 MiB (1%) |     1035243 |
| `["words", "nthreads=2"]`                           |  13.541 ms (5%) |         |  32.47 MiB (1%) |     1035325 |
| `["words", "nthreads=4"]`                           |  13.806 ms (5%) |         |  33.10 MiB (1%) |     1035457 |

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
  CPU: Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2593 MHz      87544 s         19 s       2896 s      15691 s          0 s
       #2  2593 MHz      67667 s          3 s       2663 s      36386 s          0 s
       
  Memory: 6.790924072265625 GB (3430.74609375 MB free)
  Uptime: 1071.0 sec
  Load Avg:  1.64501953125  1.56689453125  1.10498046875
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

