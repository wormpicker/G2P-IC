# G2P-IC

## Introduction
Collectively, rare diseases affect millions of people worldwide, yet their pathophysiological mechanisms remain
largely obscure. Traditional genomics studies often lack the statistical power to robustly identify candidate genes
due to limited patient cohort sizes. Knowledge graphs have emerged as a powerful analytical tool in advancing
biomedical research. We aim to approach the problem through integrating protein-protein interaction (PPI) and
gene-gene coexpression (COEXP) data into a knowledge graph. Under the assumption that protein-protein and
gene-gene correlations have strong connections to functionality, the dual layer nature of the Gene-2-Protein
Interaction Coexpression (G2P-IC) knowledge graph assists in the discovery of novel disease gene candidates with
high specificity.

## Installing G2P-IC

1. Install Neo4j Desktop. Download Neo4j Desktop here:[Neo4j Download Page](https://neo4j.com/download/)
2. Create a new project
   <img width="1391" height="958" alt="Screenshot 2026-04-07 at 12 39 13 AM" src="https://github.com/user-attachments/assets/74d40128-675a-406c-9812-ccd3f7e8d853" />
4. Add the dump file to the new project<img width="1391" height="958" alt="Screenshot 2026-04-07 at 12 44 09 AM" src="https://github.com/user-attachments/assets/19103a24-f6ad-4be3-b694-aef80723851f" />
5. Select "Create new database from dump"<img width="1391" height="958" alt="Screenshot 2026-04-07 at 12 45 58 AM" src="https://github.com/user-attachments/assets/e1496e17-fefe-4367-b83e-daa34cc78099" />
6. Enter a database name and password. Click "Create".<img width="1391" height="958" alt="Screenshot 2026-04-07 at 12 47 50 AM" src="https://github.com/user-attachments/assets/6d055c34-5184-4fde-9a1e-6b16897b9e40" />

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
