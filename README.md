# Mycofactocin-like clusters analysis 
## Authors:
* Marfa Zakirova
* Dmitrii Bikmetov
## Introduction 
Ribosomally synthesized and posttranslationally modified peptide (RiPP) pathways produce a diverse array of natural products. A subset of these pathways depends on radical S-adenosylmethionine proteins to modify the RiPP-produced peptide. Mycofactocin biosynthesis is one example of an S-adenosylmethionine protein-dependent RiPP pathway.
Mycofactocin has been proposed to be a new member of the peptide-derived redox cofactor family that consists of members such as pyrroloquinoline quinone. The mycofactocin biosynthetic pathway is composed of six genes, mftABCDEF, beginning with the peptide MftA. MftA is 30 – 60 AA in length and contains a conserved C-terminal sequence (-IDGXCGVY).
## Aim
The aim is to find unusual functional mycofactocin-like clusters by analyzing the data and prepare the data for further gene research.
## Workflow
* Data preparation
  * PSI-BLAST with known MftB(RRE protein) sequence as query
  * Manual deletion of false positive results
  * mmseqs2 clusterisation
* Identify biosynthetic gene clusters
  * RODEO
  * Flags2 analysis
  * Calculating the frequency of pairwise occurrence of domains in clusters
  * MEME analysis of conserved positions in precursor (MftA)
* Results visualization
  * Cytoscape
  * RAxML tree

## Results
* Tree
![alt text](https://github.com/marfadita/mycofactocin/blob/main/mftbtree_mftb_with_pqqD/RAxML_mftb_tree_with_pqqD_id60.svg?raw=true)
MftB tree with rooting through the outgroup PqqD. The colors show the presence of certain genes in the cluster, the comments are signed by the organism of origin
![image](https://user-images.githubusercontent.com/98456969/203294392-469475ef-b9e6-45b2-8669-71683834369e.png)

* Cytoscape
The network is built by issuing EFI EST by fasta of the MftB file. Firstly, found the node closest to the original sequence in which the search began
```
blastp -query /home/marfa/Desktop/lab/mycofactocin/mftb/mftb.fa -db /home/marfa/Desktop/lab/mycofactocin/mftb/cluster_res/mftb_seq_id_for_blast_db -out /home/marfa/Desktop/lab/mycofactocin/mftb/cluster_res/mftb_seq_id_for_blast_res.tbl -outfmt 
```
```
blastp -query /home/marfa/Desktop/lab/mycofactocin/mftb/mftb.fa -db /home/marfa/Desktop/lab/mycofactocin/mftb/cluster_res/mftb_seq_id_for_blast_db -out /home/marfa/Desktop/lab/mycofactocin/mftb/cluster_res/mftb_seq_id_for_blast_res.tbl -outfmt 6
```

Discrete coloring:
![image](https://user-images.githubusercontent.com/98456969/203299777-cb63b35d-53ac-4e87-ba5a-2db067e4a6f7.png)
![image](https://user-images.githubusercontent.com/98456969/203300573-8d4bfae7-8107-49b9-9002-2fac750e55c2.png)

- 1 == min cluster: MftA, MftB, MftC
- 2 == MftABC + MftR
- 3 == MftABC + MftF
- 5 == MftABCRF
- 8 == MftABC + MftD
- 9 == MftABC + Rv0697
- 10 == MftABCD, Rv0697
- 11 == MftABCDR
- 12 == MftABCDF
- 14 == MftABCR, Rv0697
- 15 == MftABCF, Rv0697
- 17 == MftABCDR, Rv0697
- 18 == MftABCDF, Rv0697
- 21 == MftABCDFR, Rv0697
- 24 == MftABCDFR
- 25 == MftABCRF, Rv0697
- 888 == closest node

## Conclusions
According to the data obtained, mycofactocin clusters are very similar to each other. Prepared data  should be further investigated.

## Literature
* Kostenko A, Lien Y, Mendauletova A, Ngendahimana T, Novitskiy IM, Eaton SS, Latham JA. Identification of a poly-cyclopropylglycine-containing peptide via bioinformatic mapping of radical S-adenosylmethionine enzymes. J Biol Chem. 2022 May;298(5):101881. doi: 10.1016/j.jbc.2022.101881. Epub 2022 Mar 31. PMID: 35367210; PMCID: PMC9062424
* Haft DH. Bioinformatic evidence for a widely distributed, ribosomally produced electron carrier precursor, its maturation proteins, and its nicotinoprotein redox partners. BMC Genomics. 2011 Jan 11;12:21. doi: 10.1186/1471-2164-12-21. PMID: 21223593; PMCID: PMC3023750
* Ayikpoe RS, Latham JA. MftD Catalyzes the Formation of a Biologically Active Redox Center in the Biosynthesis of the Ribosomally Synthesized and Post-translationally Modified Redox Cofactor Mycofactocin. J Am Chem Soc. 2019 Aug 28;141(34):13582-13591. doi: 10.1021/jacs.9b06102. Epub 2019 Aug 15. PMID: 31381312; PMCID: PMC6716157.
