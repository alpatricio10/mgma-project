# Graph Machine Learning Analysis Project

## Overview

This project explores a range of graph machine learning methods — including community detection, link prediction, node classification, and knowledge graph embedding — across four real-world graph datasets. The analysis includes preliminary statistics, centrality measures, community detection, embedding methods, GNN-based models, and clear visualizations. All work is reproducible in Jupyter notebooks.

## Content

- `Patricio_Olajuyigbe_Part1.ipynb` — Community detection and graph analysis on Facebook and Email datasets (Part 1)
- `Patricio_Olajuyigbe_Part2.ipynb` — KG embeddings and GNN-based link prediction on Different Datasets (Part 2)
- `Progress.ipynb` — Some random initial experiments for Part 2
- Requirements file (`requirements.txt`)
- Data sources (see below)
  
## Instructions

### 1. Data Sources

- **ArXiv GR-QC Collaboration Network:** https://snap.stanford.edu/data/ca-GrQc.html
  - Undirected scientific collaboration network from the General Relativity and Quantum Cosmology section of arXiv (5,242 nodes, 14,496 edges)
  - Nodes represent authors; edges represent co-authorship relationships. Papers with multiple co-authors form fully connected subgraphs
  - Time span: January 1993 – April 2003 (124 months)
  - Download the `ca-GrQc.txt.gz` file from the link above, extract the `ca-GrQc.txt` file and place in a `data/` directory.

- **SNAP BioDecagon (Polypharmacy Side Effects):** http://snap.stanford.edu/decagon/
  - Multimodal graph capturing relationships between drugs, proteins, and polypharmacy side effects
  - Drug–Drug interactions: ~4.6M edges across 964 side-effect types linking ~19K drugs (`bio-decagon-combo.csv`)
  - Protein–Protein interactions (PPI): ~715K undirected edges linking ~19K proteins (`bio-decagon-ppi.csv`)
  - Drug–Target interactions: ~18.7K edges linking drugs to their protein targets (`bio-decagon-targets.csv`)
  - Individual drug side effects: ~175K entries mapping drugs to known single-drug side effects (`bio-decagon-mono.csv`)
  - Download the files from the link above, extract them and place in a `data/` directory.

- **SNAP Facebook Social Network Graph:** https://snap.stanford.edu/data/ego-Facebook.html
  - Undirected social network graph of Facebook friendships (4,039 nodes, 88,234 edges)
  - Download the `facebook_combined.txt.gz` file from the link above, extract the `facebook_combined.txt` file and place it in a `data/` directory located in the same directory as the main Python notebook.

- **Email-Eu-Core Network:** https://snap.stanford.edu/data/email-Eu-core.html
  - Directed network of email communications between members of a large European research institution (1,005 nodes, 25,571 directed edges)
  - Ground-truth department labels (42 departments) enable node classification evaluation
  - Download the `email-Eu-core.txt.gz` and `email-Eu-core-department-labels.txt.gz` files from the link above, extract them and place in a `data/` directory.


### 2. Libraries and Installation

Install all required Python libraries with:

```
pip install -r requirements.txt
```

### 3. Usage

Open the notebooks with Jupyter. Cells are left open with all outputs to facilitate review. They can be run as seen fit.

### 4. Structure and Steps

#### Part 1  — Community Detection and Centrality Measures
- **Preliminary analysis:** summary statistics, centrality measures (degree, betweenness, closeness, eigenvector, PageRank), and visualizations for both graphs.
- **Community Detection:** Louvain, Label Propagation, Walktrap, Spectral Clustering, and Node2Vec + K-Means on both datasets. Comparison via modularity, NMI, and ARI (where ground-truth labels are available).
- **Evaluation:** quantitative comparison of all methods with discussion of strengths and limitations.

#### Part 2 — KG Embeddings, GNN and Shallow Embeddings
- **KG Embeddings:** TransE, TransH, TransR, DistMult, ComplEx, RotatE for multi-relational link and relation prediction (MRR, Hits@K).
- **GNN Models:** GCN, GraphSAGE, GAT for binary link prediction (AUC-ROC, AP); R-GCN with multi-label BCE for relation-aware prediction.
- **Shallow Embeddings:** Laplacian Eigenmaps, Node2Vec, DeepWalk for structural baselines.
- **Evaluation:** quantitative comparison of all methods with discussion of strengths and limitations.
