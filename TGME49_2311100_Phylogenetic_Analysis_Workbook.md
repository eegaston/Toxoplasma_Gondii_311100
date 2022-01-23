# Analyzing the Phylogenetic Relationships of TGME49_311100

This workbook documents the methodology and programs utilized to examine the phylogenetic relationships of TGME49_311100 among other Apicomplexan (and non-Apicomplexan) taxa. These analyses were preformed to examine the potential conservation of function among homologous protein sequences.

# Materials

 * Hardware: PC laptop 
 * Operating System: Windows 11 Home
 * Programs Utilized:
      * BLAST
      * MAFFT (version 7)
      * MEGAX
 * Databases Utilized: 
      * ToxoDB (https://toxodb.org/toxo/app)
      * NCBI (https://blast.ncbi.nlm.nih.gov/Blast.cgi?PROGRAM=blastp&PAGE_TYPE=BlastSearch&LINK_LOC=blasthome)
       
# Summary of Methods
      
      1. Obtain the protein sequence of TGME49_311100
      2. Preform a BLAST Analysis
      3. Preform a Multiple Sequence Alignment
      4. Create Phylogenetic trees based on the above alignment. 

# Downloading TGME49_311100

TGME49_311100 is serving not only as our protein of interest, but as our reference strain for the following analyses. TGME49_311100 predictive protein sequence was obtained from ToxoDB (VEuPathDB (n.d.)). The gene was then downloaded in FASTA format, as shown below:

               >TGME49_311100  | Toxoplasma gondii ME49 | zinc finger (CCCH type) motif-containing protein | protein | length=920
                     MEGAAGTPCIDGSEEVSEKEWEDDETGRHSSGTGTCFTTSSHTGGNGARADEALDGRVDMGCRELKRRPRLKRMKLQFYKTKMCPWMAQGRCLRGLSCQYAHSECELSPLPNLLKTRMCEMLTLTGSCPRLASECKFAHTAEELRSTEFFARSKMCPLFLSGRCTANEKCRYAHSAQELRKASVASALFLQKHPSRQLQTNTGVVGKGMGNLVCVTGTHDTMLVKKKEENVSESGVSVPPSSSTSARDFLSGDAHPKLTLRYSSGKQEIPPPRFSRRPYNGVPLQRRLMPSVFLCASSGGDSLRRLSCSELGGGSQSLPASPKECATQGTPGSMSGGGGQVHGVARFYPVPQPPPPELRVALFQTATGSGSSPSKKCDQKPQVNSGVHSQEDGARSHIGDRLPKYQDRRGRKGSVWSLSGRGTSCSSSRTSVSSLGLSKEGFRSQMETLAPHAEGHGYQRRTWDRQDGPSKISEVAMPVRSEGSFSETSADTAGSELQSDMTVDALGTKNGSAGSQAGSDERQEEQAPSPASSWATRLPASEGRNFESTDLLACASHTTGLKSEMPRSEGEALPGSTKSNQEQDSASSRQEDERAHQTALADGVTSQRQWRSFSARSRNRGASTPSSQLPWLAQEKSRRPHGLNSEGRAPVAPIRRPAQGEHTGPCRPTAGFPTHGTKRNSSSSRIAAGANAQNNVRQLHQRSVLSAFVRPVFSSLAELPARQGPAWNFVHTGGYAAASTPTTWPFSYEGIPSTQLYPCEQSVPSFPYVPDSRLASPDSCMSRTSFSPQSSGSTVATPHGMPSAPYPSAGGSLLMTCQNRVGNGEVAEQRLAQPSVQTESTLRPASRVILYGSPVDQAACYAGNCGVEAAFSAEIDRQRQLLFLPQSTLGQSMQPLHPEVLLPKLSAEVLKASEPDRYED
     
# BLAST Analysis
  
Once the reference sequence was downloaded, a BLASTP analysis of the predictive protein sequence was conducted. BLASTP was utilized due to its ability to "compares an amino acid query sequence [our predictive protein sequence] against a protein sequence dataset" (Balakrishna et al. 2005). This analysis was conducted utilizing the BLASTP program on NCBI (https://blast.ncbi.nlm.nih.gov/Blast.cgi?PROGRAM=blastp&PAGE_TYPE=BlastSearch&LINK_LOC=blasthome).  This program was chosen due its large and established database, and for its prevalence in prior bioinformatic analyses of the Toxoplasma gondii genome ( Sayers et al. 2021; Smith et l. 2005; Mitra et al. 2022; and Manger et al. 1998).  To determine the validity of the results a secondary BLAST analysis was conducted utilizing the BLASTP program on VEuPathDB- a database which focuses on eukaryotic pathogens and vectors (Amos et al. 2022).
               
# NCBI BLASTP ANALYSIS

# VEuPathDB BLASTP ANALYSIS

# Multiple Sequence Alignment

# Creation of Phylogenomic Trees



# Creating a Predictive Protein Model for TGME49_311100 utilizing ChimeraX Software





# References
Amos, B., Aurrecoechea, C., Barba, M., Barreto, A., Basenko, E. Y., Bażant, W., Belnap, R., Blevins, A. S., Böhme, U., Brestelli, J., Brunk, B. P., Caddick, M., Callan, D., Campbell, L., Christensen, M. B., Christophides, G. K., Crouch, K., Davis, K., DeBarry, J., Doherty, R., … Zheng, J. (2022). VEuPathDB: the eukaryotic pathogen, vector and host bioinformatics resource center. Nucleic acids research, 50(D1), D898–D911. https://doi.org/10.1093/nar/gkab929

Balakrishnan, R., Christie, K. R., Costanzo, M. C., Dolinski, K., Dwight, S. S., Engel, S. R., Fisk, D. G., Hirschman, J. E., Hong, E. L., Nash, R., Oughtred, R., Skrzypek, M., Theesfeld, C. L., Binkley, G., Dong, Q., Lane, C., Sethuraman, A., Weng, S., Botstein, D., & Cherry, J. M. (2005). Fungal BLAST and Model Organism BLASTP Best Hits: new comparison resources at the Saccharomyces Genome Database (SGD). Nucleic acids research, 33(Database issue), D374–D377. https://doi.org/10.1093/nar/gki023

Manger, I. D., Hehl, A. B., & Boothroyd, J. C. (1998). The surface of Toxoplasma tachyzoites is dominated by a family of glycosylphosphatidylinositol-anchored antigens related to SAG1. Infection and immunity, 66(5), 2237–2244. https://doi.org/10.1128/IAI.66.5.2237-2244.1998

Mitra, P., Deshmukh, A. S., Banerjee, S., Khandavalli, C., & Choudhury, C. (2022). A functionally divergent transcription elongation factor 1-like protein in Toxoplasma gondii. FEBS letters, 596(1), 112–127. https://doi.org/10.1002/1873-3468.14241

Sayers, E. W., Beck, J., Bolton, E. E., Bourexis, D., Brister, J. R., Canese, K., Comeau, D. C., Funk, K., Kim, S., Klimke, W., Marchler-Bauer, A., Landrum, M., Lathrop, S., Lu, Z., Madden, T. L., O'Leary, N., Phan, L., Rangwala, S. H., Schneider, V. A., Skripchenko, Y., … Sherry, S. T. (2021). Database resources of the National Center for Biotechnology Information. Nucleic acids research, 49(D1), D10–D17. https://doi.org/10.1093/nar/gkaa892

Smith, A. T., Tucker-Samaras, S. D., Fairlamb, A. H., & Sullivan, W. J., Jr (2005). MYST family histone acetyltransferases in the protozoan parasite Toxoplasma gondii. Eukaryotic cell, 4(12), 2057–2065. https://doi.org/10.1128/EC.4.12.2057-2065.2005


VEuPathDB. (n.d.).  TGME49_311100 zinc finger (CCCH type) motif-containing protein . ToxoDB. Retrieved January 21, 2022, from https://toxodb.org/toxo/app/record/gene/TGME49_311100 
