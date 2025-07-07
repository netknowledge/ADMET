---
layout: page
permalink: /datasets/permeability_ncats_pampa
---

<script id="MathJax-script" async src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js"></script>


# NCATS-PAMPA

**Dataset**: Download it [here](/ADMET/datasets/permeability_NCATS_PAMPA.csv). 

**Dataset description:**: 2,033 compounds with discretized PAMPA results.

**Dataset preprocessing** 

- Obtain the original dataset from [here](https://pubchem.ncbi.nlm.nih.gov/bioassay/1508612#section=Data-Table), which contains 2,530 compounds;
- Remove one compound (2 rows) with an inconsistent outcome;

| PUBCHEM_SID | PUBCHEM_CID |                                          PUBCHEM_EXT_DATASOURCE_SMILES | PUBCHEM_ACTIVITY_OUTCOME | Phenotype | Analysis Comment |
|------------:|------------:|-----------------------------------------------------------------------:|-------------------------:|----------:|-----------------:|
|    57655021 |      661788 | CC(=O)NC1=CC=C(C=C1)OCC2=C(C=CC(=C2)C3NC4=CC=CC=C4C(=O)N3CC5=CC=CO5)OC |             Inconclusive |       N/F |              NaN |
|   124888752 |      661788 | CC(=O)NC1=CC=C(C=C1)OCC2=C(C=CC(=C2)C3NC4=CC=CC=C4C(=O)N3CC5=CC=CO5)OC |                   Active |      High |        class = 0 |

- Drop one duplicated row;

| PUBCHEM_SID | PUBCHEM_CID |           PUBCHEM_EXT_DATASOURCE_SMILES | PUBCHEM_ACTIVITY_OUTCOME | Phenotype | Analysis Comment |
|------------:|------------:|----------------------------------------:|-------------------------:|----------:|------------------|
|   109967254 |   135422895 | CN=C1CN=C(C2=C(N1)C=CC(=C2)Cl)C3=CC=CN3 |                   Active |      High |        class = 0 |
|   109967255 |   135422895 | CN=C1CN=C(C2=C(N1)C=CC(=C2)Cl)C3=CC=CN3 |                   Active |      High |        class = 0 |

- Drop 494 compounds (rows) with an inconclusive outcome;
- Use [RDKit](https://www.rdkit.org) to transform the SMILES to their canonical forms;
- Generate a new column (`low_moderate_permeability`) based on the `Analysis Comment` column: `Low` and `Moderate` phenotypes are mapped to positive class; `High` negative;


**Reference**

1. H. Sun, K. Nguyen, E. Kerns, Z. Yan, K. R. Yu, P. Shah, A. Jadhav, and X. Xu, Highly predictive and interpretable models for PAMPA permeability, [Bioorganic & medicinal chemistry 25, 1266 (2017)](https://doi.org/10.1016/j.bmc.2016.12.049).
