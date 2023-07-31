---
title: Format your data
order: 2
---

# How to format your data

All data submitted to PHAROS must be formatted according to our specifications to facilitate cross-project analysis. 

## File format

For now our data upload process only supports data in CSV format.

[comment]: <> (You should be able to download the CSV template here.)

## Column definitions

Your data may include the following fields: 

[comment]: <> (If we are going to be updating these definitions regularly we will build a tool to pull the definitions automatically from the definitions file. If not updated regularly, continue to copy the definitions and paste them here.)

- **Sample ID** The researcher generated unique ID of the sample collected.

- **Animal ID** The researcher generated unique ID of the individual animal from which the sample was collected.

- **Host species** (Required) The species of the animal from which the sample was collected, written using binomial nomenclature, e.g. 'Vicugna pacos'.

- **Host species NCBI tax ID** The NCBI taxonomic ID of the host species, if known. Must be numeric, 1-7 digits long, e.g. '30538'.

- **Latitude** (Required) The north south position of a collection site.

- **Longitude** (Required) The east west position of a collection site.

- **Spatial uncertainty** Coordinate uncertainty from GPS recordings or post-hoc digitization, expressed in meters.

- **Collection day** (Required) The day of the month on which the speciman was collected, e.g. '3' for the third day of the month.

- **Collection month** (Required) The month in which the speciman was collected, in numeric form, e.g. '12' for December.

- **Collection year** (Required) The year in which the speciman was collected, written in four digit form, e.g. '2021'.

- **Collection method or tissue** The technique used to extract the sample, e.g. 'oropharyngeal swab', or the tissue from which the sample was extracted.

- **Detection method** The type of test performed to detect the pathogen, e.g. 'conventional PCR'.

- **Primer sequence** The sequence of both forward and reverse primers used to identify the sample (e.g., forward CDCAYGARTTYTGYTCNCARC 3' ; reverse RHGGRTANGCRTCWATDGC 3').

- **Primer citation** Link to papers or publications that reference primers for use in the species tested here.

- **Detection target** The pathogen or category of pathogens a detection method is designed to identify. This should reflect methodology over study aim (e.g., a visual inspection for ticks might still recover fleas and could be reported as targeting 'Ectoparasites').

- **Detection target NCBI tax ID** NCBI taxonomic ID of the detection target, if relevant. Must be numeric, 1-7 digits long, e.g. '30538'.

- **Detection outcome** The result of the test performed. Must be one of the following: 'positive' or 'negative' or 'inconclusive', or may be left blank if the result is pending.

- **Detection measurement** Any quantitative information on pathogen detection that is more detailed than simple positive or negative results (e.g., viral titer, parasite counts).

- **Detection measurement units** Units for quantitative measurements of pathogen intensity or test results (e.g., Ct, TCID50/mL, or parasite count).

- **Pathogen** The pathogen detected by the test, if any, e.g. ‘SARS-CoV-2’. Pathogen may be different from detection target. If no pathogen is detected it should either be synonymous with detection target or omitted.

- **Pathogen NCBI tax ID** The NCBI taxonomic ID of the pathogen detected, if known. Must be numeric, 1-7 digits long, e.g. '2697049'.

- **GenBank accession** The GenBank accession numbers for each primer pair, if available.

- **Detection comments** Any additional notes about the detection process.

- **Organism sex** The sex of the inidividual animal from which the sample was collected. Must be one of the following: 'female' or 'male' or 'unknown'.

- **Dead or alive** The state of the individual animal from which the sample was collected, at the time of sample collection. Must be one of the following: 'dead' or 'alive' or 'unknown'.

- **Health notes** Any additional notes about the state of the animal at the time of sample collection.

- **Life stage** The life stage of the animal from which the sample was collection.

- **Age** The numeric age of the animal from which the sample was collected, at the time of sample collection. For now, age must be expressed in seconds. Units will eventually be configured in the dataset settings.

- **Mass** The numeric mass of the animal from which the sample was collected, at the time of sample collection. Mass must be expressed in kilograms. Units will eventually be configured in the dataset settings.

- **Length** The numeric length of the animal from which the sample was collected, at the time of sample collection. Length must be expressed in meters. Units will eventually be configured in the dataset settings.
