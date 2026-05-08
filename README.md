# Comparative Evaluation of Assumption Lean Community Detection Methods for Human Connectome Networks

## Overview

Community detection on resting-state functional connectivity provides a principled lens on mesoscale organization in functional brain networks. Currently, the choice of community count *K*, lacks a standardized or principled guideline. We conducted a systematic benchmark of three assumption-lean approaches on weighted functional connectivity matrices: the Weighted Stochastic Block Model, Spectral Clustering, and K-means Clustering. Performance was assessed on synthetic networks with known ground truth and on three neuroimaging cohorts which included adult and infant datasets. We compared several strategies for selecting *K*, including the silhouette index and other approaches commonly used in the existing literature. These were evaluated alongside a likelihood-based criterion for the weighted stochastic block model that employs bootstrap confidence intervals for differences in log-likelihood between successive values of *K*. For the synthetic networks, WSBM and Spectral Clustering correctly identified the true number of communities, whereas K-means Clustering did not. In adult datasets, most indices did not yield a unique optimum, whereas the likelihood-based criterion selected *K* =11, which is consistent with established sensory and association systems. In infants and toddlers, the same procedure supports a larger *K* around 15 and reveals developmentally distinct mesoscale architecture, including anterior and posterior subdivisions within default mode and fronto parietal systems.

## Main Article

The full article is available at <https://www.biorxiv.org/content/10.1101/2025.11.13.688333v1>.

## Repository Structure

```         
BrainNetworks_WSBM_SC_KM/
│
├── atlases/                      # Brain atlases / region definitions
|
├── biorxiv_manuscript/           # A copy of manuscript
|
├── figures/                      # Figures used in the manuscript
│   └── atlas_figures/            # Atlas figures
│
├── main_functions/               # Scripts to run main pipelines and comparisons
│   ├── atlas_comparison.m
│   ├── consensus.m
│   ├── find_optimal_comm_assignment.m
│   ├── fit_methods.m
│   ├── inter_comparison.m
│   └── intra_comparison.m
|
├── simulation/                   # Synthetic data analysis
│   └── simulation_fc_matrix.m
│
├── support_functions/            # Utility and helper functions
│
├── visualization/                # Plotting and visualization scripts
│   ├── average_fcmatrix_plot.m
│   ├── consensus_surface_plot.m
│   ├── surface_plot.m
│   └── topology_detection.m
|
└──  README.md                    # This file
```

## Requirements

WSBM partition was generated using code from <https://aaronclauset.github.io/wsbm/>.

## Reproducing the Results

1.  Clone the repository:

``` bash
git clone https://github.com/ayoushmanb/BrainNetworks_WSBM_SC_KM.git
cd BrainNetworks_WSBM_SC_KM
```

## Citation

If you use this code or data, please cite:

``` mathematica
@article {bhattacharya2025comparative,
    author = {Bhattacharya, Ayoushman and Chakraborty, Nilanjan and Wang, Xintian and Tu, Jiaxin (Cindy) and Dierker, Donna and Eck, Andy and Lahiri, Soumendra and Eggebrecht, Adam and Wheelock, Muriah D.},
    title = {{Comparative Evaluation of Assumption Lean Community Detection Methods for Human Connectome Networks}},
    elocation-id = {2025.11.13.688333},
    year = {2025},
    doi = {10.1101/2025.11.13.688333},
    publisher = {Cold Spring Harbor Laboratory},
    URL = {https://www.biorxiv.org/content/early/2025/11/14/2025.11.13.688333},
    eprint = {https://www.biorxiv.org/content/early/2025/11/14/2025.11.13.688333.full.pdf},
    journal = {bioRxiv}
}
```
