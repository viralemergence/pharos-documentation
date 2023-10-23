---
title: Common errors
order: 1
---

# Common errors

## What's in a row? 

PHAROS is designed for easy entry but can contain fairly complex data structures. Researchers working with data downloaded from PHAROS should be aware of the tension between two basic principles:
- Each row in PHAROS corresponds to a single measurement and an accompanying set of metadata
- The open structure of the data allows many-to-many relationships between several fields, including test outcomes

If researchers work with data without understanding these structures, they may incorrectly process their data.

For example, a user might be interested in estimating the prevalence of a specific pathogen at a handful of sites. However, selecting longitude, latitude, and test outcome, and summarizing prevalence without any additional processing, might lead to incorrect estimates because some samples may be pooled across multiple sites, or because some samples may be tested twice for confirmation / replication. Researchers should pay specific attention to fields like Sample ID and Animal ID, and be aware of potential many-to-many relationships among these fields. These will be easiest to anticipate and understand if researchers also explore the documentation accompanying datasets, and read publications associated with these data.

## What's in a timepoint?

Not all data in PHAROS are evidence of active infection. Researchers should pay attention to detection method, and be careful to separate serological data (which indicate past infection, at a different time than the recorded date in the dataset) from methods that can indicate active infection (PCR, isolation, or visual detection).