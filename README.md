# **Biopython and Github assignment**
Here are command lines for the *Biopython* assignment of the  *BVG-7003* course  

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
>This script prints all the 4140 *id* in *NC_000913.faa* file and their associated length.  
>The result is in the *out_count_record.txt* text file

## Checking proteins start with methionine  
### check_start_met.py
>This script counts how many protein sequences does not start by a *methionine*  
>The result is:  
>`Found 0 records in NC_000913.faa which did not start with M`  
>This result shows that all protein sequences in *NC_000913.faa* begin with a methionine (M).  

### check_start_met_1.py
>This script prints all the protein sequences id of *PGSC_DM_v3.4_pep_representative.fasta* file with their first amino acid using the standard IUPAC single letter amino acid code. Printed results are save in the out_check_start_met_1 text file
>It also counts the protein that does not begin with a methionin and report it as:   
>`Found 208 records in PGSC_DM_v3.4_pep_representative.fasta which did not start with M`  

##
