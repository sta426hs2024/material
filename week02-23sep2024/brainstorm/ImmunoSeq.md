#### Week 2 Exercise Part B (as a group): linking *Technology*/*Application* for a Sequencing Assay

### GitHub user names:
- dhasanova0
- dhumolli

# ImmunoSeq

## Description
Our adaptive immune system protects us against an enormous variety of pathogens. This is mainly mediated by antigen recognition capabilities of T cell receptors (TCRs) and B cell receptors (BCRs) expressed on the surface of T and B cells, respectively. TCRs and BCRs bind to a peptide region of an antigen called an epitope. This induces transcirtional changes in these cells and subsequent activation of other immune cells that contribute to the clearance of the pathogen. In order to recognize as many potential pathogens as possible the adaptive immune system has several mechanisms to generate diverse TCR and BCR repertoire. Here the focus is set on T cells. Upon antigen recognition by the TCR some T cell subsets can directly eliminate infected cells and others enhance or regulate the overall immune response against a given pathogen. The TCR is a heterodimer composed of $\alpha$ and $\beta$ polypeptide chains. Both chains have the so called complementary-determining regions (CDR3) which is the primary region responsible for antigen recognition presented on MHC class I and II molecules. The CDR3 region is formed at the junction of $\alpha$ and $\beta$ chain gene segments and is a result of their somatic recombination ($V\beta$, $D\beta$, $J\beta$ for $\beta$ chain and $V\alpha$ and $J\alpha$ for the $\alpha$ chain).Thus the diversity of TCRs arise from multiple gene segments of $\alpha$ and $\beta$ chains that can be rearranged in various combinations and the nucleotide insertion and deletions that are introduced at the gene segment junctions during the TCR rearrangement. Quantification and characterization of the TCR repertoire diversity is important to assess individuals' immune capability and provides insights into different disease areas such as immunodeficiency diseases and cancer. 

One method to assess individuals' TCR repertoire is Immuno-seq (1). This is a high-throughput sequencing assay used to analyze the devrsity of $TCR\beta$ CDR3 regions. Immuno-seq allows to sequence functional $TCR\beta$ loci from the genome of millions of T cells by first performing multiplex PCR to amplify the rearranged $TCR\beta$ followed by Illumnia high-throughput sequencing of 54bp which covers the entire CDR3 region. This approach captures only a fracture of all T cells of an individual and subsequently not the entire CDR3 diversity. The unseen species model is then applied to estimate the CDR3 diversity of the $TCR\beta$ chain. This is modeled by assuming poisson distribution of the CDR3 regions. By sequencing the TCR, the assay helps track immune diversity, monitor clonal expansions, and assess immune responses to pathogens, tumors, and therapies. It is also used to explore genetic variations in regulatory regions related to immune function, identifying both common and rare variants that contribute to autoimmune diseases, cancer, and other immune-related conditions.

**Technology**: ImmunoSeq -> **Application**: Immune repertoire profiling -> **Statistics**: Unseen species model assuming Poisson distribution of CDR3 diversity.


### Sources

(1) Robins, H. S., Campregher, P. V., Srivastava, S. K., Wacher, A., Turtle, C. J., Kahsai, O., Riddell, S. R., Warren, E. H., & Carlson, C. S. (2009). Comprehensive assessment of T-cell receptor β-chain diversity in αβ T cells. Blood, 114(19), 4099–4107. https://doi.org/10.1182/blood-2009-04-217604

(2) Morin, A., Kwan, T., Ge, B., Letourneau, L., Ban, M., Tandre, K., Caron, M., Sandling, J. K., Carlsson, J., Bourque, G., Laprise, C., Montpetit, A., Syvanen, A.-C., Ronnblom, L., Sawcer, S. J., Lathrop, M. G., & Pastinen, T. (2016). Immunoseq: The identification of functionally relevant variants through targeted capture and sequencing of active regulatory regions in human immune cells. BMC Medical Genomics, 9(1), 59. https://doi.org/10.1186/s12920-016-0220-7

(3) Robins, H. (2013). Immunosequencing: Applications of immune repertoire deep sequencing. Current Opinion in Immunology, 25(5), 646–652. https://doi.org/10.1016/j.coi.2013.09.017

(4) OpenAI. (2024). ChatGPT [Large language model]. Retrieved from https://www.openai.com/chatgpt; used to get the first idea about what ImmunoSeq works

