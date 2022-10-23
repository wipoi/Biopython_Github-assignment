# **Biopython-commands**
Here are command lines for the *Biopython* assignment of the  *BVG-7003* course  

## Installing Biopython on terminal  

> `python3 pip install biopython`  
> As you can see, python3 have been called before pip since pyhton 2.7 was set by default on my computer.

> Then, I verify if biopython is correctly installed with the commands:  
> `python3`  
> ```   
> import Bio  
> quit()
> ```  
> No warnings, we are good to go!  

## Reading Sequence Files in Biopython

> First, I import the data set and look for more information on it:  
> `python3`  
>  ```
> from Bio import SeqIO  
> help(SeqIO)  
> quit()
> ```

> Then, I look the first lines of the *NC_000913.faa* file:  
> `head NC_000913.faa`  
> 
> And I count the number of lines starting with *^>*:  
> `grep -c "^>" NC_000913.faa`

> Here is another way to count the record with a *for* loop:  
> `python3`  
> ```
> from Bio import SeqIO  
> filename = "NC_000913.faa"  
> count = 0  
> for record in SeqIO.parse(filename, "fasta"):  
>    count = count + 1  
> print("There were " + str(count) + " records in file " + filename)  
> quit()
> ```
>
> We can create a *.py* script:  
> `nano count_fasta.py`  
> 
> And add the previous *for* loop in it:  
> ```
> from Bio import SeqIO  
> filename = "NC_000913.faa"  
> count = 0  
> for record in SeqIO.parse(filename, "fasta"):  
>    count = count + 1  
> print("There were " + str(count) + " records in file " + filename)
> ```
> Then give the execute rigths and run it:  
> ```
> chmod 777 count_fasta.py  
> python3 ./count_fasta.py  
> ```
> 


