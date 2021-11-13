# REGSP

## A visualized application for homology-based gene searching and plotting using multiple reference sequences

ReGSP accepts multiple reference sequences for homology-based gene search. The tool incorporates cPlot, adot plot tool, for illustrating nucleotide sequence similarity between the query and the reference sequences. It performs gene searching using BLAST and two filtering parameters called maximum number of matched BLAST hits per group (*N*) and minimum number of sub-gene counts per contig (*M*).

ReGSP has a simple and convenient web tool accessible [here.](https://ds.mju.ac.kr/regsp/#/navregsp/regsp)

#### Here we provide a Linux binary package for local execution

The binary package file provided here runs on linux platform and needs the followning inputs.

- Amino acid reference sequences (CDS).
- Nucleotide Reference sequnce (Ref).
- Query file (FASTA formated).
- Maximum number of BLAST hits in a group.
- Minimum number of gene hits per contig. 
- Output file name.
- *k-mer* size for sequence similarity plot.

After downloading the binary file **ReGSP**, from the file location path: execute the following in your terminal.
```
./REGSP [CDS] [Ref] [Query] [#max BlAST hits] [#min gene hits ] [Output] [k-mer]
 ```

> The binary package **ReGSP** should be allowed to be executed as a program file. If it doesn't execute the first time, please *allow executing file as program*.
`chmod +x /path/ReGSP`

#### Dependencies 

ReGSP needs the following programs to be installed on your computer.

1. BLAST from [NCBI](https://ftp.ncbi.nlm.nih.gov/blast/executables/blast+/) (preferably BLAST 2.6+).
2. MUMmer 3. Can be found [here.](http://mummer.sourceforge.net/).

###
### Sample
Sample files for chloroplast genome analysis of *Heterosigma akashiwo* are provided inside `/sample/`

Five algae species are selected from the Bacillariophyceae (Diatoms), Eustigmatophyceae clade of kingdom Chromista and additional two species from Stylonematophyceae and Cyanidiophyceae clade of Plante kingdom to be used as references. They are *Haslea silbo, Seminavis robusta, Nannochloropsis limnetica, Bangiopsis subsimplex*, and *Cyanidium caldarium*.

##### Files
- `References_CDS.fasta` - amino acid CDS of the five references separated by '****'.
- `References_nucleotide.fasta` - FASTA formated nucleotide sequence of the five references.
- `H-akashiwo_complete.fasta` - complete chloroplast genome of *Heterosigma akashiwo*, used as a query sequence.



The overall workflow and detailed explanation about input files can be found at [ReGSP home page.](https://ds.mju.ac.kr/regsp/#/intro)
