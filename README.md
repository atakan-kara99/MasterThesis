# Master Thesis (LaTeX project)

Short repository for a Master's thesis written in LaTeX. This repo contains the source files, figures and data used to build the [final PDF](Masterarbeit___Atakan_Kara.pdf) of the thesis.

**NOTE: THIS THESIS IS RELATED TO THE [CODE FRAMEWORK](https://github.com/atakan-kara99/AutoencoderFramework).**

### Title: Autoencoder Architectures and Loss Objectives for Preserving In-Between Instances

## Abstract

Autoencoders are widely used for representation learning, yet they tend to blur the transitional regions between clusters where “in-between instances” (IBIs) reside, points that share affinities with multiple groups and carry important structural information. This thesis systematically studies how architectural choices and, more decisively, loss objectives affect an autoencoder’s ability to preserve IBIs. In a controlled setting with basic feed-forward autoencoders, we evaluate ten synthetic 2D/3D datasets containing explicit IBI ground truth and restrict latents to two or three dimensions for direct visual adjudication of cluster geometry and IBI placement. We also introduce a differentiable “soft trustworthiness” loss that approximates neighborhood preservation for gradient-based training, and we compare unsupervised losses (MSE, cosine similarity, KLD, soft trustworthiness) with supervised extensions (triplet margin, cosine embedding). 
Architecturally, deeper/wider networks in 2D reduce reconstruction error and, within reasonable capacity, preserve cluster topology and credible IBI bridges. This correlation weakens in 3D, where low MSE does not reliably predict faithful transitional geometry. Pragmatic baselines of 2–32–16–8–1 (2D) and 3–64–32–16–2 (3D) are adopted for loss studies. 
MSE emerges as the most stable objective across datasets, maintaining distinct clusters, plausible global layout, and appropriate IBI placement. Cosine similarity is a weaker but serviceable alternative on simpler structures. KLD consistently collapses structure, obscuring both cluster identity and IBI function. Soft trustworthiness is parameter-sensitive and prone to 1D collapse in reconstruction space, yet uniquely succeeds on topologically demanding cases (e.g., unrolling Swiss roll, partially disentangling a torus, separating encapsulated spheres), motivating hybrid objectives that pair MSE for global shape with soft trustworthiness for local neighborhoods. 
Supervision further strengthens class-aware organization: triplet margin and cosine embedding generally improve separability and often place IBIs in credible bridges, with triplet loss more consistently preserving inter-cluster relations. However, both can sacrifice global manifold geometry, reinforcing the value of reconstruction-anchored hybrids. 
Overall, the results show that careful loss design matters more than marginal architectural tweaks for preserving IBIs, and they chart a concrete path toward composite objectives that reconcile global fidelity, neighborhood truthfulness, and semantic separation.

## Roadmap

The project roadmap is included as a PDF in the repository and can be viewed below.

<p>
  <img src="images/roadmap.png" alt="Roadmap">
</p>

## What this repository contains

- `main.tex` — top-level LaTeX file (entry point)
- `0_abstract.tex`, `1_introduction.tex`, `2_theoretical_foundation.tex`, `3_related_work.tex`, `4_method.tex`, `5_experiments.tex`, `6_conclusion.tex`, `7_appendix.tex` — chapter/source files
- `5.1_rq1.tex`, `5.2_rq2.tex`, `5.3_rq3.tex` — experiment sub-sections used from `5_experiments.tex`
- `bibliography.bib` — BibTeX bibliography file
- `images/` — directory with figures and dataset visualizations (subfolders: `datasets`, `RQ1`, `RQ2`, `RQ3`)
