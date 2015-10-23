Carla Uranga

***Crassostria gigas* Dsx gene search**

Since the Dsx protein was shown to be expressed and potentially involved in hormone regulation as shown in class, this gene was chosen for searches. First, "Dsx" was entered in NCBI and a sequence for Dsx from *Crassostrea gigas* was obtained. Both the protein and mRNA sequences were downloaded and searched against the Geoduck proteome and transcriptome data bases we created in class. The nucleotide sequence query using the program jupyter only yielded results using the tblastx search, and the following sequences were obtained:
![](http://i.imgur.com/P8F49nO.png)

However, a grep of comp139026_c0_seq4 (the highest scoring hit) yielded a hit for the terrestrial rat parasite *Strongyloides ratti*, and all E values were generally poor (values too high). Therefore, a protein query was attempted.

When searched against the entire Uniprot database, the Dsx protein was indeed identified in a variety of species, with highest similarity to *Drosophila*. 

![](http://i.imgur.com/4jLZ3XT.png)

The protein query using jupyter against the Geoduck transcriptome yielded the following nucleotide sequences:

![](http://i.imgur.com/Fbv9OtH.png)

The top sequence (comp137832_c0_seq2) was retrieved from the entire Geoduck transcriptome FASTA file.

![](http://i.imgur.com/yUH2kw9.jpg)

This sequence was then searched in NCBI online (a BLAST search), which yielded the following top-scoring hit, homologous to a 2'-deoxynucleoside 5'-phosphate N-hydrolase from the acorn worm, *Saccoglossus kowalevskii*, also a sea-dwelling creature.
![](http://i.imgur.com/3jINQhv.png)

This is a picture of an acorn worm (from http://scitechdaily.com/similarities-between-acorn-worm-and-vertebrate-brain/  Steve Tung, Stanford University):

![](http://i.imgur.com/LTmtQrW.jpg)

It turns out this protein may be a 2'-deoxynucleoside 5'-phosphate N-hydrolase. The human version is known to be able to hydrolize DNA bases (Uniprot) from the phosphate DNA backbone. However, it may also hydrolize RNA bases in the same manner. Whether this occurs in Geoduck remains to be determined.
![](http://i.imgur.com/GqQm4mz.png)

The other protein nucleotide hits were also searched. The sequence grepped from comp109566_c0_seq1 was searched via BLAST, and the top scoring hit homologous to  *Lingula anatina* 60S ribosomal protein L18a-like (LOC106152843). *Lingula anatina* is also a sea-dwelling creature

The sequence comp111266_c0_seq was also searched via BLAST, however, the top hit was from a tomato, which of course is impossible in this case.

Therefore, the protein search of *C. gigas* with the transcriptome data showed homology to a protein from Geoduck (somewhat homologous to the Dsx protein) is more likely to have a 2' -deoxynucleoside 5'-phosphate N-hydrolase activity, which might have interesting biochemical repercussions for the homolog in Geoduck that might include a role in sex differentiation.

**NEW SEARCH**
From the annotated Geoduck transcriptome file obtained from SQL, a grep for the word "hormone" was performed. This yielded many sequences, especially from the  NCOR1 gene from mouse. The human NCOR1 was downloaded from NCBI.
A Blast of a human hormone nucleotide sequence (gi|298919178|ref|NM_001190438.1| Homo sapiens nuclear receptor corepressor 1 (NCOR1), transcript variant 2, mRNA)
using Jupyter, yielded 69 hits, and the top three hits were chosen because of the low E-values.

gi|298919178|ref|NM_001190438.1|	comp130242_c0_seq3	67.34	793	230	15	425	1207	844	71	7e-056	221
gi|298919178|ref|NM_001190438.1|	comp130242_c0_seq3	80.95	42	2	1	343	384	929	894	0.14	41.0
gi|298919178|ref|NM_001190438.1|	comp130242_c0_seq1	69.89	372	94	10	425	787	521	159	7e-031	138

The sequences were retrieved from the Geoduck transcriptome, and for brevity's sake, this is the sequence of the Geoduck top hit:
>comp130242_c0_seq1 len=1351 path=[93583393:0-36 93546237:37-178 93585495:179-682 93556409:683-1020 93561733:1021-1131 93563472:1132-1350]
CGCTAAAAGCTACATGTAATATGAAGATATCACCTTACCTCTTGTTCATTAAGTCCGTCC
ATTATTTGTTCAATTTCTGCCTCACTCCTAGCATACTGTGCACTTATACCGGCTCTGGTA
CCAGACCTGCTCAGTTTGTCATCTCTGGCCTTCTTCAGTTCTGGAAATACCTTTTCAAAG
TAATCTCTGTGTTTTGCTTCTTTAGCCTTTCGTTTTGGATTATTTTCCCACTTTTCCACT
TTCTTGACCCAGGCCTGCATCAACTGATCGTACCTCTGTGTCAAATACTTCTCCCTGATC
TTCCTTGCCTGATGTCGCTTCTTGAAATGCAAAATCAACTTCGGTTTGAAGAGAACAAAA
TTTTTCTTGTTTTCATGGTAGATGGGTGCATCTGATGGCTGGTTGTACAGGGGCAGATCA
ACTTTGCGTCCCATCTTGGAAAACTTGTTATGTGATTCTTGGGCTTTTTTCCGGTTCTCG
GCATATATAATCTGCGCAATACTCTGGTGTTTCACATCCACCGTCGTGTCGGGAGTGTCC
TCCGTCTCAACCTCGTCTTTGTGTTTATTGGCTGCCTCCTCTTGTTGCTGTTTCTTTTTC
AGTTTATTCTGTATCTGGGTCTCTACCATAACAATCTCTCTGTCGATCTTTCCAATGTTC
TGAAGCAGGTCGTCCTTGATCTTCTGTACTTTCAACGTCTCCTCCGGGGGCAGGGTCGGA
GATATGGCCTCAACCTGGGGGTTGTAGGCAGGCTCCCGCTTTGGTTCAGACTGGCTCACA
TCAATTCTCAAGGGCTGAGCCAGATCAGGTCGATCCATTGCCAAACGTGGTCGTTTAGGA
ACCTGGGGACCTGGATCTGGGGCAGCACTGATAGTAGGCTGAGGGGCTCCTTGAAGGTTA
CCCATGTTGTCTTGTCGGAAATGTTGCCCATATGCAGCTGACAGGTCCGGCCTGTATCTT
GATCTATCTACGCCGCCCTGCGTGTGACTTCCATAGTCAAGAAGTGTGGGTCGTCTCTGT
TTGTATGGATCCGCATCTCGACTGGAAGTGGCAGCTACACGCTCACGTGTAAACTGTTCC
CTGGCATGCTGCTCTTGCACTTGATGCTGTGGCGGTGGTTGAAACGGATCTCTGTAAATA
CTGCCATAATTTCCTGCTGCTACTGCAGCCGCAGCCATAAACCTGGCATCCTGGTAATAC
GCAGGGCCCGCCGACCGCTGGAGATTCTGCATAGTGGAACTGGAAGGACTCTGAGGTCGT
GACCTCTTGTAGGGGGATGCAGCGTCATGCTGTGAACCTCCCTGGCCCCTTTCATTTGGG
GGTCTATTTGCCATAATCTTTGGTTTTGTAC


This entire sequence was re-blasted using the NCBI online database. The top hit was a sequence homologous to *Crassostrea gigas* (Pacific Oyster) nuclear receptor corepressor 1-like (LOC105327345), transcript variant X7, mRNA. According to Yamamoto et al., (2011) this gene modulates muscle mass and oxidative function in mice. However, many other cellular interactions have been identified, such as interactions with the androgen receptor, etc.
