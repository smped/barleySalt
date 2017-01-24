# Expression Data
Download from https://trace.ncbi.nlm.nih.gov/Traces/study/?acc=SRP017703
Put it on `/data/biohub/`

########################################################################################
Also try https://www.ncbi.nlm.nih.gov/sra?linkname=bioproject_sra_all&from_uid=227211 ##
########################################################################################


This is RNA-Seq based on response to salinity.
The original paper is here: http://link.springer.com/article/10.1007/s11738-013-1230-0
They have no reps, but have pooled two seedlings in each condition.
Analysis using DESeq "using the conservative “blind” method to estimate variance despite lack of replicates"

Need to use Ensembl genome build http://plants.ensembl.org/Hordeum_vulgare/Info/Index

The whole point is to get away from Unigene IDs and repeat using ENSEMBL IDs, so we can compare with the DM regions/genes.

Mouni has DMMs as a response to salinity (in allGRanges_H.Rdata)

Need to see the correlation between DE genes & DMMs between experiments
- Need to look for genes within 5kb either side of DMM

# Circos plot
Need some stats (Sliding windows of 4Mb) to assess the relationsip between DMMs and the number of genes in the window, and also the hyper/hypo methylation patterns

Layers for the circos plot are:

- Gene Density & identification of DMMs
- Remove two outler layers from original plot (that took ages)
- Separate hyper-methylation from hypo-methylation