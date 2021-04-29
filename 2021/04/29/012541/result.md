# Multi-thread benchmark result

* Pull request commit: [`bd187f917e44e09f4c4c97a02d4d6f5f72331206`](https://github.com/JuliaFolds/Transducers.jl/commit/bd187f917e44e09f4c4c97a02d4d6f5f72331206)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/243> (Update */Manifest.toml)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 29 Apr 2021 - 01:19
    - Baseline: 29 Apr 2021 - 01:25
* Package commits:
    - Target: 06147e
    - Baseline: df8f12
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
| `["collect", "unordered", "basesize=1024"]`         |                1.11 (5%) :x: |                1.10 (1%) :x: |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` |                1.23 (5%) :x: |                1.07 (1%) :x: |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` |                1.16 (5%) :x: |                1.03 (1%) :x: |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` |                   0.97 (5%)  | 0.93 (1%) :white_check_mark: |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 0.93 (5%) :white_check_mark: | 0.95 (1%) :white_check_mark: |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  |                1.10 (5%) :x: |                1.15 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |                1.12 (5%) :x: |                1.15 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |                1.19 (5%) :x: |                1.40 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |                2.66 (5%) :x: |                1.80 (1%) :x: |
| `["parallel_histogram", "comm", "basesize=16384"]`  |                1.08 (5%) :x: |                   1.01 (1%)  |
| `["parallel_histogram", "comm", "basesize=4096"]`   |                   1.00 (5%)  | 0.99 (1%) :white_check_mark: |
| `["splitby", "count", "man"]`                       | 0.88 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["splitby", "count", "reduce"]`                    |                   0.96 (5%)  |                1.02 (1%) :x: |

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
  uname: Linux 5.4.0-1046-azure #48-Ubuntu SMP Tue Apr 13 07:18:42 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz      56894 s         16 s       2453 s      52088 s          0 s
       #2  2095 MHz      49023 s          3 s       2611 s      59815 s          0 s
       
  Memory: 6.791343688964844 GB (3651.91796875 MB free)
  Uptime: 1121.0 sec
  Load Avg:  1.5791015625  1.4794921875  0.91552734375
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
  uname: Linux 5.4.0-1046-azure #48-Ubuntu SMP Tue Apr 13 07:18:42 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz      80667 s         16 s       3140 s      59678 s          0 s
       #2  2095 MHz      73752 s          3 s       3320 s      66489 s          0 s
       
  Memory: 6.791343688964844 GB (3647.6171875 MB free)
  Uptime: 1443.0 sec
  Load Avg:  1.7109375  1.56640625  1.11474609375
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, skylake-avx512)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 29 Apr 2021 - 1:19
* Package commit: 06147e
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
| `["collect", "assoc", "basesize=1"]`                | 226.631 ms (5%) |         |  32.66 MiB (1%) |      286740 |
| `["collect", "assoc", "basesize=1024"]`             | 189.317 ms (5%) |         |   1.79 MiB (1%) |         569 |
| `["collect", "assoc", "basesize=32"]`               | 188.780 ms (5%) |         |   3.97 MiB (1%) |       13306 |
| `["collect", "seq"]`                                | 370.749 ms (5%) |         | 512.72 KiB (1%) |          15 |
| `["collect", "unordered", "basesize=1"]`            | 420.432 ms (5%) |         |  30.01 MiB (1%) |      360765 |
| `["collect", "unordered", "basesize=1024"]`         | 299.457 ms (5%) |         | 964.92 KiB (1%) |        7599 |
| `["collect", "unordered", "basesize=32"]`           | 216.463 ms (5%) |         |   1.48 MiB (1%) |       12709 |
| `["findfirst", "n=1000", "foldl"]`                  | 596.308 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 514.069 ms (5%) |         | 940.39 KiB (1%) |       16495 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 475.321 ms (5%) |         | 482.64 KiB (1%) |        8455 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 599.923 ms (5%) |         | 328.98 KiB (1%) |        5774 |
| `["findfirst", "n=400", "foldl"]`                   | 437.251 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 246.683 ms (5%) |         |   1.08 MiB (1%) |       19466 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 248.288 ms (5%) |         | 595.55 KiB (1%) |       10508 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 274.443 ms (5%) |         | 371.03 KiB (1%) |        6535 |
| `["findfirst", "n=500", "foldl"]`                   |  74.215 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 172.412 ms (5%) |         | 734.63 KiB (1%) |       12826 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 137.258 ms (5%) |         | 363.66 KiB (1%) |        6331 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 331.452 ms (5%) |         | 379.86 KiB (1%) |        6668 |
| `["overhead", "default"]`                           |  55.000 μs (5%) |         |  47.33 KiB (1%) |         381 |
| `["overhead", "stoppable=false"]`                   |  55.900 μs (5%) |         |  47.36 KiB (1%) |         381 |
| `["overhead", "stoppable=true"]`                    | 139.102 μs (5%) |         | 139.67 KiB (1%) |        2464 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   3.298 ms (5%) |         | 730.06 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   3.807 ms (5%) |         |   1.79 MiB (1%) |         213 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   3.556 ms (5%) |         |   1.43 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  14.920 ms (5%) |         |   1.23 MiB (1%) |         523 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  23.222 ms (5%) |         |   1.05 MiB (1%) |        2772 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  18.839 ms (5%) |         |   1.25 MiB (1%) |        1051 |
| `["parallel_histogram", "seq"]`                     |   6.032 ms (5%) |         | 364.61 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  30.246 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  15.016 ms (5%) |         |   2.66 KiB (1%) |          48 |
| `["splitby", "count", "foldl"]`                     |   3.920 ms (5%) |         |   96 bytes (1%) |           4 |
| `["splitby", "count", "man"]`                       |   1.417 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    | 982.408 μs (5%) |         |   2.84 KiB (1%) |          54 |
| `["sum", "random", "foldl"]`                        |  13.885 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "random", "reduce", "basesize=128"]`       |   6.867 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "random", "reduce", "basesize=256"]`       |   6.906 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "random", "reduce", "basesize=512"]`       |   6.700 ms (5%) |         |  25.30 KiB (1%) |         252 |
| `["sum", "uniform", "foldl"]`                       |  13.294 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   6.628 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   6.629 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   6.519 ms (5%) |         |  25.25 KiB (1%) |         251 |
| `["sum", "valley", "foldl"]`                        |  13.962 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "valley", "reduce", "basesize=128"]`       |   6.895 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   6.849 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   6.763 ms (5%) |         |  25.25 KiB (1%) |         251 |
| `["words", "nthreads=1"]`                           |  19.513 ms (5%) |         |  31.60 MiB (1%) |     1029644 |
| `["words", "nthreads=2"]`                           |  12.053 ms (5%) |         |  31.96 MiB (1%) |     1029684 |
| `["words", "nthreads=4"]`                           |  12.887 ms (5%) |         |  32.86 MiB (1%) |     1029838 |

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
  uname: Linux 5.4.0-1046-azure #48-Ubuntu SMP Tue Apr 13 07:18:42 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz      56894 s         16 s       2453 s      52088 s          0 s
       #2  2095 MHz      49023 s          3 s       2611 s      59815 s          0 s
       
  Memory: 6.791343688964844 GB (3651.91796875 MB free)
  Uptime: 1121.0 sec
  Load Avg:  1.5791015625  1.4794921875  0.91552734375
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, skylake-avx512)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 29 Apr 2021 - 1:25
* Package commit: df8f12
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
| `["collect", "assoc", "basesize=1"]`                | 233.194 ms (5%) |         |  32.66 MiB (1%) |      286741 |
| `["collect", "assoc", "basesize=1024"]`             | 187.633 ms (5%) |         |   1.79 MiB (1%) |         570 |
| `["collect", "assoc", "basesize=32"]`               | 190.580 ms (5%) |         |   3.97 MiB (1%) |       13306 |
| `["collect", "seq"]`                                | 368.871 ms (5%) |         | 512.72 KiB (1%) |          15 |
| `["collect", "unordered", "basesize=1"]`            | 404.629 ms (5%) |         |  30.01 MiB (1%) |      360585 |
| `["collect", "unordered", "basesize=1024"]`         | 269.067 ms (5%) |         | 873.73 KiB (1%) |        4699 |
| `["collect", "unordered", "basesize=32"]`           | 211.332 ms (5%) |         |   1.48 MiB (1%) |       12655 |
| `["findfirst", "n=1000", "foldl"]`                  | 595.469 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 417.539 ms (5%) |         | 881.03 KiB (1%) |       15391 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 409.933 ms (5%) |         | 466.42 KiB (1%) |        8171 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 616.594 ms (5%) |         | 352.27 KiB (1%) |        6187 |
| `["findfirst", "n=400", "foldl"]`                   | 436.039 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 265.518 ms (5%) |         |   1.13 MiB (1%) |       20399 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 251.640 ms (5%) |         | 600.33 KiB (1%) |       10597 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 248.539 ms (5%) |         | 323.00 KiB (1%) |        5710 |
| `["findfirst", "n=500", "foldl"]`                   |  75.106 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 153.277 ms (5%) |         | 637.55 KiB (1%) |       11153 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 115.560 ms (5%) |         | 260.55 KiB (1%) |        4565 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 124.766 ms (5%) |         | 210.83 KiB (1%) |        3669 |
| `["overhead", "default"]`                           |  54.901 μs (5%) |         |  47.33 KiB (1%) |         381 |
| `["overhead", "stoppable=false"]`                   |  54.401 μs (5%) |         |  47.36 KiB (1%) |         381 |
| `["overhead", "stoppable=true"]`                    | 134.101 μs (5%) |         | 139.67 KiB (1%) |        2464 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   3.324 ms (5%) |         | 730.06 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   3.841 ms (5%) |         |   1.79 MiB (1%) |         213 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   3.590 ms (5%) |         |   1.43 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  13.789 ms (5%) |         |   1.22 MiB (1%) |         160 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  23.137 ms (5%) |         |   1.07 MiB (1%) |        2780 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  19.829 ms (5%) |         |   1.25 MiB (1%) |        1232 |
| `["parallel_histogram", "seq"]`                     |   6.075 ms (5%) |         | 364.61 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  30.068 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  15.033 ms (5%) |         |   2.66 KiB (1%) |          48 |
| `["splitby", "count", "foldl"]`                     |   3.991 ms (5%) |         |   96 bytes (1%) |           4 |
| `["splitby", "count", "man"]`                       |   1.604 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    |   1.020 ms (5%) |         |   2.78 KiB (1%) |          52 |
| `["sum", "random", "foldl"]`                        |  14.044 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "random", "reduce", "basesize=128"]`       |   6.805 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "random", "reduce", "basesize=256"]`       |   6.785 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "random", "reduce", "basesize=512"]`       |   6.714 ms (5%) |         |  25.30 KiB (1%) |         252 |
| `["sum", "uniform", "foldl"]`                       |  13.425 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   6.567 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   6.505 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   6.466 ms (5%) |         |  25.25 KiB (1%) |         251 |
| `["sum", "valley", "foldl"]`                        |  13.995 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "valley", "reduce", "basesize=128"]`       |   6.896 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   6.823 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   6.756 ms (5%) |         |  25.25 KiB (1%) |         251 |
| `["words", "nthreads=1"]`                           |  19.785 ms (5%) |         |  31.79 MiB (1%) |     1035996 |
| `["words", "nthreads=2"]`                           |  12.508 ms (5%) |         |  32.15 MiB (1%) |     1036045 |
| `["words", "nthreads=4"]`                           |  12.540 ms (5%) |         |  32.86 MiB (1%) |     1036125 |

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
  uname: Linux 5.4.0-1046-azure #48-Ubuntu SMP Tue Apr 13 07:18:42 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz      80667 s         16 s       3140 s      59678 s          0 s
       #2  2095 MHz      73752 s          3 s       3320 s      66489 s          0 s
       
  Memory: 6.791343688964844 GB (3647.6171875 MB free)
  Uptime: 1443.0 sec
  Load Avg:  1.7109375  1.56640625  1.11474609375
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
    CPU MHz:                         2095.077
    BogoMIPS:                        4190.15
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

