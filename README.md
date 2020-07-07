# Automated Electronic Health Record Based detection of ARDS

This repository provides the instructions of how to apply the logistic regression model trained on patients hospitalized with acute hypoxic respiratory failure at a single center in January 1, 2016 through December 31, 2017 to your data to automatically detect ARDS.

## Getting Started

### Prerequisites

Jupyter Notebook https://jupyter.org/install

Python 3 https://www.python.org/downloads/

Apache cTAKES 4.0 <https://cwiki.apache.org/confluence/display/CTAKES/cTAKES+4.0+User+Install+Guide>



## Preparing the datasets

### Step 1: Structured Data

- Create a structured dataset named as "structured_data.csv" with all the variables listed in Structured Data Variable.docx. 

- Variable names have to be exactly the same as listed. Do not carry forward the values unless instructed. 

- Data time needs to be within 10 days since admit date.

### Step 2: cTAKES Features

- Create two cTAKES Features datasets with names "radiology_report_ctakes_features.csv" and "clinical_notes_ctakes_features.csv". 

- To make these two datasets we need to have a radiology report dataset and a clinical notes dataset to start with. Both datasets should have the following columns:

  ​	'EncounterID','time','NOTE_TEXT','NOTE_ID'

- Data time needs to be within 10 days since admit date.

- When these two datasets are ready, follow the instruction in the "process ctakes_publication" notebook to create "radiology_report_ctakes_features.csv" and "clinical_notes_ctakes_features.csv".



### Step 3: Final dataset

- After step1 and step2 are done, run script "Pre-processing data-publication" to create the final datasets "structured_2Htest.csv" and "structured+radiology50+clinical_notes250_2Htest.csv"



## Prediction

Run script "Prediction" to get the predicted probabilities of ARDS.



## Authors

* **XXX** 
* **XXX**
* **XXX**

## License

License

## Acknowledgments

Acknowledgements