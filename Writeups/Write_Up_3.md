# Write-up 3: Data

**Name:** Angelica Alvarado
**Student ID:** avocado  
**Date:** 11/18/2025  

---

## 1. Create a Local SQL Database

1. Examine create_bacteria_db.sh How many tables will be created in the database?
   - There will be three tables created: GFF Table, Protein Cluster Table, Metadata Table
2. In the insert_gff_table.py script you submitted, explain the logic of try and except. Why is this necessary?
   - The try and except logic stops the program from crashing when the database is unavailable temporarily. This logic is necessary because SQLite only allows one writer at a time, so without this, the job would crash every time two tasks were trying to be written at once.

## 2. Query the Created Database
1. Record the runtime:
   - I stopped the session early, but this took a couple minutes.
2. Uncomment db.index_record_ids() in query_bacterial_db.py. How does the runtime change? Why?
   - The run time decreased because the database doesn't scan the full table, it just jumps to the relevent rows.

## 3. HDF5 Data
1. Why does chunk configuration make sense? What kind of data access pattern is expected and why does this align with biological use cases?
   - The chunk configuration makes sense because we analyze and work with biological data in batches of proteins, not one protein at a time. When we analyze proteins we analyze them in groups, and HDF5 can read those batches quickly and efficiently. This makes our analyses faster.


