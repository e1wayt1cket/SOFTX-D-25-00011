# SOFTX-D-25-00011 — ASSUME Framework

> **Paper submission**: "ASSUME: Agent-based Simulation for Studying and Understanding Market Evolution"
>
> This repository accompanies a software paper submitted to SoftwareX (Elsevier).

## About

This repository contains a frozen snapshot of the [ASSUME framework](https://github.com/assume-framework/assume) — an open-source toolbox for agent-based electricity market simulations with Deep Reinforcement Learning integration.

ASSUME enables research into electricity market designs, bidding strategies, and market dynamics through:

- Agent-based modeling of day-ahead, intraday, and balancing markets
- Multiple market clearing algorithms (simple, complex, nodal, redispatch)
- Deep Reinforcement Learning for adaptive bidding strategies (MATD3)
- Grid-aware market simulation with PyPSA and pandapower
- Scenario loading from CSV, OEDS, AMIRIS, and PyPSA formats
- TimescaleDB + Grafana integration for result analysis

## Attribution

ASSUME is developed by researchers from INATECH (University of Freiburg), IISM (KIT), Fraunhofer ISI, Fraunhofer IEG, and FH Aachen, funded by the German Federal Ministry for Economic Affairs and Climate Action (BMWK).

- **Upstream repository**: [assume-framework/assume](https://github.com/assume-framework/assume)
- **Documentation**: [assume.readthedocs.io](https://assume.readthedocs.io/)
- **DOI**: [10.5281/zenodo.8088760](https://doi.org/10.5281/zenodo.8088760)
- **License**: AGPL-3.0-or-later

## Installation

```bash
pip install assume-framework

# With reinforcement learning
pip install 'assume-framework[learning]'

# With network clearing (requires PyPSA)
pip install 'assume-framework[network]'

# Full installation
pip install 'assume-framework[all]'
```

## Quick Start

```bash
# Run an example simulation
python examples/examples.py

# Or use the CLI
assume -s example_01b -db "postgresql://assume:assume@localhost:5432/assume"
```

Docker Compose is available for TimescaleDB + Grafana dashboard setup:

```bash
docker-compose up -d
# Access Grafana at http://localhost:3000
```
