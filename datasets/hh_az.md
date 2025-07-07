---
layout: default
permalink: /datasets/hh_az
---

<script id="MathJax-script" async src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js"></script>


# AZ-HH

AstraZeneca-Human Hepatocytes


**Dataset**: Download it [here](/ADMET/datasets/hepatocyte_human_AstraZeneca.csv). 

**Dataset description:** 407 compounds with logarithm of measured intrinsic clearance in human hepatocytes, deposited by AstraZeneca in ChEMBL. 

**Dataset preprocessing**

- Extract the raw dataset from [ChEMBL 34](https://ftp.ebi.ac.uk/pub/databases/chembl/ChEMBLdb/releases/chembl_34/) using assay ID [CHEMBL3301372](https://www.ebi.ac.uk/chembl/explore/assay/CHEMBL3301372); 
- Perform $$\log_{10}$$ transformation of intrinsic clearance values; 
- Drop one compound (row) with fewer than 4 atoms;

| molregno | standard_value |         standard_units | chembl_canonical_smiles |
|---------:|---------------:|-----------------------:|-------------------------|
|   222053 |          150.0 | uL.min-1.(10^6cells)-1 |                      CC |


**Reference**

1. M. Wenlock and N. Tomkinson, [Experimental in vitro DMPK and physicochemical data on a set of publicly disclosed compounds](https://doi.org/10.6019/CHEMBL3301361).
