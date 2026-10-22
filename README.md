# CDU-blends

## Written by Chat

# Two-Stage Residual Learning for Modelling Strength-Informed Optimisation of Thermal Systems

## Overview

This repository contains the code and supporting data for the study **“Two-Stage Residual Learning for Modelling Strength-Informed Optimisation of Thermal Systems”** by Talha Ansar, Waqar Muhammad Ashraf, Abdulelah S. Alshehri, and Omar Bayomie.

The study presents a two-stage residual learning (TSRL) framework for improving machine learning surrogate models and assessing their reliability when used in thermal-system optimisation. Conventional performance metrics, such as root mean square error (RMSE), provide an overall measure of prediction accuracy but may not reveal local modelling inaccuracies in the operating regions selected by an optimiser.

The proposed framework combines artificial neural networks (ANNs), residual learning, validation-based reliability screening, and domain-constrained optimisation to assess the modelling strength of computed solutions.

## Methodology

The TSRL framework consists of two stages:

1. **Base model:** An artificial neural network predicts the process output from the input operating conditions.
2. **Residual model:** A second neural network learns the signed residuals between the observed and predicted outputs of the base model. Its predictions are used to correct the base model's output.

The framework also includes a validation-based procedure for establishing a residual-score threshold. During optimisation, the modelling strength of each computed solution is assessed against this threshold, allowing solutions to be classified into one of two regions:

- **Good Modelled Region (GMR):** Solutions whose residual scores satisfy the established reliability criterion.
- **Weak Modelled Region (WMR):** Solutions whose residual scores do not satisfy the established reliability criterion.

This approach supports optimisation decisions that account for local surrogate-model reliability rather than relying exclusively on overall prediction accuracy.

## Case Studies

The framework is evaluated using two thermal-system datasets.

### 1. Crude Distillation Unit (CDU)

The refinery case study uses 817 simulation observations from a crude distillation unit. The analysis examines surrogate modelling performance for refinery process outputs, including Fuel Oil.

For Fuel Oil, the test RMSE decreases from **10.3 g/s to 4.7 g/s** using the TSRL framework.

### 2. Industrial Gas Turbine

The second case study uses operating records from a 395 MW industrial gas turbine. The target output is turbine heat rate (THR), expressed in kJ/kWh.

For turbine heat rate, the test RMSE decreases from **151 kJ/kWh to 105 kJ/kWh** using the TSRL framework.

## Key Features

- Two-stage artificial neural network modelling with residual learning.
- Improved predictive accuracy for thermal-system process outputs.
- Validation-based residual-score threshold selection.
- Domain-constrained optimisation using ANN surrogate models.
- Post-optimisation assessment of local modelling strength.
- Classification of computed solutions into Good Modelled Regions (GMRs) and Weak Modelled Regions (WMRs).
- Evaluation using refinery simulation data and industrial gas turbine operating records.

## Repository Contents

This repository provides the code and data associated with the CDU-blends study. The specific scripts, datasets, trained models, and supporting files should be documented here according to the contents of the repository.

## Data Availability

The data supporting the findings of this study are openly available in this repository:

https://github.com/omarbay/CDU-blends

## Authors

- **Talha Ansar** — Department of Mechanical Engineering, University of Engineering and Technology Lahore, Pakistan.
- **Waqar Muhammad Ashraf** — The Sargent Centre for Process Systems Engineering, Department of Chemical Engineering, University College London, UK.
- **Abdulelah S. Alshehri** — Department of Chemical Engineering, College of Engineering, King Saud University, Saudi Arabia.
- **Omar Bayomie** — Advanced Centre for Biochemical Engineering, University College London, UK; SSPC, University College Dublin, Ireland; and Institut des Systèmes Intelligents et de Robotique, Sorbonne University, France.

**Corresponding author:** Omar Bayomie — omar.bayomie.23@ucl.ac.uk

## Citation

If you use this repository in your research, please cite the associated publication:

Ansar, T., Ashraf, W. M., Alshehri, A. S., & Bayomie, O. *Two-Stage Residual Learning for Modelling Strength-Informed Optimisation of Thermal Systems*. International Journal of Energy Research.

Add the publication year, volume, issue, page numbers, and DOI once these details are available.

## License

Please refer to the license specified in this repository for terms governing the use, modification, and redistribution of its contents.
