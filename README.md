# PFAS Quantum Chemistry Benchmark Database

This repository contains curated quantum chemistry datasets for benchmarking **bond dissociation energies (BDEs)** and related properties of per- and polyfluoroalkyl substances (PFAS). 
The data is organized by **gas-phase and water-phase**, and includes both **protonated (neutral)** and **deprotonated (anion)** species across a wide range of computational methods. 
Properties include:
- Dipole moments
- XYZ coordinates
- Vibrational frequencies
- Electron affinity (vertical and adiabatic)
- Ionization potential (vertical and adiabatic)
- Enthalpy corrections using the quasi-rigid-rotor-harmonic oscillator (quasi-RRHO) approximation
- Entropy energies (raw from ORCA/Gaussian output files)
- Bond dissociation enthalpies
Bond dissociation enethalpies can be found manually or with the helper script below. 

---

## Repository Structure

```bash
Data/
│   ├── Neutral_Speed.csv # gas phase protonated used in A Comprehensive Benchmark Database of Per-and Polyfluoroalkyl Substance Properties from Quantum Mechanical Methods
│   └── Anion_Speed.csv # gas phase deprotonated used in A Comprehensive Benchmark Database of Per-and Polyfluoroalkyl Substance Properties from Quantum Mechanical Methods
│   ├── Neutral_Water_Speed.csv
│   └── Anion_Water_Speed.csv
```
## Usage
These files are designed to work with the companion script:
(https://github.com/mmarciesky/PFAS_BDE_helper)
## Disclaimer
This is a research-grade database. While extensive cleaning and filtering have been applied (imaginary frequency checks, spin contamination flags, etc.), users should always validate specific entries for critical applications.
# Lab & Project Acknowledgments
This dataset and workflow were developed as part of a PhD project in the Ng Group at the University of Pittsburgh.
We acknowledge support from the National Institutes of Health (NIH) under grant number 5 R01 ES032717-04. This research was supported in part by the University of Pittsburgh Center for Research Computing and Data, RRID:SCR_022735, through the resources provided. Specifically, this work used the H2P cluster, which is supported by NSF award number OAC-2117681.
# Citations
If this database or associated script is useful to your research, please cite:
