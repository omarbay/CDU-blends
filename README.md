# CDU-blends

Data repository for the paper:

**"TWO-STAGE RESIDUAL LEARNING FOR MODELLING STRENGTH-INFORMED OPTIMISATION OF THERMAL SYSTEMS"**  
(*to be published in* Energy Conversion and Management)

## Abstract

Aggregate performance metrics do not identify local modelling inaccuracies in machine learning (ML) surrogates used for thermal-system optimisation. This study assesses local modelling strength through validation-based reliability screening and post-optimisation residual assessment. A two-stage residual learning (TSRL) framework, built on artificial neural networks (ANNs), is developed for modelling-strength-informed and domain-constrained optimisation of thermal systems. Within the TSRL framework, a base ANN predicts the process output, and a residual ANN learns the signed residuals left by the base ANN. The TSRL framework is implemented on two case studies of thermal systems, including 817 simulation observations of a crude distillation unit and operating records from a 395 MW industrial gas turbine. The TSRL framework reduces the test root mean square error (RMSE) from 10.3 g/s to 4.7 g/s for Fuel Oil in the refinery dataset and from 151 kJ/kWh to 105 kJ/kWh for turbine heat rate (THR). The base ANNs trained within TSRL are embedded in domain-constrained optimisation problems, and the modelling strength at each computed solution is assessed using the locked residual-score threshold. Each computed solution receives a good modelled region (GMR) or weak modelled region (WMR) label to inform ML model-based decision-making for safety-critical operation of thermal systems.