# sstar

`sstar` is a Python package for detecting archaic introgression from population genetic data with S\* scores (Plagnol and Wall 2006), which can be used for detecting introgression not only in humans, but also in other species, e.g. Kulhwilm et al. (2019).

### Requirements

`sstar` works on UNIX/LINUX operating systems and tested with the following:

- Python 3.8/3.9
- R 4.1
- Python packages:
	- demes
	- numpy
	- pandas
	- rpy2
	- scikit-allel
	- scipy
- R packages:
	- MASS
	- mgcv
	- stat

### Installation

Users should first install [R](https://cran.r-project.org/) and all the R dependencies listed above. Please ensure the path for the dynamic libraries in R is in the environment variable `$LD_LIBRARY_PATH`. For example, if the dynamic libraries in R are in the path `/usr/local/lib/R/lib/`, users can add this path with the following command:

	export LD_LIBRARY_PATH=/usr/local/lib/R/lib:$LD_LIBRARY_PATH

Then users can install `sstar` with `pip`.

	pip install sstar

Users can also use `conda` to create a virtual environment and install `sstar` with this [conda-env.yml](https://github.com/xin-huang/sstar/blob/main/conda-env.yml) or this [environment.yml](https://github.com/admixVIE/sstar-analysis/blob/main/environment.yml) in [sstar-analysis](https://github.com/admixVIE/sstar-analysis). To install `conda`, please follow the [instruction](https://docs.conda.io/projects/conda/en/latest/user-guide/install/index.html). We recommend users use [mamba](https://github.com/mamba-org/mamba) to create the virtual environment, because `mamba` is much faster than `conda`. Then users can use the following commands:

	conda install mamba -n base -c conda-forge
	mamba env create -f conda-env.yml
	conda activate sstar
	export R_LIBS=$CONDA_PREFIX/lib/R/library

Users may verify whether using the correct versions of Python and R under the virtual environment sstar or not with the following commands:

	which python
	which R

And it should return some paths similar to

	/path/to/conda/envs/sstar/bin/python
	/path/to/conda/envs/sstar/bin/R

### Citations

If you find `sstar` is useful, please cite

- Plagnol V, Wall JD. 2006. Possible ancestral structure in human populations. *PLoS Genet*. **2**: e105.
- Vernot B, Akey JM. 2014. Resurrecting surviving Neandertal lineages from modern human genomes. *Science* **343**: 1017–1021.
- Vernot B, et al. 2016. Excavating Neandertal and Denisovan DNA from the genomes of Melanesian individuals. *Science* **352**: 235–239.
- Huang X, Kruisz P, Kuhlwilm M. 2022. sstar: A Python package for detecting archaic introgression from population genetic data with *S*\*. *Mol Biol Evol* **39**: msac212.
