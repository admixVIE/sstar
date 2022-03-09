# Examples

A Snakefile for running the whole pipeline can be found [here](https://github.com/xin-huang/sstar/blob/main/examples/snakepipe/Snakefile).

Users need to install `conda` first. See [conda installation](https://docs.conda.io/projects/conda/en/latest/user-guide/install/index.html) for instruction.

Users also need to download two tables for source match percentages from the reference population with the following commands:

	wget -c https://figshare.com/ndownloader/files/34320419
	mv 34320419 sstar_supplementary_data.tar.gz
	tar -xvf sstar_supplementary_data.tar.gz

Users can dry-run the whole pipeline as follows:

	git clone https://github.com/xin-huang/sstar
	cd ./sstar/examples/snakepipe
	conda env create -f conda-env.yaml
	conda activate sstar
	snakemake -n -p

Users can use `snakemake -c 1` for running the whole pipeline locally or submit jobs to `SLURM` with `mkdir logs_slurm && snakemake --profile . -j 1`.