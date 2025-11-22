# PARSING-FASTA-AND-GENBANK-FILES
PARSING FILES 
    Query successful

📁 Sequence File Parsing and Feature Extraction

📝 Overview

This Jupyter Notebook demonstrates core functionalities of the BioPython library for handling and extracting data from common bioinformatics file formats: FASTA and GenBank.

The script covers fundamental tasks such as iterating through multiple sequence records, retrieving meta-information (IDs, descriptions), accessing the raw sequence, and performing detailed feature analysis on complex GenBank entries (specifically, Homo sapiens Chromosome 22).

🚀 Analysis Workflow

The notebook is divided into two primary sections focusing on each file format:

1. FASTA File Parsing

This section demonstrates reading multiple sequence records from FASTA files and extracting key data for each entry.

    File Usage: Reads sequences from external files (/content/ls_orchid.fasta and /content/protein_alpha.fasta).

    Data Extraction: For each record, the script extracts and prints:

        The raw sequence string.

        The sequence identifier (seq_record.id).

        The total length of the sequence.

    Example Output Snippet (from ls_orchid.fasta):

    gi|2765658|emb|Z78533.1|CIZ78533
    740

    Example Output Snippet (from protein_alpha.fasta):

    aplha_1_protein
    88

2. GenBank File Parsing and Feature Analysis

This section focuses on handling the richer data structure of a GenBank file, which includes detailed annotations about the genomic sequence.

    File Usage: Reads a GenBank record from /content/genbanksequence.gb (Record ID: NC_000022.11, Homo sapiens chromosome 22).

    Record Information: Extracts and prints:

        Gene ID: NC_000022.11

        Description: Homo sapiens chromosome 22, GRCh38.p14 Primary Assembly

        Sequence Length: 50818468

    Feature Extraction: Identifies and counts the occurrence of different annotated feature types within the chromosome record, including:

        gene: 1273

        CDS: 2820

        mRNA: 2732

        regulatory: 3915

        exon: 260

        misc_feature: 9368

        ...and other features like tRNA, ncRNA, and various peptide annotations.

💾 Data Requirements

To run this notebook successfully, you must ensure the following files are available in your working environment (the script assumes they are located at /content/):

    ls_orchid.fasta

    protein_alpha.fasta

    genbanksequence.gb (GenBank file for Homo sapiens chromosome 22).

🛠️ Requirements

The notebook requires the core BioPython library:
Bash

!pip install biopython
