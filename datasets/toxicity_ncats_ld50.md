---
layout: default
permalink: /datasets/toxicity_ncats_ld50
---

<script id="MathJax-script" async src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js"></script>


# Extracting NCATS LD50 datasets

**Extraction steps** 

- Download the original raw dataset from [here](https://cactus.nci.nih.gov/download/acute-toxicity-db/), which include 80,081 compounds measured against a total of 59 endpoints; 
- Use [RDKit](https://www.rdkit.org) to transform the SMILES to their canonical forms;
- Endpoints with the most measurements:

| Endpoint                                                       | Compounds |
|----------------------------------------------------------------|----------:|
| mouse_intraperitoneal_LD50\_(?log(mol/kg))\_(?log(mol/kg))     | 36295     |
| mouse_oral_LD50_(?log(mol/kg))                                 | 23373     |
| mouse_intravenous_LD50_(?log(mol/kg))                          | 16978     |
| rat_oral_LD50_(?log(mol/kg))                                   | 10190     |
| mouse_subcutaneous_LD50_(?log(mol/kg))                         | 6769      |
| rat_intraperitoneal_LD50_(?log(mol/kg))                        | 5021      |
| rat_intravenous_LD50_(?log(mol/kg))                            | 2472      |
| rat_subcutaneous_LD50_(?log(mol/kg))                           | 1896      |
| mouse_unreported_LD50_(?log(mol/kg))                           | 1739      |
| rabbit_skin_LD50_(?log(mol/kg))                                | 1495      |
| mammal (species unspecified)\_unreported\_LD50\_(?log(mol/kg)) | 1129      |
| rabbit_oral_LD50_(?log(mol/kg))                                | 894       |
| rat_skin_LD50_(?log(mol/kg))                                   | 835       |

- Focus on the first eight endpoints and for each endpoint, drop compounds with fewer than 4 atoms;

| mouse_intraperitoneal_LD50_(?log(mol/kg))\_(?log(mol/kg)) | canonical_smiles |
|-----------------------------------------------------------|------------------|
| 3.193687                                                  | CNN              |
| 1.940775                                                  | CCO              |
| 0.473706                                                  | CO               |
| 2.916573                                                  | CI               |
| 1.888338                                                  | CNC              |
| 1.582446                                                  | CCBr             |
| 2.444842                                                  | CCI              |
| 2.370307                                                  | CC#N             |
| 1.945005                                                  | CC=O             |
| 2.288595                                                  | ClCCl            |
| 2.758550                                                  | ICI              |
| 1.264442                                                  | NC=O             |
| 0.890260                                                  | CSC              |
| 2.400937                                                  | C1CO1            |
| 4.399809                                                  | C[Hg]Cl          |
| 1.689866                                                  | O=CO             |
| 4.000071                                                  | N#C[Na]          |
| 4.036188                                                  | N#C[K]           |
| 2.473158                                                  | N#CN             |
| 2.040894                                                  | N#CS             |
| 1.237392                                                  | CCN              |
| 2.188689                                                  | N#CO             |
| 1.157720                                                  | CN               |
| 1.782274                                                  | C[Se]C           |
| 3.627308                                                  | N#C[SeH]         |
| 1.059158                                                  | C                |
| 2.518576                                                  | C=C              |
| 4.032669                                                  | C[Hg+]           |

| mouse_oral_LD50_(?log(mol/kg)) | canonical_smiles |
|--------------------------------|------------------|
| 2.854248                       | C=O              |
| 3.046821                       | CNN              |
| 1.125590                       | CCO              |
| 0.642397                       | CO               |
| 3.863580                       | C#N              |
| 1.478412                       | ClCBr            |
| 2.183593                       | CC#N             |
| 1.689733                       | CC=O             |
| 1.988062                       | ClCCl            |
| 1.155297                       | NC=O             |
| 1.437597                       | S=C=S            |
| 1.225149                       | CSC              |
| 3.639386                       | C[Hg]Cl          |
| 3.884269                       | N#C[K]           |
| 2.067384                       | N#CN             |
| 3.227576                       | C1CS1            |
| 2.070692                       | N#CS             |
| 1.708925                       | N#CO             |
| 1.435486                       | C[Se]C           |
| 3.896719                       | C[Te]C           |
| 2.831173                       | C[As]=S          |
| 3.627308                       | N#C[SeH]         |
| 0.205286                       | C                |

| mouse_intravenous_LD50_(?log(mol/kg)) | canonical_smiles |
|---------------------------------------|------------------|
| 3.017451                              | CNN              |
| 1.368282                              | CCO              |
| 0.832699                              | CO               |
| 4.436147                              | C#N              |
| 1.826593                              | CC#N             |
| 2.181577                              | C1CO1            |
| 2.298970                              | O=CO             |
| 4.398714                              | N#C[K]           |
| 2.173424                              | N#CN             |
| 2.579609                              | N#CS             |
| 1.561833                              | C                |

| mouse_subcutaneous_LD50_(?log(mol/kg)) | canonical_smiles |
|----------------------------------------|------------------|
| 2.000376                               | C=O              |
| 3.265506                               | CNN              |
| 0.745116                               | CCO              |
| 0.514494                               | CO               |
| 3.110709                               | CI               |
| 1.353002                               | CNC              |
| 1.667498                               | BrCBr            |
| 2.193030                               | CCI              |
| 0.962067                               | CC#N             |
| 1.895787                               | CC=O             |
| 1.118844                               | ClCCl            |
| 2.508789                               | ICI              |
| 4.133964                               | N#C[Na]          |
| 4.000774                               | N#C[K]           |
| 3.259723                               | C[As]=S          |

| rat_oral_LD50_(?log(mol/kg)) | canonical_smiles |
|------------------------------|------------------|
| 2.477497                     | C=O              |
| 3.029158                     | CNN              |
| 0.814604                     | CCO              |
| 0.902487                     | CO               |
| 2.647031                     | CBr              |
| 1.447916                     | CCl              |
| 3.271288                     | CI               |
| 3.206713                     | BrCBr            |
| 1.906957                     | CCBr             |
| 1.412911                     | ClCBr            |
| 2.096903                     | C=CCl            |
| 1.222410                     | CC#N             |
| 1.959566                     | CCS              |
| 1.724956                     | ClCCl            |
| 0.907207                     | NC=O             |
| 1.802460                     | S=C=S            |
| 1.274836                     | CSC              |
| 2.786643                     | C1CO1            |
| 3.923920                     | C[Hg]Cl          |
| 1.621601                     | O=CO             |
| 3.881381                     | N#C[Na]          |
| 4.114718                     | N#C[K]           |
| 3.458074                     | C1CN1            |
| 2.528606                     | C1CS1            |
| 3.036830                     | N#C[Ag]          |
| 1.872310                     | N#CS             |
| 1.850043                     | N#C[Cu]          |
| 2.051972                     | CCN              |
| 1.457630                     | N#CO             |
| 2.330211                     | C=CBr            |
| 1.366993                     | CC=N             |
| 1.715327                     | C[Se]C           |
| 4.322688                     | C[Te]C           |
| 3.086445                     | C[As]=S          |
| 4.025249                     | N#C[SeH]         |
| 3.176487                     | C=NO             |
| 0.945439                     | CCC              |
| 0.017765                     | C                |
| 3.697211                     | C[Hg+]           |

| rat_intraperitoneal_LD50_(?log(mol/kg)) | canonical_smiles |
|-----------------------------------------|------------------|
| 3.120623                                | CNN              |
| 4.107106                                | CCO              |
| 0.628982                                | CO               |
| 3.147780                                | CI               |
| 3.062967                                | CNC              |
| 1.794253                                | CCBr             |
| 2.674516                                | CCI              |
| 1.683926                                | CC#N             |
| 2.439242                                | CCS              |
| 1.967181                                | ClCCl            |
| 2.822562                                | ICI              |
| 0.897733                                | NC=O             |
| 4.358416                                | C[Hg]Cl          |
| 4.056799                                | N#C[Na]          |
| 4.211628                                | N#C[K]           |
| 4.090097                                | C1CN1            |
| 3.155777                                | C1CS1            |
| 3.416980                                | O=C=S            |
| 2.039142                                | N#CS             |
| 1.695123                                | C[Se]C           |

| rat_intravenous_LD50_(?log(mol/kg)) | canonical_smiles |
|-------------------------------------|------------------|
| 2.537978                            | C=O              |
| 3.162796                            | CNN              |
| 1.505046                            | CCO              |
| 1.177136                            | CO               |
| 4.523297                            | C#N              |
| 1.388036                            | CC#N             |
| 4.257385                            | N#C[K]           |
| 2.701124                            | N#CN             |

| rat_subcutaneous_LD50_(?log(mol/kg)) | canonical_smiles |
|--------------------------------------|------------------|
| 1.854248                             | C=O              |
| 3.119378                             | CNN              |
| 2.847111                             | CBr              |
| 3.110709                             | CI               |
| 1.069277                             | CC#N             |
| 1.837796                             | CC=O             |
| 1.051548                             | NC=O             |
| 2.372134                             | C1CO1            |
| 3.920814                             | N#C[K]           |
| 2.824784                             | C1CS1            |
