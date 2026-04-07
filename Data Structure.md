# Node Properties

## Gene Nodes
- **Gene name** – Standard symbol used to refer to the gene (e.g., CFTR)
- **Gene stable ID** – Unique Ensembl identifier for the gene
- **Gene type** – Classification of the gene (e.g., protein-coding, non-coding)
- **GeneID** – Internal or dataset-specific gene identifier
- **HGNC ID** – Official identifier assigned by the HUGO Gene Nomenclature Committee
- **NCBI ID** – Identifier for the gene in the NCBI database
- **Protein stable ID** – Ensembl IDs for proteins encoded by this gene
- **Transcript stable ID** – Ensembl IDs for transcripts produced from this gene

## Protein Nodes
- **Ensembl_PRO** – Ensembl protein identifiers corresponding to different isoforms of the protein
- **MIM** – OMIM (Online Mendelian Inheritance in Man) identifiers linked to diseases or phenotypes associated with the protein
- **ProteinID** – Primary protein identifier (often UniProt accession-based or dataset-specific ID)
- **RefSeq** – NCBI Reference Sequence identifier for the protein
- **UniProtKB-ID** – Standard UniProt entry name for the protein (protein-centric functional database ID)

# Edge Properties

## Gene-Gene Coexpression Edges
There are 108 different total coexpression edge types. 54 tissues (derived from GTEx). 2 directions per tissue (positive / negative correlation). Total edge labels = 108.

Each coexpression edge has a correlation value **cor_value** associated with it.

## Protein-Protein Interaction Edges
There are 3 different total interaction edge types:
- **interacts_1** – interaction supported by only 1 database
- **interacts_2** – interaction supported by 2 databases
- **interacts_3** – interaction supported by all databases

Each interaction edge has three values associated:
- **iid_exists** – 1 if supported by IID, 0 if not
- **intact_score** – confidence score provided by IntAct database
- **string_score** – confidence score provided by STRING database

## Gene-Protein Relation Edges
There is 1 total relation edge type: **gene-to-protein**

Each **gene-to-protein** edge contains:
- **HGNC ID** – gene identifier
- **Protein stable ID** – protein identifier
