# U1 — Uniformity Requirements for Weil Fingerprint Energies

This repository contains the source of the **U1 Cosmochrony paper**
*Uniformity Requirements for Weil Fingerprint Energies:
Obstructions to the Lipschitz Route to [U]*.

**Version 2.0, published.** The concept DOI below resolves to this version.

Q10 proposes a conditional route from spectral universality to the isotropy
identification ($A_H = 2$). Its coefficient and geometric steps await a separate
audit. The input it calls [U] is:

> **[U]** &nbsp; $\max_c |\sigma_c(n) - \sigma_*(n)| \leq \varepsilon(q)\,\sigma_*(n)$,
> uniformly over the fitting window $n \leq n_*(q)$, with $\varepsilon(q) \to 0$.

Version 1 of this paper claimed to prove [U] with rate $\varepsilon(q) = O(q^{-1/2})$.
**That proof is wrong, and version 2.0 withdraws the claim.** [U], its rate and
the identification $A_H = 2$ are open on the inputs available here. Nothing in
this paper shows [U] to be false.

## What is proved

**Theorem 1.1 (equidistance obstruction).** For every prime $q \geq 5$ and all
distinct central characters $c \neq c'$, the Heisenberg multiplication generators
satisfy

$$\|\rho_{q,c}(X) - \rho_{q,c'}(X)\|_{\mathrm{op}} = 2\cos\left(\frac{\pi}{2q}\right) > 1.90,$$

a value **independent of $c$ and $c'$** and tending to $2$. Distinct central
characters are therefore mutually equidistant, uniformly in $q$: the generator
distance carries no information about $|c - c'|$, and no modulus of continuity
in the reduced character $\theta = c/q$ can be extracted from it.
Separately, the example $c=1$, $c'=2$ shows that the summed operator has a
distance tending to $4$ even though $|c-c'|/q\to0$.

This is an unconditional statement about finite Heisenberg–Schrödinger representations.
The associated Weil action is distinct. The theorem uses none of
the Q5a–Q5b hypotheses, so the paper no longer stands or falls with them.

## What is withdrawn, and why

1. **The generator estimate was false.** Version 1 asserted
   $\|\rho_{q,c}(s) - \rho_{q,c'}(s)\| \leq 2\pi|c-c'|/q$. At $q = 61$ with
   $c' = c+1$, that bound reads $0.1030$ while the true distance is $1.9993$.
   The maximisation over $k$ lost a factor $q-1$. This is not a matter of
   constants: Theorem 1.1 rules out the claimed individual-generator estimate,
   and the separate summed-operator example rules out its proposed replacement.
   The equicontinuity input of the former proof is unavailable.

2. **The observable was silently replaced.** O25 defines $\delta r_n$ as the
   *number* of shell-$n$ fingerprint vectors linearly independent of the
   Gram–Schmidt span of the earlier shells, measured on a three-component block
   under a sampling protocol. Version 1 set this integer equal to a compressed
   operator norm $\|\Pi_{S_n} \, d\rho_{q,c} \, \Pi_{S_n}\|_{\mathrm{op}}$
   without any identification, and without defining $\Pi_{S_n}$ as a subspace of
   the $q$-dimensional carrier.

3. **The imported rate does not exist.** Version 1 attributed a
   Gromov–Hausdorff rate $O(q^{-1/2})$ to Q5b Theorem 2.1. That theorem is the
   Bass–Guivarc'h ball growth $|B_n| \sim Cn^4$; Q5b's Carnot convergence
   theorem is qualitative and states no rate.

Further retyped steps: the $\theta$-independence argument used a Carnot
dilation, which is an equivalence after pullback and does not preserve the
central character; Arzelà–Ascoli yields uniform convergence but no rate; the
small-$\theta$ argument reversed an inequality and substituted a $q$-dependent
$\theta_1$ into a fixed-$\theta_1$ proposition; and absolute error was exchanged
for the relative error [U] actually demands.

## What remains usable

- The operator-norm stability inequality
  $\bigl|\|PAP\| - \|PBP\|\bigr| \leq \|A - B\|$, at its own scope.
- The O25 measurements, as measurements.

The former parity reduction $c\leftrightarrow q-c$ is not retained for O25's
sampled-block observable: O22 does not prove equality of those rank increments.

## Consequences

Corollary 7.1 is withdrawn in full: $A_H(q) \to 2$ is not established here, the
effective co-metric $g^{\mu\nu} = \mathrm{diag}(-A_\tau, 2, 2, 2)$ is not
established by this paper, and the claim to resolve the Q7 bridge in the
isotropic case is withdrawn. Q10's proposed coefficient step awaits separate
audit and remains conditional on [U].

Remark 7.4 states the two estimates a proof of [U] would still have to supply:
a proved comparison between the O25 rank increment and whatever analytic
quantity is estimated, and a quantitative transfer from metric convergence of
BFS balls to the independence count, in relative form.

## Keywords

Weil fingerprint, finite Heisenberg representation, central character, operator perturbation,
spectral universality, equicontinuity, Gram–Schmidt rank increment, withdrawn
claim.

## Repository Contents

```
u1/
├── tex/         # LaTeX sources (u1.tex, cosmochrony-bibliography.bib, references.bib)
├── compile.sh   # Build script (pdflatex + bibtex)
├── zenodo.json  # Zenodo deposition metadata
├── CITATION.cff # Citation metadata
└── README.md
```

## Compilation

```bash
bash compile.sh
```

## Links

- 🔗 Concept DOI: [10.5281/zenodo.19881146](https://doi.org/10.5281/zenodo.19881146)
- 🌐 Website: https://cosmochrony.org/science/emergent-geometry/u1/

## Citation

If you reference this work, please cite:

> J. Beau, *Uniformity Requirements for Weil Fingerprint Energies:
> Obstructions to the Lipschitz Route to [U]*, Zenodo, 2026.
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
discuss the equidistance obstruction, the status of the O25 observable, or the
estimates a proof of [U] would require.
