# Multi-thread benchmark result

* Pull request commit: [`7424230ba86099e4dd9ae008a5ec62f0a8cc06fc`](https://github.com/JuliaFolds/Transducers.jl/commit/7424230ba86099e4dd9ae008a5ec62f0a8cc06fc)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/243> (Update */Manifest.toml)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 2 Feb 2022 - 01:21
    - Baseline: 2 Feb 2022 - 01:26
* Package commits:
    - Target: 5e518b
    - Baseline: 332ac4
* Julia commits:
    - Target: ac5cc9
    - Baseline: ac5cc9
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
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 0.72 (5%) :white_check_mark: | 0.70 (1%) :white_check_mark: |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` |                   1.00 (5%)  |                1.05 (1%) :x: |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  |                   1.00 (5%)  |                1.02 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |                1.43 (5%) :x: |                1.22 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |                1.29 (5%) :x: |                1.15 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |                1.40 (5%) :x: |                1.28 (1%) :x: |
| `["parallel_histogram", "comm", "basesize=4096"]`   |                   1.00 (5%)  | 0.99 (1%) :white_check_mark: |
| `["parallel_histogram", "comm", "basesize=8192"]`   |                   0.96 (5%)  | 0.97 (1%) :white_check_mark: |
| `["sum", "uniform", "reduce", "basesize=256"]`      | 0.95 (5%) :white_check_mark: |                   1.00 (1%)  |

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
Julia Version 1.7.1
Commit ac5cc99908 (2021-12-22 19:35 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 20.04.3 LTS
  uname: Linux 5.11.0-1027-azure #30~20.04.1-Ubuntu SMP Wed Jan 12 20:56:50 UTC 2022 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2593 MHz       4760 s          1 s        287 s       2403 s          0 s
       #2  2593 MHz       5933 s          2 s        298 s       1236 s          0 s
       
  Memory: 6.788978576660156 GB (3464.4609375 MB free)
  Uptime: 752.45 sec
  Load Avg:  1.74  1.55  0.95
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, skylake-avx512)
```

### Baseline
```
Julia Version 1.7.1
Commit ac5cc99908 (2021-12-22 19:35 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 20.04.3 LTS
  uname: Linux 5.11.0-1027-azure #30~20.04.1-Ubuntu SMP Wed Jan 12 20:56:50 UTC 2022 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2593 MHz       7344 s          1 s        366 s       3128 s          0 s
       #2  2593 MHz       8377 s          2 s        383 s       2092 s          0 s
       
  Memory: 6.788978576660156 GB (3378.4765625 MB free)
  Uptime: 1091.75 sec
  Load Avg:  1.43  1.52  1.12
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, skylake-avx512)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 2 Feb 2022 - 1:21
* Package commit: 5e518b
* Julia commit: ac5cc9
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
| `["collect", "assoc", "basesize=1"]`                | 251.688 ms (5%) |         |   25.97 MiB (1%) |      306853 |
| `["collect", "assoc", "basesize=1024"]`             | 199.702 ms (5%) |         |    2.61 MiB (1%) |         455 |
| `["collect", "assoc", "basesize=32"]`               | 202.710 ms (5%) |         |    4.82 MiB (1%) |       11715 |
| `["collect", "seq"]`                                | 395.428 ms (5%) |         |  812.73 KiB (1%) |          11 |
| `["collect", "unordered", "basesize=1"]`            | 362.195 ms (5%) |         |   23.71 MiB (1%) |      406659 |
| `["collect", "unordered", "basesize=1024"]`         | 214.963 ms (5%) |         | 1001.80 KiB (1%) |         944 |
| `["collect", "unordered", "basesize=32"]`           | 226.712 ms (5%) |         |    1.58 MiB (1%) |       14539 |
| `["findfirst", "n=1000", "foldl"]`                  | 629.719 ms (5%) |         |                  |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 355.955 ms (5%) |         |  229.12 KiB (1%) |        3232 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 424.754 ms (5%) |         |  157.20 KiB (1%) |        2193 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 568.650 ms (5%) |         |  108.58 KiB (1%) |        1510 |
| `["findfirst", "n=400", "foldl"]`                   | 472.308 ms (5%) |         |                  |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 247.059 ms (5%) |         |  385.39 KiB (1%) |        5480 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 249.651 ms (5%) |         |  200.86 KiB (1%) |        2873 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 362.763 ms (5%) |         |  154.00 KiB (1%) |        2178 |
| `["findfirst", "n=500", "foldl"]`                   |  81.898 ms (5%) |         |                  |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 124.523 ms (5%) |         |  194.03 KiB (1%) |        2641 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 155.134 ms (5%) |         |  118.80 KiB (1%) |        1636 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 117.619 ms (5%) |         |   63.66 KiB (1%) |         865 |
| `["overhead", "default"]`                           |  77.101 μs (5%) |         |   32.70 KiB (1%) |         417 |
| `["overhead", "stoppable=false"]`                   |  78.501 μs (5%) |         |   32.78 KiB (1%) |         419 |
| `["overhead", "stoppable=true"]`                    |  92.001 μs (5%) |         |   44.22 KiB (1%) |         609 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   3.257 ms (5%) |         |  728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   3.927 ms (5%) |         |    1.79 MiB (1%) |         216 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   3.607 ms (5%) |         |    1.42 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  18.199 ms (5%) |         |    1.58 MiB (1%) |        2411 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  24.578 ms (5%) |         |    1.22 MiB (1%) |        6078 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  20.524 ms (5%) |         |    1.61 MiB (1%) |        3287 |
| `["parallel_histogram", "seq"]`                     |   5.794 ms (5%) |         |  364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  35.325 ms (5%) |         |                  |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  17.686 ms (5%) |         |   736 bytes (1%) |          11 |
| `["splitby", "count", "foldl"]`                     |   2.289 ms (5%) |         |                  |             |
| `["splitby", "count", "man"]`                       |   1.419 ms (5%) |         |                  |             |
| `["splitby", "count", "reduce"]`                    |   1.146 ms (5%) |         |    1.06 KiB (1%) |          18 |
| `["sum", "random", "foldl"]`                        |  16.271 ms (5%) |         |                  |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   8.383 ms (5%) |         |   74.11 KiB (1%) |        1102 |
| `["sum", "random", "reduce", "basesize=256"]`       |   8.214 ms (5%) |         |   36.70 KiB (1%) |         545 |
| `["sum", "random", "reduce", "basesize=512"]`       |   8.153 ms (5%) |         |   18.08 KiB (1%) |         269 |
| `["sum", "uniform", "foldl"]`                       |  15.676 ms (5%) |         |                  |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   8.105 ms (5%) |         |   74.17 KiB (1%) |        1104 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   7.526 ms (5%) |         |   36.70 KiB (1%) |         545 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   7.880 ms (5%) |         |   18.03 KiB (1%) |         268 |
| `["sum", "valley", "foldl"]`                        |  16.147 ms (5%) |         |                  |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   8.363 ms (5%) |         |   74.05 KiB (1%) |        1100 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   8.275 ms (5%) |         |   36.67 KiB (1%) |         544 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   8.015 ms (5%) |         |   18.00 KiB (1%) |         267 |
| `["words", "nthreads=1"]`                           |  30.865 ms (5%) |         |   31.79 MiB (1%) |     1036245 |
| `["words", "nthreads=2"]`                           |  17.325 ms (5%) |         |   32.51 MiB (1%) |     1036318 |
| `["words", "nthreads=4"]`                           |  16.991 ms (5%) |         |   32.95 MiB (1%) |     1036416 |

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
Julia Version 1.7.1
Commit ac5cc99908 (2021-12-22 19:35 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 20.04.3 LTS
  uname: Linux 5.11.0-1027-azure #30~20.04.1-Ubuntu SMP Wed Jan 12 20:56:50 UTC 2022 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2593 MHz       4760 s          1 s        287 s       2403 s          0 s
       #2  2593 MHz       5933 s          2 s        298 s       1236 s          0 s
       
  Memory: 6.788978576660156 GB (3464.4609375 MB free)
  Uptime: 752.45 sec
  Load Avg:  1.74  1.55  0.95
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, skylake-avx512)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 2 Feb 2022 - 1:26
* Package commit: 332ac4
* Julia commit: ac5cc9
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
| `["collect", "assoc", "basesize=1"]`                | 252.827 ms (5%) |         |   25.97 MiB (1%) |      306797 |
| `["collect", "assoc", "basesize=1024"]`             | 199.098 ms (5%) |         |    2.61 MiB (1%) |         456 |
| `["collect", "assoc", "basesize=32"]`               | 202.221 ms (5%) |         |    4.82 MiB (1%) |       11711 |
| `["collect", "seq"]`                                | 395.482 ms (5%) |         |  812.73 KiB (1%) |          11 |
| `["collect", "unordered", "basesize=1"]`            | 359.150 ms (5%) |         |   23.83 MiB (1%) |      410554 |
| `["collect", "unordered", "basesize=1024"]`         | 214.481 ms (5%) |         | 1001.64 KiB (1%) |         966 |
| `["collect", "unordered", "basesize=32"]`           | 226.015 ms (5%) |         |    1.58 MiB (1%) |       14731 |
| `["findfirst", "n=1000", "foldl"]`                  | 631.266 ms (5%) |         |                  |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 494.061 ms (5%) |         |  326.62 KiB (1%) |        4562 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 424.749 ms (5%) |         |  157.20 KiB (1%) |        2193 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 566.920 ms (5%) |         |  103.56 KiB (1%) |        1455 |
| `["findfirst", "n=400", "foldl"]`                   | 473.700 ms (5%) |         |                  |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 246.844 ms (5%) |         |  378.27 KiB (1%) |        5392 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 251.215 ms (5%) |         |  200.95 KiB (1%) |        2876 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 368.789 ms (5%) |         |  153.05 KiB (1%) |        2192 |
| `["findfirst", "n=500", "foldl"]`                   |  82.125 ms (5%) |         |                  |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |  87.297 ms (5%) |         |  159.44 KiB (1%) |        2157 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 120.454 ms (5%) |         |  103.38 KiB (1%) |        1410 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  83.871 ms (5%) |         |   49.59 KiB (1%) |         671 |
| `["overhead", "default"]`                           |  77.501 μs (5%) |         |   32.73 KiB (1%) |         418 |
| `["overhead", "stoppable=false"]`                   |  76.702 μs (5%) |         |   32.75 KiB (1%) |         418 |
| `["overhead", "stoppable=true"]`                    |  88.802 μs (5%) |         |   44.25 KiB (1%) |         610 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   3.277 ms (5%) |         |  728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   3.945 ms (5%) |         |    1.79 MiB (1%) |         215 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   3.619 ms (5%) |         |    1.42 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  18.192 ms (5%) |         |    1.59 MiB (1%) |        2712 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  24.645 ms (5%) |         |    1.23 MiB (1%) |        6528 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  21.472 ms (5%) |         |    1.65 MiB (1%) |        4723 |
| `["parallel_histogram", "seq"]`                     |   5.799 ms (5%) |         |  364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  35.263 ms (5%) |         |                  |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  17.656 ms (5%) |         |   736 bytes (1%) |          11 |
| `["splitby", "count", "foldl"]`                     |   2.249 ms (5%) |         |                  |             |
| `["splitby", "count", "man"]`                       |   1.419 ms (5%) |         |                  |             |
| `["splitby", "count", "reduce"]`                    |   1.185 ms (5%) |         |    1.06 KiB (1%) |          18 |
| `["sum", "random", "foldl"]`                        |  16.168 ms (5%) |         |                  |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   8.244 ms (5%) |         |   74.08 KiB (1%) |        1101 |
| `["sum", "random", "reduce", "basesize=256"]`       |   7.983 ms (5%) |         |   36.77 KiB (1%) |         547 |
| `["sum", "random", "reduce", "basesize=512"]`       |   8.066 ms (5%) |         |   18.05 KiB (1%) |         268 |
| `["sum", "uniform", "foldl"]`                       |  15.721 ms (5%) |         |                  |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   8.057 ms (5%) |         |   74.20 KiB (1%) |        1105 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   7.956 ms (5%) |         |   36.70 KiB (1%) |         545 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   7.864 ms (5%) |         |   18.03 KiB (1%) |         268 |
| `["sum", "valley", "foldl"]`                        |  16.107 ms (5%) |         |                  |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   8.324 ms (5%) |         |   74.14 KiB (1%) |        1103 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   8.266 ms (5%) |         |   36.73 KiB (1%) |         546 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   8.195 ms (5%) |         |   18.03 KiB (1%) |         268 |
| `["words", "nthreads=1"]`                           |  29.512 ms (5%) |         |   31.79 MiB (1%) |     1035843 |
| `["words", "nthreads=2"]`                           |  18.171 ms (5%) |         |   32.50 MiB (1%) |     1035947 |
| `["words", "nthreads=4"]`                           |  17.087 ms (5%) |         |   32.95 MiB (1%) |     1036027 |

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
Julia Version 1.7.1
Commit ac5cc99908 (2021-12-22 19:35 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 20.04.3 LTS
  uname: Linux 5.11.0-1027-azure #30~20.04.1-Ubuntu SMP Wed Jan 12 20:56:50 UTC 2022 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2593 MHz       7344 s          1 s        366 s       3128 s          0 s
       #2  2593 MHz       8377 s          2 s        383 s       2092 s          0 s
       
  Memory: 6.788978576660156 GB (3378.4765625 MB free)
  Uptime: 1091.75 sec
  Load Avg:  1.43  1.52  1.12
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

