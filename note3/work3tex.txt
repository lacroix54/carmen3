## Look at gene

**COXI *M. lusoria***

[http://www.ncbi.nlm.nih.gov/nuccore/AB076924.1](http://www.ncbi.nlm.nih.gov/nuccore/AB076924.1) 

**Fasta save:**
/c/Users/curso18/Desktop/carmen3/data3


Picture from my computer (win)

1. in the same directory picture and file MP-notes
2. write the code folliwing

![some Picture](ostras-perla.jpg)


A look to the fasta file:

*my code:*

,,,,,,,,,,,,,,,,,,,,,,,

    !head ../carmen3/data3/MlusoriaCOXI.fasta

,,,,,,,,,,,,,,,,,,,,,,,,,,,

>gi|18307619|dbj|AB076924.1| Meretrix lusoria mitochondrial COI gene for cytochrome c oxidase subunit I, partial cds
CTGGTTCCTTTAATGTTAACAGCTCCTGACATAGCTTTTCCTCGTTTGAATAATTTAAGTTTCTGATTAT
TAACTAGTTCTTTGTTGCTTTTATTAGGTTCTACTTATGTGGAAGCTGGTTCTGGTACGGGTTGAACTAT
TTATCCTCCTTTATCTAGTTGAAAATATCATTCTGGTGTAAGTGTAGATTATTTAATTTTATCTCTACAT
GTAGGTGGTGCTTCTTCTATTATGTCTGGTATTAACTTTACTACTACAGCTATTTGTATACGTCCAGGAG
TTATAGCTTTAGTTCGAACGCCAATGTTTGTTTGGTGTATTGCTGTGACTGGTTTTTTATTAATTTGTGC
TATACCTGTTTTAGCGGCTGGTTTAACAATACTTTTGACAGATCGTAATTTTAATACAGGGTT


**Create the files:** .phr . pin and .psp 

*my code*

''''''''
    
    !makeblastdb -dbtype prot -in ../big-data/blast/db/uniprot_sprot.fasta \
    -out ../big-data/blast/db/uniprot_d3Mlus

''''''''''


do blastp

*my code*

'''''''''

    !blastp -query ../carmen3/data3/MlusoriaCOXI.fasta -db ../big-data/blast/db/uniprot_sprot
    
'''''''''''''''''
**Results:** 

*****No hits found *****


so went i want to do my blastn i have problem with my route or something like that.

**Blastn**

*my code*

'''''''''
try 1

    !blastn -query ../carmen3/data3/MlusoriaCOXI.fasta -db ../big-data/blast/query/Geoduck-proteome-v2


try 2


    !blastn -query ../carmen3/data3/MlusoriaCOXI.fasta -db ../big-data/blast/query/Geoduck-proteome-v2.fasta \
    -task blastn -outfmt 6 -out ../big-data/blast/out/Mlus_blastn_Geoduck.out


try 3

    !blastn -query ../carmen3/data3/MlusoriaCOXI.fasta -db ../big-data/blast/db/uniprot_sprot


![](blastnMlusProblem.PNG)

*Jupyter mark **error***

''''''''

BLAST Database error: No alias or index file found for nucleotide database [..\big-data\blast\db\uniprot_sprot] in search path [C:\Users\curso18\Desktop\carmen3;;]

''''''''

my mistake

**blastx**

*my code*

    !blastx -query ../carmen3/data3/MlusoriaCOXI.fasta -db ../big-data/blast/db/uniprot_sprot

**out file**

*my code*

    !blastx -query ../carmen3/data3/MlusoriaCOXI.fasta -db ../big-data/blast/db/uniprot_sprot -outfmt 6 -out ../big-data/blast/out/Mlus_blastx_Geoduck.out


