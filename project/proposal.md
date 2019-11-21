---
layout: default_site
title: 15618 Project Proposal
---

## Lock-Free Red-Black Tree Using CAS

Our team: Shun Zhang, Guancheng Li

Check this: [Project checkpoint report](https://zhangshun97.github.io/project/checkpoint/)

---

### Summary

We are going to implement the lock-free version of red-black tree proposed by this [paper](https://www.cs.umanitoba.ca/~hacamero/Research/RBTreesKim.pdf) with multi-cores on shared address space.

### Background

- Red-black tree is widely used. In Java, the implementation of java.util.TreeMap and java.util.TreeSet uses it. In C++ STL, it is used in implementing map, multimap and multiset. It is also used in Linux Kernel for the Completely Fair Scheduler.
- With the lock-free version of red-black tree, a large amount of insertion and deletion can be executed concurrently.

### Challenges

- the insertion and deletion of red-black tree includes rotation to keep balance, which induces conflicts between operations, so it is challenging to parallelize it.
- If we simply apply a lock of the whole tree, the performance will be extremely bad because of the contention that every operation needs to acquire the lock.
- It is hard to write lock-free code.

### Resources

- [Main paper](https://www.cs.umanitoba.ca/~hacamero/Research/RBTreesKim.pdf), where this lock-free implementation is proposed
- Starter code: there are lots of implementations of conventional red-black trees, but we will probably use them as reference and write our own sequential version.
- GHC machines for running with multi-cores on shared address space

### Goals and deliverables

##### Plan to achieve

- Implement sequential version of red-black tree
- Implement lock-based red-black tree.
- Implement lock-free red-black tree using CAS
- Compare the performance of those three versions.

##### Hope to achieve

- If we finish the tasks above in advance, we are going to also implement a fine-grained lock-based red-black tree and make more tests to compare those four versions.

##### The demo

- We are going to show the speedup graph of the lock-free version and the lock-based version.
- The speedup graph will show the time it costs to complete a huge amount of operations on the tree, including various combinations of insertion and deletion.

### Platform Choice

We choose shared address space model because tree structure is easier to manipulate in single address space and usually a shared tree structure is expected. Besides, the insertion and deletion of tree is not compute-intensive so there is no reason to use message passing parallel model here. Also such tree operations are inherently not data-parallel.



### Schedule

| Week          | Plan to do                                                   | Status      |
| ------------- | ------------------------------------------------------------ | ----------- |
| 10/28 - 11/03 | project proposal, read paper, start to implement sequential red-black tree | Done        |
| 11/04 - 11/10 | about to finish sequential version and lock-based version    | Almost done |
| 11/11 - 11/17 | hopefully finish lock-free version                           | Doing       |
| 11/18 - 11/24 | time for debugging and extra plan                            |             |
| 11/25 - 12/01 | start writing report, do full experiments                    |             |
| 12/02 - 12/08 | finish final report, clean up codes                          |             |
| Extra plan    | implement fine-grained lock-based red-black tree             |             |

###  






