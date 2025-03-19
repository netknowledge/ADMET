---
layout: page
permalink: /datasets/permeability_csu_caco2
---

<script id="MathJax-script" async src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js"></script>


# CSU(Central South University)-Caco2

**Dataset**: Download it [here](/ADMET/datasets/). 

**Dataset description:** 1,018 compounds a curated dataset containing experimental values of $$\log P_{\text{app}}$$.  

**Dataset preprocessing** 

- Obtain the raw dataset from [here](https://pubs.acs.org/doi/10.1021/acs.jcim.5b00642), which contains 1,272 compounds;
- Remove duplicate entries based on SMILES string and $\log P_{\text{app}}$ values
- Excluding one compound with fewer than four atoms
- Calculate the average $\log P_{\text{app}}$ value for SMILES with more than one $\log P_{\text{app}}$ value.

**Reference**

1. N.-N. Wang, J. Dong, Y.-H. Deng, M.-F. Zhu, M. Wen, Z.-J. Yao, A.-P. Lu, J.-B. Wang, and D.-S. Cao, Adme properties evaluation in drug discovery: prediction of caco-2 cell permeability using a combination of nsga-ii and boosting, [Journal of Chemical Information and Modeling
56, 763 (2016)](https://doi.org/10.1021/acs.jcim.5b00642).
