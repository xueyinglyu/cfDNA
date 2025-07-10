# cfDNA pipeline instruction

### AVID is a sensitive and accurate tool for viral integration detection by next-generation sequencing data.

# 1. Installation
Installation depends on conda. All necessary packages and tools should be set up.
```
sh cfDNA_pipeline.sh [tool_dir]
```

e.g.
```
sh cfDNA_pipeline.sh /pathowh01/disk1/lyuxy/pipeline/env
```
[env] directory does not need to be created.

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

```
python cfDNA_pipeline.py [tool_dir] sample.txt [out_dir] [cfDNA_reference] [fastq_dir]
```
e.g.
```
python cfDNA_pipeline.py /pathowh01/disk1/lyuxy/pipeline/env/ sample.list /pathowh01/disk1/lyuxy/pipeline/result/ /pathowh01/disk1/lyuxy/pipeline/cfDNA_reference/ /pathowh01/disk1/lyuxy/cfDNA/raw_data/
```
