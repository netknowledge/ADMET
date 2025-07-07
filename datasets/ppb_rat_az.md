---
layout: default
permalink: /datasets/ppb_rat_az
---

<script id="MathJax-script" async src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js"></script>


# AZ(AstraZeneca)-RPPB

**Dataset**: Download it [here](/ADMET/datasets/PPB_rat_AstraZeneca.csv). 

**Dataset description:** 717 compounds with measured logarithm of the percentage **unbound** to rat plasma protein, deposited by AstraZeneca in ChEMBL. 

**Dataset preprocessing**

- Extract the raw dataset from [ChEMBL 34](https://ftp.ebi.ac.uk/pub/databases/chembl/ChEMBLdb/releases/chembl_34/) using assay ID [CHEMBL3301366](https://www.ebi.ac.uk/chembl/explore/assay/CHEMBL3301366); 
- Convert the data from percentage bound to $$\log_{10}$$-based percentage unbound;


**Reference**

1. M. Wenlock and N. Tomkinson, [Experimental in vitro DMPK and physicochemical data on a set of publicly disclosed compounds](https://doi.org/10.6019/CHEMBL3301361).
