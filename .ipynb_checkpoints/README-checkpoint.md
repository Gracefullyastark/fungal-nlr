## Overview

These are Python scripts for computing highly variable sites in candidate fungal NLRs. The general procedure is as follows:

1) Use hmmer to search reference fungal proteome for candidate NLRs containing certain pfam domains\
2) Use exonerate protein2genome to align candidate NLR to all known genome assemblies in the species\
3) Generate multiple sequence alignment of NLR instraspecies orthologs across the genomes and compute entropy

## Dependencies

I recommend [Anaconda](https://docs.conda.io/projects/conda/en/latest/user-guide/install/macos.html) for installing packages. Visit the Miniconda download page [(link)](https://docs.conda.io/en/latest/miniconda.html) and run the installer 'Miniconda3 MacOSX 64-bit pkg' listed under Python version 3.x.

From this point on you can use ```conda``` or ```pip``` (a package manager included with Anaconda) to install Python packages. Run the following commands in terminal to install any of the following packages you don't already have:

Jupyter notebook:\
```conda install -c conda-forge notebook```

Biopython:\
```pip install biopython```

exonerate:\
```conda config --add channels bioconda```\
```conda install -c bioconda exonerate```


hmmer:\
```conda config --add channels bioconda``` (if you didn't already run it above)\
```conda install -c bioconda hmmer```

clustal omega:\
```conda config --add channels bioconda``` (if you didn't already run it above)\
```conda install -c bioconda clustalo```


## How to use these notebooks

When you run Jupyter notebook, first change to your working directory containing your notebook(s). For example,

```cd ~/```\
```git clone https://github.com/boxu855/fungal-nlr.git```\
```cd fungal-nlr```\
```jupyter notebook```

will open the browser window of the fungal-nlr directory.

Use the *get_ncbi_genomes.ipynb* notebook to download NCBI genomes and proteomes into the *proteomes* and *genomes* directories.


Run the *find_nlr.ipynb* notebook for identifying NLR candidates in the reference proteome, searching for orthologs across genomes, aligning amino acid translations, and saving entropy plots.

### Directories with some output files I have already generated:

*/clustalo_out*: multiple alignments of NLR orthologs by Clustal Omega

*/entropy*: entropy plots and sequences for NLR alignments

*/hmmsearch_out*: hmmsearch output for NLR candidates in reference proteoms



