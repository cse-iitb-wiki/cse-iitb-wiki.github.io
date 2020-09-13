---
layout: post
title: State of High Performance Computing at IITB
categories: [GPU, Compute]
author: Vihari Piratla, Diptesh Kanojia
---

## GPUs
Computer Center (CC) provides access to 64 GPU nodes with P100 (these are decent GPUs at the time of this post). You can know more about the facility at this [link](https://spacetime.iitb.ac.in/).

SpaceTime summary (thanks to Diptesh) -- hope it helps anyone else.
SpaceTime has 64 GPU P100 (16GB, cutting-edge) nodes. 
Your faculty must create an account for you to be able to access the facility. 
You should submit your job through PBS. The typical queue wait time for your process to even begin is around 12-24 hrs. There is also an upper limit to how long your process can run (do not know what).
Not straight-forward to use PBS to submit jobs, a steep learning curve: software, libraries, support, debugging, MPI threads, code changes, arch., network adaptations etc. The provided manuals are no match for the needed support.
