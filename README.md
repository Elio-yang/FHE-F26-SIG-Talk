# Overview of Fully Homomorphic Encryption (FHE)

*Construction, Application and Acceleration* — SIG talk, Fall 2026

Yang Yang, Insight Computer Architecture Lab, Department of Computer Science, University of Virginia (yangyang@virginia.edu)

## Contents

| File | Description |
| --- | --- |
| `fhe-sig.pdf` | Talk slides |
| `fhe_showcase.ipynb` | Companion notebook that reproduces the slides' constructions. Sections 0–3 use plain numpy (lattice problems, NTT/CRT, toy CKKS); Section 4 uses the OpenFHE Python bindings for real-size CKKS. |
| `2026-06-FHE_Cheddar_Tutorial_1.pdf` | J. H. Ahn, J. Kim, W. Choi, *FHE & Cheddar*, ISCA 2026 tutorial (lecture part) |
| `2026-06-FHE_Cheddar_Tutorial_2.pdf` | Same tutorial (live-coding part) |

The notebook needs `numpy`, `scipy`, `matplotlib`, `plotly`, and `openfhe` (the last one only for Section 4).

## References

**Foundations**

1. C. Gentry, *A Fully Homomorphic Encryption Scheme*, PhD thesis, Stanford, 2009.
2. M. van Dijk, C. Gentry, S. Halevi, V. Vaikuntanathan, "Fully Homomorphic Encryption over the Integers," EUROCRYPT 2010.
3. O. Regev, "On Lattices, Learning with Errors, Random Linear Codes, and Cryptography," STOC 2005.
4. NIST, FIPS 203 (ML-KEM) and FIPS 204 (ML-DSA), 2024.
5. J. H. Cheon, A. Kim, M. Kim, Y. Song, "Homomorphic Encryption for Arithmetic of Approximate Numbers," ASIACRYPT 2017.
6. Microsoft SEAL, CKKS basics example (`native/examples/5_ckks_basics.cpp`).

**Figures and tutorial**

7. J. H. Ahn, J. Kim, W. Choi, *FHE & Cheddar*, ISCA 2026 tutorial — source of the HE-flow figures and of the GPU-section charts and tables.
8. Jayashankar et al., "Cerium: A GPU-Efficient Framework for FHE-Based Inference," arXiv:2512.11269 — RNS-CKKS figure.

**GPUs and accelerators**

9. S. Kim, W. Jung, J. Park, J. H. Ahn, "Accelerating Number Theoretic Transformations for Bootstrappable HE on GPUs," IISWC 2020.
10. W. Jung et al., "Accelerating FHE Through Architecture-Centric Analysis and Optimization," IEEE Access 2021.
11. W. Jung, S. Kim, J. H. Ahn, J. H. Cheon, Y. Lee, "Over 100x Faster Bootstrapping in FHE through Memory-centric Optimization with GPUs," CHES 2021.
12. W. Choi, J. Kim, J. H. Ahn, "Cheddar: A Swift FHE Library Designed for GPU Architectures," ASPLOS 2026.
13. W. Choi et al., "Theodosian: A Deep Dive into Memory-Hierarchy-Centric FHE Acceleration," arXiv 2026.
14. S. Kim et al., "BTS," ISCA 2022; J. Kim et al., "ARK," MICRO 2022; J. Kim et al., "SHARP," ISCA 2023.
15. E. Lee et al., "Low-Complexity Deep Convolutional Neural Networks on FHE Using Multiplexed Parallel Convolutions," ICML 2022.
16. J. H. Ju et al., "NeuJeans: Private Neural Network Inference with Joint Optimization of Convolution and FHE Bootstrapping," CCS 2024.
17. D. B. Cousins et al., "TREBUCHET Fully Homomorphic Encryption Accelerator: Phase Two Performance Estimation Results," GOMACTech 2024.
18. N. P. Jouppi et al., "Ten Lessons From Three Generations Shaped Google's TPUv4i," ISCA 2021.

## Acknowledgment

The GPU-section figures, charts, and tables are taken from the *FHE & Cheddar* ISCA 2026 tutorial by J. H. Ahn, J. Kim, and W. Choi [7]. The tutorial PDFs in this repository are their work, and all rights to them remain with the authors.

These slides were organized with help from **Claude Code** (Anthropic): restructuring the CKKS section for an architecture audience, the worked NTT / CRT / CKKS examples (every number checked by script), the TikZ figures, the GPU-section charts and tables taken from [7], and the build setup.
