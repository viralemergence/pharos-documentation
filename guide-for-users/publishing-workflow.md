---
title: Publishing workflow
order: 4
---

# Follow these steps to publish your data

Publishing your data adds it to the public PHAROS database, which means that your datasets and your project metadata will be visible on the public map and in the public data table and will be downloadable by anyone with a PHAROS account. Data can be unpublished at any time.

**Note: please make sure your data is formatted correctly according to our data dictionary before going through the steps to publish it. Data that is outside of our column structure will not be able to be published.**

## Create a new project

- Click your name in the navigation bar to access the list of your projects

- To create a new project, click the "New project" button

- From the project page you may also download the dataset template and the column definitions CSVs

- The new project modal will ask you to fill in various metadata about your project; this can all be accessed later for additions and edits

## Create a new dataset within that project

- Name the dataset

- You will see the default dataset units; at the moment the system accepts only SI units, but they will be customizable soon

## Upload a CSV into your dataset

- In the toolbar on the right, press the "Add rows from CSV" button to upload a CSV

- Uploading a second CSV will add the new data to the end of the dataset

- CSV template and column definitions can be downloaded on the project list page

- Having extra columns in your dataset will stop the dataset from being publishable on PHAROS

## Click "Release dataset" when you are ready for the system to validate your data

Refer to the column defintions CSV, or click the "+" sign in each cell to read the defintion. Columns that currently are validated are:

- **Host species** must not be humans

- **Host species NCBI tax ID** must be numerical and between 1-7 digits

- **Latitude** must be a valid latitudinal value

- **Longitude** must be a valid longitudinal value

- **Spatial uncertainty** must be a numerical value

- **Collection day, collection month, and collection year** must, taken together, read as a valid date

- **Organism sex** must be a non-ambiguous value like "female" or "male" or "unknown" ("m" and "f" are also fine) 

- **Dead or alive** must be a non-ambiguous value 

- **Age** must be a numerical value

- **Mass** must be a numerical value

- **Length** must be a numerical value

- **Detection outcome** must be a non-ambiguous value

## Fix any errors discovered after dataset validation

Potential errors include:

- Cell data is invalid for that column

- Cell data is empty and that column is required

## Press the "Release dataset" button

- The "Release dataset" button will keep generating the validation reports until all your errors are fixed

- When all errors are fixed the dataset is marked as "Released" which means it can be published

## Return to the project page and press the "Publish" button

- Data is only publishable at the project level
  
- When you click the "Publish" button on a project, all "Released" datasets will be published

- Unreleased datasets will not be published and will remain editable in your project

## If you want to publish a new dataset in an already published project

- At the moment, to publish an additional dataset to a project that is already published, you have to mark the new dataset as "Released", "Unpublish" the whole project, and then "Publish" the project again

- This workflow is understandably a bit clunky and will be updated to a better workflow soon

## If you want to unpublish your data

- Projects can be unpublished at any time, and republished at any time after that

- To unpublish, click the dot menu and then click "Unpublish project"
