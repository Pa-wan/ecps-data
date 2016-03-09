# ecps-data

This repository contains the raw data gathered during the experiment described in "Evaluating Container Platforms at Scale" by Jeff Nickoloff.

Each file contains newline delimited samples of the test described by the filename. Any number of tools can be used to analyze the data including R, Rscript, Octave, 

You might even try running the following command to get percentiles:

    docker run --rm -v "$(pwd)"/swarm-results/swarm-run-3000.raw:/tmp/target.digest mesosphere/rscript-curl Rscript -e 'quantile(read.table(file("/tmp/target.digest"))$V1, c(.10, .25, .50, .90, .99))'

Copyright &copy; 2016  Jeff Nickoloff - All in Geek Consulting Services, LLC
