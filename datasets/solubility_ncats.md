---
layout: default
permalink: /datasets/solubility_ncats
---

<script id="MathJax-script" async src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js"></script>


# NCATS-sol

**Dataset**: Download it [here](/ADMET/datasets/solubility_NCATS.csv). 

**Dataset description:** 2,453 compounds and binary labels indicating whether they have low solubility. 

**Dataset preprocessing**

- Download the original dataset from [here](https://pubchem.ncbi.nlm.nih.gov/bioassay/1645848#section=Data-Table), which contains 2,532 records; 
- Drop one compound (2 rows) with inconsistent outcomes;

| PUBCHEM_CID |                                          PUBCHEM_EXT_DATASOURCE_SMILES | PUBCHEM_ACTIVITY_OUTCOME |     Phenotype | Analysis Comment |
|------------:|-----------------------------------------------------------------------:|-------------------------:|--------------:|-----------------:|
| 661788      | CC(=O)NC1=CC=C(C=C1)OCC2=C(C=CC(=C2)C3NC4=CC=CC=C4C(=O)N3CC5=CC=CO5)OC | Active                   | Moderate/High | class = 0        |
| 661788      | CC(=O)NC1=CC=C(C=C1)OCC2=C(C=CC(=C2)C3NC4=CC=CC=C4C(=O)N3CC5=CC=CO5)OC | Inactive                 | Low           | class = 1        |

- Drop one duplicated row;

| PUBCHEM_CID |           PUBCHEM_EXT_DATASOURCE_SMILES | PUBCHEM_ACTIVITY_OUTCOME |     Phenotype | Analysis Comment |
|------------:|----------------------------------------:|-------------------------:|--------------:|-----------------:|
| 135422895   | CN=C1CN=C(C2=C(N1)C=CC(=C2)Cl)C3=CC=CN3 | Active                   | Moderate/High | class = 0        |
| 135422895   | CN=C1CN=C(C2=C(N1)C=CC(=C2)Cl)C3=CC=CN3 | Active                   | Moderate/High | class = 0        |

- Drop 76 compounds (rows) with an inconclusive outcome;
- Generate a new column `low_solubility` based on the `Analysis Comment` column: `Low` phenotype is mapped to positive class, `Moderate/High` negative class;
- Use [RDKit](https://www.rdkit.org) to transform the SMILES to their canonical forms;


**Reference**

1. H. Sun, P. Shah, K. Nguyen, K. R. Yu, E. Kerns, M. Kabir, Y. Wang, and X. Xu, Predictive models of aqueous solubility of organic compounds built on a large dataset of high integrity, [Bioorganic & Medicinal Chemistry 27, 3110 (2019)](https://doi.org/10.1016/j.bmc.2019.05.037).
