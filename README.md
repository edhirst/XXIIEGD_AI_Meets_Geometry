# AI Meets Geometry — Lecture Notebooks

Introductory Jupyter notebooks for the **XXII EGD School** (Piauí, Brazil 2026).  

No prior background in differential geometry or machine learning is assumed.

## Contents

| Notebook | Topic |
|----------|-------|
| `lecture_3.ipynb` | Learning Willmore-minimising maps for the Clifford torus |

## Getting Started

See [`environment/README.md`](environment/README.md) for setup instructions, then open
`lecture_3.ipynb` in JupyterLab or VS Code.

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
