``` ini

BenchmarkDotNet=v0.10.1, OS=Microsoft Windows NT 6.2.9200.0
Processor=Intel(R) Core(TM) i7-6700 CPU 3.40GHz, ProcessorCount=8
Frequency=3328120 Hz, Resolution=300.4699 ns, Timer=TSC
  [Host]     : Clr 4.0.30319.42000, 64bit RyuJIT-v4.6.1586.0
  Job-DZPVZX : Clr 4.0.30319.42000, 64bit RyuJIT-v4.6.1586.0

Platform=X64  LaunchCount=2  TargetCount=15  
WarmupCount=10  

```
     Method |           Mean |        StdErr |        StdDev | Scaled | Scaled-StdDev |  Gen 0 | Allocated |
----------- |--------------- |-------------- |-------------- |------- |-------------- |------- |---------- |
 Dictionary |    243.5642 ns |     0.7127 ns |     3.8380 ns |   1.00 |          0.00 | 0.0257 |     160 B |
    Runtime |  2,462.5431 ns |    15.6490 ns |    85.7133 ns |  10.11 |          0.38 | 1.2548 |   5.68 kB |
   MsMemory |  1,307.1531 ns |     2.8219 ns |    14.6628 ns |   5.37 |          0.10 | 0.1915 |   1.02 kB |
      Redis |  2,138.2635 ns |    12.3456 ns |    64.1494 ns |   8.78 |          0.29 | 0.0768 |    1.1 kB |
  Memcached | 96,120.9035 ns | 1,375.9735 ns | 7,409.8438 ns | 394.74 |         30.51 | 0.3255 |     13 kB |
