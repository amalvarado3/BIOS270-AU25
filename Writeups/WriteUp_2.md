# Write-up 2: Environment

**Name:** Angelica Alvarado
**Student ID:** avocado  
**Date:** 11/18/2025  

---
---

## 1. Micromamba Questions

Comparing (bioinfo_example_latest.yaml) with the original (bioinfo_example.yaml):
This is the Original:
- <img width="558" height="402" alt="image" src="https://github.com/user-attachments/assets/bb835358-785e-4ca2-884c-6181f503c4ad" />
This is the latest:
- <img width="563" height="306" alt="image" src="https://github.com/user-attachments/assets/d4660da1-fef5-410a-895f-78e6862217ea" />

Notes:
- The latest yamp file contains all of the same packages as the original
- The change between the two is that the latest has rpy2 installed
- There is also a prefix at the end of the latest yaml file because this is where the environment was stored before exporting

1. What micromamba command can you use to list all created environemnts?
   - ***micromamba env list***
3. What micromamba command can you use to list all packages installed in a specific environment?
   - ***micromamba list -n env_name***
5. What micromamba command can you use to remove a package?
   - ***micromamba remove -n env_name package_name***
7. What micromamba command can you use to install a package from a specific channel?
   - ***micromamba install -n env_name -c specific_channel_name package_name***
9. What micromamba command can you use to remove an environment?
   - ***micromamba env remove -n bioinfo_example***
11. What are all the r-base and Bioconductor packages that were installed in the bioinfo_example environment?
   - ***micromamba list -n bioinfo_example | grep -E "r-base|bioconductor***


## 2. Container Questions
1. Can you execute the python file that prints "Hello World!" from your singularity container? Why or why not?
   - ***No, you cannot.***



