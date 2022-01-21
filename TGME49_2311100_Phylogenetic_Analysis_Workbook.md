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
  
Once the reference sequence was downloaded, a BLASTP analysis of the protein was conducted. BLASTP was utilized due to its ability to "compares an amino acid query sequence [our predictive protein sequence] against a protein sequence dataset" (Balakrishna et al. 2005). This analysis was run utilizing NCBI's BLASTP program
               Citation for why for above
               
               
To determine the validity of the results a secondary BLASTP Analysis was conducted in VEuPathDB.

# Multiple Sequence Alignment

# Creation of Phylogenomic Trees



# Creating a Predictive Protein Model for TGME49_311100 utilizing ChimeraX Software

# References
Balakrishnan, R., Christie, K. R., Costanzo, M. C., Dolinski, K., Dwight, S. S., Engel, S. R., Fisk, D. G., Hirschman, J. E., Hong, E. L., Nash, R., Oughtred, R., Skrzypek, M., Theesfeld, C. L., Binkley, G., Dong, Q., Lane, C., Sethuraman, A., Weng, S., Botstein, D., & Cherry, J. M. (2005). Fungal BLAST and Model Organism BLASTP Best Hits: new comparison resources at the Saccharomyces Genome Database (SGD). Nucleic acids research, 33(Database issue), D374–D377. https://doi.org/10.1093/nar/gki023

VEuPathDB. (n.d.).  TGME49_311100 zinc finger (CCCH type) motif-containing protein . ToxoDB. Retrieved January 21, 2022, from https://toxodb.org/toxo/app/record/gene/TGME49_311100 
