Engineer 1: Kasandra Pepkolaj

DNAscent v2: detecting replication forks in nanopore sequencing data with deep learning by Michael A. Boemo.
Github link: https://github.com/MBoemo/DNAscent

	1. Used a Kali Linux Virtual Machine to install Singularity/Apptainer since it's better suited to use this container in Linux systems.
	2. Tried running the singularity image provided, but it wasn't possible since my primary machine is Apple Silicon Mac, while the image only runs on x86_64 intel AMD machines. 
	3. Tried the building from source method provided. Followed the steps, didn't work since the Makefile tries to download and compile an old version of HDF5 as a dependency. Need to install HDF5 from my system packages. Used command sudo apt install libhdf5-dev. 



