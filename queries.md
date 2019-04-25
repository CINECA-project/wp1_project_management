# Proposed Query Prioritization

## Summary

Here is the quick summary of the queries and their timelines.

### Month 12 (T1.1.1)

- Discovery return values
  - list of ids or URIs of relevant entities

- Must be able to query Calls, Variants, Samples, and simple Patient data (demographics, phenotypes, diseases), and links between them

Examples:

- Samples corresponding to patients with disease X and variants in gene Y
    - return list of sample identifiers

- Patients with disease X and variants in gene Y that have samples of tissue Z available
    - return list of patient identifiers


### Month 18 (T1.1.2)

- More complex return values
    - histogram of counts, min/max, etc

- Include RNA expression

- Deeper clin/phen fields, in collaboration w/ WP3
    - include capabilities for treatments, outcomes, lab work, references to other data 

Examples:

- Hypothesis-driven association query: contingency table of phenotype X vs mutations in gene Y

- Patients with disease X and mutations in gene Y with RNA expression data available in gene Y

- Histogram of variants in pathway X in patients with phenotype Y by counts; or by consequence

- Counting of patients in registry with a specific rare disease


- Information retrevial queries on some fields (or push to D1.2, Month 24?)
    - need good examples for this
    - is this part of the underlying query API or built on top?


A longer description of the entities, queries, prioritization, and rationale follows.
For more informatino, consult [the list of collected use cases](./collected_use_cases.md).

## Entities

The entities (and their fields) we aim to query over the next 18 months as part of CINECA WP1 are identified as:

### Genomics

- Variants, with annotations
    - Gene, Pathway
    - Type, Consequence
    - Germline/Somatic (sample)

- Calls
    - Variants
    - Samples/Patients
    - Interpretation

- RNA Expression
    - Samples associated if any
    - Patients associated if any

### Specimen

- Samples
    - Tissue Type
    - Genomic data, Patients associated if any

### Clinical/Phenotypic

- Patients
     - Demographic info
     - Phenotypes
     - Diseases
     - Treatments
     - Outcomes
     - Samples associated if any
     - Genomic data associated if any
     - Lab work
     - Other data modalities (links to imaging, etc)

## Requirements/Constraints

Hard requirements for query implementations include:

- Clin/Phen + Variants needed for short term WP5 use cases
- Clin/Phen + Samples needed for biobanking use cases
- Not all data sets will have all fields; handle this gracefully
- Must be able to make use of existing infrastructure
- Biobanking use cases will also have needs for information-retrieval type queries

## Queries

### For Month 12 (Dec 2019)

- Discovery return values
  - list of ids or URIs of relevant entities

- No RNA expression (will be easier later when GA4GH RNA expression data formats/APIs well established)

- Must be able to query Calls, Variants, Samples, and simple Patient data (demographics, phenotypes, diseases), and links between them

Examples:

- Samples corresponding to patients with disease X and variants in gene Y
    - return list of sample identifiers

- Patients with disease X and variants in gene Y that have samples of tissue Z available
    - return list of patient identifiers

### For Month 18 (Jun 2020)

- Add Treatments, Outcomes, Lab work, Other data modalities to clin/phen

- Add access to RNA expression data 
    - GA4GH API/standard matrix format should be well established by then

- Add information retrieval queries (fuzzy search)
    - Need concrete examples

- Add complex return values
   - _e.g._, List/Histogram of Patient.Outcomes where variant X is present and treatment Y was undergone

Examples:

- Hypothesis-driven association query: contingency table of phenotype X vs mutations in gene Y

- Patients with disease X and mutations in gene Y with RNA expression data available in gene Y

- Histogram of variants in pathway X in patients with phenotype Y by counts; or by consequence

- Counting of patients in registry with a specific rare disease

- Information retrevial queries on some fields (or push to D1.2, Month 24?)
    - need good examples for this
    - is this part of the underlying query API or built on top?