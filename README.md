# Coupled Climate-Epidemiological Model for Dengue and Malaria Outbreaks

This repository contains a coupled climate-epidemiological model designed to study how climate conditions (temperature, rainfall, and humidity) influence the outbreak dynamics of dengue and malaria. The model integrates climate-driven vector population dynamics with disease transmission equations to simulate realistic outbreak scenarios.

## Table of Contents
- [Overview](#overview)
- [Model Structure](#model-structure)
- [Dependencies](#dependencies)
- [How to Run the Model](#how-to-run-the-model)
- [Key Outputs](#key-outputs)
- [Analysis and Visualization](#analysis-and-visualization)
- [Contributing](#contributing)

## Overview
The model simulates the spread of dengue and malaria in a population, considering climate variables such as temperature, rainfall, and humidity. It explores:
1. How climate anomalies (e.g., temperature and rainfall changes) affect outbreak risk.
2. The interaction between dengue and malaria due to shared vector populations.
3. The impact of adaptive interventions based on outbreak severity.

## Model Structure
### Climate Parameters
- **Temperature**: Simulated with seasonal oscillations and a baseline of 25°C.
- **Rainfall**: Simulated with seasonal oscillations and a baseline of 50 mm.
- **Humidity**: Simulated with seasonal oscillations and a baseline of 70%.

### Disease Parameters
- **Dengue Transmission**: Base transmission rate (`beta_d`), vector population (`V_d`), and climate sensitivity.
- **Malaria Transmission**: Base transmission rate (`beta_m`), vector population (`V_m`), and climate sensitivity.
- **Coupled Transmission**: Cross-enhancement factors (`theta` for dengue, `delta` for malaria) account for interactions between the diseases.

### Adaptive Interventions
- Intervention strength scales with outbreak severity (cases/day) up to a maximum reduction of 60% in transmission.

## Dependencies
- Python 3.x
- NumPy
- SciPy
- Matplotlib

## How to Run the Model
1. **Install Dependencies**:
   ```bash
   pip install numpy scipy matplotlib
   ```

2. **Run the Model**:
   ```bash
   python epi_model.py
   ```

3. **Output**:
   - The model generates plots and visualizations showing:
     - Temperature/rainfall anomalies vs. outbreak risk.
     - Realistic coupled outbreak dynamics over time.
     - Phase-plane plots of mosquito density vs. infected human population.
     - Heatmaps and contour plots showing climate-driven changes in outbreak metrics (e.g., R0, duration).

## Key Outputs
### 1. Temperature/Rainfall vs. Outbreak Risk
- Plots showing how temperature and rainfall anomalies affect outbreak severity.

### 2. Realistic Coupled Outbreak Dynamics
- Time-series plots of dengue and malaria cases, including climate bands indicating high-risk periods.

### 3. R0 vs. Temperature and Rainfall
- Heatmap showing how the basic reproduction number (R0) for dengue varies with temperature and rainfall.

### 4. Outbreak Duration vs. Humidity and Temperature
- Contour plot showing how outbreak duration depends on humidity and temperature.

### 5. Partial Rank Correlation Coefficients (PRCC)
- Analysis of the sensitivity of total infections to climate parameters (temperature, rainfall, humidity).

## Analysis and Visualization
The model includes several visualization tools to interpret results:
- **Line Plots**: Show relationships between climate variables and outbreak risk.
- **Time-Series Plots**: Display outbreak dynamics and climate variables over time.
- **Heatmaps and Contour Plots**: Visualize how climate conditions influence outbreak metrics.
- **PRCC Analysis**: Quantifies the relative importance of climate parameters on outbreak severity.

## Contributing
Contributions to improve the model are welcome! Please submit issues or pull requests if you have suggestions for:
- Adding new climate parameters (e.g., wind speed, vegetation index).
- Improving the disease transmission model (e.g., incorporating age structure or immunity).
- Extending the model to include other diseases or vector species.

## License
This project is licensed under the Apache 2.0 License. See the LICENSE file for details.
