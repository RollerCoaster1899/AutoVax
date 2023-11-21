NOTE: Web Driver EDGE file .exe must downloaded through official channels (https://developer.microsoft.com/en-us/microsoft-edge/tools/webdriver/) and be in the same file folder. Please cite the different programs used.  

This Python script presents a pipeline for identifying and analyzing epitopes (antigenic determinants) for MHC-I, MHC-II, and B cells, and then constructing a multi-epitopic peptide vaccine. Let's break down the steps and functions of the Python code:

1.- Identification of MHC-I Epitopes:

Platform Used: MHC-I Binding Predictions (NetMHCpan 4.1) from the National Institutes of Health.
Method: NetMHCpan 4.1, using HLA reference alleles.
Selection Criteria: Top 100 epitopes based on affinity scores.
Result Processing: Selecting the top 100 epitopes for further analysis.

2.- Identification of MHC-II Epitopes:

Platform Used: MHC-II Binding Predictions (NetMHCIIpan 4.1) from the National Institutes of Health.
Method: NetMHCIIpan 4.1, using HLA-DR reference alleles.
Selection Criteria: Top 100 epitopes based on affinity scores.
Result Processing: Selecting the top 100 epitopes for further analysis.

3.- Identification of B Cell Epitopes:

Platform Used: Antibody Epitope Prediction from the National Institutes of Health, utilizing various models.
Models Used: Bepipred Linear Epitope Prediction 2.0, Bepipred Linear Epitope Prediction, Chou & Fasman Beta-Turn Prediction, Emini Surface Accessibility Prediction, Karplus & Schulz Flexibility Prediction, Kolaskar & Tongaonkar Antigenicity, and Parker Hydrophilicity Prediction.
Result Processing: Obtaining different B cell epitopes from different models.

4.- Epitope Cleaning:

Objective: Eliminating duplicate peptide sequences.
Result Processing: Reducing the number of MHC-I epitopes from 100 to 50, MHC-II epitopes from 100 to 67, and B cell epitopes from 33 to 27.

5.- Evaluation of Antigenicity and Safety:

Tools Used: VaxiJen v2.0 and AllerTop v2.0.
Antigenicity Evaluation: Using VaxiJen with a threshold of 0.6.
Allergenicity Evaluation: Using AllerTop.
Result Processing: Identifying MHC-I epitopes, MHC-II epitopes, and B cell epitopes that passed the antigenicity level.

6.- Construction of Multi-Epitopic Peptide Vaccine:

Linkers Used: "EAAAK" for adjuvants, "AAY" for MHC-I, "GPGPG" for MHC-II, and "KK" for B cell epitopes.
Overlap Processing: Overlapping regions to improve immunogenic coverage.
Result Processing: Constructing final regions with different safe and antigenic MHC-II epitopes, MHC-II epitopes, and B cell epitopes.

7.- Final Structure:

Combining the constructed regions to form a multi-epitopic peptide vaccine for MHC-I, MHC-II, and B cells.

This script integrates various bioinformatics tools and platforms to predict, filter, and construct a potential peptide vaccine with optimized immunogenicity and safety. The final structure represents a concatenated sequence of epitopes with appropriate linkers for each type of immune response.


References: 
Vita R, Mahajan S, Overton JA, Dhanda SK, Martini S, Cantrell JR, Wheeler DK, Sette A, Peters B. The Immune Epitope Database (IEDB): 2018 update. Nucleic Acids Res. 2018 Oct 24. doi: 10.1093/nar/gky1006. PMID: 30357391; PMCID: PMC6324067 
Doytchinova, I.A., Flower, D.R. VaxiJen: a server for prediction of protective antigens, tumour antigens and subunit vaccines. BMC Bioinformatics 8, 4 (2007). https://doi.org/10.1186/1471-2105-8-4 
Dimitrov, I., Bangov, I., Flower, D.R., Doytchinova, I. AllerTOP v.2 - a server for in silico prediction of allergens. J. Mol. Model., 20, 2278, 2014.
Chung EH. Vaccine allergies. Clin Exp Vaccine Res. 2014 Jan;3(1):50-7. doi: 10.7774/cevr.2014.3.1.50. Epub 2013 Dec 18. PMID: 24427763; PMCID: PMC3890451.
Md. Shakhawat Hossain, Mohammad Imran Hossan, Shagufta Mizan, Abu Tayab Moin, Yasmin, F., Al-Shahriar Akash, Shams Nur Powshi, A.K Rafeul Hasan, & Afrin Sultana Chowdhury. (2021). Immunoinformatics approach to designing a multi-epitope vaccine against Saint Louis Encephalitis Virus. Informatics in Medicine Unlocked, 22, 100500–100500. https://doi.org/10.1016/j.imu.2020.100500


Disclamer:
Web scraping might violate the terms of service or rules of some websites, and users should exercise caution to comply with legal and ethical standards. Users of the library should be reminded to review and respect the terms of use, privacy policies, and any applicable laws of the websites they intend to scrape. The disclaimer may also advise users to obtain explicit permission from website owners before scraping their content and emphasize that any misuse or violation of terms is the sole responsibility of the user. 