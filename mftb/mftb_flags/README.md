We decided to check how Flags works with existing clusters, as an alternative to the pipeline with mmseqs2 and rodeo

env == eFlaGs2
The cases of the absence of MftA are not considered separately, since the reading frames of precursor peptides are often mistakenly not annotated, because they are short. With a detailed analysis of the obtained frames, we see that MftCs are often not annotated because they fall on the edge of the contigue



![image](https://user-images.githubusercontent.com/98456969/203296361-9b5683df-0ca4-46c9-bd82-98ba79820a8a.png)
A fragment of the results. Detailed description of the contents in the table mftb_g8_flankgene_desc.csv. The minimum cluster of an effective cofactor contains at least MftABCDE.
1 == MftF
2 == MftR (TetR)
3 == MftA (mycofactocin)
4 == MftC (mycofact_rSAM)
6 == MftD (actino_HemFlav)
7 == MftE (mycofact_creat)
