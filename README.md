# **Biopython-scripts**
Here are scripts for the *Biopython* assignment of the  *BVG-7003* course  

## Installing Biopython on terminal  

> `python3 pip install biopython`  
> As you can see, python3 have been called before pip since pyhton 2.7 was set by default on my computer.

> Then, I verify if biopython is correctly installed with the commands:  
> ```
> python3   
> import Bio  
> quit()
> ```  
> No warnings, we are good to go!  

## Reading Sequence Files in Biopython

> First, I import the data set and look for more information on it:  
> ```
> python3  
> from Bio import SeqIO  
> help(SeqIO)  
> quit()
> ```

> Then, I look the first lines of the *NC_000913.faa* file:  
> `head NC_000913.faa`  
> And I count the number of lines starting with *^>*:  
> `grep -c "^>" NC_000913.faa`





