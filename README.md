# Entropic Exponents Reveal Universal Degradation Attractors in Lithium-Ion Batteries

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.XXXXXXX.svg)](https://doi.org/10.5281/zenodo.XXXXXXX)  
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)  
[![Python 3.9+](https://img.shields.io/badge/python-3.9+-blue.svg)](https://www.python.org/downloads/)  
[![Nature Energy](https://img.shields.io/badge/Nature%20Energy-under%20review-red)](https://www.nature.com/nenergy/)

---

## **Abstract**

> **Battery degradation remains a critical barrier to electric vehicle adoption, costing over $10 billion annually in lost capacity.**  
> Here we introduce **Entropy-Oriented Mechanics (EOM)**, a thermodynamic-control framework that defines the **entropic Lyapunov exponent**  
> $\lambda_\text{EOM} = \dot{\Sigma}/\Sigma$ as a universal degradation metric.  
>  
> Using **7,000+ real-world drive cycles from NASA and Oxford datasets**, we reveal a **global stability attractor** at  
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

## **Authors & Correspondence**

**Truong Xuan Khanh¹,²,***, **Truong Quynh Hoa¹**, **Co-Author²**  

¹ H/&K Research Lab, Clevix LLC, Hanoi, Vietnam  
² H/&K Research Lab, Clevix LLC, Hanoi, Vietnam  

*Correspondence: khanh@clevix.vn

---

## **Key Results**

| Metric | EOM-AI | Severson (2019) | Ma et al. (2024) |
|--------|--------|------------------|------------------|
| **SOH RMSE (%)** | **1.8** | 3.2 | 2.9 |
| **RUL Error (cycles)** | **42** | 85 | 68 |
| **Entropy-aware?** | Yes | No | Partial |
| **Cross-chemistry?** | Yes (NMC + LFP) | No | No |

> **25% lifetime extension** | **Entropy–Impedance Bridge**: $r = 0.71$, $p < 10^{-200}$

---

## **Quick Start**

```bash
git clone https://github.com/clevix-lab/EOM-AI-Battery-Degradation.git
cd EOM-AI-Battery-Degradation
conda env create -f environment.yml
conda activate eom-ai
python scripts/EOM_AI_Extended.py --all

Data Sources
Dataset,Chemistry,Profiles,Temp,Link
NASA,NMC,Randomized,24°C,NASA PCoE
Oxford,NMC,Artemis,40°C,Zenodo
CALCE,LFP,DST/US06/FUDS,0/25/50°C,calce.umd.edu

Repository Structure
EOM-AI-Battery-Degradation/
├── data/           ← Raw (sample only)
├── scripts/        ← EOM_AI_*.py
├── results/        ← Tables & Figures
├── paper/          ← main.tex
└── .github/        ← CI/CD

Reproducibility
Python 3.9–3.11
environment.yml (conda)
GitHub Actions CI
Zenodo DOI: 10.5281/zenodo.XXXXXXX

Contact
H/&K Research Lab, Clevix LLC
Email: khanh@clevix.vn
