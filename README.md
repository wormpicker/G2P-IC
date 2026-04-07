# G2P-IC

## Construction:
The G2P-IC knowledge graph was constructed in Neo4j, a graph database environment. PPI data were obtained
from STRING (v12), IntAct (release 250) and IID (v2025-05). COEXP data was obtained from GTEx by calculating
pairwise Spearman correlation scores and selecting the top and bottom 0.1%. Node annotations were derived from
UniProt (proteins), HGNC (genes), and BioMart (genes). Finally, the gene-protein mapping was extracted from
BioMart (Fig 1).

The constructed knowledge graph contained 205,303 protein nodes with 43,679 of them categorized as
UniProtKB/Swiss-Prot, the manually reviewed section of UniProt proteins, and 89,273 gene nodes with 20,351 of
them recognized as protein coding as annotated by BioMart (Fig 2). These nodes are connected by protein-protein
interaction edges and gene-gene coexpression edges across 54 GTEx tissues.

<img width="793" height="662" alt="Screenshot 2026-04-07 at 12 26 28 AM" src="https://github.com/user-attachments/assets/493bf35f-365d-4cc4-b59f-00a4ba0b5ef6" />
