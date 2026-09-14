# TechMedBuddy

The Basic Local Alignment Search Tool (BLAST) finds regions of local similarity between a query sequence and database records. It helps researchers identify unknown 
genes, classify organisms, and infer evolutionary relationships. 
BLASTn: Compares a nucleotide query (DNA/RNA) to a sequence database. 
BLASTp: Compares a protein (amino acid query) to a protein database. 
BLASTx: Translates a nucleotide query in six reading frames and compares it to a protein database. 
tBLASTn: Compares a protein query to a nucleotide database translated in six reading frames. 

This script provides a comprehensive tool for performing various types of sequence similarity searches (BLAST) directly from a Google Colab notebook. It leverages the Biopython library to interact with NCBI's BLAST web services.

The overall workflow is:

Setup: Installs Biopython and imports necessary modules.
BLAST Functionality: Defines a reusable function (run_blast) to abstract away the details of sending a query to NCBI, retrieving results, and parsing the complex XML output into Python objects.
User Input: Prompts the user to upload a FASTA file containing their DNA sequence of interest.
Sequence Extraction: Reads the uploaded FASTA file to extract the primary DNA sequence.
Multi-faceted BLAST: Executes five different types of BLAST searches (blastn, blastx, blastp, tblastn, tblastx) using the input DNA sequence (and its protein translation where appropriate) against the nr (non-redundant) NCBI database. This covers comparisons between DNA and DNA, translated DNA and protein, protein and protein, and various combinations of translated nucleotide databases.
It automates the process of performing a full suite of common BLAST analyses on a user-provided sequence, preparing the results for further analysis within the notebook.
