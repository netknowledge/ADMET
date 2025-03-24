---
layout: default
permalink: /datasets/stability_biogen_rlm
---

<script id="MathJax-script" async src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js"></script>


# Biogen-RLM

**Dataset**: Download it [here](/ADMET/datasets/stability_Biogen_RLM.csv). 

**Dataset description:** 3,054 compounds with measured logarithm of intrinsic clearance ($$\log \text{CL}_\text{int}$$) in the unit of mL/min/kg, released by Biogen. 

**Dataset preprocessing** 

- Download the original dataset from [here](https://github.com/molecularinformatics/Computational-ADME/blob/main/ADME_public_set_3521.csv), which contains 3,054 compounds with available measurements; 
- Use [RDKit](https://www.rdkit.org) to transform the SMILES to their canonical forms (most SMILES are already canonical.); 

**Reference**

1. C. Fang, Y. Wang, R. Grater, S. Kapadnis, C. Black, P. Trapa, and S. Sciabola, Prospective validation of machine learning algorithms for absorption, distribution, metabolism, and excretion prediction: An industrial perspective, [Journal of Chemical Information and Modeling 63, 3263 (2023)](https://doi.org/10.1021/acs.jcim.3c00160). 
