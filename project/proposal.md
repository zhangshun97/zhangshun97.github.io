---
layout: default_site
title: 15618 Project Proposal
tags: cmu-course project parallel
---

## Lock-Free Red-Black Tree Using CAS

Our team: Shun Zhang, Guangcheng Li

Project URL: 

---

### Summary

We are going to implement the lock-free version of red-black tree proposed by this [paper](https://www.cs.umanitoba.ca/~hacamero/Research/RBTreesKim.pdf) with multi-cores on shared address space.

### Background

Red-black tree is widely used ...

### Challenges

- It's hard to write lock-free code.

### Resources

- [Main paper](https://www.cs.umanitoba.ca/~hacamero/Research/RBTreesKim.pdf), where this lock-free implementation is proposed
- Starter code: there are lots of implementations of conventional red-black trees, but we will probably write our own sequential version.
- GHC machines for running with multi-cores on shared address space

### Goals and deliverables

- Implement a sequential version of red-black tree
- Implement lock-free red-black tree using CAS



### Platform Choice

We choose shared address space because...



### Schedule

| Week          | Plan to do                                                   | Status |
| ------------- | ------------------------------------------------------------ | ------ |
| 10/28 - 11/03 | project proposal, read paper, start to implement sequential red-black tree |        |
| 11/04 - 11/10 | about to finish sequential version and try to start writing lock-free version |        |
| 11/11 - 11/17 | finish sequential version and hopefully finish lock-free version |        |
| 11/18 - 11/24 | time for debugging and extra plan                            |        |
| 11/25 - 12/01 | start writing report, do full experiments                    |        |
| 12/02 - 12/08 | finish final report, clean up codes                          |        |
| Extra plan    | implement lock-based red-black tree                          |        |








