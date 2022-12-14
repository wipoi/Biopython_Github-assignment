# **Biopython and Github assignment**
Here are command lines for the *Biopython* assignment of the  *BVG-7003* course.  

## Prior requiered steps   
>Biopython **must** be installed before running scripts in this repository, for example running:  
> `python3 pip install biopython` 
>  
> Installation can be verified using the following command:  
> ``` 
> python3  
> >>>import Bio  
> >>>quit()
> ```  
> If no warnings are obtained, we are good to go!  

## Reading Sequence Files in Biopython  
### count_fasta.py  
>This script counts the record in *NC_000913.faa* file.  
>The result is:  
>`There were 4140 records in file NC_000913.faa`

### count_record.py  
>This script prints all the 4140 ID of *NC_000913.faa* file and their associated length.  
>The result is in the *out_count_record.txt* text file.

## Checking proteins start with methionine  
### check_start_met.py
>This script counts how many protein sequences do not start by a *methionine*.  
>The result is:  
>`Found 0 records in NC_000913.faa which did not start with M`  
>This result shows that all protein sequences in *NC_000913.faa* begin with a methionine (M).  

### check_start_met_1.py
>This script prints all the protein sequences ID of *PGSC_DM_v3.4_pep_representative.fasta* file with their first amino acid using the standard IUPAC single letter amino acid code. Printed results are save in the *out_check_start_met_1 text file*.  
>It also counts the protein sequences that do not begin with a methionin. The result is:   
>`Found 208 records in PGSC_DM_v3.4_pep_representative.fasta which did not start with M`  

## Converting a sequence file  
### convert.py  
>This script converts *.gbk* (Genbank) files in *fasta* files using the convert() method.  
>Applied to *"NC_000913.gbk* file, it generates a *NC_000913_converted.fasta* file.  
>It also counts the number of converted files, herein, one have been converted:  
>`1 records converted`  

## Filtering a sequence file  
### filter.py  
>This script writes protein sequences egal or bigger than 100 amino acids long of the *NC_000913.faa* file in the *NC_000913_long_only.faa* file using the write() method.  
>It also prints the number of retained sequences among all:  
>`3720 records selected out of 4140`  

### filter1.1.py  
>This script doesn't work since no *output_handle* local object have been defined in it:  
>``` 
>Traceback (most recent call last):
>   File "filter1.1.py", line 12, in <module>
>        SeqIO.write(record, output_handle, "fasta")
>NameError: name 'output_handle' is not defined
>```  

## Editing sequences  
### edit.py  
>This script removes the last letter (the asterix) at the end of each of the protein sequences in *PGSC_DM_v3.4_pep_representative.fasta* file and put the troncated sequences in the *PGSC_DM_v3.4_pep_rep_no_stars.fasta* file.

## Working with Sequence Features  
### filter_2.py  
>This script selects records of type *CDS* in *NC_000913.gbk* and makes a file named *NC_000913_cds.fasta* that contains a feature_name (herein *locus_tag*) and the sequence for each records.  
>It also counts the number of CDS sequences extracted:  
>`4319 CDS sequences extracted`  

### total_gene_lengths.py  
>This script selects *gene* type features in *NC_000913.gbk* and calculates the total length including all genes.  
>It gives the following results:  
>`Total length of all genes is 4137209`  

## Phylogenetics with Bio-Phylo  
### simple.dnd  
>A Newick file containing phylogenetic groups.  
  
### phylo.py  
>This script uses *phylo.read* to generate a phylogenetic tree with the groups of *simple.dnd* file.  
>Result is in *out_phylo* file.  

### phylo2.py  
>This script generates a more convenient phylogenetical tree with *simple.dnd* file using *Phylo.draw_ascii*.  
>Result is in *out_phylo2* file.  

### phylo3.py  
>This script plots the previous phylogenetical tree using *Phylo.draw*.  
>***matplotlib* or *pylab* must be installed to use this script**.  
>Result is in *out_phylo3* file.  
