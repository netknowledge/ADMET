---
layout: default
permalink: /datasets/solubility_biogen
---

<script id="MathJax-script" async src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js"></script>


# Biogen-sol

**Dataset**: Download it [here](/ADMET/datasets/solubility_Biogen.csv). 

**Dataset description:** 2,173 compounds with measured solubility in $$\log S$$, released by Biogen. 

**Dataset preprocessing** 

- Download the original dataset from [here](https://github.com/molecularinformatics/Computational-ADME/blob/main/ADME_public_set_3521.csv), which contains 2,173 compounds with available solubility values in $$\log \mu \text{g}/\text{mL}$$; 
- Use [RDKit](https://www.rdkit.org) to transform the SMILES to their canonical forms (most SMILES are already canonical.); 
- Convert the unit from $$\log \mu \text{g}/\text{mL}$$ to $$\log S = \log_{10} \left( \frac{10^x}{\text{mw}} \cdot 1000 \cdot 10^{-6} \right)$$, where mw is the molecular weight calculated using [RDKit](https://www.rdkit.org). 

**Reference**

1. C. Fang, Y. Wang, R. Grater, S. Kapadnis, C. Black, P. Trapa, and S. Sciabola, Prospective validation of machine learning algorithms for absorption, distribution, metabolism, and excretion prediction: An industrial perspective, [Journal of Chemical Information and Modeling 63, 3263 (2023)](https://doi.org/10.1021/acs.jcim.3c00160). 
