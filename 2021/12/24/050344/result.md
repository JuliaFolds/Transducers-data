# Multi-thread benchmark result

* Pull request commit: [`3118cd54591f464504c10b79bed3136ccc036e10`](https://github.com/JuliaFolds/Transducers.jl/commit/3118cd54591f464504c10b79bed3136ccc036e10)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/501> (Test with Julia 1.7)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 24 Dec 2021 - 04:57
    - Baseline: 24 Dec 2021 - 05:03
* Package commits:
    - Target: 136559
    - Baseline: ed4189
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
| `["collect", "unordered", "basesize=1024"]`         |                1.05 (5%) :x: |                1.02 (1%) :x: |
| `["findfirst", "n=1000", "foldl"]`                  | 0.95 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` |                1.98 (5%) :x: |                2.02 (1%) :x: |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 0.86 (5%) :white_check_mark: | 0.95 (1%) :white_check_mark: |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` |                   0.99 (5%)  |                1.06 (1%) :x: |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  |                   1.02 (5%)  |                1.01 (1%) :x: |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  |                   0.96 (5%)  | 0.96 (1%) :white_check_mark: |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  |                   0.99 (5%)  | 0.99 (1%) :white_check_mark: |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |                   1.04 (5%)  |                1.20 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |                1.26 (5%) :x: |                1.26 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |                   0.98 (5%)  |                1.04 (1%) :x: |
| `["overhead", "default"]`                           | 0.92 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["overhead", "stoppable=false"]`                   | 0.91 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["overhead", "stoppable=true"]`                    |                1.06 (5%) :x: |                   1.00 (1%)  |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |                   1.04 (5%)  | 0.87 (1%) :white_check_mark: |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |                1.09 (5%) :x: |                   1.00 (1%)  |
| `["parallel_histogram", "comm", "basesize=8192"]`   |                   1.03 (5%)  | 0.98 (1%) :white_check_mark: |
| `["partition_length_maximum", "rand", "reduce"]`    | 0.95 (5%) :white_check_mark: | 0.99 (1%) :white_check_mark: |
| `["sum", "random", "reduce", "basesize=256"]`       | 0.94 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["words", "nthreads=1"]`                           |                1.06 (5%) :x: |                   1.00 (1%)  |
| `["words", "nthreads=2"]`                           | 0.94 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["words", "nthreads=4"]`                           | 0.91 (5%) :white_check_mark: |                   0.99 (1%)  |

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
  uname: Linux 5.11.0-1022-azure #23~20.04.1-Ubuntu SMP Fri Nov 19 10:20:52 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz      56580 s         15 s       2486 s      30532 s          0 s
       #2  2095 MHz      52709 s          6 s       2672 s      34415 s          0 s
       
  Memory: 6.788982391357422 GB (3067.69140625 MB free)
  Uptime: 905.0 sec
  Load Avg:  1.6240234375  1.46875  0.89990234375
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
  uname: Linux 5.11.0-1022-azure #23~20.04.1-Ubuntu SMP Fri Nov 19 10:20:52 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz      80106 s         15 s       3028 s      38096 s          0 s
       #2  2095 MHz      77515 s          6 s       3116 s      40869 s          0 s
       
  Memory: 6.788982391357422 GB (3046.38671875 MB free)
  Uptime: 1223.0 sec
  Load Avg:  1.67138671875  1.55322265625  1.1044921875
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, skylake-avx512)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 24 Dec 2021 - 4:57
* Package commit: 136559
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
| `["collect", "assoc", "basesize=1"]`                | 250.420 ms (5%) |         |  32.66 MiB (1%) |      286741 |
| `["collect", "assoc", "basesize=1024"]`             | 210.311 ms (5%) |         |   1.79 MiB (1%) |         570 |
| `["collect", "assoc", "basesize=32"]`               | 213.930 ms (5%) |         |   3.97 MiB (1%) |       13306 |
| `["collect", "seq"]`                                | 408.887 ms (5%) |         | 512.72 KiB (1%) |          15 |
| `["collect", "unordered", "basesize=1"]`            | 493.039 ms (5%) |         |  30.01 MiB (1%) |      360597 |
| `["collect", "unordered", "basesize=1024"]`         | 274.369 ms (5%) |         | 813.27 KiB (1%) |        2764 |
| `["collect", "unordered", "basesize=32"]`           | 241.505 ms (5%) |         |   1.48 MiB (1%) |       12762 |
| `["findfirst", "n=1000", "foldl"]`                  | 653.972 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 809.726 ms (5%) |         |   1.34 MiB (1%) |       24127 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 480.721 ms (5%) |         | 480.19 KiB (1%) |        8409 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 679.979 ms (5%) |         | 347.31 KiB (1%) |        6088 |
| `["findfirst", "n=400", "foldl"]`                   | 490.766 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 292.492 ms (5%) |         |   1.18 MiB (1%) |       21163 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 270.421 ms (5%) |         | 572.39 KiB (1%) |       10100 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 290.035 ms (5%) |         | 338.95 KiB (1%) |        5976 |
| `["findfirst", "n=500", "foldl"]`                   |  82.200 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 178.612 ms (5%) |         | 770.00 KiB (1%) |       13389 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 170.602 ms (5%) |         | 405.27 KiB (1%) |        7053 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 119.406 ms (5%) |         | 185.75 KiB (1%) |        3243 |
| `["overhead", "default"]`                           |  56.903 μs (5%) |         |  47.33 KiB (1%) |         381 |
| `["overhead", "stoppable=false"]`                   |  56.703 μs (5%) |         |  47.36 KiB (1%) |         381 |
| `["overhead", "stoppable=true"]`                    | 142.707 μs (5%) |         | 139.64 KiB (1%) |        2463 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   3.646 ms (5%) |         | 730.06 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   4.463 ms (5%) |         |   1.79 MiB (1%) |         213 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   4.187 ms (5%) |         |   1.43 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  15.461 ms (5%) |         |   1.23 MiB (1%) |         507 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  24.492 ms (5%) |         |   1.06 MiB (1%) |        2137 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  20.593 ms (5%) |         |   1.22 MiB (1%) |         171 |
| `["parallel_histogram", "seq"]`                     |   6.311 ms (5%) |         | 364.61 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  33.040 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  16.993 ms (5%) |         |   2.63 KiB (1%) |          47 |
| `["splitby", "count", "foldl"]`                     |   3.914 ms (5%) |         |   96 bytes (1%) |           4 |
| `["splitby", "count", "man"]`                       |   1.418 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    | 991.244 μs (5%) |         |   2.75 KiB (1%) |          51 |
| `["sum", "random", "foldl"]`                        |  15.281 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "random", "reduce", "basesize=128"]`       |   8.030 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "random", "reduce", "basesize=256"]`       |   7.891 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "random", "reduce", "basesize=512"]`       |   7.434 ms (5%) |         |  25.30 KiB (1%) |         252 |
| `["sum", "uniform", "foldl"]`                       |  14.915 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   7.736 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   7.395 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   7.664 ms (5%) |         |  25.25 KiB (1%) |         251 |
| `["sum", "valley", "foldl"]`                        |  15.512 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "valley", "reduce", "basesize=128"]`       |   7.773 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   8.321 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   8.256 ms (5%) |         |  25.28 KiB (1%) |         252 |
| `["words", "nthreads=1"]`                           |  23.314 ms (5%) |         |  31.78 MiB (1%) |     1035165 |
| `["words", "nthreads=2"]`                           |  14.351 ms (5%) |         |  32.49 MiB (1%) |     1035239 |
| `["words", "nthreads=4"]`                           |  14.547 ms (5%) |         |  32.94 MiB (1%) |     1035310 |

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
  uname: Linux 5.11.0-1022-azure #23~20.04.1-Ubuntu SMP Fri Nov 19 10:20:52 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz      56580 s         15 s       2486 s      30532 s          0 s
       #2  2095 MHz      52709 s          6 s       2672 s      34415 s          0 s
       
  Memory: 6.788982391357422 GB (3067.69140625 MB free)
  Uptime: 905.0 sec
  Load Avg:  1.6240234375  1.46875  0.89990234375
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, skylake-avx512)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 24 Dec 2021 - 5:3
* Package commit: ed4189
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

| ID                                                  | time            | GC time  | memory          | allocations |
|-----------------------------------------------------|----------------:|---------:|----------------:|------------:|
| `["collect", "assoc", "basesize=1"]`                | 256.129 ms (5%) |          |  32.66 MiB (1%) |      286743 |
| `["collect", "assoc", "basesize=1024"]`             | 212.755 ms (5%) |          |   1.79 MiB (1%) |         570 |
| `["collect", "assoc", "basesize=32"]`               | 215.770 ms (5%) |          |   3.97 MiB (1%) |       13306 |
| `["collect", "seq"]`                                | 409.739 ms (5%) |          | 512.72 KiB (1%) |          15 |
| `["collect", "unordered", "basesize=1"]`            | 471.677 ms (5%) |          |  30.01 MiB (1%) |      360705 |
| `["collect", "unordered", "basesize=1024"]`         | 261.010 ms (5%) |          | 796.05 KiB (1%) |        2213 |
| `["collect", "unordered", "basesize=32"]`           | 243.277 ms (5%) |          |   1.48 MiB (1%) |       12686 |
| `["findfirst", "n=1000", "foldl"]`                  | 690.010 ms (5%) |          |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 408.001 ms (5%) |          | 682.48 KiB (1%) |       11972 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 557.302 ms (5%) |          | 503.78 KiB (1%) |        8833 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 688.398 ms (5%) |          | 329.03 KiB (1%) |        5776 |
| `["findfirst", "n=400", "foldl"]`                   | 490.544 ms (5%) |          |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 286.168 ms (5%) |          |   1.16 MiB (1%) |       20867 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 283.069 ms (5%) |          | 595.52 KiB (1%) |       10505 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 292.560 ms (5%) |          | 343.59 KiB (1%) |        6060 |
| `["findfirst", "n=500", "foldl"]`                   |  85.145 ms (5%) |          |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 171.806 ms (5%) |          | 643.64 KiB (1%) |       11219 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 135.194 ms (5%) |          | 322.20 KiB (1%) |        5612 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 121.873 ms (5%) |          | 178.88 KiB (1%) |        3125 |
| `["overhead", "default"]`                           |  61.903 μs (5%) |          |  47.33 KiB (1%) |         381 |
| `["overhead", "stoppable=false"]`                   |  62.203 μs (5%) |          |  47.36 KiB (1%) |         381 |
| `["overhead", "stoppable=true"]`                    | 135.106 μs (5%) |          | 139.67 KiB (1%) |        2464 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   3.536 ms (5%) |          | 730.06 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   4.311 ms (5%) |          |   2.06 MiB (1%) |         219 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   3.845 ms (5%) |          |   1.43 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  15.265 ms (5%) |          |   1.23 MiB (1%) |         654 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  25.284 ms (5%) |          |   1.06 MiB (1%) |        2795 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  19.916 ms (5%) | 2.492 ms |   1.25 MiB (1%) |        1033 |
| `["parallel_histogram", "seq"]`                     |   6.482 ms (5%) |          | 364.61 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  34.656 ms (5%) |          |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  17.914 ms (5%) |          |   2.66 KiB (1%) |          48 |
| `["splitby", "count", "foldl"]`                     |   3.823 ms (5%) |          |   96 bytes (1%) |           4 |
| `["splitby", "count", "man"]`                       |   1.421 ms (5%) |          |                 |             |
| `["splitby", "count", "reduce"]`                    | 989.748 μs (5%) |          |   2.75 KiB (1%) |          52 |
| `["sum", "random", "foldl"]`                        |  15.062 ms (5%) |          |   32 bytes (1%) |           2 |
| `["sum", "random", "reduce", "basesize=128"]`       |   7.744 ms (5%) |          | 103.23 KiB (1%) |        1018 |
| `["sum", "random", "reduce", "basesize=256"]`       |   8.354 ms (5%) |          |  51.23 KiB (1%) |         506 |
| `["sum", "random", "reduce", "basesize=512"]`       |   7.693 ms (5%) |          |  25.30 KiB (1%) |         252 |
| `["sum", "uniform", "foldl"]`                       |  15.612 ms (5%) |          |   32 bytes (1%) |           2 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   7.922 ms (5%) |          | 103.23 KiB (1%) |        1018 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   7.179 ms (5%) |          |  51.23 KiB (1%) |         506 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   7.649 ms (5%) |          |  25.25 KiB (1%) |         251 |
| `["sum", "valley", "foldl"]`                        |  15.189 ms (5%) |          |   32 bytes (1%) |           2 |
| `["sum", "valley", "reduce", "basesize=128"]`       |   8.059 ms (5%) |          | 103.23 KiB (1%) |        1018 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   8.036 ms (5%) |          |  51.23 KiB (1%) |         506 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   7.956 ms (5%) |          |  25.25 KiB (1%) |         251 |
| `["words", "nthreads=1"]`                           |  22.036 ms (5%) |          |  31.88 MiB (1%) |     1038473 |
| `["words", "nthreads=2"]`                           |  15.203 ms (5%) |          |  32.59 MiB (1%) |     1038545 |
| `["words", "nthreads=4"]`                           |  16.041 ms (5%) |          |  33.23 MiB (1%) |     1038700 |

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
  uname: Linux 5.11.0-1022-azure #23~20.04.1-Ubuntu SMP Fri Nov 19 10:20:52 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz      80106 s         15 s       3028 s      38096 s          0 s
       #2  2095 MHz      77515 s          6 s       3116 s      40869 s          0 s
       
  Memory: 6.788982391357422 GB (3046.38671875 MB free)
  Uptime: 1223.0 sec
  Load Avg:  1.67138671875  1.55322265625  1.1044921875
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
    CPU MHz:                         2095.170
    BogoMIPS:                        4190.34
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

