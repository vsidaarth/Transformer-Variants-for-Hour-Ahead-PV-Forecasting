# Transformer Benchmarks for Hour-Ahead PV Forecasting

[![DOI](https://img.shields.io/badge/DOI-10.3390%2Fen18185000-blue)](https://doi.org/10.3390/en18185000)
[![License: CC0-1.0](https://img.shields.io/badge/License-CC0--1.0-lightgrey.svg)](LICENSE)

Research code and experimental data accompanying the paper:

> V. Suresh, “Benchmarking Transformer Variants for Hour-Ahead PV Forecasting: PatchTST with Adaptive Conformal Inference,” *Energies*, vol. 18, no. 18, article 5000, 2025. https://doi.org/10.3390/en18185000

## Overview

This repository provides a common experimental implementation for benchmarking modern time-series architectures for hour-ahead photovoltaic (PV) power forecasting. It compares PatchTST, Informer, FEDformer, Autoformer, and DLinear using the same data and evaluation setting. The study then combines the strongest deterministic model, PatchTST, with Adaptive Conformal Inference (ACI) to generate uncertainty-aware forecasts.

## Scientific contribution

- A controlled comparison of five modern forecasting architectures for the same hour-ahead PV task.
- Application of PatchTST to short-term PV power forecasting.
- Integration of PatchTST with ACI to produce adaptive prediction intervals.
- Joint evaluation of point accuracy, interval reliability, interval sharpness, and computational cost.

## Main results

PatchTST achieved an MAE of **0.194 kW** and an RMSE of **0.381 kW**. PatchTST–ACI achieved **86.2% empirical coverage**, a **0.62 kW mean interval width**, a **0.54 CRPS**, and a **1.86 Winkler score**. These values refer to the experimental setting reported in the paper; consult the article for the complete protocol and interpretation.

## Repository contents

| File | Purpose |
| --- | --- |
| **PatchTST.ipynb** | PatchTST forecasting workflow and the principal model used with ACI |
| **Informer.ipynb** | Informer benchmark |
| **FEDformer.ipynb** | FEDformer benchmark |
| **Solar_Autoformer.ipynb** | Autoformer benchmark |
| **DLInear2.ipynb** | DLinear benchmark |
| **updated_timetable.txt** | Data file used by the notebooks |

## Reproducing the experiments

1. Clone or download this repository.
2. Open the required notebook in Jupyter or Google Colab.
3. Keep **updated_timetable.txt** in the repository root, or update the data path in the notebook.
4. Install the Python packages imported at the beginning of the selected notebook.
5. Run the notebook cells in order.

Random initialization, library versions, and hardware can lead to small numerical differences. The paper is the authoritative source for the final experimental configuration and reported results.

## Citation

If this repository supports your work, please cite:

~~~bibtex
@article{suresh2025transformer,
  author  = {Suresh, Vishnu},
  title   = {Benchmarking Transformer Variants for Hour-Ahead PV Forecasting: PatchTST with Adaptive Conformal Inference},
  journal = {Energies},
  volume  = {18},
  number  = {18},
  pages   = {5000},
  year    = {2025},
  doi     = {10.3390/en18185000}
}
~~~

## License

This repository is released under the [CC0 1.0 Universal license](LICENSE). Please cite the associated paper when using the research implementation or results.
