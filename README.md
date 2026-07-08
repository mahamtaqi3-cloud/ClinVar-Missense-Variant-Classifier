# 🧬 ClinVar Missense Variant Classifier

## 📌 Project Overview

This project leverages machine learning to predict the clinical significance of missense variants found in the ClinVar dataset. By transforming complex genomic metadata into predictive features, this model automates the classification of variants into **Benign**, **Uncertain**, or **Pathogenic** categories.

## 🚀 Key Achievements

* **Pipeline Development:** Built an end-to-end ML pipeline, from raw CSV cleaning to model inference.
* **Target Refinement:** Optimized model stability by re-grouping 5 clinical classes into 3 actionable categories.
* **Model Optimization:** Fine-tuned a Random Forest Classifier using `GridSearchCV` to maximize predictive accuracy.
* **Biological Enrichment:** Automated the mapping of cryptic NCBI `GeneID` numbers to official **Gene Symbols** (e.g., *BRCA1, PAH, GCK*) using the `mygene` API.

## 📊 Performance & Insights

### Feature Importance

The analysis reveals that `GeneID` is the most critical feature, confirming the biological consensus that the identity and functional constraint of a gene are primary determinants of missense variant pathogenicity.

### Top Clinically Significant Genes

Our model identified the following genes as the most frequent in the dataset, reflecting their high clinical relevance:

| Rank | Gene Symbol | Biological Context |
| --- | --- | --- |
| 1 | **PAH** | Phenylalanine hydroxylase |
| 2 | **GCK** | Glucokinase |
| 3 | **BRCA1** | Breast cancer gene (DNA repair) |
| 4 | **BRCA2** | Breast cancer gene (DNA repair) |
| 5 | **LDLR** | Low-density lipoprotein receptor |
| 6 | **HNF1A** | Hepatocyte nuclear factor 1-alpha |
| 7 | **TP53** | Tumor suppressor protein |
| 8 | **MLH1** | DNA mismatch repair protein |
| 9 | **GAA** | Acid alpha-glucosidase |
| 10 | **MECP2** | Methyl-CpG binding protein 2 |

## 🛠 Tech Stack

* **Language:** Python 3.12
* **Data Processing:** `pandas`, `mygene` (Genomic API)
* **Machine Learning:** `scikit-learn`
* **Visualization:** `matplotlib`, `seaborn`

## 💡 Discussion

The high predictive power of `GeneID` in our model suggests that variant pathogenicity is heavily dependent on the biological context of the affected gene. The prevalence of genes like *PAH* and *BRCA1* in our dataset underscores why the model relies so heavily on gene-level data to achieve high classification accuracy.

---

### How to reproduce this project

1. Clone this repository.
2. Ensure you have the necessary libraries installed: `pip install pandas scikit-learn matplotlib mygene`.
3. Run the `ClinVar_Missense_Variant_Classifier.ipynb` notebook.

---

