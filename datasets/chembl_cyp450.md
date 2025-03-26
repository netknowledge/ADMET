---
layout: default
permalink: /datasets/chembl_cyp450
---

<script id="MathJax-script" async src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js"></script>


# Extracting CYP450 datasets from ChEMBL

**Extraction steps** 

- Download [ChEMBL 34](https://ftp.ebi.ac.uk/pub/databases/chembl/ChEMBLdb/releases/chembl_34/); 
- Select targets whose type is "SINGLE PROTEIN", organism is "Homo sapiens", and name contains "Cytochrome P450" and obtain 36 targets (identified by `tid`);

| tid   | target_pref_name     | target_chembl_id |
|-------|----------------------|------------------|
| 32    | Cytochrome P450 11A1 | CHEMBL2033       |
| 65    | Cytochrome P450 19A1 | CHEMBL1978       |
| 76    | Cytochrome P450 11B1 | CHEMBL1908       |
| 94    | Cytochrome P450 7A1  | CHEMBL1851       |
| 10147 | Cytochrome P450 1B1  | CHEMBL4878       |

- Extract all the assays whose target is in the list of 36 selected targets and obtain 19,018 assays (identified by `assay_id` or `chembl_id`); top targeted CYP450 are:

| tid   | target_pref_name     | assays |
|-------|----------------------|--------|
| 17045 | Cytochrome P450 3A4  | 4931   |
| 11365 | Cytochrome P450 2D6  | 3000   |
| 12911 | Cytochrome P450 2C9  | 2872   |
| 12912 | Cytochrome P450 2C19 | 2238   |
| 12594 | Cytochrome P450 1A2  | 2207   |
| 10163 | Cytochrome P450 2C8  | 692    |
| 65    | Cytochrome P450 19A1 | 676    |
| 20085 | Cytochrome P450 2B6  | 564    |
| 12739 | Cytochrome P450 3A5  | 267    |
| 11113 | Cytochrome P450 1A1  | 239    |

- These assays in total involve 91,189 compounds; however, there are only 10 assays that test at least 500 compounds:

| assay_chembl_id | compounds |
|-----------------|-----------|
| CHEMBL1741322   | 9600      |
| CHEMBL1741323   | 8850      |
| CHEMBL1741324   | 8629      |
| CHEMBL1741325   | 7220      |
| CHEMBL1614108   | 6472      |
| CHEMBL1613886   | 6472      |
| CHEMBL1741321   | 5461      |
| CHEMBL1613777   | 3518      |
| CHEMBL1614110   | 3343      |
| CHEMBL1614027   | 2898      |
