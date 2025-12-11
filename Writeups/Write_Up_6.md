# Write-up 6: Project 2

**Name:** Angelica Alvarado
**Student ID:** avocado  
**Date:** 12/11/2025  

---

## 1. Project Overview

The primary objective of this project is to build off of the experiments that I did as a part of an independent research project. The overarching goal is to build a bioninformatics and machine learning pipeline that identifies which immune pathways are activated in immune cells after exposure to environmental particulate matter (PM2.5) and how that differs between allergic and non-allergic patients. PM2.5 is known to trigger inflammation and immune disregulation. 
    - On key aim is to build a tool that uses Gene Set Enrichment Analysis to determine the key immune pathways that are activated by PM2.5 exposure. The expected outcome would be enriched visualization of immune pathways associated with inflammation, visualized through network gene maps. One challenge could be the amount of pathways that are activated, which could make it confusing to map which order they are activated in. By having a larger dataset, we can mitigate this, as more timepoints would show us a clearer image of how the immune pathways are activated after exposure.\
    - Another key aim is to use machine learning to be able to predict and characterize which group a patient falls into. One challenge would be overfitting the data, which could be mitigated by cross-validating data or generating a larger dataset for the model to learn from.

---

## 2. Data 

I would look through papers on the topic to see if anyone has generated RNA-seq data where immune cells are exposed to PM2.5, especially in humans, but I would also consider using mouse models and generating hypotheses in humans based on that. If those databases are not available, then I could theoretically, in lab run experiments and generate my own RNA-seq database. 

I would aim for around 10-30 samples of patients immune cells, with different conditions like: exposed to PM2.5 vs control and possibly mutliple doses or time points. I would store these as FASTQ files. Currently, we would have to process these samples using Salmon to align and quantify, like we did in Project 1. To store the data and files, make a Git and store the intermediaries in $SCRATCH. 
---

## 3. Environment
The coding environment for this project would be in a Jupyer notebook for analysis, and we would likely use Python and R, with packages like numpy, pandas, scikit-learn, matplotlib and seaborn. Being able to re run results is important especially when we are generating plots and running multiple different samples to build the validity of our claims and model. To ensure reproducibility, we could make a Nextflow pipeline to run our analyses.

---

## 4. Pipeline
1. Clean up data and run QC on the raw RNA-seq FASTQ files
2. Use Salmon to align your reads
3. Run a DESeq2 analysis on the cleaned up files
4. Note the DEGs that come from that analysis so you can train the ML model
5. Build an ML tool that is trained on the relevant DEGs 

---

## 5. Machine Learning

The task that the ML would be trained to do is to predict whether or not a patient is exposed to PM2.5 or not based on their immune pathway markers. To convert the data into numerical form suitable for modeling, make sure that the DESeq2 results have the rlog taken, as taking this helps to make data more suitable for PCA and clustering by moderating the variance. I will apply a baseline model because it is a basic benchmark model. This would help us see if it is worth the extra time and effort to build and test a more complex model. To make sure that the model performs well on unseen data, we will make sure to split the data into train, test and validate sets, while also making sure to cross validate the data. To evaluate the model, track accuracy and ROC-AUC to minimize the false positive rate. This would also help us to see if the model is better than random guessing. 

