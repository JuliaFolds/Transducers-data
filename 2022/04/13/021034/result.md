# Multi-thread benchmark result

* Pull request commit: [`a30202dcc89292b9ea8c06f85fd19af29454e824`](https://github.com/JuliaFolds/Transducers.jl/commit/a30202dcc89292b9ea8c06f85fd19af29454e824)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/243> (Update */Manifest.toml)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 13 Apr 2022 - 02:04
    - Baseline: 13 Apr 2022 - 02:10
* Package commits:
    - Target: e9f59c
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
| `["collect", "unordered", "basesize=1024"]`         |                   1.01 (5%)  |                1.01 (1%) :x: |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` |                1.40 (5%) :x: |                1.43 (1%) :x: |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` |                1.14 (5%) :x: |                1.19 (1%) :x: |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 0.74 (5%) :white_check_mark: | 0.75 (1%) :white_check_mark: |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  |                   1.05 (5%)  | 0.97 (1%) :white_check_mark: |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  |                   0.98 (5%)  | 0.99 (1%) :white_check_mark: |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  |                1.10 (5%) :x: |                   1.00 (1%)  |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |                1.87 (5%) :x: |                1.71 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |                2.34 (5%) :x: |                2.04 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |                2.29 (5%) :x: |                1.70 (1%) :x: |
| `["overhead", "default"]`                           |                1.07 (5%) :x: |                   1.00 (1%)  |
| `["overhead", "stoppable=false"]`                   |                1.05 (5%) :x: |                   1.00 (1%)  |
| `["overhead", "stoppable=true"]`                    |                1.08 (5%) :x: |                   1.00 (1%)  |
| `["parallel_histogram", "assoc", "basesize=4096"]`  | 0.88 (5%) :white_check_mark: | 0.87 (1%) :white_check_mark: |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |                1.06 (5%) :x: |                   1.00 (1%)  |
| `["parallel_histogram", "comm", "basesize=16384"]`  | 0.95 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["parallel_histogram", "comm", "basesize=4096"]`   |                   0.98 (5%)  | 0.97 (1%) :white_check_mark: |
| `["parallel_histogram", "comm", "basesize=8192"]`   |                   0.99 (5%)  | 0.97 (1%) :white_check_mark: |
| `["partition_length_maximum", "rand", "reduce"]`    |                   0.96 (5%)  |                1.05 (1%) :x: |
| `["splitby", "count", "foldl"]`                     | 0.90 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["splitby", "count", "reduce"]`                    | 0.92 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["sum", "random", "foldl"]`                        | 0.91 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["sum", "random", "reduce", "basesize=128"]`       | 0.95 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["sum", "random", "reduce", "basesize=256"]`       | 0.89 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["sum", "random", "reduce", "basesize=512"]`       | 0.90 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["sum", "uniform", "reduce", "basesize=512"]`      | 0.94 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["sum", "valley", "reduce", "basesize=128"]`       | 0.91 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["words", "nthreads=2"]`                           |                1.06 (5%) :x: | 0.99 (1%) :white_check_mark: |

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
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz       5131 s          1 s        233 s       3169 s          0 s
       #2  2095 MHz       5352 s          2 s        248 s       2944 s          0 s
       
  Memory: 6.783611297607422 GB (3650.25390625 MB free)
  Uptime: 858.54 sec
  Load Avg:  1.65  1.49  0.93
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, skylake-avx512)
```

### Baseline
```
Julia Version 1.7.2
Commit bf53498635 (2022-02-06 15:21 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 20.04.4 LTS
  uname: Linux 5.13.0-1021-azure #24~20.04.1-Ubuntu SMP Tue Mar 29 15:34:22 UTC 2022 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz       7935 s          1 s        305 s       3499 s          0 s
       #2  2095 MHz       7444 s          2 s        305 s       4001 s          0 s
       
  Memory: 6.783611297607422 GB (3594.76953125 MB free)
  Uptime: 1179.6 sec
  Load Avg:  1.73  1.58  1.13
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, skylake-avx512)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 13 Apr 2022 - 2:4
* Package commit: e9f59c
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

| ID                                                  | time            | GC time | memory           | allocations |
|-----------------------------------------------------|----------------:|--------:|-----------------:|------------:|
| `["collect", "assoc", "basesize=1"]`                | 259.024 ms (5%) |         |   25.97 MiB (1%) |      306860 |
| `["collect", "assoc", "basesize=1024"]`             | 227.218 ms (5%) |         |    2.61 MiB (1%) |         455 |
| `["collect", "assoc", "basesize=32"]`               | 227.319 ms (5%) |         |    4.82 MiB (1%) |       11714 |
| `["collect", "seq"]`                                | 416.656 ms (5%) |         |  812.73 KiB (1%) |          11 |
| `["collect", "unordered", "basesize=1"]`            | 383.264 ms (5%) |         |   23.87 MiB (1%) |      411928 |
| `["collect", "unordered", "basesize=1024"]`         | 245.004 ms (5%) |         | 1011.42 KiB (1%) |        1030 |
| `["collect", "unordered", "basesize=32"]`           | 252.666 ms (5%) |         |    1.58 MiB (1%) |       14734 |
| `["findfirst", "n=1000", "foldl"]`                  | 674.574 ms (5%) |         |                  |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 561.816 ms (5%) |         |  329.28 KiB (1%) |        4608 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 536.364 ms (5%) |         |  168.66 KiB (1%) |        2354 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 488.968 ms (5%) |         |   81.36 KiB (1%) |        1147 |
| `["findfirst", "n=400", "foldl"]`                   | 503.455 ms (5%) |         |                  |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 277.655 ms (5%) |         |  376.19 KiB (1%) |        5371 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 271.853 ms (5%) |         |  200.80 KiB (1%) |        2871 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 388.798 ms (5%) |         |  141.58 KiB (1%) |        2019 |
| `["findfirst", "n=500", "foldl"]`                   |  84.566 ms (5%) |         |                  |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 245.671 ms (5%) |         |  298.92 KiB (1%) |        4128 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 318.876 ms (5%) |         |  198.75 KiB (1%) |        2785 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 247.017 ms (5%) |         |   93.91 KiB (1%) |        1290 |
| `["overhead", "default"]`                           |  82.807 μs (5%) |         |   32.70 KiB (1%) |         417 |
| `["overhead", "stoppable=false"]`                   |  81.907 μs (5%) |         |   32.75 KiB (1%) |         418 |
| `["overhead", "stoppable=true"]`                    |  94.908 μs (5%) |         |   44.22 KiB (1%) |         609 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   3.156 ms (5%) |         |  728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   3.773 ms (5%) |         |    1.79 MiB (1%) |         216 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   3.664 ms (5%) |         |    1.42 MiB (1%) |         118 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  19.291 ms (5%) |         |    1.60 MiB (1%) |        3051 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  28.292 ms (5%) |         |    1.24 MiB (1%) |        6752 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  25.968 ms (5%) |         |    1.26 MiB (1%) |        5844 |
| `["parallel_histogram", "seq"]`                     |   5.447 ms (5%) |         |  364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  36.546 ms (5%) |         |                  |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  18.052 ms (5%) |         |   736 bytes (1%) |          11 |
| `["splitby", "count", "foldl"]`                     |   1.916 ms (5%) |         |                  |             |
| `["splitby", "count", "man"]`                       |   1.460 ms (5%) |         |                  |             |
| `["splitby", "count", "reduce"]`                    |   1.055 ms (5%) |         |    1.06 KiB (1%) |          18 |
| `["sum", "random", "foldl"]`                        |  16.235 ms (5%) |         |                  |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   8.669 ms (5%) |         |   74.17 KiB (1%) |        1104 |
| `["sum", "random", "reduce", "basesize=256"]`       |   7.919 ms (5%) |         |   36.77 KiB (1%) |         547 |
| `["sum", "random", "reduce", "basesize=512"]`       |   8.028 ms (5%) |         |   18.08 KiB (1%) |         269 |
| `["sum", "uniform", "foldl"]`                       |  15.591 ms (5%) |         |                  |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   8.508 ms (5%) |         |   74.14 KiB (1%) |        1103 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   8.145 ms (5%) |         |   36.70 KiB (1%) |         545 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   7.568 ms (5%) |         |   18.03 KiB (1%) |         268 |
| `["sum", "valley", "foldl"]`                        |  16.287 ms (5%) |         |                  |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   8.061 ms (5%) |         |   74.08 KiB (1%) |        1101 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   8.238 ms (5%) |         |   36.77 KiB (1%) |         547 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   7.947 ms (5%) |         |   18.03 KiB (1%) |         268 |
| `["words", "nthreads=1"]`                           |  22.428 ms (5%) |         |   31.67 MiB (1%) |     1032012 |
| `["words", "nthreads=2"]`                           |  16.420 ms (5%) |         |   32.03 MiB (1%) |     1032053 |
| `["words", "nthreads=4"]`                           |  15.878 ms (5%) |         |   32.74 MiB (1%) |     1032131 |

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
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz       5131 s          1 s        233 s       3169 s          0 s
       #2  2095 MHz       5352 s          2 s        248 s       2944 s          0 s
       
  Memory: 6.783611297607422 GB (3650.25390625 MB free)
  Uptime: 858.54 sec
  Load Avg:  1.65  1.49  0.93
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, skylake-avx512)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 13 Apr 2022 - 2:10
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

| ID                                                  | time            | GC time | memory           | allocations |
|-----------------------------------------------------|----------------:|--------:|-----------------:|------------:|
| `["collect", "assoc", "basesize=1"]`                | 269.305 ms (5%) |         |   25.97 MiB (1%) |      306842 |
| `["collect", "assoc", "basesize=1024"]`             | 218.512 ms (5%) |         |    2.61 MiB (1%) |         456 |
| `["collect", "assoc", "basesize=32"]`               | 227.629 ms (5%) |         |    4.82 MiB (1%) |       11709 |
| `["collect", "seq"]`                                | 423.758 ms (5%) |         |  812.73 KiB (1%) |          11 |
| `["collect", "unordered", "basesize=1"]`            | 382.473 ms (5%) |         |   23.92 MiB (1%) |      413494 |
| `["collect", "unordered", "basesize=1024"]`         | 243.219 ms (5%) |         | 1001.08 KiB (1%) |        1049 |
| `["collect", "unordered", "basesize=32"]`           | 254.442 ms (5%) |         |    1.58 MiB (1%) |       14753 |
| `["findfirst", "n=1000", "foldl"]`                  | 672.703 ms (5%) |         |                  |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 400.987 ms (5%) |         |  230.42 KiB (1%) |        3243 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 472.384 ms (5%) |         |  141.14 KiB (1%) |        1996 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 657.340 ms (5%) |         |  108.55 KiB (1%) |        1509 |
| `["findfirst", "n=400", "foldl"]`                   | 497.052 ms (5%) |         |                  |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 265.302 ms (5%) |         |  387.19 KiB (1%) |        5509 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 276.243 ms (5%) |         |  202.89 KiB (1%) |        2915 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 352.560 ms (5%) |         |  142.12 KiB (1%) |        2012 |
| `["findfirst", "n=500", "foldl"]`                   |  86.510 ms (5%) |         |                  |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 131.490 ms (5%) |         |  175.03 KiB (1%) |        2395 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 136.151 ms (5%) |         |   97.23 KiB (1%) |        1335 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 108.031 ms (5%) |         |   55.09 KiB (1%) |         743 |
| `["overhead", "default"]`                           |  77.107 μs (5%) |         |   32.70 KiB (1%) |         417 |
| `["overhead", "stoppable=false"]`                   |  77.806 μs (5%) |         |   32.78 KiB (1%) |         419 |
| `["overhead", "stoppable=true"]`                    |  88.007 μs (5%) |         |   44.25 KiB (1%) |         610 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   3.105 ms (5%) |         |  728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   4.305 ms (5%) |         |    2.05 MiB (1%) |         221 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   3.447 ms (5%) |         |    1.42 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  20.355 ms (5%) |         |    1.60 MiB (1%) |        3165 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  28.745 ms (5%) |         |    1.27 MiB (1%) |        7814 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  26.268 ms (5%) |         |    1.30 MiB (1%) |        6256 |
| `["parallel_histogram", "seq"]`                     |   5.682 ms (5%) |         |  364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  35.788 ms (5%) |         |                  |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  18.830 ms (5%) |         |   704 bytes (1%) |          10 |
| `["splitby", "count", "foldl"]`                     |   2.139 ms (5%) |         |                  |             |
| `["splitby", "count", "man"]`                       |   1.464 ms (5%) |         |                  |             |
| `["splitby", "count", "reduce"]`                    |   1.148 ms (5%) |         |    1.06 KiB (1%) |          18 |
| `["sum", "random", "foldl"]`                        |  17.817 ms (5%) |         |                  |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   9.164 ms (5%) |         |   74.14 KiB (1%) |        1103 |
| `["sum", "random", "reduce", "basesize=256"]`       |   8.910 ms (5%) |         |   36.67 KiB (1%) |         544 |
| `["sum", "random", "reduce", "basesize=512"]`       |   8.892 ms (5%) |         |   18.11 KiB (1%) |         270 |
| `["sum", "uniform", "foldl"]`                       |  16.304 ms (5%) |         |                  |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   8.794 ms (5%) |         |   74.05 KiB (1%) |        1100 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   8.173 ms (5%) |         |   36.77 KiB (1%) |         547 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   8.050 ms (5%) |         |   17.97 KiB (1%) |         266 |
| `["sum", "valley", "foldl"]`                        |  16.471 ms (5%) |         |                  |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   8.855 ms (5%) |         |   74.11 KiB (1%) |        1102 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   8.220 ms (5%) |         |   36.70 KiB (1%) |         545 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   8.171 ms (5%) |         |   18.06 KiB (1%) |         269 |
| `["words", "nthreads=1"]`                           |  22.874 ms (5%) |         |   31.72 MiB (1%) |     1033881 |
| `["words", "nthreads=2"]`                           |  15.461 ms (5%) |         |   32.44 MiB (1%) |     1033957 |
| `["words", "nthreads=4"]`                           |  15.203 ms (5%) |         |   33.06 MiB (1%) |     1034094 |

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
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz       7935 s          1 s        305 s       3499 s          0 s
       #2  2095 MHz       7444 s          2 s        305 s       4001 s          0 s
       
  Memory: 6.783611297607422 GB (3594.76953125 MB free)
  Uptime: 1179.6 sec
  Load Avg:  1.73  1.58  1.13
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
    CPU MHz:                         2095.227
    BogoMIPS:                        4190.45
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

