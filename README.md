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


### 2. Spam Email Classification Model Performance Comparison: Python vs R

| Metric      | SVM (Python) | SVM (R)     | Random Forest (Python) | Random Forest (R) |
|-------------|--------------|-------------|--------------------------|--------------------|
| Accuracy    | 98.91%       | 50.00%      | 99.02%                   | 98.60%             |
| Precision   | 99.68%       | 50.00%      | 99.89%                   | 99.79%             |
| Recall      | 98.13%       | 100.00%     | 98.13%                   | 97.41%             |
| F1 Score    | 98.90%       | 66.67%      | 99.01%                   | 98.58%             |

---

**Observations**:

*Random Forest*:
- Consistently performs well in both environments.
- Slight differences are expected due to implementation nuances between `sklearn` (Python) and `randomForest` (R).
- Very high precision and recall, indicating robustness in detecting both spam and ham messages.

*SVM Performance*:
- SVM performance in R is significantly worse (accuracy = 50%, precision = 50%), suggesting:
  - Possible issue with **text preprocessing** or **feature alignment**.
  - Potential model **underfitting** due to improper weighting, kernel choice, or missing text normalization.

