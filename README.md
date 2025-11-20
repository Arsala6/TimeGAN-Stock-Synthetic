# TimeGAN Stock Synthetic Data Project

This repository contains implementation of a TimeGAN model for generating synthetic stock market data. The goal is to create realistic synthetic time-series data that resembles real stock prices, which can be useful for research, testing, or forecasting models.

## Project Overview

- Implemented a **TimeGAN model** to generate synthetic stock data for multiple companies.  
- Notebook written in **Python** using **TensorFlow, pandas, and NumPy**.  
- Generated synthetic data is saved in CSV files for further analysis.

## Files in the Repository

- **`TimeGan.ipynb`** – Main Colab notebook with data preprocessing, model training, and synthetic data generation.  
- **`synthetic_timegan_data.csv`** – Sample synthetic stock data.  
- **`synthetic_timegan_data_named.csv`** – Synthetic data with company names included.  
- **`README.md`** – This file describing the project.

## How to Use

1. Open **`TimeGan.ipynb`** in Google Colab.  
2. Mount your Google Drive to save outputs.  
3. Run all cells in order to:  
   - Load and preprocess stock data  
   - Train the TimeGAN model  
   - Generate synthetic stock data  
4. Download the generated CSV files from Drive or use them directly in Colab for analysis.

## Evaluation Metrics

- **DTW Distance** – Measures similarity of temporal patterns between real and synthetic data.  
- **MMD Score** – Compares distribution similarity.  
- **Predictive Utility (MSE & R²)** – Tests how well synthetic data can predict real data trends.

## Notes

- Preprocessing and missing value handling are included in the notebook.  
- Synthetic data is scaled between 0–1 before training.  
- Clear notebook outputs before pushing to GitHub to reduce file size.
