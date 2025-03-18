---
layout: default
permalink: /datasets/lipophilicity_az
---

<script id="MathJax-script" async src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js"></script>


# AZ(AstraZeneca)-lipo

**Dataset**: Download it [here](/ADMET/datasets/lipophilicity_AstraZeneca.csv). 

**Dataset description:** 4,195 compounds and their measured $$\log D_{7.4}$$ values, octanol-water partition coefficient at pH7.4 measured using a shake flask method, deposited by AstraZeneca in ChEMBL. 

**Dataset preprocessing** 

- Extract the raw dataset from [ChEMBL 34](https://ftp.ebi.ac.uk/pub/databases/chembl/ChEMBLdb/releases/chembl_34/) using assay ID [CHEMBL3301363](https://www.ebi.ac.uk/chembl/explore/assay/CHEMBL3301363), which contains 4,200 compounds; 
- For the 3 compounds with 2 different $$\log D_{7.4}$$ values, drop the 2 compounds (4 rows) with a large difference in $$\log D_{7.4}$$: 

| logD7.4 | canonical_smiles                                 |
|:-------:|--------------------------------------------------|
|   3.04  | CN1CCC[C@@H]1CCO[C@](C)(c1ccccc1)c1ccc(Cl)cc1    |
|   3.48  | CN1CCC[C@@H]1CCO[C@](C)(c1ccccc1)c1ccc(Cl)cc1    |
|  -0.66  | CN1[C@@H]2CC[C@H]1C[C@@H](OC(=O)C(CO)c1ccccc1)C2 |
|  -0.09  | CN1[C@@H]2CC[C@H]1C[C@@H](OC(=O)C(CO)c1ccccc1)C2 |

and take the average for the third compound:

| logD7.4 | canonical_smiles                                      |
|:-------:|-------------------------------------------------------|
|   2.16  | C=C[C@H]1CN2CC[C@H]1C[C@H]2[C@H](O)c1ccnc2ccc(OC)cc12 |
|   2.26  | C=C[C@H]1CN2CC[C@H]1C[C@H]2[C@H](O)c1ccnc2ccc(OC)cc12 |

**Reference**

1. M. Wenlock and N. Tomkinson, [Experimental in vitro DMPK and physicochemical data on a set of publicly disclosed compounds](https://doi.org/10.6019/CHEMBL3301361).
