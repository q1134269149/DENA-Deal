# Python Scipts for dealing with the prediction results of DENA  

## **(1) Coverting transcriptome coordinate of m6A sites from DENA to genomic coordinate using `transLoci2GenoLoci_AHCPSM_v1.py` script**  
*Note:*  
Only supporting to eight species (**Arabidopsis thaliana, Homo sapiens, Caenorhabditis elegans, Populus trichocarpa,Saccharomyces cerevisiae, Schizosaccharomyces pombe, Mouse, Zebrefish**) at present.  

```python
python ${path}/transLoci2GenoLoci_AHCPSM_v1.py -s {Species} -g ${path}/Arabidopsis_thaliana.TAIR10.50.gtf -i ${path}/Col0-0_DENA_prediction.tsv -o Col0-0_DENA_prediction_genoCor.txt
```  
  
*Parameters*  
`-s`, '--select', default="Tair10", help="select the species `Tair10, Human38, Celegans101, Pop_tri, S_cerevisiae, S_pombe, Mouse, Zebrefish`, default: Tair10"  
`-g`, '--gtf', required = True, help="the gtf file download from ensembl database"  
`-i`, '--input', required = True, help="DENA prediction containing transcriptome coordinate of m6A sites, including six columns `transid, transLoci, motif, modRN, totalRN, ratio`"  
`-o`, '--output', required = True, help="name of Output file" 

*Notes:*   
`gtf` : please confirm that the GTF annotation is consistent with the transcriptome reference used in DENA in order to ensure the consistence of gene ids and gene names, that is, they are all come from Ensembl database, preferably the same release version.  
