# tensorOmics: Data integration for longitudinal omics data using tensor factorisation

Saritha Kodikara<sup>1,&amp;</sup>,
Brendan Lu<sup>1,&amp;</sup>,
Shuhe Wang<sup>1,2</sup>,
Ziqi Lei<sup>1</sup>,
Kim-Anh Lê Cao<sup>1,&ast;</sup>

<sup>1</sup> Melbourne Integrative Genomics, School of Mathematics and Statistics, The University of Melbourne, Royal Parade, 3052, Victoria, Australia

<sup>2</sup> Department of Biostatistics, University of Washington, Seattle, WA, USA

<sup>&amp;</sup> Joint first authors. &nbsp; <sup>&ast;</sup> Corresponding author.

## Abstract

Longitudinal multi-omics studies profile molecular changes across biological layers and
over time, but their analysis must account for dependence among repeated measurements
from the same subject. Conventional matrix approaches often flatten this temporal
structure. Although tensor methods preserve the multi-way organisation of the data,
existing approaches are predominantly unsupervised or limited to a single omic, leaving
few options for phenotype-guided analysis of several longitudinal omics datasets.

We present tensorOmics, a framework of five tensor methods for exploratory analysis,
regression, classification and multi-omics integration. The framework represents each
subject's trajectory in an orthogonal temporal basis, retains subjects as the unit of
analysis and enables fitted models to score new subjects. We evaluated tensorOmics in
simulations with known temporal signals, by subject-level cross-validation in three
larger public longitudinal cohorts, and in three biological case studies. These
evaluations examined the recovery of group differences encoded in trajectory shape,
prediction in held-out subjects, multi-omics integration, and interpretation of the
temporal patterns and molecular features identified by the models. tensorOmics provides
a unified set of R tools for analysing longitudinal single- and multi-omic data while
retaining their temporal structure.

tensorOmics is available as an [R package](https://github.com/brendanlu/tensorOmics).

---

## Repository contents

This repository holds the case studies reported in the manuscript. Each folder contains
one worked example, with its data, its analysis file and the rendered report.

| folder | case study | data |
|---|---|---|
| [`CS1-Antibiotic_Study`](CS1-Antibiotic_Study) | Microbiome recovery after an antibiotic course, comparing PCA, PLS-DA, tPCA, TEMPTED and tPLS-DA | `data/` |
| [`CS2-Ammonia_Study`](CS2-Ammonia_Study) | Metabolite dynamics in anaerobic digestion under ammonia inhibition | `Data_org/`, `Data_filtered/` |
| [`CS3-FMT-HIV_Study`](CS3-FMT-HIV_Study) | Multiblock integration of taxonomic, functional and protein profiles after faecal microbiota transplantation | `data/`, `data_filtered/` |

Each case study has a `Case study N.Rmd` and the corresponding rendered
`Case-study-N.html`. The [`helper`](helper) folder holds the plotting function shared by
the case studies.

Case studies 1 and 3 report results produced with the development version of
`tensorOmics`, and their analysis chunks are not evaluated when the files are rendered.
Each of those files opens with a software note saying so.

## Requirements

- R 4.4.0 or later
- [tensorOmics](https://github.com/brendanlu/tensorOmics)
- The other R packages are listed in each rendered `.html` file, with the version we used.

## Data sources

The data in this repository were produced by other researchers. If you use them, please
cite the original source as well as this repository.

- **Case study 1.** Suez J, Zmora N, Zilberman-Schapira G, et al. (2018). Post-antibiotic
  gut mucosal microbiome reconstitution is impaired by probiotics and improved by
  autologous FMT. *Cell*. We used the normalised dataset provided by Mor U, Cohen Y,
  Valdés-Mas R, et al. (2022). Dimensionality reduction of longitudinal 'omics data using
  modern tensor factorizations. *PLOS Computational Biology*.
- **Case study 2.** Wang X, Campuzano S, Guenne A, Mazéas L, Chapleur O (2024). Inhibition
  of anaerobic digestion by various ammonia sources resulted in subtle differences in
  metabolite dynamics. *Chemosphere*.
- **Case study 3.** Díaz-García C, Moreno E, Talavera-Rodríguez A, et al. (2024). Faecal
  microbiota transplantation alters the proteomic landscape of inflammation in HIV:
  identifying bacterial drivers. *Microbiome*.

## Citation

If you use this code or data, please cite the tensorOmics manuscript (reference to follow
on publication) and the original source of any dataset you use, listed above.

GitHub's "Cite this repository" button, built from [`CITATION.cff`](CITATION.cff), gives
the citation in APA and BibTeX formats.

## Licence

- **Code** (the R code in the `.Rmd` files, the scripts and the helper functions) is
  licensed under the [GNU Affero General Public License v3.0](LICENSE).
- **Documentation, figures, rendered reports and processed data** are licensed under
  [Creative Commons Attribution 4.0](LICENSE-docs-data.md). The original datasets remain
  under their own terms and must be cited; see [Data sources](#data-sources) above.

## Questions and issues

- For questions about these case studies, please
  [open an issue](https://github.com/lecaolab/lecaolab-paper-tensorOmics/issues) here.
- For bugs or feature requests in the tensorOmics package itself, please open an issue in
  [brendanlu/tensorOmics](https://github.com/brendanlu/tensorOmics/issues).

See [`CONTRIBUTING.md`](CONTRIBUTING.md) and our [Code of Conduct](CODE_OF_CONDUCT.md).

---

Developed at the [Lê Cao Lab](https://lecao-lab.science.unimelb.edu.au/), The University
of Melbourne.
