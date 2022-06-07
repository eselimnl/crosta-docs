## 2.1. Input file
Please upload a Multiple Sequence Alignment (MSA) in FASTA format. Any alignment tool can be used to produce the MSA, such as MAFFT or MUSCLE as long as the input sequences provided to CROSTA are in FASTA format. 
CROSTA will screen the sequences before the analysis starts and will inform the user about the problematic sequences. 

```{note}
Download sample data through the SAMPLES button on the home page. 
```

## 2.2.	Header Parsing
Many viral sequence databases (such as NCBI Virus, ViPR, GISAID, etc.) allow data retrieval in FASTA format with a header including metadata such as geo location, host-species, data collection, etc. To integrate the metadata into the analysis, the user is expected to tag the appropriate format. Please make sure that your sequences have rich and consistent (standardized for all) metadata as CROSTA depends on these to produce insights into the transmissibility. 

CROSTA has a built-in tool, co-alignment splitter, to help with pre-processing of data.  This tool provides extracting host-specific sequences from a co-alignment based on selected metadata after the header parsing. 
Click on “SAVE DATASETS” and “NEXT” to go to the next step, adjustment of analysis parameters. 

```{note}
Example of a definition line: >ATY74257.1 |2017|China|Homo sapiens. In this case, the user should fill out the metadata tags as followed: Accession | Year | Geo Location| Host
```

## 2.3. Parameters
 ### 2.3.1. Protein name
  Name of sequence to be analysed. For example: HIV-1 Clade B Pol protein.
 ### 2.3.2. Low support threshold
  The support is defined as the number of sequences at a given *k-mer* position that do not harbor a gap and unknown and/or ambiguous residues. Positions below a statistical support of 30 sequences (default) are defined as of low support. The user has the flexibility to set the threshold for low support.
 ### 2.3.3. K-mer length
  Select a *k-mer* window size that is appropriate for the analysis.\ 
While the minimum applicable size is 3, the maximum can equal to the alignment length of the uploaded input file. By default, DiMA uses a window size of nine (9; nonamer; 9-mer) to evaluate the viral diversity with respect to cellular immune response.

