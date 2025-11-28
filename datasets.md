---
layout: page
title: Datasets
permalink: /datasets/
order: 1
---

<script id="MathJax-script" async src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js"></script>


**Note**:

* All the SMILES strings are canonical;
* "x" column: "canonical_smiles";


## ADME


### Aqueous solubility

| Task       | $$N$$  | y    | Dataset                                            | Preprocessing                             |
|:----------:|-------:|:----:|:--------------------------------------------------:|:-----------------------------------------:|
| ESOL       |  1,084 | logS | [here](/ADMET/datasets/solubility_ESOL.csv)        | [here](/ADMET/datasets/solubility_esol)   |
| EPA-sol    | 10,093 | logS | [here](/ADMET/datasets/solubility_EPA-sol.csv)     | [here](/ADMET/datasets/solubility_epa)    |
| AZ-sol     |  1,763 | logS | [here](/ADMET/datasets/solubility_AZ-sol.csv)      | [here](/ADMET/datasets/solubility_az)     |
| Biogen-sol |  2,173 | logS | [here](/ADMET/datasets/solubility_Biogen-sol.csv)  | [here](/ADMET/datasets/solubility_biogen) |
| NCATS-sol  |  2,453 | low_solubility | [here](/ADMET/datasets/solubility_NCATS-sol.csv) | [here](/ADMET/datasets/solubility_ncats) |


### Lipophilicity

| Task    | $$N$$ | y       | Dataset                                           | Preprocessing                            |
|:-------:|------:|:-------:|:-------------------------------------------------:|:----------------------------------------:|
| AZ-lipo | 4,195 | logD7.4 | [here](/ADMET/datasets/lipophilicity_AZ-lipo.csv) | [here](/ADMET/datasets/lipophilicity_az) |


### Permeability

| Task        | $$N$$ | y                            | Dataset                                              | Preprocessing                                    |
|:-----------:|------:|:----------------------------:|:----------------------------------------------------:|:------------------------------------------------:|
| CSU-Caco2   | 1,018 | logPapp                      | [here](/ADMET/datasets/permeability_CSU-Caco2.csv)   | [here](/ADMET/datasets/permeability_csu_caco2)   |
| USTL-Caco2  | 1,780 | logPapp                      | [here](/ADMET/datasets/permeability_USTL-Caco2.csv)  | [here](/ADMET/datasets/permeability_ustl_caco2)  |
| Biogen-MDCK | 2,642 | "LOG MDR1-MDCK ER (B-A/A-B)" | [here](/ADMET/datasets/permeability_Biogen-MDCK.csv) | [here](/ADMET/datasets/permeability_biogen_mdck) |
| NCATS-PAMPA-pH7.4 | 2,033 | low_moderate_permeability | [here](/ADMET/datasets/permeability_NCATS-PAMPA-pH7.4.csv) |
| NCATS-PAMPA-pH5   | 486   | low_permeability          | [here](/ADMET/datasets/permeability_NCATS-PAMPA-pH5.csv)   |

**Note**:

- [Caco2]()
- [MDCK]()
- [PAMPA]()


### Plasma protein binding (PPB)

| Task        | $$N$$ | y                                                | Dataset                                        | Preprocessing                            |
|:-----------:|------:|:------------------------------------------------:|:----------------------------------------------:|:----------------------------------------:|
| AZ-rPPB     | 717   | log_pct_unbound                                  | [here](/ADMET/datasets/PPB_AZ-rPPB.csv)        |
| Biogen-rPPB | 168   | "LOG PLASMA PROTEIN BINDING (RAT) (% unbound)"   | [here](/ADMET/datasets/PPB_Biogen-rPPB.csv)    | [here](/ADMET/datasets/ppb_rat_biogen)   |
| AZ-dPPB     | 244   | log_pct_unbound                                  | [here](/ADMET/datasets/PPB_AZ-dPPB.csv)        |
| AZ-mPPB     | 162   | log_pct_unbound                                  | [here](/ADMET/datasets/PPB_AZ-mPPB.csv)        |
| AZ-hPPB     | 1,614 | log_pct_unbound                                  | [here](/ADMET/datasets/PPB_AZ-hPPB.csv)        | [here](/ADMET/datasets/ppb_human_az)     |
| Biogen-hPPB | 194   | "LOG PLASMA PROTEIN BINDING (HUMAN) (% unbound)" | [here](/ADMET/datasets/PPB_Biogen-hPPB.csv)    | [here](/ADMET/datasets/ppb_human_biogen) |


### Hepatocyte stability

| Task      | $$N$$ | y                                   | Dataset                                        | Preprocessing                            |
|:---------:|------:|:-----------------------------------:|:----------------------------------------------:|:----------------------------------------:|
| AZ-rH     | 837   | "LOG RH_CLint (uL/min/1E6 cells)"   | [here](/ADMET/datasets/hepatocyte_AZ-rH.csv)   |
| AZ-hH     | 407   | "LOG HH_CLint (uL/min/1E6 cells)"   | [here](/ADMET/datasets/hepatocyte_AZ-hH.csv)   |    |


### Liver microsomal stability

| Task       | $$N$$ | y                           | Dataset                                           | Preprocessing                                |
|:----------:|------:|:---------------------------:|:-------------------------------------------------:|:--------------------------------------------:|
| NCATS-rLM  | 2,528 | unstable                    | [here](/ADMET/datasets/microsomal_NCATS-rLM.csv)  | 
| Biogen-rLM | 3,054 | "LOG RLM_CLint (mL/min/kg)" | [here](/ADMET/datasets/microsomal_Biogen-rLM.csv) | [here](/ADMET/datasets/stability_biogen_rlm) |
| AZ-hLM     | 1,102 | "LOG HLM_CLint (mL/min/g)"  | [here](/ADMET/datasets/microsomal_AZ-hLM.csv)     |
| Biogen-HLM | 3,087 | "LOG HLM_CLint (mL/min/kg)" | [here](/ADMET/datasets/microsomal_Biogen-hLM.csv) | [here](/ADMET/datasets/stability_biogen_hlm) |


### CYP450 interactions

| Task                                                                              | $$N$$ | y             | Dataset                                           |
|:----------------------------------------------------------------------------------|------:|:-------------:|:-------------------------------------------------:|
| CYP1A2_[CHEMBL1741322](https://www.ebi.ac.uk/chembl/explore/assay/CHEMBL1741322)  | 9,600 | pchembl_value | [here](/ADMET/datasets/CYP1A2_CHEMBL1741322.csv)  |
| CYP2C9_[CHEMBL1614027](https://www.ebi.ac.uk/chembl/explore/assay/CHEMBL1614027)  | 2,898 | pchembl_value | [here](/ADMET/datasets/CYP2C9_CHEMBL1614027.csv)  |
| CYP2C9_[CHEMBL1741325](https://www.ebi.ac.uk/chembl/explore/assay/CHEMBL1741325)  | 7,220 | pchembl_value | [here](/ADMET/datasets/CYP2C9_CHEMBL1741325.csv)  |
| CYP2C19_[CHEMBL1613777](https://www.ebi.ac.uk/chembl/explore/assay/CHEMBL1613777) | 3,518 | pchembl_value | [here](/ADMET/datasets/CYP2C19_CHEMBL1613777.csv) |
| CYP2C19_[CHEMBL1741323](https://www.ebi.ac.uk/chembl/explore/assay/CHEMBL1741323) | 8,850 | pchembl_value | [here](/ADMET/datasets/CYP2C19_CHEMBL1741323.csv) |
| CYP2D6_[CHEMBL1614110](https://www.ebi.ac.uk/chembl/explore/assay/CHEMBL1614110)  | 3,343 | pchembl_value | [here](/ADMET/datasets/CYP2D6_CHEMBL1614110.csv)  |
| CYP2D6_[CHEMBL1741321](https://www.ebi.ac.uk/chembl/explore/assay/CHEMBL1741321)  | 5,461 | pchembl_value | [here](/ADMET/datasets/CYP2D6_CHEMBL1741321.csv)  |
| CYP3A4_[CHEMBL1613886](https://www.ebi.ac.uk/chembl/explore/assay/CHEMBL1613886)  | 6,471 | pchembl_value | [here](/ADMET/datasets/CYP3A4_CHEMBL1613886.csv)  |
| CYP3A4_[CHEMBL1614108](https://www.ebi.ac.uk/chembl/explore/assay/CHEMBL1614108)  | 6,471 | pchembl_value | [here](/ADMET/datasets/CYP3A4_CHEMBL1614108.csv)  |
| CYP3A4_[CHEMBL1741324](https://www.ebi.ac.uk/chembl/explore/assay/CHEMBL1741324)  | 8,628 | pchembl_value | [here](/ADMET/datasets/CYP3A4_CHEMBL1741324.csv)  |

**Note**:

- See [here](/ADMET/datasets/chembl_cyp450) for the data extraction steps;
- [What is pCHEMBL?](https://chembl.gitbook.io/chembl-interface-documentation/frequently-asked-questions/chembl-data-questions#what-is-pchembl)


## Acute toxicity

### NCATS-LD50

| Task       | $$N$$  | y                                          | Dataset                                            |
|:----------:|-------:|:-------------------------------------------|:--------------------------------------------------:|
| rat-SC     |  1,886 | "rat_subcutaneous_LD50_(?log(mol/kg))"     | [here](/ADMET/datasets/toxicity_NCATS_LD50_rat_subcutaneous.csv) |
| rat-IV     |  2,464 | "rat_intravenous_LD50_(?log(mol/kg))"      | [here](/ADMET/datasets/toxicity_NCATS_LD50_rat_intravenous.csv) |
| rat-IP     |  5,001 | "rat_intraperitoneal_LD50_(?log(mol/kg))"  | [here](/ADMET/datasets/toxicity_NCATS_LD50_rat_intraperitoneal.csv) |
| rat-oral   | 10,151 | "rat_oral_LD50_(?log(mol/kg))"             | [here](/ADMET/datasets/toxicity_NCATS_LD50_rat_oral.csv) |
| mouse-SC   |  6,754 | "mouse_subcutaneous_LD50_(?log(mol/kg))"                   | [here](/ADMET/datasets/toxicity_NCATS_LD50_mouse_subcutaneous.csv)    |
| mouse-IV   | 16,967 | "mouse_intravenous_LD50_(?log(mol/kg))"                    | [here](/ADMET/datasets/toxicity_NCATS_LD50_mouse_intravenous.csv)     |
| mouse-IP   | 36,267 | "mouse_intraperitoneal_LD50_(?log(mol/kg))\_(?log(mol/kg))" | [here](/ADMET/datasets/toxicity_NCATS_LD50_mouse_intraperitoneal.csv) |
| mouse-oral | 23,350 | "mouse_oral_LD50_(?log(mol/kg))"                           | [here](/ADMET/datasets/toxicity_NCATS_LD50_mouse_oral.csv)            |


**Note**:

- See [here](/ADMET/datasets/toxicity_ncats_ld50) for the data extraction steps;
- SC: subcutaneous; IV: intravenous; IP: intraperitoneal
- LD50: [median lethal dose](https://en.wikipedia.org/wiki/Median_lethal_dose)
