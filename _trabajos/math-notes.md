---
title: "Math Notes"
date: 2025-12-31
categories:
  - "trabajos"
# layout: page_light
---

> [!NOTE] Summary
> These notes collect some useful math links.

Six-functor formalisms:
- A gentle introduction: Gallauer's [An introduction to six-functor formalisms](https://arxiv.org/abs/2112.10456).
- Why do we need $\infty$-categories? There is a nice brief explanation in the introduction of Liu-Zheng's [Enhanced six operations and base change theorem for higher Artin stacks](https://arxiv.org/abs/1211.5948). Their another paper, [Gluing restricted nerves of ∞-categories](https://arxiv.org/abs/1211.5294), deals with the glueing of simplicial nerves associated with **multisimplicial** nerves.

Connectivity in integral $p$-adic Hodge theory:
- AMMN's [On the Beilinson fiber square](https://arxiv.org/abs/2003.12541), syntomic complexes are integral modification of étale cohomology.
- Bhatt-Mathew's [Syntomic complexes and $p$-adic étale Tate twists](https://arxiv.org/abs/2202.04818v2): syntomic complexes is compared with the truncated étale cohomology, the difference lies only in the top degree, where syntomic complexes do not touch the whole symbol filtration but only the integral part (the coherent part, not the log-differential part).

Root stacks and Kato-Nakayama spaces:
- CSST's [paper](https://arxiv.org/pdf/1511.00037)

Modular forms and Elliptic Curves Database:
- <https://www.lmfdb.org/EllipticCurve/>

Hellmann: $A$ is more like coefficient -- we do not take the FF-curve.

$$
\newcommand{\B}{\mathbf{B}}
\newcommand{\Sfrak}{\mathfrak{S}}
\newcommand{\DM}{\mathrm{DM}}
\newcommand{\FF}{\mathrm{FF}}
\newcommand{\RigDA}{\mathrm{RigDA}}
\newcommand{\sp}{\mathrm{sp}}
$$

Vezzani: motives give you "mysterious pullback functors" that would not exist if we do not contract $\B^1$.
- The motivic "specialisation functor" $\Sfrak_\eta \to \Sfrak_0$ that allows pullback $\sp^* \colon \DM(\Sfrak_0) \to \RigDA(\Sfrak_\eta)$.
- The motivic "map" $X_{\FF,S} \to S$ that gives $\pi^* \colon \RigDA(S) \to \RigDA(X_{\FF,S})$.
- (Spreading out) If $S \sim \varprojlim_\alpha S_\alpha$, then $\RigDA(S) \simeq \varinjlim_{\alpha,\mathrm{Pr}^L} \RigDA(S_\alpha)$.
	- Subtleties: cannot descent smooth maps over $S$ to some $S_\alpha$ without homotopies.