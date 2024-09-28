# About SHAPE-Seq sequencing.
*GitHub names : juslecl, Julia-Frank, JetteGutzeit, MasjaHoogendoorn

## Summary
 In a nutshell, SHAPE-seq *( from its full name : Selective 2'-Hydroxyl Acylation analyzed by Primer Extension sequencing)* is a technique used to study the structure of RNA molecules. It helps scientists understand how RNA folds and interacts with other molecules, which is important because RNA shape can affect its function. It is widely used because it provides a detailed picture of RNA structure, and this information can be crucial for studying RNA-related diseases or designing RNA-based therapies.

## SHAPE-Seq sequencing's proceeding

- **Chemical Probing**: In the first step, a chemical reagent is added to the RNA that reacts specifically with the 2'-OH group of the ribose sugar. This reaction, called nucleophilic acyl substitution, occurs mainly in unpaired or flexible regions of the RNA, such as single-stranded loops or bulges. In contrast, the double-stranded (paired) regions of RNA are more rigid, and the 2'-OH group is less accessible due to steric hindrance, making them less reactive to the SHAPE reagent.

- **Primer Extension**: The next step involves reverse transcription, where the RNA is copied into DNA. When the reverse transcriptase enzyme encounters a bulky chemical adduct at the 2'-position of a modified ribose, it creates steric hindrance, causing the enzyme to pause or stop. This leads to the formation of truncated cDNA fragments that correspond to the modified, flexible sites on the RNA.

- **Sequencing**: The resulting cDNA fragments are then sequenced, revealing the positions where the chemical reagent modified the RNA. This information identifies the regions of the RNA that are flexible or unstructured.

- **Data Analysis**: Finally, by analyzing the sequencing data, scientists can generate a map of the RNA’s structure, showing which parts are paired or unpaired. This map helps researchers understand how the RNA folds and how its structure might influence its biological function.


## Applications
The structural insight provided by this technique is crucial for understanding **disease mechanisms** (examples follow), and for designing **RNA-based therapies​**.

**1. HIV Research:**
SHAPE-seq has been used to study the structure of the HIV-1 RNA genome for developing new treatments. It helped researchers map how HIV RNA folds, providing insights into how these structures might influence viral replication and potential drug targets​.

**2. Cancer Research:**
In cancer biology, SHAPE-seq has been used to study the structure of non-coding RNAs, which can act as regulatory molecules in cancer progression. Researchers aim so to understand how RNA misfolding or changes in RNA regulatory elements contribute to oncogenesis (e.g. how it controls the expression of oncogenes or tumor suppressor genes​).

**3. Splicing Disorders:**
Mutations affecting RNA splicing are linked to many genetic diseases. SHAPE-seq has been applied to analyze the secondary structures of pre-mRNA and how mutations might alter RNA folding, thereby affecting splicing mechanisms. Diseases like spinal muscular atrophy (SMA) have  for example been studied using SHAPE-seq.

**4. COVID-19 Research:**
During the COVID-19 pandemic, SHAPE-seq was used to study the structure of the SARS-CoV-2 RNA genome. This helped in understanding how the viral RNA folds and how that structure plays a role in the virus’s ability to evade the host immune system or in its replication. Anti-viral drugs could thus be identified.

**5. Neurodegenerative Diseases:**
SHAPE-seq has been utilized to study RNA misfolding in neurodegenerative diseases like Amyotrophic Lateral Sclerosis (ALS) and Fragile X Syndrome (which are often linked to the abnormal folding of RNA-binding proteins or non-coding RNAs).

**6. RNA Therapeutics:**
SHAPE-Seq has played a key role in developing RNA-based drugs like siRNAs and antisense oligonucleotides (ASOs) by providing detailed maps of RNA structure. It helps optimize the design of these therapeutics by revealing the flexible, accessible regions of target RNAs, ensuring more effective binding and gene silencing. Additionally, SHAPE-Seq aids in improving the stability of RNA therapeutics by identifying vulnerable regions that can be modified to enhance durability within the body.

## Statistical methods involved.
**1. Normalization of SHAPE Reactivity Data:**

After sequencing, the raw data must be normalized to account for differences in experimental conditions or sequencing depth. This is often done by calculating a **Z-score** or more generally by fitting the reactivity data to a statistical model that **corrects for bias or variability**.

**2. Outlier Identification:**

RNA structure data from SHAPE-seq can contain noise. To distinguish true reactivity (regions that react to the chemical probe due to flexibility) from noise, statistical methods such as **thresholding** (e.g., using a cutoff for SHAPE reactivity) or **outlier detection algorithms** are applied.

**3. Probabilistic RNA Structure Prediction:**

Statistical models like **maximum-likelihood estimation (MLE) or Bayesian methods** are often used to predict RNA structures based on the reactivity data. 

**4. Statistical Testing for Hypotheses:**

When comparing different RNA samples, statistical tests like the **Wilcoxon rank-sum test or Student's t-test** can be used to determine whether differences in SHAPE reactivity between the samples are significant.

**5. Bootstrap Methods:**

To assess the confidence in RNA structure predictions, researchers sometimes use **bootstrapping**. This resampling technique helps estimate the variability or uncertainty in SHAPE reactivity values and structure predictions.

**6. Correlation Analysis:**

Correlation techniques, like **Pearson's correlation or Spearman’s rank correlation**, are sometimes applied to check if SHAPE reactivity correlates with other data (e.g., thermodynamic predictions).

## AI-tools
To compile the article, we used Chat-GPT as a tool to understand in an easier way what the assay does. It is especially appreciated if one has no background in biology, and struggles thus to understand more applied papers about it.

**Prompts (ChatGPT-4):** 

- "What is SHAPE-Seq and how does it work?"
- "Can you make me an easy-to-understand summary about SHAPE-seq technique and its concrete applications?"
- "What kind of chemical reaction happens exactly and why does it stop the reverse transcriptase enzymes?"
- "Is there any precise statistical method/test used ?"

## References
Interesting papers about the technique can be found there :

- Julius B. Lucks et al., “Multiplexed RNA Structure Characterization with Selective 2′-hydroxyl Acylation Analyzed by Primer Extension Sequencing (SHAPE-Seq),” Proceedings of the National Academy of Sciences 108, no. 27 (July 5, 2011): 11063–11068, doi:10.1073/pnas.1106501108.

- Sharon Aviran et al., “Modeling and Automation of Sequencing-based Characterization of RNA Structure,” Proceedings of the National Academy of Sciences (June 3, 2011), doi:10.1073/pnas.1106541108.
