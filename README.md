# PFAS Quantum Chemistry Database

This repository contains curated **quantum chemistry datasets for per- and polyfluoroalkyl substances (PFAS)**.  
Two complementary datasets are provided:

- **PFAS_BM** – a benchmarking dataset used to evaluate quantum mechanical methods.
- **Validated PFAS Database** – a larger dataset generated using the automated workflow described below.

The datasets include **bond dissociation energies (BDEs)** and related electronic and thermodynamic properties across multiple PFAS classes, protonation states, and phases.

All energies in this repository are reported in **Hartree** unless otherwise noted.

---

# Database Overview

## 1. Benchmark Database (PFAS_BM)

The benchmarking dataset contains **gas-phase neutral/neutral radical and anion/anion radical PFAS species** used in the study:

**"A Comprehensive Benchmark Database of Per- and Polyfluoroalkyl Substance Properties from Quantum Mechanical Methods."**

These structures were calculated across many quantum methods and used to evaluate accuracy for PFAS thermochemistry and electronic structure predictions.

Files:

Neutral_BM.csv

Anion_BM.csv

---

## 2. Validated PFAS Database

The validated dataset contains PFAS structures and fragments generated using the automated **fragmentation and conformer workflow** shown below.

This dataset expands the chemical space beyond the benchmarking set and includes **neutral, radical, and anionic species across gas and  water**
A much larger datbase with more PFAS families and solvents (DMSO and 1-OCTANOL) is coming Summer 2026.
These datapotins are generated using this pipeline:
<img width="2120" height="621" alt="image" src="https://github.com/user-attachments/assets/437ee5de-fc1e-43c2-ac7c-5098ba46d9fb" />

Files:

PFAS_QM

# Reported Properties

The database contains the following computed properties:

- Dipole moments (Debye)
- HOMO–LUMO energies
- Mulliken and Löwdin charges
- XYZ coordinates (Å)
- Vibrational frequencies
- Electron affinity (vertical and adiabatic) (Hartree)
- Ionization potential (vertical and adiabatic) (Hartree)
- Enthalpy corrections using the **quasi-rigid-rotor-harmonic oscillator (quasi-RRHO)** approximation
- Entropy (Hartree/K)
- Gibbs Free Energy (Hartree)

---

# Notes on Thermodynamic Quantities

## Electron Affinity and Ionization Potential

- In **Neutral_BM** and **Anion_BM**, adiabatic EA and IP were calculated using:
  - electronic energy
  - zero-point energy (ZPE)

- In **all other datasets**, adiabatic EA and IP are calculated using the **full Gibbs free energy**.

---

## Entropy and Gibbs Free Energy

- In **Neutral_BM and Anion_BM**, entropy and Gibbs free energy values are taken directly from **ORCA/Gaussian outputs**.

- In **all other datasets**, entropy and Gibbs free energy are calculated using vibrational frequencies and the **quasi-RRHO correction**.

---


---

# Usage

The **Neutral_BM** and **Anion_BM** files are designed to be used with the companion analysis script:

https://github.com/mmarciesky/PFAS_BDE_helper

This script provides utilities for:

- BDE analysis
- radical fragment matching
- PFAS property comparisons

---

# Disclaimer

This is a **research-grade database**.

Extensive cleaning and validation steps were applied, including:

- imaginary frequency checks
- spin contamination flags
- conformer filtering

However, users should **independently validate specific entries** for critical applications.

---

# Lab & Project Acknowledgments

This dataset and workflow were developed as part of a **PhD project in the Ng Group at the University of Pittsburgh**.

We acknowledge support from:

- **National Institutes of Health (NIH)**  
  Grant: **5 R01 ES032717-04**

- **University of Pittsburgh Center for Research Computing and Data**  
  RRID: **SCR_022735**

This work used the **H2P cluster**, supported by:

**NSF Award OAC-2117681**

---

# Citation

If this database or associated workflow is useful to your research, please cite:

