# PFAS Quantum Chemistry Benchmark Database

This repository contains curated quantum chemistry datasets for benchmarking **bond dissociation energies (BDEs)** and related properties of per- and polyfluoroalkyl substances (PFAS). 
The data is organized by **gas-phase and water-phase**, and includes both **protonated (neutral)** and **deprotonated (anion)** species across a wide range of computational methods.
Please note that all properties are reported in Hartree.
Properties include:
- Dipole moments (Debye)
- Homo-Lumo
- Mulliken and Löwdin Charges
- XYZ coordinates (Angstroms)
- Vibrational frequencies
- *Electron affinity (vertical and adiabatic) (Hartree)
- *Ionization potential (vertical and adiabatic) (Hartree)
- Enthalpy corrections using the quasi-rigid-rotor-harmonic oscillator (quasi-RRHO) approximation
- **Entropy (Hartree/K)
- **Gibbs Free Energy (Hartree)
  
\* Please note that EA and IP adiabatic are calculated via electronic energry and ZPE in Neutral_BM and Anion_BM. All other releases they are calcualted from the full Gibbs Free Energy.

\* \* The Entropy and Gibbs Free Energy in Neutral_BM and Anion_BM are taken from ORCA/Gaussian outputs. All other releases they are calcualted using the vibrqational frequencies quasi-Rigid Rotor Harmonic Oscillator.

---

## Repository Structure

```bash
Data/
│   ├── Neutral_BM.csv # gas phase protonated used in A Comprehensive Benchmark Database of Per-and Polyfluoroalkyl Substance Properties from Quantum Mechanical Methods (benchmarking methods)
│   └── Anion_BM.csv # gas phase deprotonated used in A Comprehensive Benchmark Database of Per-and Polyfluoroalkyl Substance Properties from Quantum Mechanical Methods (benchmarking methods)
│   ├── Neutral_Water.csv # water phase neutral/neutral radical species used in 
│   └── Anion_Water.csv # water phase anion/anion radical species used in
|   └── Neutral_Gas.csv # gas phase neutral/neutral radical species used in 
```
## Usage
These Neutral_BM and Anion_BM files are designed to work with the companion script:
(https://github.com/mmarciesky/PFAS_BDE_helper)
## Disclaimer
This is a research-grade database. While extensive cleaning and filtering have been applied (imaginary frequency checks, spin contamination flags, etc.), users should always validate specific entries for critical applications.
# Lab & Project Acknowledgments
This dataset and workflow were developed as part of a PhD project in the Ng Group at the University of Pittsburgh.
We acknowledge support from the National Institutes of Health (NIH) under grant number 5 R01 ES032717-04. This research was supported in part by the University of Pittsburgh Center for Research Computing and Data, RRID:SCR_022735, through the resources provided. Specifically, this work used the H2P cluster, which is supported by NSF award number OAC-2117681.
# Citations
If this database or associated script is useful to your research, please cite:
