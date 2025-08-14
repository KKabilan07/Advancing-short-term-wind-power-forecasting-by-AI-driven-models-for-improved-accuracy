# Advancing Short-Term Wind Power Forecasting by AI-Driven Models

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Python](https://img.shields.io/badge/Python-3.8%2B-blue.svg)](https://www.python.org/)
[![Jupyter Notebook](https://img.shields.io/badge/Jupyter-Notebook-orange.svg)](https://jupyter.org/)
[![DOI](https://img.shields.io/badge/DOI-10.1007%2Fs00202--025--03295--1-green.svg)](https://doi.org/10.1007/s00202-025-03295-1)

This repository contains the implementation of the research paper titled **"Advancing Short-Term Wind Power Forecasting by AI-Driven Models for Improved Accuracy"**, published in *Electrical Engineering* (Springer). The study introduces an AI-driven framework for short-term wind power forecasting using SCADA data, combining robust preprocessing, anomaly detection, and a comparative analysis of machine learning (ML) and deep learning (DL) models.

## 📄 Paper Abstract

Accurate short-term wind power forecasting is critical for integrating renewable energy into modern power systems. This study presents an advanced AI-driven framework that compares ML and DL models, including XGBoost, LightGBM, Random Forest, Transformer variations, and Temporal Fusion Transformer, using processed SCADA data (wind speed, direction, theoretical power, and actual power output at 10-minute intervals). The framework addresses limitations in existing approaches, such as inadequate preprocessing, lack of anomaly detection, and absence of physics-informed constraints. Anomaly detection is performed using physics-informed neural networks (PINN) and long short-term memory (LSTM) networks, ensuring physical plausibility under Betz’ law. Preprocessing includes Gaussian noise augmentation, normalization, and principal component analysis (PCA), retaining over 90% of variance. XGBoost achieved the highest accuracy with an R² score of 0.9890, MSE of 0.0015, RMSE of 0.0385, and MAE of 0.0151. This data-driven, preprocessing-enhanced methodology significantly improves prediction reliability, supporting intelligent and sustainable energy systems.

**Keywords:** Machine Learning, Deep Learning, Wind Power Forecasting, Temporal Fusion Transformer, Variational Mode Decomposition, Anomaly Detection

## 📊 Dataset

The dataset is sourced from the [Wind Turbine SCADA Dataset](https://www.kaggle.com/datasets/berkerisen/wind-turbine-scada-dataset) on Kaggle, collected at 10-minute intervals. Features include:
- **Date/Time**: Timestamp for temporal analysis
- **Wind Speed (m/s)**: Measured at turbine hub height
- **Theoretical Power Curve (kWh)**: Manufacturer’s expected output
- **Wind Direction (°)**: Affects turbine yaw control
- **Target: LV Active Power (kW)**: Actual power output

The dataset has no missing values, but preprocessing addresses noise and non-stationarity.


## 📈 Results

| Model                        | R²    | MSE   | RMSE  | MAE   |
|------------------------------|-------|-------|-------|-------|
| XGBoost                     | 0.9890| 0.0015| 0.0385| 0.0151|
| LightGBM                    | 0.9799| 0.0026| 0.0514| 0.0233|
| Temporal Fusion Transformer | 0.9649| 0.0349| 0.1868| 0.1109|
| Random Forest               | 0.9651| 0.0045| 0.0674| 0.0281|
| Informer                    | 0.9483| 0.0067| 0.0821| 0.0519|
| Vanilla Transformer         | 0.9484| 0.0078| 0.0881| 0.0640|
| Autoformer                  | 0.9231| 0.0666| 0.2760| 0.1657|


## 📚 Citation

Please cite our paper if you use this code:
```
@article{kishore2025advancing,
  title={Advancing short-term wind power forecasting by AI-driven models for improved accuracy},
  author={Kishore, B. and Kabilan, K. and Rahul, L. S. and Priyadarshan, G. Prajwal and Vishnutheerth, E. P. and Satheesh, Rahul and Kolhe, Mohan Lal},
  journal={Electrical Engineering},
  year={2025},
  publisher={Springer},
  doi={10.1007/s00202-025-03295-1}
}
```

## 🤝 Contributing

Contributions are welcome! Please:
1. Fork the repository.
2. Create a feature branch (`git checkout -b feature/YourFeature`).
3. Commit changes (`git commit -m 'Add YourFeature'`).
4. Push to the branch (`git push origin feature/YourFeature`).
5. Open a pull request.

For major changes, open an issue to discuss first.

