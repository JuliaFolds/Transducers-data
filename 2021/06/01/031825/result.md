# Multi-thread benchmark result

* Pull request commit: [`523e3564d88b1c0ab44e81609594eb794afaa76c`](https://github.com/JuliaFolds/Transducers.jl/commit/523e3564d88b1c0ab44e81609594eb794afaa76c)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/243> (Update */Manifest.toml)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 1 Jun 2021 - 03:12
    - Baseline: 1 Jun 2021 - 03:17
* Package commits:
    - Target: 55a0b4
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
| `["collect", "seq"]`                                | 0.95 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["collect", "unordered", "basesize=1024"]`         | 0.89 (5%) :white_check_mark: | 0.91 (1%) :white_check_mark: |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 0.63 (5%) :white_check_mark: | 0.70 (1%) :white_check_mark: |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` |                   0.99 (5%)  | 0.97 (1%) :white_check_mark: |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  |                1.12 (5%) :x: |                1.12 (1%) :x: |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  |                   0.99 (5%)  |                1.01 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |                1.38 (5%) :x: |                1.28 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 0.81 (5%) :white_check_mark: | 0.88 (1%) :white_check_mark: |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |                1.60 (5%) :x: |                1.40 (1%) :x: |
| `["splitby", "count", "man"]`                       | 0.84 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["sum", "random", "reduce", "basesize=128"]`       | 0.95 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["sum", "random", "reduce", "basesize=512"]`       |                1.10 (5%) :x: |                   1.00 (1%)  |
| `["sum", "valley", "foldl"]`                        |                1.09 (5%) :x: |                   1.00 (1%)  |
| `["sum", "valley", "reduce", "basesize=512"]`       |                1.07 (5%) :x: |                   1.00 (1%)  |
| `["words", "nthreads=4"]`                           |                1.09 (5%) :x: |                   1.00 (1%)  |

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
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz      53825 s         19 s       2456 s      64958 s          0 s
       #2  2095 MHz      56754 s         10 s       2610 s      62064 s          0 s
       
  Memory: 6.791339874267578 GB (3621.80859375 MB free)
  Uptime: 1221.0 sec
  Load Avg:  1.65966796875  1.49169921875  0.92041015625
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
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz      83168 s         19 s       3102 s      68918 s          0 s
       #2  2095 MHz      78140 s         10 s       3254 s      73934 s          0 s
       
  Memory: 6.791339874267578 GB (3586.515625 MB free)
  Uptime: 1561.0 sec
  Load Avg:  1.5703125  1.49169921875  1.0947265625
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, skylake-avx512)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 1 Jun 2021 - 3:12
* Package commit: 55a0b4
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
| `["collect", "assoc", "basesize=1"]`                | 273.076 ms (5%) |         |  32.66 MiB (1%) |      286740 |
| `["collect", "assoc", "basesize=1024"]`             | 232.812 ms (5%) |         |   1.79 MiB (1%) |         569 |
| `["collect", "assoc", "basesize=32"]`               | 229.575 ms (5%) |         |   3.97 MiB (1%) |       13306 |
| `["collect", "seq"]`                                | 433.171 ms (5%) |         | 512.72 KiB (1%) |          15 |
| `["collect", "unordered", "basesize=1"]`            | 480.839 ms (5%) |         |  30.01 MiB (1%) |      360612 |
| `["collect", "unordered", "basesize=1024"]`         | 354.519 ms (5%) |         | 963.77 KiB (1%) |        7580 |
| `["collect", "unordered", "basesize=32"]`           | 261.461 ms (5%) |         |   1.48 MiB (1%) |       12666 |
| `["findfirst", "n=1000", "foldl"]`                  | 702.093 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 512.370 ms (5%) |         | 924.64 KiB (1%) |       16158 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 506.258 ms (5%) |         | 482.66 KiB (1%) |        8455 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 728.099 ms (5%) |         | 352.30 KiB (1%) |        6188 |
| `["findfirst", "n=400", "foldl"]`                   | 531.121 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 326.830 ms (5%) |         |   1.21 MiB (1%) |       21864 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 294.933 ms (5%) |         | 595.58 KiB (1%) |       10507 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 327.102 ms (5%) |         | 375.63 KiB (1%) |        6616 |
| `["findfirst", "n=500", "foldl"]`                   |  86.792 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 239.235 ms (5%) |         | 864.33 KiB (1%) |       15083 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 137.078 ms (5%) |         | 342.64 KiB (1%) |        5958 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 244.767 ms (5%) |         | 295.94 KiB (1%) |        5161 |
| `["overhead", "default"]`                           |  59.604 μs (5%) |         |  47.33 KiB (1%) |         381 |
| `["overhead", "stoppable=false"]`                   |  62.404 μs (5%) |         |  47.36 KiB (1%) |         381 |
| `["overhead", "stoppable=true"]`                    | 154.209 μs (5%) |         | 139.67 KiB (1%) |        2464 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   4.152 ms (5%) |         | 730.06 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   5.098 ms (5%) |         |   1.79 MiB (1%) |         213 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   4.498 ms (5%) |         |   1.43 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  16.196 ms (5%) |         |   1.23 MiB (1%) |         583 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  26.378 ms (5%) |         |   1.04 MiB (1%) |        2218 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  23.132 ms (5%) |         |   1.27 MiB (1%) |        1855 |
| `["parallel_histogram", "seq"]`                     |   7.264 ms (5%) |         | 364.61 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  38.450 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  19.038 ms (5%) |         |   2.66 KiB (1%) |          48 |
| `["splitby", "count", "foldl"]`                     |   4.623 ms (5%) |         |   96 bytes (1%) |           4 |
| `["splitby", "count", "man"]`                       |   1.430 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    |   1.140 ms (5%) |         |   2.84 KiB (1%) |          54 |
| `["sum", "random", "foldl"]`                        |  16.079 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "random", "reduce", "basesize=128"]`       |   8.441 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "random", "reduce", "basesize=256"]`       |   8.495 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "random", "reduce", "basesize=512"]`       |   9.044 ms (5%) |         |  25.30 KiB (1%) |         252 |
| `["sum", "uniform", "foldl"]`                       |  16.243 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   8.346 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   8.123 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   8.172 ms (5%) |         |  25.25 KiB (1%) |         251 |
| `["sum", "valley", "foldl"]`                        |  17.960 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "valley", "reduce", "basesize=128"]`       |   8.950 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   8.838 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   9.234 ms (5%) |         |  25.25 KiB (1%) |         251 |
| `["words", "nthreads=1"]`                           |  23.421 ms (5%) |         |  31.80 MiB (1%) |     1036232 |
| `["words", "nthreads=2"]`                           |  15.323 ms (5%) |         |  32.16 MiB (1%) |     1036277 |
| `["words", "nthreads=4"]`                           |  16.071 ms (5%) |         |  32.88 MiB (1%) |     1036349 |

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
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz      53825 s         19 s       2456 s      64958 s          0 s
       #2  2095 MHz      56754 s         10 s       2610 s      62064 s          0 s
       
  Memory: 6.791339874267578 GB (3621.80859375 MB free)
  Uptime: 1221.0 sec
  Load Avg:  1.65966796875  1.49169921875  0.92041015625
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, skylake-avx512)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 1 Jun 2021 - 3:17
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

| ID                                                  | time            | GC time  | memory          | allocations |
|-----------------------------------------------------|----------------:|---------:|----------------:|------------:|
| `["collect", "assoc", "basesize=1"]`                | 275.569 ms (5%) |          |  32.66 MiB (1%) |      286738 |
| `["collect", "assoc", "basesize=1024"]`             | 228.113 ms (5%) |          |   1.79 MiB (1%) |         570 |
| `["collect", "assoc", "basesize=32"]`               | 231.684 ms (5%) |          |   3.97 MiB (1%) |       13307 |
| `["collect", "seq"]`                                | 456.795 ms (5%) |          | 512.72 KiB (1%) |          15 |
| `["collect", "unordered", "basesize=1"]`            | 490.802 ms (5%) |          |  30.01 MiB (1%) |      360592 |
| `["collect", "unordered", "basesize=1024"]`         | 400.041 ms (5%) |          |   1.03 MiB (1%) |       10538 |
| `["collect", "unordered", "basesize=32"]`           | 260.587 ms (5%) |          |   1.47 MiB (1%) |       12568 |
| `["findfirst", "n=1000", "foldl"]`                  | 727.159 ms (5%) |          |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 815.485 ms (5%) |          |   1.30 MiB (1%) |       23265 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 525.526 ms (5%) |          | 485.00 KiB (1%) |        8497 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 738.279 ms (5%) |          | 361.52 KiB (1%) |        6353 |
| `["findfirst", "n=400", "foldl"]`                   | 538.306 ms (5%) |          |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 291.940 ms (5%) |          |   1.09 MiB (1%) |       19589 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 294.756 ms (5%) |          | 590.69 KiB (1%) |       10414 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 331.774 ms (5%) |          | 370.95 KiB (1%) |        6535 |
| `["findfirst", "n=500", "foldl"]`                   |  90.647 ms (5%) |          |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 173.684 ms (5%) |          | 673.83 KiB (1%) |       11754 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 168.747 ms (5%) |          | 389.19 KiB (1%) |        6781 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 153.149 ms (5%) |          | 210.83 KiB (1%) |        3669 |
| `["overhead", "default"]`                           |  60.603 μs (5%) |          |  47.33 KiB (1%) |         381 |
| `["overhead", "stoppable=false"]`                   |  62.803 μs (5%) |          |  47.36 KiB (1%) |         381 |
| `["overhead", "stoppable=true"]`                    | 155.708 μs (5%) |          | 139.64 KiB (1%) |        2463 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   4.109 ms (5%) |          | 730.06 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   4.922 ms (5%) |          |   1.79 MiB (1%) |         213 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   4.403 ms (5%) |          |   1.43 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  16.359 ms (5%) |          |   1.23 MiB (1%) |         613 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  26.357 ms (5%) |          |   1.05 MiB (1%) |        2340 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  22.571 ms (5%) | 2.399 ms |   1.26 MiB (1%) |        1501 |
| `["parallel_histogram", "seq"]`                     |   7.330 ms (5%) |          | 364.61 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  36.890 ms (5%) |          |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  18.968 ms (5%) |          |   2.66 KiB (1%) |          48 |
| `["splitby", "count", "foldl"]`                     |   4.658 ms (5%) |          |   96 bytes (1%) |           4 |
| `["splitby", "count", "man"]`                       |   1.694 ms (5%) |          |                 |             |
| `["splitby", "count", "reduce"]`                    |   1.159 ms (5%) |          |   2.84 KiB (1%) |          54 |
| `["sum", "random", "foldl"]`                        |  16.211 ms (5%) |          |   32 bytes (1%) |           2 |
| `["sum", "random", "reduce", "basesize=128"]`       |   8.902 ms (5%) |          | 103.23 KiB (1%) |        1018 |
| `["sum", "random", "reduce", "basesize=256"]`       |   8.605 ms (5%) |          |  51.23 KiB (1%) |         506 |
| `["sum", "random", "reduce", "basesize=512"]`       |   8.226 ms (5%) |          |  25.30 KiB (1%) |         252 |
| `["sum", "uniform", "foldl"]`                       |  15.605 ms (5%) |          |   32 bytes (1%) |           2 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   8.061 ms (5%) |          | 103.23 KiB (1%) |        1018 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   8.030 ms (5%) |          |  51.23 KiB (1%) |         506 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   8.156 ms (5%) |          |  25.25 KiB (1%) |         251 |
| `["sum", "valley", "foldl"]`                        |  16.502 ms (5%) |          |   32 bytes (1%) |           2 |
| `["sum", "valley", "reduce", "basesize=128"]`       |   8.800 ms (5%) |          | 103.23 KiB (1%) |        1018 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   8.478 ms (5%) |          |  51.23 KiB (1%) |         506 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   8.631 ms (5%) |          |  25.25 KiB (1%) |         251 |
| `["words", "nthreads=1"]`                           |  23.509 ms (5%) |          |  31.74 MiB (1%) |     1034104 |
| `["words", "nthreads=2"]`                           |  14.799 ms (5%) |          |  32.10 MiB (1%) |     1034151 |
| `["words", "nthreads=4"]`                           |  14.780 ms (5%) |          |  32.82 MiB (1%) |     1034223 |

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
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz      83168 s         19 s       3102 s      68918 s          0 s
       #2  2095 MHz      78140 s         10 s       3254 s      73934 s          0 s
       
  Memory: 6.791339874267578 GB (3586.515625 MB free)
  Uptime: 1561.0 sec
  Load Avg:  1.5703125  1.49169921875  1.0947265625
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
    CPU MHz:                         2095.176
    BogoMIPS:                        4190.35
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

