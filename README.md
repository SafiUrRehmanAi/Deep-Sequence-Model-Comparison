# Deep Sequence Model Comparison

## 1. Overview

This project compares deep learning architectures for multivariate financial time series forecasting. It evaluates unidirectional and bidirectional GRU/LSTM models, together with a CNN-LSTM hybrid model.

## 2. Objective

The objective is to study how different sequence modeling architectures perform when learning patterns from historical market data and related financial indicators.

## 3. Dataset

The source dataset is stored in `data/raw/gold.csv`. It contains dated market observations, including OHLCV data and additional indicators.

## 4. Workflow

The notebooks implement the project in stages:

1. Exploratory data analysis
2. Feature engineering
3. Data preprocessing and scaling
4. Sequence creation for recurrent models
5. Baseline model comparison
6. CNN-LSTM data preparation
7. CNN-LSTM training and evaluation

## 5. Models

- Uni-LSTM
- Bi-LSTM
- Uni-GRU
- Bi-GRU
- CNN-LSTM

The trained model files are available in the `models/` directory.

## 6. Evaluation Metrics

Models are evaluated using:

- R2 score
- Root Mean Squared Error (RMSE)
- Mean Absolute Error (MAE)
- Mean Squared Error (MSE)

## 7. Results

The recorded results show the CNN-LSTM model performing best among the saved evaluations, with an R2 score of approximately `0.8865`, RMSE of `1.5667`, MAE of `1.2699`, and MSE of `2.4546`. Among the recurrent baselines, Uni-GRU has the strongest recorded R2 score at approximately `0.5426`.

Detailed results are available in `results/model_result.csv` and `results/cnn_lstm_model_result.csv`.

## 8. Repository Structure

```text
data/          Raw and processed datasets
models/        Trained Keras model files
notebooks/     EDA, preprocessing, modeling, and evaluation notebooks
results/       Model metrics and training histories
```

## 9. Getting Started

Create a Python environment, install the required packages, and run the notebooks in numerical order. Start with `01_eda.ipynb` and finish with `07_cnn_lstm_hybrid.ipynb`. Ensure the notebook kernel uses the same environment where the project dependencies are installed.

Example installation command:

```bash
python -m pip install -r requirement.txt
```

If `lightgbm` is required by a notebook and is not installed, run:

```bash
python -m pip install lightgbm
```

## 10. Notes

The supplied models and result files are included for reproducibility and comparison. Results can vary depending on the Python environment, library versions, random seeds, preprocessing choices, and hardware.

## Disclaimer

This project was created purely for educational and research purposes. It is not financial advice, and its outputs should not be used as the sole basis for investment or trading decisions.