# Environment Setup

## Prerequisites

- [Anaconda](https://www.anaconda.com/download) or [Miniconda](https://docs.conda.io/en/latest/miniconda.html)

## Creating the environment

```bash
# Create a fresh Python 3.10 environment
conda create -n willmore-lectures python=3.10 -y

# Activate it
conda activate willmore-lectures

# Install PyTorch (CPU build — sufficient for the notebooks)
conda install pytorch cpuonly -c pytorch -y

# Install the remaining dependencies
pip install -r requirements.txt

# Install JupyterLab so you can open the notebooks
conda install jupyterlab -y
```

## Running the notebooks

From the repository root:

```bash
conda activate willmore-lectures
jupyter lab
```

Then open `lecture_2.ipynb`.

## Notes

- All computation uses CPU with `float32`.  A GPU is *not* required.
- Expected total runtime for `lecture_2.ipynb` is **3–5 minutes** on a modern laptop.
- If you already have a suitable PyTorch environment, you can skip the `conda create`
  step and just run `pip install -r requirements.txt` inside it.
