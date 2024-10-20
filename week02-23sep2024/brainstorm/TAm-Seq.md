---
title: "TAm-Seq"
output: html_document
date: "2024-09-23"
---

GitHub usernames: goleniki, jordan-villiers

**TAm-Seq** (Tagged-Amplicon deep Sequencing) is a targeted next-generation sequencing method used for detecting and analyzing circulating tumor DNA (ctDNA) in liquid biopsy samples. Here's a brief summary:

- Purpose: TAm-Seq enables the identification and quantification of low-frequency mutations in cell-free DNA from cancer patients.

- Method:
  - Uses multiplex PCR to amplify specific genomic regions of interest
  - Incorporates unique molecular tags to reduce sequencing errors
  - Employs a two-step amplification process to improve sensitivity

<font size="5">**Technology -> application -> statistics link**</font> 

**TAm-Seq technology**

**Applications**

- Cancer Genomics: One of the main applications of TAm-Seq is detecting mutations in circulating tumor DNA (ctDNA). This is particularly valuable for:
    - Liquid biopsies: Non-invasive tests that monitor cancer progression or treatment response using blood samples rather than tissue biopsies.
    - Early cancer detection: Identifying cancer mutations in blood before symptoms appear.
    - Tracking tumor evolution: Monitoring genetic changes in a tumor over time to detect emerging treatment-resistant mutations.
- Monitoring Therapy Resistance: It’s used to track how tumors evolve during treatment, allowing for the early detection of drug-resistant mutations.
- Mutation Profiling in Research: TAm-Seq is also used in genomic studies that require sensitive detection of rare variants, especially when studying heterogeneous samples (like tumors or blood).

**Statistical approaches**

- Distributions: Binomial, Negative Binomial, Poisson
- Error Models: Bayesian, Poisson error correction
- Variant Detection: Likelihood models, Hidden Markov Models, Bayesian inference
- Machine Learning: Random forests, SVMs for variant classification
- Performance Metrics: Sensitivity, Specificity, FDR correction
- Statistical Power: Dependent on sequencing depth and coverage

**Relevant resources**

The description of TAm-Seq technology and it's applications was formed using Perplexity AI. Information for the search was used from the following websites:

1. https://www.ncbi.nlm.nih.gov/pmc/articles/PMC5856404/

2. https://pubmed.ncbi.nlm.nih.gov/22649089/

3. https://genomebiology.biomedcentral.com/articles/10.1186/s13059-022-02796-7

4. https://atm.amegroups.org/article/view/7851/html

5. https://humgenomics.biomedcentral.com/articles/10.1186/s40246-019-0220-8

6. https://www.mdpi.com/1424-8247/14/6/596

7. https://www.ncbi.nlm.nih.gov/pmc/articles/PMC10703097/

8. https://alitheagenomics.com/blog/what-is-high-throughput-rna-sequencing

The summary of statistical approaches was formed by ChatGTP.
