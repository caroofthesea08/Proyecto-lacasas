# Metodología
- Descargar la secuencia y determinar sus principales características

```
#!/usr/local/bin/
# Busca la secuencia de proteínas en la base de datos de la ncbi

from Bio import Entrez
from Bio import SeqIO

Entrez.email = "carolina.gamez@eia.edu.co"

with Entrez.efetch(
    db="protein", rettype="fasta", retmode="text", id="WP_024024624.1") as handle:
    seq_record = SeqIO.read(handle, "fasta")

print("La longitud de la secuencia es de", len(seq_record.seq), "aminoácidos")
print("La secuencia", seq_record.description, " es: ")
print(seq_record.seq)
SeqIO.write(seq_record, "mprofundimaris_prot.fa", "fasta")
```

- Entrar a https://www.ebi.ac.uk/interpro/search/sequence/ y pegar en la casilla la secuencia de aminoácidos de la proteína para determinar si los dominios de esta corresponden con el verdadero funcionamiento de la proteína

![image](https://github.com/user-attachments/assets/e00a8fa7-1581-4007-a7c2-a902e55cfa5e)

