## To use the container, you need singularity in your PATH:

export PATH=/primary/vari/software/singularity/singularity-3.5.2/bin:$PATH

## We are going to install R packages locally since the container is immutable,$

## To run the container and bind a directory to install packages from within th$

singularity shell -B /secondary/projects/triche/tools/bioc_devel_singularity/R_$

## Now you should be able to work interactively

## Startup R
Singularity> R

## Install packages as usual
>BiocManager::install("scater")
