# Group members

- Giacomo Castagnetti: kcajj

- Andrew: AKirabo639

- Almira: mimyle

Technique: Methyl-seq
# Summary ([1](#chatgpt))

## What is it?

Methyl-seq (methylation sequencing) is a genomic technology that detects DNA methylation patterns at a high resolution, typically focusing on cytosine-phosphate-guanine (CpG) sites. Methylation is an epigenetic modification where a methyl group is added to cytosines, influencing gene regulation without changing the DNA sequence itself. Two common methods are whole-genome bisulfite sequencing (WGBS), which provides a complete methylation map across the genome, and reduced representation bisulfite sequencing (RRBS), which targets CpG-rich regions for a more cost-effective approach.

## Key Uses

Methyl-seq is widely used in:
- Cancer research, to identify abnormal methylation patterns linked to tumorigenesis.
- Developmental biology, to study how methylation controls gene expression during growth.
- Environmental epigenetics, where environmental exposures impact methylation patterns.

## Data Analysis

Data from Methyl-seq can be analyzed using various bioinformatics tools that quantify differential methylation, e.g.:
- Differential Methylation Analysis: Statistical tests (e.g., t-tests, ANOVA, or generalized linear models) are used to compare methylation levels between different biological conditions (e.g., healthy vs. diseased tissues).
- Principal Component Analysis (PCA): Often applied to identify patterns and distinguish between different sample groups based on their methylation profiles.
- Heatmaps and Hierarchical Clustering: These visualization tools are used to highlight patterns of differential methylation across samples or conditions.

# Connection between a Methyl-seq experiment and Statistical data analysis

To describe the connection between a Methyl-sew experiment and the statistical analyses performed on the data, we will describe a specific experiment and explain a specific statistical analysis that can be performed.

## WGBS experiment on cancer cells ([2](#chatgpt))

Methyl-seq combines bisulfite treatment of DNA, which converts unmethylated cytosines into uracil (and later to thymine during sequencing), with next-generation sequencing (NGS). Methylated cytosines remain unchanged, enabling the identification of methylated vs. unmethylated sites in the genome. This method offers a comprehensive analysis of DNA methylation at single-base resolution across the entire genome or targeted regions.

1. To detect specific methylation patterns in tumor cells, DNA is extracted from tumor tissues and healthy control tissues. This allows for a direct comparison of methylation patterns between cancerous and normal cells.

2. Bisulfite Treatment: both tumor and control DNA are treated with sodium bisulfite. This chemical converts unmethylated cytosines to uracil, which are read as thymine during sequencing. Methylated cytosines remain unchanged.

3. Sequencing: The bisulfite-treated DNA is then sequenced using high-throughput sequencing technology. This produces reads where methylated and unmethylated cytosines can be distinguished based on whether cytosines remain or are converted to thymine.

4. Data Analysis ([3](#other)): The sequencing data is aligned to the reference genome, and the methylation status of each cytosine across the genome is determined. By comparing the methylation levels between tumor and normal samples, differential methylation regions (DMRs) are identified. These regions highlight where methylation levels are significantly different between the two samples.
    
    To identify DMRs, the fisher's exact test is performed for each methylation site. For each site, we count of how many cancer tissues are methylated/non-methylated and we compare this with the control tissues. 
    The fisher's exact test gives a p-value for each position. It is possible to detect the differentially methylated regions by adjusting for multiple hypothesis testing. The significant q values correspond to the differentially methylated sites.

# References

### ChatGPT

(1) prompt: write a short summary on 'Methyl-seq' technology. In this summary, include information about what the assay does and what it is used for (include links to real and relevant references and resources). Also in this summary, show how this technology is used in application, and the statistics that can be used to analyse the information generated in its application.

(2) prompt: how is WGBS used to identify hypermethylation in tumors?

### Other

(3): https://compgenomr.github.io/book/extracting-interesting-regions-differential-methylation-and-segmentation.html#differential-methylation


