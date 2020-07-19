# CellID: gene signature extraction and cell identity recognition at individual cell level

<img src=tools/sticker.png height="100">

CellID take as input a matrix of expression level generated by SCRNA-Seq and performs dimensionality reduction using Multiple Corespondance Analysis. This enables a representation of both genes and cell in the same euclidean space with genes close to a particular cell or group of cells being specificly expressed in those. This property allows to get a ranking of specificity of genes for each cells giving the opportunity to extract meaningful geneset or perform geneset enrichment analysis without any need of clustering.

# Installation

CellID contains dependencies with Biocondutor packages. Please use first `setRepositories()` and type 1 2, to enable the download of bioconducor package.
```r
install.packages("devtools")
setRepositories(ind = c(1,2,3))
devtools::install_github("cbl-imagine/CellID")
```

python umap-learn package can be handy for fast umap computation but is not mandatory.
``` bash
pip install umap-learn
```
# Usage

CellID is used with single cell specific S4objects. Curreltly supported are SingleCellExperiment from Bioconductor and Seurat Version 3 from CRAN.

# Vignettes

You can find a vignette for the basic functionalities and usage of the package [here](https://rauselllab.github.io/CelliD/vignettes/vign.html)

## Authors

* **Akira Cortal** - *Package Maintainer* - [Antonio Rausell Lab](https://github.com/RausellLab)
* **Antonio Rasuell** - *Supervisor* - [Antonio Rausell Lab](https://github.com/RausellLab)

## License

This project is licensed under the GNU General Public License - see the [LICENSE](LICENSE) file for details

# References

* Rausell, A., Juan, D., Pazos, F., & Valencia, A. (2010). Protein interactions and ligand binding: from protein subfamilies to functional specificity. Proceedings of the National Academy of Sciences of the United States of America, 107(5), 1995–2000. [url](https://doi.org/10.1073/pnas.0908044107)

* Aan, Z., & Greenacre, M. (2011). Biplots of fuzzy coded data. Fuzzy Sets and Systems, 183(1), 57–71. [url](https://doi.org/10.1016/j.fss.2011.03.007)

* Alexey Sergushichev. An algorithm for fast preranked gene set enrichment analysis using cumulative statistic calculation. bioRxiv (2016), 
[url](https://doi.org/10.1101/060012)

* Stuart and Butler et al. Comprehensive integration of single cell data. bioRxiv (2018).
[url](https://doi.org/10.1101/460147)

* Aaron Lun and Davide Risso (2019). SingleCellExperiment: S4 Classes for Single Cell Data. R package version 1.4.1.
[url](https://www.bioconductor.org/packages/release/bioc/html/SingleCellExperiment.html)

## Acknowledgments

A big thanks to the fast growing SingleCell community that keeps giving and delivering amazing data and software.
