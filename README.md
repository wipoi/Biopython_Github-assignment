# **Biopython and Github assignment**
Here are command lines for the *Biopython* assignment of the  *BVG-7003* course  

## Prior requiered steps   
>Biopython must be installed before running scripts in this repository, for example running:  
> `python3 pip install biopython` 
>  
> Installation can be verified using the following command:  
> ``` 
> python3  
> >>>import Bio  
> >>>quit()
> ```  
> If no warnings are obtained, we are good to go!  

## count_fasta.py  
>This script counts the record in *NC_000913.faa* file.  
>The result is:  
>`There were 4140 records in file NC_000913.faa`

## count_record.py  
>This script prints all the 4140 *id* in *NC_000913.faa* file and their associated length.  
>The result is in the object *out_count_record.txt*

## check_start_met.py
>This script counts how many protein sequences does not start by a *methionine*  
>The result is:  
>`Found 0 records in NC_000913.faa which did not start with M`  
>This result shows that all protein sequences in *NC_000913.faa* begins with a methionine (M).  



