# Figures

This folder contains simulation results, experimental measurements, and comparative visualizations for the circular patch antenna.

## Contents

| File | Description |
|---|---|
| `S11 Antena Individual simulacion.png` | S11 parameter from FEKO simulation — resonance at 5.72 GHz |
| `Antena Parche_s11_simulated_vs_measured.png` | S11 comparison generated in FEKO, overlaying simulation and VNA measurements. Shows resonance frequency, minimum S11, and bandwidth for both curves |
| `S11_simulation_vs_measured_matlab.png` | Same comparison regenerated in MATLAB from the raw data files |
| `Antena vista desde Feko.png` | 3D view of the antenna model as seen in FEKO |
| `CSV4.csv` | Raw S11 data measured with the Vector Network Analyzer (VNA) — imported into FEKO and MATLAB to generate the comparison plots |
| `antenadatos.s1p` | S11 simulation data exported from FEKO in Touchstone format — used as input for the MATLAB script |
| `Graficas_comparativa_antenas_simu_medicion.mlx` | MATLAB Live Script that loads `CSV4.csv` and `antenadatos.s1p` and generates the comparison plot |
