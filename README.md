## Integrated Analysis of Gene Expression and Biological Sequences in R


## Project Objective

This repository aims to:

- Provide a comprehensive analysis of gene expression data (RNA-Seq) and tree growth data using R.
- Demonstrate data wrangling, mathematical operations, and visualizations.
- Compare biological sequence diversity between E. coli and another organism through codon usage, sequence length, and nucleotide/amino acid frequency analyses.
- Showcase teamwork and collaboration through contributions and commits using GitHub.
- Create reproducible R scripts that yield clear and accurate results, including tables and plots.
- Ensure thorough documentation (README and comments) to facilitate understanding of each workflow step.

## Contributors

- *Tasfia Tasnim*
- *Tanjila Tabassum*
- *Razieh Fathinezhad*

Each contributor has actively participated in coding, analysis, and preparing results for the final report.

## Methods Used

- Data Wrangling
- Descriptive Statistics
- Inferential Statistics
- Data Visualization
- Exploratory Data Analysis (EDA)
- Comparative Genomics
- Codon Usage Analysis
- Sequence Length Analysis
- Nucleotide and Amino Acid Frequency Analysis
- k-mer Frequency Analysis
- Statistical Hypothesis Testing (t-test)
- RNA-Seq Analysis
- Creation of Boxplots, Histograms, and Barplots
- GitHub Collaboration & Version Control
## Part 1: Importing Files, Data Wrangling, Mathematical Operations, Plots, and Saving Code on GitHub

### Content

Part 1 is divided into two main sections:

1. *RNA-Seq Count Data Analysis:* Analyzes RNA-seq count data from the gene_expression.tsv file, which includes expression data for three samples. The data is processed and converted to numeric format for analysis. Key steps include calculating mean expression values, identifying the top 10 genes with the highest mean expression, and visualizing the distribution of mean values using histograms. This section demonstrates fundamental skills in processing gene expression data, computing descriptive statistics, and visualizing results.

2. *Tree Growth Data Analysis:* Explores tree growth data from the growth_data.csv file, tracking tree circumference at two different sites (control and treatment) over a 20-year period. The analysis includes computing mean and standard deviation, comparing growth rates, and performing a t-test to assess statistical significance, visualized using box plots.

### Purpose and Significance

Part 1 highlights key data analysis techniques using R, focusing on data importation, manipulation, and statistical computation. It emphasizes the importance of data visualization through histograms and box plots and the application of statistical tests, such as the t-test, to assess the significance of differences between two samples. The exercises provide hands-on experience with biological and environmental datasets while promoting team collaboration through GitHub for version control and project management.

## Part 2: Examining Biological Sequence Diversity

### Content

This section investigates genetic differences between Mycobacterium tuberculosis and E. coli by analyzing their coding DNA sequences (CDS), sourced from the Ensembl genome database. We calculate the total CDS count and length for each organism and perform statistical analyses, including summary statistics and box plots, to compare coding sequence lengths. 

Further analyses focus on nucleotide and amino acid composition, with bar plots created to visualize base and protein frequencies. Codon usage bias is assessed using codon tables and visualizations. We identify and compare the most over- and under-represented k-mers in the protein sequences of both organisms, uncovering important insights into sequence composition and potential functional differences.

### Purpose and Significance

Part 2 emphasizes the importance of comparing genetic sequence data to understand biological diversity. By examining differences in sequence length, codon usage, and k-mer representation between Mycobacterium tuberculosis and E. coli, the project provides insights into genomic organization and evolutionary pressures shaping these organisms. Analyzing codon usage bias uncovers evolutionary trends and adaptations that optimize protein synthesis for specific environments, while k-mer analysis offers a detailed perspective on nucleotide sequences and genomic characteristics. Together, these analyses deepen our understanding of the evolutionary and functional relationships between the two species.

## Code Documentation

To solve the questions, consider setting up a virtual environment using the following codes:

- *For downloading files:* download.file()
- *For reading in the file:* read.table()
- *For downloading the whole DNA sequence of the organism of interest:* 
  - download.file()
  - gunzip()
- *For determining the mean:* rowMeans()
- *For determining the median:* median()
- *For determining the standard deviation:* sd()
- *For calculating the t-test:* t.test()
- *For calculating Relative Synonymous Codon Usage (RSCU):* uco()
- *For calculating k-mer values:* count(, wordsize=N)
- *For making histogram plots:* hist()
- *For making box plots:* boxplot()
- *For making bar plots:* barplot()

## Download and Set Up Data

To download the coding DNA sequences for E. coli and Mycobacterium tuberculosis, you can use the following R commands. These commands download the files from the Ensembl genome database:


```R
# Set the URLs for the CDS files
ecoli_url <- "https://ftp.ensemblgenomes.ebi.ac.uk/pub/bacteria/release-59/fasta/bacteria_0_collection/escherichia_coli_str_k_12_substr_mg1655_gca_000005845/cds/Escherichia_coli_str_k_12_substr_mg1655_gca_000005845.ASM584v2.cds.all.fa.gz"
mtb_url <- "https://ftp.ensemblgenomes.ebi.ac.uk/pub/bacteria/release-59/fasta/bacteria_4_collection/mycobacterium_tuberculosis_gca_001318445/cds/Mycobacterium_tuberculosis_gca_001318445.6505_5_10.cds.all.fa.gz"



## Open RStudio.
Load the desired R script.
Click on the Run button next to the code or use the command line to execute it.
View Outputs
Outputs include:

Tables of CDS lengths
Codon usage tables
K-mer counts
Various plots (bar charts, box plots)
You can view plots directly in RStudio, or save them as image files using the following commands: # Example of saving a plot
png("output_plot.png")
plot(data)  # Replace 'data' with your plotting code
dev.off()  # Close the device
How to Raise Issues or Get Help

## If you encounter issues or have questions, you can:

Navigate to the repository's Issues tab and create a new issue, providing a detailed description of the problem along with error messages or steps to reproduce the issue.
Leave comments on the relevant GitHub repository sections for help or suggestions.

## Reference List
Becher, H., Sampson, J., & Twyford, A.D. (2022). Measuring the Invisible: The Sequences Causal of Genome Size Differences in Eyebrights (Euphrasia) Revealed by k-mers. Frontiers in Plant Science, 13. doi: 10.3389/fpls.2022.818410.

Bernard, G., Greenfield, P., Ragan, M.A., & Cheong Xin Chan (2018). k-mer Similarity, Networks of Microbial Genomes, and Taxonomic Rank. MSystems, 3(6). doi: 10.1128/msystems.00257-18.

Forsdyke, D.R. (2019). Success of alignment-free oligonucleotide (k-mer) analysis confirms relative importance of genomes not genes in speciation and phylogeny. Biological Journal of the Linnean Society. doi: 10.1093/biolinnean/blz096.

Lo, R., Dougan, K.E., Chen, Y., Shah, S., Bhattacharya, D., & Chan, C.X. (2022). Alignment-Free Analysis of Whole-Genome Sequences From Symbiodiniaceae Reveals Different Phylogenetic Signals in Distinct Regions. Frontiers in Plant Science, 13. doi: 10.3389/fpls.2022.815714.




