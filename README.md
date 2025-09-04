### Hi, I'm Fauzia 👋
**PhD student (Materials Science & Eng., UArk)** working on **molecular dynamics (MD)**, **biomolecular simulations**, and **ML for trajectory analysis**.

- 🔬 MD: NAMD/GROMACS + VMD analysis
- 🤖 ML: Python, TensorFlow/PyTorch; synthetic trajectory generation
- 🧮 HPC: SLURM on Frontera, Pinnacle, Expanse

**Pinned projects below:** MD+ML pipeline, VMD/Tcl scripts, NAMD workflows.
md-trajectory-ml/
├─ README.md
├─ src/
│  ├─ data.py
│  ├─ model.py
│  └─ train.py
├─ notebooks/
│  └─ 01_quick_demo.ipynb
├─ scripts/
│  └─ fe_surface_plot.py
├─ tests/
│  └─ test_shapes.py
├─ requirements.txt
├─ environment.yml
├─ .gitignore
└─ LICENSE

# MD-Trajectory-ML
End-to-end pipeline for analyzing MD trajectories and training ML models to generate/compare synthetic trajectories.

## Features
- Load small sample trajectories (or your own) and compute features
- Train a simple MLP/autoencoder baseline
- Plot free energy surfaces for real vs synthetic data

## Quickstart
```bash
python3 -m venv .venv && source .venv/bin/activate
pip install -r requirements.txt
python src/train.py --epochs 5
python scripts/fe_surface_plot.py --input data/sample.csv
