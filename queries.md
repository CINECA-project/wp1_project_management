# Proposed Query Prioritization

## Entities

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

### Samples

- Tissue Type
- Genomic data, Patients associated if any

### Patient Clinical/Phenotypic

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

- Clin/Phen + Variants needed for short term WP5 use cases
- Clin/Phen + Samples needed for biobanking use cases
- Biobanking use cases will also have needs for information-retrieval type queries
- Not all data sets will have all fields
- Make use of existing query infrastructure

## Queries

### For Month 12 (Dec 2019)

- Discovery return values
  - id or URI of relevant entity

- No RNA expression (will be easier later when GA4GH RNA expression data formats/APIs well established)

- 
- Samples from patients with phenotype Y and variants in pathway Z
- Patients with variants in gene X

### For Month 18 (Jun 2020)

- Add Treatments, Outcomes, Lab work, Other data modalities to clin/phen

- Add access to RNA expression data 
    - GA4GH API/standard matrix format should be well established by then

- Add information retrieval queries (fuzzy search)
    - Need concrete examples

- Add complex return values
   - _e.g._, List/Histogram of Patient.Outcomes where variant X is present and treatment Y was undergone


       - Proceed to linked entities by M12
       - Evaluate beacon vs search APIs for these cases
           - Regardless of API, possible backends (proposed by GA4GH Discovery Search API):
               - Presto (https://prestodb.github.io)
               - GraphQL (https://graphql.org)
               - CanDIG to have FHIR/Variants demo for end of April
       - Other projects are evaluating APIs including:
            - FAIR data point
            - DataShield
        - Should consider those?