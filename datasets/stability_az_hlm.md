---
layout: default
permalink: /datasets/stability_az_hlm
---

<script id="MathJax-script" async src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js"></script>


# AZ-HLM

AstraZeneca-Human Liver Microsomes


**Dataset**: Download it [here](/ADMET/datasets/stability_AstraZeneca_HLM.csv). 

**Dataset description:** 1102 compounds with logarithm of measured intrinsic clearance in human liver microsomes, deposited by AstraZeneca in ChEMBL. 

**Dataset preprocessing**

- Extract the raw dataset from [ChEMBL 34](https://ftp.ebi.ac.uk/pub/databases/chembl/ChEMBLdb/releases/chembl_34/) using assay ID [CHEMBL3301370](https://www.ebi.ac.uk/chembl/explore/assay/CHEMBL3301370); 
- Perform $$\log_{10}$$ transformation of intrinsic clearance values; 


**Reference**

1. M. Wenlock and N. Tomkinson, [Experimental in vitro DMPK and physicochemical data on a set of publicly disclosed compounds](https://doi.org/10.6019/CHEMBL3301361).
