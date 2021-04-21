# Multi-thread benchmark result

* Pull request commit: [`0d32ffd2ec787d6034ff93a276d30d060e5291c9`](https://github.com/JuliaFolds/Transducers.jl/commit/0d32ffd2ec787d6034ff93a276d30d060e5291c9)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/446> (Test with Julia 1.6.0-beta1)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 21 Apr 2021 - 21:07
    - Baseline: 21 Apr 2021 - 21:12
* Package commits:
    - Target: 45644d
    - Baseline: 163057
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
| `["collect", "unordered", "basesize=1024"]`         |                   0.97 (5%)  | 0.96 (1%) :white_check_mark: |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 0.50 (5%) :white_check_mark: | 0.51 (1%) :white_check_mark: |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` |                1.12 (5%) :x: |                1.10 (1%) :x: |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  |                1.15 (5%) :x: |                1.16 (1%) :x: |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  |                   0.99 (5%)  | 0.98 (1%) :white_check_mark: |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 0.78 (5%) :white_check_mark: | 0.73 (1%) :white_check_mark: |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |                1.26 (5%) :x: |                1.10 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |                   1.01 (5%)  |                1.19 (1%) :x: |
| `["parallel_histogram", "comm", "basesize=4096"]`   |                1.16 (5%) :x: |                   0.99 (1%)  |
| `["partition_length_maximum", "rand", "reduce"]`    |                   1.00 (5%)  |                1.01 (1%) :x: |
| `["splitby", "count", "man"]`                       | 0.87 (5%) :white_check_mark: |                   1.00 (1%)  |

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
  uname: Linux 5.4.0-1043-azure #45-Ubuntu SMP Fri Mar 19 17:33:38 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2593 MHz      54709 s          0 s       2354 s      39913 s          0 s
       #2  2593 MHz      51929 s          0 s       2494 s      42555 s          0 s
       
  Memory: 6.791343688964844 GB (3720.42578125 MB free)
  Uptime: 975.0 sec
  Load Avg:  1.748046875  1.52685546875  0.92529296875
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
  uname: Linux 5.4.0-1043-azure #45-Ubuntu SMP Fri Mar 19 17:33:38 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2593 MHz      75993 s          0 s       2956 s      48106 s          0 s
       #2  2593 MHz      77176 s          0 s       3054 s      46880 s          0 s
       
  Memory: 6.791343688964844 GB (3729.609375 MB free)
  Uptime: 1277.0 sec
  Load Avg:  1.68798828125  1.57568359375  1.11474609375
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, skylake-avx512)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 21 Apr 2021 - 21:7
* Package commit: 45644d
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
| `["collect", "assoc", "basesize=1"]`                | 237.517 ms (5%) |         |  32.66 MiB (1%) |      286732 |
| `["collect", "assoc", "basesize=1024"]`             | 198.074 ms (5%) |         |   1.79 MiB (1%) |         570 |
| `["collect", "assoc", "basesize=32"]`               | 200.074 ms (5%) |         |   3.97 MiB (1%) |       13306 |
| `["collect", "seq"]`                                | 394.960 ms (5%) |         | 512.72 KiB (1%) |          15 |
| `["collect", "unordered", "basesize=1"]`            | 416.130 ms (5%) |         |  30.01 MiB (1%) |      360553 |
| `["collect", "unordered", "basesize=1024"]`         | 237.341 ms (5%) |         | 806.86 KiB (1%) |        2541 |
| `["collect", "unordered", "basesize=32"]`           | 222.648 ms (5%) |         |   1.48 MiB (1%) |       12718 |
| `["findfirst", "n=1000", "foldl"]`                  | 627.675 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 341.281 ms (5%) |         | 659.41 KiB (1%) |       11575 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 444.222 ms (5%) |         | 485.00 KiB (1%) |        8497 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 604.314 ms (5%) |         | 352.27 KiB (1%) |        6187 |
| `["findfirst", "n=400", "foldl"]`                   | 471.294 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 280.904 ms (5%) |         |   1.23 MiB (1%) |       22062 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 249.270 ms (5%) |         | 590.66 KiB (1%) |       10412 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 276.267 ms (5%) |         | 364.25 KiB (1%) |        6426 |
| `["findfirst", "n=500", "foldl"]`                   |  81.718 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 151.132 ms (5%) |         | 675.97 KiB (1%) |       11778 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 140.764 ms (5%) |         | 375.52 KiB (1%) |        6542 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 106.637 ms (5%) |         | 199.41 KiB (1%) |        3475 |
| `["overhead", "default"]`                           |  61.200 μs (5%) |         |  47.36 KiB (1%) |         382 |
| `["overhead", "stoppable=false"]`                   |  60.901 μs (5%) |         |  47.39 KiB (1%) |         382 |
| `["overhead", "stoppable=true"]`                    | 152.801 μs (5%) |         | 139.67 KiB (1%) |        2464 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   3.962 ms (5%) |         | 730.06 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   4.571 ms (5%) |         |   1.79 MiB (1%) |         213 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   4.277 ms (5%) |         |   1.43 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  12.768 ms (5%) |         |   1.23 MiB (1%) |         465 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  23.754 ms (5%) |         |   1.05 MiB (1%) |        2582 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  18.903 ms (5%) |         |   1.26 MiB (1%) |        1397 |
| `["parallel_histogram", "seq"]`                     |   7.238 ms (5%) |         | 364.61 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  33.733 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  16.878 ms (5%) |         |   2.66 KiB (1%) |          48 |
| `["splitby", "count", "foldl"]`                     |   4.687 ms (5%) |         |   96 bytes (1%) |           4 |
| `["splitby", "count", "man"]`                       |   1.693 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    |   1.169 ms (5%) |         |   2.84 KiB (1%) |          54 |
| `["sum", "random", "foldl"]`                        |  15.916 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "random", "reduce", "basesize=128"]`       |   8.157 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "random", "reduce", "basesize=256"]`       |   8.064 ms (5%) |         |  51.27 KiB (1%) |         507 |
| `["sum", "random", "reduce", "basesize=512"]`       |   8.020 ms (5%) |         |  25.30 KiB (1%) |         252 |
| `["sum", "uniform", "foldl"]`                       |  15.483 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   7.934 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   7.844 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   7.806 ms (5%) |         |  25.25 KiB (1%) |         251 |
| `["sum", "valley", "foldl"]`                        |  15.984 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "valley", "reduce", "basesize=128"]`       |   8.173 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   8.085 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   8.046 ms (5%) |         |  25.25 KiB (1%) |         251 |
| `["words", "nthreads=1"]`                           |  21.546 ms (5%) |         |  31.50 MiB (1%) |     1026653 |
| `["words", "nthreads=2"]`                           |  13.829 ms (5%) |         |  32.22 MiB (1%) |     1026760 |
| `["words", "nthreads=4"]`                           |  13.979 ms (5%) |         |  32.67 MiB (1%) |     1026843 |

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
  uname: Linux 5.4.0-1043-azure #45-Ubuntu SMP Fri Mar 19 17:33:38 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2593 MHz      54709 s          0 s       2354 s      39913 s          0 s
       #2  2593 MHz      51929 s          0 s       2494 s      42555 s          0 s
       
  Memory: 6.791343688964844 GB (3720.42578125 MB free)
  Uptime: 975.0 sec
  Load Avg:  1.748046875  1.52685546875  0.92529296875
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, skylake-avx512)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 21 Apr 2021 - 21:12
* Package commit: 163057
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
| `["collect", "assoc", "basesize=1"]`                | 238.274 ms (5%) |         |  32.66 MiB (1%) |      286741 |
| `["collect", "assoc", "basesize=1024"]`             | 198.345 ms (5%) |         |   1.79 MiB (1%) |         570 |
| `["collect", "assoc", "basesize=32"]`               | 199.938 ms (5%) |         |   3.97 MiB (1%) |       13307 |
| `["collect", "seq"]`                                | 395.099 ms (5%) |         | 512.72 KiB (1%) |          15 |
| `["collect", "unordered", "basesize=1"]`            | 416.673 ms (5%) |         |  30.01 MiB (1%) |      360559 |
| `["collect", "unordered", "basesize=1024"]`         | 245.433 ms (5%) |         | 839.86 KiB (1%) |        3615 |
| `["collect", "unordered", "basesize=32"]`           | 223.080 ms (5%) |         |   1.47 MiB (1%) |       12631 |
| `["findfirst", "n=1000", "foldl"]`                  | 626.555 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 680.201 ms (5%) |         |   1.26 MiB (1%) |       22524 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 442.600 ms (5%) |         | 485.00 KiB (1%) |        8497 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 538.880 ms (5%) |         | 319.72 KiB (1%) |        5606 |
| `["findfirst", "n=400", "foldl"]`                   | 470.094 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 244.814 ms (5%) |         |   1.06 MiB (1%) |       19032 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 250.797 ms (5%) |         | 604.70 KiB (1%) |       10662 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 270.030 ms (5%) |         | 366.38 KiB (1%) |        6457 |
| `["findfirst", "n=500", "foldl"]`                   |  81.492 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 194.817 ms (5%) |         | 923.34 KiB (1%) |       16076 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 111.615 ms (5%) |         | 340.33 KiB (1%) |        5917 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 105.197 ms (5%) |         | 167.50 KiB (1%) |        2934 |
| `["overhead", "default"]`                           |  62.001 μs (5%) |         |  47.36 KiB (1%) |         382 |
| `["overhead", "stoppable=false"]`                   |  62.101 μs (5%) |         |  47.39 KiB (1%) |         382 |
| `["overhead", "stoppable=true"]`                    | 156.601 μs (5%) |         | 139.67 KiB (1%) |        2464 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   3.990 ms (5%) |         | 730.06 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   4.596 ms (5%) |         |   1.79 MiB (1%) |         213 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   4.299 ms (5%) |         |   1.43 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  12.902 ms (5%) |         |   1.22 MiB (1%) |         282 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  20.459 ms (5%) |         |   1.06 MiB (1%) |        2712 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  18.936 ms (5%) |         |   1.25 MiB (1%) |        1150 |
| `["parallel_histogram", "seq"]`                     |   7.317 ms (5%) |         | 364.61 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  33.730 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  16.878 ms (5%) |         |   2.63 KiB (1%) |          47 |
| `["splitby", "count", "foldl"]`                     |   4.704 ms (5%) |         |   96 bytes (1%) |           4 |
| `["splitby", "count", "man"]`                       |   1.945 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    |   1.186 ms (5%) |         |   2.84 KiB (1%) |          54 |
| `["sum", "random", "foldl"]`                        |  15.879 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "random", "reduce", "basesize=128"]`       |   8.157 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "random", "reduce", "basesize=256"]`       |   8.060 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "random", "reduce", "basesize=512"]`       |   8.010 ms (5%) |         |  25.30 KiB (1%) |         252 |
| `["sum", "uniform", "foldl"]`                       |  15.483 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   7.984 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   7.866 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   7.816 ms (5%) |         |  25.25 KiB (1%) |         251 |
| `["sum", "valley", "foldl"]`                        |  16.110 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "valley", "reduce", "basesize=128"]`       |   8.229 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   8.100 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   8.101 ms (5%) |         |  25.25 KiB (1%) |         251 |
| `["words", "nthreads=1"]`                           |  21.568 ms (5%) |         |  31.68 MiB (1%) |     1032266 |
| `["words", "nthreads=2"]`                           |  13.208 ms (5%) |         |  32.04 MiB (1%) |     1032313 |
| `["words", "nthreads=4"]`                           |  13.717 ms (5%) |         |  32.76 MiB (1%) |     1032414 |

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
  uname: Linux 5.4.0-1043-azure #45-Ubuntu SMP Fri Mar 19 17:33:38 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2593 MHz      75993 s          0 s       2956 s      48106 s          0 s
       #2  2593 MHz      77176 s          0 s       3054 s      46880 s          0 s
       
  Memory: 6.791343688964844 GB (3729.609375 MB free)
  Uptime: 1277.0 sec
  Load Avg:  1.68798828125  1.57568359375  1.11474609375
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
    CPU MHz:                         2593.904
    BogoMIPS:                        5187.80
    Hypervisor vendor:               Microsoft
    Virtualization type:             full
    L1d cache:                       64 KiB
    L1i cache:                       64 KiB
    L2 cache:                        2 MiB
    L3 cache:                        35.8 MiB
    NUMA node0 CPU(s):               0,1
    Vulnerability Itlb multihit:     KVM: Vulnerable
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

