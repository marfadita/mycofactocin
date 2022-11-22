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
1. Data preparation
  * PSI-BLAST with known MftB(RRE protein) sequences as queries
  * Manual deletion of false positive results
  * mmseq2 clusterisation
2. Identify biosynthetic gene clusters
  * RODEO with MftB clusters
  * Flags2 analysis
3. Results visualization
  * Cytoscape
  * RAxML tree

## Results
![alt text](https://github.com/marfadita/mycofactocin/blob/main/mftbtree_mftb_with_pqqD/RAxML_tree_mftb_id60_pqqD.svg?raw=true)
*MftB tree with rooting through the outgroup PqqD*
