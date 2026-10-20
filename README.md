# Nephro Candidate Score - a tool for automatic prioritization of variants in kidney disease patients

Welcome to the GitHub repository "Nephro Candidate Score". The Nephro Candidate Score (N-CS) is a tool for standardized and automatic prioritization of candidate variants in kidney disease patients. It integrates information from multiple open-source databases and scores variants based on a machine learning algorithm.

## Table of contents

- [Overview and Methods](#overview-and-methods)
- [Usage](#usage)
- [File structure](#file-structure)
- [License](#license)
- [Creators](#creators-and-contributors)
- [Contact](#contact)


## Overview and Methods

The Nephro Candidate Score (N-CS) is a machine learning (ML) framework for variant prioritization combining a Nephro Gene Score (N-GS), Nephro Variant Score (N-VS), and a heuristic Inheritance Score. The ML-based N-GS and N-VS predict gene-disease relevance and variant pathogenicity from diverse genomic features. The composite score provides a standardized, automated, and resource-efficient assessment of candidate variants for genetic kidney diseases.


## Usage

The N-CS is publicly available and accessible. 
* A web tool version for single variant scoring is available at https://nc-scorer.kidney-genetics.org/.
* A command line tool for scoring .vcf files is available at https://github.com/halbritter-lab/nc-scorer.


## File Structure

The repository has the following structure:

```text
.
├── gene_score/
│   ├── features/
│   │   ├── raw/
│   │   ├── results/
│   │   ├── scripts/
│   │   │   ├── cellxgene.R
│   │   │   ├── descartes.R
│   │   │   ├── exon_CpG_o2e_ratio.R
│   │   │   ├── exon_and_prom_conservation.R
│   │   │   ├── gnomad.R
│   │   │   ├── gtex.R
│   │   │   ├── kidney_network.R
│   │   │   ├── mgi_mpo.R
│   │   │   ├── nephrogenesis_atlas.R
│   │   │   ├── paralogues.R
│   │   │   └── promoter_CpG_o2e_ratio.R
│   │   └── helper_functions.R
│   ├── labels/
│   │   ├── raw/
│   │   ├── results/
│   │   └── scripts/
│   │       ├── dispensable_genes.R
│   │       └── positive_genes.R
│   ├── raw/
│   ├── training/
│   ├── gene_score_preprocessing_master.R
│   ├── helper_functions.R
│   └── hgnc_functions.R
└── variant_score/
    ├── features_labels/
    │   ├── results/
    │   └── scripts/
    │       ├── extract_variant_features_per_chrom.py
    │       ├── extract_variant_features_per_chrom.sh
    │       ├── filter_clinvar_vcf_for_kidney_genes.py
    │       ├── preprocess_features_labels.py
    │       ├── variant_annotation.sh
    │       └── vs_helper_functions.py
    ├── predictions/
    │   └── predictions.py
    ├── raw/
    └── training/
        ├── config_files/
        ├── feature_importance/
        ├── raw/
        ├── results/
        ├── scripts/
        │   ├── compare_auc_delong.py
        │   ├── create_train_test_sets.py
        │   ├── get_SHAP_values.py
        │   ├── results_view_and_final_model.py
        │   ├── run_training_vs.py
        │   └── run_training_vs.sh
        └── train_test_data/
```

- The `gene_score/` directory contains all scripts relevant for data acquisition and machine learning development of the gene score. Due to large file sizes, the raw data is not completely stored on GitHub.
- The `variant_score/` directory contains all scripts relevant for variant feature extraction, labels preprocessing, and the training and predictions of the machine learning model for the Nephro Variant Score.


## License

This project is licensed under the terms of the MIT license. For more information, please refer to the [License](LICENSE.md) file.


## Creators and contributors
**Nina Rank**

- <https://github.com/ninarank>
- <https://orcid.org/0000-0002-5984-4836>


**Bernt Popp**

- <https://twitter.com/berntpopp>
- <https://github.com/berntpopp>
- <https://orcid.org/0000-0002-3679-1081>
- <https://scholar.google.com/citations?user=Uvhu3t0AAAAJ>


**Soeren Lukassen**
- <https://github.com/slukassen>
- <https://orcid.org/0000-0001-7045-6327>
- <https://scholar.google.com/citations?user=wWiHGZkAAAAJ&hl=en>


**Constantin Aaron Wolff**

- <https://github.com/ConstantinWolff>
- <https://orcid.org/0000-0002-3277-4559>

**Jan Halbritter**

- <https://orcid.org/0000-0002-1377-9880>
- <https://scholar.google.com/citations?user=Jt1S5fkAAAAJ>

## Contact

If you have any questions, suggestions, or feedback, please feel free to contact nina.rank@charite.de.