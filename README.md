# SchizoApathy
# SchizApathy: Functional Connectivity Disruptions in Apathy-Linked Brain Circuits

This repository contains code and analysis for identifying functional connectivity (FC) alterations in schizophrenia, with a focus on apathy-related brain regions. Using resting-state fMRI data from the COBRE dataset and the Schaefer 100-ROI functional atlas, the project investigates differences between schizophrenia (SZ) patients and healthy controls (HC).

## 📂 Dataset

This project uses the [COBRE preprocessed dataset](https://figshare.com/articles/dataset/COBRE_preprocessed_with_NIAK_0_17_-_lightweight_release/4197885), containing resting-state fMRI scans from 72 SZ patients and 74 HCs.

- **Source**: Figshare
- **Preprocessing**: NIAK v0.17
- **Access**: Download and extract into a directory like `~/Downloads/4197885/` and update the `base_dir` variable in the notebook if needed.

## 🧠 Project Workflow

1. **Load Data**: Preprocessed NIfTI fMRI files + confounds
2. **Atlas Registration**: Schaefer 100-region atlas is resampled to individual brains
3. **Time Series Extraction**: Regional mean signals are extracted
4. **Functional Connectivity**: Correlation matrices are computed
5. **Group Comparison**: SZ vs HC differences calculated (t-tests)
6. **Apathy Analysis**: Focused inspection of frontal, cingulate, insula, OFC, etc.
7. **Visualization**: Heatmaps and connectomes saved

## 📁 Structure

```
schizapathy-connectivity/
├── README.md
├── requirements.txt
├── notebooks/
│   └── SchizApathy_Final.ipynb
├── report/
│   └── Apathy_FC_Report.md
├── results/
│   ├── fc_schizophrenia.png
│   ├── fc_control.png
│   ├── fc_difference.png
│   ├── fc_significant_diff.png
│   ├── apathy_connectome.png
│   ├── network_barplot.png
│   ├── t_stat_matrix.csv
│   ├── p_val_matrix.csv
│   └── apathy_top_differences.csv
```

## 📊 Key Findings

- Decreased connectivity within somatomotor, control, and limbic regions in SZ
- Increased cross-network interactions (e.g., somatomotor ↔ control)
- Top apathy-related alterations involved PFC, insula, and cingulate circuits

## 🚀 How to Run

Clone the repo and install dependencies:

```bash
git clone https://github.com/Ishsirjan/schizapathy-connectivity.git
cd schizapathy-connectivity
pip install -r requirements.txt
jupyter notebook notebooks/SchizApathy_Final.ipynb
```



## 📬 Contact

Reach out to Ishsirjan via GitHub or ishsirjanchandok.iskc@gmail.com for questions or collaborations.
