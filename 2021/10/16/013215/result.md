# Multi-thread benchmark result

* Pull request commit: [`f8d36fe5b216b7d8fc510c579a940059001325a9`](https://github.com/JuliaFolds/Transducers.jl/commit/f8d36fe5b216b7d8fc510c579a940059001325a9)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/243> (Update */Manifest.toml)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 16 Oct 2021 - 01:25
    - Baseline: 16 Oct 2021 - 01:31
* Package commits:
    - Target: 8c86a6
    - Baseline: 1e5e53
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
| `["collect", "unordered", "basesize=1024"]`         | 0.86 (5%) :white_check_mark: | 0.89 (1%) :white_check_mark: |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 0.73 (5%) :white_check_mark: | 0.76 (1%) :white_check_mark: |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` |                1.21 (5%) :x: |                1.09 (1%) :x: |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  |                   0.98 (5%)  | 0.98 (1%) :white_check_mark: |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 0.93 (5%) :white_check_mark: | 0.84 (1%) :white_check_mark: |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 0.51 (5%) :white_check_mark: | 0.60 (1%) :white_check_mark: |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 0.60 (5%) :white_check_mark: | 0.66 (1%) :white_check_mark: |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |                1.51 (5%) :x: |                1.31 (1%) :x: |
| `["parallel_histogram", "comm", "basesize=16384"]`  | 0.92 (5%) :white_check_mark: | 0.83 (1%) :white_check_mark: |
| `["parallel_histogram", "comm", "basesize=4096"]`   | 0.95 (5%) :white_check_mark: |                1.01 (1%) :x: |
| `["parallel_histogram", "comm", "basesize=8192"]`   |                1.10 (5%) :x: |                   1.00 (1%)  |
| `["partition_length_maximum", "rand", "reduce"]`    |                   1.00 (5%)  |                1.01 (1%) :x: |
| `["splitby", "count", "foldl"]`                     | 0.54 (5%) :white_check_mark: | 0.17 (1%) :white_check_mark: |
| `["splitby", "count", "man"]`                       |                1.16 (5%) :x: |                   1.00 (1%)  |
| `["splitby", "count", "reduce"]`                    | 0.95 (5%) :white_check_mark: | 0.93 (1%) :white_check_mark: |

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
  uname: Linux 5.8.0-1042-azure #45~20.04.1-Ubuntu SMP Wed Sep 15 14:24:15 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2593 MHz      53394 s         21 s       2407 s      41049 s          0 s
       #2  2593 MHz      54203 s          2 s       2361 s      40736 s          0 s
       
  Memory: 6.790924072265625 GB (3187.44140625 MB free)
  Uptime: 977.0 sec
  Load Avg:  1.623046875  1.447265625  0.88134765625
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
  uname: Linux 5.8.0-1042-azure #45~20.04.1-Ubuntu SMP Wed Sep 15 14:24:15 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2593 MHz      84700 s         21 s       3078 s      43206 s          0 s
       #2  2593 MHz      73514 s          2 s       3044 s      54840 s          0 s
       
  Memory: 6.790924072265625 GB (3171.2421875 MB free)
  Uptime: 1320.0 sec
  Load Avg:  1.689453125  1.54931640625  1.1015625
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, skylake-avx512)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 16 Oct 2021 - 1:25
* Package commit: 8c86a6
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
| `["collect", "assoc", "basesize=1"]`                | 241.282 ms (5%) |         |  32.66 MiB (1%) |      286750 |
| `["collect", "assoc", "basesize=1024"]`             | 198.242 ms (5%) |         |   1.79 MiB (1%) |         570 |
| `["collect", "assoc", "basesize=32"]`               | 200.627 ms (5%) |         |   3.97 MiB (1%) |       13307 |
| `["collect", "seq"]`                                | 394.988 ms (5%) |         | 512.72 KiB (1%) |          15 |
| `["collect", "unordered", "basesize=1"]`            | 425.913 ms (5%) |         |  30.01 MiB (1%) |      360570 |
| `["collect", "unordered", "basesize=1024"]`         | 234.844 ms (5%) |         | 804.89 KiB (1%) |        2478 |
| `["collect", "unordered", "basesize=32"]`           | 224.102 ms (5%) |         |   1.47 MiB (1%) |       12641 |
| `["findfirst", "n=1000", "foldl"]`                  | 626.225 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 386.945 ms (5%) |         | 795.45 KiB (1%) |       13915 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 538.177 ms (5%) |         | 527.56 KiB (1%) |        9276 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 572.856 ms (5%) |         | 328.98 KiB (1%) |        5774 |
| `["findfirst", "n=400", "foldl"]`                   | 469.922 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 244.549 ms (5%) |         |   1.06 MiB (1%) |       19114 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 258.676 ms (5%) |         | 600.14 KiB (1%) |       10585 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 250.899 ms (5%) |         | 307.00 KiB (1%) |        5427 |
| `["findfirst", "n=500", "foldl"]`                   |  81.433 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |  67.118 ms (5%) |         | 378.66 KiB (1%) |        6586 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |  75.139 ms (5%) |         | 230.05 KiB (1%) |        4014 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 192.940 ms (5%) |         | 275.34 KiB (1%) |        4809 |
| `["overhead", "default"]`                           |  61.702 μs (5%) |         |  47.36 KiB (1%) |         382 |
| `["overhead", "stoppable=false"]`                   |  61.001 μs (5%) |         |  47.39 KiB (1%) |         382 |
| `["overhead", "stoppable=true"]`                    | 156.904 μs (5%) |         | 139.67 KiB (1%) |        2464 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   4.001 ms (5%) |         | 730.06 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   4.621 ms (5%) |         |   1.79 MiB (1%) |         213 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   4.318 ms (5%) |         |   1.43 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  13.115 ms (5%) |         |   1.03 MiB (1%) |         401 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  20.676 ms (5%) |         |   1.06 MiB (1%) |        2632 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  19.244 ms (5%) |         |   1.27 MiB (1%) |        1810 |
| `["parallel_histogram", "seq"]`                     |   7.285 ms (5%) |         | 364.61 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  33.772 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  16.895 ms (5%) |         |   2.66 KiB (1%) |          48 |
| `["splitby", "count", "foldl"]`                     |   2.439 ms (5%) |         |   16 bytes (1%) |           1 |
| `["splitby", "count", "man"]`                       |   1.949 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    |   1.119 ms (5%) |         |   2.66 KiB (1%) |          48 |
| `["sum", "random", "foldl"]`                        |  15.945 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "random", "reduce", "basesize=128"]`       |   8.171 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "random", "reduce", "basesize=256"]`       |   8.078 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "random", "reduce", "basesize=512"]`       |   8.017 ms (5%) |         |  25.30 KiB (1%) |         252 |
| `["sum", "uniform", "foldl"]`                       |  15.559 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   7.995 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   7.884 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   7.815 ms (5%) |         |  25.25 KiB (1%) |         251 |
| `["sum", "valley", "foldl"]`                        |  15.996 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "valley", "reduce", "basesize=128"]`       |   8.216 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   8.148 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   8.088 ms (5%) |         |  25.25 KiB (1%) |         251 |
| `["words", "nthreads=1"]`                           |  23.446 ms (5%) |         |  31.77 MiB (1%) |     1035014 |
| `["words", "nthreads=2"]`                           |  15.202 ms (5%) |         |  32.13 MiB (1%) |     1035050 |
| `["words", "nthreads=4"]`                           |  15.911 ms (5%) |         |  32.84 MiB (1%) |     1035144 |

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
  uname: Linux 5.8.0-1042-azure #45~20.04.1-Ubuntu SMP Wed Sep 15 14:24:15 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2593 MHz      53394 s         21 s       2407 s      41049 s          0 s
       #2  2593 MHz      54203 s          2 s       2361 s      40736 s          0 s
       
  Memory: 6.790924072265625 GB (3187.44140625 MB free)
  Uptime: 977.0 sec
  Load Avg:  1.623046875  1.447265625  0.88134765625
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, skylake-avx512)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 16 Oct 2021 - 1:31
* Package commit: 1e5e53
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
| `["collect", "assoc", "basesize=1"]`                | 239.285 ms (5%) |         |  32.66 MiB (1%) |      286735 |
| `["collect", "assoc", "basesize=1024"]`             | 198.876 ms (5%) |         |   1.79 MiB (1%) |         570 |
| `["collect", "assoc", "basesize=32"]`               | 200.430 ms (5%) |         |   3.97 MiB (1%) |       13305 |
| `["collect", "seq"]`                                | 394.939 ms (5%) |         | 512.72 KiB (1%) |          15 |
| `["collect", "unordered", "basesize=1"]`            | 424.568 ms (5%) |         |  30.01 MiB (1%) |      360573 |
| `["collect", "unordered", "basesize=1024"]`         | 271.553 ms (5%) |         | 908.64 KiB (1%) |        5798 |
| `["collect", "unordered", "basesize=32"]`           | 222.965 ms (5%) |         |   1.48 MiB (1%) |       12799 |
| `["findfirst", "n=1000", "foldl"]`                  | 627.001 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 531.042 ms (5%) |         |   1.03 MiB (1%) |       18447 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 443.134 ms (5%) |         | 485.00 KiB (1%) |        8497 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 572.328 ms (5%) |         | 328.98 KiB (1%) |        5774 |
| `["findfirst", "n=400", "foldl"]`                   | 470.691 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 249.443 ms (5%) |         |   1.08 MiB (1%) |       19509 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 254.573 ms (5%) |         | 604.52 KiB (1%) |       10652 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 270.660 ms (5%) |         | 366.38 KiB (1%) |        6457 |
| `["findfirst", "n=500", "foldl"]`                   |  81.621 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 131.224 ms (5%) |         | 636.09 KiB (1%) |       11076 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 125.989 ms (5%) |         | 349.86 KiB (1%) |        6089 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 127.780 ms (5%) |         | 210.83 KiB (1%) |        3669 |
| `["overhead", "default"]`                           |  60.001 μs (5%) |         |  47.36 KiB (1%) |         382 |
| `["overhead", "stoppable=false"]`                   |  60.401 μs (5%) |         |  47.39 KiB (1%) |         382 |
| `["overhead", "stoppable=true"]`                    | 155.203 μs (5%) |         | 139.67 KiB (1%) |        2464 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   3.979 ms (5%) |         | 730.06 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   4.607 ms (5%) |         |   1.79 MiB (1%) |         213 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   4.291 ms (5%) |         |   1.43 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  14.187 ms (5%) |         |   1.24 MiB (1%) |         978 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  21.826 ms (5%) |         |   1.04 MiB (1%) |        2372 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  17.508 ms (5%) |         |   1.27 MiB (1%) |        1613 |
| `["parallel_histogram", "seq"]`                     |   7.257 ms (5%) |         | 364.61 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  33.746 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  16.880 ms (5%) |         |   2.63 KiB (1%) |          47 |
| `["splitby", "count", "foldl"]`                     |   4.513 ms (5%) |         |   96 bytes (1%) |           4 |
| `["splitby", "count", "man"]`                       |   1.683 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    |   1.184 ms (5%) |         |   2.84 KiB (1%) |          54 |
| `["sum", "random", "foldl"]`                        |  16.021 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "random", "reduce", "basesize=128"]`       |   8.172 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "random", "reduce", "basesize=256"]`       |   8.103 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "random", "reduce", "basesize=512"]`       |   8.070 ms (5%) |         |  25.30 KiB (1%) |         252 |
| `["sum", "uniform", "foldl"]`                       |  15.442 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   7.946 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   7.859 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   7.814 ms (5%) |         |  25.25 KiB (1%) |         251 |
| `["sum", "valley", "foldl"]`                        |  16.003 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "valley", "reduce", "basesize=128"]`       |   8.220 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   8.106 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   8.071 ms (5%) |         |  25.25 KiB (1%) |         251 |
| `["words", "nthreads=1"]`                           |  22.995 ms (5%) |         |  31.73 MiB (1%) |     1033665 |
| `["words", "nthreads=2"]`                           |  15.678 ms (5%) |         |  32.44 MiB (1%) |     1033739 |
| `["words", "nthreads=4"]`                           |  15.981 ms (5%) |         |  32.89 MiB (1%) |     1033821 |

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
  uname: Linux 5.8.0-1042-azure #45~20.04.1-Ubuntu SMP Wed Sep 15 14:24:15 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2593 MHz      84700 s         21 s       3078 s      43206 s          0 s
       #2  2593 MHz      73514 s          2 s       3044 s      54840 s          0 s
       
  Memory: 6.790924072265625 GB (3171.2421875 MB free)
  Uptime: 1320.0 sec
  Load Avg:  1.689453125  1.54931640625  1.1015625
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

