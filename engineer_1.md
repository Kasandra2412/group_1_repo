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
	* The singularity image also didn't recognize my computer's architecture. After a few changes it seemed that files were being downloaded but this lead to my computer beeping, which signified some RAM issues.

2. Building from Source
	* Cloned the repository: `git clone --recursive https://github.com/MBoemo/DNAscent.git`
	* Followed these commands: `cd DNAscent` --> `git checkout 4.1.1` --> `make`
	* `make` caused errors due to older dependencies. DNAscent tried to download HDF5 version 1.8.14 (2014 version) and compile it manually. However, this version is very old and the scripts didn't recognize ARM64 architecture.
	* tried updating the scripts, config.guess and config.sub, but this also didn't work.
	* tried changing the Makefile manually, and this didn't work. I kept getting errors about dependencies that only work with x86_64 architecture.