# DWMProject

### 1. Comparison of Python vs R Agglomerative Clustering Results

| Python Cluster | Python Count | R Cluster | R Count |
|----------------|--------------|-----------|---------|
| 0              | ~5000        | 1         | ~4400   |
| 1              | ~300         | 2         | ~1100   |
| 2              | ~900         | 3         | ~2700   |
| 3              | ~2700        | 4         | ~400    |

**Observations**:

- *Primary Clusters:* Both implementations identify a dominant cluster, but Python's largest cluster (0) contains ~5000 samples while R's largest (1) has ~4400.

- *Secondary Clusters:* Interestingly, both implementations have a secondary cluster of similar size (~2700 samples) - Python's cluster 3 and R's cluster 3.

- *Smaller Clusters:* The distribution of smaller clusters differs significantly between implementations.

- *Balance:* R's implementation produces more evenly distributed clusters overall, while Python's shows more extreme concentration in the largest cluster.

These differences highlight how implementation details can significantly impact agglomerative hierarchical clustering results despite using conceptually similar algorithms.
