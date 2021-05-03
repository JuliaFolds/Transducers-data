# Multi-thread benchmark result

* Pull request commit: [`46bc232197c7616ce8ea691a662d2a48d5532274`](https://github.com/JuliaFolds/Transducers.jl/commit/46bc232197c7616ce8ea691a662d2a48d5532274)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/243> (Update */Manifest.toml)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 3 May 2021 - 01:22
    - Baseline: 3 May 2021 - 01:27
* Package commits:
    - Target: 545a4d
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
| `["collect", "assoc", "basesize=1"]`                | 0.94 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["collect", "seq"]`                                |                1.10 (5%) :x: |                   1.00 (1%)  |
| `["collect", "unordered", "basesize=1024"]`         |                1.08 (5%) :x: |                1.06 (1%) :x: |
| `["findfirst", "n=1000", "foldl"]`                  |                1.07 (5%) :x: |                   1.00 (1%)  |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 0.58 (5%) :white_check_mark: | 0.64 (1%) :white_check_mark: |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` |                1.06 (5%) :x: |                1.02 (1%) :x: |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 0.86 (5%) :white_check_mark: | 0.91 (1%) :white_check_mark: |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 0.91 (5%) :white_check_mark: | 0.89 (1%) :white_check_mark: |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 0.94 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  |                   1.00 (5%)  | 0.99 (1%) :white_check_mark: |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 0.78 (5%) :white_check_mark: | 0.86 (1%) :white_check_mark: |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |                   0.97 (5%)  | 0.95 (1%) :white_check_mark: |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 0.75 (5%) :white_check_mark: | 0.88 (1%) :white_check_mark: |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |                   0.99 (5%)  | 0.87 (1%) :white_check_mark: |
| `["parallel_histogram", "comm", "basesize=4096"]`   | 0.80 (5%) :white_check_mark: |                   0.99 (1%)  |
| `["splitby", "count", "reduce"]`                    |                1.06 (5%) :x: |                   0.99 (1%)  |
| `["sum", "random", "foldl"]`                        | 0.93 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["sum", "random", "reduce", "basesize=128"]`       | 0.95 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["sum", "random", "reduce", "basesize=256"]`       | 0.90 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["sum", "random", "reduce", "basesize=512"]`       | 0.90 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["sum", "valley", "reduce", "basesize=256"]`       |                1.06 (5%) :x: |                   1.00 (1%)  |
| `["words", "nthreads=2"]`                           | 0.93 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["words", "nthreads=4"]`                           | 0.90 (5%) :white_check_mark: |                   1.00 (1%)  |

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
  CPU: Intel(R) Xeon(R) CPU E5-2673 v3 @ 2.40GHz: 
              speed         user         nice          sys         idle          irq
       #1  2397 MHz      50798 s         10 s       2079 s      26942 s          0 s
       #2  2397 MHz      58820 s         10 s       2366 s      18821 s          0 s
       
  Memory: 6.791343688964844 GB (3764.6015625 MB free)
  Uptime: 805.0 sec
  Load Avg:  1.65478515625  1.47021484375  0.8857421875
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
  uname: Linux 5.4.0-1046-azure #48-Ubuntu SMP Tue Apr 13 07:18:42 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v3 @ 2.40GHz: 
              speed         user         nice          sys         idle          irq
       #1  2397 MHz      77454 s         10 s       2621 s      33870 s          0 s
       #2  2397 MHz      83196 s         10 s       2909 s      28065 s          0 s
       
  Memory: 6.791343688964844 GB (3759.546875 MB free)
  Uptime: 1148.0 sec
  Load Avg:  1.689453125  1.552734375  1.10400390625
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, haswell)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 3 May 2021 - 1:22
* Package commit: 545a4d
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

| ID                                                  | time            | GC time   | memory          | allocations |
|-----------------------------------------------------|----------------:|----------:|----------------:|------------:|
| `["collect", "assoc", "basesize=1"]`                | 269.593 ms (5%) |           |  32.66 MiB (1%) |      286757 |
| `["collect", "assoc", "basesize=1024"]`             | 243.622 ms (5%) |           |   1.79 MiB (1%) |         570 |
| `["collect", "assoc", "basesize=32"]`               | 244.511 ms (5%) |           |   3.97 MiB (1%) |       13307 |
| `["collect", "seq"]`                                | 492.306 ms (5%) |           | 512.72 KiB (1%) |          15 |
| `["collect", "unordered", "basesize=1"]`            | 490.005 ms (5%) | 15.531 ms |  30.01 MiB (1%) |      360609 |
| `["collect", "unordered", "basesize=1024"]`         | 326.041 ms (5%) |           | 886.61 KiB (1%) |        5111 |
| `["collect", "unordered", "basesize=32"]`           | 259.591 ms (5%) |           |   1.47 MiB (1%) |       12543 |
| `["findfirst", "n=1000", "foldl"]`                  | 703.355 ms (5%) |           |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 489.341 ms (5%) |           | 853.89 KiB (1%) |       14954 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 520.748 ms (5%) |           | 473.50 KiB (1%) |        8298 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 649.534 ms (5%) |           | 329.05 KiB (1%) |        5776 |
| `["findfirst", "n=400", "foldl"]`                   | 487.079 ms (5%) |           |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 288.248 ms (5%) |           |   1.09 MiB (1%) |       19694 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 270.670 ms (5%) |           | 597.78 KiB (1%) |       10543 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 291.319 ms (5%) |           | 345.98 KiB (1%) |        6105 |
| `["findfirst", "n=500", "foldl"]`                   |  84.330 ms (5%) |           |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 123.539 ms (5%) |           | 523.22 KiB (1%) |        9125 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 156.836 ms (5%) |           | 363.59 KiB (1%) |        6327 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 157.223 ms (5%) |           | 204.25 KiB (1%) |        3571 |
| `["overhead", "default"]`                           |  57.402 μs (5%) |           |  47.36 KiB (1%) |         382 |
| `["overhead", "stoppable=false"]`                   |  54.702 μs (5%) |           |  47.39 KiB (1%) |         382 |
| `["overhead", "stoppable=true"]`                    | 164.905 μs (5%) |           | 139.67 KiB (1%) |        2464 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   4.165 ms (5%) |           | 730.06 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   4.838 ms (5%) |           |   1.79 MiB (1%) |         213 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   4.479 ms (5%) |           |   1.43 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  11.032 ms (5%) |           |   1.22 MiB (1%) |         182 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  15.573 ms (5%) |           |   1.00 MiB (1%) |        1081 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  15.283 ms (5%) |           |   1.23 MiB (1%) |         419 |
| `["parallel_histogram", "seq"]`                     |   7.551 ms (5%) |           | 364.61 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  56.545 ms (5%) |           |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  29.831 ms (5%) |           |   2.66 KiB (1%) |          48 |
| `["splitby", "count", "foldl"]`                     |   4.084 ms (5%) |           |   96 bytes (1%) |           4 |
| `["splitby", "count", "man"]`                       |   1.570 ms (5%) |           |                 |             |
| `["splitby", "count", "reduce"]`                    | 932.530 μs (5%) |           |   2.83 KiB (1%) |          55 |
| `["sum", "random", "foldl"]`                        |  16.221 ms (5%) |           |   32 bytes (1%) |           2 |
| `["sum", "random", "reduce", "basesize=128"]`       |   8.228 ms (5%) |           | 103.23 KiB (1%) |        1018 |
| `["sum", "random", "reduce", "basesize=256"]`       |   8.130 ms (5%) |           |  51.23 KiB (1%) |         506 |
| `["sum", "random", "reduce", "basesize=512"]`       |   8.063 ms (5%) |           |  25.30 KiB (1%) |         252 |
| `["sum", "uniform", "foldl"]`                       |  15.845 ms (5%) |           |   32 bytes (1%) |           2 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   8.188 ms (5%) |           | 103.23 KiB (1%) |        1018 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   8.132 ms (5%) |           |  51.23 KiB (1%) |         506 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   7.927 ms (5%) |           |  25.25 KiB (1%) |         251 |
| `["sum", "valley", "foldl"]`                        |  16.463 ms (5%) |           |   32 bytes (1%) |           2 |
| `["sum", "valley", "reduce", "basesize=128"]`       |   8.418 ms (5%) |           | 103.23 KiB (1%) |        1018 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   8.709 ms (5%) |           |  51.23 KiB (1%) |         506 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   8.423 ms (5%) |           |  25.25 KiB (1%) |         251 |
| `["words", "nthreads=1"]`                           |  23.870 ms (5%) |           |  31.81 MiB (1%) |     1036864 |
| `["words", "nthreads=2"]`                           |  14.893 ms (5%) |           |  32.17 MiB (1%) |     1036918 |
| `["words", "nthreads=4"]`                           |  15.689 ms (5%) |           |  33.07 MiB (1%) |     1037124 |

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
  CPU: Intel(R) Xeon(R) CPU E5-2673 v3 @ 2.40GHz: 
              speed         user         nice          sys         idle          irq
       #1  2397 MHz      50798 s         10 s       2079 s      26942 s          0 s
       #2  2397 MHz      58820 s         10 s       2366 s      18821 s          0 s
       
  Memory: 6.791343688964844 GB (3764.6015625 MB free)
  Uptime: 805.0 sec
  Load Avg:  1.65478515625  1.47021484375  0.8857421875
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, haswell)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 3 May 2021 - 1:27
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
| `["collect", "assoc", "basesize=1"]`                | 286.178 ms (5%) |         |  32.66 MiB (1%) |      286756 |
| `["collect", "assoc", "basesize=1024"]`             | 239.367 ms (5%) |         |   1.79 MiB (1%) |         570 |
| `["collect", "assoc", "basesize=32"]`               | 245.540 ms (5%) |         |   3.97 MiB (1%) |       13307 |
| `["collect", "seq"]`                                | 448.151 ms (5%) |         | 512.72 KiB (1%) |          15 |
| `["collect", "unordered", "basesize=1"]`            | 506.745 ms (5%) |         |  30.01 MiB (1%) |      360684 |
| `["collect", "unordered", "basesize=1024"]`         | 302.032 ms (5%) |         | 834.33 KiB (1%) |        3438 |
| `["collect", "unordered", "basesize=32"]`           | 250.736 ms (5%) |         |   1.47 MiB (1%) |       12559 |
| `["findfirst", "n=1000", "foldl"]`                  | 658.362 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 838.570 ms (5%) |         |   1.31 MiB (1%) |       23472 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 489.376 ms (5%) |         | 466.42 KiB (1%) |        8171 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 759.512 ms (5%) |         | 361.52 KiB (1%) |        6353 |
| `["findfirst", "n=400", "foldl"]`                   | 485.533 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 317.024 ms (5%) |         |   1.23 MiB (1%) |       22084 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 287.087 ms (5%) |         | 600.08 KiB (1%) |       10583 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 290.101 ms (5%) |         | 350.56 KiB (1%) |        6183 |
| `["findfirst", "n=500", "foldl"]`                   |  85.229 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 157.834 ms (5%) |         | 606.27 KiB (1%) |       10559 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 161.242 ms (5%) |         | 384.33 KiB (1%) |        6688 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 210.456 ms (5%) |         | 232.13 KiB (1%) |        4069 |
| `["overhead", "default"]`                           |  60.002 μs (5%) |         |  47.36 KiB (1%) |         382 |
| `["overhead", "stoppable=false"]`                   |  56.802 μs (5%) |         |  47.39 KiB (1%) |         382 |
| `["overhead", "stoppable=true"]`                    | 169.905 μs (5%) |         | 139.67 KiB (1%) |        2464 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   4.182 ms (5%) |         | 730.06 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   4.895 ms (5%) |         |   2.06 MiB (1%) |         219 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   4.494 ms (5%) |         |   1.43 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  11.392 ms (5%) |         |   1.22 MiB (1%) |         190 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  19.572 ms (5%) |         |   1.01 MiB (1%) |        1370 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  14.715 ms (5%) |         |   1.22 MiB (1%) |         267 |
| `["parallel_histogram", "seq"]`                     |   7.609 ms (5%) |         | 364.61 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  58.231 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  30.092 ms (5%) |         |   2.66 KiB (1%) |          48 |
| `["splitby", "count", "foldl"]`                     |   4.084 ms (5%) |         |   96 bytes (1%) |           4 |
| `["splitby", "count", "man"]`                       |   1.578 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    | 876.829 μs (5%) |         |   2.84 KiB (1%) |          54 |
| `["sum", "random", "foldl"]`                        |  17.392 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "random", "reduce", "basesize=128"]`       |   8.663 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "random", "reduce", "basesize=256"]`       |   9.064 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "random", "reduce", "basesize=512"]`       |   8.951 ms (5%) |         |  25.30 KiB (1%) |         252 |
| `["sum", "uniform", "foldl"]`                       |  15.895 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   8.038 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   7.979 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   7.965 ms (5%) |         |  25.25 KiB (1%) |         251 |
| `["sum", "valley", "foldl"]`                        |  16.315 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "valley", "reduce", "basesize=128"]`       |   8.305 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   8.246 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   8.725 ms (5%) |         |  25.25 KiB (1%) |         251 |
| `["words", "nthreads=1"]`                           |  24.666 ms (5%) |         |  31.89 MiB (1%) |     1039352 |
| `["words", "nthreads=2"]`                           |  15.997 ms (5%) |         |  32.25 MiB (1%) |     1039391 |
| `["words", "nthreads=4"]`                           |  17.466 ms (5%) |         |  33.15 MiB (1%) |     1039583 |

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
  CPU: Intel(R) Xeon(R) CPU E5-2673 v3 @ 2.40GHz: 
              speed         user         nice          sys         idle          irq
       #1  2397 MHz      77454 s         10 s       2621 s      33870 s          0 s
       #2  2397 MHz      83196 s         10 s       2909 s      28065 s          0 s
       
  Memory: 6.791343688964844 GB (3759.546875 MB free)
  Uptime: 1148.0 sec
  Load Avg:  1.689453125  1.552734375  1.10400390625
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
    CPU MHz:                         2397.222
    BogoMIPS:                        4794.44
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

