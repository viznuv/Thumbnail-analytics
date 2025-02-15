# YouTube Thumbnail & Metadata Regression Analysis with SHAP

This repository contains a Google Colab notebook and associated data files to perform regression analysis on YouTube video engagement metrics using features extracted from video thumbnails and metadata. It also utilizes SHAP (SHapley Additive exPlanations) to determine feature importance across different dependent variables.

## Overview

The analysis includes:
- **Data Merging**: Combines YouTube video metadata (with metrics such as view count, like count, favorites, and comment count) with thumbnail analysis data (face detection, image metrics, OCR-based text extraction, and title features).
- **Feature Engineering**: Computes additional features such as:
  - Average face size ratio (from comma-separated face size ratios)
  - Title word count and sentiment (if not already provided)
- **Data Imputation**: Fills missing values with the column mean to ensure that all data points (e.g., 180 rows) are used.
- **Regression Analysis**: Performs Ordinary Least Squares (OLS) regression for each dependent variable using `statsmodels`.
- **SHAP Analysis**: Uses a scikit-learn LinearRegression model along with SHAP’s `LinearExplainer` to generate summary plots for feature importance.

## Repository Structure


## Prerequisites

- **Python 3.x**
- **Packages**:  
  - `pandas`
  - `numpy`
  - `statsmodels`
  - `shap`
  - `scikit-learn`
  - `matplotlib`
  - `openpyxl`
  - `textblob`
  - `pytesseract`
- **Tesseract OCR**:  
  - In Google Colab, install using:
    ```bash
    !apt-get install -y tesseract-ocr
    ```
- **TextBlob Corpora**:  
  - Download required corpora:
    ```bash
    !python -m textblob.download_corpora
    ```

## Getting Started

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/yourusername/your-repository.git
   cd your-repository
