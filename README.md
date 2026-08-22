# Open Source Contributions

## 1. IB2d — Immersed Boundary Method in 2D

**Repository:** [nickabattista/IB2d](https://github.com/nickabattista/IB2d)

**Stars:** 202 ⭐ | **Forks:** 100

### Bug Report and Fix — June 14, 2026

**Issue opened:** 2026-06-14 by Md. Obaidullah, North South University

**Observation:** A single circular spring ring in still fluid driven by a 
symmetric radial fluid source was not expanding isotropically.

**Fix:** The bug was identified in the half-step convective term where 
`2*V.*Vx` was incorrectly used instead of `2*V.*Vy`. After correcting 
this, the ring stays circular with y/x ratio = 1.0000, confirmed 
reproducible at two grid resolutions.

**Confirmation:** Repository author Nick Battista (NB) confirmed the 
observation for a production test with the rubberband-with-springs example. 
The bias was clearest in the symmetric radial-source case, which explains 
why the bug went unnoticed in typical examples where differences are small 
perturbations rather than obvious failures.

**Status:** Simulation runs and maintains symmetry.

**Commit:** [a5136ac](https://github.com/nickabattista/IB2d/commit/a5136ac) — 
*"FIX: bug in half-step convective term: 2*V.*Vx --> 2*V.*Vy"*

**Affiliation:** Md. Obaidullah, North South University, Dhaka, Bangladesh
