# cfDNA pipeline instruction

### AVID is a sensitive and accurate tool for viral integration detection by next-generation sequencing data.

# 1. Installation
Installation depends on conda. All necessary tools and packages should be set up.
```
git clone https://github.com/xueyinglyu/AVID.git
cd AVID
sh setup.sh
```
if these packages or tools cannot be installed sucessfully by conda, please specify the path of tools in cfDNA_pipeline.py
Required packages and tools:
<ol>
<li>fastp</li>
<li>bwa</li>
<li>samtools</li>
<li>gatk4</li>
<li>picard</li>
<li>AVID</li>
<li>cnvkit</li>
</ol>
# 2. Test AVID
AVID package includes a dataset, necessary references, and indexes for testing. Users can directly run the command below to test the installation without any index file preparation. Users can refer to the example below.


```
sh run_test.sh
```
