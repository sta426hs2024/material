# Exercise 2: Part A
Group members: jmehdy, cozv

## Short summary on Long-read RNA sequencing
Long-read RNA sequencing (RNA-Seq) is a technology that captures and sequences full-length RNA molecules, providing a more comprehensive view of transcriptomes. It uses platforms like Oxford Nanopore and PacBio, which can read RNA or cDNA molecules in lengths exceeding 10,000 base pairs. Unlike short-read methods, this technology reduces the need for assembly and can identify complex transcript variants, alternative splicing, and gene fusions. It works by transcribing RNA to cDNA (in some protocols) and then sequencing each molecule directly, providing high-resolution insights into RNA structure and expression.

### How we did it:
- Prompt: write a short summary of how long-read-rna-sequencing technology works
- Tool: GPT-4o

# Exercise 2: Part B

## TIF-Seq
- Transcript isoform sequencing (TIF-Seq) identifies transcript isoforms by selective sequencing of full-length mRNA molecules with 5'caps and poly(A) tails. Capped mRNA molecules are selected by substituting the 5'caps with oligonucleotides.
- To achieve this result, 5'-phosphate groups are removed from non-capped RNAs to differentiate them from their capped counterparts. The caps are removed by tobacco acid pyrophosphatase (TAP) treatment to expose the 5'-phosphate groups for ligation with oligonucleotides. mRNAs are separated into 2 different tubes and reverse-transcribed to generate full-length cDNA (flcDNA). flcDNA in each tube is annealed to barcoded 5'-biotinylated primers and 3' primers. The primers contain barcode sequences unique to each tube, as a control mechanism against chimeric fragments and intermolecular ligation. The 2 tubes are combined, digested with NotI enzyme to produce sticky ends, and ligated to form circular double-stranded cDNA, which is fragmented subsequently. Fragments containing the biotinylated 3' and 5' ends are isolated with streptavidin. Multiplexing barcodes are added to the 3' and 5' ends of the purified cDNA fragments to create a cDNA library for sequencing.

### Pros:
- Identifies transcript isoforms by sequencing the 5' and 3' end of the same RNA strand
- Chimera-control barcodes filter out intermolecular ligation of cDNA fragments

### Cons:
- Requires a large amount of full-length RNA in the sample
- Use of NotI enzyme to introduce sticky ends is only viable for AT-rich genomes like yeast
- Strong bias toward short RNA strands.

### How we dit it:
- Source: https://www.illumina.com/science/sequencing-method-explorer/kits-and-arrays/tif-seq.html

## What is TIF-Seq used for?
- TIF-Seq (Transcript Isoform Sequencing) is an RNA sequencing assay designed to capture full-length transcript isoforms by simultaneously sequencing both the 5' and 3' ends of individual RNA molecules at single-nucleotide resolution.Technology

### Technology:
- TIF-Seq utilizes a combination of RNA processing and short-read sequencing technologies:
1. RNA oligo capping to select for capped mRNA molecules
2. Full-length cDNA generation
3. Circularization of cDNA
4. Fragmentation and selection of fragments containing both 5' and 3' ends
5. Short-read paired-end sequencing
This approach allows for the identification of complete transcript isoforms, including information about both transcription start sites (TSS) and polyadenylation sites (PAS).

### Application
TIF-Seq is used to:Identify and quantify full-length transcript isoforms
- Detect novel isoforms and unannotated transcripts
- Characterize complex transcriptional landscapes, including overlapping transcripts
- Study transcriptome diversity and gene regulation
- Improve genome annotations, especially for less-studied organisms
- Analyze differential isoform expression between conditions or samples
### TIF-Seq is particularly useful for:
- Detecting lowly expressed transcripts
- Distinguishing between mono- and bicistronic transcripts
- Identifying 3' UTR variations and short overlapping transcripts

### Statistics
The application of TIF-Seq generates data that requires specialized statistical approaches:Isoform clustering:
- Statistical methods to group similar transcript isoforms and define distinct clusters.
- Differential isoform expression analysis: Statistical models to identify significant changes in isoform usage between conditions or samples. Take DESeq2 for example:
	- Usage: DESeq2 is one of the most popular tools for differential gene expression analysis, and it can also be applied to isoform expression data if isoform counts are available. It fits a negative binomial distribution to model count data and uses shrinkage estimators for dispersion to calculate differential expression.
	- Example: If you have TIF-Seq data showing multiple transcript isoforms from a gene in normal versus disease samples, DESeq2 can be used to calculate which isoforms are significantly differentially expressed across conditions.
	- Statistical Model: DESeq2 models count data using a generalized linear model (GLM), which takes into account variability and biological replicates. It estimates fold changes and tests for significance using the Wald test or likelihood ratio tests.
- Noise reduction: Techniques to distinguish true isoforms from technical artifacts or background noise.
- Quantification of isoform abundance: Statistical approaches to estimate the relative abundance of different isoforms, accounting for biases in the sequencing process.
- Correlation analysis: Methods to assess reproducibility between replicates and compare TIF-Seq data with other RNA-seq approaches.
- Transcript boundary analysis: Statistical techniques to accurately define and compare transcript start and end sites across different conditions or genotypes.

### How we did it:
- Prompt:
```
(MAIN QUESTION): we chose TIF-Seq instead of Iso-seq. (PREVIOUS QUESTION): Week 2 Exercise Part B (as a group): linking *Technology*/*Application* of Long-read-RNA-Sequencing for a Sequencing Assay
- browse the list of **-seq assays (see [1,2] below) and pick one to summarize; once picked, post to #exercises Slack channel
- using a ChatGPT-like tool or web searches, write a short summary about what the assay does and what it is used for (include links to relevant resources)
- make the link (technology -> application -> statistics); add this to your summary
Links to **-seq:
[1] https://liorpachter.wordpress.com/seq/
[2] https://www.illumina.com/content/dam/illumina-marketing/documents/applications/ngs-library-prep/ForAllYouSeqMethods.pdf
```
- Tool: Perplexity

## Make the link technology -> application -> statistics
For TIF-Seq (Transcript Isoform Sequencing), the link between technology -> application -> statistics can be outlined as follows:
1. **Technology**:
TIF-Seq is a sequencing method designed to map the exact start (5′) and end (3′) sites of transcript isoforms at a genome-wide scale. It works by generating full-length cDNA libraries, circularizing the cDNA, and sequencing the junction fragments. This technology uses random barcoding to capture the full diversity of isoforms without bias introduced by PCR amplification.
**Key Features**:
- Circularization of full-length cDNA
- Paired-end sequencing of 5′ and 3′ ends
- Random barcoding for duplicate removal
- Designed for eukaryotic systems (yeast, mouse, human)
2. **Application**: TIF-Seq is used to study the diversity of transcript isoforms in eukaryotic organisms. It allows researchers to:
- Identify transcript variants arising from alternative transcription start and end sites.
- Analyze how transcript isoforms differ in mRNA stability, localization, translation efficiency, or how they generate truncated proteins with different functions.
- Discover novel transcript isoforms that are otherwise missed by methods focused on either the 5′ or 3′ ends alone, such as short abortive transcripts or bicistronic messages.
- Example applications include exploring transcriptional heterogeneity in yeast, human, or mouse samples and identifying the functional impact of RNA processing events such as alternative polyadenylation.
3. **Statistics**:
- Sequencing Depth: TIF-Seq requires 5-10 times deeper sequencing than standard RNA-Seq due to the need to map both the 5′ and 3′ ends of isoforms. Typically, only 5-10% of the reads are usable for this purpose, requiring large sequencing efforts to capture a sufficient number of isoforms.
- Bias Correction: Random molecular barcoding is used to remove PCR duplicates, which ensures that amplification bias is minimized and isoform abundance measurements are accurate.
- Isoform Detection: The method provides high specificity in detecting full-length isoforms, but is biased towards shorter transcripts, which can overestimate their abundance relative to longer transcripts. Statistical analyses must account for this bias, and complementary techniques may be needed for robust quantification of long isoforms.
- Error Rates: Around 0.19% of reads are chimeric after filtering, which can affect data interpretation if not addressed. Additionally, the use of random barcodes helps remove PCR duplicates, ensuring the integrity of quantitative comparisons.
Overall Link:
Technology (TIF-Seq) enables precise detection of transcript isoforms by sequencing both 5′ and 3′ ends.
Application of this technology helps in identifying transcriptional variation, alternative splicing events, and other forms of RNA processing that affect mRNA function.
Statistics play a critical role in ensuring that the data generated is reliable, addressing biases (e.g., length bias, duplicate reads) and ensuring deep enough sequencing to capture the diversity of isoforms. The analysis focuses on accurately measuring isoform diversity, correcting for biases, and ensuring reproducibility across experiments.

### How we did it:
- Source: https://www.ncbi.nlm.nih.gov/pmc/articles/PMC4111111/
- Prompt:
```
What is the link technology -> applpication -> statistics
```
- Tool: GPT-4o