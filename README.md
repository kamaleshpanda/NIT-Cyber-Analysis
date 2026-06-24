# NIT Cyber Analysis — Network Intrusion Detection using CIC-IDS2017

Research project on network intrusion detection using the CIC-IDS2017 dataset.
Covers data preprocessing, exploratory analysis, and deep learning classification across 15 traffic categories (14 attack types + benign).

---

## Dataset

CIC-IDS2017 — Canadian Institute for Cybersecurity

* 8 CSV files
* ~2.8 million network flow records
* 78 features + label

Dataset Download: https://www.unb.ca/cic/datasets/ids-2017.html

> CSV files are not tracked in this repository due to their large size.

---

## Project Structure

```text
.
├── notebooks
│   ├── 01_pre-processing.ipynb
│   ├── 02_EDA.ipynb
│   └── 03_modelling.ipynb
├── requirements.txt
└── README.md
```

| File                    | Description                                     |
| ----------------------- | ----------------------------------------------- |
| 01_pre-processing.ipynb | Data cleaning and preprocessing pipeline        |
| 02_EDA.ipynb            | Exploratory Data Analysis                       |
| 03_modelling.ipynb      | Encoding, scaling, SMOTE, and model preparation |
| requirements.txt        | Project dependencies                            |

---

## Work Division

### Undergraduate Contribution (This Repository)

* Loaded and merged all 8 CIC-IDS2017 CSV files into a single dataframe (~2.8M rows)
* Handled missing values, infinite values, and duplicate records
* Cleaned column names and label inconsistencies present in the raw dataset
* Performed exploratory data analysis including:

  * Label distribution analysis
  * Binary vs multi-class distribution
  * Correlation heatmaps
  * Outlier detection using boxplots
  * Feature distribution analysis
* Prepared data for modelling through:

  * Label Encoding
  * Feature selection
  * Stratified train-test split (80:20)
  * StandardScaler normalization
  * SMOTE class balancing

### PhD Scholar Contribution

* Deep learning model architecture design
* Model training and experimentation
* Hyperparameter tuning
* Performance evaluation and benchmarking
* Result analysis

---

## Pipeline

```text
Raw CSV Files
      ↓
    Merge
      ↓
    Clean
      ↓
     EDA
      ↓
   Encode
      ↓
    Split
      ↓
    Scale
      ↓
    SMOTE
      ↓
 Deep Learning Model
```

---

## Setup

```bash
pip install -r requirements.txt
jupyter notebook
```

Run the notebooks in the following order:

```text
notebooks/01_pre-processing.ipynb
                ↓
notebooks/02_EDA.ipynb
                ↓
notebooks/03_modelling.ipynb
```

---

## Team

**NIT Research Collaboration**
B.Tech CSE Student + PhD Scholar

Dataset Credit: Canadian Institute for Cybersecurity (CIC), University of New Brunswick
