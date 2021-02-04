IntAssoPlot: Visualize Genome-Wide Association Study with Gene Annotation and Linkage Disequiblism
====

![GPLv3](http://www.gnu.org/graphics/gplv3-88x31.png)
[GNU General Public License, GPLv3](http://www.gnu.org/copyleft/gpl.html)

![Availability](https://github.com/whweve/IntAssoPlot)

# Installation
## install compiler
The `install_github()`, in the R package remotes, requires that you build from source, thus `make` and compilers must be installed on your system -- see the [R FAQ](http://cran.r-project.org/faqs.html) for your operating system; you may also need to install dependencies manually. 

* For Windows system, rtools, a compiler, is required and can be found at https://cran.r-project.org/bin/windows/Rtools/.

* For Ubuntu/Linux system, compilers could be installed by the command: sudo apt-get install libcurl4-openssl-dev libssl-dev. For more information, please see https://stackoverflow.com/questions/20923209/problems-installing-the-devtools-package.

* install R package devtools and remotes
```R
install.packages(c("devtools","remotes"))
```

## install depended packages, including ggplot2, SNPRelate, ggrepel, gdsfmt and reshape2
```R
#ggplot2, ggrepel, and reshape2 are installed from CRAN
install.packages(c("ggplot2","ggrepel","reshape2"))
#SNPRelate and gdsfmt are installed from Bioconductor
if (!requireNamespace("BiocManager", quietly = TRUE))
    install.packages("BiocManager")
BiocManager::install(c("SNPRelate","gdsfmt"))
```
## install IntAssoPlot from GitHub:
```R
library(remotes) # version 2.1.0
#download, build, and install IntAssoPlot without creating vignette
install_github("whweve/IntAssoPlot")
#download, build, and install IntAssoPlot with creating vignette
install_github("whweve/IntAssoPlot",build=TRUE,build_vignettes = TRUE)
```

# example
```R
#load IntAssoPlot
library(IntAssoPlot)
# an example of association plot at a gene level
example("IntGenicPlot")
# an example of association plot at a region level
example("IntRegionalPlot")
```

# Citation
*If IntAssoPlot is used in your work, you may cite IntAssoPlot.
Fengyu, He, Shuangcheng, Ding, Hongwei, Wang and Feng, Qin. IntAssoPlot: An R Package for Integrated Visualization of Genome-Wide Association Study Results With Gene Structure and Linkage Disequilibrium Matrix. Frontiers in Genetics 2020. doi: 10.3389/fgene.2020.00260.
