# Quantum Mechanics for Beginners

A beginner-friendly interactive book for learning quantum mechanics and quantum computing with Python, MyST Markdown, and Jupyter notebooks.

The project is structured as a MyST/Jupyter Book site. It combines conceptual explanations, worked code examples, exercises, a glossary, and custom SVG learning diagrams.

## Contents

- `index.md` - landing page and table of contents
- `00_welcome_and_setup.md` - setup guide and learning roadmap
- `ch01_introduction.md` - classical physics, early quantum experiments, wave-particle duality
- `ch02_*.ipynb` - mathematical foundations
- `ch03_wave_mechanics.ipynb` - Schrodinger equation, particle in a box, uncertainty, tunneling
- `ch04_spin_qubits.ipynb` - spin, qubits, Bloch sphere, gates, measurement
- `ch05_entanglement.md` - Bell states, Bell's theorem, teleportation, QKD, GHZ states
- `ch06_quantum_algorithms.ipynb` - Deutsch-Jozsa, Grover, QFT, Shor, error correction
- `exercises_ch*.md` - chapter exercises and answers
- `glossary.md` - key terms
- `assets/` - custom SVG diagrams used throughout the book
- `myst.yml` - MyST project configuration and table of contents

Generated site output lives under `_build/` and should not be edited directly.

## Requirements

This repository includes a local virtual environment at `.venv/`. If you need to recreate it, install:

- Python 3
- NumPy
- Matplotlib
- SymPy
- Jupyter / nbconvert
- Jupyter Book v2 / MyST tooling

Example setup from scratch:

```bash
python3 -m venv .venv
.venv/bin/pip install numpy matplotlib sympy jupyter nbconvert jupyter-book
```

## Run Notebooks

Open notebooks in Jupyter:

```bash
.venv/bin/jupyter notebook
```

Or execute the source notebooks non-interactively:

```bash
MPLBACKEND=Agg .venv/bin/jupyter nbconvert \
  --to notebook \
  --execute \
  --ExecutePreprocessor.timeout=180 \
  --output-dir /tmp/qmlearning_nbcheck \
  ch02_01_numbers_algebra.ipynb \
  ch02_02_functions_trigonometry.ipynb \
  ch02_03_probability_complex.ipynb \
  ch02_04_linear_algebra.ipynb \
  ch03_wave_mechanics.ipynb \
  ch04_spin_qubits.ipynb \
  ch06_quantum_algorithms.ipynb
```

## Build The Site

Build the MyST/Jupyter Book site:

```bash
.venv/bin/jupyter-book build --site --strict
```

To test without modifying the local `_build/` directory, build from a temporary copy:

```bash
rm -rf /tmp/qmlearning_build_src
mkdir -p /tmp/qmlearning_build_src
rsync -a --exclude _build --exclude .venv ./ /tmp/qmlearning_build_src/
cd /tmp/qmlearning_build_src
MPLBACKEND=Agg /path/to/QMLearning/.venv/bin/jupyter-book build --site --strict
```

## Visual Assets

The `assets/` directory contains SVG diagrams used to improve learning flow:

- `quantum_journey.svg`
- `quantum_scale.svg`
- `double_slit_interference.svg`
- `bloch_sphere_states.svg`
- `entanglement_bell_pair.svg`
- `quantum_algorithm_flow.svg`

When adding new images, prefer project-local paths such as:

```markdown
![Short descriptive alt text.](assets/example.svg)
```

## Editing Guidelines

- Edit source files only: top-level `.md`, `.ipynb`, `assets/`, and `myst.yml`.
- Do not manually edit `_build/`.
- Keep exercise pages aligned with their corresponding chapters.
- Validate notebooks after changing executable code.
- Run a strict site build after changing navigation, MyST syntax, images, or cross-page content.

## Author

Adrian Feeger
