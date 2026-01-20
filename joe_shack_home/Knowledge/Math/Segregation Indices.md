---
type:
  - Note
---

* **Creation date**: `= this.file.ctime`
* **Last modified date**: `= this.file.mtime`
* **Tags**: #information_theory #shannon_entropy #segregation


Given some contingency table with $U$ rows (units of observation e.g., schools) and $G$ columns (groupings e.g., race), a segregation index should help us understand how segregated our observations are on the basis of some grouping (e.g., schools on the basis of race).

## Measures of evenness or uniformity

The [[Mutual information|Mutual Information Index]] will the basis of our analysis. We will be also be extending the Mutual Information Index by using the [[Theil Index]]. For segregation analyses, we typically use the Theil Index and divide by the entropy of the grouping variable (e.g., race). However, some analyses also divide by the largest possible value of mutual information which could be obtained.