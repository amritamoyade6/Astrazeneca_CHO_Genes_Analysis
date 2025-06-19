# Gene Marker Identification and Constitutive Gene Analysis in CHO Cells
*AstraZeneca Project*

## 📌 Project Summary

This project was conducted in collaboration with AstraZeneca to analyze RNA-seq data from CHO (Chinese Hamster Ovary) cell lines. The goal was two-fold:

1. **Gene Marker Identification** – Discover genes strongly correlated with light chain (PRODUCT-TG) for use in clone selection.
2. **Constitutive Gene Characterization** – Analyze gene expression stability and sequence patterns (5'UTR, CDS, 3'UTR) of non-variable genes.

## 🧪 Methodology

### Gene Marker Identification
- **Data Preprocessing**: Batch effect correction using ComBat, normalization
- **Feature Selection**:
  - Spearman correlation with PRODUCT-TG
  - Random Forest Regressor and Classifier importance
  - Composite scoring of genes using combined metrics
- **Visualization**: Expression heatmaps, t-SNE, PCA

### Constitutive Gene Analysis
- **Stability Ranking**: Based on expression variance and standard deviation
- **Sequence Embedding**: DNABERT for 5'UTR, CDS, and 3'UTR
- **Cluster Analysis**: PCA on embeddings to check gene spread

```markdown
## 📁 Project Structure**

├── data/                # Raw RNA-seq data
├── notebooks/           # Jupyter notebooks (exploration, modeling)
├── figures/             # Visualizations (embeddings, feature importances)
├── results/             # Final gene ranking tables
├── report/              # Final PDF report
└── README.md            # Project overview and instructions
```

## 📥 Download Intermediate Outputs

We’ve bundled all of the intermediate analysis files (FIMO outputs, MEME summaries, DNABERT embeddings, etc.) into the **v1.0** release. To fetch and unpack them, run:

```bash
wget https://github.com/amritamoyade6/Projects/releases/download/v1.0/processed_outputs.zip
unzip processed_outputs.zip -d Astrazeneca_CHO_Analysis/data/processed/
```

## 📊 Key Tools & Technologies
- Python (Pandas, Scikit-learn, Seaborn, Matplotlib)
- DNABERT embeddings (HuggingFace)
- MEME/FIMO
- PCA, t-SNE, ComBat
- Git

## 🚀 **How to Run**
1. **Clone the repository**

  ```bash
  git clone https://github.com/amritamoyade6/astrazeneca_CHO_analysis.git
  ```

2. Dependencies

  - Python packages: see [`requirements.txt`](requirements.txt)  
  - MEME Suite (meme, fimo): see [`INSTALL.md`](INSTALL.md)

3. Launch notebooks  
jupyter notebook notebooks/

## 👩‍💻 Authors
- Amrita Moyade
