# Sparse + Low-Rank Gaussian Graphical Models

**Research & Technical Writing · STAT 802 · May 2026**  
**Xinyu (Ricky) Wang — Statistics & Data Science PhD candidate, University of Delaware**

A technical review connecting latent-variable modeling, convex optimization, and statistical recovery in high-dimensional Gaussian graphical models.

**[Read the report (PDF)](report.pdf)** · [LaTeX source](report.tex) · [Reference paper](https://doi.org/10.1214/11-AOS949)

## My contribution

- Explained how marginalizing hidden variables produces a sparse-minus-low-rank precision matrix, distinguishing marginal from conditional dependence.
- Connected the regularized likelihood objective to tangent-space geometry and the assumptions needed for structure recovery.
- Synthesized the source paper's simulation and stock-return examples, with explicit attribution and a discussion of what their reported metrics establish.

This is a literature-review and technical-writing artifact based on **Chandrasekaran, Parrilo, and Willsky (2012)**. It presents my exposition of the material, not an original estimator, new theorem, or independently reproduced benchmark. The portfolio edition was revised in November 2026.

## At a glance

| Component | Focus |
| --- | --- |
| Statistical model | Gaussian graphical models; conditional independence; latent variables |
| Estimation | Sparse + low-rank precision decomposition; regularized maximum likelihood |
| Optimization | Convex optimization; entrywise L1 and trace/nuclear-norm penalties |
| Theory | Tangent spaces; identifiability; Fisher information; consistency |
| Scientific interpretation | Attribution of numerical results; distinction between fit and generalization |

The report's numerical table summarizes **the reference paper's results**. In particular, the reported KL values of 44.4 and 17.7 are not results of a new experiment conducted for this repository.

## Report guide

1. Why latent variables change the graph
2. A joint estimation objective
3. Geometric identifiability
4. Statistical recovery and its assumptions
5. Reported numerical evidence and limitations

## Build the PDF

Requires a LaTeX installation with the packages listed in `report.tex` (for example, TeX Live).

```bash
pdflatex -interaction=nonstopmode -halt-on-error report.tex
pdflatex -interaction=nonstopmode -halt-on-error report.tex
```

The source is self-contained. The original draft referenced two image files that were not supplied; this edition cites the original figures and uses a textual summary and an attributed table. It does not include executable model-training or simulation code.

## Reference

Chandrasekaran, V., Parrilo, P. A., & Willsky, A. S. (2012). *Latent variable graphical model selection via convex optimization*. The Annals of Statistics, 40(4), 1935–1967. [DOI](https://doi.org/10.1214/11-AOS949) · [Open-access text](https://arxiv.org/html/1008.1290)
