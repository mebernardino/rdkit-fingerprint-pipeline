# rdkit-fingerprint-pipeline
# UChicago Summer STEM Lab Internship 2025: Feature Extraction Pipeline

Developed during the **UChicago Summer STEM Lab Internship (2025)**, this repository contains a Python-based data processing pipeline designed for high-dimensional feature engineering. The script parses structural text representations (SMILES strings), transforms them into fixed-length binary feature vectors using RDKit, and formats the output into vectorized NumPy arrays for downstream machine learning workflows and algorithmic analysis.

For public release, compound identities have been mapped to public alias labels (`Compound 1`, `Compound 2`, etc.) while preserving the underlying vector computation logic.

---

## **Key Features**

* **High-Dimensional Feature Extraction:** Converts sequence inputs into 1024-bit Morgan bit vectors (ECFP equivalent) using RDKit.
* **Vectorized Array Generation:** Formats extraction outputs directly into NumPy arrays for seamless integration with machine learning frameworks (e.g., PyTorch, scikit-learn).
* **Data Anonymization Support:** Implements an alias-mapping structure for public dataset sharing without exposing underlying target names.

---

## **Tech Stack**

* **Language:** Python 3.x
* **Data Processing & ML:** RDKit, NumPy, Pandas

---

## **Pipeline Overview**

1. **Input:** Extract string data from structured data frames by index.
2. **Transformation:** Generate Morgan fingerprint bit vectors at specified radius ($r$) and bit lengths.
3. **Output:** Append vectorized numerical representations (`np.array`) into a primary feature set array for computational modeling.

---

## **Repository Setup & Usage**

### **Prerequisites**
```bash
pip install rdkit numpy pandas
