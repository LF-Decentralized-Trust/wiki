1. [Besu](index.html)
2. [Besu](Besu_22151173.html)
3. [Performance &amp; Stability](22155524.html)

# Besu : Reduce Memory usage by choosing a different low level allocator

Created by Ameziane Hamlat on Jan 18, 2024

- [Introduction](#ReduceMemoryusagebychoosingadifferentlowlevelallocator-Introduction)
- [The test setup](#ReduceMemoryusagebychoosingadifferentlowlevelallocator-Thetestsetup)
- [The metrics](#ReduceMemoryusagebychoosingadifferentlowlevelallocator-Themetrics)
  
  - [Malloc vs TcMalloc vs Jemalloc vs Mimalloc](#ReduceMemoryusagebychoosingadifferentlowlevelallocator-MallocvsTcMallocvsJemallocvsMimalloc)
  - [Malloc vs JeMalloc](#ReduceMemoryusagebychoosingadifferentlowlevelallocator-MallocvsJeMalloc)
    
    - [Resident memory utilization](#ReduceMemoryusagebychoosingadifferentlowlevelallocator-Residentmemoryutilization)
    - [Memory page faults](#ReduceMemoryusagebychoosingadifferentlowlevelallocator-Memorypagefaults)
  - [Test different values for MALLOC\_ARENA\_MAX](#ReduceMemoryusagebychoosingadifferentlowlevelallocator-TestdifferentvaluesforMALLOC_ARENA_MAX)
- [Conclusion](#ReduceMemoryusagebychoosingadifferentlowlevelallocator-Conclusion)

# Introduction

We came across an interesting feedback around RocksDB memory consumption regarding the used low level allocator. We found that for some workloads, other allocators than the default one (glibc malloc) may consume much less memory because they manage better memory fragmentation. 

Here is an interesting example : [https://blog.cloudflare.com/the-effect-of-switching-to-tcmalloc-on-rocksdb-memory-use/](https://blog.cloudflare.com/the-effect-of-switching-to-tcmalloc-on-rocksdb-memory-use/)

We then decided to test different low level allocators on Besu but also different values for MALLOC\_ARENA\_MAX. 

# The test setup

We decided to test these allocators :

- Malloc : default
- TcMalloc (Google) : [https://github.com/google/tcmalloc](https://github.com/google/tcmalloc)
- MiMalloc (Microsoft) : [https://github.com/microsoft/mimalloc](https://github.com/microsoft/mimalloc)
- JeMalloc : [https://github.com/jemalloc/jemalloc](https://github.com/jemalloc/jemalloc)

And different values for MALLOC\_ARENA\_MAX.

All the tests are done on t3.xlarge AWS instance (4 vCPU, 16 GiB) with EBS Disk.

# The metrics

## Malloc vs TcMalloc vs Jemalloc vs Mimalloc

The results show that Besu is consuming less than 5 GiB with JeMalloc and TcMalloc allocators while with Malloc Besu consumes more than 9 GiB,

![](attachments/22156632/22156633.png?height=400)

## Malloc vs JeMalloc

### Resident memory utilization

After few days of running,  Besu memory usage is around 4.8 GiB while it is around 9 GiB for Glibc Malloc.

![](attachments/22156632/22156636.png?height=400)

UPDATE : After running continuously for two months, Besu's memory usage with Jemalloc remains quite stable at around 4.8 GiB, in contrast to reaching 10 GiB when using Glibc Malloc.

![](attachments/22156632/22156635.png?width=1319)

### Memory page faults

We noticed more minor memory page faults with JeMalloc compared to Glibc Malloc. Minor page faults occur when the page is present in the memory but is not mapped properly either because of invalid mapping or data is not cleared from the page by its previous process . Minor faults are normal and fine, and rarely do the programs suffer from performance problems due to minor faults. 

**JeMalloc**

![](attachments/22156632/22156637.png?width=1319)

**Glibc Malloc**

**![](attachments/22156632/22156638.png?width=1319)**

## Test different values for MALLOC\_ARENA\_MAX

We did tests with different MALLOC\_ARENA\_MAX values: 1, 2, 4, and the default (which is 8 times the number of CPU cores on a 64-bit Linux OS). The graph below represents the results from five AWS instances:

- Instance-1: Running Besu version 22.4.2 with the default MALLOC\_ARENA\_MAX value.
- Instance-2: Running Besu version 22.4.3, also with the default MALLOC\_ARENA\_MAX value.
- Instance-3: Running Besu version 22.4.3 with MALLOC\_ARENA\_MAX set to 1.
- Instance-4: Running Besu version 22.4.3 with MALLOC\_ARENA\_MAX set to 2.
- Instance-5: Running Besu version 22.4.3 with MALLOC\_ARENA\_MAX set to 4.

The results show that Besu consumes less memory with MALLOC\_ARENA\_MAX = 1 (5.90 GiB) than the default value on version 22.4.2 (8.11 GiB) or 22.4.3 (12.1 GiB).

![](attachments/22156632/22156639.png?width=1319)

# Conclusion

The results showed that Besu with JeMalloc and TcMalloc consumes much less memory than the default Glibc malloc, 4 GiB less on 16 GiB VM.

We've also noticed that specifying MALLOC\_ARENA\_MAX to 1 or 2 reduced significantly Resident memory usage.

## Attachments:

![](images/icons/bullet_blue.gif) [image-2024-1-18\_12-12-11.png](attachments/22156632/22156633.png) (image/png)  
![](images/icons/bullet_blue.gif) [image-2024-1-18\_12-13-41.png](attachments/22156632/22156634.png) (image/png)  
![](images/icons/bullet_blue.gif) [image-2024-1-18\_12-14-58.png](attachments/22156632/22156635.png) (image/png)  
![](images/icons/bullet_blue.gif) [image-2024-1-18\_12-19-38.png](attachments/22156632/22156636.png) (image/png)  
![](images/icons/bullet_blue.gif) [image-2024-1-18\_12-25-43.png](attachments/22156632/22156637.png) (image/png)  
![](images/icons/bullet_blue.gif) [image-2024-1-18\_12-26-37.png](attachments/22156632/22156638.png) (image/png)  
![](images/icons/bullet_blue.gif) [image-2024-1-18\_12-32-38.png](attachments/22156632/22156639.png) (image/png)

Document generated by Confluence on Nov 26, 2024 13:01

[Atlassian](http://www.atlassian.com/)
