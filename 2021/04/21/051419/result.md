# Multi-thread benchmark result

* Pull request commit: [`93ac54bd633a5b79f8d6dc6c66030ae25313bdc3`](https://github.com/JuliaFolds/Transducers.jl/commit/93ac54bd633a5b79f8d6dc6c66030ae25313bdc3)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/475> (Always run vanilla-test)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 21 Apr 2021 - 05:08
    - Baseline: 21 Apr 2021 - 05:13
* Package commits:
    - Target: a8837c
    - Baseline: 2cc4af
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
| `["collect", "unordered", "basesize=1024"]`         | 0.92 (5%) :white_check_mark: | 0.96 (1%) :white_check_mark: |
| `["findfirst", "n=1000", "foldl"]`                  | 0.94 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 0.52 (5%) :white_check_mark: | 0.57 (1%) :white_check_mark: |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` |                1.06 (5%) :x: |                1.06 (1%) :x: |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` |                   0.99 (5%)  |                1.02 (1%) :x: |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  |                   1.01 (5%)  |                1.04 (1%) :x: |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 0.92 (5%) :white_check_mark: | 0.98 (1%) :white_check_mark: |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 0.90 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |                1.59 (5%) :x: |                1.52 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |                1.30 (5%) :x: |                1.15 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 0.93 (5%) :white_check_mark: | 0.99 (1%) :white_check_mark: |
| `["overhead", "stoppable=false"]`                   |                1.10 (5%) :x: |                   1.00 (1%)  |
| `["parallel_histogram", "assoc", "basesize=8192"]`  | 0.94 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["splitby", "count", "foldl"]`                     |                2.28 (5%) :x: |                6.00 (1%) :x: |
| `["splitby", "count", "man"]`                       | 0.92 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["splitby", "count", "reduce"]`                    |                1.09 (5%) :x: |                1.02 (1%) :x: |
| `["words", "nthreads=2"]`                           |                   1.04 (5%)  |                1.02 (1%) :x: |

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
  CPU: Intel(R) Xeon(R) CPU E5-2673 v3 @ 2.40GHz: 
              speed         user         nice          sys         idle          irq
       #1  2397 MHz      53558 s         14 s       2082 s      30572 s          0 s
       #2  2397 MHz      58045 s         12 s       2350 s      25963 s          0 s
       
  Memory: 6.791343688964844 GB (3684.8671875 MB free)
  Uptime: 869.0 sec
  Load Avg:  1.57177734375  1.46435546875  0.89013671875
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, haswell)
```

### Baseline
```
Julia Version 1.5.4
Commit 69fcb5745b (2021-03-11 19:13 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 20.04.2 LTS
  uname: Linux 5.4.0-1043-azure #45-Ubuntu SMP Fri Mar 19 17:33:38 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v3 @ 2.40GHz: 
              speed         user         nice          sys         idle          irq
       #1  2397 MHz      78830 s         14 s       2522 s      37258 s          0 s
       #2  2397 MHz      82499 s         12 s       2786 s      33543 s          0 s
       
  Memory: 6.791343688964844 GB (3654.70703125 MB free)
  Uptime: 1195.0 sec
  Load Avg:  1.703125  1.5927734375  1.1162109375
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, haswell)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 21 Apr 2021 - 5:8
* Package commit: a8837c
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
| `["collect", "assoc", "basesize=1"]`                | 302.492 ms (5%) |         |  32.66 MiB (1%) |      286755 |
| `["collect", "assoc", "basesize=1024"]`             | 254.385 ms (5%) |         |   1.79 MiB (1%) |         570 |
| `["collect", "assoc", "basesize=32"]`               | 256.028 ms (5%) |         |   3.97 MiB (1%) |       13307 |
| `["collect", "seq"]`                                | 502.779 ms (5%) |         | 512.72 KiB (1%) |          15 |
| `["collect", "unordered", "basesize=1"]`            | 527.616 ms (5%) |         |  30.01 MiB (1%) |      360612 |
| `["collect", "unordered", "basesize=1024"]`         | 294.888 ms (5%) |         | 830.89 KiB (1%) |        3328 |
| `["collect", "unordered", "basesize=32"]`           | 278.224 ms (5%) |         |   1.47 MiB (1%) |       12597 |
| `["findfirst", "n=1000", "foldl"]`                  | 702.381 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 448.925 ms (5%) |         | 777.13 KiB (1%) |       13610 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 553.792 ms (5%) |         | 515.41 KiB (1%) |        9038 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 663.916 ms (5%) |         | 335.83 KiB (1%) |        5889 |
| `["findfirst", "n=400", "foldl"]`                   | 528.080 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 300.640 ms (5%) |         |   1.16 MiB (1%) |       20867 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 291.409 ms (5%) |         | 590.70 KiB (1%) |       10414 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 314.672 ms (5%) |         | 350.56 KiB (1%) |        6183 |
| `["findfirst", "n=500", "foldl"]`                   |  89.234 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 243.505 ms (5%) |         | 923.98 KiB (1%) |       16098 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 201.410 ms (5%) |         | 428.61 KiB (1%) |        7467 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 152.800 ms (5%) |         | 210.84 KiB (1%) |        3669 |
| `["overhead", "default"]`                           |  57.801 μs (5%) |         |  47.36 KiB (1%) |         382 |
| `["overhead", "stoppable=false"]`                   |  60.802 μs (5%) |         |  47.39 KiB (1%) |         382 |
| `["overhead", "stoppable=true"]`                    | 157.404 μs (5%) |         | 139.67 KiB (1%) |        2464 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   4.239 ms (5%) |         | 730.06 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   5.412 ms (5%) |         |   1.79 MiB (1%) |         213 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   4.634 ms (5%) |         |   1.43 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  12.552 ms (5%) |         |   1.22 MiB (1%) |         206 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  19.254 ms (5%) |         |   1.01 MiB (1%) |        1066 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  14.581 ms (5%) |         |   1.23 MiB (1%) |         431 |
| `["parallel_histogram", "seq"]`                     |   7.741 ms (5%) |         | 364.61 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  61.309 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  30.772 ms (5%) |         |   2.66 KiB (1%) |          48 |
| `["splitby", "count", "foldl"]`                     |   4.466 ms (5%) |         |   96 bytes (1%) |           4 |
| `["splitby", "count", "man"]`                       |   1.591 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    | 966.425 μs (5%) |         |   2.83 KiB (1%) |          55 |
| `["sum", "random", "foldl"]`                        |  17.280 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "random", "reduce", "basesize=128"]`       |   9.048 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "random", "reduce", "basesize=256"]`       |   9.119 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "random", "reduce", "basesize=512"]`       |   9.072 ms (5%) |         |  25.30 KiB (1%) |         252 |
| `["sum", "uniform", "foldl"]`                       |  17.092 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   9.125 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   9.174 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   8.767 ms (5%) |         |  25.25 KiB (1%) |         251 |
| `["sum", "valley", "foldl"]`                        |  18.284 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "valley", "reduce", "basesize=128"]`       |   9.390 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   9.386 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   9.391 ms (5%) |         |  25.25 KiB (1%) |         251 |
| `["words", "nthreads=1"]`                           |  25.061 ms (5%) |         |  31.87 MiB (1%) |     1038057 |
| `["words", "nthreads=2"]`                           |  16.039 ms (5%) |         |  32.58 MiB (1%) |     1038143 |
| `["words", "nthreads=4"]`                           |  16.452 ms (5%) |         |  33.03 MiB (1%) |     1038213 |

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
  CPU: Intel(R) Xeon(R) CPU E5-2673 v3 @ 2.40GHz: 
              speed         user         nice          sys         idle          irq
       #1  2397 MHz      53558 s         14 s       2082 s      30572 s          0 s
       #2  2397 MHz      58045 s         12 s       2350 s      25963 s          0 s
       
  Memory: 6.791343688964844 GB (3684.8671875 MB free)
  Uptime: 869.0 sec
  Load Avg:  1.57177734375  1.46435546875  0.89013671875
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, haswell)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 21 Apr 2021 - 5:13
* Package commit: 2cc4af
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
| `["collect", "assoc", "basesize=1"]`                | 298.615 ms (5%) |         |  32.66 MiB (1%) |      286757 |
| `["collect", "assoc", "basesize=1024"]`             | 250.385 ms (5%) |         |   1.79 MiB (1%) |         570 |
| `["collect", "assoc", "basesize=32"]`               | 253.609 ms (5%) |         |   3.97 MiB (1%) |       13306 |
| `["collect", "seq"]`                                | 501.568 ms (5%) |         | 512.72 KiB (1%) |          15 |
| `["collect", "unordered", "basesize=1"]`            | 509.949 ms (5%) |         |  30.01 MiB (1%) |      360602 |
| `["collect", "unordered", "basesize=1024"]`         | 319.766 ms (5%) |         | 862.70 KiB (1%) |        4328 |
| `["collect", "unordered", "basesize=32"]`           | 277.741 ms (5%) |         |   1.48 MiB (1%) |       12729 |
| `["findfirst", "n=1000", "foldl"]`                  | 746.771 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 867.059 ms (5%) |         |   1.33 MiB (1%) |       23854 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 520.831 ms (5%) |         | 484.97 KiB (1%) |        8496 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 672.514 ms (5%) |         | 329.02 KiB (1%) |        5775 |
| `["findfirst", "n=400", "foldl"]`                   | 545.660 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 296.695 ms (5%) |         |   1.12 MiB (1%) |       20097 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 317.401 ms (5%) |         | 602.27 KiB (1%) |       10617 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 348.652 ms (5%) |         | 350.56 KiB (1%) |        6183 |
| `["findfirst", "n=500", "foldl"]`                   |  93.231 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 153.527 ms (5%) |         | 608.58 KiB (1%) |       10600 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 155.321 ms (5%) |         | 373.23 KiB (1%) |        6506 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 164.089 ms (5%) |         | 213.25 KiB (1%) |        3716 |
| `["overhead", "default"]`                           |  56.001 μs (5%) |         |  47.36 KiB (1%) |         382 |
| `["overhead", "stoppable=false"]`                   |  55.201 μs (5%) |         |  47.39 KiB (1%) |         382 |
| `["overhead", "stoppable=true"]`                    | 159.404 μs (5%) |         | 139.67 KiB (1%) |        2464 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   4.416 ms (5%) |         | 730.06 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   5.193 ms (5%) |         |   1.79 MiB (1%) |         213 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   4.911 ms (5%) |         |   1.43 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  12.558 ms (5%) |         |   1.22 MiB (1%) |         199 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  20.246 ms (5%) |         |   1.01 MiB (1%) |        1409 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  14.607 ms (5%) |         |   1.23 MiB (1%) |         351 |
| `["parallel_histogram", "seq"]`                     |   7.861 ms (5%) |         | 364.61 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  60.938 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  31.860 ms (5%) |         |   2.66 KiB (1%) |          48 |
| `["splitby", "count", "foldl"]`                     |   1.957 ms (5%) |         |   16 bytes (1%) |           1 |
| `["splitby", "count", "man"]`                       |   1.735 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    | 883.923 μs (5%) |         |   2.78 KiB (1%) |          52 |
| `["sum", "random", "foldl"]`                        |  17.859 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "random", "reduce", "basesize=128"]`       |   9.222 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "random", "reduce", "basesize=256"]`       |   9.047 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "random", "reduce", "basesize=512"]`       |   9.114 ms (5%) |         |  25.30 KiB (1%) |         252 |
| `["sum", "uniform", "foldl"]`                       |  17.454 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   9.176 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   8.963 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   8.742 ms (5%) |         |  25.25 KiB (1%) |         251 |
| `["sum", "valley", "foldl"]`                        |  17.924 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "valley", "reduce", "basesize=128"]`       |   9.011 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   9.359 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   9.314 ms (5%) |         |  25.25 KiB (1%) |         251 |
| `["words", "nthreads=1"]`                           |  25.182 ms (5%) |         |  31.74 MiB (1%) |     1033574 |
| `["words", "nthreads=2"]`                           |  15.400 ms (5%) |         |  32.09 MiB (1%) |     1033622 |
| `["words", "nthreads=4"]`                           |  16.490 ms (5%) |         |  32.81 MiB (1%) |     1033709 |

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
  CPU: Intel(R) Xeon(R) CPU E5-2673 v3 @ 2.40GHz: 
              speed         user         nice          sys         idle          irq
       #1  2397 MHz      78830 s         14 s       2522 s      37258 s          0 s
       #2  2397 MHz      82499 s         12 s       2786 s      33543 s          0 s
       
  Memory: 6.791343688964844 GB (3654.70703125 MB free)
  Uptime: 1195.0 sec
  Load Avg:  1.703125  1.5927734375  1.1162109375
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, haswell)
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
    Model:                           63
    Model name:                      Intel(R) Xeon(R) CPU E5-2673 v3 @ 2.40GHz
    Stepping:                        2
    CPU MHz:                         2397.218
    BogoMIPS:                        4794.43
    Hypervisor vendor:               Microsoft
    Virtualization type:             full
    L1d cache:                       64 KiB
    L1i cache:                       64 KiB
    L2 cache:                        512 KiB
    L3 cache:                        30 MiB
    NUMA node0 CPU(s):               0,1
    Vulnerability Itlb multihit:     KVM: Vulnerable
    Vulnerability L1tf:              Mitigation; PTE Inversion
    Vulnerability Mds:               Mitigation; Clear CPU buffers; SMT Host state unknown
    Vulnerability Meltdown:          Mitigation; PTI
    Vulnerability Spec store bypass: Vulnerable
    Vulnerability Spectre v1:        Mitigation; usercopy/swapgs barriers and __user pointer sanitization
    Vulnerability Spectre v2:        Mitigation; Full generic retpoline, STIBP disabled, RSB filling
    Vulnerability Srbds:             Not affected
    Vulnerability Tsx async abort:   Not affected
    Flags:                           fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush mmx fxsr sse sse2 ss ht syscall nx pdpe1gb rdtscp lm constant_tsc rep_good nopl xtopology cpuid pni pclmulqdq ssse3 fma cx16 pcid sse4_1 sse4_2 movbe popcnt aes xsave avx f16c rdrand hypervisor lahf_lm abm invpcid_single pti fsgsbase bmi1 avx2 smep bmi2 erms invpcid xsaveopt md_clear
    

| Cpu Property       | Value                                                   |
|:------------------ |:------------------------------------------------------- |
| Brand              | Intel(R) Xeon(R) CPU E5-2673 v3 @ 2.40GHz               |
| Vendor             | :Intel                                                  |
| Architecture       | :Haswell                                                |
| Model              | Family: 0x06, Model: 0x3f, Stepping: 0x02, Type: 0x00   |
| Cores              | 2 physical cores, 2 logical cores (on executing CPU)    |
|                    | No Hyperthreading hardware capability detected          |
| Clock Frequencies  | Not supported by CPU                                    |
| Data Cache         | Level 1:3 : (32, 256, 30720) kbytes                     |
|                    | 64 byte cache line size                                 |
| Address Size       | 48 bits virtual, 46 bits physical                       |
| SIMD               | 256 bit = 32 byte max. SIMD vector size                 |
| Time Stamp Counter | TSC is accessible via `rdtsc`                           |
|                    | TSC increased at every clock cycle (non-invariant TSC)  |
| Perf. Monitoring   | Performance Monitoring Counters (PMC) are not supported |
| Hypervisor         | Yes, Microsoft                                          |

