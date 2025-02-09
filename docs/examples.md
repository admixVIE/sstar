# Examples

A Snakefile for running the whole pipeline can be found [here](https://github.com/xin-huang/sstar/blob/main/examples/snakepipe/Snakefile).

Users need to install `conda` first. See [conda installation](https://docs.conda.io/projects/conda/en/latest/user-guide/install/index.html) for instruction. We recommend users use [mamba](https://github.com/mamba-org/mamba) to create the virtual environment, because `mamba` is much faster than `conda`.

Users can dry-run the whole pipeline as follows:

	git clone https://github.com/xin-huang/sstar
	cd ./sstar/examples/snakepipe
	conda install mamba -n base -c conda-forge
	mamba env create -f conda-env.yml
	conda activate sstar
	export R_LIBS=$CONDA_PREFIX/lib/R/library
	snakemake -n -p

Users can use `snakemake -c 1` for running the whole pipeline locally or submit jobs to `SLURM` with `mkdir logs_slurm && snakemake --profile . -j 1`. Users can modify [config.yaml](https://github.com/xin-huang/sstar/blob/main/examples/snakepipe/config.yaml) for submitting jobs to other scheduling system, such as `SGE`.
