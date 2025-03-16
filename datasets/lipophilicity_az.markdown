---
layout: default
permalink: /datasets/lipophilicity_az
---

<script id="MathJax-script" async src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js"></script>


# AZ(AstraZeneca)-lipo

**Dataset**: Download it [here](/ADMET/datasets/lipophilicity_AstraZeneca.csv). 

**Dataset description:** 4,195 compounds and their experimental measurements $\log D_{7.4}$ values, octanol-water partition coefficient at pH7.4 measured using a shake flask method, deposited by AstraZeneca in ChEMBL. 

**Dataset preprocessing** 

- Extract the raw dataset from [ChEMBL 34](https://ftp.ebi.ac.uk/pub/databases/chembl/ChEMBLdb/releases/chembl_34/) using assay ID [CHEMBL3301363](https://www.ebi.ac.uk/chembl/explore/assay/CHEMBL3301363), which contains 4,200 compounds and their ; 
- three compounds that have two $\log D_{7.4}$ values, and drop the two compounds with a large $\log D_{7.4}$ difference and take the average for the third compound.

**Reference**

1. M. Wenlock and N. Tomkinson, [Experimental in vitro DMPK and physicochemical data on a set of publicly disclosed compounds](https://doi.org/10.6019/CHEMBL3301361).
