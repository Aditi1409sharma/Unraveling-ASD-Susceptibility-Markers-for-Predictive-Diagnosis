# Unraveling-ASD-Susceptibility-Markers-for-Predictive-Diagnosis

## Project Overview

This project involves the analysis of a large dataset from Varicarta, containing 309,239 gene variants associated with Autism Spectrum Disorder (ASD). The dataset comprises 466,926 rows and 54 columns, compiled from various research papers. The analysis focuses on identifying significant gene variants, their chromosomal locations, and their potential pathogenicity using various computational techniques.

## Dataset Description

The dataset (`final_data.tsv`) contains detailed information on gene variants, including:
- Gene symbols
- Chromosome numbers
- Start positions (hg19)
- Various test scores (e.g., PolyPhen2, SIFT)
- Validation methods

## Project Steps

### 1. Data Loading and Initial Inspection
The dataset is loaded and inspected to understand its structure and contents.

### 2. Chromosomal Sorting and Data Organization
The data is sorted chromosomally and stored in a dictionary for easier access and analysis. This step ensures that data related to each chromosome can be analyzed independently.

### 3. Handling Missing Values
A function is used to replace NaN values with the median of the column. This is crucial for maintaining the integrity of the dataset and ensuring that subsequent analyses are accurate.

### 4. Gene Symbol Data Cleaning
Float values in the `gene_symbol` column are identified and removed to ensure that the column contains only valid gene symbols.

### 5. Filtering Specific Genes
The dataset is filtered to include only specific genes of interest. These genes are selected based on a provided gene list, focusing on those with significant relevance to ASD.

### 6. Column Reduction
Unnecessary columns are removed to streamline the dataset for analysis. This step helps in reducing computational complexity and focusing on the most relevant data.

### 7. Further Filtering for PolyPhen2 and SIFT Scores
Rows where values for PolyPhen2 and SIFT scores are null are removed. These scores are crucial for assessing the pathogenicity of gene variants.

### 8. Analyzing SFARI Genes
SFARI gene data is filtered based on gene scores and syndromic nature. The data is divided into four categories:
- High gene score (3.0), syndromic
- High gene score (3.0), non-syndromic
- Low gene score (1.0), syndromic
- Low gene score (1.0), non-syndromic

### 9. Visualization
Scatter plots are generated for `start_hg19` vs. `Polyphen2_HVAR_score` and `SIFT_score`, with specific genes highlighted. This visualization helps in identifying significant loci and understanding the distribution of scores across chromosomes.

## Conclusion

This project provides a comprehensive analysis of gene variants associated with ASD. By organizing, cleaning, and filtering the data, and then visualizing the results, significant insights into the genetic basis of ASD can be obtained. The use of PolyPhen2 and SIFT scores helps in identifying potentially pathogenic variants, which could be crucial for further research and understanding of ASD.
