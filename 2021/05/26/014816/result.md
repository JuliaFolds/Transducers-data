# Multi-thread benchmark result

* Pull request commit: [`592fdffd4fc80f54176f46fcb4ae435e9dd39065`](https://github.com/JuliaFolds/Transducers.jl/commit/592fdffd4fc80f54176f46fcb4ae435e9dd39065)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/243> (Update */Manifest.toml)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 26 May 2021 - 01:42
    - Baseline: 26 May 2021 - 01:47
* Package commits:
    - Target: 9fdd47
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
| `["collect", "unordered", "basesize=1024"]`         | 0.81 (5%) :white_check_mark: | 0.91 (1%) :white_check_mark: |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` |                   0.96 (5%)  | 0.93 (1%) :white_check_mark: |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 0.90 (5%) :white_check_mark: | 0.93 (1%) :white_check_mark: |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  |                1.06 (5%) :x: |                   1.00 (1%)  |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  |                   1.04 (5%)  |                1.01 (1%) :x: |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  |                   1.03 (5%)  |                1.09 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |                1.12 (5%) :x: |                1.11 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |                1.25 (5%) :x: |                1.13 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 0.46 (5%) :white_check_mark: | 0.57 (1%) :white_check_mark: |
| `["parallel_histogram", "comm", "basesize=4096"]`   | 0.93 (5%) :white_check_mark: | 0.97 (1%) :white_check_mark: |
| `["parallel_histogram", "comm", "basesize=8192"]`   | 0.80 (5%) :white_check_mark: |                   1.01 (1%)  |
| `["splitby", "count", "man"]`                       | 0.88 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["splitby", "count", "reduce"]`                    |                   0.98 (5%)  | 0.99 (1%) :white_check_mark: |

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
  uname: Linux 5.4.0-1047-azure #49-Ubuntu SMP Thu Apr 22 14:30:37 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2593 MHz      53142 s         15 s       2386 s      27730 s          0 s
       #2  2593 MHz      53530 s          3 s       2309 s      27508 s          0 s
       
  Memory: 6.791339874267578 GB (3549.31640625 MB free)
  Uptime: 839.0 sec
  Load Avg:  1.68896484375  1.50048828125  0.91650390625
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
  uname: Linux 5.4.0-1047-azure #49-Ubuntu SMP Thu Apr 22 14:30:37 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2593 MHz      74954 s         15 s       2985 s      37781 s          0 s
       #2  2593 MHz      80600 s          3 s       3000 s      32247 s          0 s
       
  Memory: 6.791339874267578 GB (3527.47265625 MB free)
  Uptime: 1165.0 sec
  Load Avg:  1.64306640625  1.53515625  1.10009765625
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, skylake-avx512)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 26 May 2021 - 1:42
* Package commit: 9fdd47
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
| `["collect", "assoc", "basesize=1"]`                | 236.953 ms (5%) |         |  32.66 MiB (1%) |      286736 |
| `["collect", "assoc", "basesize=1024"]`             | 198.134 ms (5%) |         |   1.79 MiB (1%) |         570 |
| `["collect", "assoc", "basesize=32"]`               | 199.934 ms (5%) |         |   3.97 MiB (1%) |       13305 |
| `["collect", "seq"]`                                | 394.890 ms (5%) |         | 512.72 KiB (1%) |          15 |
| `["collect", "unordered", "basesize=1"]`            | 415.581 ms (5%) |         |  30.01 MiB (1%) |      360567 |
| `["collect", "unordered", "basesize=1024"]`         | 228.747 ms (5%) |         | 803.05 KiB (1%) |        2437 |
| `["collect", "unordered", "basesize=32"]`           | 222.221 ms (5%) |         |   1.47 MiB (1%) |       12596 |
| `["findfirst", "n=1000", "foldl"]`                  | 626.994 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 619.242 ms (5%) |         |   1.16 MiB (1%) |       20775 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 442.253 ms (5%) |         | 485.00 KiB (1%) |        8497 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 572.299 ms (5%) |         | 328.98 KiB (1%) |        5774 |
| `["findfirst", "n=400", "foldl"]`                   | 470.696 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 267.960 ms (5%) |         |   1.17 MiB (1%) |       21090 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 257.104 ms (5%) |         | 597.77 KiB (1%) |       10540 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 279.013 ms (5%) |         | 370.98 KiB (1%) |        6537 |
| `["findfirst", "n=500", "foldl"]`                   |  81.599 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 165.897 ms (5%) |         | 772.77 KiB (1%) |       13451 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 166.709 ms (5%) |         | 412.73 KiB (1%) |        7202 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 106.357 ms (5%) |         | 167.63 KiB (1%) |        2940 |
| `["overhead", "default"]`                           |  57.600 μs (5%) |         |  47.36 KiB (1%) |         382 |
| `["overhead", "stoppable=false"]`                   |  59.901 μs (5%) |         |  47.39 KiB (1%) |         382 |
| `["overhead", "stoppable=true"]`                    | 153.003 μs (5%) |         | 139.67 KiB (1%) |        2464 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   3.968 ms (5%) |         | 730.06 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   4.580 ms (5%) |         |   1.79 MiB (1%) |         213 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   4.277 ms (5%) |         |   1.43 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  13.951 ms (5%) |         |   1.24 MiB (1%) |         801 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  21.658 ms (5%) |         |   1.04 MiB (1%) |        2390 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  16.935 ms (5%) |         |   1.26 MiB (1%) |        1564 |
| `["parallel_histogram", "seq"]`                     |   7.254 ms (5%) |         | 364.61 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  33.725 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  16.877 ms (5%) |         |   2.66 KiB (1%) |          48 |
| `["splitby", "count", "foldl"]`                     |   4.699 ms (5%) |         |   96 bytes (1%) |           4 |
| `["splitby", "count", "man"]`                       |   1.693 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    |   1.172 ms (5%) |         |   2.81 KiB (1%) |          54 |
| `["sum", "random", "foldl"]`                        |  15.875 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "random", "reduce", "basesize=128"]`       |   8.133 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "random", "reduce", "basesize=256"]`       |   8.057 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "random", "reduce", "basesize=512"]`       |   8.001 ms (5%) |         |  25.30 KiB (1%) |         252 |
| `["sum", "uniform", "foldl"]`                       |  15.534 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   7.931 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   7.841 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   7.801 ms (5%) |         |  25.25 KiB (1%) |         251 |
| `["sum", "valley", "foldl"]`                        |  15.969 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "valley", "reduce", "basesize=128"]`       |   8.201 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   8.124 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   8.062 ms (5%) |         |  25.25 KiB (1%) |         251 |
| `["words", "nthreads=1"]`                           |  21.774 ms (5%) |         |  31.63 MiB (1%) |     1030457 |
| `["words", "nthreads=2"]`                           |  14.062 ms (5%) |         |  32.35 MiB (1%) |     1030576 |
| `["words", "nthreads=4"]`                           |  14.404 ms (5%) |         |  32.98 MiB (1%) |     1030733 |

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
  uname: Linux 5.4.0-1047-azure #49-Ubuntu SMP Thu Apr 22 14:30:37 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2593 MHz      53142 s         15 s       2386 s      27730 s          0 s
       #2  2593 MHz      53530 s          3 s       2309 s      27508 s          0 s
       
  Memory: 6.791339874267578 GB (3549.31640625 MB free)
  Uptime: 839.0 sec
  Load Avg:  1.68896484375  1.50048828125  0.91650390625
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, skylake-avx512)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 26 May 2021 - 1:47
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
| `["collect", "assoc", "basesize=1"]`                | 236.680 ms (5%) |         |  32.66 MiB (1%) |      286739 |
| `["collect", "assoc", "basesize=1024"]`             | 198.481 ms (5%) |         |   1.79 MiB (1%) |         570 |
| `["collect", "assoc", "basesize=32"]`               | 199.824 ms (5%) |         |   3.97 MiB (1%) |       13306 |
| `["collect", "seq"]`                                | 395.055 ms (5%) |         | 512.72 KiB (1%) |          15 |
| `["collect", "unordered", "basesize=1"]`            | 422.803 ms (5%) |         |  30.01 MiB (1%) |      360567 |
| `["collect", "unordered", "basesize=1024"]`         | 281.187 ms (5%) |         | 879.98 KiB (1%) |        4881 |
| `["collect", "unordered", "basesize=32"]`           | 223.122 ms (5%) |         |   1.48 MiB (1%) |       12741 |
| `["findfirst", "n=1000", "foldl"]`                  | 624.156 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 645.448 ms (5%) |         |   1.24 MiB (1%) |       22297 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 440.961 ms (5%) |         | 485.00 KiB (1%) |        8497 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 636.934 ms (5%) |         | 352.30 KiB (1%) |        6188 |
| `["findfirst", "n=400", "foldl"]`                   | 468.387 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 253.200 ms (5%) |         |   1.17 MiB (1%) |       20968 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 248.290 ms (5%) |         | 590.69 KiB (1%) |       10414 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 270.193 ms (5%) |         | 341.34 KiB (1%) |        6024 |
| `["findfirst", "n=500", "foldl"]`                   |  81.190 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 147.803 ms (5%) |         | 696.22 KiB (1%) |       12123 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 133.620 ms (5%) |         | 363.75 KiB (1%) |        6336 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 230.128 ms (5%) |         | 296.34 KiB (1%) |        5187 |
| `["overhead", "default"]`                           |  59.901 μs (5%) |         |  47.36 KiB (1%) |         382 |
| `["overhead", "stoppable=false"]`                   |  59.401 μs (5%) |         |  47.39 KiB (1%) |         382 |
| `["overhead", "stoppable=true"]`                    | 153.202 μs (5%) |         | 139.67 KiB (1%) |        2464 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   4.006 ms (5%) |         | 730.06 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   4.625 ms (5%) |         |   1.79 MiB (1%) |         213 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   4.327 ms (5%) |         |   1.43 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  13.608 ms (5%) |         |   1.23 MiB (1%) |         595 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  23.311 ms (5%) |         |   1.07 MiB (1%) |        3256 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  21.229 ms (5%) |         |   1.26 MiB (1%) |        1327 |
| `["parallel_histogram", "seq"]`                     |   7.285 ms (5%) |         | 364.61 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  33.724 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  16.874 ms (5%) |         |   2.66 KiB (1%) |          48 |
| `["splitby", "count", "foldl"]`                     |   4.799 ms (5%) |         |   96 bytes (1%) |           4 |
| `["splitby", "count", "man"]`                       |   1.930 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    |   1.200 ms (5%) |         |   2.84 KiB (1%) |          54 |
| `["sum", "random", "foldl"]`                        |  15.875 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "random", "reduce", "basesize=128"]`       |   8.064 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "random", "reduce", "basesize=256"]`       |   8.013 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "random", "reduce", "basesize=512"]`       |   7.988 ms (5%) |         |  25.30 KiB (1%) |         252 |
| `["sum", "uniform", "foldl"]`                       |  15.357 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   7.903 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   7.798 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   7.742 ms (5%) |         |  25.25 KiB (1%) |         251 |
| `["sum", "valley", "foldl"]`                        |  15.961 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "valley", "reduce", "basesize=128"]`       |   8.173 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   8.093 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   8.039 ms (5%) |         |  25.25 KiB (1%) |         251 |
| `["words", "nthreads=1"]`                           |  21.568 ms (5%) |         |  31.89 MiB (1%) |     1039027 |
| `["words", "nthreads=2"]`                           |  14.458 ms (5%) |         |  32.61 MiB (1%) |     1039119 |
| `["words", "nthreads=4"]`                           |  14.514 ms (5%) |         |  33.06 MiB (1%) |     1039202 |

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
  uname: Linux 5.4.0-1047-azure #49-Ubuntu SMP Thu Apr 22 14:30:37 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2593 MHz      74954 s         15 s       2985 s      37781 s          0 s
       #2  2593 MHz      80600 s          3 s       3000 s      32247 s          0 s
       
  Memory: 6.791339874267578 GB (3527.47265625 MB free)
  Uptime: 1165.0 sec
  Load Avg:  1.64306640625  1.53515625  1.10009765625
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
    CPU MHz:                         2593.907
    BogoMIPS:                        5187.81
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

