# Write-up 3: Environment

**Name:** Angelica Alvarado
**Student ID:** avocado  
**Date:** 11/18/2025  

---
---

## 1. Micromamba Questions

Comparing (bioinfo_example_latest.yaml) with the original (bioinfo_example.yaml):

1. What micromamba command can you use to list all created environemnts?
   ***micromamba env list***
3. What micromamba command can you use to list all packages installed in a specific environment?
   ***micromamba list -n env_name***
5. What micromamba command can you use to remove a package?
   ***micromamba remove -n env_name package_name***
7. What micromamba command can you use to install a package from a specific channel?
   ***micromamba install -n env_name -c specific_channel_name package_name***
9. What micromamba command can you use to remove an environment?
    ***micromamba env remove -n bioinfo_example***
11. What are all the r-base and Bioconductor packages that were installed in the bioinfo_example environment?
    ***micromamba list -n bioinfo_example | grep -E "r-base|bioconductor***

You can use some text formating, lists, and tables to imporve the write-up readability
#### **Text Formatting**

You can make text **bold**, *italic*, or even ***bold and italic*** for emphasis.

## 2. Container Questions

#### **Lists**

**Unordered list:**
- Apple  
- Banana  
- Cherry  

**Ordered list:**
1. First step  
2. Second step  
3. Third step  

#### **Table Example**

| Tool | Description         | Example Command        |
|------|---------------------|------------------------|
| `ls` | Lists files         | `ls -la`               |
| `grep` | Searches text     | `grep "pattern" file.txt` |
| `wc` | Counts words/lines  | `wc -l filename.txt`   |

Code snippets and images are highly recommended to document your work.

#### **Code Examples**

**Inline code example:** Use the `print()` function to display text.  

**Code block example:**

```bash
# Example command line code
echo "Hello, Markdown!"
```

```python
# Example Python code
for i in range(3):
    print("Iteration:", i)
```

For longer script, you can say something like, `script1.py` contains functions for reading fasta file. Ideally, all codes you run should be saved in corresponding files. 


#### **Image Example**

![Example placeholder image](./snyderlab.png)

#### **Link Example**

Learn more about Markdown syntax here:  
[Markdown Guide](https://www.markdownguide.org/basic-syntax/)

---


## Acknowledgement
Collaborator: Brady Hislop
