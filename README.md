# Precision Forecasting of Cloudbursts with CNNs and GAF for Real-Time Disaster Response

> **Published:** Layek, S., Bhushan, M., Mall, S., Vyas, S., Singh, U., & Khaire, U. M. (2026). Precision forecasting of cloudbursts with CNNs and GAF for real-time disaster response. *Modeling Earth Systems and Environment*, 12, 184.
> DOI: [10.1007/s40808-026-02826-4](https://doi.org/10.1007/s40808-026-02826-4)

## Overview

This repository contains code and data for a cloudburst forecasting framework for the Himalayan region of Uttarakhand, India. The model integrates Convolutional Neural Networks (CNN) with Gramian Angular Field (GAF) encoding to convert multivariate meteorological time-series into 2D visual representations, enabling spatial feature extraction for accurate early warnings. Data is sourced from the Indian Meteorological Department (IMD).

**Results:**
- 6-hour lead prediction — AUC: **97.73%**
- 12-hour lead prediction — AUC: **98.41%**

## Repository Structure

| File | Description |
|------|-------------|
| `Training.ipynb` | Model training |
| `Testing.ipynb` | Model evaluation |
| `API.ipynb` | Continuous monitoring using pre-trained model |
| `CB6.npy` | Cloudburst training-testing data (6-hour prediction) |
| `CB12.npy` | Cloudburst training-testing data (12-hour prediction) |
| `NB.npy` | Non-cloudburst training-testing data |
| `TEST6.npy` | Cloudburst validation data (6-hour prediction) |
| `TEST12.npy` | Cloudburst validation data (12-hour prediction) |
| `Model6.h5` | Pre-trained 6-hour prediction model |
| `Model12.h5` | Pre-trained 12-hour prediction model |

## Model Configuration

| Parameter | 6H Model | 12H Model |
|-----------|----------|-----------|
| Optimizer | Adam | RMSprop |
| Kernel Size | 2×2 | 1×1 |
| Pooling Size | 3×3 | 3×3 |
| Learning Rate | 0.0005 | 0.0005 |
| Epochs | 50 | 50 |

## Authors

Shirshendu Layek · Megha Bhushan · Shrey Mall · **Satyam Vyas** · Ugarsain Singh · Utkarsh Mahadeo Khaire

## Citation

```bibtex
@article{layek2026precision,
  title={Precision forecasting of cloudbursts with CNNs and GAF for real-time disaster response},
  author={Layek, Shirshendu and Bhushan, Megha and Mall, Shrey and Vyas, Satyam and Singh, Ugarsain and Khaire, Utkarsh Mahadeo},
  journal={Modeling Earth Systems and Environment},
  volume={12},
  pages={184},
  year={2026},
  publisher={Springer Nature},
  doi={10.1007/s40808-026-02826-4}
}
```

> **Note:** Since the code shuffles data before splitting, results may vary for newly trained models. The 3rd event in the testing dataset (TEST6 and TEST12) is a repeated event from the training-testing dataset — please ignore it.
