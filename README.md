# hicov
Bioinformatic pipeline for HCoV project (IMI MF UL and Hiscox Lab UL)

When in doubt, write alen.suljic@mf.uni-lj.si

Prerequisites:
- Singularity (https://singularity-tutorial.github.io/01-installation/)

Usage:
1. Build the Singularity container:
```
sudo singularity build hicov.sif 20240710_hicov.def
singularity build --fakeroot hicov.sif 20240710_hicov.def #if no sudo privileges
```
2. Enter hicov.sif:
```
singularity shell /path/to/hicov.sif/hicov.sif
```
     
3. Run the hicov.sh script:
```
bash hicov.sh hcov_nl63 /path/to/data.fastq.gz
```


Best use example:
1. To avoid issues with data naming, follow the convention in example (sample name should include only "-".
Read orientation is delimited by "_".):
   - hcov-0001_R1.fastq.gz
   - hcov-0001_R2.fastq.gz
   - ...
  
2. Create a directory where desired.
3. Copy the hicov.sh script and "reference" directory to created directory.
4. Enter hicov.sif container.
5. Optional: If required, open the hicov.sh with your favourite text editor and adjust pipeline parameters (thread count, quality settings, etc...).
6. Run the hicov.sh script. The script takes reference name as positional argument 1 and input data (fastq.gz) directory as positional argument 2.
7. Additional information is provided in header section in hicov.sh script.
   
# micov

micov is an ONT counterpart of hicov. It follows the exact same logic, with the exception of raw read naming convention (hcov-0001.fastq.gz, instead of hcov-0001_R1.fastq.gz).
