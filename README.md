<p align="center">
  <h1 align="center"> ChampSim </h1>
  <p> ChampSim is a trace-based simulator for a microarchitecture study. You can sign up to the public mailing list by sending an empty mail to champsim+subscribe@googlegroups.com. If you have questions about how to use ChampSim, you can often receive a quicker response on the mailing list. Please reserve GitHub Issues for bugs. <p>
</p>

# Clone ChampSim repository
```
git clone https://github.com/ChampSim/ChampSim.git
```
# Cache Miss Reduction Project

## Objective

The objective of this project is to understand cache misses and propose a solution to reduce conflict misses, thereby improving hit rate, AMAT, IPC, and performance.

## Problem Statement

Given a fixed configuration of last level cache, the goal is to find a suitable remapping of addresses to cache lines to reduce conflict misses. A reduction in conflict misses will improve hit rate, AMAT, IPC, and performance.

### Remapping Solution

One proposed solution involves creating an intermediate data structure to remap addresses to new indices. For example, a two-dimensional array can be used to represent a remap table.

Example remap table for a 4 ways 8 set cache:
```
╔═══╦═══╦═══╦═══╦═══╗
║ 0 ║ 0 ║ 0 ║ 0 ║ 0 ║
╠═══╬═══╬═══╬═══╬═══╣
║ 1 ║ 1 ║ 1 ║ 1 ║ 6 ║
╠═══╬═══╬═══╬═══╬═══╣
║ 2 ║ 2 ║ 2 ║ 2 ║ 2 ║
╠═══╬═══╬═══╬═══╬═══╣
║ 3 ║ 3 ║ 3 ║ 3 ║ 3 ║
╠═══╬═══╬═══╬═══╬═══╣
║ 4 ║ 4 ║ 4 ║ 4 ║ 4 ║
╠═══╬═══╬═══╬═══╬═══╣
║ 5 ║ 5 ║ 5 ║ 5 ║ 5 ║
╠═══╬═══╬═══╬═══╬═══╣
║ 6 ║ 6 ║ 1 ║ 1 ║ 6 ║
╠═══╬═══╬═══╬═══╬═══╣
║ 7 ║ 7 ║ 7 ║ 7 ║ 7 ║
╚═══╩═══╩═══╩═══╩═══╝
```


### Cache Set Classification

Sets are classified as Very Hot, Hot, Very Cold, and Cold based on access and eviction counts.

## Stages [Versions]

### Stage 1: Simple Remap without Buffer

- Novel remapping approach.
- Performance monitored by IPC values.
- Overhead measured by Average number of tag comparisons for one memory search.


### Stage 2: Simple Remap with Buffer

- Using Buffer you can reduce the cold misses too 

### Stage 3: Potential Remap with Buffer

- Here , We have Some Potential sets that Need to be checked while remapping

  
## Team Members

| Name                     | Entry Number |
|--------------------------| -------------|
| [Prashant Kumar](https://github.com/Prashant370)            | 2022CSB1202  |
| [Pranav Dipesh Bhole](https://github.com/pranavbhole123) | 2022CSB1103  |
| [Kartikey Sahu](https://github.com/kartikeysahu987)          | 2022CSB1087  |


## Traces 

- [Traces Download Link](https://drive.google.com/drive/folders/1lxbyLJ30uXWaxK7uy_84BHyr5WjlC8Qu?usp=sharing)
- Traces must be used in compressed format only.

## Champsim Simulator

Instructions for using the Champsim Simulator are provided.

- [Champsim Download Link](https://drive.google.com/file/d/1RgT3E2AUDhLu2mxse0W6U7rG4hcGFfCx/view?usp=sharing)



