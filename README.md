# Smart Manufacturing: Predictive Defect Detection on Bosch Production Lines

> Prediction of manufacturing defects in Bosch production lines using machine learning to reduce quality defects and production costs.

## Project overview

**Problem:**
Manufacturing errors cause high costs due to rejects, rework and customer complaints. The aim is to identify faulty components at an early stage before they reach quality control.

**Database:**  
Anonymised measurement data from Bosch production lines with thousands of features, organised by:
- `L{Line}` – Production line
- `S{Station}` – Measuring station
- `F{Feature}` – Measured value

**Challenges:**
- **Extreme class imbalance:** Only ~0.1% of components are faulty
- **Large amount of data:** Several GB of numerical, categorical and timestamp data
- **Feature engineering:** Thousands of anonymised features require intelligent aggregation

**Goal:**  
Development of a binary classification model for predicting faulty components (`Response = 1`), optimised for the **Matthews Correlation Coefficient (MCC)**.

---

## Project structure

```
├── data/
│   ├── raw/              # Original data from Kaggle
│   └── processed/        # Prepared features
├── notebooks/
│   └── 01_exploration.ipynb      # Data exploration
└── src/
    └── core/             # Helper functions (Data Loading etc.)
```

---

## Setup

### Prerequisites
- Python 3.11+
- [uv](https://docs.astral.sh/uv/) Package manager
- Kaggle API Credentials (for data access)

### Installation

```bash
# Clone repository
git clone https://github.com/YunusAhmetSari/Smart-Manufacturing-Predictive-Defect-Detection-on-Bosch-Production-Lines.git
cd Smart-Manufacturing-Predictive-Defect-Detection-on-Bosch-Production-Lines

# Install dependencies
uv sync
```

### Kaggle API setup
1. Kaggle account create at [kaggle.com](https://www.kaggle.com)
2. API Token generate: Account → Settings → API → Create New Token
3. `kaggle.json` in `~/.kaggle/` (Linux/Mac) or `%USERPROFILE%\.kaggle\` (Windows) save

---

## Execution

Notebooks in this order:

1. **`01_exploration.ipynb`** – Data loading and exploration

---

## Evaluation metric

**Matthews Correlation Coefficient (MCC):**

$$MCC = \frac{TP \cdot TN - FP \cdot FN}{\sqrt{(TP+FP)(TP+FN)(TN+FP)(TN+FN)}}$$

The MCC was chosen, as it is more robust than accuracy or F1-Score for imbalanced datasets.

---

## Data source

[Kaggle: Bosch Production Line Performance](https://www.kaggle.com/competitions/bosch-production-line-performance)

---

## About this Project

- **Context:** Data-Science Project
- **Duration:** 01.02.2026 - 
- **Author:** Yunus Ahmet Sari

## Kontakt

**[GitHub](https://github.com/YunusAhmetSari)** | **[LinkedIn](https://www.linkedin.com/in/yunussari/)** | **[E-Mail](mailto:yunusahmet61@gmail.com)**
