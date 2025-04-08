# GWAS-Sex-Stratified
GWAS 
Description:
This script performs a genome-wide association study (GWAS) using PLINK. It runs logistic regression analyses for all individuals, females only, and males only, calculates allele frequencies for each group, and performs a sex-interaction test to identify variants with differential effects by sex. It also extracts the interaction term (ADDxSEX) from the logistic output for further analysis.

Dependencies:

PLINK v1.9 or later – Required for logistic regression, frequency calculation, and sex-stratified filtering.
Input: Binary PLINK dataset (.bed, .bim, .fam)

GWAMA
Description:
This script prepares male and female GWAS summary statistics for a sex-difference meta-analysis using GWAMA. It converts PLINK output files to GWAMA-compatible format, builds a marker map, generates the GWAMA input file, and executes GWAMA to identify SNPs with significantly different effects between sexes.

Dependencies:

PLINK2GWAMA.pl – A Perl script to convert PLINK output into GWAMA input format. Must be present in the bin/ directory.
GWAMA binary – The GWAMA executable must be located in bin/ and accessible as ./bin/GWAMA.
Perl – Required to run PLINK2GWAMA.pl.
Input: PLINK .assoc.logistic and .frq files for both female and male datasets
