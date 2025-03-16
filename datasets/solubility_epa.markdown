---
layout: default
permalink: /datasets/solubility_epa
---

<script id="MathJax-script" async src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js"></script>


# EPA-sol

**Dataset**: Download it [here](/ADMET/datasets/solubility_EPA.csv).

**Dataset description:** 10,093 compounds and their measured water solubilities in $$\log S$$. 

**Dataset preprocessing** 

- Download the original dataset from [here](https://doi.org/10.1021/acs.chemrestox.2c00379), which contains a training set of 7,655 compounds and a test set of 2,552 compounds (10,207 in total);
- Use [RDKit](https://www.rdkit.org) to transform the SMILES to their canonical forms;
- Remove 9 duplicated rows based on "median_WS" and canonical SMILES;

| median_WS | Standardized_SMILES                                                          | canonical_smiles                                                         |
|:---------:|------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| -4.260836 | CN(C)C(C)CN1C2=CC=CC=C2SC2C=CC=CC1=2                                         | CC(CN1c2ccccc2Sc2ccccc21)N(C)C                                           |
| -4.260836 | CN(C)C(C)CN1C2C=CC=CC=2SC2C=CC=CC1=2                                         | CC(CN1c2ccccc2Sc2ccccc21)N(C)C                                           |
| -3.371020 | CC1CN(CC(C)N1)C1=C(F)C2=C(C(N)=C1F)C(=O)C(=CN2C1CC1)C(O)=O                   | CC1CN(c2c(F)c(N)c3c(=O)c(C(=O)O)cn(C4CC4)c3c2F)CC(C)N1                   |
| -3.371020 | CC1CN(CC(C)N1)C1C(F)=C2C(=C(N)C=1F)C(=O)C(=CN2C1CC1)C(O)=O                   | CC1CN(c2c(F)c(N)c3c(=O)c(C(=O)O)cn(C4CC4)c3c2F)CC(C)N1                   |
| -3.570223 | CC(OC1=CC=CC2=CC=CC=C21)C(=O)N(CC)CC                                         | CCN(CC)C(=O)C(C)Oc1cccc2ccccc12                                          |
| -3.570223 | CC(OC1C=CC=C2C=CC=CC2=1)C(=O)N(CC)CC                                         | CCN(CC)C(=O)C(C)Oc1cccc2ccccc12                                          |
| -4.272675 | CC1=NN(C2=CC(CC(Cl)C(=O)OCC)=C(Cl)C=C2F)C(=O)N1C(F)F                         | CCOC(=O)C(Cl)Cc1cc(-n2nc(C)n(C(F)F)c2=O)c(F)cc1Cl                        |
| -4.272675 | CC1=NN(C2C=C(CC(Cl)C(=O)OCC)C(Cl)=CC=2F)C(=O)N1C(F)F                         | CCOC(=O)C(Cl)Cc1cc(-n2nc(C)n(C(F)F)c2=O)c(F)cc1Cl                        |
| -4.109436 | COC1=CC=C2C(OC(=O)C2=C1OC)C1C2C=C3OCOC3=CC=2CCN1C                            | COc1ccc2c(c1OC)C(=O)OC2C1c2cc3c(cc2CCN1C)OCO3                            |
| -4.109436 | COC1C2C(=O)OC(C3C4C=C5OCOC5=CC=4CCN3C)C=2C=CC=1OC                            | COc1ccc2c(c1OC)C(=O)OC2C1c2cc3c(cc2CCN1C)OCO3                            |
| -2.663338 | CC1OC(CC(N)C1O)OC1CC(O)(CC2=C1C(O)=C1C(=O)C3=C(C=CC=C3C(=O)C1=C2O)OC)C(=O)CO | COc1cccc2c1C(=O)c1c(O)c3c(c(O)c1C2=O)CC(O)(C(=O)CO)CC3OC1CC(N)C(O)C(C)O1 |
| -2.663338 | CC1OC(CC(N)C1O)OC1CC(O)(CC2C1=C(O)C1C(=O)C3=C(C=CC=C3C(=O)C=1C=2O)OC)C(=O)CO | COc1cccc2c1C(=O)c1c(O)c3c(c(O)c1C2=O)CC(O)(C(=O)CO)CC3OC1CC(N)C(O)C(C)O1 |
| -3.591281 | NS(=O)(=O)C1=CC2=C(C=C1C(F)(F)F)NC(CC1=CC=CC=C1)NS2(=O)=O                    | NS(=O)(=O)c1cc2c(cc1C(F)(F)F)NC(Cc1ccccc1)NS2(=O)=O                      |
| -3.591281 | NS(=O)(=O)C1C=C2C(=CC=1C(F)(F)F)NC(CC1=CC=CC=C1)NS2(=O)=O                    | NS(=O)(=O)c1cc2c(cc1C(F)(F)F)NC(Cc1ccccc1)NS2(=O)=O                      |
| -2.679618 | O=C1CCC(C(=O)N1)N1C(=O)C2C=CC=CC=2C1=O                                       | O=C1CCC(N2C(=O)c3ccccc3C2=O)C(=O)N1                                      |
| -2.679618 | O=C1CCC(C(=O)N1)N1C(=O)C2=CC=CC=C2C1=O                                       | O=C1CCC(N2C(=O)c3ccccc3C2=O)C(=O)N1                                      |
| -3.368405 | OC(CN1C=NC=N1)(C1C=CC=CC=1F)C1C=CC(F)=CC=1                                   | OC(Cn1cncn1)(c1ccc(F)cc1)c1ccccc1F                                       |
| -3.368405 | OC(CN1C=NC=N1)(C1=CC=CC=C1F)C1C=CC(F)=CC=1                                   | OC(Cn1cncn1)(c1ccc(F)cc1)c1ccccc1F                                       |

- For the 36 compounds with two diffferent solubility values, drop the 18 compounds (36 rows) with solubility difference larger than 0.1:

| median_WS | Standardized_SMILES                                                   | canonical_smiles                                             |
|:---------:|-----------------------------------------------------------------------|--------------------------------------------------------------|
| -1.619627 | CC(C)(C)NCC(O)COC1=CC=CC=C1C1CCCC1                                    | CC(C)(C)NCC(O)COc1ccccc1C1CCCC1                              |
| -1.840260 | CC(C)(C)NCC(O)COC1C=CC=CC=1C1CCCC1                                    | CC(C)(C)NCC(O)COc1ccccc1C1CCCC1                              |
| -8.002529 | CC(C)C(NC1C=CC(=CC=1Cl)C(F)(F)F)C(=O)OC(C#N)C1C=C(C=CC=1)OC1C=CC=CC=1 | CC(C)C(Nc1ccc(C(F)(F)F)cc1Cl)C(=O)OC(C#N)c1cccc(Oc2ccccc2)c1 |
| -8.344296 | CC(C)C(NC1C=CC(=CC=1Cl)C(F)(F)F)C(=O)OC(C#N)C1C=CC=C(C=1)OC1C=CC=CC=1 | CC(C)C(Nc1ccc(C(F)(F)F)cc1Cl)C(=O)OC(C#N)c1cccc(Oc2ccccc2)c1 |
| -4.394861 | CC(C)OC(=O)C(C)N(C1=CC(Cl)=C(F)C=C1)C(=O)C1C=CC=CC=1                  | CC(C)OC(=O)C(C)N(C(=O)c1ccccc1)c1ccc(F)c(Cl)c1               |
| -4.561000 | CC(C)OC(=O)C(C)N(C1C=C(Cl)C(F)=CC=1)C(=O)C1C=CC=CC=1                  | CC(C)OC(=O)C(C)N(C(=O)c1ccccc1)c1ccc(F)c(Cl)c1               |
| -3.129500 | CC(OC1=CC(Cl)=C(Cl)C=C1Cl)C(O)=O                                      | CC(Oc1cc(Cl)c(Cl)cc1Cl)C(=O)O                                |
| -3.448321 | CC(OC1C=C(Cl)C(Cl)=CC=1Cl)C(O)=O                                      | CC(Oc1cc(Cl)c(Cl)cc1Cl)C(=O)O                                |
| -8.180311 | CC1(C)C(C1C=C(Cl)C(F)(F)F)C(=O)OC(C#N)C1C=CC=C(C=1)OC1C=CC=CC=1       | CC1(C)C(C=C(Cl)C(F)(F)F)C1C(=O)OC(C#N)c1cccc(Oc2ccccc2)c1    |
| -9.677296 | CC1(C)C(C1C=C(Cl)C(F)(F)F)C(=O)OC(C#N)C1C=C(C=CC=1)OC1C=CC=CC=1       | CC1(C)C(C=C(Cl)C(F)(F)F)C1C(=O)OC(C#N)c1cccc(Oc2ccccc2)c1    |
| -6.639761 | CC1(C)C(C1C=C(Cl)Cl)C(=O)OCC1C=C(C=CC=1)OC1C=CC=CC=1                  | CC1(C)C(C=C(Cl)Cl)C1C(=O)OCc1cccc(Oc2ccccc2)c1               |
| -6.290000 | CC1(C)C(C1C=C(Cl)Cl)C(=O)OCC1C=CC=C(C=1)OC1C=CC=CC=1                  | CC1(C)C(C=C(Cl)Cl)C1C(=O)OCc1cccc(Oc2ccccc2)c1               |
| -5.889709 | COC(=O)C1C(C(C(=O)OCC)C(C)=NC=1C)C1=CC=CC(Cl)=C1Cl                    | CCOC(=O)C1C(C)=NC(C)=C(C(=O)OC)C1c1cccc(Cl)c1Cl              |
| -6.559308 | COC(=O)C1C(C(C(=O)OCC)C(C)=NC=1C)C1C=CC=C(Cl)C=1Cl                    | CCOC(=O)C1C(C)=NC(C)=C(C(=O)OC)C1c1cccc(Cl)c1Cl              |
| -2.523381 | CCOC1C=CC=CC=1C=CC(O)=O                                               | CCOc1ccccc1C=CC(=O)O                                         |
| -2.924196 | CCOC1=CC=CC=C1C=CC(O)=O                                               | CCOc1ccccc1C=CC(=O)O                                         |
| -2.545239 | CN(C)CCC(C1C=CC=CN=1)C1C=CC(Cl)=CC=1                                  | CN(C)CCC(c1ccc(Cl)cc1)c1ccccn1                               |
| -2.670000 | CN(C)CCC(C1=CC=CC=N1)C1C=CC(Cl)=CC=1                                  | CN(C)CCC(c1ccc(Cl)cc1)c1ccccn1                               |
| -3.856203 | CN(C)CCC=C1C2C=CC=CC=2COC2C=CC=CC=21                                  | CN(C)CCC=C1c2ccccc2COc2ccccc21                               |
| -3.400877 | CN(C)CCC=C1C2=CC=CC=C2COC2C=CC=CC=21                                  | CN(C)CCC=C1c2ccccc2COc2ccccc21                               |
| -3.424487 | CN(CC1C=NC2N=C(N)N=C(N)C=2N=1)C1C=CC(=CC=1)C(=O)NC(CCC(O)=O)C(O)=O    | CN(Cc1cnc2nc(N)nc(N)c2n1)c1ccc(C(=O)NC(CCC(=O)O)C(=O)O)cc1   |
| -4.000427 | CN(CC1=CN=C2N=C(N)N=C(N)C2=N1)C1C=CC(=CC=1)C(=O)NC(CCC(O)=O)C(O)=O    | CN(Cc1cnc2nc(N)nc(N)c2n1)c1ccc(C(=O)NC(CCC(=O)O)C(=O)O)cc1   |
| -3.140641 | CON=C(CC1C=NC=CC=1)C1C=CC(Cl)=CC=1Cl                                  | CON=C(Cc1cccnc1)c1ccc(Cl)cc1Cl                               |
| -3.291081 | CON=C(CC1=CN=CC=C1)C1C=CC(Cl)=CC=1Cl                                  | CON=C(Cc1cccnc1)c1ccc(Cl)cc1Cl                               |
| -4.171919 | CN(CCCC(C#N)(C(C)C)C1C=C(OC)C(=CC=1)OC)CCC1C=C(OC)C(=CC=1)OC          | COc1ccc(CCN(C)CCCC(C#N)(c2ccc(OC)c(OC)c2)C(C)C)cc1OC         |
| -3.975495 | CN(CCCC(C#N)(C(C)C)C1=CC(OC)=C(C=C1)OC)CCC1C=C(OC)C(=CC=1)OC          | COc1ccc(CCN(C)CCCC(C#N)(c2ccc(OC)c(OC)c2)C(C)C)cc1OC         |
| -4.260000 | COC1C=CC=CC=1OCCNCC(O)COC1=CC=CC2NC3C=CC=CC=3C=21                     | COc1ccccc1OCCNCC(O)COc1cccc2[nH]c3ccccc3c12                  |
| -6.146643 | COC1=CC=CC=C1OCCNCC(O)COC1=CC=CC2NC3=CC=CC=C3C=21                     | COc1ccccc1OCCNCC(O)COc1cccc2[nH]c3ccccc3c12                  |
| -2.549976 | CC1=CC(Cl)=CC=C1OC(C)C(O)=O                                           | Cc1cc(Cl)ccc1OC(C)C(=O)O                                     |
| -2.431634 | CC1C=C(Cl)C=CC=1OC(C)C(O)=O                                           | Cc1cc(Cl)ccc1OC(C)C(=O)O                                     |
| -2.690526 | FC1C=C2CCC(OC2=CC=1)C1CO1                                             | Fc1ccc2c(c1)CCC(C1CO1)O2                                     |
| -2.559907 | FC1=CC2CCC(OC=2C=C1)C1CO1                                             | Fc1ccc2c(c1)CCC(C1CO1)O2                                     |
| -5.187179 | O=C1CCC(CC1)C1CCC(CC1)C1=CC(F)=C(F)C=C1                               | O=C1CCC(C2CCC(c3ccc(F)c(F)c3)CC2)CC1                         |
| -5.863873 | O=C1CCC(CC1)C1CCC(CC1)C1C=C(F)C(F)=CC=1                               | O=C1CCC(C2CCC(c3ccc(F)c(F)c3)CC2)CC1                         |
| -4.375283 | OC(CNCC1=CC=CC=C1)C1CCC2=CC(F)=CC=C2O1                                | OC(CNCc1ccccc1)C1CCc2cc(F)ccc2O1                             |
| -3.900448 | OC(CNCC1=CC=CC=C1)C1CCC2C=C(F)C=CC=2O1                                | OC(CNCc1ccccc1)C1CCc2cc(F)ccc2O1                             |

and calculate the average solubility for the remaining 18 compounds:

| median_WS | Standardized_SMILES                                                  | canonical_smiles                                                    |
|:---------:|----------------------------------------------------------------------|---------------------------------------------------------------------|
| -2.801135 | COC1C=CC2=NC=CC(C(O)C3CC4CCN3CC4C=C)=C2C=1                           | C=CC1CN2CCC1CC2C(O)c1ccnc2ccc(OC)cc12                               |
| -2.786837 | COC1=CC=C2N=CC=C(C(O)C3CC4CCN3CC4C=C)C2=C1                           | C=CC1CN2CCC1CC2C(O)c1ccnc2ccc(OC)cc12                               |
| -3.090537 | C=CC1CN2CCC1CC2C(O)C1=CC=NC2C=CC=CC1=2                               | C=CC1CN2CCC1CC2C(O)c1ccnc2ccccc12                                   |
| -3.069261 | C=CC1CN2CCC1CC2C(O)C1=CC=NC2=CC=CC=C21                               | C=CC1CN2CCC1CC2C(O)c1ccnc2ccccc12                                   |
| -5.840410 | CC(=O)CC(C1=C(O)C2=CC=CC=C2OC1=O)C1C=CC(Cl)=CC=1                     | CC(=O)CC(c1ccc(Cl)cc1)c1c(O)c2ccccc2oc1=O                           |
| -5.837352 | CC(=O)CC(C1=C(O)C2C=CC=CC=2OC1=O)C1C=CC(Cl)=CC=1                     | CC(=O)CC(c1ccc(Cl)cc1)c1c(O)c2ccccc2oc1=O                           |
| -2.312200 | CC(=O)NC(CC1=CNC2C=CC=CC=21)C(O)=O                                   | CC(=O)NC(Cc1c[nH]c2ccccc12)C(=O)O                                   |
| -2.312223 | CC(=O)NC(CC1=CNC2=CC=CC=C21)C(O)=O                                   | CC(=O)NC(Cc1c[nH]c2ccccc12)C(=O)O                                   |
| -4.490234 | CC(C(O)=O)C1=CC(F)=C(C=C1)C1C=CC=CC=1                                | CC(C(=O)O)c1ccc(-c2ccccc2)c(F)c1                                    |
| -4.390593 | CC(C(O)=O)C1C=C(F)C(=CC=1)C1C=CC=CC=1                                | CC(C(=O)O)c1ccc(-c2ccccc2)c(F)c1                                    |
| -1.220607 | CC(C)(C)NCC(O)C1C=C(CO)C(O)=CC=1                                     | CC(C)(C)NCC(O)c1ccc(O)c(CO)c1                                       |
| -1.220000 | CC(C)(C)NCC(O)C1C=CC(O)=C(CO)C=1                                     | CC(C)(C)NCC(O)c1ccc(O)c(CO)c1                                       |
| -4.459671 | CC(NC(=O)C(NC(=O)OC(C)C)C(C)C)C1=NC2C=CC(F)=CC=2S1                   | CC(C)OC(=O)NC(C(=O)NC(C)c1nc2ccc(F)cc2s1)C(C)C                      |
| -4.464189 | CC(NC(=O)C(NC(=O)OC(C)C)C(C)C)C1=NC2=CC=C(F)C=C2S1                   | CC(C)OC(=O)NC(C(=O)NC(C)c1nc2ccc(F)cc2s1)C(C)C                      |
| -4.843556 | CC12CCC3C(CCC4C=C(O)C=CC=43)C1CCC2O                                  | CC12CCC3c4ccc(O)cc4CCC3C1CCC2O                                      |
| -4.878885 | CC12CCC3C(CCC4=CC(O)=CC=C43)C1CCC2O                                  | CC12CCC3c4ccc(O)cc4CCC3C1CCC2O                                      |
| -3.590151 | CC1CC2=CC=CC=C2N1NC(=O)C1C=C(C(Cl)=CC=1)S(N)(=O)=O                   | CC1Cc2ccccc2N1NC(=O)c1ccc(Cl)c(S(N)(=O)=O)c1                        |
| -3.643076 | CC1CC2C=CC=CC=2N1NC(=O)C1=CC(=C(Cl)C=C1)S(N)(=O)=O                   | CC1Cc2ccccc2N1NC(=O)c1ccc(Cl)c(S(N)(=O)=O)c1                        |
| -3.488982 | CCCC1COC(CN2C=NC=N2)(O1)C1=CC=C(Cl)C=C1Cl                            | CCCC1COC(Cn2cncn2)(c2ccc(Cl)cc2Cl)O1                                |
| -3.490941 | CCCC1COC(CN2C=NC=N2)(O1)C1C=CC(Cl)=CC=1Cl                            | CCCC1COC(Cn2cncn2)(c2ccc(Cl)cc2Cl)O1                                |
| -3.462350 | CCOP(=O)(OC(=CCl)C1=CC=C(Cl)C=C1Cl)OCC                               | CCOP(=O)(OCC)OC(=CCl)c1ccc(Cl)cc1Cl                                 |
| -3.426403 | CCOP(=O)(OC(=CCl)C1C=CC(Cl)=CC=1Cl)OCC                               | CCOP(=O)(OCC)OC(=CCl)c1ccc(Cl)cc1Cl                                 |
| -3.120000 | CC1(O)C2CC3C(C(=O)C(C(N)=O)C(=O)C3(O)C(=O)C2C(=O)C2=C1C=CC=C2O)N(C)C | CN(C)C1C(=O)C(C(N)=O)C(=O)C2(O)C(=O)C3C(=O)c4c(O)cccc4C(C)(O)C3CC12 |
| -3.120183 | CC1(O)C2CC3C(C(=O)C(C(N)=O)C(=O)C3(O)C(=O)C2C(=O)C2C1=CC=CC=2O)N(C)C | CN(C)C1C(=O)C(C(N)=O)C(=O)C2(O)C(=O)C3C(=O)c4c(O)cccc4C(C)(O)C3CC12 |
| -4.600000 | COC1=CC(=O)CC(C)C21OC1C(Cl)=C(C=C(OC)C=1C2=O)OC                      | COC1=CC(=O)CC(C)C12Oc1c(Cl)c(OC)cc(OC)c1C2=O                        |
| -4.609974 | COC1=CC(=O)CC(C)C21OC1=C(Cl)C(=CC(OC)=C1C2=O)OC                      | COC1=CC(=O)CC(C)C12Oc1c(Cl)c(OC)cc(OC)c1C2=O                        |
| -3.407463 | COP(=O)(OC(=CCl)C1C=CC(Cl)=CC=1Cl)OC                                 | COP(=O)(OC)OC(=CCl)c1ccc(Cl)cc1Cl                                   |
| -3.406553 | COP(=O)(OC(=CCl)C1=CC=C(Cl)C=C1Cl)OC                                 | COP(=O)(OC)OC(=CCl)c1ccc(Cl)cc1Cl                                   |
| -4.130182 | COC1C=C(C=CC=1OC)C(=CC(=O)N1CCOCC1)C1C=CC(Cl)=CC=1                   | COc1ccc(C(=CC(=O)N2CCOCC2)c2ccc(Cl)cc2)cc1OC                        |
| -4.126277 | COC1=CC(=CC=C1OC)C(=CC(=O)N1CCOCC1)C1C=CC(Cl)=CC=1                   | COc1ccc(C(=CC(=O)N2CCOCC2)c2ccc(Cl)cc2)cc1OC                        |
| -1.599188 | NC(CC1=CC(O)=C(O)C=C1)C(O)=O                                         | NC(Cc1ccc(O)c(O)c1)C(=O)O                                           |
| -1.600280 | NC(CC1C=C(O)C(O)=CC=1)C(O)=O                                         | NC(Cc1ccc(O)c(O)c1)C(=O)O                                           |
| -2.635988 | OC(=O)C=CC1C=C(Br)C=CC=1                                             | O=C(O)C=Cc1cccc(Br)c1                                               |
| -2.635976 | OC(=O)C=CC1C=CC=C(Br)C=1                                             | O=C(O)C=Cc1cccc(Br)c1                                               |
| -4.571488 | OCC(O)COC(=O)C1=CC=CC=C1NC1C=CN=C2C=C(Cl)C=CC2=1                     | O=C(OCC(O)CO)c1ccccc1Nc1ccnc2cc(Cl)ccc12                            |
| -4.539032 | OCC(O)COC(=O)C1C=CC=CC=1NC1C=CN=C2C=C(Cl)C=CC2=1                     | O=C(OCC(O)CO)c1ccccc1Nc1ccnc2cc(Cl)ccc12                            |

- Drop 51 compounds with fewer than 4 atoms;

| median_WS | canonical_smiles |
|:---------:|------------------|
| -1.347515 | CCF              |
| -0.889653 | ClCBr            |
| -1.360000 | C=CCl            |
|  1.366672 | C1CN1            |
|  0.056435 | N#CCl            |
|  1.368763 | CN               |
|  0.576820 | CN=O             |
|  1.347062 | CCN              |
| -1.170000 | BrCBr            |
| -1.473280 | O=C=O            |
| -0.314879 | CS               |
| -2.240461 | C=CC             |
|  1.339015 | CNN              |
| -1.050749 | CCCl             |
| -0.880000 | CCl              |
| -0.450879 | CSC              |
| -0.175874 | CF               |
| -0.600177 | CCS              |
|  0.324877 | C=NC             |
|  0.280601 | CNCl             |
| -0.795601 | CBr              |
| -1.437450 | FCF              |
| -2.043161 | C1CC1            |
| -0.630208 | ClCCl            |
|  1.568786 | C#N              |
|  1.356959 | C1CO1            |
| -0.318889 | C#C              |
|  1.100019 | CCO              |
| -1.599872 | CCI              |
| -0.936116 | C#CC             |
|  1.257576 | O=CO             |
|  1.347358 | NC=O             |
|  1.207961 | CC=O             |
| -1.550000 | S=C=S            |
| -2.341509 | ICI              |
| -1.123776 | C=C              |
| -1.274916 | C=CBr            |
| -0.275892 | C=CF             |
| -0.077333 | C=O              |
| -2.698898 | CC               |
|  0.260000 | CC#N             |
| -1.089857 | CCBr             |
| -2.840270 | CCC              |
| -1.001525 | CI               |
|  1.558953 | CNC              |
|  1.514753 | CO               |
|  0.663283 | COC              |
| -0.819365 | FCCl             |
| -0.633020 | N#CI             |
|  1.124515 | N#CN             |
| -1.690370 | O=C=S            |

- Rename the column name from "median_WS" to "logS";


**Reference**

1. C. N. Lowe, N. Charest, C. Ramsland, D. T. Chang, T. M. Martin, and A. J. Williams, Transparency in modeling through careful application of oecd’s qsar/qspr principles via a curated water solubility data set, [Chemical Research in Toxicology 36, 465 (2023)](https://doi.org/10.1021/acs.chemrestox.2c00379). 
