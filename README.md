# AI Meets Geometry — Lecture Notebooks

Introductory Jupyter notebooks for the **XXII EGD School** (Piauí, Brazil 2026).  

No prior background in differential geometry or machine learning is assumed.

## Contents

| Notebook | Topic |
|----------|-------|
| `Lecture_2/lecture_2-part-I.ipynb` | Rediscovering Euler's formula with a single neuron |
| `Lecture_2/lecture_2-part-II.ipynb` | Learning a Ricci-flat Calabi–Yau metric (supervised) |
| `Lecture_3/lecture_3.ipynb` | Learning Willmore-minimising maps for the Clifford torus |

## Getting Started

See [`environment/README.md`](environment/README.md) for setup instructions, then open any of the
notebooks above in JupyterLab or VS Code.

## Lecture 2 Background

Two hands-on PyTorch notebooks introducing the recipe **encode → choose a loss → train → verify**,
first on a problem whose answer is a theorem, then on one with no closed-form answer at all.

**Part I — Rediscovering Euler's formula.** From a dataset of convex polytopes generated entirely
in the notebook (prisms, antiprisms, pyramids, the Platonic and Archimedean solids, and random
convex hulls), a single linear neuron learns the map $(V,E)\mapsto F$ and rediscovers **Euler's
polyhedron formula**

$$V - E + F = 2,$$

without ever being told it. Famous solids are held out as a test set to check that it generalises,
and the setup scales up to 4-polytopes to recover the general **Euler–Poincaré** relation.

**Part II — Learning a Ricci-flat Calabi–Yau metric.** The same four-step recipe is applied to a
genuinely hard object: the Ricci-flat Kähler metric on the **Fermat quintic** threefold

$$Q = \big\{[z_0:\dots:z_4]\in\mathbb{P}^4 \ :\ \textstyle\sum_{i=0}^4 z_i^5 = 0\big\}.$$

Yau's theorem guarantees such a metric exists and is unique in each Kähler class, but gives no
formula. An expensive *teacher* produces ground-truth metrics via **Donaldson's balanced-metric
algorithm**, a fast *student* network learns them by minimising mean-squared error, and an
independent **$\sigma$-measure** reports how close the result is to Ricci-flat. Method after
Ashmore, He & Ovrut, *Machine Learning Calabi–Yau Metrics*
([arXiv:1910.08605](https://arxiv.org/abs/1910.08605)).

## Lecture 3 Background

Developed from the paper
[*Minimising Willmore Energy via Neural Flow*](https://arxiv.org/abs/2604.04321)
by E. Hirst, H. N. Sá Earp, and T. S. R. Silva.

The **Willmore energy** of a smooth surface $\varphi : \Sigma \to \mathbb{R}^3$ is

$$W(\varphi) = \iint_\Sigma H^2 \, dA,$$

where $H$ is the mean curvature. The **Willmore conjecture** (Marques–Neves 2012) states
that among all embedded tori the minimum is

$$W \geq 2\pi^2,$$

achieved uniquely by the **Clifford torus**. The notebooks demonstrate how a small
Physics-Informed Neural Network (PINN) can discover this minimum by gradient descent.

## Citation

If you use this material, please cite:

```bibtex
@article{Heyes2026,
  title = {Neural and numerical methods for G2-structures on contact Calabi–Yau 7–manifolds},
  volume = {878},
  ISSN = {0370-2693},
  url = {http://dx.doi.org/10.1016/j.physletb.2026.140566},
  DOI = {10.1016/j.physletb.2026.140566},
  journal = {Physics Letters B},
  publisher = {Elsevier BV},
  author = {Heyes,  Elli and Hirst,  Edward and Sá Earp,  Henrique N. and Silva,  Tomás S.R.},
  year = {2026},
  month = July,
  pages = {140566}
}

@article{Hirst:2026qwi,
    author       = "Hirst, Edward and Earp, Henrique N. S{\'a} and Silva, Tom{\'a}s S. R.",
    title        = "{Minimising Willmore Energy via Neural Flow}",
    eprint       = "2604.04321",
    archivePrefix = "arXiv",
    primaryClass = "math.DG",
    year         = "2026"
}
```

## License

MIT — see [LICENSE](LICENSE).
