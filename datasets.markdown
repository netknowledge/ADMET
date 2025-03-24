---
layout: page
title: Datasets
permalink: /datasets/
order: 1
---

<script id="MathJax-script" async src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js"></script>


Note:

* All the SMILES strings are canonical;
* "x" column: "canonical_smiles";


## ADME


### Aqueous solubility

| Task       | $$N$$  | y    | Dataset                                            | Preprocessing                             |
|:----------:|-------:|:----:|:--------------------------------------------------:|:-----------------------------------------:|
| ESOL       |  1,084 | logS | [here](/ADMET/datasets/solubility_ESOL.csv)        | [here](/ADMET/datasets/solubility_esol)   |
| EPA-sol    | 10,093 | logS | [here](/ADMET/datasets/solubility_EPA.csv)         | [here](/ADMET/datasets/solubility_epa)    |
| AZ-sol     |  1,763 | logS | [here](/ADMET/datasets/solubility_AstraZeneca.csv) | [here](/ADMET/datasets/solubility_az)     |
| Biogen-sol |  2,173 | logS | [here](/ADMET/datasets/solubility_Biogen.csv)      | [here](/ADMET/datasets/solubility_biogen) |


### Lipophilicity

| Task    | $$N$$ | y       | Dataset                                               | Preprocessing                            |
|:-------:|------:|:-------:|:-----------------------------------------------------:|:----------------------------------------:|
| AZ-lipo | 4,195 | logD7.4 | [here](/ADMET/datasets/lipophilicity_AstraZeneca.csv) | [here](/ADMET/datasets/lipophilicity_az) |


### Permeability

| Task        | $$N$$ | y                            | Dataset                                              | Preprocessing                                    |
|:-----------:|------:|:----------------------------:|:----------------------------------------------------:|:------------------------------------------------:|
| CSU-Caco2   | 1,018 | logPapp                      | [here](/ADMET/datasets/permeability_CSU_Caco2.csv)   | [here](/ADMET/datasets/permeability_csu_caco2)   |
| USTL-Caco2  | 1,780 | logPapp                      | [here](/ADMET/datasets/permeability_USTL_Caco2.csv)  | [here](/ADMET/datasets/permeability_ustl_caco2)  |
| Biogen-MDCK | 2,642 | "LOG MDR1-MDCK ER (B-A/A-B)" | [here](/ADMET/datasets/permeability_Biogen_MDCK.csv) | [here](/ADMET/datasets/permeability_biogen_mdck) |

**Note**:

- [Caco2]()
- [MDCK]()


### Plasma protein binding (PPB)

| Task        | $$N$$ | y                                                | Dataset                                           | Preprocessing                            |
|:-----------:|------:|:------------------------------------------------:|:-------------------------------------------------:|:----------------------------------------:|
| Biogen-rPPB | 168   | "LOG PLASMA PROTEIN BINDING (RAT) (% unbound)"   | [here](/ADMET/datasets/PPB_rat_Biogen.csv)        | [here](/ADMET/datasets/ppb_rat_biogen)   |
| Biogen-hPPB | 194   | "LOG PLASMA PROTEIN BINDING (HUMAN) (% unbound)" | [here](/ADMET/datasets/PPB_human_Biogen.csv)      | [here](/ADMET/datasets/ppb_human_biogen) |
| AZ-hPPB     | 1,614 | log_pct_unbound                                  | [here](/ADMET/datasets/PPB_human_AstraZeneca.csv) | [here](/ADMET/datasets/ppb_human_az)     |


### Liver microsomal stability

| Task       | $$N$$ | y                           | Dataset                                          | Preprocessing                                |
|:----------:|------:|:---------------------------:|:------------------------------------------------:|:--------------------------------------------:|
| Biogen-RLM | 3,054 | "LOG RLM_CLint (mL/min/kg)" | [here](/ADMET/datasets/stability_Biogen_RLM.csv) | [here](/ADMET/datasets/stability_biogen_rlm) |
| Biogen-HLM | 3,087 | "LOG HLM_CLint (mL/min/kg)" | [here](/ADMET/datasets/stability_Biogen_HLM.csv) | [here](/ADMET/datasets/stability_biogen_hlm) |


### CYP450 interactions

| Task       | $$N$$  | y    | Dataset                                            | Preprocessing                             |
|:----------:|-------:|:----:|:--------------------------------------------------:|:-----------------------------------------:|
| 


## Acute toxicity

### NCATS-LD50

| Task       | $$N$$  | y    | Dataset                                            | Preprocessing                             |
|:----------:|-------:|:----:|:--------------------------------------------------:|:-----------------------------------------:|
| rat-SC     |  1,886 |      | [here](/ADMET/datasets/) | 
| rat-IV     |  2,464 | rat_intravenous_LD50_(?log(mol/kg)) | | [here](/ADMET/datasets/) | 
| rat-IP     |  5,001 | rat_intraperitoneal_LD50_(?log(mol/kg)) | [here](/ADMET/datasets/) | 
| rat-oral   | 10,151 | | [here](/ADMET/datasets/) | 
| mouse-SC   |  6,754 | mouse_subcutaneous_LD50_(?log(mol/kg))                   | [here](/ADMET/datasets/) | 
| mouse-IV   | 16,967 | mouse_intravenous_LD50_(?log(mol/kg))                    | [here](/ADMET/datasets/) | 
| mouse-IP   | 36,267 | mouse_intraperitoneal_LD50_(?log(mol/kg))_(?log(mol/kg)) | [here](/ADMET/datasets/) | 
| mouse-oral | 23,350 | mouse_oral_LD50_(?log(mol/kg))                           | [here](/ADMET/datasets/) | 


**Note**:

- SC: subcutaneous; IV: intravenous; IP: intraperitoneal

