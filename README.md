# Quantum Computing Teaching Labs

Qiskit 2.x teaching laboratories for quantum computing and structured data.

> **Status:** Private development scaffold. Make public only after the release checklist is complete.

## Intended public result

Publish concise laboratories with learning objectives, runnable notebooks, exercises, and expected outputs covering circuits, sampling, noise, graph problems, and finite-shot estimation.

## Quick start

```bash
git clone https://github.com/LukeJamesMiller/quantum-computing-teaching-labs.git
cd quantum-computing-teaching-labs
python -m venv .venv
source .venv/bin/activate
python -m pip install -e ".[dev]"
pytest
```

## Structure

- `src/`: reusable implementation
- `tests/`: correctness and regression tests
- `examples/`: short runnable demonstrations
- `notebooks/`: exposition and figure reproduction
- `scripts/`: experiment entry points
- `figures/`: generated public figures
- `data/`: public-data instructions only

Research profile: https://lukejamesmiller.com/research
