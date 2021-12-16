### Deregressed EBV
Deregression of EBVs is following [Garrick et al. (2009)](http://gsejournal.biomedcentral.com/articles/10.1186/1297-9686-41-55)  
Part of the script were sourced from [Badke et al. (2014)](http://www.ncbi.nlm.nih.gov/pmc/articles/PMC4059235/)

The deregression R-scripts requires the following parameters and information to run sucessfully  
 1. **trait**: The file containing the EBV and reliability of the trait -- columns = (ID, EBV, reliability)  
 2. **Pedigree**: The file containing the Pedigree information -- columns = (ID, Sire, Dam)  
 3. **genoIDs**: The file containing the IDs of the genotyped individuals  
 4. **dataformat**: Specify if the files are in the directory or it an R-object (options are 'DIR','R-object')  
 5. **h2**: The heritabilty of the trait  
 6. **p.varSNP**: The portion of genetic variance accounted for by marker genotypes  
 7. **outname**: Output filename

## Example run  

 ```R
source("dEBV.R")  
debv <-dEBV(trait="Pheno_trait.txt", Pedigree="Pedigree_info.txt", genoIDs="IDs_genotyped.txt", dataformat="DIR", h2=0.30, p.varSNP=0.50, outname="dereg_example")

```

