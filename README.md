# U1 — Uniform Spectral Universality for Weil Fingerprint Energies

This repository contains the source of the **U1 Cosmochrony paper**
[*Uniform Spectral Universality for Weil Fingerprint Energies:
Proof of [U] with Rate $O(q^{-1/2})$*](out/u1.pdf).

This work closes a technical gap in the emergent-geometry sub-programme.
The Q10 paper reduces the proof of spatial isotropy ($A_H = 2$) to a single
spectral universality hypothesis:

> **[U]** &nbsp; $\max_c |\sigma_c(n) - \sigma_*(n)| \leq \varepsilon(q)\,\sigma_*(n) \to 0$,
> uniformly over the fitting window $n \leq n_*(q)$.

The present paper **establishes [U] with rate $\varepsilon(q) = O(q^{-1/2})$**,
turning the isotropy result of Q10 into an unconditional statement.

## Conceptual Overview

The proof rests on two independent inputs about the Weil fingerprint energy
$\sigma_c(n)$, seen as a function of the reduced character $\theta = c/q$:

1. **Lipschitz continuity in $\theta$** (equicontinuity).
   $\sigma_c(n)$ is Lipschitz in $\theta = c/q$, uniformly in $n$, as a consequence
   of a standard operator-perturbation estimate on the Weil generators.

2. **Pointwise convergence** for each fixed $\theta$.
   $\sigma_c(n) \to \sigma_*(n)$ pointwise, inherited from the
   BFS–Carnot–Carathéodory convergence of Q5b at rate $O(q^{-1/2})$.

Lipschitz equicontinuity together with pointwise convergence yields **uniform
convergence on compact subsets** $\theta \in [\theta_1, 1/2]$ by the
Arzelà–Ascoli theorem. The complementary small-$\theta$ regime
$\theta \in (0, \theta_0(q))$ with $\theta_0(q) = q^{-1/2}$ is handled by a
Lipschitz triangle argument and requires **no Born–Infeld input**. Combining the
two regimes gives the uniform rate $\varepsilon(q) = O(q^{-1/2})$.

## Core Results

1. **Uniform universality [U] holds**, with explicit rate $\varepsilon(q) = O(q^{-1/2})$.
2. **The rate is structural**: it is inherited from the $O(q^{-1/2})$ convergence
   of the underlying sub-Riemannian (Q5b) geometry, not fitted.
3. **Isotropy becomes unconditional**: the $A_H = 2$ result of Q10 no longer
   depends on an assumed universality hypothesis.
4. **The argument is elementary given its two inputs**: perturbative Lipschitz
   continuity plus Arzelà–Ascoli, with no appeal to the Born–Infeld dynamics.

## What This Paper Does Not Assume

- no Born–Infeld input in the small-$\theta$ regime,
- no fitted convergence rate (the $O(q^{-1/2})$ rate is derived from Q5b),
- no uniformity beyond the compact fitting window $n \leq n_*(q)$,
- no dynamical or background-geometry assumptions.

## Keywords

Weil representation, Heisenberg group, BFS convergence, Lipschitz continuity,
Arzelà–Ascoli, spectral universality, Gromov–Hausdorff convergence.

## Repository Contents

```
u1/
├── tex/         # LaTeX sources (u1.tex, cosmochrony-bibliography.bib, references.bib)
├── out/         # Compiled paper PDF (u1.pdf)
├── compile.sh   # Build script (pdflatex + bibtex)
├── zenodo.json  # Zenodo deposition metadata
└── README.md
```

## Compilation

```bash
bash compile.sh
# or manually:
pdflatex -output-directory=out tex/u1.tex
cd out && bibtex u1 && cd ..
pdflatex -output-directory=out tex/u1.tex
pdflatex -output-directory=out tex/u1.tex
```

## Links

- 📄 [Paper PDF](out/u1.pdf)
- 🔗 DOI: [10.5281/zenodo.19881146](https://doi.org/10.5281/zenodo.19881146)
- 🌐 Website: https://cosmochrony.org/science/emergent-geometry/u1/

## Citation

If you reference this work, please cite:

> J. Beau, *Uniform Spectral Universality for Weil Fingerprint Energies:
> Proof of [U] with Rate $O(q^{-1/2})$*, Zenodo, 2026.
> DOI: 10.5281/zenodo.19881146.

## Acknowledgements

Portions of the editorial refinement benefited from iterative interactions with
large language models, used as analytical assistants for exploring alternative
formulations, checking internal consistency, and improving clarity.
All claims, interpretations, and final formulations remain the sole
responsibility of the author.

## Contributions

This repository is intended as a research reference. Critical feedback,
independent analyses, and formal scrutiny are welcome. Please open an issue to
discuss the Lipschitz continuity estimate, the Arzelà–Ascoli argument, the
small-$\theta$ regime, or the inherited $O(q^{-1/2})$ rate.
