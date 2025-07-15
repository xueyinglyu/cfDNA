# cfDNA pipeline instruction



# 1. Installation
All necessary packages and tools will be set up in [tool_dir] by conda. 
```
sh cfDNA_pipeline.sh [tool_dir]
```

e.g., 
```
sh cfDNA_pipeline.sh /pathowh01/disk1/lyuxy/pipeline/
```

If the installation is successful, subdirectories will be generated as below:

[tool_dir]

-[env]

--[tools]

--[AVID]

--[cnvkit]

## Tips
1. If one of the tools called cnvkit cannot be installed successfully, please update conda, add necessary channels (conda-forge and bioconda), and try the installation again.
 
2. If these packages and tools cannot be installed successfully by conda, please try to install them in other ways and replace the paths of the tools in cfDNA_pipeline.py

Required packages and tools:
<ol>
<li>fastp (https://github.com/OpenGene/fastp)</li>
<li>bwa (https://github.com/lh3/bwa)</li>
<li>samtools (https://www.htslib.org/download/)</li>
<li>gatk4 (https://github.com/broadinstitute/gatk/releases)</li>
<li>picard (https://broadinstitute.github.io/picard/)</li>
<li>AVID (https://github.com/xueyinglyu/AVID)</li>
<li>cnvkit (https://pypi.org/project/CNVkit/)</li>
<li>pandas</li>
<li>numpy</li>
<li>pysam</li> 
</ol>

# 2. Preparation 
All necessary reference files are located in [cfDNA_reference] directory. 

Users need to prepare a list of samples by themselves before running the pipeline (e.g., sample.list).

The name of sample matches to fastq file.  e.g., (sample1_1.fastq.gz, sample1_1.fq.gz, sample1_R1.fastq.gz or sample1_R1.fq.gz)

| sample1 |
| --------|
| sample2 |
| sample3 |
| sample4 |
| sample5 |


# 3. Execution

Run the pipeline to generate files for each sample. 

[tool_dir]: directory of installed tools, created in the first step of installation.

[out_dir]: output directory.

[cfDNA_reference]: reference files, provided by the pipeline.

[fastq_dir]: directory of fastq files.

```
python cfDNA_pipeline.py [tool_dir] sample.list [out_dir] [cfDNA_reference] [fastq_dir]
cd [out_dir]/script
sh sample1.sh
sh sample2.sh
...
```
e.g.,
```
python cfDNA_pipeline.py /pathowh01/disk1/lyuxy/pipeline/ sample.list /pathowh01/disk1/lyuxy/pipeline/result/ /pathowh01/disk1/lyuxy/pipeline/cfDNA_reference/ /pathowh01/disk1/lyuxy/cfDNA/raw_data/
cd /pathowh01/disk1/lyuxy/pipeline/result/script
sh 8846_cfDNA.sh
```

# 4. Output

Below directories will be created under [out_dir]. Please copy these directories (cnvkit, endmotif, HBV, mpileup, SNV) to the hard disk. Thank you!

|   bam    |
| -------- |
|  cnvkit  |
|  endmotif |
|   fastp   |
|    HBV   |
|   mpileup  |
|   script   |
|      SNV      |









