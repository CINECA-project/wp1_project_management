# Collected WP1 Query Use Cases

### WP5 (Clinical analyses)

* Outcome of treatment of a condition in patients stratified by genotype, phenotype
    - Initial discovery version: patients with a given condition and treatment; outcome data available
    - Final query: table of counts for outcome, genotype, phenotype"

### CanDIG

* Hypothesis-driven genotype/phenotype association query
    - Initial Discovery version: patients with given genotype/phenotype combination
    - Final query: case/control contingency table

* Given a patient phenotype or genotype find closest N number of similar patients - what treatment did they receive, what was the outcome?
    - similarity matching (eg., MME-type queries) on genotypes + phenotypes, return clinical info (treatment + outcomes)

* Where are the variants located in a certain gene? Do they correlate with coded protein domains / post translational modification sites / functionally important residues?
    - search variants by annotation, bin results by location

* Variant hot spot discovery. Which genes accumulate variants? Are the corresponding patients in the same cohort / has the same tumour type / had the same treatment?
    - histogram, "k-heavy-hitter" queries

* Does drug treatment / work exposure correlates with certain variants? Random appearance in untreated, but increased appearance in treated population? Do DNA damage drug / immune / citotoxic treated patients has increased mutational burden?

* Do DNA damage drug / immune / citotoxic treated patients has increased mutational burden?
    - (differential?) somatic counts vs treatment

* Which variants co-occur in different cancer types / cohorts - coevolution of genes in cancer
    - variants by diagnosis or other parameter that defines a virtual cohort

* Type of disruption of the variants (missence, non-sense, ...) effecting a gene and its distribution
    - variants by annotation (gene) and category
    - Does a variant modify the expressional profile of a gene? If yes, which direction

* Searching across variant and RNA expression data, possibly contingency matrix of results
    - Genes or variants targeted by a treatment. Which variants were the reason for a treatment
    - linking variants to clinical data

* Tumour content of the tissue a somatic variant identified from - does it correlates with callers used
    - correlation between variants and pipeline data

### UMCG/EUCAN-Connect

* Initial discovery of cohorts with participant for which specific data items have been collected. 

### UMCG/BBMRI

* Initial discovery of biobanks with patients with a certain diagnosis for which specific material or data is collected

### UMCG/EJP

* Counting of patients in registry with a specific rare disease, counting of patients with RD comorbidity across registries from the different ERNs.

### HES-SO, SIB

* Pathogenicities & druggability of variants as well as biosamples:
    - Finding data regarding pathways, e.g., -- Find data of all types related to TGF-β signaling pathway across all databases
    - Find data of all types on synaptic growth and remodeling related to glycolysis in the human brain across all databases "

* Associations of genes and variants with diseases and cancers or finding data on gene related to specific diseases, _e.g._:
    - Search for data on BRCA gene mutations and the estrogen signaling pathway in women with stage I breast cancer.
    - Search for data of all types that mention ALP gene in an osteosarcoma across all databases. 
    - Find samples of somatic mutations of BRAF for all cancers.
    - Find data about melanoma and BRAF V600E or V600K mutations. 
    - Search for data of all types related to the ob gene in obese M. musculus across all databases.
    - Search for all data for the HTT gene related to Huntington’s disease across all databases.
    - Search for all data on the SNCA gene related to Parkinson’s disease across all databases.
    - Search for data of all types related to MIP-2 gene related to biliary atresia across all databases.
    - Search for data of all types related to the LDLR gene related to cardiovascular disease across all databases.

* Finding data on diseases, e.g.
    - Search for data of all types on multiple sclerosis of all types across all databases
    - Find data on T-cell homeostasis related to multiple sclerosis across all databases

* Finding data on gene expressions, e.g., 
    - Search for all data types related to gene TP53INP1 in relation to p53 activation across all databases
    - Search for gene expression data that mention E2F cell line in cellular differentiation across all databases

* Finding drug-genome associations and interactions, e.g., -- Find datasets about BRAFV600 mutation-positive metastatic melanoma treated with vemurafenib.

* Finding cross-tissue variant gene expression and functions.

* Finding data on tissue expression of the gene products.
