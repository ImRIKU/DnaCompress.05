# DnaCompress.05
temporary adding.

## jarvis and jarvis2 and jarvis3 repo

https://github.com/cobilab/jarvis.git
https://github.com/cobilab/jarvis2.git
https://github.com/cobilab/jarvis3.git


# Changes made to add cpu and ram usage
1. cpuUsage.c file was added in src directory of jarvis, jarvis2, jarvis3, geco
2. the files containing main method are modified
      like jarvis.c, jarvis2.c, jarvis3.c.
      extern function is declared and cpuusage function is called at the beginning of main() function which stops at the end of the compression/decompression and shows the result.
3. Makefile is modified to add cpuUsage.c to the project.

# To compile go to the jarvis/src folder and run
make


## Only for raw file (CONTAINING A/C/G/T only)
# Jarvis2 run
SAMPLE                                                             
      Run Compression   -> ./JARVIS2 -v -l 30 sequence.txt          
      Run Decompression -> ./JARVIS2 -v -d sequence.txt.jc   

# Jarvis3 run
SAMPLE                                                             
      Run Compression   -> ./JARVIS3 -v -l 14 sequence.txt         
      Run Decompression -> ./JARVIS3 -v -d sequence.txt.jc 

## For .fa and .fastq files

# JARVIS2

First, make sure to give permissions to the script by typing the following at the src/ folder

chmod +x JARVIS2.sh
The extension of compressing FASTA and FASTQ data contains a menu to expose the parameters that can be accessed using:

./JARVIS2.sh --help
Preparing JARVIS2 for FASTA and FASTQ:

./JARVIS2.sh --install
Compression of FASTA data:

./JARVIS2.sh --threads 8 --fasta --block 10MB --input sample.fa
Decompression of FASTA data:

./JARVIS2.sh --decompress --fasta --threads 4 --input sample.fa.tar
Compression of FASTQ data:

./JARVIS2.sh --threads 8 --fastq --block 40MB --input sample.fq
Decompression of FASTQ data:

./JARVIS2.sh --decompress --fastq --threads 4 --input sample.fq.tar

# JARVIS3


./JARVIS3.sh --install
Compression of FASTA data:

./JARVIS3.sh --threads 8 --fasta --block 10MB --input sample.fa
Decompression of FASTA data:

./JARVIS3.sh --decompress --fasta --threads 4 --input sample.fa.tar
Compression of FASTQ data:

./JARVIS3.sh --threads 8 --fastq --block 40MB --input sample.fq
Decompression of FASTQ data:

./JARVIS3.sh --decompress --fastq --threads 4 --input sample.fq.tar

# Limitations: 
Jarvis3 does not properly work with .fastq files.