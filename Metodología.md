# Metodología
### 1. Identificación de la lacasa de _M. produnfimaris_
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

### 2. Alineamiento de la lacasa de _M. profundimaris_ y similares
- Realizar un blast para buscar las secuencias más similares de todas las disponibles en la base de datos
  
![image](https://github.com/user-attachments/assets/7009c6b4-efb2-47a6-a6fa-149d39429015)

- Se descargan 15 secuencias brindadas por el NCBI en el blastp

```
#!/usr/local/bin/
# Busca la secuencia de proteínas en la base de datos de la ncbi

from Bio import Entrez
from Bio import SeqIO

Entrez.email = "carolina.gamez@eia.edu.co"

#Secuencia oxidasa multicobre de Zooshikella harenae
with Entrez.efetch(
    db="protein", rettype="fasta", retmode="text", id="WP_230409021.1") as handle:
    seq_record = SeqIO.read(handle, "fasta")

SeqIO.write(seq_record, "zharenae_prot.fa", "fasta")

#Secuencia oxidasa multicobre de Salinivibrio kushneri
with Entrez.efetch(
    db="protein", rettype="fasta", retmode="text", id="WP_077605313.1") as handle:
    seq_record = SeqIO.read(handle, "fasta")

SeqIO.write(seq_record, "skushneri_prot.fa", "fasta")

#Secuencia oxidasa multicobre de Gammaproteobacteria bacterium
with Entrez.efetch(
    db="protein", rettype="fasta", retmode="text", id="HBO92458.1") as handle:
    seq_record = SeqIO.read(handle, "fasta")

SeqIO.write(seq_record, "gbacterium_prot.fa", "fasta")

#Secuencia oxidasa multicobre de Pseudomonadales bacterium
with Entrez.efetch(
    db="protein", rettype="fasta", retmode="text", id="MAA61049.1") as handle:
    seq_record = SeqIO.read(handle, "fasta")

SeqIO.write(seq_record, "psebacterium_prot.fa", "fasta")

#Secuencia oxidasa multicobre de Salinivibrio sharmensis
with Entrez.efetch(
    db="protein", rettype="fasta", retmode="text", id="WP_077771786.1") as handle:
    seq_record = SeqIO.read(handle, "fasta")

SeqIO.write(seq_record, "ssharmensis_prot.fa", "fasta")

#Secuencia oxidasa multicobre de Salinivibrio kushneri
with Entrez.efetch(
    db="protein", rettype="fasta", retmode="text", id="WP_269580392.1") as handle:
    seq_record = SeqIO.read(handle, "fasta")

SeqIO.write(seq_record, "skushneri_prot.fa", "fasta")

#Secuencia oxidasa multicobre de Zooshikella ganghwensis
with Entrez.efetch(
    db="protein", rettype="fasta", retmode="text", id="WP_094786916.1") as handle:
    seq_record = SeqIO.read(handle, "fasta")

SeqIO.write(seq_record, "zganghwensis_prot.fa", "fasta")

#Secuencia oxidasa multicobre de Zooshikella marina
with Entrez.efetch(
    db="protein", rettype="fasta", retmode="text", id="MBU2706886.1") as handle:
    seq_record = SeqIO.read(handle, "fasta")

SeqIO.write(seq_record, "zmarina_prot.fa", "fasta")

#Secuencia oxidasa multicobre de Spartinivicinus ruber
with Entrez.efetch(
    db="protein", rettype="fasta", retmode="text", id="WP_163836319.1") as handle:
    seq_record = SeqIO.read(handle, "fasta")

SeqIO.write(seq_record, "sruber_prot.fa", "fasta")

#Secuencia oxidasa multicobre de Spartinivicinus poritis
with Entrez.efetch(
    db="protein", rettype="fasta", retmode="text", id="WP_274690405.1") as handle:
    seq_record = SeqIO.read(handle, "fasta")

SeqIO.write(seq_record, "sporitis_prot.fa", "fasta")

#Secuencia oxidasa multicobre de Marinobacterium ramblicola
with Entrez.efetch(
    db="protein", rettype="fasta", retmode="text", id="WP_217415637.1") as handle:
    seq_record = SeqIO.read(handle, "fasta")

SeqIO.write(seq_record, "mramblicola_prot.fa", "fasta")

#Secuencia oxidasa multicobre de Marinobacter xestospongiae
with Entrez.efetch(
    db="protein", rettype="fasta", retmode="text", id="WP_316972399.1") as handle:
    seq_record = SeqIO.read(handle, "fasta")

SeqIO.write(seq_record, "mxestospongiae_prot.fa", "fasta")

#Secuencia oxidasa multicobre de Oceanospirillaceae bacterium
with Entrez.efetch(
    db="protein", rettype="fasta", retmode="text", id="NVK72961.1") as handle:
    seq_record = SeqIO.read(handle, "fasta")

SeqIO.write(seq_record, "ocebacterium_prot.fa", "fasta")

#Secuencia oxidasa multicobre de Marinomonas colpomeniae
with Entrez.efetch(
    db="protein", rettype="fasta", retmode="text", id="WP_235963151.1") as handle:
    seq_record = SeqIO.read(handle, "fasta")

SeqIO.write(seq_record, "mcolpomeniae_prot.fa", "fasta")

#Secuencia oxidasa multicobre de Marinomonas primoryensis
with Entrez.efetch(
    db="protein", rettype="fasta", retmode="text", id="WP_244959793.1") as handle:
    seq_record = SeqIO.read(handle, "fasta")

SeqIO.write(seq_record, "mprimoryensis_prot.fa", "fasta")
```
- Agrupar las secuencias en un archivo de texto y realizar un alineamiento con clustal
```
clustalw -infile=CuOxidase_seqs.txt -type=protein
```
- Observar el alineamiento y analizar
```
clustalx CuOxidase_seqs.aln
```
