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
      * VEuPathDB (https://veupathdb.org/veupathdb/app/)
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
  
Once the reference sequence was downloaded, a BLASTP analysis of the predictive protein sequence was conducted. BLASTP was utilized due to its ability to "compares an amino acid query sequence [our predictive protein sequence] against a protein sequence dataset" (Balakrishna et al. 2005). This analysis was conducted utilizing the BLASTP program on VEuPathDB (https://veupathdb.org/veupathdb/app/).This program was chosen due its large and established database of eukaryotic pathogens (i.e. parasites) and vectors, as well as its prevalence in prior bioinformatic analyses of T.gondii's genome (Amos et al.2022; Waldman et al. 2020).

The query in VEupathDB was ran under the following conditions:
* Target type: Proteins
* Target organisms : All accepted ( for this database specifically,  eukaryotic pathogens and vectors are).
* E-value : 20
* Maximum Description: 300
* Low-Complexity Filter: Yes

To narrow down results generated from the BLAST analysis, sequences with a E-value above E-20 were discarded. Duplicate gene sequences among the same genus, but different species (or subspecies) were also exclude (the gene sequence with the lowest E value was kept). 

Summary of BLAST Hits:


               1.	>TGRH88_050610 Toxoplasma gondii RH-88 zinc finger (CCCH type) motif-containing protein; E-value = 0
               2.	>HHA_311100 Hammondia hammondi strain H.H.34 zinc finger (CCCH type) motif-containing protein; E-value = 0
               3.	>NCLIV_055080 Neospora caninum Liverpool putative zinc finger (CCCH type) protein; E-value = 0
               4.	>Ncaninum_LIV_000396500 Neospora caninum Liverpool 2019  putative zinc finger (CCCH type) protein; E-value = 0
               5.	>BESB_072600  Besnoitia besnoiti strain Bb-Ger1 unspecified product; E-value = 1E-99
               6.	>Vbra_14922 Vitrella brassicaformis CCMP3155 Tristetraprolin, putative; E-value = 3E-25
               7.	>PCHAS_1238100 Plasmodium chabaudi chabaudi zinc finger protein, putative; E-value = 4E -24
               8.	>PVBDA_1203970 Plasmodium vinckei brucechwatti DA Zinc finger protein, putative ; E-value = 5E -24
               9.	>PY17X_1240900  Plasmodium yoelii yoelii 17X zinc finger protein, putative; E-value = 4E -24
               10.	>PYYM_1240100 Plasmodium yoelii yoelii YM zinc finger protein, putative, fragment; E-value = 4E -24
               11.	>PVSEL_1203530 Plasmodium vinckei Cameroon EL Zinc finger protein, putative; E-value = 8E -24
               12.	>PVVCY_1203840 Plasmodium vinckei vinckei CY  Zinc finger protein, putative; E-value = 7E -24
               13.	>PY06948 Plasmodium yoelii yoelii 17XNL ERYTHROCYTE MEMBRANE PROTEIN PFEMP3; E-value = 4E -24
               14.	>YYE_01715  Plasmodium vinckei vinckei strain vinckei hypothetical protein; E-value = 7E -24
               15.	>PVLDE_1204030 Plasmodium vinckei lentum DE Zinc finger protein, putative; E-value = 1E -23
               16.	>PVPCR_1203860 Plasmodium vinckei petteri CR 2020 Zinc finger protein, putative; E-value = 9E -24
               17.	>YYG_02201 Plasmodium vinckei petteri strain CR hypothetical protein; E-value = 9E -24
               18.	>PBANKA_1237600 Plasmodium berghei ANKA zinc finger protein, putative; E-value = 2E -23
               19.	>PCOAH_00018590 Plasmodium coatneyi Hackeri Uncharacterized protein; E-value = 2E -23
               20.	>PKA1H_070009300 Plasmodium knowlesi strain A1H1 zinc finger protein, putative; E-value = 1E -23
               21.	>PKNH_0704400 Plasmodium knowlesi strain H zinc finger protein, putative; E-value = 1E -23 
               22.	>PKNOH_S06405900 Plasmodium knowlesi strain Malayan Strain Pk1 A putative Zinc finger protein; E-value = 1E -23
               23.	>PcyM_0704500 Plasmodium cynomolgi strain M zinc finger protein, putative; E-value = 2E -23
               24.	>Vbra_11878 Vitrella brassicaformis CCMP3155 hypothetical protein; E-value = 1E -23
               25.	>Vbra_995 Vitrella brassicaformis CCMP3155 Zinc finger CCCH domain-containing protein 28, putative; E-value = 6E -24
               26.	>AK88_00888 Plasmodium fragile strain nilgiri hypothetical protein; E-value = 1E -23
               27.	>HEP_00055900 Hepatocystis sp. ex Piliocolobus tephrosceles 2019 zinc finger protein, putative; E-value = 4E -23
               28.	>PBILCG01_0521400 Plasmodium billcollinsi G01 zinc finger protein, putative; E-value = 5E -23
               29.	 >PCHAS_0415600 Plasmodium chabaudi chabaudi zinc finger protein, putative; E-value = 2E -23
               30.	>PVL_000130100 Plasmodium vivax-like Pvl01 zinc finger protein, putative; E-value = 3E -23
               31.	>PVP01_0705100 Plasmodium vivax P01 zinc finger protein, putative; E-value = 3E -23
               32.	 >PVX_098775 Plasmodium vivax Sal-1 zinc finger protein, putative; E-value = 3E -23
               33.	>Vbra_612 Vitrella brassicaformis CCMP3155 Zinc finger protein 36, C3H1 type-like 2, putative; E-value = 2E -24
               34.	>C922_01502 Plasmodium inui San Antonio 1 hypothetical protein; E-value = 4E -23
               35.	>HEP_00109300 Hepatocystis sp. ex Piliocolobus tephrosceles 2019  zinc finger protein, putative; E-value = 1E -22
               36.	>PRELSG_1008900 Plasmodium relictum SGS1-like zinc finger protein, putative; E-value = 1E -22
               37.	>PVL_100013000 Plasmodium vivax-like Pvl01 zinc finger protein, putative; E-value = 2E -22
               38.	>PVPCR_0401740 Plasmodium vinckei petteri CR 2020 Zinc finger protein, putative; E-value = 5E -23
               39.	>PmUG01_07018200 Plasmodium malariae UG01 zinc finger protein, putative; E-value = 5E -23
               40.	>Vbra_6028 Vitrella brassicaformis CCMP3155 hypothetical protein; E-value = 3E -23
               41.	>Vbra_6051 Vitrella brassicaformis CCMP3155 Tristetraprolin, putative; E-value = 9E -23
               42.	>Vbra_8755 Vitrella brassicaformis CCMP3155 Zinc finger CCCH domain-containing protein 28, putative; E-value = 1E -23
               43.	>YYG_04001 Plasmodium vinckei petteri strain CR hypothetical protein; E-value = 5E -23 
               44.	>AK88_02815 Plasmodium fragile strain nilgiri hypothetical protein; E-value = 3E -22
               45.	>C922_01372 Plasmodium inui San Antonio 1 hypothetical protein; E-value = 2E -22
               46.	>Cvel_16490 Chromera velia CCMP2878 Cleavage and polyadenylation specificity factor, putative; E-value = 2E -22
               47.	>NCLIV_001710 Neospora caninum Liverpool putative zinc finger (CCCH type) protein; E-value = 2E -22
               48.	>Ncaninum_LIV_000522200 Neospora caninum Liverpool 2019 putative zinc finger (CCCH type) protein; E-value = 2E -22
               49.	>PADL01_0521900 Plasmodium adleri G01 zinc finger protein, putative; E-value = 2E -22
               50.	>PBLACG01_0524700 Plasmodium blacklocki G01 zinc finger protein, putative; E-value = 1E -22
               51.	>PCOAH_00029320 Plasmodium coatneyi Hackeri Uncharacterized protein; E-value = 2E -22
               52.	>PCYB_101880 Plasmodium cynomolgi strain B hypothetical protein; E-value = 2E -22
               53.	>PKA1H_100015200 Plasmodium knowlesi strain A1H1 zinc finger protein, putative; E-value = 2E -22
               54.	>PKNH_1010000 Plasmodium knowlesi strain H zinc finger protein, putative; E-value = 2E -22 
               55.	>PKNOH_S07447900 Plasmodium knowlesi strain Malayan Strain Pk1 A putative Zinc finger protein; E-value = 2E -22
               56.	>PRCDC_0522000 Plasmodium reichenowi CDC zinc finger protein, putative; E-value = 2E -22
               57.	>PYYM_0417500 Plasmodium yoelii yoelii YM zinc finger protein, putative; E-value = 1E -22
               58.	>PocGH01_07014100 Plasmodium ovale curtisi GH01 zinc finger protein, putative; E-value = 6E -23
               59.	>Vbra_20021 Vitrella brassicaformis CCMP3155 mRNA 3'-end-processing protein yth1, putative; E-value = 1E -22
               60.	>Vbra_8964  Vitrella brassicaformis CCMP3155 hypothetical protein; E-value = 1E -23
               61.	>BEWA_019250 Theileria equi strain WA  hypothetical protein; E-value = 3E -24
               62.	>PADL01_0905700 Plasmodium adleri G01 zinc finger protein, putative; E-value = 3E -22
               63.	>PBANKA_0414700 Plasmodium berghei ANKA zinc finger protein, putative; E-value = 1E -22
               64.	>PBLACG01_0522600 Plasmodium blacklocki G01 zinc finger protein, putative; E-value = 4E -22
               65.	>PBLACG01_0905900 Plasmodium blacklocki G01 zinc finger protein, putative; E-value = 2E -22
               66.	>PGABG01_0904100 Plasmodium gaboni strain G01 zinc finger protein, putative; E-value = 3E -22
               67.	>PGSY75_0522900 Plasmodium gaboni strain SY75 putative zinc finger protein; E-value = 3E -22 
               68.	>PGSY75_0906600 Plasmodium gaboni strain SY75 putative zinc finger protein; E-value = 3E -22
               69.	>PPRFG01_0524100 Plasmodium praefalciparum strain G01 zinc finger protein, putative; E-value = 4E -22
               70.	>PPRFG01_0905500 Plasmodium praefalciparum strain G01 zinc finger protein, putative; E-value = 4E -22
               71.	>PRELSG_0703900 Plasmodium relictum SGS1-like zinc finger protein, putative; E-value = 7E -23
               72.	>PRG01_0522200 Plasmodium reichenowi G01 zinc finger protein, putative; E-value = 3E -22
               73.	>PRG01_0914000 Plasmodium reichenowi G01 zinc finger protein, putative; E-value = 3E -22
               74.	>PVBDA_0401710 Plasmodium vinckei brucechwatti DA Zinc finger protein, putative; E-value = 2E -22
               75.	 >PVLDE_0401700 Plasmodium vinckei lentum DE Zinc finger protein, putative; E-value = 3E -22
               76.	>PVP01_1011000 Plasmodium vivax P01 zinc finger protein, putative; E-value = 5E -22
               77.	>PVSEL_0401690 Plasmodium vinckei Cameroon EL Zinc finger protein, putative; E-value = 2E -22
               78.	>PVVCY_0401580 Plasmodium vinckei vinckei CY unspecified product; E-value = 2E -22
               79.	PVX_080105 Plasmodium vivax Sal-1 hypothetical protein, conserved; E-value = 5E -22
               80.	>Pf7G8-2_000142100 Plasmodium falciparum 7G8 2019 zinc finger protein, putative; E-value = 5E -22 
               81.	>Pf7G8_050028100 Plasmodium falciparum 7G8 zinc finger protein, putative; E-value = 5E -22
               82.	>PfCD01_050029200 Plasmodium falciparum CD01 zinc finger protein, putative; E-value = 5E -22
               83.	>PfGA01_050027300  | Plasmodium falciparum GA01 | zinc finger protein, putative; E-value = 4E -22
               84.	>PfGB4_050028800 Plasmodium falciparum GB4 zinc finger protein, putative; E-value = 4E -22
               85.	>PfGN01_050027800 Plasmodium falciparum GN01 zinc finger protein, putative; E-value = 4E -22
               86.	>PfHB3_050027900 Plasmodium falciparum HB3 zinc finger protein, putative; E-value = 4E -22
               87.	>PfKH01_050028200 Plasmodium falciparum KH01 zinc finger protein, putative; E-value = 5E -22 
               88.	>PfKH02_050028400 Plasmodium falciparum KH02 zinc finger protein, putative; E-value = 5E -22
               89.	>PfNF135_000005600 Plasmodium falciparum NF135.C10 zinc finger protein, putative; E-value = 5E -22
               90.	>PfNF166_090010700 Plasmodium falciparum NF166 zinc finger protein, putative; E-value = 4E -22
               91.	>PfNF54_050027100 Plasmodium falciparum NF54 zinc finger protein, putative; E-value = 5E -22
               92.	>PfNF54_090011800 Plasmodium falciparum NF54 zinc finger protein, putative; E-value = 4E -22
               93.	>PfSD01_050027700 Plasmodium falciparum SD01 zinc finger protein, putative; E-value = 5E -22
               94.	>PfSN01_050028000 Plasmodium falciparum SN01 zinc finger protein, putative; E-value = 4E -22 
               95.	>PfSN01_090011300 Plasmodium falciparum SN01 zinc finger protein, putative; E-value = 4E -22  
               96.	>PocGH01_10018800 Plasmodium ovale curtisi GH01 zinc finger protein, putative; E-value = 5E -22 
               97.	>YYE_04042 Plasmodium vinckei vinckei strain vinckei hypothetical protein; E-value = 2E -22  
               98.	>HHA_218300 Hammondia hammondi strain H.H.34 zinc finger (CCCH type) motif-containing protein; E-value = 2E -22  
               99.	>PBILCG01_0523300  Plasmodium billcollinsi G01 zinc finger protein, putative; E-value = 5E -22  
               100.	>PBILCG01_0910200 Plasmodium billcollinsi G01 zinc finger protein, putative; E-value = 5E -22  
               101.	>PGABG01_0524000 Plasmodium gaboni strain G01 zinc finger protein, putative; E-value = 4E -22  
               102.	>PGAL8A_00070100 Plasmodium gallinaceum 8A zinc finger protein, putative; E-value = 8E -22  
               103.	>PGAL8A_00419200 Plasmodium gallinaceum 8A zinc finger protein, putative; E-value = 2E -22   
               104.	>PGSY75_0525000 Plasmodium gaboni strain SY75 putative zinc finger protein; E-value = 4E -22  
               105.	>PRCDC_0904700 Plasmodium reichenowi CDC zinc finger protein, putative; E-value = 5E -22  
               106.	>Pf7G8-2_000254700 Plasmodium falciparum 7G8 2019 zinc finger protein, putative; E-value = 4E -22   
               107.	>Pf7G8_090011500 Plasmodium falciparum 7G8 zinc finger protein, putative; E-value = 4E -22   
               108.	>PfCD01_090011000 Plasmodium falciparum CD01 zinc finger protein, putative; E-value = 4E -22    
               109.	 >PfDd2_090011900 Plasmodium falciparum Dd2 zinc finger protein, putative; E-value = 4E -22
               110.	>PfGB4_090011600 Plasmodium falciparum GB4 zinc finger protein, putative; E-value = 4E -22
               111.	 >PfKH02_090011400 Plasmodium falciparum KH02 zinc finger protein, putative; E-value = 4E -22
               112.	 >PfML01_090011100 Plasmodium falciparum ML01 zinc finger protein, putative; E-value = 4E -22
               113.	>PfNF135_090010300 Plasmodium falciparum NF135.C10 zinc finger protein, putative; E-value = 4E -22
               114.	>PfSD01_090011700 Plasmodium falciparum SD01 zinc finger protein, putative; E-value = 4E -22
               115.	>PmUG01_10021700 Plasmodium malariae UG01 zinc finger protein, putative; E-value = 7E -22
               116.	>TGARI_218300 Toxoplasma gondii ARI zinc finger (CCCH type) motif-containing protein; E-value = 7E -22
               117.	>Vbra_4732 Vitrella brassicaformis CCMP3155 Zinc finger CCCH domain-containing protein 15, putative; E-value = 1E -22
               118.	>EfaB_PLUS_7048.g667  Eimeria falciformis Bayer Haberkorn 1970 unspecified product; E-value = 2E -21
               119.	 >NCLIV_061920 Neospora caninum Liverpool putative zinc finger (CCCH type) protein; E-value = 1E -21
               120.	>Ncaninum_LIV_000317500 Neospora caninum Liverpool 2019 putative zinc finger (CCCH type) protein; E-value = 1E -21
               121.	>PBANKA_1239800 Plasmodium berghei ANKA zinc finger protein, putative; E-value = 9E -22
               122.	>PPRFG01_0526200 Plasmodium praefalciparum strain G01 zinc finger protein, putative; E-value = 7E -22
               123.	>PRG01_0524300 Plasmodium reichenowi G01 zinc finger protein, putative; E-value = 5E -22
               124.	>Pf7G8-2_000144200 Plasmodium falciparum 7G8 2019 zinc finger protein, putative; E-value = 7E -22
               125.	>Pf7G8_050030200 Plasmodium falciparum 7G8 zinc finger protein, putative; E-value = 7E -22
               126.	 >PfCD01_050031300 Plasmodium falciparum CD01 zinc finger protein, putative; E-value = 7E -22
               127.	>PfDd2_050029900  Plasmodium falciparum Dd2 zinc finger protein, putative; E-value = 8E -22
               128.	>PfGA01_050029400 Plasmodium falciparum GA01 zinc finger protein, putative; E-value = 7E -22
               129.	>PfGB4_050030900 Plasmodium falciparum GB4 zinc finger protein, putative; E-value = 7E -22
               130.	>PfHB3_050030000 Plasmodium falciparum HB3 zinc finger protein, putative; E-value = 7E -22
               131.	>TGP89_294840 Toxoplasma gondii p89 zinc finger (CCCH type) motif-containing protein; E-value = 1E -21
               132.	>TGRH88_019880  Toxoplasma gondii RH-88  zinc finger (CCCH type) motif-containing protein; E-value = 1E -21
               133.	>Vbra_18848 Vitrella brassicaformis CCMP3155 mRNA 3'-end-processing protein yth-1, putative; E-value = 9E -23
               134.	>AK88_02794 Plasmodium fragile strain nilgiri hypothetical protein; E-value = 2E -21 
               135.	>C922_01393 Plasmodium inui San Antonio 1 hypothetical protein; E-value = 3E -21 
               136.	>EAH_00030720 Eimeria acervulina Houghton hypothetical protein, conserved; E-value = 2E -21
               137.	>HHA_294840 Hammondia hammondi strain H.H.34 zinc finger (CCCH type) motif-containing protein; E-value = 3E -21
               138.	>PCHAS_1240200 Plasmodium chabaudi chabaudi zinc finger protein, putative; E-value = 1E -21 
               139.	>PVBDA_1204180 Plasmodium vinckei brucechwatti DA  Zinc finger protein, putative; E-value = 1E -21
               140.	>PVLDE_0700540  Plasmodium vinckei lentum DE Zinc finger protein, putative; E-value = 2E -21
               141.	>PVP01_1008800 Plasmodium vivax P01 zinc finger protein, putative; E-value = 3E -21
               142.	>PVPCR_1204070 Plasmodium vinckei petteri CR 2020 Zinc finger protein, putative ; E-value = 1E -21
               143.	>PVSEL_1203740 Plasmodium vinckei Cameroon EL  Zinc finger protein, putative; E-value = 2E -21
               144.	>PVVCY_1204050 Plasmodium vinckei vinckei CY Zinc finger protein, putative ; E-value = 2E -21
               145.	>PVX_079995 Plasmodium vivax Sal-1 hypothetical protein, conserved; E-value = 2E -21
               146.	>PY06412 Plasmodium yoelii yoelii 17XNL asparagine-rich protein, putative; E-value = 1E -21
               147.	>PY17X_1243000 Plasmodium yoelii yoelii 17X zinc finger protein, putative; E-value = 1E -21
               148.	>PYYM_1242200 Plasmodium yoelii yoelii YM zinc finger protein, putative ; E-value = 1E -21
               149.	>PcyM_1006600  Plasmodium cynomolgi strain M zinc finger protein, putative; E-value = 3E -21
               150.	>YYE_01736 Plasmodium vinckei vinckei strain vinckei hypothetical protein; E-value = 2E -21 
               151.	>YYG_02180 Plasmodium vinckei petteri strain CR hypothetical protein; E-value = 1E -21
               152.	>BESB_026190 Besnoitia besnoiti strain Bb-Ger1 unspecified product; E-value = 7E -21
               153.	>Cvel_13961 Chromera velia CCMP2878 Zinc finger CCCH domain-containing protein 54, putative ; E-value = 6E -21
               154.	>Cvel_26722  Chromera velia CCMP2878 Zinc finger protein 36, C3H1 type-like 2, putative; E-value = 6E -21
               155.	>PKNH_1007800 Plasmodium knowlesi strain H zinc finger protein, putative; E-value = 5E -21
               156.	>PKNOH_S07445700 Plasmodium knowlesi strain Malayan Strain Pk1 A putative Zinc finger protein; E-value = 5E -21
               157.	>PVL_100011100  Plasmodium vivax-like Pvl01 zinc finger protein, putative; E-value = 5E -21
               158.	>CSUI_003564 Cystoisospora suis strain Wien I zinc finger (ccch type) motif-containing protein; E-value = 9E -21
               159.	>Cvel_23282 Chromera velia CCMP2878 Zinc finger protein 36, C3H1 type-like 1, putative ; E-value = 2E -20
               160.	>ENH_00012580 Eimeria necatrix Houghton hypothetical protein, conserved ; E-value = 8E -21
               161.	>ETH2_1046200 Eimeria tenella Houghton 2021 Zinc finger C-x8-C-x5-C-x3-H type (and similar), putative; E-value = 6E -21
               162.	>ETH_00021925 Eimeria tenella strain Houghton hypothetical protein, conserved; E-value = 6E -21
               163.	>PGAL8A_00072300 Plasmodium gallinaceum 8A zinc finger protein, putative; E-value = 3E -21
               164.	>PRELSG_1006700  Plasmodium relictum SGS1-like zinc finger protein, putative; E-value = 3E -21
               165.	>PocGH01_10016600 Plasmodium ovale curtisi GH01 zinc finger protein, putative ; E-value = 7E -21
               166.	 >Vbra_14116 Vitrella brassicaformis CCMP3155 Zinc finger protein 36, C3H1 type-like 1, putative; E-value = 1E -20
               167.	>BESB_039210 Besnoitia besnoiti strain Bb-Ger1 unspecified product; E-value = 3E -20
               168.	>CSUI_002545 Cystoisospora suis strain Wien I zinc finger (ccch type) motif-containing protein; E-value = 3E -20
               169.	>LOC34617604 Cyclospora cayetanensis isolate NF1_C8 uncharacterized LOC34617604; E-value = 2E -20
               170.	>CF003286  Cytauxzoon felis strain Winnie unspecified product; E-value = 2E -21
               171.	 >Vbra_19705 Vitrella brassicaformis CCMP3155 hypothetical protein; E-value = 2E -20
               172.	>Vbra_22380 Vitrella brassicaformis CCMP3155 RING finger protein unkempt homolog, putative; E-value = 2E -20
               173.	>Bdiv_036840c Babesia divergens strain 1802A Zinc finger C-x8-C-x5-C-x3-H type domain containing protein; E-value = 6E -21
               174.	 >Cvel_21852 Chromera velia CCMP2878 Tristetraprolin, putative; E-value = 6E -21
               175.	>EfaB_PLUS_15724.g1358 Eimeria falciformis Bayer Haberkorn 1970 unspecified product; E-value = 4E -20
               176.	>GNI_181660 Gregarina niphandrodes Unknown strain putative zinc finger protein; E-value = 5E -21
               177.	>Vbra_14940 Vitrella brassicaformis CCMP3155 hypothetical protein; E-value = 5E -20 
               178.	>BBBOND_0311270 Babesia bigemina strain BOND Zinc finger C-x8-C-x5-C-x3-H type domain containing protein, putative; E-value = 8E -21
               179.	>CmeUKMEL1_04785 Cryptosporidium meleagridis strain UKMEL1 Zinc finger C-x8-C-x5-C-x3-H type (and similar) family protein; E-value = 3E -20
               180.	>CPATCC_002651 Cryptosporidium parvum IOWA-ATCC hypothetical protein; E-value = 8E -20
               181.	 >cgd6_1330 Cryptosporidium parvum Iowa II Uncharacterized protein with CCCH-type Zinc finger; E-value = 8E -20
               182.	 >ChTU502y2012_406g0395 Cryptosporidium hominis isolate TU502_2012 hypothetical protein; E-value = 9E -20
               183.	>GY17_00000134 Cryptosporidium hominis isolate 30976 Uncharacterized protein with CCCH-type Zinc finger; E-value = 9E -20
               184.	>CMU_008650 Cryptosporidium muris RN66 zinc finger, CCCH type domain-containing protein; E-value = 8E -20


# VEuPathDB BLASTP ANALYSIS

# Multiple Sequence Alignment

# Creation of Phylogenomic Trees



# Creating a Predictive Protein Model for TGME49_311100 utilizing ChimeraX Software





# References
Amos, B., Aurrecoechea, C., Barba, M., Barreto, A., Basenko, E. Y., Bażant, W., Belnap, R., Blevins, A. S., Böhme, U., Brestelli, J., Brunk, B. P., Caddick, M., Callan, D., Campbell, L., Christensen, M. B., Christophides, G. K., Crouch, K., Davis, K., DeBarry, J., Doherty, R., … Zheng, J. (2022). VEuPathDB: the eukaryotic pathogen, vector and host bioinformatics resource center. Nucleic acids research, 50(D1), D898–D911. https://doi.org/10.1093/nar/gkab929

Balakrishnan, R., Christie, K. R., Costanzo, M. C., Dolinski, K., Dwight, S. S., Engel, S. R., Fisk, D. G., Hirschman, J. E., Hong, E. L., Nash, R., Oughtred, R., Skrzypek, M., Theesfeld, C. L., Binkley, G., Dong, Q., Lane, C., Sethuraman, A., Weng, S., Botstein, D., & Cherry, J. M. (2005). Fungal BLAST and Model Organism BLASTP Best Hits: new comparison resources at the Saccharomyces Genome Database (SGD). Nucleic acids research, 33(Database issue), D374–D377. https://doi.org/10.1093/nar/gki023

Waldman, B. S., Schwarz, D., Wadsworth, M. H., 2nd, Saeij, J. P., Shalek, A. K., & Lourido, S. (2020). Identification of a Master Regulator of Differentiation in Toxoplasma. Cell, 180(2), 359–372.e16. https://doi.org/10.1016/j.cell.2019.12.013

VEuPathDB. (n.d.).  TGME49_311100 zinc finger (CCCH type) motif-containing protein . ToxoDB. Retrieved January 21, 2022, from https://toxodb.org/toxo/app/record/gene/TGME49_311100 
