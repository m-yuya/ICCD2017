
# ICCD2017: Exploring Scalable Data Allocation and Parallel Computing on NoC-based Embedded Many Cores

## Abstract 
In embedded systems, high processing requirements and low power consumption need heterogeneous computing platforms.
Considering embedded requirements, applications need to be designed based on scalable data allocation and parallel computing with non-uniform memory access (NUMA) many cores.
In this paper, we use one of the embedded commercial off-the-shelf (COTS) multi/many-core components, the Massively Parallel Processor Arrays (MPPA) 256 developed by Kalray, and conduct evaluations of data transfer and parallelization of a practical application.
We investigate currently achievable data transfer latencies between distributed memories on network-on-chip (NoC), memory access characteristics, and parallelization potential with many cores.
Subsequently, we run a practical application, the core of the autonomous driving system, on many-core processors and acceleration by parallelization indicates practicality of many cores.
By highlighting many-core computing capabilities, we explore the scalable data allocation and parallel computing on NoC-based embedded many cores.


## How to build this repo
```shell
# Build main file
$ make
# Build main without bibtex
$ make simple
# Build main file only for dvi
$ make dvi
# Clean internal files
$ make clean
# Clean internal files including pdf
$ make realclean
```
