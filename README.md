# Snakemake example

This is an example of [Snakemake](https://snakemake.readthedocs.io/en/stable/) installation for Stanage HPC.

This repository contains a Snakemake workflow that is organised following the guidance on the [Distribution and Reproducibility](https://snakemake.readthedocs.io/en/stable/snakefiles/deployment.html) page on the Snakemake documentation.

# Installation

Load the [Anaconda module](https://docs.hpc.shef.ac.uk/en/latest/stanage/software/apps/python.html#gsc.tab=0):

```bash
module load Anaconda3
```

Create a new Conda virtual environment that [contains Snakemake](https://snakemake.readthedocs.io/en/stable/getting_started/installation.html):

```bash
conda create -n snakemake-env -c conda-forge conda=25 bioconda::snakemake=8
```

Activate the virtual environment:

```bash
source activate snakemake-env
```

# Usage

[Run the workflow](https://snakemake.readthedocs.io/en/stable/executing/cli.html) defined in [`Snakefile`](./Snakefile):

```bash
snakemake --sdm conda
```

For more information about [writing workflows](https://snakemake.readthedocs.io/en/stable/snakefiles/writing_snakefiles.html) please consult the [Snakemake documentation](https://snakemake.readthedocs.io/en/stable/index.html).
