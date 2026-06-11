# Landslide Event Detection using Temporal Transformers and Rotary Positional Embeddings

## Overview

This project explores the use of Transformer-based deep learning models for detecting landslide-related events from multi-temporal satellite imagery. The goal is to automatically identify temporal patterns in geospatial observations and improve event detection accuracy using advanced positional encoding techniques.

The work was developed as part of my research in deep learning for Earth observation and remote sensing applications.


##Problem Statement

Monitoring landslides over large geographic regions is challenging and often requires extensive manual analysis of satellite data. Traditional machine learning approaches struggle to capture long-term temporal dependencies present in satellite time-series observations.

This project investigates whether Transformer architectures can effectively model temporal information and improve landslide event detection performance.



## Dataset

The project uses multi-temporal Sentinel-2 satellite observations stored in NetCDF format.

The dataset contains:

* Multi-spectral Sentinel-2 bands
* Temporal observations across multiple timestamps
* Landslide and non-landslide labels
* Geospatial information for each sample

Data preprocessing includes:

* Band extraction
* Temporal sequence construction
* Feature normalization
* Train-validation splitting
* Data quality checks



## Approach

### Feature Engineering

Several preprocessing techniques were applied to improve the quality of temporal representations:

* Spectral band selection
* Edge-based feature extraction
* Temporal sequence generation
* Data normalization

### Transformer-Based Architecture

The model leverages temporal attention mechanisms to learn relationships across multiple satellite observations.

Key components include:

* Transformer Encoder
* Multi-Head Self-Attention
* Temporal Feature Fusion
* Sequence Classification Head

### Positional Encoding Experiments

A major focus of this project was evaluating different positional encoding strategies:

* No Positional Encoding
* Learned Positional Embeddings
* Sinusoidal Positional Encoding
* Rotary Positional Embeddings (RoPE)

The experiments demonstrate that incorporating positional information significantly improves temporal understanding.

---

## Results

| Positional Encoding Method          | F1 Score |
| ----------------------------------- | -------- |
| None                                | 0.71     |
| Learned Embeddings                  | 0.75     |
| Sinusoidal Encoding                 | 0.83     |
| Rotary Positional Embeddings (RoPE) | 0.91     |

### Key Findings

* Positional information is critical for temporal satellite analysis.
* Rotary Positional Embeddings achieved the best overall performance.
* RoPE improved model generalization and temporal pattern recognition.
* Transformer architectures effectively capture long-range dependencies in geospatial time-series data.



## Technologies Used

### Machine Learning

* PyTorch
* Scikit-Learn
* NumPy
* Pandas

### Data Processing

* Xarray
* NetCDF
* SciPy

### Visualization

* Matplotlib

### Deep Learning Concepts

* Transformers
* Self-Attention
* Temporal Modeling
* Rotary Positional Embeddings (RoPE)
* Sequence Classification

-

## Project Structure

```text
├── notebooks/
│   ├── experiment-3m-rope-positonal-ebedding.ipynb
│   └── project-notebook.ipynb
│
├── data/
│   └── Sentinel-2 time-series data
│
├── models/
│   └── Saved checkpoints
│
└── README.md


## Future Improvements

* Temporal Fusion Transformer (TFT) integration
* Vision Transformer (ViT) based feature extraction
* Multi-class hazard classification
* Larger-scale geospatial datasets
* Real-time landslide monitoring pipeline




yush Kumar

B.Tech, VNIT Nagpur

Interested in Deep Learning, Transformers, Remote Sensing, and Machine Learning Research.

GitHub: https://github.com/AyushKumar5944
LinkedIn: https://linkedin.com/in/ayush-kumar-a4259831b
