# Dataset

This folder contains the PubMed publication dataset used for the nutrigenomics co-authorship network analysis.

## Data Source

The publication data were collected from PubMed for research related to nutrigenomics and related concepts.

The search covered publications from 2020 to 2024 using the following search strategy:

(nutrigenomics OR nutritional genomics OR gene based diet OR precision nutrition)

combined with the publication date range:

2020–2024

## Dataset Structure

The dataset contains publication-level information including:

- PMID
- Title
- Authors
- First Author
- Journal/Book
- Publication Year
- Create Date
- PMCID
- NIHMS ID
- DOI

The original dataset contains 924 publication records.

During preprocessing, records without author information are removed before constructing the co-authorship network.

## From Publications to a Network

The analysis initially represents the data as a bipartite network:

- Author nodes
- PubMed article (PMID) nodes

An edge connects an author to a publication when the author contributed to that publication.

The bipartite network is subsequently projected into a one-modeauthor–author network, where:

- Nodes represent authors
- Edges represent co-authorship relationships

Two authors are connected when they have co-authored at least one publication.
