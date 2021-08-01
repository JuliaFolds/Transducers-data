# Multi-thread benchmark result

* Pull request commit: [`0168d3c7b1fed0a77fc3e2d2db1ff4054d1dbee1`](https://github.com/JuliaFolds/Transducers.jl/commit/0168d3c7b1fed0a77fc3e2d2db1ff4054d1dbee1)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/243> (Update */Manifest.toml)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 1 Aug 2021 - 01:24
    - Baseline: 1 Aug 2021 - 01:30
* Package commits:
    - Target: a27739
    - Baseline: 9ac175
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
| `["collect", "unordered", "basesize=1024"]`         |                1.09 (5%) :x: |                1.06 (1%) :x: |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` |                1.06 (5%) :x: |                1.10 (1%) :x: |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 0.95 (5%) :white_check_mark: | 0.95 (1%) :white_check_mark: |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  |                   1.01 (5%)  |                1.05 (1%) :x: |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  |                   0.99 (5%)  |                1.04 (1%) :x: |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 0.92 (5%) :white_check_mark: | 0.92 (1%) :white_check_mark: |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 0.94 (5%) :white_check_mark: | 0.94 (1%) :white_check_mark: |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |                1.68 (5%) :x: |                1.57 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |                1.16 (5%) :x: |                1.17 (1%) :x: |
| `["parallel_histogram", "comm", "basesize=4096"]`   |                   0.99 (5%)  |                1.02 (1%) :x: |
| `["parallel_histogram", "comm", "basesize=8192"]`   | 0.90 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["splitby", "count", "foldl"]`                     |                1.08 (5%) :x: |                   1.00 (1%)  |
| `["splitby", "count", "reduce"]`                    | 0.91 (5%) :white_check_mark: |                1.03 (1%) :x: |

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
  uname: Linux 5.8.0-1039-azure #42~20.04.1-Ubuntu SMP Thu Jul 15 14:11:07 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz      56926 s         12 s       2338 s      28935 s          0 s
       #2  2095 MHz      53673 s         10 s       2420 s      32424 s          0 s
       
  Memory: 6.790924072265625 GB (3627.796875 MB free)
  Uptime: 891.0 sec
  Load Avg:  1.587890625  1.46728515625  0.89697265625
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
  uname: Linux 5.8.0-1039-azure #42~20.04.1-Ubuntu SMP Thu Jul 15 14:11:07 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz      83248 s         12 s       2922 s      36292 s          0 s
       #2  2095 MHz      78255 s         10 s       3088 s      41229 s          0 s
       
  Memory: 6.790924072265625 GB (3667.99609375 MB free)
  Uptime: 1234.0 sec
  Load Avg:  1.6416015625  1.55126953125  1.1103515625
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, skylake-avx512)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 1 Aug 2021 - 1:24
* Package commit: a27739
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
| `["collect", "assoc", "basesize=1"]`                | 285.491 ms (5%) |         |  32.66 MiB (1%) |      286742 |
| `["collect", "assoc", "basesize=1024"]`             | 244.130 ms (5%) |         |   1.79 MiB (1%) |         570 |
| `["collect", "assoc", "basesize=32"]`               | 244.842 ms (5%) |         |   3.97 MiB (1%) |       13306 |
| `["collect", "seq"]`                                | 472.987 ms (5%) |         | 512.72 KiB (1%) |          15 |
| `["collect", "unordered", "basesize=1"]`            | 498.374 ms (5%) |         |  30.01 MiB (1%) |      360569 |
| `["collect", "unordered", "basesize=1024"]`         | 332.554 ms (5%) |         | 896.48 KiB (1%) |        5409 |
| `["collect", "unordered", "basesize=32"]`           | 270.110 ms (5%) |         |   1.47 MiB (1%) |       12570 |
| `["findfirst", "n=1000", "foldl"]`                  | 743.478 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 813.843 ms (5%) |         |   1.24 MiB (1%) |       22296 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 506.703 ms (5%) |         | 466.42 KiB (1%) |        8171 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 688.816 ms (5%) |         | 328.98 KiB (1%) |        5774 |
| `["findfirst", "n=400", "foldl"]`                   | 562.287 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 299.160 ms (5%) |         |   1.09 MiB (1%) |       19625 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 298.726 ms (5%) |         | 597.64 KiB (1%) |       10533 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 323.629 ms (5%) |         | 341.34 KiB (1%) |        6024 |
| `["findfirst", "n=500", "foldl"]`                   |  97.779 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 181.328 ms (5%) |         | 698.72 KiB (1%) |       12171 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 176.969 ms (5%) |         | 391.55 KiB (1%) |        6821 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 186.370 ms (5%) |         | 256.72 KiB (1%) |        4467 |
| `["overhead", "default"]`                           |  70.105 μs (5%) |         |  47.33 KiB (1%) |         381 |
| `["overhead", "stoppable=false"]`                   |  68.106 μs (5%) |         |  47.36 KiB (1%) |         381 |
| `["overhead", "stoppable=true"]`                    | 172.614 μs (5%) |         | 139.64 KiB (1%) |        2463 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   4.549 ms (5%) |         | 730.06 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   5.475 ms (5%) |         |   1.79 MiB (1%) |         213 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   5.035 ms (5%) |         |   1.43 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  15.174 ms (5%) |         |   1.23 MiB (1%) |         469 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  26.172 ms (5%) |         |   1.06 MiB (1%) |        1106 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  18.371 ms (5%) |         |   1.25 MiB (1%) |        1143 |
| `["parallel_histogram", "seq"]`                     |   8.408 ms (5%) |         | 364.61 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  38.922 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  19.664 ms (5%) |         |   2.66 KiB (1%) |          48 |
| `["splitby", "count", "foldl"]`                     |   5.304 ms (5%) |         |   96 bytes (1%) |           4 |
| `["splitby", "count", "man"]`                       |   1.872 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    |   1.196 ms (5%) |         |   2.88 KiB (1%) |          55 |
| `["sum", "random", "foldl"]`                        |  18.649 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "random", "reduce", "basesize=128"]`       |   9.544 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "random", "reduce", "basesize=256"]`       |   9.673 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "random", "reduce", "basesize=512"]`       |   9.637 ms (5%) |         |  25.30 KiB (1%) |         252 |
| `["sum", "uniform", "foldl"]`                       |  17.989 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   9.178 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   9.038 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   9.270 ms (5%) |         |  25.25 KiB (1%) |         251 |
| `["sum", "valley", "foldl"]`                        |  18.482 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "valley", "reduce", "basesize=128"]`       |   9.708 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   9.475 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   9.518 ms (5%) |         |  25.25 KiB (1%) |         251 |
| `["words", "nthreads=1"]`                           |  27.043 ms (5%) |         |  31.80 MiB (1%) |     1035502 |
| `["words", "nthreads=2"]`                           |  16.291 ms (5%) |         |  32.16 MiB (1%) |     1035546 |
| `["words", "nthreads=4"]`                           |  17.007 ms (5%) |         |  33.06 MiB (1%) |     1035706 |

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
  uname: Linux 5.8.0-1039-azure #42~20.04.1-Ubuntu SMP Thu Jul 15 14:11:07 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz      56926 s         12 s       2338 s      28935 s          0 s
       #2  2095 MHz      53673 s         10 s       2420 s      32424 s          0 s
       
  Memory: 6.790924072265625 GB (3627.796875 MB free)
  Uptime: 891.0 sec
  Load Avg:  1.587890625  1.46728515625  0.89697265625
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, skylake-avx512)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 1 Aug 2021 - 1:30
* Package commit: 9ac175
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
| `["collect", "assoc", "basesize=1"]`                | 286.691 ms (5%) |         |  32.66 MiB (1%) |      286745 |
| `["collect", "assoc", "basesize=1024"]`             | 244.150 ms (5%) |         |   1.79 MiB (1%) |         570 |
| `["collect", "assoc", "basesize=32"]`               | 242.788 ms (5%) |         |   3.97 MiB (1%) |       13307 |
| `["collect", "seq"]`                                | 470.465 ms (5%) |         | 512.72 KiB (1%) |          15 |
| `["collect", "unordered", "basesize=1"]`            | 508.792 ms (5%) |         |  30.01 MiB (1%) |      360603 |
| `["collect", "unordered", "basesize=1024"]`         | 305.547 ms (5%) |         | 842.42 KiB (1%) |        3679 |
| `["collect", "unordered", "basesize=32"]`           | 275.071 ms (5%) |         |   1.48 MiB (1%) |       12682 |
| `["findfirst", "n=1000", "foldl"]`                  | 752.795 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 771.024 ms (5%) |         |   1.13 MiB (1%) |       20368 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 504.581 ms (5%) |         | 466.42 KiB (1%) |        8171 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 726.730 ms (5%) |         | 347.13 KiB (1%) |        6083 |
| `["findfirst", "n=400", "foldl"]`                   | 562.687 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 296.688 ms (5%) |         |   1.04 MiB (1%) |       18708 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 302.822 ms (5%) |         | 577.06 KiB (1%) |       10183 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 351.207 ms (5%) |         | 370.98 KiB (1%) |        6537 |
| `["findfirst", "n=500", "foldl"]`                   |  96.957 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 192.340 ms (5%) |         | 744.63 KiB (1%) |       12943 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 105.652 ms (5%) |         | 248.75 KiB (1%) |        4345 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 160.186 ms (5%) |         | 220.05 KiB (1%) |        3830 |
| `["overhead", "default"]`                           |  67.206 μs (5%) |         |  47.33 KiB (1%) |         381 |
| `["overhead", "stoppable=false"]`                   |  68.805 μs (5%) |         |  47.36 KiB (1%) |         381 |
| `["overhead", "stoppable=true"]`                    | 171.113 μs (5%) |         | 139.64 KiB (1%) |        2463 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   4.614 ms (5%) |         | 730.06 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   5.425 ms (5%) |         |   1.79 MiB (1%) |         213 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   4.828 ms (5%) |         |   1.43 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  15.494 ms (5%) |         |   1.22 MiB (1%) |         160 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  26.374 ms (5%) |         |   1.03 MiB (1%) |        2159 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  20.441 ms (5%) |         |   1.25 MiB (1%) |        1107 |
| `["parallel_histogram", "seq"]`                     |   8.290 ms (5%) |         | 364.61 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  39.835 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  20.183 ms (5%) |         |   2.66 KiB (1%) |          48 |
| `["splitby", "count", "foldl"]`                     |   4.929 ms (5%) |         |   96 bytes (1%) |           4 |
| `["splitby", "count", "man"]`                       |   1.889 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    |   1.317 ms (5%) |         |   2.78 KiB (1%) |          52 |
| `["sum", "random", "foldl"]`                        |  18.623 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "random", "reduce", "basesize=128"]`       |   9.543 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "random", "reduce", "basesize=256"]`       |   9.285 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "random", "reduce", "basesize=512"]`       |   9.560 ms (5%) |         |  25.30 KiB (1%) |         252 |
| `["sum", "uniform", "foldl"]`                       |  18.072 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   9.400 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   9.365 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   9.199 ms (5%) |         |  25.25 KiB (1%) |         251 |
| `["sum", "valley", "foldl"]`                        |  19.000 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "valley", "reduce", "basesize=128"]`       |   9.698 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   9.535 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   9.410 ms (5%) |         |  25.25 KiB (1%) |         251 |
| `["words", "nthreads=1"]`                           |  26.155 ms (5%) |         |  31.65 MiB (1%) |     1031108 |
| `["words", "nthreads=2"]`                           |  16.064 ms (5%) |         |  32.01 MiB (1%) |     1031144 |
| `["words", "nthreads=4"]`                           |  17.066 ms (5%) |         |  32.90 MiB (1%) |     1031286 |

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
  uname: Linux 5.8.0-1039-azure #42~20.04.1-Ubuntu SMP Thu Jul 15 14:11:07 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz      83248 s         12 s       2922 s      36292 s          0 s
       #2  2095 MHz      78255 s         10 s       3088 s      41229 s          0 s
       
  Memory: 6.790924072265625 GB (3667.99609375 MB free)
  Uptime: 1234.0 sec
  Load Avg:  1.6416015625  1.55126953125  1.1103515625
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
    CPU MHz:                         2095.213
    BogoMIPS:                        4190.42
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

