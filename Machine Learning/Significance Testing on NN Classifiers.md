# Demsar, 2006
* Average balanced accuracy
	* Debatable whether accuracy across datasets are really comparable
	* Susceptible to outliers
	* **Unpopular in research**
* Paired t-test
	* Only makes sense when datasets are commensurate - **Rare**
	* Requires normality of datasets to compare - Rare
	* Affected by outliers
	* Popular, but isn't good
* Wilcoxin signed ranks test
	* Non-parametric t-test
	* When t-test assumptions met (rare) > weaker than t-test
	* When t-test assumptions not met (common) > more powerful than t-test
* Sign test - Counts of wins, losses ties
	* Count number of sets on which an algorithm is an overall winner
	* Does not assume score commensurability, nor normality > **applicable to any data**
		* Can count only significant wins losses (i.e. datasets where model a performs *significantly* better than model b)
		* Actually not useful because: Demsar, 2006, page 9
* ANOVA
	* H0 - All models perform the same
	* Requires post-hoc test to identify which classifiers differ
		* Tukey - Compare all classifiers with each other
		* **Dunnett - Compare all classifiers with control**
			* E.g. base classifier and different improvements to it
		* Standard error of difference between 2 classifiers = residual variance / datasets
	* Assumptions usually violated
		* Assumes samples from normal distribution (minor problem)
		* Sphericity - Random variables do not have equal variance > massive effect on post-hoc tests
* **Friedman test**
	* Non-parametric repeated measure ANOVA
		* Less power than ANOVA when ANOVA assumption met - **But this is very rare**
	* Requires post-hoc tests if H0 rejected
		* Bonferroni-Dunn or similar
			* Controls family-wise error
			* Power greater when classifiers only compared to control and not amongst themselves
			* Easiest to compute and visualise
		* Holm step-down
			* **More powerful than Bonferroni-Dunn**
			* Demsar, 2006, end of page 12
		* Hommel Method
			* Considerably more complex than Holm
			* Perhaps marginal improvement vs Holm - Insubstantial in practice
			* Demsar, 2006, middle of page 13
	* Friedman test may detect significant difference that goes undetected by post-hoc testing - This is due to higher relative power of Friedman vs the post-hoc tests
		* Must conclude that some models differ but we cannot say which ones
	* Cannot use ANOVA or Friedman variations accounting for multiple observations per cell as random samples overlap
