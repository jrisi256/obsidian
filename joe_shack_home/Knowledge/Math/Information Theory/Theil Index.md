---
type:
  - Note
aliases:
  - theil index
---

* **Creation date**: `= this.file.ctime`
* **Last modified date**: `= this.file.mtime`
* **Tags**: #segregation #information_theory 

## Definition

The Theil Index is an expansion of the [[Mutual information|Mutual Information Index]]. It takes the Mutual Information Index and divides it by the [[Shannon entropy]] for one of the relevant variables. It can be thought of as a normalized version of the Mutual Information Index and constrains the index to be between 0 and 1.

## Intuition

Typically, segregation scholars will begin by using the Shannon entropy to describe the overall diversity of some system (e.g., a school district). A higher entropy typically means a more uniform or even distribution of groups (e.g., racial groups) across the system.

If we go back to entropy and ideas of information and surprise, when an unlikely event happens, we says that surprises us more than when a likely event happens. If every group has roughly equal probability of membership, then every outcome is equally surprising and the overall amount of uncertainty or surprise or entropy in the system is relatively high.

Of course, this measure is more akin to a *diversity index* rather than a segregation index because it does not communicate anything about how integrated or segregated the various groups (e.g., racial groups) are within each of the component units (e.g., schools) making up the whole (e.g., school district). For example, a school district could be 50% White and 50% Black (high entropy, high diversity), but it might be very segregated if every school is either all Black or all White.

We can then calculate each unit's (e.g., each schools) diversity (entropy) score. Finally, the Theil Index for segregation is the weighted average deviation of each unit's entropy from the system-wide entropy expressed as a fraction of the system-wide area's total entropy. Interpreting the index in the segregation context, if it has a value of 0, then all units have the same composition as the entire system (maximum integration). If it has a value of 1, then all units contain one group only and are thus maximally different from the system-wide composition (maximum segregation).

Scholars often call this measure a measure of *evenness* since it measures how evenly groups are distributed across the units of observation (as compared to the overall composition of all units in the system). As a result, it is not influenced by the relative sizes of the groups.
## Note

Many different fields define the Index differently and use it in slightly different ways to suit their purposes.

## Limitations

If you have a school district that is 90% White and 10% Black, and every school in that school district is 90% White and 10% Black, then the Theil Index would return a value of 0 indicating perfect integration. Common sense would tell us these schools might not be very integrated, though. We would need to be explicit, of course, in describing why we might not think the schools are very integrated. Likely, it is because it is because it is imbalanced with reference to some other population of interest (e.g., the racial distribution of people living in the school district). This intuition would need to be incorporated into the Theil Index to give it quantitative heft.