### Find CFTR Protein, find 10 neighbors
```
MATCH(p:Protein {ProteinID:"P13569"})
MATCH(p)-[]-(n2:Protein)
RETURN p, n2
LIMIT 10
```
<img width="1391" height="958" alt="Screenshot 2026-04-07 at 1 44 07 AM" src="https://github.com/user-attachments/assets/2c2e8dc5-015c-481d-979a-571f393bf7bb" />

### Find CFTR Gene, find 10 neighbors
```
MATCH(g:Gene {`Gene name`:"CFTR"})
MATCH(g)-[]-(n1:Gene)
RETURN g, n1
LIMIT 10
```
<img width="1391" height="958" alt="Screenshot 2026-04-07 at 1 43 00 AM" src="https://github.com/user-attachments/assets/39aa9a74-3807-417f-9382-75bdfb7686af" />

### Find CFTR Gene, CFTR Protein
```
MATCH(g:Gene {`Gene name`:"CFTR"})
MATCH(p:Protein {ProteinID:"P13569"})
RETURN g, p
```
<img width="1391" height="958" alt="Screenshot 2026-04-07 at 1 44 45 AM" src="https://github.com/user-attachments/assets/84a9de79-d610-43ae-ae12-00ba52ab87c5" />
