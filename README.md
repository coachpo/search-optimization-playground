# IT00CJ42 · Search and Optimization Algorithms

This repository collects course material, shared utilities, and weekly notebooks for the IT00CJ42 course. Everything is organized to keep the shared Python code in one place while weekly exercises and mini‑projects live in their own folders.

## Quickstart

```bash
python3 -m venv .venv
source .venv/bin/activate        # Windows: .venv\\Scripts\\activate
pip install -r requirements.txt
jupyter lab                      # or: jupyter notebook
```

If you prefer Conda:

```bash
conda env create -f environment.yml  # if you create one later
conda activate it00cj42
```

## Repository Map

- `common/` — shared Python package and data used by notebooks  
  - `aerobench/` flight‑sim utilities (gcas/highlevel/lowlevel)  
  - `data/` sample datasets (`nug20.dat`, `problem1.txt`, etc.)  
  - `lectures/` reference notebooks (e.g., `tsp.ipynb`, `tsp-sa.ipynb`)  
  - `run_f16_sim.py`, `util.py` helpers
- `mini-project/` — mini‑project notebooks (`miniproject1.ipynb` …)
- `weekly-task/` — weekly exercise notebooks (`week1.ipynb` … `week8.ipynb`), assets (`experimental-data.xlsx`, `img.png`, `week6/Task1.png`)
- `requirements.txt` — minimal Python stack for the notebooks
- `.gitignore` — ignores Python/Jupyter build artefacts and checkpoints

## How to Run the Notebooks

1. Activate your environment (`.venv`/Conda).
2. Launch Jupyter (`jupyter lab` or `jupyter notebook`).
3. Open the notebook you need inside `weekly-task/` or `mini-project/`.
4. Ensure the kernel points to your environment so imports resolve.

### Data paths

- Prefer placing shared datasets in `common/data/`.
- Keep week‑specific assets inside `weekly-task/` alongside the notebook.
- Use relative paths (e.g., `../common/data/problem1.txt`) to stay portable.

## Best Practices (lightweight)

- **Keep notebooks clean**: clear outputs before committing; avoid committing `.ipynb_checkpoints/`.
- **Seeds for reproducibility**: set random seeds when using stochastic algorithms.
- **Small outputs**: avoid embedding large images/binaries directly; store them under `common/data/` or `weekly-task/`.
- **Reuse helpers**: import utilities from `common/` instead of duplicating code across notebooks.
- **Naming**: keep descriptive filenames (`week7_ga.ipynb` vs. `new.ipynb`) and short markdown headers inside notebooks.

## Contributing / Housekeeping

- Stick to the folder purposes outlined above; avoid moving shared data out of `common/data/`.
- If you add packages, append them to `requirements.txt`.
- Consider running `pip freeze > requirements-lock.txt` in your environment if you need exact versions for grading/repro.

## Mini‑projects (context)

1. Ground collision avoidance system (jet plane)
2. AI player for chess
3. Video decoding configuration for low power on SBC

## Weekly Topics (reference)

- Week 1 – Intro to optimization and metaheuristics
- Week 2 – Random & local search (hill climbing)
- Week 3 – Experimental methodology
- Week 4 – Tabu search
- Week 5 – Simulated annealing
- Week 6 – Minimax and alpha‑beta search
- Week 7 – Evolutionary & genetic algorithms
- Week 8 – Multi‑objective optimization & genetic algorithms
- Week 9 – Search‑based software engineering
