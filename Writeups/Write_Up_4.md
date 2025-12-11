# Write-up 4: Pipeline

**Name:** Angelica Alvarado
**Student ID:** avocado  
**Date:** 11/20/2025  

---

## 1. SLURM Pipeline

How could one add a differential expression analysis (DESeq2) step to the rnaseq_pipeline_array_depend.sh script such that DESeq2 runs only after all salmon jobs for all samples have completed?
    - You could make the DESeq2 step run only after all of the jobs finish running by making the DESeq2 a separate SLURM job that depends on the Salmon job array. This would make DESeq2 wait before running.
---
