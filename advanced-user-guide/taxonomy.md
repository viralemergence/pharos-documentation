---
title: Taxonomy
order: 5
---

# Taxonomy

Users might encounter a number of different taxonomic issues while formatting their data for PHAROS. Some issues identified in beta testing are described below:

## Identification above the species level

Species-level identification isn't always possible: for example, species concepts are contentious and in flux for many microbial organisms, and many diagnostic methods work above the species level. It's always okay to use higher-level taxonomic identification in PHAROS; for example:

| Host species      | Host NCBI tax ID | Pathogen         | Pathogen NCBI tax ID |
|-------------------|------------------|------------------|----------------------|
| Desmodus rotundus | 9430           | Alphacoronavirus | 693996               |

For novel viruses, including a GenBank accession can help efforts to re-assign these records to species later on, or researchers can simply update their datasets.

## Identification to mixed taxonomic levels

Some datasets will contain results with multiple taxonomic levels, even for the same sample. This is easily managed by splitting records across rows. 

If this solution is used, researchers should be careful to split count data in a non-overlapping way. For example, if a baboon fecal sample contains 10 nematode eggs, of which 3 can be identified as _Strongyloides_ sp., this should be entered as:

| | Sample ID    | Animal ID | Host species | Pathogen      | Pathogen NCBI tax ID | 
|-|--------------|-----------|--------------|---------------|----------------------|
|1| PapioWorms24 | Paan1     | Papio anubis | Nematoda      | 693996               | 
|2| PapioWorms24 | Paan1     | Papio anubis | Strongyloides | 6247                 | 


| | Detection outcome | Detection measurement | Detection measurement units |
|-|-------------------|-----------------------|-----------------------------|
|1| Positive          | 7                     | egg count                   |
|2| Positive          | 3                     | egg count                   |


## Uncertain identification

Host identification based on morphology (i.e., without molecular confirmation) may be unreliable for some taxa. Researchers can flag this in the "Detection comments" field.

## Mismatch between target and organism

In some cases, detection target and pathogen identification may be misaligned. Researchers should aim to capture molecular methods, or - for visual studies - study scope, as accurately as possible. 


| Animal ID | Host species        | Detection target | Detection outcome | Pathogen          |
|-----------|---------------------|------------------|-------------------|-------------------|
| Pl001     | Peromyscus leucopus | Arthropoda       | Positive          | Ixodes scapularis |
| Pl002     | Peromyscus leucopus | Arthropoda       | Negative          |                   |

## Taxonomic changes

At the moment, PHAROS is not very robust to changing host or pathogen taxonomy - especially rapidly-changing viral and bacterial taxonomy. The NCBI taxonomic backbone uses unique identifiers to track changes over time, and we suggest that if possible, users fill in these fields ("Host species NCBI tax ID", "Detection target NCBI tax ID", and "Pathogen NCBI tax ID") to make their data more robust to these changes. Eventually, we hope to add back-end integration to update names automatically. 

