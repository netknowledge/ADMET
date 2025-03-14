---
layout: page
title: ADMET tasks
permalink: /datasets/admet
---

<script id="MathJax-script" async src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js"></script>

Note:

* All the SMILES strings are canonical. 

## Aqueous solubility



### ESOL

**Dataset**: Download it [here]().

**Dataset description:** 1,084 compounds and their measured water solubilities in $$\log S$$ ($$\log_{10}$$ based solubility in the unit of mol/L). 

**Dataset preprocessing** 

1. Download the original dataset from [here](https://doi.org/10.1021/ci034243x), which contains 1,144 compounds; 
2. Use [RDKit](https://www.rdkit.org) to transform the SMILES to their canonical forms;
3. Drop duplicated records. For compounds with multiple $\log S$, we exclude those with an absolute difference greater than 0.09, and calculate average $\log S$ for the remaining. We then 
3. Drop compounds with fewer than 4 atoms. 

**Reference**

1. J. S. Delaney, ESOL: estimating aqueous solubility directly from molecular structure, [Journal
of Chemical Information and Computer Sciences 44, 1000 (2004)](https://doi.org/10.1021/ci034243x).


### EPA-sol

**Dataset**: Download it [here]().

**Dataset description:** 10,093 compounds and their measured water solubilities in $$\log S$$. 

**Dataset preprocessing** 

1. Download the original dataset from [here](https://pubs.acs.org/doi/10.1021/acs.chemrestox.2c00379), which comprises 10,207 compounds (7,655 training compounds and 2,552 a test set).
2. Remove duplicate instances. 
3. For compounds with multiple solubility values:
	* drop those with an absolute difference larger than 0.1
	* calculate the average for the rest
4. Drop compounds with fewer than 4 atoms.

**Reference**

1. C. N. Lowe, N. Charest, C. Ramsland, D. T. Chang, T. M. Martin, and A. J. Williams, Transparency in modeling through careful application of oecd’s qsar/qspr principles via a curated water solubility data set, [Chemical Research in Toxicology 36, 465 (2023)](https://doi.org/10.1021/acs.chemrestox.2c00379). 


### AZ(AstraZeneca)-sol

**Dataset**: Download it [here]().

**Dataset description:** 1,763 compounds deposited by AstraZeneca in ChEMBL~\cite{zdrazil2024chembl} experimental measurements of a collection of compounds in a number of assays, including solubility.

**Dataset preprocessing** 

1. Extract the raw dataset from the [ChEMBL version 34 database](https://ftp.ebi.ac.uk/pub/databases/chembl/ChEMBLdb/releases/chembl_34/) using assay ID [CHEMBL3301364](https://www.ebi.ac.uk/chembl/explore/assay/CHEMBL3301364). 
2. Convert the unit from to $$\log S$$ based on 

**Reference**

1. 


### Biogen-sol

**Dataset**: Download it [here]().

**Dataset description:** 2,173 compounds with measured solubility in $$\log S$$.

**Dataset preprocessing** 

Researchers at Biogen released a dataset containing a total of $3,521$ compounds and six measured ADME properties, including water solubility. 

1. Download the original dataset from [here](https://github.com/molecularinformatics/Computational-ADME/blob/main/ADME_public_set_3521.csv).
2. perform a unit conversion from $$\log ug/mL$$ to $$\log S$$, using calculated molecular mass based on RDKit. 
3. No filtering steps are needed for this dataset

**Reference**

1. C. Fang, Y. Wang, R. Grater, S. Kapadnis, C. Black, P. Trapa, and S. Sciabola, Prospective validation of machine learning algorithms for absorption, distribution, metabolism, and excretion
prediction: An industrial perspective, [Journal of Chemical Information and Modeling 63, 3263
(2023)](https://doi.org/10.1021/acs.jcim.3c00160). 


---

## Lipophilicity

### AZ-lipo

We extract this dataset from ChEMBL version 34 (assay ID \href{https://www.ebi.ac.uk/chembl/explore/assay/CHEMBL3301363}{CHEMBL3301363}). It consists of $4,200$ compounds and their $\log D_{7.4}$ values, octanol-water partition coefficient at pH7.4 measured using a shake flask method. We identify three compounds that have two $\log D_{7.4}$ values, and drop the two compounds with a large $\log D_{7.4}$ difference and take the average for the third compound. The final dataset includes $4,195$ compounds. 


---

## Permeability

We focus on two types of permeability assays: Caco-2 and MDR1-MDCK. Caco-2 permeability assays are \emph{in vitro} tests that measure the transport of compounds through a layer of human intestinal epithelial cells (Caco-2). As Caco-2 assays are known to have high variability between experiments, we identify two datasets published from previous literature. MDR1-MDCK permeability assays are \emph{in vitro} tests that use the MDR1-MDCK cell line to measure efflux ratio.

### CSU-Caco2

Researchers from Central South University (CSU) made available a curated dataset containing experimental values of $\log P_{\text{app}}$ for $1,272$ compounds~\cite{wang2016adme}. We obtain this dataset from \url{https://pubs.acs.org/doi/10.1021/acs.jcim.5b00642}. After removing duplicate entries based on SMILES string and $\log P_{\text{app}}$ values, as well as excluding one compound with fewer than four atoms, we calculate the average $\log P_{\text{app}}$ value for SMILES with more than one $\log P_{\text{app}}$ value. This process results in a final dataset of $1,018$ compounds. 

### USTL-Caco2

Researchers from the University of Science and Technology Liaoning (USTL) provided a curated  dataset comprising $1,827$ compounds and their $\log P_{\text{app}}$ values~\cite{wang2020qspr}. We download this dataset from \url{https://pubs.rsc.org/en/content/articlelanding/2020/ra/d0ra08209k}. After filtering out duplicates and compounds with a difference in $\log P_{\text{app}}$ greater than 0.1, we take the average for SMILES with more than one $\log P_{\text{app}}$ value, leaving us with $1,780$ compounds. 

### Biogen-MDCK

In the Biogen dataset mentioned above~\cite{fang2023prospective}, there are $2,642$ compounds with available measured efflux ratio values in the MDR1-MDCK assay. No preprocessing steps are needed for this task. 

**Reference**

1. C. Fang, Y. Wang, R. Grater, S. Kapadnis, C. Black, P. Trapa, and S. Sciabola, Prospective validation of machine learning algorithms for absorption, distribution, metabolism, and excretion
prediction: An industrial perspective, [Journal of Chemical Information and Modeling 63, 3263
(2023)](https://doi.org/10.1021/acs.jcim.3c00160). 


---


