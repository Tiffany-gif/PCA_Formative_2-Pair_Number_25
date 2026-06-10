# Principal Component Analysis (PCA) on African Pangolin Seizure Data

This repository contains an individual implementation of Principal Component Analysis (PCA) applied to a wildlife dataset concerning African pangolin seizures. The project demonstrates the use of advanced linear algebra to reduce the dimensionality of ecological data while preserving the variance that explains species and haplotype distributions.

---

## Project Overview

The goal is to simplify a complex dataset containing over 15 distinct features into a 2D visualization, allowing for the identification of patterns in seizure data that are not easily visible in high-dimensional space.

---

## Key Implementation Details

- **Specialized Data Handling** — Correctly processes "Africanized" data formatting, including converting semicolon-delimited values and comma-based decimals (e.g., `2,08` → `2.08`) into standard numeric formats.
- **Categorical Encoding** — Dynamically identifies and encodes categorical seizure metrics (such as regression models used) into numerical values suitable for mathematical analysis.
- **Standardization** — Implements manual z-score normalization to ensure variables with different units (e.g., seizure counts vs. haplotype estimates) are scaled equally.
- **Eigendecomposition** — Utilizes the covariance matrix to derive eigenvalues and eigenvectors, identifying the principal components of the dataset.
- **Variance Analysis** — Includes a calculation of cumulative explained variance to determine how much information is retained after dimensionality reduction.

---

## Installation

Python is required to run this project.

### 1. Clone the repository

```bash
git clone <your-github-repo-link>
cd <your-repo-name>
```

### 2. Install dependencies

```bash
pip install pandas numpy matplotlib
```

| Library      | Purpose                                                           |
| ------------ | ----------------------------------------------------------------- |
| `pandas`     | Advanced data cleaning and handling semicolon-delimited CSV files |
| `numpy`      | Matrix operations and manual PCA algorithm implementation         |
| `matplotlib` | Generating the final "Before and After" comparison plots          |

---

## Usage

1. **Dataset** — Ensure `African pangolin (1).csv` is placed in the project root folder.
2. **Open the notebook** — Open `PCA_Formative_2[Peer_Pair_25].ipynb.ipynb` in VS Code or Google Colab.
3. **Execute the workflow** in order:
   - **Step 1** — Data cleaning and standardization
   - **Steps 3–5** — Covariance matrix and eigendecomposition
   - **Step 8** — Final scatter plots showing the PCA-reduced data

---

## Results

The implementation successfully reduces the pangolin seizure features into two principal components:

- **PC1** — Captures the primary axis of variance in the data
- **PC2** — Captures the secondary, orthogonal variance
  The resulting 2D scatter plot visualizes how seizure records cluster based on underlying patterns in species and haplotype distribution data.
