Here are the list of the main papers for this project 
Here is a professionally structured `README.md` for your `/papers` folder. This file acts as an annotated bibliography, helping students understand why each paper is included and which sections are most critical for their coding tasks.

---

# 📚 Research Library: Optimizer Foundations

This directory contains the seminal papers and technical reports that form the mathematical basis for the **Gradient Games** project.

## 📂 Core Papers

### 1. Muon: Matrix-Aware Optimization

* **Title:** *Muon: An optimizer for hidden layers in neural networks*
* **Author:** Keller Jordan (2024)
* **Key Contribution:** Introduces the use of **Newton-Schulz iteration** to perform post-processing orthogonalization on SGD-momentum updates.
* **Reading Focus:** * **Section 3 (Algorithm):** Understand why Muon is only applied to  2D parameters.
* **Newton-Schulz convergence:** Note the specific coefficients  used in the update rule to ensure the matrix approaches the Stiefel manifold.



### 2. MARS: Variance Reduction

* **Title:** *MARS: Unleashing the Power of Variance Reduction for Training Large Models*
* **Authors:** Yuan et al. (2024)
* **Key Contribution:** Proposes **Recursive Momentum**, a technique that corrects gradient drift to achieve better "gradient complexity" than AdamW.
* **Reading Focus:**
* **Algorithm 1:** The mathematical definition of "Scaled Stochastic Recursive Momentum."
* **Convergence Analysis:** Compare the  rate against standard adaptive methods.



### 3. Lion: Symbolic Discovery

* **Title:** *Symbolic Discovery of Optimization Algorithms*
* **Authors:** Chen et al. (Google Brain, 2023)
* **Key Contribution:** Uses program search to discover a sign-based optimizer that is more memory-efficient and often faster than Adam.
* **Reading Focus:**
* **Algorithm 1:** Notice the simplicity of the `sign()` function update and the lack of a second-moment () term.



### 4. AdamW: The Gold Standard

* **Title:** *Decoupled Weight Decay Regularization*
* **Authors:** Loshchilov & Hutter (2017)
* **Key Contribution:** Identifies the flaw in how Adam handles  regularization and introduces **Weight Decay Decoupling**.
* **Reading Focus:**
* **Figure 1 & 2:** Comparison of the hyperparameter landscapes between Adam and AdamW. This is the baseline your students must attempt to "beat."



---

