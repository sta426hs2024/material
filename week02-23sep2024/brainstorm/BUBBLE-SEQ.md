Github usernames: zoevma, pimoen, jubuerk, hseifried

Bubble-seq is a method to identify replication initiation sites by isolating DNA replication bubbles. DNA replication bubbles are structures formed during the S-phase of the cell cycle. During S-phase, the DNA double-strand is being unwound in preparation for replication. Trapping DNA replication bubbles can therefore reveal replication initiation sites, also called origins of replication. Origins of replication are identified by isolating bubbles in an agarose gel, recovering the DNA and sequencing it. The distribution of origins of replication is expressed as a "density", explained as "the percentage of bubble-containing fragments in each timing sector divided by the percentage of the genome that partitions to that sector". Densities can be related to replication timing, revealing how replication activity is distributed across S-phase. Bubble-seq is thus used not only used to compile origin maps, but also allows us to investigate gene regulation driven by epigenetic factors.

| Technology | Applications                                                                                     | Statistics                     |
|------------|--------------------------------------------------------------------------------------------------|--------------------------------|
| Bubble-seq | Identification of replication origins in the genome (important for understanding DNA regulation) | Negative binomial distribution |
|            | Identification of replication frequency in identifying tumorous cells                            | P-values and 0.1% FDR          |
|            |                                                                                                  | Moving average (loess)         |
|            |                                                                                                  | Null model                     |


Some more details about the proposed statistics:
- In the article, the frequency in number of fragments observed was fitted with a pseudo-binomial distribution $p^2 (1 - p)^n$ null model. Then they used a timed data Multiple-Initiator model (MIM) to determine origin firing (i.e. early, mid, late-S phase). They proposed by fitting the MIM to the replication timing data that increasing numbers of initiators would result in earlier, more narrowly distributed, origin firing times.
- Negative binomial distribution: Modeled read-depth data to establish statistical significance
- P-values and 0.1% FDR: Ensured a highly reliable identification of bubble-containing fragments.
- Moving average (loess): Used to validate the 0.0144 RD cutoff, corresponding to ~60% fragment coverage.
- Null model: Helped define genomic "zones" by analyzing the pattern of bubble-containing fragments
- Read-Depth (RD) Cutoff Determination:
  - sequencing reads were modeled using a negative binomial distribution, which is well-suited to handle overdispersed data, typical in sequencing experiments
  - distribution was fitted to the lowest read-depth values to estimate a baseline, which allowed for calculating P-values and FDRs
- Cutoff:
  - RD cutoff of 0.0144 ensured that the fragments labeled as bubble-containing were statistically significant and likely represented regions of the genome involved in replication origin activity
- Null Model and Bubble-Containing Fragments:
  - discrete probability model (null model) was used to analyze the occurrence of negative EcoRI fragments (those without bubbles) between two bubble-containing fragments
  - analysis revealed a 3.6-fold enrichment in the actual data compared to the null model when n = 1 (one negative fragment between two positive fragments). This led to the adoption of a one-fragment joining rule, defining a "zone" as a cluster of adjacent bubble-containing fragments where no two are separated by more than one negative fragment. 


Relevant resources:

https://genome.cshlp.org/content/early/2013/07/16/gr.155218.113.abstract

http://enseqlopedia.com/wiki-entry/dna-sequencing-methods/sequence-rearrangements/bubble-seq/

https://www.ncbi.nlm.nih.gov/pmc/articles/PMC3814878/

To get some inputs and an overview we asked perplexity-AI “What is Bubble-seq”.

For the statistics task we asked Chat GPT "Could you summarize the statistics part of the paper «Bubble-seq analysis of the human genome reveals distinct chromatin-mediated mechanisms for regulating early- and late-firing origins»". To make sure it uses the right reference we copied the statistics part of that paper into the Chat GPT search.


