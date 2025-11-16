# Community Detection Analysis Project

## Overview

This project analyzes and compares community structures in at least two different graph datasets using two different community detection algorithms. The analysis includes preliminary statistics, centrality measures, quality evaluation metrics, and clear visualizations. All work is reproducible in a single Python notebook or script.

## Contents

- `Patricio_Olajuyigbe.ipynb` — Main analysis notebook with all results, code, and instructions
- Requirements file (`requirements.txt`)
- Data sources
  
## Instructions

### 1. Data Sources

- **SNAP Facebook Social Network Graph:** https://snap.stanford.edu/data/ego-Facebook.html
  - This is a Facebook Social Network graph extracted from SNAP
  - Download the facebook_combined.txt.gz file from the link above, extract the facebook_combined.txt file and place it in a data/ directory located in the same directory as the main Python notebook.
- **Email-Eu-Core Network:** https://snap.stanford.edu/data/email-Eu-core.html
  - This is a directed network of email communications between members of a large European research institution
  - Nodes represent individual members (1,005 nodes) and edges represent email communications (25,571 directed edges)
  - Download the email-Eu-core.txt.gz file from the link above, extract the email-Eu-core.txt file and place it in a data/ directory located in the same directory as the main Python notebook.

### 2. Libraries and Installation

Install all required Python libraries with:

pip install -r requirements.txt

### 3. Usage

Open the notebook with Jupyter. Cells are left open with all outputs to facilitate review. It can be run as seen fit.

### 4. Structure and Steps

- **Preliminary analysis:** summary statistics, centrality measures (e.g. degree, betweenness, closeness, eigenvector, PageRank), and visualizations for both graphs.
- **Community Detection:** application of different algorithms on both datasets. Visual and quantitative comparison of community membership, number of communities, modularity, and community size distributions.
- **Evaluation:** use of metrics such as modularity to interpret the results.
- **Discussion:** insights and interpretation referring back to centrality statistics and network structure.