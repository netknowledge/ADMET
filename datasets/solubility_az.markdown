---
layout: default
permalink: /datasets/solubility_az
---

<script id="MathJax-script" async src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js"></script>


# AZ(AstraZeneca)-sol

**Dataset**: Download it [here](/ADMET/datasets/solubility_AstraZeneca.csv). 

**Dataset description:** 1,763 compounds and their experimental measurements of water solubility, deposited by AstraZeneca in ChEMBL. 

**Dataset preprocessing** 

- Extract the raw dataset from [ChEMBL 34](https://ftp.ebi.ac.uk/pub/databases/chembl/ChEMBLdb/releases/chembl_34/) using assay ID [CHEMBL3301364](https://www.ebi.ac.uk/chembl/explore/assay/CHEMBL3301364); 
- Convert the unit from nM to $$\log S = \log_{10} (\text{nM} \cdot 10^{-9})$$. 

**Reference**

1. M. Wenlock and N. Tomkinson, [Experimental in vitro DMPK and physicochemical data on a set of publicly disclosed compounds](https://doi.org/10.6019/CHEMBL3301361).
