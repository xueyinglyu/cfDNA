# cfDNA pipeline instruction



# 1. Installation
All necessary packages and tools will be set up by conda.
```
sh cfDNA_pipeline.sh [tool_dir]
```

e.g., [env] subdirectory will be created automatically.
```
sh cfDNA_pipeline.sh /pathowh01/disk1/lyuxy/pipeline/env
```


If these packages and tools cannot be installed successfully by conda, please try to install them in other ways and replace the paths of the tools in cfDNA_pipeline.py

Required packages and tools:
<ol>
<li>fastp (https://github.com/OpenGene/fastp)</li>
<li>bwa</li>
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

Users need to prepare a list of samples by themselves before running the pipeline (e.g., sample.txt).

The name of sample matches to fastq files.  e.g., (sample1_1.fastq.gz/sample1_1.fq.gz)


| sample1 | 
| -------- |
| sample2 |
| sample3 |
| sample4 |
| sample5 |


# 3. Running

```
python cfDNA_pipeline.py [tool_dir] sample.txt [out_dir] [cfDNA_reference] [fastq_dir]
```
e.g.
```
python cfDNA_pipeline.py /pathowh01/disk1/lyuxy/pipeline/env/ sample.list /pathowh01/disk1/lyuxy/pipeline/result/ /pathowh01/disk1/lyuxy/pipeline/cfDNA_reference/ /pathowh01/disk1/lyuxy/cfDNA/raw_data/
```
