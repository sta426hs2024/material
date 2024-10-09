[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/DTJX0Xc6)

# About Single-cell RNA sequencing.
*GitHub names : juslecl, Julia-Frank, JetteGutzeit, MasjaHoogendoorn

## Functioning of scRNA-seq
Single-cell RNA sequencing (scRNA-seq) is a technique to analyse the gene expression of single cells. Usually, it broadly follows 6 steps from preparing the sample to the data analysis.

**1. Sample Preparation:** 
The first step is acquiring the cells you want to analyze, which depends on the type of tissue you are working with. It’s important to ensure that your sample contains only cells and no other contaminants.

**2. Cell Isolation:**
Individual cells must be isolated to prevent mixing RNA from different cells. There are several technologies for isolating single cells, and the choice of method depends on the tissue type. Common techniques include:
- Fluorescence-activated cell sorting (FACS)
- Magnetic-activated cell sorting (MACS)
- Microfluidic systems
- Laser microdissection

**3. Cell Lysis and RNA Capture:**
In this step, the cells are lysed (broken down) to release their RNA. Poly-T primers are then added to capture the RNA, initiating reverse transcription, which results in complementary DNA (cDNA). During this process, each cell is assigned a unique barcode, allowing individual cells to be identified during the analysis.

**4. cDNA Amplification:**
To ensure there is enough cDNA for analysis, polymerase chain reaction (PCR) is used to amplify the cDNA.

**5. Library Preparation and Sequencing:**
Once amplified, the tagged cDNA from all cells is pooled together and prepared for sequencing using next-generation sequencing (NGS) platforms. The same library preparation techniques, sequencing platforms, and genomic alignment tools used for bulk RNA sequencing are employed here.

**6. Data Analysis:**
The final step involves analyzing the sequencing data to determine the gene expression profiles of individual cells.

## Applications ofscRNA-seq:
**- Developmental Biology:**
scRNA-seq is used to study how stem cells differentiate into various cell types, mapping the developmental lineages of tissues such as the brain, heart, and blood.

**- Cancer Research:** 
Tumors are often composed of highly heterogeneous cell populations. scRNA-seq can help identify subpopulations of cancer cells, including rare drug-resistant or metastatic cells.

**- Immunology:**
scRNA-seq allows for deep profiling of immune cell populations, revealing their roles in infection, autoimmune diseases, or cancer immunotherapy.

**- Neuroscience:**
Mapping brain cell diversity, understanding neurodegenerative diseases, and exploring how neurons respond to stimuli.

## Advantages and disadvantages of scRNA-seq:
There are several advantages to the scRNA-seq technique, some of which are: 

**- Information about Individual Cells:**
scRNA-seq provides gene expression data at the level of individual cells, allowing researchers to identify cellular heterogeneity within tissues.

**- Discovery of Rare Cells:**
It enables the detection of rare or previously unknown cell populations that may be missed in bulk RNA sequencing.

**- Tracking over Time:** scRNA-seq captures changes in gene expression, helping to track cellular processes like differentiation and development over time.

Nevertheless, scRNA-seq also comes with its own set of disadvantages:

**- Expensive and Specialized Technique:** The technique requires significant financial investment and specialized equipment, which can limit its accessibility, especially for smaller labs.

**- Complex Data Analysis:** scRNA-seq generates large, complex datasets that necessitate advanced bioinformatics tools and expertise, making the analysis process labor-intensive and computationally demanding.

**- Variability:** The procedure can introduce noise and batch effects, which may compromise the accuracy and reproducibility of results if not carefully controlled.

## References:
Lun, A. T., & Marioni, J. C. (2017). Overcoming confounding plate effects in differential expression analyses of single-cell RNA-seq data. Genome Medicine, 9(1), 1-12. https://doi.org/10.1186/s13073-017-0467-4

## Use of AI tools:
We used the ChatGPT framework based on GPT-4 which is trained on a knowlegdebase up until September 2023.
