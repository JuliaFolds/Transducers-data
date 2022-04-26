# Multi-thread benchmark result

* Pull request commit: [`7dcb7426a3b4d2328f92fb758692e3cb5b533bdc`](https://github.com/JuliaFolds/Transducers.jl/commit/7dcb7426a3b4d2328f92fb758692e3cb5b533bdc)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/243> (Update */Manifest.toml)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 26 Apr 2022 - 02:10
    - Baseline: 26 Apr 2022 - 02:16
* Package commits:
    - Target: 3c875e
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
| `["collect", "assoc", "basesize=1"]`                |                1.06 (5%) :x: |                   1.00 (1%)  |
| `["collect", "assoc", "basesize=1024"]`             |                1.06 (5%) :x: |                   1.00 (1%)  |
| `["collect", "assoc", "basesize=32"]`               |                1.07 (5%) :x: |                   1.00 (1%)  |
| `["collect", "unordered", "basesize=1024"]`         |                   1.00 (5%)  |                1.03 (1%) :x: |
| `["findfirst", "n=1000", "foldl"]`                  |                1.13 (5%) :x: |                   1.00 (1%)  |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` |                1.08 (5%) :x: |                1.03 (1%) :x: |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` |                   0.97 (5%)  | 0.94 (1%) :white_check_mark: |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 0.85 (5%) :white_check_mark: | 0.75 (1%) :white_check_mark: |
| `["findfirst", "n=400", "foldl"]`                   |                1.13 (5%) :x: |                   1.00 (1%)  |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  |                   1.03 (5%)  | 0.94 (1%) :white_check_mark: |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  |                1.07 (5%) :x: |                1.01 (1%) :x: |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  |                1.10 (5%) :x: | 0.98 (1%) :white_check_mark: |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 0.85 (5%) :white_check_mark: | 0.86 (1%) :white_check_mark: |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 0.33 (5%) :white_check_mark: | 0.41 (1%) :white_check_mark: |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |                1.17 (5%) :x: |                1.08 (1%) :x: |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |                   0.99 (5%)  |                1.15 (1%) :x: |
| `["parallel_histogram", "comm", "basesize=16384"]`  |                1.13 (5%) :x: |                1.01 (1%) :x: |
| `["parallel_histogram", "comm", "basesize=4096"]`   | 0.94 (5%) :white_check_mark: |                   1.01 (1%)  |
| `["parallel_histogram", "comm", "basesize=8192"]`   |                   0.96 (5%)  |                1.20 (1%) :x: |
| `["parallel_histogram", "seq"]`                     |                1.13 (5%) :x: |                   1.00 (1%)  |
| `["partition_length_maximum", "rand", "foldl"]`     |                1.14 (5%) :x: |                   1.00 (1%)  |
| `["splitby", "count", "foldl"]`                     |                1.06 (5%) :x: |                   1.00 (1%)  |
| `["sum", "random", "reduce", "basesize=128"]`       |                1.07 (5%) :x: |                   1.00 (1%)  |
| `["sum", "random", "reduce", "basesize=256"]`       |                1.07 (5%) :x: |                   1.00 (1%)  |
| `["sum", "random", "reduce", "basesize=512"]`       |                1.07 (5%) :x: |                   1.00 (1%)  |
| `["sum", "uniform", "reduce", "basesize=128"]`      |                1.07 (5%) :x: |                   1.00 (1%)  |
| `["sum", "uniform", "reduce", "basesize=256"]`      |                1.07 (5%) :x: |                   1.00 (1%)  |
| `["sum", "uniform", "reduce", "basesize=512"]`      |                1.07 (5%) :x: |                   1.00 (1%)  |
| `["sum", "valley", "reduce", "basesize=128"]`       |                1.07 (5%) :x: |                   1.00 (1%)  |
| `["sum", "valley", "reduce", "basesize=256"]`       |                1.07 (5%) :x: |                   1.00 (1%)  |
| `["sum", "valley", "reduce", "basesize=512"]`       |                1.07 (5%) :x: |                   1.00 (1%)  |
| `["words", "nthreads=1"]`                           |                1.07 (5%) :x: |                   1.00 (1%)  |
| `["words", "nthreads=2"]`                           | 0.94 (5%) :white_check_mark: | 0.99 (1%) :white_check_mark: |

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
  CPU: Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2593 MHz       5512 s          2 s        219 s       3027 s          0 s
       #2  2593 MHz       4736 s          1 s        223 s       3826 s          0 s
       
  Memory: 6.783611297607422 GB (3882.4375 MB free)
  Uptime: 883.71 sec
  Load Avg:  1.51  1.44  0.88
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
  CPU: Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2593 MHz       7948 s          2 s        286 s       3641 s          0 s
       #2  2593 MHz       7042 s          1 s        292 s       4568 s          0 s
       
  Memory: 6.783611297607422 GB (3842.35546875 MB free)
  Uptime: 1196.02 sec
  Load Avg:  1.63  1.55  1.1
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, skylake-avx512)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 26 Apr 2022 - 2:10
* Package commit: 3c875e
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

| ID                                                  | time            | GC time | memory          | allocations |
|-----------------------------------------------------|----------------:|--------:|----------------:|------------:|
| `["collect", "assoc", "basesize=1"]`                | 248.305 ms (5%) |         |  25.97 MiB (1%) |      306829 |
| `["collect", "assoc", "basesize=1024"]`             | 198.492 ms (5%) |         |   2.61 MiB (1%) |         455 |
| `["collect", "assoc", "basesize=32"]`               | 201.018 ms (5%) |         |   4.82 MiB (1%) |       11714 |
| `["collect", "seq"]`                                | 395.227 ms (5%) |         | 812.73 KiB (1%) |          11 |
| `["collect", "unordered", "basesize=1"]`            | 349.595 ms (5%) |         |  24.00 MiB (1%) |      416243 |
| `["collect", "unordered", "basesize=1024"]`         | 200.304 ms (5%) |         |   1.02 MiB (1%) |        1302 |
| `["collect", "unordered", "basesize=32"]`           | 212.296 ms (5%) |         |   1.61 MiB (1%) |       15540 |
| `["findfirst", "n=1000", "foldl"]`                  | 629.593 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 343.961 ms (5%) |         | 230.78 KiB (1%) |        3239 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 424.004 ms (5%) |         | 157.20 KiB (1%) |        2193 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 579.783 ms (5%) |         | 103.62 KiB (1%) |        1457 |
| `["findfirst", "n=400", "foldl"]`                   | 472.203 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 241.740 ms (5%) |         | 371.53 KiB (1%) |        5309 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 249.378 ms (5%) |         | 203.31 KiB (1%) |        2906 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 375.984 ms (5%) |         | 152.44 KiB (1%) |        2188 |
| `["findfirst", "n=500", "foldl"]`                   |  81.907 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 119.751 ms (5%) |         | 187.94 KiB (1%) |        2593 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |  72.330 ms (5%) |         |  71.47 KiB (1%) |         979 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 233.659 ms (5%) |         |  99.38 KiB (1%) |        1359 |
| `["overhead", "default"]`                           |  71.401 μs (5%) |         |  32.77 KiB (1%) |         419 |
| `["overhead", "stoppable=false"]`                   |  69.401 μs (5%) |         |  32.75 KiB (1%) |         418 |
| `["overhead", "stoppable=true"]`                    |  79.201 μs (5%) |         |  44.25 KiB (1%) |         610 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   3.224 ms (5%) |         | 728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   3.744 ms (5%) |         |   2.05 MiB (1%) |         222 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   3.537 ms (5%) |         |   1.42 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  17.476 ms (5%) |         |   1.58 MiB (1%) |        2315 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  24.370 ms (5%) |         |   1.23 MiB (1%) |        6456 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  22.085 ms (5%) |         |   1.63 MiB (1%) |        4037 |
| `["parallel_histogram", "seq"]`                     |   5.784 ms (5%) |         | 364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  35.291 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  17.651 ms (5%) |         |  736 bytes (1%) |          11 |
| `["splitby", "count", "foldl"]`                     |   2.312 ms (5%) |         |                 |             |
| `["splitby", "count", "man"]`                       |   1.752 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    |   1.089 ms (5%) |         |   1.09 KiB (1%) |          19 |
| `["sum", "random", "foldl"]`                        |  16.275 ms (5%) |         |                 |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   8.175 ms (5%) |         |  74.20 KiB (1%) |        1105 |
| `["sum", "random", "reduce", "basesize=256"]`       |   8.065 ms (5%) |         |  36.73 KiB (1%) |         546 |
| `["sum", "random", "reduce", "basesize=512"]`       |   8.027 ms (5%) |         |  18.14 KiB (1%) |         271 |
| `["sum", "uniform", "foldl"]`                       |  15.645 ms (5%) |         |                 |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   8.034 ms (5%) |         |  74.23 KiB (1%) |        1106 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   7.927 ms (5%) |         |  36.73 KiB (1%) |         546 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   7.871 ms (5%) |         |  18.00 KiB (1%) |         267 |
| `["sum", "valley", "foldl"]`                        |  16.126 ms (5%) |         |                 |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   8.248 ms (5%) |         |  74.14 KiB (1%) |        1103 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   8.151 ms (5%) |         |  36.70 KiB (1%) |         545 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   8.128 ms (5%) |         |  18.06 KiB (1%) |         269 |
| `["words", "nthreads=1"]`                           |  24.006 ms (5%) |         |  31.77 MiB (1%) |     1034734 |
| `["words", "nthreads=2"]`                           |  14.842 ms (5%) |         |  32.13 MiB (1%) |     1034796 |
| `["words", "nthreads=4"]`                           |  14.581 ms (5%) |         |  33.02 MiB (1%) |     1034943 |

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
  CPU: Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2593 MHz       5512 s          2 s        219 s       3027 s          0 s
       #2  2593 MHz       4736 s          1 s        223 s       3826 s          0 s
       
  Memory: 6.783611297607422 GB (3882.4375 MB free)
  Uptime: 883.71 sec
  Load Avg:  1.51  1.44  0.88
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, skylake-avx512)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 26 Apr 2022 - 2:16
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
| `["collect", "assoc", "basesize=1"]`                | 233.481 ms (5%) |         |   25.97 MiB (1%) |      306842 |
| `["collect", "assoc", "basesize=1024"]`             | 186.453 ms (5%) |         |    2.61 MiB (1%) |         457 |
| `["collect", "assoc", "basesize=32"]`               | 188.276 ms (5%) |         |    4.82 MiB (1%) |       11707 |
| `["collect", "seq"]`                                | 395.353 ms (5%) |         |  812.73 KiB (1%) |          11 |
| `["collect", "unordered", "basesize=1"]`            | 349.241 ms (5%) |         |   23.93 MiB (1%) |      413966 |
| `["collect", "unordered", "basesize=1024"]`         | 200.930 ms (5%) |         | 1012.80 KiB (1%) |        1221 |
| `["collect", "unordered", "basesize=32"]`           | 211.400 ms (5%) |         |    1.59 MiB (1%) |       15059 |
| `["findfirst", "n=1000", "foldl"]`                  | 555.889 ms (5%) |         |                  |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 317.050 ms (5%) |         |  224.89 KiB (1%) |        3172 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 437.259 ms (5%) |         |  166.38 KiB (1%) |        2328 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 680.663 ms (5%) |         |  138.06 KiB (1%) |        1916 |
| `["findfirst", "n=400", "foldl"]`                   | 416.880 ms (5%) |         |                  |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 234.907 ms (5%) |         |  393.28 KiB (1%) |        5583 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 232.600 ms (5%) |         |  200.62 KiB (1%) |        2865 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 341.368 ms (5%) |         |  156.19 KiB (1%) |        2229 |
| `["findfirst", "n=500", "foldl"]`                   |  81.935 ms (5%) |         |                  |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 141.564 ms (5%) |         |  217.34 KiB (1%) |        3021 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 219.779 ms (5%) |         |  174.33 KiB (1%) |        2400 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 199.488 ms (5%) |         |   92.23 KiB (1%) |        1262 |
| `["overhead", "default"]`                           |  69.300 μs (5%) |         |   32.70 KiB (1%) |         417 |
| `["overhead", "stoppable=false"]`                   |  69.701 μs (5%) |         |   32.75 KiB (1%) |         418 |
| `["overhead", "stoppable=true"]`                    |  81.000 μs (5%) |         |   44.25 KiB (1%) |         610 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   3.239 ms (5%) |         |  728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   3.775 ms (5%) |         |    1.79 MiB (1%) |         216 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   3.564 ms (5%) |         |    1.42 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  15.462 ms (5%) |         |    1.56 MiB (1%) |        1771 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  25.957 ms (5%) |         |    1.22 MiB (1%) |        6103 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  23.041 ms (5%) |         |    1.36 MiB (1%) |        6034 |
| `["parallel_histogram", "seq"]`                     |   5.100 ms (5%) |         |  364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  31.088 ms (5%) |         |                  |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  17.662 ms (5%) |         |   736 bytes (1%) |          11 |
| `["splitby", "count", "foldl"]`                     |   2.189 ms (5%) |         |                  |             |
| `["splitby", "count", "man"]`                       |   1.754 ms (5%) |         |                  |             |
| `["splitby", "count", "reduce"]`                    |   1.090 ms (5%) |         |    1.09 KiB (1%) |          19 |
| `["sum", "random", "foldl"]`                        |  16.186 ms (5%) |         |                  |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   7.605 ms (5%) |         |   74.17 KiB (1%) |        1104 |
| `["sum", "random", "reduce", "basesize=256"]`       |   7.550 ms (5%) |         |   36.73 KiB (1%) |         546 |
| `["sum", "random", "reduce", "basesize=512"]`       |   7.496 ms (5%) |         |   18.08 KiB (1%) |         269 |
| `["sum", "uniform", "foldl"]`                       |  15.723 ms (5%) |         |                  |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   7.508 ms (5%) |         |   74.11 KiB (1%) |        1102 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   7.399 ms (5%) |         |   36.70 KiB (1%) |         545 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   7.333 ms (5%) |         |   18.06 KiB (1%) |         269 |
| `["sum", "valley", "foldl"]`                        |  16.135 ms (5%) |         |                  |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   7.741 ms (5%) |         |   74.11 KiB (1%) |        1102 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   7.640 ms (5%) |         |   36.70 KiB (1%) |         545 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   7.602 ms (5%) |         |   18.03 KiB (1%) |         268 |
| `["words", "nthreads=1"]`                           |  22.422 ms (5%) |         |   31.77 MiB (1%) |     1034905 |
| `["words", "nthreads=2"]`                           |  15.810 ms (5%) |         |   32.48 MiB (1%) |     1034978 |
| `["words", "nthreads=4"]`                           |  14.830 ms (5%) |         |   33.11 MiB (1%) |     1035138 |

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
  CPU: Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2593 MHz       7948 s          2 s        286 s       3641 s          0 s
       #2  2593 MHz       7042 s          1 s        292 s       4568 s          0 s
       
  Memory: 6.783611297607422 GB (3842.35546875 MB free)
  Uptime: 1196.02 sec
  Load Avg:  1.63  1.55  1.1
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
    Vulnerability Spectre v2:        Mitigation; Retpolines, STIBP disabled, RSB filling
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

