# Social Network Analysis of Nutrigenomics Research

A data-driven co-authorship network analysis of nutrigenomics research using macro- and micro-level Social Network Analysis (SNA).

---

## Overview

Scientific research increasingly depends on collaboration between researchers, institutions, and research communities.

This project analyzes the structure of collaboration in the field of **nutrigenomics** by constructing and analyzing a large-scale co-authorship network from publications indexed in PubMed.

The analysis combines network-level metrics, node-level centrality measures, community analysis, and network visualization to understand how researchers collaborate and how different positions within the network can be identified.

---

## Research Question

The main question addressed by this project is:

> How is the research collaboration network in nutrigenomics structured, and which researchers and communities occupy important positions within the network?

The analysis examines the network from two complementary perspectives:

* **Macro-level:** overall structure and organization of the network
* **Micro-level:** position and importance of individual researchers

---

## Data

Publication data related to nutrigenomics were collected from the **PubMed** database for the period **2020–2024**.

The dataset was used to construct a co-authorship network in which:

* Each unique researcher is represented as a **node**
* A co-authorship relationship is represented as an **edge**
* Researchers who collaborate on publications are connected through the network

The final network contains **4,901 independent authors**.

The average number of authors per paper was reported as **10.615**.

---

## Analytical Workflow

```text
PubMed Publications
        ↓
Data Collection
        ↓
Data Cleaning
        ↓
Co-authorship Network Construction
        ↓
Macro-level Network Analysis
        ↓
Micro-level Centrality Analysis
        ↓
Community Detection
        ↓
Gephi Visualization
        ↓
Interpretation
```

---

## Macro-level Network Analysis

The overall structure of the co-authorship network was analyzed using several network-level metrics.

### Network Density

Density measures the proportion of possible connections that are actually present in the network.

The reported network density was:**0.002**

This indicates that only a small proportion of all possible author-to-author connections are present.

### Clustering Coefficient

The average clustering coefficient was reported as:**0.951**

This indicates a high tendency for researchers' collaborators to also collaborate with one another.

### Network Diameter

The diameter of the main component was reported as:**18**

The average path length was reported as approximately:**6.2**

### Modularity

Community structure was analyzed using modularity.

The reported modularity was:**0.960**

The analysis identified: **424 distinct communities**

This indicates a highly modular collaboration structure in the analyzed network.

---

## Micro-level Network Analysis

To examine the position of individual researchers within the collaboration network, several centrality measures were calculated.

### Degree Centrality

Degree centrality captures the number of direct connections of a researcher within the co-authorship network.

The analysis identified highly connected researchers based on their collaboration relationships.

### Betweenness Centrality

Betweenness centrality identifies researchers that frequently lie on paths connecting other researchers.

This metric can reveal researchers who occupy bridging positions within the collaboration network.

### Katz Centrality

Katz centrality considers both direct and indirect connections and therefore captures influence through multiple levels of the network.

### PageRank

PageRank was used to identify researchers whose network position is supported by connections to other well-connected or influential researchers.

---

## Network Visualization

Network visualization was performed using **Gephi**.

Different layouts and filtering approaches were used to investigate the structure of the network.

### Top Authors

![Top Authors Network](results/figures/top-authors-network.png)

The network visualization highlights highly productive or highly connected researchers within the nutrigenomics collaboration network.

---

### PageRank-based Network

![PageRank Network](results/figures/pagerank-network.png)

This visualization represents the network from the perspective of PageRank centrality.

---

### Bipartite Author–Paper Network

![Bipartite Network](results/figures/bipartite-network.png)

The bipartite representation connects researchers with the publications to which they contributed.

This provides a different view of the underlying collaboration structure.

---

### K-Core Analysis

![K-Core Network](results/figures/kcore-network.png)

A k-core filter with **k = 5** was applied to obtain a more focused representation of the core collaborative structure.

---

## Community Structure

![Research Communities](results/figures/research-communities.png)

The network exhibited a highly modular structure.

The analysis identified **424 communities**, with a modularity coefficient of **0.960**.

The largest community contained **276 authors**, representing approximately **5.63%** of the network, while the second-largest contained **187 authors**, representing approximately **3.82%**.

The community analysis provides a way to examine how researchers are organized into groups with relatively stronger internal collaboration.

---

## Key Findings

The analysis produced several important observations:

* The analyzed publication set contained **4,901 independent authors**.
* The average number of authors per paper was **10.615**.
* The network had relatively low density (**0.002**).
* The average clustering coefficient was high (**0.951**).
* The main component had a diameter of **18**.
* The network exhibited strong community structure with a modularity of **0.960**.
* A total of **424 research communities** were identified.
* Multiple centrality measures were used to examine different aspects of researcher position within the network.

These results demonstrate that a large scientific collaboration network can simultaneously exhibit sparse global connectivity and highly clustered local collaboration.

---

## How to Explore the Project

### Python Analysis

Open:

```text
src/coauthorship_network_analysis.ipynb
```

The notebook contains the data processing, network construction, network metrics, centrality analysis, and analytical workflow.

### Gephi

The Gephi project is located in:

```text
gephi/nutrigenomics_network.gephi
```

It can be opened using Gephi to explore the network interactively.

---

## Reproducibility

The analysis is organized around a Python notebook and a Gephi network project.

The notebook documents the main analytical workflow from data preparation to network analysis.

The Gephi project provides an interactive representation of the resulting network structure.

---

## Publication

This project is associated with the following publication:

Khasha, R., Haghshenas, M., Sarikhani, S., & Saeidi, F. (2025).

**Co-authorship Network Analysis of Nutrigenomics Research Using Micro- and Macro-level Social Network Analysis.**

*Journal of Industrial and Systems Engineering*, e232606.

---

Amirkabir University of Technology
