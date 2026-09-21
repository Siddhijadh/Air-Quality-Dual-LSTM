# Air Quality Prediction Based on Integrated Dual LSTM Model

## Project Overview

This project implements an air quality prediction system based on the Integrated Dual LSTM approach described in the reference research paper.

The implementation uses the Beijing Multi-Site Air-Quality dataset and predicts PM2.5 concentration.

## Methodology

1. Data preprocessing
2. Missing-value handling
3. Feature preparation
4. Data normalization
5. 48-hour historical input sequence
6. Single-Factor LSTM
7. Attention Multi-Factor LSTM
8. XGBoost integration
9. PM2.5 prediction
10. Model evaluation

## Models

### Single-Factor LSTM

Uses historical PM2.5 information to learn temporal patterns.

### Attention Multi-Factor LSTM

Uses multiple air-quality and meteorological factors with an attention mechanism.

### XGBoost Integration

Combines the LSTM model outputs to produce the final PM2.5 prediction.

## Evaluation Metrics

- RMSE
- MAE
- MAPE
- R2
- Index of Agreement (IA)

## Experimental Results

The experiment generated 1,393 PM2.5 test predictions.

| Model | RMSE | MAE | MAPE (%) | R2 | IA |
|---|---:|---:|---:|---:|---:|
| Single-Factor LSTM | 17.941 | 10.370 | 34.560 | 0.9551 | 0.9882 |
| Attention Multi-Factor LSTM | 16.141 | 9.894 | 28.745 | 0.9636 | 0.9908 |
| Integrated Dual LSTM + XGBoost | 26.782 | 13.044 | 45.296 | 0.9392 | 0.9833 |

## Results

The prediction results generally follow the variation of the actual PM2.5 values. Larger errors occur during some extreme PM2.5 concentration events.

## Project Structure

Air_Quality_Dual_LSTM/

    models/
        Single_Factor_LSTM.keras
        Multi_Factor_Attention_LSTM.keras
        XGBoost_Integrator.json

    results/
        PM25_Final_Predictions.csv
        Model_Comparison_Metrics.csv

    graphs/
        Actual_vs_Predicted_PM25.png
        PM25_Error_Distribution.png
        Single_Factor_LSTM_Loss.png
        Attention_Multi_Factor_LSTM_Loss.png
        RMSE_Model_Comparison.png

## Reference Paper

Chen, H., Guan, M., and Li, H. (2021).
Air Quality Prediction Based on Integrated Dual LSTM Model.
IEEE Access.

## Note

This project is an implementation of the research approach using a publicly available Beijing multi-site air-quality dataset. The experimental results are independently generated and should not be considered a reproduction of the numerical results reported in the original paper.
