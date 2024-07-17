# hicov
Bioinformatic pipeline for HCoV project (IMI MF UL and Hiscox Lab UL)

Prerequisites:
- Singularity

Usage:
1. Build the Singularity container:
   - sudo singularity build hicov.sif 20240710_hicov.def
   - if no sudo privileges: singularity build --fakeroot hicov.sif 20240710_hicov.def
     
2. Enter hicov.sif:
   ´singularity shell /path/to/hicov.sif/hicov.sif´
     
3. Run the hicov.sh script:
   

