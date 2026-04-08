# ⚡ Equal Incremental Cost Method with Adjustable Gamma Control (EIC-AGC) — Initial Release
[![DOI](https://zenodo.org/badge/1204746735.svg)](https://doi.org/10.5281/zenodo.19468859)

This release provides the implementation of the **Equal Incremental Cost Method with Adjustable Gamma Control (EIC-AGC)** for generator scheduling in power systems.

The method enhances the classical Equal Incremental Cost (EIC) approach by introducing a **Gamma (γ) control parameter** to improve convergence behavior and solution accuracy.

---

## 🚀 Highlights

- Implementation of **EIC with Adjustable Gamma Control**
- Supports generator scheduling with:
  - Power balance constraint
  - Generation limits
  - Ramp rate consideration
- Achieves **100% convergence accuracy** (power matches demand)
- Provides flexible trade-off between:
  - Solution accuracy
  - Computational time

---

## 🧠 About the Method

The EIC-AGC method iteratively updates the Lagrange multiplier (λ) using a Gamma control parameter:

- λ is incrementally adjusted using γ
- Power output is recalculated for each generator
- Iteration continues until total generated power matches demand

This approach improves control over convergence speed and stability compared to the standard EIC method.

---

## 📊 Key Results

| Parameter | Value |
|-----------|-------|
| Load demand | 2,650 MW |
| Best cost | $32,289.03 /h |
| Convergence accuracy | 100% |
| Computation time | ~195 seconds |

The method achieves competitive performance and ranks second-best after VLIM in cost efficiency.

---

## 📄 Related Publication

Basuki Rahmat et al. (2024)
*Equal Incremental Cost Method with Adjustable Gamma Control to Solve Generator Scheduling*
https://doi.org/10.20895/infotel.v16i3.1170

---

## 📦 Contents

- Core implementation of EIC-AGC algorithm
- Iterative optimization approach
- Generator scheduling simulation logic
- Example configuration based on IEEE 15-unit system

---

## ⚠️ Notes

- Dataset used in the original study is not included
- Users can provide their own generator parameters:
  - Cost coefficients (a, b, c)
  - Generation limits (Pmin, Pmax)

---

## 🔗 Citation

If you use this software, please cite:

```bibtex
@article{rahmat2024eicagc,
  title={Equal Incremental Cost Method with Adjustable Gamma Control to Solve Generator Scheduling},
  author={Rahmat, Basuki and Wijaya, I.G.P.O. Indra and Ikhsan, Rifki Rahman Nur and others},
  journal={Jurnal Infotel},
  volume={16},
  number={3},
  pages={541--553},
  year={2024},
  doi={10.20895/infotel.v16i3.1170}
}
```
