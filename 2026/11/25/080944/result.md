# Multi-thread benchmark result

* Pull request commit: [`9148e2b519636e9d6491eaaa55338e9de9938b8c`](https://github.com/JuliaFolds/Transducers.jl/commit/9148e2b519636e9d6491eaaa55338e9de9938b8c)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/243> (Update */Manifest.toml)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 25 Nov 2026 - 08:04
    - Baseline: 25 Nov 2026 - 08:09
* Package commits:
    - Target: e85187c
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
| `["collect", "unordered", "basesize=1024"]`         |                   0.99 (5%)  |                1.02 (1%) :x: |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` |                   1.00 (5%)  | 0.99 (1%) :white_check_mark: |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` |                1.25 (5%) :x: |                1.24 (1%) :x: |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 0.93 (5%) :white_check_mark: | 0.91 (1%) :white_check_mark: |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  |                   0.99 (5%)  | 0.98 (1%) :white_check_mark: |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  |                   0.95 (5%)  | 0.96 (1%) :white_check_mark: |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  |                   0.95 (5%)  |                1.01 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 0.89 (5%) :white_check_mark: | 0.91 (1%) :white_check_mark: |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |                1.29 (5%) :x: |                1.18 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |                1.09 (5%) :x: |                1.08 (1%) :x: |
| `["parallel_histogram", "assoc", "basesize=16384"]` |                1.12 (5%) :x: |                   1.00 (1%)  |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |                1.07 (5%) :x: |                1.15 (1%) :x: |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |                1.06 (5%) :x: |                   1.00 (1%)  |
| `["parallel_histogram", "comm", "basesize=16384"]`  | 0.87 (5%) :white_check_mark: | 0.77 (1%) :white_check_mark: |
| `["parallel_histogram", "comm", "basesize=4096"]`   |                   1.01 (5%)  | 0.99 (1%) :white_check_mark: |
| `["parallel_histogram", "comm", "basesize=8192"]`   |                1.13 (5%) :x: |                1.08 (1%) :x: |
| `["parallel_histogram", "seq"]`                     |                1.14 (5%) :x: |                   1.00 (1%)  |
| `["partition_length_maximum", "rand", "reduce"]`    |                   1.01 (5%)  | 0.96 (1%) :white_check_mark: |
| `["splitby", "count", "foldl"]`                     |                1.15 (5%) :x: |                   1.00 (1%)  |
| `["splitby", "count", "reduce"]`                    |                   1.01 (5%)  |                1.03 (1%) :x: |
| `["words", "nthreads=1"]`                           |                1.11 (5%) :x: |                1.02 (1%) :x: |
| `["words", "nthreads=2"]`                           |                1.23 (5%) :x: |                1.02 (1%) :x: |
| `["words", "nthreads=4"]`                           |                1.23 (5%) :x: |                1.02 (1%) :x: |

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
  uname: Linux 7.0.0-1020-azure #21-Ubuntu SMP PREEMPT Tue Oct 27 22:34:38 UTC 2026 x86_64 unknown
  CPU: AMD EPYC 9V45 96-Core Processor: 
              speed         user         nice          sys         idle          irq
       #1  4088 MHz       2200 s          0 s        161 s       5656 s          0 s
       #2  4086 MHz       2540 s          0 s        182 s       5314 s          0 s
       #3  4145 MHz       2143 s          0 s        158 s       5750 s          0 s
       #4  4088 MHz       2736 s          0 s        182 s       5133 s          0 s
       
  Memory: 15.608436584472656 GB (13166.98046875 MB free)
  Uptime: 810.12 sec
  Load Avg:  1.87  1.59  0.9
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, generic)
```

### Baseline
```
Julia Version 1.7.3
Commit 742b9abb4d (2022-05-06 12:58 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 26.04.1 LTS
  uname: Linux 7.0.0-1020-azure #21-Ubuntu SMP PREEMPT Tue Oct 27 22:34:38 UTC 2026 x86_64 unknown
  CPU: AMD EPYC 9V45 96-Core Processor: 
              speed         user         nice          sys         idle          irq
       #1  4264 MHz       3164 s          0 s        218 s       7546 s          0 s
       #2  4340 MHz       3893 s          0 s        244 s       6812 s          0 s
       #3  4243 MHz       3272 s          0 s        232 s       7460 s          0 s
       #4  4232 MHz       3880 s          0 s        247 s       6837 s          0 s
       
  Memory: 15.608436584472656 GB (13170.11328125 MB free)
  Uptime: 1101.9 sec
  Load Avg:  1.73  1.69  1.14
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, generic)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 25 Nov 2026 - 08:04
* Package commit: e85187c
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
| `["collect", "assoc", "basesize=1"]`                | 109.254 ms (5%) |         |   4.36 MiB (1%) |       32800 |
| `["collect", "assoc", "basesize=1024"]`             | 106.005 ms (5%) |         |   1.09 MiB (1%) |          53 |
| `["collect", "assoc", "basesize=32"]`               | 105.676 ms (5%) |         |   1.48 MiB (1%) |        1052 |
| `["collect", "seq"]`                                | 213.160 ms (5%) |         | 256.05 KiB (1%) |           2 |
| `["collect", "unordered", "basesize=1"]`            | 176.797 ms (5%) |         |  23.75 MiB (1%) |      408056 |
| `["collect", "unordered", "basesize=1024"]`         | 107.610 ms (5%) |         |   1.01 MiB (1%) |        1101 |
| `["collect", "unordered", "basesize=32"]`           | 115.482 ms (5%) |         |   1.59 MiB (1%) |       15033 |
| `["findfirst", "n=1000", "foldl"]`                  | 361.372 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 198.322 ms (5%) |         | 230.41 KiB (1%) |        3242 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 341.422 ms (5%) |         | 199.28 KiB (1%) |        2815 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 233.575 ms (5%) |         |  77.39 KiB (1%) |        1092 |
| `["findfirst", "n=400", "foldl"]`                   | 270.890 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 142.582 ms (5%) |         | 375.36 KiB (1%) |        5354 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 141.283 ms (5%) |         | 199.28 KiB (1%) |        2852 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 160.190 ms (5%) |         | 121.58 KiB (1%) |        1756 |
| `["findfirst", "n=500", "foldl"]`                   |  45.889 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |  80.854 ms (5%) |         | 200.97 KiB (1%) |        2788 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |  53.147 ms (5%) |         |  87.38 KiB (1%) |        1189 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  53.706 ms (5%) |         |  54.80 KiB (1%) |         733 |
| `["overhead", "default"]`                           |  38.238 μs (5%) |         |  32.70 KiB (1%) |         417 |
| `["overhead", "stoppable=false"]`                   |  38.578 μs (5%) |         |  32.78 KiB (1%) |         419 |
| `["overhead", "stoppable=true"]`                    |  43.135 μs (5%) |         |  44.28 KiB (1%) |         611 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   1.722 ms (5%) |         | 728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   2.200 ms (5%) |         |   2.05 MiB (1%) |         222 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   1.882 ms (5%) |         |   1.42 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |   5.887 ms (5%) |         |   1.16 MiB (1%) |         137 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |   9.777 ms (5%) |         |   1.28 MiB (1%) |        8113 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |   9.322 ms (5%) |         |   1.36 MiB (1%) |        5378 |
| `["parallel_histogram", "seq"]`                     |   3.083 ms (5%) |         | 364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  31.667 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  15.506 ms (5%) |         |  704 bytes (1%) |          10 |
| `["splitby", "count", "foldl"]`                     |   1.390 ms (5%) |         |                 |             |
| `["splitby", "count", "man"]`                       | 718.243 μs (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    | 646.135 μs (5%) |         |   1.09 KiB (1%) |          19 |
| `["sum", "random", "foldl"]`                        |   8.039 ms (5%) |         |                 |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   4.159 ms (5%) |         |  74.12 KiB (1%) |        1102 |
| `["sum", "random", "reduce", "basesize=256"]`       |   4.064 ms (5%) |         |  36.78 KiB (1%) |         547 |
| `["sum", "random", "reduce", "basesize=512"]`       |   4.030 ms (5%) |         |  18.08 KiB (1%) |         269 |
| `["sum", "uniform", "foldl"]`                       |   7.904 ms (5%) |         |                 |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   4.017 ms (5%) |         |  74.16 KiB (1%) |        1103 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   4.005 ms (5%) |         |  36.78 KiB (1%) |         547 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   3.989 ms (5%) |         |  18.08 KiB (1%) |         269 |
| `["sum", "valley", "foldl"]`                        |   8.087 ms (5%) |         |                 |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   4.174 ms (5%) |         |  74.12 KiB (1%) |        1102 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   4.156 ms (5%) |         |  36.78 KiB (1%) |         547 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   4.072 ms (5%) |         |  18.08 KiB (1%) |         269 |
| `["words", "nthreads=1"]`                           |   9.739 ms (5%) |         |  32.03 MiB (1%) |     1043877 |
| `["words", "nthreads=2"]`                           |   7.377 ms (5%) |         |  32.75 MiB (1%) |     1043964 |
| `["words", "nthreads=4"]`                           |   8.043 ms (5%) |         |  33.38 MiB (1%) |     1044148 |

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
  uname: Linux 7.0.0-1020-azure #21-Ubuntu SMP PREEMPT Tue Oct 27 22:34:38 UTC 2026 x86_64 unknown
  CPU: AMD EPYC 9V45 96-Core Processor: 
              speed         user         nice          sys         idle          irq
       #1  4088 MHz       2200 s          0 s        161 s       5656 s          0 s
       #2  4086 MHz       2540 s          0 s        182 s       5314 s          0 s
       #3  4145 MHz       2143 s          0 s        158 s       5750 s          0 s
       #4  4088 MHz       2736 s          0 s        182 s       5133 s          0 s
       
  Memory: 15.608436584472656 GB (13166.98046875 MB free)
  Uptime: 810.12 sec
  Load Avg:  1.87  1.59  0.9
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, generic)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 25 Nov 2026 - 08:09
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

| ID                                                  | time            | GC time | memory           | allocations |
|-----------------------------------------------------|----------------:|--------:|-----------------:|------------:|
| `["collect", "assoc", "basesize=1"]`                | 105.708 ms (5%) |         |    4.36 MiB (1%) |       32800 |
| `["collect", "assoc", "basesize=1024"]`             | 108.099 ms (5%) |         |    1.09 MiB (1%) |          53 |
| `["collect", "assoc", "basesize=32"]`               | 103.267 ms (5%) |         |    1.48 MiB (1%) |        1052 |
| `["collect", "seq"]`                                | 216.276 ms (5%) |         |  256.05 KiB (1%) |           2 |
| `["collect", "unordered", "basesize=1"]`            | 171.747 ms (5%) |         |   23.76 MiB (1%) |      408254 |
| `["collect", "unordered", "basesize=1024"]`         | 109.211 ms (5%) |         | 1014.52 KiB (1%) |        1053 |
| `["collect", "unordered", "basesize=32"]`           | 115.132 ms (5%) |         |    1.59 MiB (1%) |       15043 |
| `["findfirst", "n=1000", "foldl"]`                  | 372.566 ms (5%) |         |                  |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 198.578 ms (5%) |         |  232.86 KiB (1%) |        3276 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 272.482 ms (5%) |         |  161.08 KiB (1%) |        2266 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 250.470 ms (5%) |         |   85.11 KiB (1%) |        1193 |
| `["findfirst", "n=400", "foldl"]`                   | 265.439 ms (5%) |         |                  |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 143.554 ms (5%) |         |  384.22 KiB (1%) |        5479 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 148.459 ms (5%) |         |  206.58 KiB (1%) |        2952 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 168.469 ms (5%) |         |  120.08 KiB (1%) |        1714 |
| `["findfirst", "n=500", "foldl"]`                   |  47.859 ms (5%) |         |                  |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |  90.775 ms (5%) |         |  221.02 KiB (1%) |        3056 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |  41.148 ms (5%) |         |   74.34 KiB (1%) |        1006 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  49.054 ms (5%) |         |   50.72 KiB (1%) |         677 |
| `["overhead", "default"]`                           |  37.417 μs (5%) |         |   32.73 KiB (1%) |         418 |
| `["overhead", "stoppable=false"]`                   |  37.146 μs (5%) |         |   32.69 KiB (1%) |         416 |
| `["overhead", "stoppable=true"]`                    |  42.985 μs (5%) |         |   44.22 KiB (1%) |         609 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   1.534 ms (5%) |         |  728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   2.055 ms (5%) |         |    1.79 MiB (1%) |         216 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   1.778 ms (5%) |         |    1.42 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |   6.805 ms (5%) |         |    1.51 MiB (1%) |         154 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |   9.706 ms (5%) |         |    1.29 MiB (1%) |        8527 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |   8.261 ms (5%) |         |    1.26 MiB (1%) |        6183 |
| `["parallel_histogram", "seq"]`                     |   2.696 ms (5%) |         |  364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  31.680 ms (5%) |         |                  |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  15.301 ms (5%) |         |   736 bytes (1%) |          11 |
| `["splitby", "count", "foldl"]`                     |   1.208 ms (5%) |         |                  |             |
| `["splitby", "count", "man"]`                       | 712.755 μs (5%) |         |                  |             |
| `["splitby", "count", "reduce"]`                    | 637.581 μs (5%) |         |    1.06 KiB (1%) |          18 |
| `["sum", "random", "foldl"]`                        |   8.085 ms (5%) |         |                  |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   3.982 ms (5%) |         |   74.12 KiB (1%) |        1102 |
| `["sum", "random", "reduce", "basesize=256"]`       |   3.999 ms (5%) |         |   36.66 KiB (1%) |         543 |
| `["sum", "random", "reduce", "basesize=512"]`       |   3.976 ms (5%) |         |   18.05 KiB (1%) |         268 |
| `["sum", "uniform", "foldl"]`                       |   7.898 ms (5%) |         |                  |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   4.040 ms (5%) |         |   74.09 KiB (1%) |        1101 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   3.945 ms (5%) |         |   36.72 KiB (1%) |         545 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   3.976 ms (5%) |         |   18.05 KiB (1%) |         268 |
| `["sum", "valley", "foldl"]`                        |   8.013 ms (5%) |         |                  |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   4.028 ms (5%) |         |   74.12 KiB (1%) |        1102 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   4.113 ms (5%) |         |   36.75 KiB (1%) |         546 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   4.013 ms (5%) |         |   18.14 KiB (1%) |         271 |
| `["words", "nthreads=1"]`                           |   8.785 ms (5%) |         |   31.54 MiB (1%) |     1027595 |
| `["words", "nthreads=2"]`                           |   6.021 ms (5%) |         |   32.26 MiB (1%) |     1027699 |
| `["words", "nthreads=4"]`                           |   6.527 ms (5%) |         |   32.71 MiB (1%) |     1027766 |

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
  uname: Linux 7.0.0-1020-azure #21-Ubuntu SMP PREEMPT Tue Oct 27 22:34:38 UTC 2026 x86_64 unknown
  CPU: AMD EPYC 9V45 96-Core Processor: 
              speed         user         nice          sys         idle          irq
       #1  4264 MHz       3164 s          0 s        218 s       7546 s          0 s
       #2  4340 MHz       3893 s          0 s        244 s       6812 s          0 s
       #3  4243 MHz       3272 s          0 s        232 s       7460 s          0 s
       #4  4232 MHz       3880 s          0 s        247 s       6837 s          0 s
       
  Memory: 15.608436584472656 GB (13170.11328125 MB free)
  Uptime: 1101.9 sec
  Load Avg:  1.73  1.69  1.14
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, generic)
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
    Model name:                              AMD EPYC 9V45 96-Core Processor
    CPU family:                              26
    Model:                                   2
    Thread(s) per core:                      2
    Core(s) per socket:                      2
    Socket(s):                               1
    Stepping:                                1
    BogoMIPS:                                5192.24
    Flags:                                   fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush mmx fxsr sse sse2 ht syscall nx mmxext fxsr_opt pdpe1gb rdtscp lm constant_tsc rep_good nopl xtopology tsc_reliable nonstop_tsc cpuid extd_apicid aperfmperf tsc_known_freq pni pclmulqdq ssse3 fma cx16 pcid sse4_1 sse4_2 x2apic movbe popcnt aes xsave avx f16c rdrand hypervisor lahf_lm cmp_legacy svm cr8_legacy abm sse4a misalignsse 3dnowprefetch osvw topoext vmmcall fsgsbase bmi1 avx2 smep bmi2 erms invpcid avx512f avx512dq rdseed adx smap avx512ifma clflushopt clwb avx512cd sha_ni avx512bw avx512vl xsaveopt xsavec xgetbv1 xsaves user_shstk avx_vnni avx512_bf16 clzero xsaveerptr rdpru arat npt nrip_save tsc_scale vmcb_clean flushbyasid decodeassists pausefilter pfthreshold v_vmsave_vmload avx512vbmi umip avx512_vbmi2 gfni vaes vpclmulqdq avx512_vnni avx512_bitalg avx512_vpopcntdq rdpid fsrm avx512_vp2intersect
    Virtualization:                          AMD-V
    Hypervisor vendor:                       Microsoft
    Virtualization type:                     full
    L1d cache:                               96 KiB (2 instances)
    L1i cache:                               64 KiB (2 instances)
    L2 cache:                                2 MiB (2 instances)
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
    Vulnerability Tsa:                       Not affected
    Vulnerability Tsx async abort:           Not affected
    Vulnerability Vmscape:                   Not affected
    

| Cpu Property       | Value                                                      |
|:------------------ |:---------------------------------------------------------- |
| Brand              | AMD EPYC 9V45 96-Core Processor                            |
| Vendor             | :AMD                                                       |
| Architecture       | :Unknown                                                   |
| Model              | Family: 0xbf, Model: 0x02, Stepping: 0x01, Type: 0x00      |
| Cores              | 8 physical cores, 16 logical cores (on executing CPU)      |
|                    | Hyperthreading hardware capability detected                |
| Clock Frequencies  | Not supported by CPU                                       |
| Data Cache         | Level 1:3 : (48, 1024, 32768) kbytes                       |
|                    | 64 byte cache line size                                    |
| Address Size       | 48 bits virtual, 48 bits physical                          |
| SIMD               | 512 bit = 64 byte max. SIMD vector size                    |
| Time Stamp Counter | TSC is accessible via `rdtsc`                              |
|                    | TSC runs at constant rate (invariant from clock frequency) |
| Perf. Monitoring   | Performance Monitoring Counters (PMC) are not supported    |
| Hypervisor         | Yes, Microsoft                                             |

