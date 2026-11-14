# Nephro Candidate Score

[![Web tool](https://img.shields.io/badge/web%20tool-nc--scorer.kidney--genetics.org-blue)](https://nc-scorer.kidney-genetics.org/)

The Nephro Candidate Score (N-CS) is a tool for standardized and automatic
prioritization of candidate variants in kidney disease patients. It integrates
information from multiple open-source databases and scores variants based on a
machine learning algorithm.

The N-CS is a machine learning (ML) framework for variant prioritization
combining a Nephro Gene Score (N-GS), Nephro Variant Score (N-VS), and a
heuristic Inheritance Score. The ML-based N-GS and N-VS predict gene-disease
relevance and variant pathogenicity from diverse genomic features. This
repository contains the research code (R and Python) for data acquisition,
feature extraction, training, and predictions of both scores.

Research use only.

## Usage

To score variants, use [nc-scorer](https://github.com/kidney-genetics-org/nc-scorer):

- Web tool for single variant scoring: <https://nc-scorer.kidney-genetics.org/>
- Command line tool for scoring .vcf files:
  <https://github.com/kidney-genetics-org/nc-scorer>

## Documentation

- [Repository details](docs/repository.md): file structure, creators and
  contributors, contact
- Gene score: [`gene_score/`](gene_score/); variant score:
  [`variant_score/`](variant_score/); shared settings in
  [`config_NCS.yml`](config_NCS.yml)
- Related: [nc-scorer](https://github.com/kidney-genetics-org/nc-scorer),
  [kidney-genetics-v1](https://github.com/kidney-genetics-org/kidney-genetics-v1)
  (source of the kidney gene list)

## License

This project is licensed under the terms of the MIT license.
