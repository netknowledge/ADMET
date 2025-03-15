---
layout: default
title: ESOL
permalink: /datasets/solubility_esol
---

<script id="MathJax-script" async src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js"></script>


# ESOL

**Dataset**: Download it [here](/ADMET/datasets/solubility_ESOL.csv).

**Dataset description:** 1,084 compounds and their measured water solubilities in $$\log S$$ ($$\log_{10}$$ based solubility in the unit of mol/L). 

**Dataset preprocessing** 

- Download the original dataset from [here](https://doi.org/10.1021/ci034243x), which contains 1,144 compounds; 
- Rename the column name from "measured log(solubility:mol/L)" to "logS";
- Drop 6 duplicated rows;

| logS  | SMILES                                      |
|:-----:|---------------------------------------------|
| -3.42 | CCOC2Oc1ccc(OS(C)(=O)=O)cc1C2(C)C           |
| -3.42 | CCOC2Oc1ccc(OS(C)(=O)=O)cc1C2(C)C           |
| -1.96 | COc1ccccc1O                                 |
| -1.96 | COc1ccccc1O                                 |
| -6.90 | ClC(Cl)=C(c1ccc(Cl)cc1)c2ccc(Cl)cc2         |
| -6.90 | ClC(Cl)=C(c1ccc(Cl)cc1)c2ccc(Cl)cc2         |
| -7.20 | ClC(Cl)C(c1ccc(Cl)cc1)c2ccc(Cl)cc2          |
| -7.20 | ClC(Cl)C(c1ccc(Cl)cc1)c2ccc(Cl)cc2          |
| -2.68 | NS(=O)(=O)c2cc1c(NC(NS1(=O)=O)C(Cl)Cl)cc2Cl |
| -2.68 | NS(=O)(=O)c2cc1c(NC(NS1(=O)=O)C(Cl)Cl)cc2Cl |
| -2.70 | Nc1ccc(cc1)c2ccc(N)cc2                      |
| -2.70 | Nc1ccc(cc1)c2ccc(N)cc2                      |

- Use [RDKit](https://www.rdkit.org) to transform the SMILES to their canonical forms;
- Drop 3 duplicated rows based on $$\log S$$ and canonical SMILES;

| logS   | SMILES                                  | canonical_SMILES                        |
|:------:|---------------------------------------- |-----------------------------------------|
| -4.400 | c1c(Br)ccc2ccccc12                      | Brc1ccc2ccccc2c1                        |
| -4.400 | Brc1ccc2ccccc2c1                        | Brc1ccc2ccccc2c1                        |
| -2.322 | O=C1NC(=O)NC(=O)C1(CC)c1ccccc1          | CCC1(c2ccccc2)C(=O)NC(=O)NC1=O          |
| -2.322 | CCC1(C(=O)NC(=O)NC1=O)c2ccccc2          | CCC1(c2ccccc2)C(=O)NC(=O)NC1=O          |
| -6.340 | CCOP(=S)(OCC)SC(CCl)N1C(=O)c2ccccc2C1=O | CCOP(=S)(OCC)SC(CCl)N1C(=O)c2ccccc2C1=O |
| -6.340 | CCOP(=S)(OCC)SC(CCl)N2C(=O)c1ccccc1C2=O | CCOP(=S)(OCC)SC(CCl)N1C(=O)c2ccccc2C1=O |

- There are 18 compounds with two diffferent $$\log S$$. Drop the 10 compounds (20 rows) with $$\log S$$ difference larger than 0.09:

| logS   | SMILES                                         | canonical_smiles                                       |
|:------:|------------------------------------------------|--------------------------------------------------------|
| -1.740 | CC12CCC(CC1)C(C)(C)O2                          | CC12CCC(CC1)C(C)(C)O2                                  |
| -1.640 | CC12CCC(CC1)C(C)(C)O2                          | CC12CCC(CC1)C(C)(C)O2                                  |
| -4.402 | CC12CCC(O)CC1CCC3C2CCC4(C)C3CCC4=O             | CC12CCC3C(CCC4CC(O)CCC43C)C1CCC2=O                     |
| -4.160 | CC34CCC1C(CCC2CC(O)CCC12C)C3CCC4=O             | CC12CCC3C(CCC4CC(O)CCC43C)C1CCC2=O                     |
| -2.658 | O=C1NC(=O)NC(=O)C1(CC)CCC(C)C                  | CCC1(CCC(C)C)C(=O)NC(=O)NC1=O                          |
| -2.468 | CCC1(CCC(C)C)C(=O)NC(=O)NC1=O                  | CCC1(CCC(C)C)C(=O)NC(=O)NC1=O                          |
| -3.561 | CCN(CC)c1c(cc(c(N)c1N(=O)=O)C(F)(F)F)N(=O)=O   | CCN(CC)c1c([N+](=O)[O-])cc(C(F)(F)F)c(N)c1[N+](=O)[O-] |
| -5.470 | CCN(CC)c1c(cc(c(N)c1N(=O)=O)C(F)(F)F)N(=O)=O   | CCN(CC)c1c([N+](=O)[O-])cc(C(F)(F)F)c(N)c1[N+](=O)[O-] |
| -2.100 | CCOC(=O)c1ccc(N)cc1                            | CCOC(=O)c1ccc(N)cc1                                    |
| -2.616 | CCOC(=O)c1ccc(N)cc1                            | CCOC(=O)c1ccc(N)cc1                                    |
| -3.430 | CN(C)C(=O)Nc1cccc(c1)C(F)(F)F                  | CN(C)C(=O)Nc1cccc(C(F)(F)F)c1                          |
| -3.320 | CN(C)C(=O)Nc1cccc(c1)C(F)(F)F                  | CN(C)C(=O)Nc1cccc(C(F)(F)F)c1                          |
| -6.290 | ClC4=C(Cl)C5(Cl)C3C1CC(C2OC12)C3C4(Cl)C5(Cl)Cl | ClC1=C(Cl)C2(Cl)C3C4CC(C5OC45)C3C1(Cl)C2(Cl)Cl         |
| -6.180 | ClC4=C(Cl)C5(Cl)C3C1CC(C2OC12)C3C4(Cl)C5(Cl)Cl | ClC1=C(Cl)C2(Cl)C3C4CC(C5OC45)C3C1(Cl)C2(Cl)Cl         |
| -3.535 | C2c1ccccc1N(CCF)C(=O)c3ccccc23                 | O=C1c2ccccc2Cc2ccccc2N1CCF                             |
| -4.799 | C2c1ccccc1N(CCF)C(=O)c3ccccc23                 | O=C1c2ccccc2Cc2ccccc2N1CCF                             |
|  0.060 | OCC(O)C(O)C(O)C(O)CO                           | OCC(O)C(O)C(O)C(O)CO                                   |
|  1.090 | OCC(O)C(O)C(O)C(O)CO                           | OCC(O)C(O)C(O)C(O)CO                                   |
| -0.244 | OCC1OC(OC2C(O)C(O)C(O)OC2CO)C(O)C(O)C1O        | OCC1OC(OC2C(CO)OC(O)C(O)C2O)C(O)C(O)C1O                |
|  0.358 | OCC1OC(OC2C(O)C(O)C(O)OC2CO)C(O)C(O)C1O        | OCC1OC(OC2C(CO)OC(O)C(O)C2O)C(O)C(O)C1O                |

and calculate the average $$\log S$$ for the remaining 8 compounds:

| logS   | SMILES                      | canonical_smiles            |
|:------:|-----------------------------|-----------------------------|
| -0.720 | CCC(C)CCO                   | CCC(C)CCO                   |
| -0.710 | CCC(C)CCO                   | CCC(C)CCO                   |
| -2.148 | O=C1NC(=O)NC(=O)C1(CC)C(C)C | CCC1(C(C)C)C(=O)NC(=O)NC1=O |
| -2.210 | CCC1(C(C)C)C(=O)NC(=O)NC1=O | CCC1(C(C)C)C(=O)NC(=O)NC1=O |
| -3.460 | CN(C)C(=O)Nc1ccc(C)c(Cl)c1  | Cc1ccc(NC(=O)N(C)C)cc1Cl    |
| -3.483 | CN(C)C(=O)Nc1ccc(C)c(Cl)c1  | Cc1ccc(NC(=O)N(C)C)cc1Cl    |
| -1.260 | Cc1ncc(N(=O)=O)n1CCO        | Cc1ncc([N+](=O)[O-])n1CCO   |
| -1.220 | Cc1ncc(N(=O)=O)n1CCO        | Cc1ncc([N+](=O)[O-])n1CCO   |
| -6.270 | Clc1ccc(cc1)c2cc(Cl)ccc2Cl  | Clc1ccc(-c2cc(Cl)ccc2Cl)cc1 |
| -6.250 | Clc1ccc(cc1)c2cc(Cl)ccc2Cl  | Clc1ccc(-c2cc(Cl)ccc2Cl)cc1 |
| -6.290 | Clc1ccc(cc1)c2cccc(Cl)c2Cl  | Clc1ccc(-c2cccc(Cl)c2Cl)cc1 |
| -6.260 | Clc1ccc(cc1)c2cccc(Cl)c2Cl  | Clc1ccc(-c2cccc(Cl)c2Cl)cc1 |
| -5.280 | Clc1ccc(cc1)c2ccccc2Cl      | Clc1ccc(-c2ccccc2Cl)cc1     |
| -5.250 | Clc1ccc(cc1)c2ccccc2Cl      | Clc1ccc(-c2ccccc2Cl)cc1     |
| -1.820 | NC(=O)c1ccccc1O             | NC(=O)c1ccccc1O             |
| -1.836 | NC(=O)c1ccccc1O             | NC(=O)c1ccccc1O             |

- Drop 23 compounds with fewer than 4 atoms. 

|  logS | canonical_smiles |
|:-----:|------------------|
|  0.26 | CC#N             |
| -0.89 | ClCBr            |
| -1.09 | CCBr             |
| -0.79 | CBr              |
| -1.06 | CCCl             |
| -1.75 | C=CCl            |
| -1.17 | BrCBr            |
| -0.63 | ClCCl            |
| -2.34 | ICI              |
| -0.45 | CSC              |
| -1.36 | CC               |
| -0.60 | CCS              |
|  1.10 | CCO              |
| -0.40 | C=C              |
|  0.29 | C#C              |
| -1.60 | CCI              |
| -1.00 | CI               |
| -0.90 | C                |
|  1.57 | CO               |
|  1.34 | CNN              |
| -1.94 | CCC              |
| -1.08 | C=CC             |
| -0.41 | C#CC             |


**Reference**

1. J. S. Delaney, ESOL: estimating aqueous solubility directly from molecular structure, [Journal
of Chemical Information and Computer Sciences 44, 1000 (2004)](https://doi.org/10.1021/ci034243x).
