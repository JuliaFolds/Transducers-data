# Multi-thread benchmark result

* Pull request commit: [`dfe5883a6c2a8cc91c9bdf0229dba4f6626d5d36`](https://github.com/JuliaFolds/Transducers.jl/commit/dfe5883a6c2a8cc91c9bdf0229dba4f6626d5d36)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/243> (Update */Manifest.toml)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 20 Nov 2026 - 06:51
    - Baseline: 20 Nov 2026 - 06:56
* Package commits:
    - Target: 6e80bc5
    - Baseline: 2a51f8d
* Julia commits:
    - Target: 742b9ab
    - Baseline: 742b9ab
* Julia command flags:
    - Target: None
    - Baseline: None
* Environment variables:
    - Target: `JULIA_NUM_THREADS => 2`
    - Baseline: `JULIA_NUM_THREADS => 2`

## Results
A ratio greater than `1.0` denotes a possible regression (marked with :x:), while a ratio less
than `1.0` denotes a possible improvement (marked with :white_check_mark:). Brackets display [tolerances](https://juliaci.github.io/BenchmarkTools.jl/stable/manual/#Benchmark-Parameters) for the benchmark estimates. Only significant results - results
that indicate possible regressions or improvements - are shown below (thus, an empty table means that all
benchmark results remained invariant between builds).

| ID                                                  | time ratio                   | memory ratio                 |
|-----------------------------------------------------|------------------------------|------------------------------|
| `["findfirst", "n=1000", "reduce", "basesize=128"]` |                1.06 (5%) :x: | 0.98 (1%) :white_check_mark: |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` |                1.11 (5%) :x: |                1.07 (1%) :x: |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` |                   0.99 (5%)  | 0.98 (1%) :white_check_mark: |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 0.92 (5%) :white_check_mark: |                   0.99 (1%)  |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 0.92 (5%) :white_check_mark: |                   1.01 (1%)  |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 0.38 (5%) :white_check_mark: | 0.49 (1%) :white_check_mark: |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 0.76 (5%) :white_check_mark: | 0.77 (1%) :white_check_mark: |
| `["overhead", "default"]`                           |                1.18 (5%) :x: |                   1.00 (1%)  |
| `["overhead", "stoppable=false"]`                   | 0.91 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["overhead", "stoppable=true"]`                    | 0.92 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["parallel_histogram", "comm", "basesize=16384"]`  |                1.12 (5%) :x: | 0.88 (1%) :white_check_mark: |
| `["parallel_histogram", "comm", "basesize=4096"]`   |                   1.00 (5%)  |                1.02 (1%) :x: |
| `["parallel_histogram", "comm", "basesize=8192"]`   | 0.86 (5%) :white_check_mark: | 0.70 (1%) :white_check_mark: |
| `["parallel_histogram", "seq"]`                     |                1.07 (5%) :x: |                   1.00 (1%)  |
| `["partition_length_maximum", "rand", "reduce"]`    |                1.14 (5%) :x: |                   1.00 (1%)  |
| `["words", "nthreads=4"]`                           |                1.06 (5%) :x: |                1.01 (1%) :x: |

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
Julia Version 1.7.3
Commit 742b9abb4d (2022-05-06 12:58 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 26.04.1 LTS
  uname: Linux 7.0.0-1019-azure #20-Ubuntu SMP PREEMPT Mon Oct 19 22:41:16 UTC 2026 x86_64 unknown
  CPU: Intel(R) Xeon(R) 6973P-C: 
              speed         user         nice          sys         idle          irq
       #1  4001 MHz       2014 s          0 s        119 s       6011 s          0 s
       #2  3995 MHz       2858 s          0 s        156 s       5156 s          0 s
       #3  3999 MHz       2574 s          0 s        138 s       5434 s          0 s
       #4  4000 MHz       2462 s          0 s        144 s       5598 s          0 s
       
  Memory: 15.607479095458984 GB (13182.5 MB free)
  Uptime: 825.7 sec
  Load Avg:  1.84  1.62  0.94
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, icelake-client)
```

### Baseline
```
Julia Version 1.7.3
Commit 742b9abb4d (2022-05-06 12:58 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 26.04.1 LTS
  uname: Linux 7.0.0-1019-azure #20-Ubuntu SMP PREEMPT Mon Oct 19 22:41:16 UTC 2026 x86_64 unknown
  CPU: Intel(R) Xeon(R) 6973P-C: 
              speed         user         nice          sys         idle          irq
       #1  3793 MHz       3177 s          0 s        172 s       7794 s          0 s
       #2  3785 MHz       4017 s          0 s        208 s       6945 s          0 s
       #3  3934 MHz       3488 s          0 s        181 s       7474 s          0 s
       #4  3804 MHz       3932 s          0 s        204 s       7067 s          0 s
       
  Memory: 15.607479095458984 GB (13165.14453125 MB free)
  Uptime: 1126.15 sec
  Load Avg:  1.92  1.76  1.2
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, icelake-client)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 20 Nov 2026 - 06:51
* Package commit: 6e80bc5
* Julia commit: 742b9ab
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
| `["collect", "assoc", "basesize=1"]`                | 114.078 ms (5%) |         |   4.36 MiB (1%) |       32800 |
| `["collect", "assoc", "basesize=1024"]`             | 114.305 ms (5%) |         |   1.09 MiB (1%) |          53 |
| `["collect", "assoc", "basesize=32"]`               | 113.501 ms (5%) |         |   1.48 MiB (1%) |        1052 |
| `["collect", "seq"]`                                | 226.066 ms (5%) |         | 256.05 KiB (1%) |           2 |
| `["collect", "unordered", "basesize=1"]`            | 200.782 ms (5%) |         |  23.80 MiB (1%) |      409733 |
| `["collect", "unordered", "basesize=1024"]`         | 123.628 ms (5%) |         |   1.02 MiB (1%) |        1373 |
| `["collect", "unordered", "basesize=32"]`           | 131.382 ms (5%) |         |   1.60 MiB (1%) |       15206 |
| `["findfirst", "n=1000", "foldl"]`                  | 348.397 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 205.688 ms (5%) |         | 232.75 KiB (1%) |        3273 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 263.297 ms (5%) |         | 163.89 KiB (1%) |        2287 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 240.568 ms (5%) |         |  79.78 KiB (1%) |        1125 |
| `["findfirst", "n=400", "foldl"]`                   | 261.264 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 139.274 ms (5%) |         | 383.12 KiB (1%) |        5454 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 139.396 ms (5%) |         | 199.64 KiB (1%) |        2866 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 154.061 ms (5%) |         | 128.05 KiB (1%) |        1804 |
| `["findfirst", "n=500", "foldl"]`                   |  45.110 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |  84.713 ms (5%) |         | 224.89 KiB (1%) |        3102 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |  37.319 ms (5%) |         |  66.06 KiB (1%) |         903 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  47.494 ms (5%) |         |  43.94 KiB (1%) |         593 |
| `["overhead", "default"]`                           |  58.157 μs (5%) |         |  32.64 KiB (1%) |         415 |
| `["overhead", "stoppable=false"]`                   |  51.306 μs (5%) |         |  32.72 KiB (1%) |         417 |
| `["overhead", "stoppable=true"]`                    |  60.102 μs (5%) |         |  44.25 KiB (1%) |         610 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   1.869 ms (5%) |         | 728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   2.341 ms (5%) |         |   1.79 MiB (1%) |         216 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   2.130 ms (5%) |         |   1.42 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |   9.231 ms (5%) |         |   1.33 MiB (1%) |        1055 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  22.804 ms (5%) |         |   1.40 MiB (1%) |       12062 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  16.805 ms (5%) |         |   1.26 MiB (1%) |        7453 |
| `["parallel_histogram", "seq"]`                     |   3.306 ms (5%) |         | 364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  29.723 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  14.713 ms (5%) |         |  736 bytes (1%) |          11 |
| `["splitby", "count", "foldl"]`                     |   1.410 ms (5%) |         |                 |             |
| `["splitby", "count", "man"]`                       | 875.086 μs (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    | 673.845 μs (5%) |         |   1.06 KiB (1%) |          18 |
| `["sum", "random", "foldl"]`                        |   8.079 ms (5%) |         |                 |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   4.137 ms (5%) |         |  74.16 KiB (1%) |        1103 |
| `["sum", "random", "reduce", "basesize=256"]`       |   4.131 ms (5%) |         |  36.78 KiB (1%) |         547 |
| `["sum", "random", "reduce", "basesize=512"]`       |   4.093 ms (5%) |         |  18.08 KiB (1%) |         269 |
| `["sum", "uniform", "foldl"]`                       |   7.932 ms (5%) |         |                 |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   4.143 ms (5%) |         |  74.16 KiB (1%) |        1103 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   4.065 ms (5%) |         |  36.78 KiB (1%) |         547 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   4.030 ms (5%) |         |  18.02 KiB (1%) |         267 |
| `["sum", "valley", "foldl"]`                        |   8.144 ms (5%) |         |                 |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   4.244 ms (5%) |         |  74.03 KiB (1%) |        1099 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   4.179 ms (5%) |         |  36.78 KiB (1%) |         547 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   4.150 ms (5%) |         |  18.05 KiB (1%) |         268 |
| `["words", "nthreads=1"]`                           |  13.579 ms (5%) |         |  31.85 MiB (1%) |     1037179 |
| `["words", "nthreads=2"]`                           |   8.887 ms (5%) |         |  32.56 MiB (1%) |     1037302 |
| `["words", "nthreads=4"]`                           |   9.613 ms (5%) |         |  33.19 MiB (1%) |     1037457 |

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
Julia Version 1.7.3
Commit 742b9abb4d (2022-05-06 12:58 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 26.04.1 LTS
  uname: Linux 7.0.0-1019-azure #20-Ubuntu SMP PREEMPT Mon Oct 19 22:41:16 UTC 2026 x86_64 unknown
  CPU: Intel(R) Xeon(R) 6973P-C: 
              speed         user         nice          sys         idle          irq
       #1  4001 MHz       2014 s          0 s        119 s       6011 s          0 s
       #2  3995 MHz       2858 s          0 s        156 s       5156 s          0 s
       #3  3999 MHz       2574 s          0 s        138 s       5434 s          0 s
       #4  4000 MHz       2462 s          0 s        144 s       5598 s          0 s
       
  Memory: 15.607479095458984 GB (13182.5 MB free)
  Uptime: 825.7 sec
  Load Avg:  1.84  1.62  0.94
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, icelake-client)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 20 Nov 2026 - 06:56
* Package commit: 2a51f8d
* Julia commit: 742b9ab
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
| `["collect", "assoc", "basesize=1"]`                | 113.730 ms (5%) |         |   4.36 MiB (1%) |       32800 |
| `["collect", "assoc", "basesize=1024"]`             | 113.039 ms (5%) |         |   1.09 MiB (1%) |          53 |
| `["collect", "assoc", "basesize=32"]`               | 112.864 ms (5%) |         |   1.48 MiB (1%) |        1052 |
| `["collect", "seq"]`                                | 227.380 ms (5%) |         | 256.05 KiB (1%) |           2 |
| `["collect", "unordered", "basesize=1"]`            | 206.735 ms (5%) |         |  23.80 MiB (1%) |      409824 |
| `["collect", "unordered", "basesize=1024"]`         | 125.114 ms (5%) |         |   1.01 MiB (1%) |        1226 |
| `["collect", "unordered", "basesize=32"]`           | 131.896 ms (5%) |         |   1.60 MiB (1%) |       15150 |
| `["findfirst", "n=1000", "foldl"]`                  | 348.572 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 194.826 ms (5%) |         | 236.98 KiB (1%) |        3331 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 237.323 ms (5%) |         | 153.69 KiB (1%) |        2164 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 242.363 ms (5%) |         |  81.33 KiB (1%) |        1146 |
| `["findfirst", "n=400", "foldl"]`                   | 261.533 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 137.065 ms (5%) |         | 380.77 KiB (1%) |        5425 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 137.380 ms (5%) |         | 200.89 KiB (1%) |        2874 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 167.135 ms (5%) |         | 128.97 KiB (1%) |        1843 |
| `["findfirst", "n=500", "foldl"]`                   |  44.904 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |  91.738 ms (5%) |         | 222.81 KiB (1%) |        3093 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |  97.532 ms (5%) |         | 134.16 KiB (1%) |        1841 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  62.636 ms (5%) |         |  56.84 KiB (1%) |         779 |
| `["overhead", "default"]`                           |  49.298 μs (5%) |         |  32.73 KiB (1%) |         418 |
| `["overhead", "stoppable=false"]`                   |  56.175 μs (5%) |         |  32.75 KiB (1%) |         418 |
| `["overhead", "stoppable=true"]`                    |  65.328 μs (5%) |         |  44.28 KiB (1%) |         611 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   1.784 ms (5%) |         | 728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   2.274 ms (5%) |         |   1.79 MiB (1%) |         216 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   2.039 ms (5%) |         |   1.42 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |   8.249 ms (5%) |         |   1.51 MiB (1%) |         243 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  22.830 ms (5%) |         |   1.37 MiB (1%) |       11032 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  19.536 ms (5%) |         |   1.79 MiB (1%) |        9300 |
| `["parallel_histogram", "seq"]`                     |   3.076 ms (5%) |         | 364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  29.723 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  12.884 ms (5%) |         |  736 bytes (1%) |          11 |
| `["splitby", "count", "foldl"]`                     |   1.438 ms (5%) |         |                 |             |
| `["splitby", "count", "man"]`                       | 895.359 μs (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    | 700.345 μs (5%) |         |   1.06 KiB (1%) |          18 |
| `["sum", "random", "foldl"]`                        |   8.136 ms (5%) |         |                 |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   4.262 ms (5%) |         |  74.12 KiB (1%) |        1102 |
| `["sum", "random", "reduce", "basesize=256"]`       |   4.180 ms (5%) |         |  36.78 KiB (1%) |         547 |
| `["sum", "random", "reduce", "basesize=512"]`       |   4.141 ms (5%) |         |  18.02 KiB (1%) |         267 |
| `["sum", "uniform", "foldl"]`                       |   7.956 ms (5%) |         |                 |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   4.144 ms (5%) |         |  74.09 KiB (1%) |        1101 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   4.069 ms (5%) |         |  36.78 KiB (1%) |         547 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   4.040 ms (5%) |         |  18.02 KiB (1%) |         267 |
| `["sum", "valley", "foldl"]`                        |   8.038 ms (5%) |         |                 |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   4.190 ms (5%) |         |  74.16 KiB (1%) |        1103 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   4.186 ms (5%) |         |  36.66 KiB (1%) |         543 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   4.142 ms (5%) |         |  18.11 KiB (1%) |         270 |
| `["words", "nthreads=1"]`                           |  13.250 ms (5%) |         |  31.68 MiB (1%) |     1031923 |
| `["words", "nthreads=2"]`                           |   8.551 ms (5%) |         |  32.40 MiB (1%) |     1032001 |
| `["words", "nthreads=4"]`                           |   9.036 ms (5%) |         |  32.84 MiB (1%) |     1032112 |

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
Julia Version 1.7.3
Commit 742b9abb4d (2022-05-06 12:58 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 26.04.1 LTS
  uname: Linux 7.0.0-1019-azure #20-Ubuntu SMP PREEMPT Mon Oct 19 22:41:16 UTC 2026 x86_64 unknown
  CPU: Intel(R) Xeon(R) 6973P-C: 
              speed         user         nice          sys         idle          irq
       #1  3793 MHz       3177 s          0 s        172 s       7794 s          0 s
       #2  3785 MHz       4017 s          0 s        208 s       6945 s          0 s
       #3  3934 MHz       3488 s          0 s        181 s       7474 s          0 s
       #4  3804 MHz       3932 s          0 s        204 s       7067 s          0 s
       
  Memory: 15.607479095458984 GB (13165.14453125 MB free)
  Uptime: 1126.15 sec
  Load Avg:  1.92  1.76  1.2
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, icelake-client)
```

---
# Runtime information
| Runtime Info | |
|:--|:--|
| BLAS #threads | 4 |
| `BLAS.vendor()` | `openblas64` |
| `Sys.CPU_THREADS` | 4 |

`lscpu` output:

    Architecture:                            x86_64
    CPU op-mode(s):                          32-bit, 64-bit
    Address sizes:                           48 bits physical, 57 bits virtual
    Byte Order:                              Little Endian
    CPU(s):                                  4
    On-line CPU(s) list:                     0-3
    Vendor ID:                               GenuineIntel
    Model name:                              Intel(R) Xeon(R) 6973P-C
    CPU family:                              6
    Model:                                   173
    Thread(s) per core:                      2
    Core(s) per socket:                      2
    Socket(s):                               1
    Stepping:                                1
    CPU(s) scaling MHz:                      146%
    CPU max MHz:                             2600.0000
    CPU min MHz:                             800.0000
    BogoMIPS:                                5200.00
    Flags:                                   fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush mmx fxsr sse sse2 ss ht syscall nx pdpe1gb rdtscp lm constant_tsc rep_good nopl xtopology tsc_reliable nonstop_tsc cpuid aperfmperf tsc_known_freq pni pclmulqdq vmx ssse3 fma cx16 pcid sse4_1 sse4_2 x2apic movbe popcnt tsc_deadline_timer aes xsave avx f16c rdrand hypervisor lahf_lm abm 3dnowprefetch tpr_shadow ept vpid ept_ad fsgsbase tsc_adjust bmi1 hle avx2 smep bmi2 erms invpcid rtm avx512f avx512dq rdseed adx smap avx512ifma clflushopt clwb avx512cd sha_ni avx512bw avx512vl xsaveopt xsavec xgetbv1 xsaves user_shstk avx_vnni avx512_bf16 vnmi avx512vbmi umip waitpkg avx512_vbmi2 gfni vaes vpclmulqdq avx512_vnni avx512_bitalg avx512_vpopcntdq la57 rdpid cldemote movdiri movdir64b fsrm serialize tsxldtrk ibt amx_bf16 avx512_fp16 amx_tile amx_int8 arch_capabilities
    Virtualization:                          VT-x
    Hypervisor vendor:                       Microsoft
    Virtualization type:                     full
    L1d cache:                               96 KiB (2 instances)
    L1i cache:                               128 KiB (2 instances)
    L2 cache:                                4 MiB (2 instances)
    L3 cache:                                480 MiB (1 instance)
    NUMA node(s):                            1
    NUMA node0 CPU(s):                       0-3
    Vulnerability Gather data sampling:      Not affected
    Vulnerability Ghostwrite:                Not affected
    Vulnerability Indirect target selection: Mitigation; Aligned branch/return thunks
    Vulnerability Itlb multihit:             Not affected
    Vulnerability L1tf:                      Not affected
    Vulnerability Mds:                       Not affected
    Vulnerability Meltdown:                  Not affected
    Vulnerability Mmio stale data:           Not affected
    Vulnerability Old microcode:             Not affected
    Vulnerability Reg file data sampling:    Not affected
    Vulnerability Retbleed:                  Vulnerable
    Vulnerability Spec rstack overflow:      Not affected
    Vulnerability Spec store bypass:         Vulnerable
    Vulnerability Spectre v1:                Mitigation; usercopy/swapgs barriers and __user pointer sanitization
    Vulnerability Spectre v2:                Mitigation; Retpolines; STIBP disabled; RSB filling; PBRSB-eIBRS Not affected; BHI Retpoline
    Vulnerability Srbds:                     Not affected
    Vulnerability Tsa:                       Not affected
    Vulnerability Tsx async abort:           Not affected
    Vulnerability Vmscape:                   Not affected
    

| Cpu Property       | Value                                                      |
|:------------------ |:---------------------------------------------------------- |
| Brand              | Intel(R) Xeon(R) 6973P-C                                   |
| Vendor             | :Intel                                                     |
| Architecture       | :UnknownIntel                                              |
| Model              | Family: 0x06, Model: 0xad, Stepping: 0x01, Type: 0x00      |
| Cores              | 2 physical cores, 4 logical cores (on executing CPU)       |
|                    | Hyperthreading hardware capability detected                |
| Clock Frequencies  | Not supported by CPU                                       |
| Data Cache         | Level 1:3 : (48, 2048, 491520) kbytes                      |
|                    | 64 byte cache line size                                    |
| Address Size       | 57 bits virtual, 48 bits physical                          |
| SIMD               | 512 bit = 64 byte max. SIMD vector size                    |
| Time Stamp Counter | TSC is accessible via `rdtsc`                              |
|                    | TSC runs at constant rate (invariant from clock frequency) |
| Perf. Monitoring   | Performance Monitoring Counters (PMC) are not supported    |
| Hypervisor         | Yes, Microsoft                                             |

