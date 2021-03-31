## Readme file for data analysis for publicly available used for the mitochondrial gene project

Publicly available placental gene expression datasets (Microarrays and RNA-sequencing) datasets were used to determine if specific placental transcripts that were related to mitochondrial function were differentially expressed in healthy and pathologies pregnancies.

**Table 1**: Placental gene expression datasets used for data mining

| Dataset          | Samples (N)                                                  | RNA-Sequencing or Microarray |
| ---------------- | ------------------------------------------------------------ | ---------------------------- |
| GSE28551 [1]     | Placental tissue from first trimester and third trimester (36) | Microarray                   |
| GSE18809 [2]     | Placental tissue from term and preterm birth (10)            | Microarray                   |
| PRJNA448842  [3] | Chorioamniotic membranes of severe preterm birth (28)        | RNA-sequencing               |
| PRJNA485683 [4]  | Placental tissue from idiopathic spontaneous preterm birth (17) | RNA-sequencing               |
| PRJNA472249 [5]  | Placental tissue from controls and intrauterine growth restriction (39) | RNA-sequencing               |
| PRJNA358255 [6]  | Placental tissue from appropriate for gestational age (AGA) and small for gestational (SGA) infants (145) | RNA-sequencing               |

[1] Sitras V, Fenton C, Paulssen R, Vårtun Å, Acharya G. Differences in Gene Expression between First and Third Trimester Human Placenta: A Microarray Study. PLoS One [Internet]. 2012 Mar 19 [cited 2021 Mar 31];7(3). Available from: https://www.ncbi.nlm.nih.gov/pmc/articles/PMC3307733/

[2] Chim SSC, Lee WS, Ting YH, Chan OK, Lee SWY, Leung TY. Systematic identification of spontaneous preterm birth-associated RNA transcripts in maternal plasma. PLoS One. 2012;7(4):e34328. 

[3] Pereyra S, Sosa C, Bertoni B, Sapiro R. Transcriptomic analysis of fetal membranes reveals pathways involved in preterm birth. BMC Med Genomics [Internet]. 2019 Apr 1 [cited 2021 Mar 31];12. Available from: https://www.ncbi.nlm.nih.gov/pmc/articles/PMC6444860/

[4] Brockway HM, Kallapur SG, Buhimschi IA, Buhimschi CS, Ackerman WE, Muglia LJ, et al. Unique transcriptomic landscapes identified in idiopathic spontaneous and infection related preterm births compared to normal term births. PLoS One. 2019;14(11):e0225062. 

[5] Awamleh Z, Gloor GB, Han VKM. Placental microRNAs in pregnancies with early onset intrauterine growth restriction and preeclampsia: potential impact on gene expression and pathophysiology. BMC Med Genomics. 2019 Dec;12(1):91. 

[6] Deyssenroth MA, Peng S, Hao K, Lambertini L, Marsit CJ, Chen J. Whole-transcriptome analysis delineates the human placenta gene network and its associations with fetal growth. BMC Genomics. 2017 Jul 10;18(1):520. 



*For RNA-sequencing analysis the following pre-processing tasks were completed. All scripts can be found in the RNA-sequencing pre-processing folder.*

1. FastQC to check transcript quality
2. Trimmomatic to trim away low quality and erroneous sequence 
3. Mapping to the human genome using Salmon
4. Quantification of transcript counts using Trinity

*For microarray analysis, the preprocessed data was downloaded from NCBI using the GEOquery function below.*

gds <- getGEO("GSE142974", GSEMatrix = TRUE)
GSE142974 <- gds$GSE142974_series_matrix.txt.gz
GSE142974_clinical_metadata <- pData(GSE14771)
write.csv(GSE142974_clinical_metadata , file="GSE14771_clinical_metadata.csv")
save(GSE14771, file= "GSE14771_eset.RData")



**Differential gene expression analysis**

For both datasets, differential gene expression analysis was completed with limma and the scripts for this analysis can be found in the differential_gene_expression_analysis subfolder. 



 

