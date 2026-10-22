# Multi-thread benchmark result

* Pull request commit: [`6ae35083dbfa60e2f2fec52d109f37207dbf511f`](https://github.com/JuliaFolds/Transducers.jl/commit/6ae35083dbfa60e2f2fec52d109f37207dbf511f)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/243> (Update */Manifest.toml)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 22 Oct 2026 - 04:19
    - Baseline: 22 Oct 2026 - 04:25
* Package commits:
    - Target: 5c08edc
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
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 0.56 (5%) :white_check_mark: | 0.59 (1%) :white_check_mark: |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 0.74 (5%) :white_check_mark: | 0.82 (1%) :white_check_mark: |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` |                   1.02 (5%)  |                1.02 (1%) :x: |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  |                   0.99 (5%)  | 0.98 (1%) :white_check_mark: |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 0.87 (5%) :white_check_mark: | 0.82 (1%) :white_check_mark: |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 0.54 (5%) :white_check_mark: | 0.59 (1%) :white_check_mark: |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |                2.96 (5%) :x: |                2.03 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 0.83 (5%) :white_check_mark: | 0.93 (1%) :white_check_mark: |
| `["parallel_histogram", "comm", "basesize=4096"]`   |                   1.00 (5%)  | 0.97 (1%) :white_check_mark: |
| `["parallel_histogram", "comm", "basesize=8192"]`   |                   0.98 (5%)  | 0.99 (1%) :white_check_mark: |

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
      Ubuntu 24.04.5 LTS
  uname: Linux 6.17.0-1022-azure #22-Ubuntu SMP Mon Jul 27 17:24:03 UTC 2026 x86_64 x86_64
  CPU: AMD EPYC 7763 64-Core Processor: 
              speed         user         nice          sys         idle          irq
       #1  3241 MHz       2649 s          0 s        152 s       3662 s          0 s
       #2  3234 MHz       2059 s          0 s        198 s       4184 s          0 s
       #3  3239 MHz       2565 s          0 s        141 s       3756 s          0 s
       #4  3230 MHz       2740 s          0 s        175 s       3556 s          0 s
       
  Memory: 15.614940643310547 GB (11331.37109375 MB free)
  Uptime: 650.87 sec
  Load Avg:  1.62  1.49  0.9
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, znver3)
```

### Baseline
```
Julia Version 1.7.3
Commit 742b9abb4d (2022-05-06 12:58 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 24.04.5 LTS
  uname: Linux 6.17.0-1022-azure #22-Ubuntu SMP Mon Jul 27 17:24:03 UTC 2026 x86_64 x86_64
  CPU: AMD EPYC 7763 64-Core Processor: 
              speed         user         nice          sys         idle          irq
       #1  3220 MHz       3904 s          0 s        203 s       5418 s          0 s
       #2  3243 MHz       3436 s          0 s        274 s       5794 s          0 s
       #3  3239 MHz       3569 s          0 s        186 s       5771 s          0 s
       #4  3243 MHz       3880 s          0 s        240 s       5417 s          0 s
       
  Memory: 15.614940643310547 GB (11293.5234375 MB free)
  Uptime: 958.05 sec
  Load Avg:  1.57  1.58  1.11
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, znver3)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 22 Oct 2026 - 04:19
* Package commit: 5c08edc
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
| `["collect", "assoc", "basesize=1"]`                | 150.080 ms (5%) |         |   4.36 MiB (1%) |       32800 |
| `["collect", "assoc", "basesize=1024"]`             | 148.625 ms (5%) |         |   1.09 MiB (1%) |          53 |
| `["collect", "assoc", "basesize=32"]`               | 148.693 ms (5%) |         |   1.48 MiB (1%) |        1052 |
| `["collect", "seq"]`                                | 296.510 ms (5%) |         | 256.05 KiB (1%) |           2 |
| `["collect", "unordered", "basesize=1"]`            | 250.925 ms (5%) |         |  23.72 MiB (1%) |      406988 |
| `["collect", "unordered", "basesize=1024"]`         | 157.945 ms (5%) |         |   1.01 MiB (1%) |        1136 |
| `["collect", "unordered", "basesize=32"]`           | 168.274 ms (5%) |         |   1.60 MiB (1%) |       15302 |
| `["findfirst", "n=1000", "foldl"]`                  | 510.733 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 278.523 ms (5%) |         | 232.73 KiB (1%) |        3272 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 336.310 ms (5%) |         | 151.11 KiB (1%) |        2120 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 349.620 ms (5%) |         |  81.33 KiB (1%) |        1146 |
| `["findfirst", "n=400", "foldl"]`                   | 382.202 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 196.588 ms (5%) |         | 379.56 KiB (1%) |        5417 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 199.732 ms (5%) |         | 201.14 KiB (1%) |        2882 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 222.153 ms (5%) |         | 112.56 KiB (1%) |        1621 |
| `["findfirst", "n=500", "foldl"]`                   |  66.219 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |  86.223 ms (5%) |         | 161.41 KiB (1%) |        2224 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 186.642 ms (5%) |         | 159.58 KiB (1%) |        2254 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  71.195 ms (5%) |         |  53.05 KiB (1%) |         709 |
| `["overhead", "default"]`                           |  51.166 μs (5%) |         |  32.73 KiB (1%) |         418 |
| `["overhead", "stoppable=false"]`                   |  52.128 μs (5%) |         |  32.75 KiB (1%) |         418 |
| `["overhead", "stoppable=true"]`                    |  60.272 μs (5%) |         |  44.25 KiB (1%) |         610 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   2.408 ms (5%) |         | 728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   2.955 ms (5%) |         |   1.79 MiB (1%) |         216 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   2.686 ms (5%) |         |   1.42 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |   8.763 ms (5%) |         |   1.58 MiB (1%) |        2306 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  13.204 ms (5%) |         |   1.32 MiB (1%) |        9488 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  11.619 ms (5%) |         |   1.28 MiB (1%) |        7888 |
| `["parallel_histogram", "seq"]`                     |   4.266 ms (5%) |         | 364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  31.365 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  15.712 ms (5%) |         |  736 bytes (1%) |          11 |
| `["splitby", "count", "foldl"]`                     |   1.551 ms (5%) |         |                 |             |
| `["splitby", "count", "man"]`                       |   1.167 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    | 718.283 μs (5%) |         |   1.06 KiB (1%) |          18 |
| `["sum", "random", "foldl"]`                        |  11.122 ms (5%) |         |                 |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   5.690 ms (5%) |         |  74.22 KiB (1%) |        1105 |
| `["sum", "random", "reduce", "basesize=256"]`       |   5.650 ms (5%) |         |  36.69 KiB (1%) |         544 |
| `["sum", "random", "reduce", "basesize=512"]`       |   5.606 ms (5%) |         |  18.08 KiB (1%) |         269 |
| `["sum", "uniform", "foldl"]`                       |  10.927 ms (5%) |         |                 |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   5.577 ms (5%) |         |  74.12 KiB (1%) |        1102 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   5.533 ms (5%) |         |  36.78 KiB (1%) |         547 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   5.507 ms (5%) |         |  18.05 KiB (1%) |         268 |
| `["sum", "valley", "foldl"]`                        |  11.177 ms (5%) |         |                 |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   5.728 ms (5%) |         |  74.09 KiB (1%) |        1101 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   5.674 ms (5%) |         |  36.81 KiB (1%) |         548 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   5.665 ms (5%) |         |  18.08 KiB (1%) |         269 |
| `["words", "nthreads=1"]`                           |  14.185 ms (5%) |         |  31.57 MiB (1%) |     1028642 |
| `["words", "nthreads=2"]`                           |   9.288 ms (5%) |         |  31.93 MiB (1%) |     1028678 |
| `["words", "nthreads=4"]`                           |  10.050 ms (5%) |         |  32.83 MiB (1%) |     1028835 |

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
      Ubuntu 24.04.5 LTS
  uname: Linux 6.17.0-1022-azure #22-Ubuntu SMP Mon Jul 27 17:24:03 UTC 2026 x86_64 x86_64
  CPU: AMD EPYC 7763 64-Core Processor: 
              speed         user         nice          sys         idle          irq
       #1  3241 MHz       2649 s          0 s        152 s       3662 s          0 s
       #2  3234 MHz       2059 s          0 s        198 s       4184 s          0 s
       #3  3239 MHz       2565 s          0 s        141 s       3756 s          0 s
       #4  3230 MHz       2740 s          0 s        175 s       3556 s          0 s
       
  Memory: 15.614940643310547 GB (11331.37109375 MB free)
  Uptime: 650.87 sec
  Load Avg:  1.62  1.49  0.9
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, znver3)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 22 Oct 2026 - 04:25
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
| `["collect", "assoc", "basesize=1"]`                | 150.027 ms (5%) |         |   4.36 MiB (1%) |       32800 |
| `["collect", "assoc", "basesize=1024"]`             | 148.771 ms (5%) |         |   1.09 MiB (1%) |          53 |
| `["collect", "assoc", "basesize=32"]`               | 148.691 ms (5%) |         |   1.48 MiB (1%) |        1052 |
| `["collect", "seq"]`                                | 296.505 ms (5%) |         | 256.05 KiB (1%) |           2 |
| `["collect", "unordered", "basesize=1"]`            | 262.477 ms (5%) |         |  23.73 MiB (1%) |      407526 |
| `["collect", "unordered", "basesize=1024"]`         | 158.351 ms (5%) |         |   1.01 MiB (1%) |        1083 |
| `["collect", "unordered", "basesize=32"]`           | 169.266 ms (5%) |         |   1.60 MiB (1%) |       15375 |
| `["findfirst", "n=1000", "foldl"]`                  | 510.766 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 500.534 ms (5%) |         | 394.62 KiB (1%) |        5551 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 456.865 ms (5%) |         | 184.42 KiB (1%) |        2622 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 343.734 ms (5%) |         |  79.86 KiB (1%) |        1128 |
| `["findfirst", "n=400", "foldl"]`                   | 382.278 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 196.075 ms (5%) |         | 376.28 KiB (1%) |        5371 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 201.711 ms (5%) |         | 206.27 KiB (1%) |        2941 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 255.952 ms (5%) |         | 137.97 KiB (1%) |        1973 |
| `["findfirst", "n=500", "foldl"]`                   |  66.355 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 158.726 ms (5%) |         | 275.66 KiB (1%) |        3824 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |  62.997 ms (5%) |         |  78.52 KiB (1%) |        1070 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  85.913 ms (5%) |         |  56.83 KiB (1%) |         778 |
| `["overhead", "default"]`                           |  53.370 μs (5%) |         |  32.73 KiB (1%) |         418 |
| `["overhead", "stoppable=false"]`                   |  52.267 μs (5%) |         |  32.75 KiB (1%) |         418 |
| `["overhead", "stoppable=true"]`                    |  59.392 μs (5%) |         |  44.25 KiB (1%) |         610 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   2.412 ms (5%) |         | 728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   2.970 ms (5%) |         |   1.79 MiB (1%) |         216 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   2.712 ms (5%) |         |   1.42 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |   9.040 ms (5%) |         |   1.59 MiB (1%) |        2610 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  13.241 ms (5%) |         |   1.36 MiB (1%) |       10708 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  11.872 ms (5%) |         |   1.29 MiB (1%) |        8241 |
| `["parallel_histogram", "seq"]`                     |   4.285 ms (5%) |         | 364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  31.362 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  15.727 ms (5%) |         |  736 bytes (1%) |          11 |
| `["splitby", "count", "foldl"]`                     |   1.516 ms (5%) |         |                 |             |
| `["splitby", "count", "man"]`                       |   1.142 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    | 727.040 μs (5%) |         |   1.06 KiB (1%) |          18 |
| `["sum", "random", "foldl"]`                        |  11.032 ms (5%) |         |                 |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   5.633 ms (5%) |         |  74.22 KiB (1%) |        1105 |
| `["sum", "random", "reduce", "basesize=256"]`       |   5.589 ms (5%) |         |  36.78 KiB (1%) |         547 |
| `["sum", "random", "reduce", "basesize=512"]`       |   5.561 ms (5%) |         |  18.08 KiB (1%) |         269 |
| `["sum", "uniform", "foldl"]`                       |  10.929 ms (5%) |         |                 |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   5.629 ms (5%) |         |  74.22 KiB (1%) |        1105 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   5.558 ms (5%) |         |  36.75 KiB (1%) |         546 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   5.515 ms (5%) |         |  18.05 KiB (1%) |         268 |
| `["sum", "valley", "foldl"]`                        |  11.177 ms (5%) |         |                 |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   5.743 ms (5%) |         |  74.12 KiB (1%) |        1102 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   5.679 ms (5%) |         |  36.78 KiB (1%) |         547 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   5.669 ms (5%) |         |  18.08 KiB (1%) |         269 |
| `["words", "nthreads=1"]`                           |  14.471 ms (5%) |         |  31.74 MiB (1%) |     1034112 |
| `["words", "nthreads=2"]`                           |   9.084 ms (5%) |         |  32.09 MiB (1%) |     1034153 |
| `["words", "nthreads=4"]`                           |   9.662 ms (5%) |         |  32.99 MiB (1%) |     1034319 |

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
      Ubuntu 24.04.5 LTS
  uname: Linux 6.17.0-1022-azure #22-Ubuntu SMP Mon Jul 27 17:24:03 UTC 2026 x86_64 x86_64
  CPU: AMD EPYC 7763 64-Core Processor: 
              speed         user         nice          sys         idle          irq
       #1  3220 MHz       3904 s          0 s        203 s       5418 s          0 s
       #2  3243 MHz       3436 s          0 s        274 s       5794 s          0 s
       #3  3239 MHz       3569 s          0 s        186 s       5771 s          0 s
       #4  3243 MHz       3880 s          0 s        240 s       5417 s          0 s
       
  Memory: 15.614940643310547 GB (11293.5234375 MB free)
  Uptime: 958.05 sec
  Load Avg:  1.57  1.58  1.11
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, znver3)
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
    Address sizes:                           48 bits physical, 48 bits virtual
    Byte Order:                              Little Endian
    CPU(s):                                  4
    On-line CPU(s) list:                     0-3
    Vendor ID:                               AuthenticAMD
    Model name:                              AMD EPYC 7763 64-Core Processor
    CPU family:                              25
    Model:                                   1
    Thread(s) per core:                      2
    Core(s) per socket:                      2
    Socket(s):                               1
    Stepping:                                1
    BogoMIPS:                                4890.85
    Flags:                                   fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush mmx fxsr sse sse2 ht syscall nx mmxext fxsr_opt pdpe1gb rdtscp lm constant_tsc rep_good nopl tsc_reliable nonstop_tsc cpuid extd_apicid aperfmperf tsc_known_freq pni pclmulqdq ssse3 fma cx16 pcid sse4_1 sse4_2 movbe popcnt aes xsave avx f16c rdrand hypervisor lahf_lm cmp_legacy svm cr8_legacy abm sse4a misalignsse 3dnowprefetch osvw topoext vmmcall fsgsbase bmi1 avx2 smep bmi2 erms invpcid rdseed adx smap clflushopt clwb sha_ni xsaveopt xsavec xgetbv1 xsaves user_shstk clzero xsaveerptr rdpru arat npt nrip_save tsc_scale vmcb_clean flushbyasid decodeassists pausefilter pfthreshold v_vmsave_vmload umip vaes vpclmulqdq rdpid fsrm
    Virtualization:                          AMD-V
    Hypervisor vendor:                       Microsoft
    Virtualization type:                     full
    L1d cache:                               64 KiB (2 instances)
    L1i cache:                               64 KiB (2 instances)
    L2 cache:                                1 MiB (2 instances)
    L3 cache:                                32 MiB (1 instance)
    NUMA node(s):                            1
    NUMA node0 CPU(s):                       0-3
    Vulnerability Gather data sampling:      Not affected
    Vulnerability Ghostwrite:                Not affected
    Vulnerability Indirect target selection: Not affected
    Vulnerability Itlb multihit:             Not affected
    Vulnerability L1tf:                      Not affected
    Vulnerability Mds:                       Not affected
    Vulnerability Meltdown:                  Not affected
    Vulnerability Mmio stale data:           Not affected
    Vulnerability Old microcode:             Not affected
    Vulnerability Reg file data sampling:    Not affected
    Vulnerability Retbleed:                  Not affected
    Vulnerability Spec rstack overflow:      Vulnerable: Safe RET, no microcode
    Vulnerability Spec store bypass:         Vulnerable
    Vulnerability Spectre v1:                Mitigation; usercopy/swapgs barriers and __user pointer sanitization
    Vulnerability Spectre v2:                Mitigation; Retpolines; STIBP disabled; RSB filling; PBRSB-eIBRS Not affected; BHI Not affected
    Vulnerability Srbds:                     Not affected
    Vulnerability Tsa:                       Vulnerable: No microcode
    Vulnerability Tsx async abort:           Not affected
    Vulnerability Vmscape:                   Not affected
    

| Cpu Property       | Value                                                      |
|:------------------ |:---------------------------------------------------------- |
| Brand              | AMD EPYC 7763 64-Core Processor                            |
| Vendor             | :AMD                                                       |
| Architecture       | :Unknown                                                   |
| Model              | Family: 0xaf, Model: 0x01, Stepping: 0x01, Type: 0x00      |
| Cores              | 16 physical cores, 16 logical cores (on executing CPU)     |
|                    | No Hyperthreading hardware capability detected             |
| Clock Frequencies  | Not supported by CPU                                       |
| Data Cache         | Level 1:3 : (32, 512, 32768) kbytes                        |
|                    | 64 byte cache line size                                    |
| Address Size       | 48 bits virtual, 48 bits physical                          |
| SIMD               | 256 bit = 32 byte max. SIMD vector size                    |
| Time Stamp Counter | TSC is accessible via `rdtsc`                              |
|                    | TSC runs at constant rate (invariant from clock frequency) |
| Perf. Monitoring   | Performance Monitoring Counters (PMC) are not supported    |
| Hypervisor         | Yes, Microsoft                                             |

