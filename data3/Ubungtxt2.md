##**Practica Dia 3**




1. **Look at fasta**

Un gen de synechococcus ![](http://cfb.unh.edu/phycokey/Choices/Cyanobacteria/cyano_unicells/SYNECHOCOCCUS/Synechococcus_03_600x450.jpg)

**pANL**

[http://www.ncbi.nlm.nih.gov/nuccore/NC_004073.2?report=fasta&from=42508&to=43308](http://www.ncbi.nlm.nih.gov/nuccore/NC_004073.2?report=fasta&from=42508&to=43308 "Fastagen")

Secuencia guardada en

*/c/Users/curso18/Desktop/carmen3*



> Nombre archivo: pANLsyx.fasta


 
2. **se generaron 3 archivos:** *.phr, .pin y psq

!makeblastdb -dbtype prot -in ../big-data/blast/db/uniprot_sprot.fasta \
-out ../big-data/blast/db/uniprot_d3syx

3. **Hacer un blast de proteinas**
 !blastp -query ../carmen3/data3/pANLsyx.fasta -db ../big-data/blast/db/uniprot_sprot

**Results:**
BLASTP 2.2.31+


Reference: Stephen F. Altschul, Thomas L. Madden, Alejandro A.
Schaffer, Jinghui Zhang, Zheng Zhang, Webb Miller, and David J.
Lipman (1997), "Gapped BLAST and PSI-BLAST: a new generation of
protein database search programs", Nucleic Acids Res. 25:3389-3402.


Reference for composition-based statistics: Alejandro A. Schaffer,
L. Aravind, Thomas L. Madden, Sergei Shavirin, John L. Spouge, Yuri
I. Wolf, Eugene V. Koonin, and Stephen F. Altschul (2001),
"Improving the accuracy of PSI-BLAST protein database searches with
composition-based statistics and other refinements", Nucleic Acids
Res. 29:2994-3005.



Database: ..\..\big-data\blast\db\uniprot_sprot.fasta
           549,646 sequences; 195,983,064 total letters



Query= gi|47060311:42508-43308 Synechococcus elongatus PCC 7942 plasmid
pANL, complete sequence

Length=801


***** No hits found *****



Lambda      K        H        a         alpha
   0.327    0.138    0.575    0.792     4.96 

Gapped
Lambda      K        H        a         alpha    sigma
   0.267   0.0410    0.140     1.90     42.6     43.6 

Effective search space used: 85541175900


  Database: ..\..\big-data\blast\db\uniprot_sprot.fasta
    Posted date:  Oct 21, 2015  12:47 PM
  Number of letters in database: 195,983,064
  Number of sequences in database:  549,646



Matrix: BLOSUM62
Gap Penalties: Existence: 11, Extension: 1
Neighboring words threshold: 11
Window for multiple hits: 40




