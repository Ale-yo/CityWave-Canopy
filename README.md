# Dynamic Analysis of the CityWave Canopy

Modal identification and numerical validation of the **CityWave Canopy** structure in the CityLife district in Milan, developed for the *Advanced Dynamics of Mechanical Systems* course at Politecnico di Milano (A.Y. 2025/2026).

## Project Overview

The study compares Experimental Modal Analysis (EMA) results against a numerical Finite Element Model (FEM), using data from a wind-tunnel scaled model excited via a modal shaker (swept sine) and measured across **202 points** using a laser Doppler vibrometer.

The analysis focuses on the **2–8 Hz** frequency range and covers:
- **Eigenfrequency Identification**: Averaging FRF magnitudes across all 202 sensors to extract resonance peaks and scaling wind-tunnel frequencies to full scale for comparison with FEM.
- **Damping Estimation**: Peak-picking method applied to anti-nodal sensors exceeding an 80% peak-amplitude threshold for each mode.
- **Mode Shape Extraction & Interpolation**: Computing operational/experimental mode shapes from FRF imaginary parts and interpolating sensor data onto the numerical FEM mesh.
- **FEM–EMA Correlation**: Visual mode-shape comparisons alongside MAC and CoMAC statistical indices to evaluate global and degree-of-freedom correlation.

## Repository Structure

- `scripts/` — MATLAB scripts and `.mat` datasets (`main.m`, `find_sensors.m`, `connectivity.mat`, `FRF_H1.mat`, `punti_laser.mat`, `modal_output.mat`, `peak_picking.m`).
- `report/` — Project report (`Canopy.pdf`).
- `LICENSE` — Project licens.

## Usage

1. Clone the repository.
2. Open MATLAB and add the `scripts/` folder (and datasets) to the path.
3. Run `main.m` (or the relevant analysis scripts) to process the FRFs, identify modal parameters, and generate FEM–EMA comparisons and MAC/CoMAC plots.
4. Refer to `report/Canopy.pdf` for full methodology, equations, and discussion.
