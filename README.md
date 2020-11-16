I highly recommend installing [Anaconda](https://docs.conda.io/projects/conda/en/latest/user-guide/install/macos.html) if you haven't already done so. It allows you to install many packages with just a single command. Visit the Miniconda download page [(link)](https://docs.conda.io/en/latest/miniconda.html) and run the installer 'Miniconda3 MacOSX 64-bit pkg' listed under Python version 3.x.

From this point on you can use ```conda``` or ```pip``` (a package manager included with Anaconda) to install Python packages. Run the following commands in terminal to install any of the following packages you don't already have:

Jupyter notebook:

```conda install -c conda-forge notebook```

Biopython:

```pip install biopython```

exonerate:

```conda config --add channels bioconda```

```conda install -c bioconda exonerate```


hmmer:

```conda config --add channels bioconda``` (if you didn't already run it above)

```conda install -c bioconda hmmer```

clustal omega:

```conda config --add channels bioconda``` (if you didn't already run it above)

```conda install -c bioconda clustalo```


Whenever you run Jupyter notebook, you should first change to your working directory containing your notebook(s). For example, if you want to use the notebooks I made for this fungal-nlr repository, you should clone the repository using ```git```, ```cd``` to the repository, then run ```jupyter notebook```. In terminal,


```
cd ~/
git clone fungal-nlr
cd fungal-nlr
jupyter notebook
```

will open the browser window of the fungal-nlr directory.

## How to use fungal-nlr

First, use the "get_ncbi_genomes.ipynb" notebook to download NCBI genomes and proteomes into the '/proteomes' and '/genomes' directories.

For the main pipeline of identifying NLR candidates in the reference proteome, searching for orthologs across genomes, aligning amino acid translations, and saving entropy plots, run the "find_nlr.ipynb" notebook

### Directories with some output files I have already generated:

'/clustalo_out': multiple alignments of NLR orthologs by Clustal Omega

'/entropy': entropy plots and sequences for NLR alignments

'/hmmsearch_out': hmmsearch output for NLR candidates in reference proteoms



