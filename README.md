## To use the container, you need singularity in your PATH:

export PATH=/primary/vari/software/singularity/singularity-3.5.2/bin:$PATH

## We are going to install R packages locally since the container is immutable, for good reason.

## To run the container and bind a directory to install packages from within the container:

singularity shell -B /secondary/projects/triche/tools/bioc_devel_singularity/R_pkg_local_lib:/usr/local/lib/R/host-site-library /secondary/projects/triche/tools/bioc_devel_singularity/latest/bioconductor_docker_devel.sif

## Now you should be able to work interactively

## Startup R
Singularity> R

## Install packages as usual
>BiocManager::install("scater")
