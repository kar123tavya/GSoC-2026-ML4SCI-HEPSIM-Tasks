# HEPSIM: Jet Observable Library for Simulation Validation
### GSoC 2026 Evaluation Task | ML4SCI

This repository contains the complete implementation of the evaluation tasks for the **HEPSIM** project. The goal of this work is to develop a standardized library of jet observables to quantify simulation biases between Monte Carlo generators like **Pythia 8** and **Herwig**.

## 🚀 Key Achievements
* **Robust Data Ingestion**: Successfully processed the `QG_jets.npz` dataset (100,000 jets), implementing zero-padding removal to recover true constituent multiplicities.
* **Physics Feature Engineering**: Derived four-momentum kinematics $(E, p_x, p_y, p_z)$ to calculate core jet observables: Invariant Mass ($m_J$), Jet Width ($w$), and $p_T$ Dispersion ($p_DT$).
* **Lorentz Covariance**: Engineered a relativistic Lorentz boost to the jet rest frame (Center-of-Momentum frame). Verified the implementation by confirming total 3-momentum conservation to $O(10^{-12})$ GeV.
* **ML Classification**: Trained a Random Forest classifier achieving a **Test AUC of 0.8629**.
* **Interpretability**: Conducted feature importance analysis, identifying **Constituent Multiplicity** as the dominant physical discriminant (approx. 49% importance), consistent with QCD theoretical expectations ($C_A/C_F$ color factor ratios).

## 🛠️ Technologies Used
* **Python 3.13**
* **NumPy & SciPy**: Vectorized kinematic computations and Lorentz transformations.
* **Scikit-Learn**: Machine learning pipeline and diagnostic metrics.
* **Matplotlib**: Statistical distribution plotting and rest-frame visualizations.

## 📊 Summary of Findings
The analysis confirms that gluon-initiated jets exhibit higher multiplicity and broader angular distributions compared to quark-initiated jets. The successful rest-frame transformation demonstrates a baseline for developing frame-agnostic libraries for the HEPSIM database.

---
**Applicant:** Kartavya Rustagi  
**Institution:** Delhi Technological University  
**Project:** HEPSIM - Jet Observable Library
