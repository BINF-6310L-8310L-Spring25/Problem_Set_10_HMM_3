# Problem_Set_10

This week we continued to learn about Hidden Markov Models. A common use for HMMs is analysis of biological sequence data. 

For this problem set we will build and analyze an HMM using the aphid package. https://cran.r-project.org/web/packages/aphid/aphid.pdf

The scenario we will be replicating is very common in my work. We are often interested in identifying homologous genes in new genomes using a reference set of gene annotations. 

First we build an HMM from the reference sequences. Then we use that HMM to find orthologues in the new genome. 

### Step 1 - Load Packages

Install and load the aphid package ("aphid")
Install and load the sequence input package ("seqinr")

### Step 2 - Read in Sequences

Our reference sequences are in the file BBH1.fasta . This is a part of a real analysis conducted on budding yeast species. 

The BBH1 gene is a part of the carnitine biosynthesis pathway. In our preliminary analysis of budding yeast species we had identified enzymes corresponding to the first 2 enzymes in this biosynthesis pathway. This preliminary anlaysis was based on HMMs built from other eukaryotic species. A literature search demonstrated that BBH1 is known to exist in _Candida_ yeast species. This suggested we needed to construct a new HMM! 

Read in the sequence file using the function ```read.fasta()```. 
Make sure to specify the sequence type

### Step 3 - Align the sequences

Use the ```align()``` function from aphid to align the input sequences. Save the output into a new variable

Answer the following questions about the alignment
1) How many modules were in the PHMM used to create the alignment
2) How many of the hidden states were "Insertion" states? 

