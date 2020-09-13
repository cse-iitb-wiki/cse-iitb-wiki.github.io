---
layout: post
title: State of High Performance Computing
categories: [GPU, Compute]
author: Vihari Piratla, Diptesh Kanojia, Sabyasachi Ghosh
---

## GPUs
### SpaceTime
Computer Center (CC) provides access to 64 GPU nodes with P100 (these are decent GPUs at the time of this post). You can know more about the facility called SpaceTime at this (IITB internal) [link](https://spacetime.iitb.ac.in/).


SpaceTime has 64 GPU P100 (16GB, cutting-edge) nodes.  
Your faculty must create an account for you to be able to access the facility. 
You should submit your job through PBS. The typical queue wait time for your process is around **12-24 hrs**. There is also an upper limit to how long your process can run (do not know what).  

It is not straight-forward to use PBS to submit jobs, a steep learning curve: software, libraries, debugging, MPI threads, code changes, arch., network adaptations etc. The provided manuals are no match for the needed support.

### Painless PBS
Submitting jobs to a server through PBS can be taxing especially if you are a beginner. The following interfaces to PBS somewhat easier. 

The **Dask library** for distributed computing in python provides a [PBS backend](https://jobqueue.dask.org/en/latest/generated/dask_jobqueue.PBSCluster.html). It should allow you to transparently run jobs on PBS, without worrying too much about the internal details. It also supports other backends, such as threads, processes, and SSH cluster. 

Similar support is available for Julia using the [Distributed](https://docs.julialang.org/en/v1/stdlib/Distributed/) library. 

## Distributed Computing with CPU  
CC hosts around 100 low-end SL machines. Since they are conected to the common NTFS server, it is easy to setup distributed compute on the shared memory and several machines.  
If your task can be parallelized on CPUs, you should consider this. You may create an ssh cluster with the sl2 lab machines. Hostnames of sl2 machines are `sl2-<num>.cse.iitb.ac.in` e.g. `sl2-58.cse.iitb.ac.in` where `num` spans the range `[1-110]` almost wholly. 
