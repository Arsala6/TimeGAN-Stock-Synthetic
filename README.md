# TimeGAN Stock Synthetic Data Project

This repository contains implementation of a TimeGAN model for generating synthetic stock market data. The goal is to create realistic synthetic time-series data that resembles real stock prices, which can be useful for research, testing, or forecasting models.

## Project Overview

- Implemented a **TimeGAN model** to generate synthetic stock data for multiple companies.  
- Notebook written in **Python** using **TensorFlow, pandas, and NumPy**.  
- Generated synthetic data is saved in CSV files for further analysis.
  
## Files in the Repository

- **`TimeGan.ipynb`** – Main Colab notebook with data preprocessing, model training, and synthetic data generation.
- **`Dataset`** – all_stocks_5yr.csv.
- **`synthetic_timegan_data.csv`** – Sample synthetic stock data.  
- **`synthetic_timegan_data_named.csv`** – Synthetic data with company names included.  
- **`README.md`** – This file describing the project.
  
## Dataset

The project uses the `all_stocks_5yr.csv` dataset, which contains historical stock prices for multiple companies over 5 years.  
- **Source:** Kaggle ([link to dataset](https://www.kaggle.com/datasets/szrlee/stock-time-series-5yr))  
- **Columns:** `date`, `open`, `high`, `low`, `close`, `volume`, `Name`  
- **Usage:** This dataset is used for training the TimeGAN model to generate synthetic stock price sequences.

## How to Use

1. Open **`TimeGan.ipynb`** in Google Colab.
2. Make sure to select **GPU runtime** for faster training:  
   - Go to `Runtime` → `Change runtime type` → Select `T4 GPU` → Save.   
3. Mount your Google Drive to save outputs.  
4. Run all cells in order to:  
   - Load and preprocess stock data  
   - Train the TimeGAN model  
   - Generate synthetic stock data
   - make sure all the libraries is installed
5. Download the generated CSV files from Drive or use them directly in Colab for analysis.

## Evaluation Metrics

- **DTW Distance** – Measures similarity of temporal patterns between real and synthetic data.  
- **MMD Score** – Compares distribution similarity.  
- **Predictive Utility (MSE & R²)** – Tests how well synthetic data can predict real data trends.

## Notes

- Preprocessing and missing value handling are included in the notebook.  
- Synthetic data is scaled between 0–1 before training.  
- Clear notebook outputs before pushing to GitHub to reduce file size.
