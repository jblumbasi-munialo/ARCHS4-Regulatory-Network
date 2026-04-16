# Regulatory Network Reconstruction

## Overview
A computational pipeline for reconstructing transcription factor-gene regulatory networks using expression data, machine learning, and blockchain.

## Key Results

| Metric | Value |
|--------|-------|
| Samples | 200 |
| Genes | 10,000 |
| Regulatory Edges | 637 |
| Network Density | 0.102 |
| Communities | 5 |

## Top Regulators
- **ANXA2** (Degree: 0.625) - Cell signaling
- **ALDOA** (Degree: 0.615) - Glycolysis
- **AKR1C2** (Degree: 0.563) - Metabolism
- **B2M** (Degree: 0.510) - Immune response
- **ACTB** (Degree: 0.469) - Cytoskeleton

## Repository Structure
```
├── data/          # Expression & correlation data
├── figures/       # All visualizations
├── network/       # Cytoscape files (.graphml)
├── ml_results/    # ML predictions
├── blockchain/    # Immutable ledger
└── survival/      # KM & Cox analysis
```

## Quick Start
```python
import pandas as pd
import networkx as nx

# Load network
G = nx.read_graphml('network/regulatory_network.graphml')
print(f'Nodes: {G.number_of_nodes()}, Edges: {G.number_of_edges()}')
```

## Methods
- **Data**: ARCHS4 (real RNA-seq)
- **Inference**: GRNBoost2, Correlation, Random Forest
- **Validation**: ENCODE ChIP-seq, Motif analysis
- **Analysis**: Graph theory, Communities, Pathways
- **Clinical**: Disease associations, Drug targets, Survival

## Output Files

| File | Description |
|------|-------------|
| `regulatory_network.graphml` | Cytoscape-ready network |
| `grnboost2_network.csv` | 637 regulatory edges |
| `consensus_network.graphml` | Ensemble network |
| `drug_targets.csv` | Top therapeutic targets |
| `survival_analysis_results.csv` | KM statistics |

## Citation
```bibtex
@misc{RegulatoryNetwork2026,
  author = {HCMI-CMDC Research Team},
  title = {Regulatory Network Reconstruction},
  year = {2026}
}
```

---
**HCMI-CMDC Bioinformatics Pipeline**