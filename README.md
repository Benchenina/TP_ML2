# Machine Learning - Lab Session 2: Principal Component Analysis (PCA)

**Institution:** National Higher School of Advanced Technologies  
**Level:** First Year of Master (M1)  
**Academic Year:** 2026/2027  
**Course:** Machine Learning  

---

## 1. Project Overview

This laboratory session focuses on the implementation of **Principal Component Analysis (PCA)** from scratch using Python and compares its performance and numerical results with Scikit-Learn's predefined `PCA` class.

As specified, **Question 4 calculates the Correlation Matrix** directly on the standardized dataset instead of the covariance matrix.

---

## 2. Repository Contents

* `Lab_Session_2_PCA.ipynb`: Complete Jupyter Notebook containing:
  * **Part A:** Step-by-step PCA implementation from scratch using NumPy and Pandas.
  * **Part B:** PCA implementation using `sklearn.decomposition.PCA`.
  * **Part C:** Side-by-side numerical comparison, 2D scatter plots, and theoretical explanations.
* `README.md`: Project documentation and execution instructions.

---

## 3. Dataset

The dataset contains the grades of six students across four academic subjects:

* **Students:** S1, S2, S3, S4, S5, S6
* **Subjects (Features):** Mathematics, Statistics, Programming, Algorithms

---

## 4. Requirements and Installation

To execute the notebook, ensure Python 3.8+ is installed along with the following libraries:

```bash
pip install numpy pandas matplotlib scikit-learn
```

---

## 5. Execution Instructions

1. Start the Jupyter Notebook interface:
   ```bash
   jupyter notebook Lab_Session_2_PCA.ipynb
   ```
2. Run all cells sequentially from top to bottom.

---

## 6. Summary of Key Findings

* **Correlation Matrix vs. Covariance Matrix (Q4):**
  When numerical variables are standardized ($\mu = 0$, $\sigma = 1$), the covariance matrix of the standardized data is mathematically equivalent to the correlation matrix ($R = \frac{1}{n} Z^T Z$).
* **Sign Ambiguity (Q17):**
  Eigenvectors $\mathbf{v}$ and $-\mathbf{v}$ define the exact same principal component axis ($A\mathbf{v} = \lambda\mathbf{v} \iff A(-\mathbf{v}) = \lambda(-\mathbf{v})$). Any sign difference between the scratch implementation and Scikit-Learn represents a reflection across the axis and preserves all relative geometric distances.
* **Variance Retained (Q18):**
  The first two principal components account for approximately **97.63%** of the total variance ($\text{PC1} \approx 92.20\%$, $\text{PC2} \approx 5.43\%$). This demonstrates that reducing the dimensionality from 4 features to 2 principal components preserves virtually all informational content.