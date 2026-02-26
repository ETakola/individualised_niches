# Welcome! 
This is a folder to support a manuscript on the quantification of individualised niches, as they were defined in Takola & Schielzeth (2022). 

This is a conceptual figure of the main idea behind the study. 

<img width="547" height="185" alt="UpdatedFig" src="https://github.com/user-attachments/assets/d4bbccee-c482-4795-b84b-a2944e117f9b" />


Figure: Heuristic representation of the different niche levels. A) A community can be represented as a set of species where each one occupies a different niche. B) A species can be represented as a set of meta-populations with different niches. C) A population consists of multiple individuals with different individualised niches (potential niche is shown with transparent dots, realized niche is shown with bold dots). 
## What is the individualised niche?
In 2022, Takola & Schielzeth published [a study](https://www.researchgate.net/publication/361497997_Hutchinson's_ecological_niche_for_individuals) introducing the concept of individualised niche.
They defined it as the range of environmental conditions under which a particular individual has an expected lifetime reproductive success of ≥ 1 surviving offspring. 
Similarly to the Hutchinsonian ecological niche, they distinguished between the realized and the potential individualised niche. 

* The realized individualized niche is the place in environmental space in which a particular individual is found and has an expected lifetime reproductive success of ≥ 1. The realized individualized niche can be quantified empirically.
* The potential individualized niche is the volume in environmental space in which a particular individual could be found with an expected lifetime reproductive success of ≥ 1. The potential individualized niche cannot directly be quantified, but significant parts of the niche space can usually be statistically inferred.

They also defined a fundamental individualised niche, but this is not relevant to this study (a definition is provided [here](https://www.researchgate.net/publication/361497997_Hutchinson's_ecological_niche_for_individuals)). 

## Repository folders
There are three folders in this repository: _Data_, _Results_ and _Script_. 
* The folder _Data_ contains the data used in the analysis. Please note that the table "data_with_RSPs.csv" contains already the scaled relative selection probabilities, thus someone who would like to reproduce the Results should consider the code only after line 685. 
* The folder _Results_ contains 9 tables with outputs of the corresponding code.
* The folder _Script_ contains all the code needed to reproduce the analyses and the Figures of this study. 

## Open science statement
I commit to conducting this project according to open science principles to maximize transparency, reproducibility, and reuse. Where feasible, I will preregister key research questions and the analysis plan, and I will clearly document and justify any deviations. I will share analysis code, workflows, and documentation using version control (e.g., GitHub/GitLab) and archive a release in a trusted repository (e.g., Zenodo/OSF) with a DOI. Data and metadata (including a data dictionary and provenance notes) will be deposited in an appropriate repository under an open license whenever possible. If data cannot be fully shared due to privacy, sensitive locations, legal constraints, or community/Indigenous data sovereignty, I will provide a transparent explanation, share de-identified or aggregated data when appropriate, and/or enable controlled access. I will support computational reproducibility by providing scripts to regenerate all results and figures and, where feasible, a reproducible computing environment. I will disseminate findings through preprints and open-access publication when possible and will make project outputs findable and reusable by following [FAIR principles](https://www.nature.com/articles/sdata201618) and the [TADA guidelines](https://ecoevorxiv.org/repository/view/9806/).
