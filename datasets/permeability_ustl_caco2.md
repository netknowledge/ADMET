---
layout: page
permalink: /datasets/permeability_ustl_caco2
---

<script id="MathJax-script" async src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js"></script>


# USTL(University of Science and Technology Liaoning)-Caco2

**Dataset**: Download it [here](/ADMET/datasets/permeability_USTL_Caco2.csv). 

**Dataset description:** A curated dataset containing 1,780 compounds and their experimental $$\log P_{\text{app}}$$ values. 

**Dataset preprocessing** 

- Download the original dataset from [here](https://doi.org/10.1039/D0RA08209K), which contains 1,827 compounds; 
- Drop 2 duplicate rows;

| logPapp   | SMILES                                           |
|-----------|--------------------------------------------------|
| -5.521434 | ONC(=O)\C=C\c1ccc2c(c1)nc(CCc3ccccc3)n2CCN4CCCC4 |
| -5.521434 | ONC(=O)\C=C\c1ccc2c(c1)nc(CCc3ccccc3)n2CCN4CCCC4 |
| -5.100000 | O1c2c(C(=O)C=C1c1cc(OC)c(OC)c(OC)c1)c(O)cc(O)c2  |
| -5.100000 | O1c2c(C(=O)C=C1c1cc(OC)c(OC)c(OC)c1)c(O)cc(O)c2  |

- Use [RDKit](https://www.rdkit.org) to transform the SMILES to their canonical forms;
- For 28 compounds with two difference in $$\log P_{\text{app}}$$ values, drop 17 compounds (34 rows) with $$\log P_{\text{app}}$$ difference larger than 0.1:

| logPapp   | canonical_smiles                                                                                                                     |
|-----------|--------------------------------------------------------------------------------------------------------------------------------------|
| -4.590067 | CC(C(=O)O)c1cccc(C(=O)c2ccccc2)c1                                                                                                    |
| -4.707191 | CC(C(=O)O)c1cccc(C(=O)c2ccccc2)c1                                                                                                    |
| -5.657577 | CCN(CC)CCCC(C)Nc1ccnc2cc(Cl)ccc12                                                                                                    |
| -4.550000 | CCN(CC)CCCC(C)Nc1ccnc2cc(Cl)ccc12                                                                                                    |
| -5.522879 | CC[C@H]1CN2CCc3cc(OC)c(OC)cc3[C@@H]2C[C@@H]1C[C@H]1NCCc2cc(OC)c(OC)cc21                                                              |
| -5.690000 | CC[C@H]1CN2CCc3cc(OC)c(OC)cc3[C@@H]2C[C@@H]1C[C@H]1NCCc2cc(OC)c(OC)cc21                                                              |
| -3.900665 | CN(C)CCC=C1c2ccccc2CCc2ccccc21                                                                                                       |
| -4.260000 | CN(C)CCC=C1c2ccccc2CCc2ccccc21                                                                                                       |
| -4.724059 | CN1C2CC(OC(=O)C(CO)c3ccccc3)CC1C1OC12                                                                                                |
| -4.928118 | CN1C2CC(OC(=O)C(CO)c3ccccc3)CC1C1OC12                                                                                                |
| -5.610834 | CNCCC(Oc1ccc(C(F)(F)F)cc1)c1ccccc1                                                                                                   |
| -4.929962 | CNCCC(Oc1ccc(C(F)(F)F)cc1)c1ccccc1                                                                                                   |
| -4.535436 | COCCc1ccc(OCC(O)CNC(C)C)cc1                                                                                                          |
| -4.751046 | COCCc1ccc(OCC(O)CNC(C)C)cc1                                                                                                          |
| -4.610000 | COc1cc2nc(N3CCN(C(=O)C4CCCO4)CC3)nc(N)c2cc1OC                                                                                        |
| -5.090444 | COc1cc2nc(N3CCN(C(=O)C4CCCO4)CC3)nc(N)c2cc1OC                                                                                        |
| -4.644357 | COc1ccc(CCN(C)CCCC(C#N)(c2ccc(OC)c(OC)c2)C(C)C)cc1OC                                                                                 |
| -5.013228 | COc1ccc(CCN(C)CCCC(C#N)(c2ccc(OC)c(OC)c2)C(C)C)cc1OC                                                                                 |
| -6.031517 | C[C@@H](O)[C@@H]1NC(=O)[C@H](CCCCN)NC(=O)[C@@H](Cc2c[nH]c3ccccc23)NC(=O)[C@H](Cc2ccccc2)NC(=O)[C@@H]2CCCN2C(=O)[C@H](Cc2ccccc2)NC1=O |
| -6.220924 | C[C@@H](O)[C@@H]1NC(=O)[C@H](CCCCN)NC(=O)[C@@H](Cc2c[nH]c3ccccc23)NC(=O)[C@H](Cc2ccccc2)NC(=O)[C@@H]2CCCN2C(=O)[C@H](Cc2ccccc2)NC1=O |
| -4.720000 | C[C@]12C=CC(=O)C=C1CC[C@@H]1[C@@H]2[C@@H](O)C[C@@]2(C)[C@H]1CC[C@]2(O)C(=O)CO                                                        |
| -5.124939 | C[C@]12C=CC(=O)C=C1CC[C@@H]1[C@@H]2[C@@H](O)C[C@@]2(C)[C@H]1CC[C@]2(O)C(=O)CO                                                        |
| -5.468521 | Cc1c(O)cccc1C(=O)N[C@@H](CSc1ccccc1)[C@H](O)CN1C[C@H]2CCCC[C@H]2C[C@H]1C(=O)NC(C)(C)C                                                |
| -6.124939 | Cc1c(O)cccc1C(=O)N[C@@H](CSc1ccccc1)[C@H](O)CN1C[C@H]2CCCC[C@H]2C[C@H]1C(=O)NC(C)(C)C                                                |
| -5.279840 | Cc1ccccc1N1C(=O)c2cc(S(N)(=O)=O)c(Cl)cc2NC1C                                                                                         |
| -5.540608 | Cc1ccccc1N1C(=O)c2cc(S(N)(=O)=O)c(Cl)cc2NC1C                                                                                         |
| -4.572189 | Cn1c(=O)c2c(ncn2C)n(C)c1=O                                                                                                           |
| -4.345198 | Cn1c(=O)c2c(ncn2C)n(C)c1=O                                                                                                           |
| -4.680000 | NC(N)=N/N=C/c1c(Cl)cccc1Cl                                                                                                           |
| -4.363412 | NC(N)=N/N=C/c1c(Cl)cccc1Cl                                                                                                           |
| -6.059484 | O=C(O)c1cc(N=Nc2ccc(S(=O)(=O)Nc3ccccn3)cc2)ccc1O                                                                                     |
| -6.474235 | O=C(O)c1cc(N=Nc2ccc(S(=O)(=O)Nc3ccccn3)cc2)ccc1O                                                                                     |
| -7.327902 | OC[C@H]1O[C@H](OC[C@H]2O[C@H](O[C@]3(CO)O[C@H](CO)[C@@H](O)[C@@H]3O)[C@H](O)[C@@H](O)[C@@H]2O)[C@H](O)[C@@H](O)[C@H]1O               |
| -7.620000 | OC[C@H]1O[C@H](OC[C@H]2O[C@H](O[C@]3(CO)O[C@H](CO)[C@@H](O)[C@@H]3O)[C@H](O)[C@@H](O)[C@@H]2O)[C@H](O)[C@@H](O)[C@H]1O               |

- Calculate the average $$\log P_{\text{app}}$$ value for the remaining 11 compounds:

| logPapp   | canonical_smiles                                                                                                                                                               |
|-----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| -4.667562 | C=CCN1CC[C@]23c4c5ccc(O)c4O[C@H]2C(=O)CC[C@@]3(O)[C@H]1C5                                                                                                                      |
| -4.670000 | C=CCN1CC[C@]23c4c5ccc(O)c4O[C@H]2C(=O)CC[C@@]3(O)[C@H]1C5                                                                                                                      |
| -3.775545 | CC(CN1c2ccccc2Sc2ccccc21)N(C)C                                                                                                                                                 |
| -3.777772 | CC(CN1c2ccccc2Sc2ccccc21)N(C)C                                                                                                                                                 |
| -5.468521 | CC[C@H]1OC(=O)[C@H](C)[C@@H](O[C@H]2C[C@@](C)(OC)[C@@H](O)[C@H](C)O2)[C@H](C)[C@@H](O[C@@H]2O[C@H](C)C[C@H](N(C)C)[C@H]2O)[C@](C)(OC)C[C@@H](C)C(=O)[C@H](C)[C@@H](O)[C@]1(C)O |
| -5.470000 | CC[C@H]1OC(=O)[C@H](C)[C@@H](O[C@H]2C[C@@](C)(OC)[C@@H](O)[C@H](C)O2)[C@H](C)[C@@H](O[C@@H]2O[C@H](C)C[C@H](N(C)C)[C@H]2O)[C@](C)(OC)C[C@@H](C)C(=O)[C@H](C)[C@@H](O)[C@]1(C)O |
| -4.170696 | COc1ccc2[nH]c(S(=O)Cc3ncc(C)c(OC)c3C)nc2c1                                                                                                                                     |
| -4.170000 | COc1ccc2[nH]c(S(=O)Cc3ncc(C)c(OC)c3C)nc2c1                                                                                                                                     |
| -4.906578 | Cc1ccc(-c2cc(C(F)(F)F)nn2-c2ccc(S(N)(=O)=O)cc2)cc1                                                                                                                             |
| -4.860121 | Cc1ccc(-c2cc(C(F)(F)F)nn2-c2ccc(S(N)(=O)=O)cc2)cc1                                                                                                                             |
| -5.890000 | NS(=O)(=O)c1cc2c(cc1C(F)(F)F)NC(Cc1ccccc1)NS2(=O)=O                                                                                                                            |
| -5.886056 | NS(=O)(=O)c1cc2c(cc1C(F)(F)F)NC(Cc1ccccc1)NS2(=O)=O                                                                                                                            |
| -6.055517 | Nc1nc(O)c2ncn([C@@H]3C[C@H](CO)[C@H]3CO)c2n1                                                                                                                                   |
| -6.055517 | Nc1nc(O)c2ncn([C@@H]3C[C@H](CO)[C@H]3CO)c2n1                                                                                                                                   |
| -5.722753 | O=C(c1ccc(OCCN2CCCCC2)cc1)c1c(-c2ccc(O)cc2)sc2cc(O)ccc12                                                                                                                       |
| -5.645507 | O=C(c1ccc(OCCN2CCCCC2)cc1)c1c(-c2ccc(O)cc2)sc2cc(O)ccc12                                                                                                                       |
| -6.368266 | O=c1cc(-c2ccc(O)c(O)c2)oc2cc(O[C@@H]3O[C@H](CO)[C@@H](O)[C@H](O)[C@H]3O)cc(O)c12                                                                                               |
| -6.370000 | O=c1cc(-c2ccc(O)c(O)c2)oc2cc(O[C@@H]3O[C@H](CO)[C@@H](O)[C@H](O)[C@H]3O)cc(O)c12                                                                                               |
| -6.545757 | OC[C@H]1O[C@@H](O[C@@H]2[C@@H](CO)O[C@](O)(CO)[C@H]2O)[C@H](O)[C@@H](O)[C@H]1O                                                                                                 |
| -6.568636 | OC[C@H]1O[C@@H](O[C@@H]2[C@@H](CO)O[C@](O)(CO)[C@H]2O)[C@H](O)[C@@H](O)[C@H]1O                                                                                                 |
| -5.102373 | Oc1ccc(-c2cnc(-c3cccc(O)c3)o2)cc1                                                                                                                                              |
| -5.101186 | Oc1ccc(-c2cnc(-c3cccc(O)c3)o2)cc1                                                                                                                                              |

**Reference**

1. Y. Wang and X. Chen, Qspr model for caco-2 cell permeability prediction using a combination of hqpso and dual-rbf neural network, [RSC Advances 10, 42938 (2020)](https://doi.org/10.1039/D0RA08209K).
