# Entanglement Entropy across the Quantum Phase Transition in the 1D Transverse-Field Ising Model

This repository contains my **final project** for the course *Scientific Computing in Quantum Information Science* @ DTU (2025).  
The project explores **entanglement entropy as a probe of quantum phase transitions**, using both exact diagonalization and **classical shadow tomography** [Huang et al., Nat. Phys. 2020](https://doi.org/10.1038/s41567-020-0932-7).

---

## 🔍 Motivation
The transverse-field Ising model (TFIM) is one of the simplest models that exhibits a **quantum phase transition** at $g/J = 1$.  
Entanglement entropy between two halves of the chain serves as a clear diagnostic of criticality.  

This project demonstrates:
- Exact computation of **von Neumann entropy** across the transition  
- Comparison with **Rényi-2 entropy**  
- **Classical shadows** as an efficient method to estimate entanglement entropy from simulated measurements

---

## ⚙️ Methods
- **Model**: 1D TFIM with periodic boundary conditions
- **Exact Diagonalization**: Compute ground states for system sizes $N=5 \dots 9$
- **Entanglement Entropy**:
  - von Neumann entropy: $S(\rho_A) = -\mathrm{Tr}(\rho_A \log \rho_A)$  
  - Rényi-2 entropy: $S_2(\rho_A) = -\log_2 \mathrm{Tr}(\rho_A^2)$  
- **Classical Shadows**:
  - Random Pauli measurements (tensor product basis)
  - Inverse channel estimator
  - Median-of-means (MoM) for error mitigation

---

## 📊 Results
- **Entropy scaling** shows a clear peak near the critical point $g/J = 1$  
- **von Neumann entropy** captures the critical entanglement growth  
- **Classical shadows** reproduce Rényi-2 entropy with moderate shot complexity  

<p align="center">
  <img src="figures/vn_entropy_vs_g.png" width="450"/>
  <img src="figures/shadow_entropy_vs_g.png" width="450"/>
</p>

---

## 📚 References
- Huang, H.-Y., Kueng, R., & Preskill, J. (2020). *Predicting many properties of a quantum system from very few measurements*.  
  Nature Physics, 16, 1050–1057. [doi:10.1038/s41567-020-0932-7](https://doi.org/10.1038/s41567-020-0932-7)

---

## 👤 Author
**Junwoo Jung** (KAIST, Exchange at DTU 2025)  
📧 Contact: [GitHub Profile](https://github.com/junwoojung0908)