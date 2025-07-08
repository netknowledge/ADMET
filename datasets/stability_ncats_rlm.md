---
layout: default
permalink: /datasets/stability_ncats_rlm
---

<script id="MathJax-script" async src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js"></script>


# NCATS-RLM

**Dataset**: Download it [here](/ADMET/datasets/stability_NCATS_RLM.csv). 

**Dataset description:** 2,528 compounds and binary labels indicating whether they are unstable in rat liver microsomals. 

**Dataset preprocessing**

- Download the original dataset from [here](https://pubchem.ncbi.nlm.nih.gov/bioassay/1508591#section=Data-Table), which contains 2,531 records; 
- Drop one compound (2 rows) with inconsistent outcomes;

| PUBCHEM_CID |           PUBCHEM_EXT_DATASOURCE_SMILES | PUBCHEM_ACTIVITY_OUTCOME | Phenotype | Analysis Comment |
|------------:|----------------------------------------:|-------------------------:|----------:|-----------------:|
| 135422895   | CN=C1CN=C(C2=C(N1)C=CC(=C2)Cl)C3=CC=CN3 | Active                   | stable    | class = 0        |
| 135422895   | CN=C1CN=C(C2=C(N1)C=CC(=C2)Cl)C3=CC=CN3 | Inactive                 | unstable  | class = 1        |

- Drop one duplicated row;

| PUBCHEM_CID |                                          PUBCHEM_EXT_DATASOURCE_SMILES | PUBCHEM_ACTIVITY_OUTCOME | Phenotype | Analysis Comment |
|------------:|-----------------------------------------------------------------------:|-------------------------:|----------:|------------------|
| 661788      | CC(=O)NC1=CC=C(C=C1)OCC2=C(C=CC(=C2)C3NC4=CC=CC=C4C(=O)N3CC5=CC=CO5)OC | Inactive                 | unstable  | class = 1        |
| 661788      | CC(=O)NC1=CC=C(C=C1)OCC2=C(C=CC(=C2)C3NC4=CC=CC=C4C(=O)N3CC5=CC=CO5)OC | Inactive                 | unstable  | class = 1        |

- Generate a new column `unstable` based on the `Analysis Comment` column: `unstable` phenotype is mapped to positive class, `stable` negative class;
- Use [RDKit](https://www.rdkit.org) to transform the SMILES to their canonical forms;


**Reference**

1. V. B. Siramshetty, P. Shah, E. Kerns, K. Nguyen, K. R. Yu, M. Kabir, J. Williams, J. Neyra, N. Southall, D.-T. Nguyen, and X. Xu, Retrospective assessment of rat liver microsomal stability at ncats: data and qsar models, [Scientific Reports 10, 20713 (2020)](https://doi.org/10.1038/s41598-020-77327-0).
