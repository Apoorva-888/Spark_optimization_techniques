# Spark_optimization_techniques
A curated collection of Apache Spark optimization techniques demonstrated through Google Colab examples, conceptual notes, and sample data.

## Overview
This repository showcases various techniques to optimize Spark jobs for better performance, resource efficiency, and scalability. Each technique is explained with theory and demonstrated using Google Colab notebooks exported as PDFs.


## Optimization Techniques Covered
- **Adaptive Query Execution (AQE)**
  - Dynamically optimizes query plans at runtime based on actual data statistics.
  - Benefits: Improved join strategies, optimized shuffle partition sizes, better skew handling.
  - Reference: `GoogleCollab_Adaptive_Query_Execution.pdf`
- **Broadcast Hash Join & Sort-Merge Join**
  - Broadcast small datasets to all executors to avoid costly shuffles in large joins.
  - Sort-Merge Join used when datasets are large and sorted on join keys.
  - Benefits: Reduced network I/O, faster joins.
  - Reference: `GoogleCollab_BroadcastHashJoin_SortMergeJoin.pdf`
- **Broadcast Join**
  - Special case of join optimization where one dataset fits entirely in memory.
  - Benefits: Reduced network I/O, faster joins.
  - Reference: `GoogleCollab_Broadcast_Join.pdf`
- **Caching & Persist**
  - Store frequently accessed DataFrames/RDDs in memory or on disk to avoid recomputation.
  - Benefits: Faster iterative algorithms, reduced job execution time.
  - Reference: `GoogleCollab_Caching_persist.pdf`
- **Dynamic Partition Pruning**
  - Prunes unnecessary partitions at runtime for queries with dynamic filter values.
  - Benefits: Reduced data scanning, improved query performance.
  - Reference: `GoogleCollab_Dynamic_Partition_Pruning.pdf`
- **Out of Memory (OOM) Experiment**
  - Demonstrates causes and solutions for OOM errors in Spark.
  - Benefits: Better memory management and prevention of executor failures.
  - Reference: `GoogleCollab_OOMExperiment.pdf`
- **Resolving OOM using Salting**
  - Technique to handle data skew by distributing skewed keys across multiple partitions.
  - Benefits: Balanced load across executors, reduced shuffle and memory pressure.
  - Reference: `GoogleCollab_ResolvingOOmusingSalting.pdf`

## How to Contribute
- Contributions are welcome! To propose new techniques or improvements:
- Fork the repo.
- Add your example PDF or notebook along with relevant notes.Update this README.md with the new technique.
- Submit a pull request.

## Prerequisites
- Apache Spark (compatible version)
- Python 3.x
- Required Python packages: pyspark, pandas, numpy

## Credits
Special thanks to [Ansh Lamba](https://www.youtube.com/watch?v=CY_WaxCxJco&t=8536s) for his *PySpark Optimization Full Course 2025 [Step-By-Step Guide]*, which inspired this repository.
