---
title: Pooling
order: 3
---

# How to handle pooled samples

Although PHAROS is designed for granular (animal-level) data, pooled testing is still a welcome data source.

Researchers who are pooling samples from multiple animals can present that information one of two ways:

## Option 1: One-to-many sample-animal relationship

Suppose a researcher swabs three marmosets, and pools the three swabs into a single test for herpesviruses---but still wants to record metadata on individual animals. They might represent the single positive test result as:

| |Sample ID | Animal ID | Host species  | Organism sex | Detection outcome | Pathogen  | GenBank accession |
|-|---------- |  ----------| ---------- |  ---------- | ---------- | ---------- | ---------- |  
|1| CApool1 | Calla01 | _Callithrix aurita_ | Female | Positive | Macacine alphaherpesvirus 1 | GB8675309 |
|2| CApool1 | Calla002 | _Callithrix aurita_ | Male |  Positive | Macacine alphaherpesvirus 1 | GB8675309 |
|3| CApool1 | Calla003 | _Callithrix aurita_ | Female |  Positive | Macacine alphaherpesvirus 1 | GB8675309 |

In this format, the metadata for each animal is given on a separate row, but attached to the "Sample ID" and "GenBank accession". 

## Option 2: One-to-none sample-animal relationship

Suppose a researcher pools several dozen mosquitoes from a trap and tests that sample for West Nile virus. 

Sample ID | Animal ID | Host species  | Detection outcome | Pathogen  | GenBank accession | Detection comments |
| ---------- |  ----------| ---------- |  ---------- | ---------- | ---------- | ---------- |  
| Tuscon1 |     | _Aedes aegypti_ | Positive | West Nile virus | GB1738 | Pooled mosquito traps |  

In this format, individual animals are not identified, and the finest resolution of the data is at the trap (= sample) level.