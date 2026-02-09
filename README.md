# Principal Component Analysis (PCA) on African Pangolin Seizure Data

This repository contains an individual implementation of **Principal Component Analysis (PCA)** applied to a wildlife dataset concerning African pangolin seizures. The project demonstrates the use of advanced linear algebra to reduce the dimensionality of ecological data while preserving the variance that explains species and haplotype distributions.

##  Project Overview

The goal is to simplify a complex dataset containing over 15 distinct features into a 2D visualization. This allows for the identification of patterns in seizure data that are not easily visible in high-dimensional space.

### Key Implementation Details:

* **Specialized Data Handling**: Correctly processes "Africanized" data formatting, including converting semicolon-delimited values and comma-based decimals (e.g., '2,08' to 2.08) into standard numeric formats.
* **Categorical Encoding**: Dynamically identifies and encodes categorical seizure metrics (like regression models used) into numerical values suitable for mathematical analysis.
* **Standardization**: Implements a manual -score normalization to ensure variables with different units (e.g., seizure counts vs. haplotype estimates) are scaled equally.
* **Eigendecomposition**: Utilizes the covariance matrix to derive eigenvalues and eigenvectors, identifying the "Principal Components" of the dataset.
* **Variance Analysis**: Includes a calculation of cumulative explained variance to determine how much information is retained after reduction.


##  Installation Instructions

To run the analysis notebook, you must have **Python 3.x** installed. The following libraries are required:

### 1. Clone the Repository

```bash
git clone <your-github-repo-link>
cd <your-repo-name>

```

### 2. Install Dependencies

You can install the necessary Python packages using pip:

```bash
pip install pandas numpy matplotlib

```

* **Pandas**: For advanced data cleaning and handling semicolon-delimited CSV files.
* **NumPy**: For matrix operations and the manual implementation of the PCA algorithm.
* **Matplotlib**: For generating the final "Before and After" comparison plots.


##  How to Use

1. **Dataset**: Ensure the file `African pangolin (1).csv` is in the project folder.
2. **Run the Notebook**: Open `Template_PCA_Formative_1.ipynb` in your preferred environment (VS Code or Google Colab).
3. **Execute Workflow**:
* **Step 1**: Run the data cleaning and standardization cell.
* **Step 3-5**: Execute the covariance and eigendecomposition steps.
* **Step 8**: Observe the final scatter plots to see how PCA has rotated and simplified the data.




## Results

The implementation successfully reduces the pangolin seizure features into two principal components:

* **PC1**: Captures the primary axis of variance in the data.
* **PC2**: Captures the secondary, orthogonal variance.
