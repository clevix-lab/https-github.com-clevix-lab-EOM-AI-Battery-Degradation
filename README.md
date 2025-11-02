# EOM-AI: Entropic Exponents Reveal Universal Degradation Attractors in Lithium-Ion Batteries

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.XXXXXXX.svg)](https://doi.org/10.5281/zenodo.XXXXXXX)  
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)  
[![Python 3.9+](https://img.shields.io/badge/python-3.9+-blue.svg)](https://www.python.org/downloads/)  
[![Nature Energy](https://img.shields.io/badge/Nature%20Energy-under%20review-red)](https://www.nature.com/nenergy/)

---

## **Abstract (Nature Energy, 2025)**

> **Battery degradation remains a critical barrier to electric vehicle adoption, costing over $10 billion annually in lost capacity.**  
> Here we introduce **Entropy-Oriented Mechanics (EOM)**, a thermodynamic-control framework that defines the **entropic Lyapunov exponent**  
> $\lambda_\text{EOM} = \dot{\Sigma}/\Sigma$ as a **universal degradation metric**.  
>  
> Using **7,000+ real-world drive cycles from NASA, Oxford, and CALCE datasets**, we reveal a **global stability attractor** at  
> $(\lambda_\text{EOM}, \kappa_\text{EOM}, \Sigma_\text{EOM}) = (0, 0, 0)$ in healthy cells.  
>  
> In degraded operation, $\lambda_\text{EOM}$ scales with **internal resistance** ($r = 0.71$, $p < 10^{-200}$) and **power loss** ($r = 0.28$),  
> forming an **entropy–impedance bridge** and **energy–entropy balance law**.  
>  
> A **3D Pareto manifold** defines the **Entropy Efficiency Zone**, enabling **AI-driven control** that  
> **reduces entropy production by 23–35%** and **extends lifetime by 25%**.  
>  
> **EOM-AI outperforms phenomenological models**, offering a **physics-informed path to next-generation battery management**.

---

## **Citation**

```bibtex
@article{truong2025eom,
  title     = {Entropic Exponents Reveal Universal Degradation Attractors in Lithium-Ion Batteries},
  author    = {Trương, Xuân Khánh and Trương, Quỳnh Hoa and Co-Author},
  journal   = {Nature Energy},
  year      = {2025},
  doi       = {10.1038/s41560-025-XXXXX},
  url       = {https://doi.org/10.1038/s41560-025-XXXXX},
  note      = {Under review}
}

Key Results
Metric,EOM-AI,Severson (2019),Ma et al. (2024)
SOH RMSE (%),1.8,3.2,2.9
RUL Error (cycles),42,85,68
Entropy-aware?,Yes,No,Partial
Cross-chemistry?,Yes (NMC + LFP),No,No
25% lifetime extension via EOM-AI control
Entropy–Impedance Bridge: $r = 0.71$, $p < 10^{-200}$

Quick Start
# 1. Clone repo
git clone https://github.com/clevix-lab/EOM-AI-Battery-Degradation.git
cd EOM-AI-Battery-Degradation

# 2. Create environment
conda env create -f environment.yml
conda activate eom-ai

# 3. Run full pipeline
python scripts/EOM_AI_Extended.py --all

# 4. View results
open results/figures/FIG_2_lambda_vs_Rint_3datasets.png

Data Sources
Dataset,Chemistry,Profiles,Temperature,DOI / Link
NASA,NMC,Randomized Walk,24°C,NASA PCoE
Oxford,NMC,Artemis Urban,40°C,10.5281/zenodo.166230
CALCE,LFP,"DST, US06, FUDS","0°C, 25°C, 50°C",calce.umd.edu
Cross-chemistry (NMC → LFP) and cross-temperature (0–50°C) validation.

Repository Structure
EOM-AI-Battery-Degradation/
├── data/                  ← Raw data (sample only)
├── scripts/               ← Python pipeline
├── results/               ← Tables & Figures
├── paper/                 ← LaTeX (Nature Energy)
├── docs/                  ← Installation, Citation
└── .github/workflows/     ← CI/CD

Reproducibility

Environment: environment.yml (conda)
Tested on: Python 3.9–3.11, macOS/Linux/Windows
CI: GitHub Actions (.github/workflows/ci.yml)
DOI: Zenodo XXXXXXX

Contact
H/&K Research Lab
Clevix LLC, Hanoi, Vietnam
Email: khanh@clevix.vn
Website: clevix.vn

