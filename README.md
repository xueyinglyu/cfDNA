# cfDNA pipeline instruction

### AVID is a sensitive and accurate tool for viral integration detection by next-generation sequencing data.

# 1. Installation
Installation depends on conda. All necessary packages and tools should be set up.
```
sh cfDNA_pipeline.sh [tool_directory]
e.g. sh cfDNA_pipeline.sh /pathowh01/disk1/lyuxy/pipeline/env
```
[env] direcotry do not need to be created.

If these packages and tools cannot be installed successfully by conda, please specify the path of the tools in cfDNA_pipeline.py

Required packages and tools:
<ol>
<li>fastp</li>
<li>bwa</li>
<li>samtools</li>
<li>gatk4</li>
<li>picard</li>
<li>AVID</li>
<li>cnvkit</li>
<li>pandas</li>
<li>numpy</li>
</ol>

# 2. Preparation 
All necessary reference files are located in cfDNA_reference directory. Users need to prepare a list of samples by themselves (e.g. sample.txt).


# 3. Running


