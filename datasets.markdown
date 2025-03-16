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

| Task       | $$N$$  | y    | Dataset                                            | Preprocessing                             |
|:----------:|-------:|:----:|:--------------------------------------------------:|:-----------------------------------------:|
| 