---
layout: default
permalink: /datasets/ppb_human_az
---

<script id="MathJax-script" async src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js"></script>


# AZ(AstraZeneca)-hPPB

**Dataset**: Download it [here](/ADMET/datasets/PPB_human_AstraZeneca.csv). 

**Dataset description:** 1,614 compounds with measured logarithm of the percentage **unbound** to human plasma protein, deposited by AstraZeneca in ChEMBL. 

**Dataset preprocessing**

- Extract the raw dataset from [ChEMBL 34](https://ftp.ebi.ac.uk/pub/databases/chembl/ChEMBLdb/releases/chembl_34/) using assay ID [CHEMBL3301365](https://www.ebi.ac.uk/chembl/explore/assay/CHEMBL3301365); 
- Convert the unit from percentage bound to $$\log_{10}$$-based percentage unbound;

**Reference**

1. M. Wenlock and N. Tomkinson, [Experimental in vitro DMPK and physicochemical data on a set of publicly disclosed compounds](https://doi.org/10.6019/CHEMBL3301361).
