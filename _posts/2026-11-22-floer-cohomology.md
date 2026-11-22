---
title: "Floer Cohomology"
date: 2026-11-22
excerpt: "Notes on Lagrangian Floer cohomology: Hamiltonian dynamics and Lagrangian submanifolds, the Novikov complex, pseudoholomorphic curves and compactness, the Floer moduli spaces, invariance of HF under Hamiltonian isotopy, and index and orientation theory. [Lecture 1–2](/files/notes/floer-cohomology-lec-1-2.pdf), [3](/files/notes/floer-cohomology-lec-3.pdf), [4](/files/notes/floer-cohomology-lec-4.pdf), [5](/files/notes/floer-cohomology-lec-5.pdf), [6](/files/notes/floer-cohomology-lec-6.pdf), [7](/files/notes/floer-cohomology-lec-7.pdf), [8](/files/notes/floer-cohomology-lec-8.pdf)."
---

Notes on Lagrangian Floer cohomology, with a summary of each lecture.

## Lecture 1

- Basic definitions and examples; Hamiltonian diffeotopy.
- Subspaces: isotropic, coisotropic, Lagrangian, symplectic.
- Local structure (soft results): Darboux and Weinstein theorems.
- Hamiltonian displaceability and $C^0$ rigidity of Lagrangian submanifolds.
- Some results on Lagrangian submanifolds.

## Lecture 2

- The idea of Lagrangian Floer (co)homology; history and some conditions.
- Definition of those conditions: monotone symplectic manifold, monotone Lagrangian submanifold, Maslov index, minimal Maslov number.
- Why we care about $J$-holomorphic curves: mimicking Morse theory (path space, action functional, gradient flow of the action).
- Review of Morse–Novikov cohomology: globally we have the differential $d_{L_0,L_1}$, but Morse theory can only deal with exact 1-forms $\alpha = df$, while Morse–Novikov cohomology cares about closed 1-forms.
- $CN^*(\alpha)$ and $\delta$ (informal definition); Novikov covering; why we need the Novikov ring.
- Formal definition of $CN^k(\alpha)$ as a freely generated module over $\Lambda_\alpha$, and $\delta \colon CN^k(\alpha) \to CN^{k+1}(\alpha)$ defined by $\delta(q^-) = \sum \sharp \mathcal{M}(q^-, q^+) q^+$; check that $\delta^2 = 0$.
- Construction of Floer cohomology: find $\widetilde{\rho}$ and $\mathcal{A}_{L_0,L_1}$; define the Novikov ring $\Lambda$ and its grading via the Maslov index; introduce $\widetilde{\rho}$ to make the grading well-defined.

[Read or download the PDF](/files/notes/floer-cohomology-lec-1-2.pdf).

## Lecture 3

- Basic properties of pseudoholomorphic curves $(\Sigma, j) \to (X, J)$; Bochner's formula for holomorphic maps and the energy estimate.
- Study of $f \colon D^* \cong (-\infty, 0] \times S^1 \to X$ holomorphic curve: regularity $W^{1,p}_{\mathrm{loc}} \Rightarrow C^\infty$, via the linear elliptic equation (Sobolev embedding + linear elliptic regularity, bootstrap).
- Derivation of estimates under the small energy assumption (Bochner's formula + mean value inequality, and rescaling).
- The Sacks–Uhlenbeck argument: for $\{f_j\}$ with uniformly bounded energy, after taking a subsequence, $f_j \to f_\infty$ on $\Sigma \setminus \{\text{finitely many points}\}$ with $f_\infty$ holomorphic; the method deletes the "bad disks" (those with too high energy) and then applies Ascoli–Arzelà.
- Removal of singularity: $f \colon D^* \to X$ extends to $D$ if $E(f) < \infty$; study how $f$ acts on $(-\infty, -R] \times S^1$, let $\gamma_r$ = image of $f$ restricted to $\{r\} \times S^1$ converge to $p \in X$, then estimate the norm of $df$ to get $f \in W^{1,p}$, $p > 2$, and apply Theorem I.

[Read or download the PDF](/files/notes/floer-cohomology-lec-3.pdf).

## Lecture 4

- Review of the construction of the Novikov complex $(CN^*(\alpha), \delta)$: direction, $\delta^2 = 0$; review of the Floer case.
- Formal definition of $CF^k(L_0, L_1)$ and introduction of the universal Novikov rings.
- Definition of the Floer moduli spaces $\mathcal{M}(\widetilde{\rho}^-, \widetilde{\rho}^+)$.
- Properties of $\mathcal{M}$: compactness / lack of compactness; transversality $\Rightarrow \dim \mathcal{M} = \mu(\widetilde{\rho}^+) - \mu(\widetilde{\rho}^-) - 1$; $\pi_2(X, L_i) = 0$ and $\pi_2(X) = 0$ $\Rightarrow$ no bubbling; monotone Lagrangian with $N_L \geq 3$ $\Rightarrow$ no bubbling.
- Method: assuming transversality, compare two moduli maps $f, g$ into $X$: $f(x) = g(x)$ $\Leftrightarrow$ $\dim \mathcal{M}_1 + \dim \mathcal{M}_2 \geq \dim X$; use Fredholm theory and index theory to find $\dim \mathcal{M}$.

[Read or download the PDF](/files/notes/floer-cohomology-lec-4.pdf).

## Lecture 5

- Definition of $\delta$; $\delta^2 = 0$ when $\mathcal{M}$ is compact (no bubbling).
- Statement: $HF(L_1, L_0)$ is invariant under Hamiltonian isotopy and under change of $J \in \mathcal{J}_\omega$.
- Proof: continuation map (two constructions); chain homotopy of two paths of isotopy / $J \sim J'$.
- Two examples of when and why $\delta^2 \neq 0$ ($T^2$ and $S^2$).

[Read or download the PDF](/files/notes/floer-cohomology-lec-5.pdf).

## Lecture 6

- Index of $\bar{\partial}_E$ over $\mathbb{CP}^1$ and $D$ (Riemann–Roch).
- Linearization of the Fredholm operator and the Fredholm (analytic) index.
- Index = spectral flow; using the spectral flow to compute $\mathrm{Ind}\, \bar{\partial}$ for the 1-dimensional case.
- Topological index: study $\Xi_{\mathbb{R}^n}$ and $\Xi_L \cap (\mathrm{LagGr} \setminus \Xi_{\mathbb{R}^n})$; define the topological index to be the signed intersection number of a path $c \subset \mathrm{LagGr}$ with $\Xi_L$.
- Topological index = analytic index, which explains why $\mathrm{Ind}\, D\bar{\partial}_u = \mu(\widetilde{\rho}^+) - \mu(\widetilde{\rho}^-)$.
- Orientation issue: for $(E, F) \to (D, \partial D)$, a trivialization of $F$ gives an orientation of $\mathrm{Ind}\, \bar{\partial}_{(E,F)}$; for $u \colon S^1 \times (D, \partial D) \to (X, L)$, assuming $L$ spin, we get an oriented index bundle $\{\mathrm{Ind}\, D\bar{\partial}_{w_\theta}\} \to S^1$, and hence an orientation of $\mathcal{M}(\widetilde{\rho}^-, \widetilde{\rho}^+)$.

[Read or download the PDF](/files/notes/floer-cohomology-lec-6.pdf).

## Lecture 7

[Read or download the PDF](/files/notes/floer-cohomology-lec-7.pdf).

## Lecture 8

[Read or download the PDF](/files/notes/floer-cohomology-lec-8.pdf).
