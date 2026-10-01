
# Results

This folder contains the main visual outputs of the nutrigenomics
co-authorship network analysis.

The visualizations were generated from the author collaboration network
and its corresponding network analyses using Python and Gephi.

The results are organized into:

- Author centrality analysis
- Bipartite network analysis
- K-core analysis
- Community structure analysis

---

## 1. Top Authors Network

The overall co-authorship network was visualized to examine the position
of highly connected researchers.

The visualization highlights prominent authors within the network and
their collaboration relationships.

![Top Authors Network](top-authors-network.png)

The analysis identified Ordovas JM, Zhang X, and Li H among the authors
with the highest degree centrality.

---

## 2. Betweenness Centrality

Betweenness centrality identifies researchers that frequently occur on
shortest paths between other researchers.

Such nodes can occupy intermediary or bridge positions within the
collaboration network.

![Betweenness Centrality](betweenness_centrality.png)

The analysis identified Ordovas JM, Chan AT, and Yan Y among the authors
with the highest betweenness centrality.

---

## 3. PageRank Centrality

PageRank evaluates the structural importance of researchers by taking
the importance of their connected researchers into account.

![PageRank Centrality](pagerank-network.png)

The highest PageRank values in the study were reported for Wang Y,
Ordovas JM, Zhang X, Chen Y, and Li Z.

---

## 4. Bipartite Author–Publication Network

The bipartite network represents two types of nodes:

- Authors
- PubMed publications

Edges connect authors to the publications on which they collaborated.

![Bipartite Network](bipartite-network.png)

This representation provides the basis for understanding the relationship
between researchers and scientific publications before projecting the
network into an author–author collaboration network.

---

## 5. K-Core Analysis

A k-core filter with:

`k = 5`

was applied to focus on the more densely connected core of the network.

The filtering process removes nodes with fewer than five relevant
connections and produces a more focused representation of the core
collaborative structure.

![K-Core Network](kcore-network.png)

---

## 6. Research Communities

Community detection was applied to identify groups of researchers with
stronger internal collaboration patterns.

The overall network had:

- Modularity: 0.960
- Number of communities: 424

The largest community contained 276 authors, representing 5.63% of the
network.

The second-largest community contained 187 authors, representing 3.82%
of the network.

### Community Network

![Research Communities](research-communities-image1.png)

The visualization shows the major communities using different colors
and network structures.

### Community Size / Major Subnetworks

![Research Community Sizes](research-communities-image2.png)

The second visualization provides a complementary view of the major
subnetworks and their relative sizes.

---

## 7. Network-Level Findings

The final co-authorship network contained:

| Metric | Value |
|---|---:|
| Authors | 4,901 |
| Average authors per paper | 10.615 |
| Density | 0.002 |
| Average clustering coefficient | 0.951 |
| Triangles | 114,890 |
| Diameter | 18 |
| Average path length | ~6.2 |
| Modularity | 0.960 |
| Communities | 424 |

These metrics describe different aspects of the network.

The low density indicates that only a small fraction of all possible
author-to-author relationships are present.

At the same time, the high clustering coefficient indicates strong
local collaboration patterns among groups of researchers.

The high modularity indicates a strongly community-structured network,
with researchers tending to collaborate more frequently within their
own communities.

---

## 8. Interpretation

Taken together, the visualizations show that the nutrigenomics research
community is not organized as a uniformly connected network.

Instead, the network contains:

- Highly connected researchers
- Researchers occupying intermediary positions
- A densely connected core
- Distinct research communities
- Different structural roles captured by different centrality measures

This demonstrates the value of combining multiple Social Network
Analysis techniques rather than relying on a single network metric.
