---
title: Vector-borne disease
order: 6
---

# How to handle vector-borne disease data

We strongly encourage the use of PHAROS to store information on vector-borne transmission of parasites and pathogens.

## Combined records of hosts, vectors, and pathogens 

In cases with where datasets capture an interaction among a wildlife host, an arthropod vector, and a microbial pathogen, users should take special care to distinguish between two options for association syntax:

### Option A: Host-vector-pathogen nested records

_Example_: "We removed a tick (_Ixodes scapularis_) from a wild mouse (_Mus musculus_), and tested it for Lyme disease (_Borrelia burgdorferi_)."

Indicate nested associations by marking the same sample _and_ the same animal (host):

| | Sample ID  | Animal ID | Host species   | Pathogen               |
|-| ---------- | --------- | -------------- | ---------------------- |
|1| s001       | mm001     | _Mus musculus_ | _Ixodes scapularis_    |
|2| _**s001**_ | mm001     | _Mus musculus_ | _Borrelia burgdorferi_ |

### Option B: Co-occurring host-parasite and host-vector associations

_Example_: "We removed a tick (_Ixodes scapularis_) from a wild mouse (_Mus musculus_). We also tested blood from the mouse, which was positive for Lyme disease (_Borrelia burgdorferi_)."

Indicate nested associations by marking _different samples_ from the same animal (host):

| | Sample ID  | Animal ID | Host species   | Pathogen               |
|-| ---------- | --------- | -------------- | ---------------------- |
|1| s001       | mm001     | _Mus musculus_ | _Ixodes scapularis_    |
|2| _**s002**_ | mm001     | _Mus musculus_ | _Borrelia burgdorferi_ |

## Pathogen testing in free-living vectors

Researchers may also find themselves in a situation where they test a free-living vector for a vector-borne pathogen. As this denotes a true host-parasite association, this would still be permissible, even if the test result is negative. In these circumstances, the free-living vector should be recorded as the host; e.g., a mosquito tested for dengue fever:

| Host species    | Detection target | Detection outcome |
| --------------- | ---------------- | ----------------- |
| _Aedes aegypti_ | Dengue virus     | Negative          |

On the other hand, free-living stages without pathogens are outside the scope of this database, and **should not be submitted**; e.g., a questing tick found in the environment:

| Host species        | Detection target | Detection outcome |
| ------------------- | ---------------- | ----------------- |
| _Ixodes scapularis_ | None             | Not applicable    |

These types of records can be shared in databases like [GBIF] (gbif.org).