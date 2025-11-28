***Engineer 1: Kasandra Pepkolaj***

# Report 1 - DNAscent v2

---

**Paper:** DNAscent v2: detecting replication forks in nanopore sequencing data with deep learning by Michael A. Boemo.
**Github link:** (https://github.com/MBoemo/DNAscent)
**Results:** Not reproducible due to computer architecture incompatibility.
** Tools used:** Ubuntu VM, ChatGPT, Claude AI, Google, git, singularity

---

## **Main issues:**
1. Pre-build Singularity containers were designed for x86_64 architecture, not ARM64 architecture of my laptop. Tried using Singularity image that might work on ARM64 but the size was too big and I encountered hardware warnings (continuous beeping).
2. DNAscent relies on very old dependencies, HDF5 1.8.14, which is not designed for ARM64. Tried to install dependency according to the right architecture, but kept getting architecture errors and compiling issues.

---

# **Steps taken:**

1. Singularity image
	* Copied the commands provided from the instructions on the Github. The recommended way was to run the DNAscent via the supported Singularity images through running:  `singularity pull DNAscent.sif library://mboemo/dnascent/dnascent:4.1.1.`
	* The singularity image also didn't recognize my computer's architecture. After a few changes it seemed that files were being downloaded but this lead to my computer beeping, which signified some RAM issues.h

2. Building from Source
	* Cloned the repository: `git clone --recursive https://github.com/MBoemo/DNAscent.git`
	* Followed these commands: `cd DNAscent` --> `git checkout 4.1.1` --> `make`
	* `make` caused errors due to older dependencies. DNAscent tried to download HDF5 version 1.8.14 (2014 version) and compile it manually. However, this version is very old and the scripts didn't recognize ARM64 architecture.
	* tried updating the scripts, config.guess and config.sub, but this also didn't work.
	* tried changing the Makefile manually, and this didn't work. I kept getting errors about dependencies that only work with x86_64 architecture.
	
---

# Report 2 - OKseqHMM

---

**Paper:** OKseqHMM: a genome-wide replication fork directionality analysis toolkit
**Github link:** (https://github.com/CL-CHEN-Lab/OK-Seq)
**Results:** Reproduced!
** Tools used:** Ubuntu VM, R, ChatGPT, Google, git, samtools 

---

# **Steps taken:**
1. Used a Ubuntu VM instead of Mac, since Mac was presenting package compilation issues. In the VM first step was to download tools and R. Used this command: `sudo apt install -y build-essential libcurl4-gnutls-dev libxml2-dev libssl-dev \  libbz2-dev liblzma-dev zlib1g-dev wget curl git r-base r-base-dev'. 
2. Cloned the github link and received the folder and subfolders. The authors provided sample data of BAM files that can be used. Within the 
template folder there is sample data and a script template.
3. Opened R and installed packages HMM from CRAN and BiocManager. Then I installed the Bioconductor packages (Rsamtools, GenomicAlignments)
4. Dowloaded the zip file provided that contained the BAM file: `wget http://xfer.curie.fr/get/LfyDX92pNQs/template.bam.zip` and unzipped it: `unzip template.bam.zip` --> received the BAM files as *template_chr21_22.bam and template-chr21_22.bam.bai*.
5. Loaded OKseqHMM in R and ran OKseqHMM in R based on the template script they provided:
```OKseqHMM(bamfile = "template_chr21_22.bam", thresh=10, chrsizes = "hg19.chr.size.txt",winS=15, fileOut = "hmm",binSize=1000)```
and received the files in the current directory.
6. Loaded OKseqOEM in R and ran the code provided in the template:
```OKseqOEM(bamInF = "hmm_fwd.bam",
         bamInR = "hemm_rev.bam",
         chrsizes = "hg19.chr.size.txt",
         fileOut ="hela_OEM",
	 binsize=1000,
	 binList=c(1,10,20,50,100,250,500,1000))```
and received the .wig files.
	* During this phase I encountered issues with my files from OkseqHMM, mostly due to OKseqOEM trying to detect mapped reads in chr1 and the hg19.chr.size.txt only included up to chr19, while the mapped read of my files were in chr21-ch22. 
	* Ran `samtools view -c hmm_fwd.bam` and `samtools view -c hmm_rev.bam` to confirm that there was data available in my files. Ran `samtools idxstats hmm_fwd.bam` to see where the reads were mapped to. It showed  that chr11-chr20 had no mapped reads and only chr21-ch22 were mapped.
	* Had to create a new file and enter chr21   48129895 chr22   51304566 and used this file instead of the one provided on github. After running OKseqOEM again i finally received the .wig files.
	
**Final Product - Visualized**

