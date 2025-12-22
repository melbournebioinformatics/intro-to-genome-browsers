---
title: "UCSC Genome Browser: Gene expression data"
teaching: 34
exercises: 6
---

:::::::::::::::::::::::::::::::::::::: questions 

- How can we explore gene expression data in the UCSC genome browser?

::::::::::::::::::::::::::::::::::::::::::::::::

::::::::::::::::::::::::::::::::::::: objectives

Use the UCSC gene browser to:

- Compare a region of one genome to genomes of other species
- Determine the tissue/cell type expression profiles of a gene of interest in mouse and human expression data

::::::::::::::::::::::::::::::::::::::::::::::::

![](episodes/fig/06geneexpression_coverage_plot.png)

## Viewing GTEx data in the UCSC Genome Browser

Human tissue specific expression data from the [GTEX project](https://gtexportal.org/home/) 
is available in the UCSC genome browser.

1. Gene level expression data from `GTEx Gene V8` donors can be turned on from the 
blue bar under `Expression`. These are displayed as coloured bar plots.

2. Transcript level expression data is available by turning on `GTEx Transcript` under the same
blue bar. This is also displayed as bar plots.

3. Transcript level expression data for GTEx V6 is also available as coverage plots.
    a. `Toolbar  >  My data  >  Track Hubs  `
    b. Scroll down to `GTEx RNA-seq Signal Hub`. Select `hg38`
  
  ![](episodes/fig/06geneexpression_trackhubs_GTEx.png)
  
#### Default settings

By default, all the available data from one individual only is loaded. Data from other subjects 
in the study can be loaded as desired. For example, you could load all available samples for one tissue region only.

The data is *autoscale to data view* with a track height or 12 pixels for each samples. 
You can change the height of the track or add a data transformation.

As usual, you can right click on the grey bar on the left hand side to configure the track set. 

  ![](episodes/fig/06geneexpression_GTEx_V6_settings.png)
  
<br>

### Your task

1. Using the selection matrix for female donors aged 20-49 years, deselect the default samples 
and select only Brain cortex and Pancreas samples. 

2. Navigate to the location for the gene *MYRF*. You can increase the height of the datatrack to improve visualisation.

::: challenge

## CHALLENGE 1

Can you locate an exon in the MYRF gene that is present in transcripts expressed in the brain but not in the pancreas?

:::

::: challenge

## CHALLENGE 2

Does this alternative splicing event result in a frame shift of the coding sequence?

:::

::: challenge

## CHALLENGE 3

How many amino acids are there in the protein products for each MYRF transcript?

:::

## FACS data

The FACS derived data from the [Tabula Muris](https://tabula-muris.ds.czbiohub.org/) cell type data can be visualised as a coverage plot.

<br>

### Your task

1. Navigate back to the *NTRK2* gene in the human genome. Navigate to the Ntrk2 gene in the mouse genome via  `Toolbar  >  View  >  In Other Genomes (Convert) `
  
2. Under `New Genome` select `Mouse`, under `New Assembly` select `GRC38/mm10`, then click `Submit`

3. Select the region with the greatest homology

4. Click on the bar chart icon for the Tabula muris data in the default view to see a summary bar chart of the cell type data.

![](episodes/fig/06geneexpression_TabMurisbarchart.png)

5. To see a coverage plot of the expression data, we have to configure the Tabula Muris track.
    a. Right click on the grey bar to `Configure Tabula Muris track set`
    b. Hide `Cell expression`
    c. Select `Genome coverage` to full
    d. Select `submit`
  
  This can look a bit overwhelming as there are many tracks and the default track height is set very high, 
  but it is easy to simplify it by focusing on a few cell types of interest.

6. Right click on the grey bar to `configure Genome Coverage track set`
    a. Change `Track height` to 30 pixels
    b. for `Data view scaling` select `group auto-scale`
    c. `Hide All`  subtracks and then manually select only these few cell types of interest:
          - astrocyte Cv
          - Bergmann glial Cv
          - microglia Cv
          - neuron Cv
          - oligodendrocyte Cv
          - OPC Cv
    d. `Submit`

::: challenge

## CHALLENGE 4

Which cell type has the highest level expression of Ntrk2 in this dataset?

:::

7. Go back to the configuration page to change `Data view scaling` to `auto-scale to data view` and `Submit`

8. Export a PDF image of the genome view:  `Toolbar  >  View  >  PDF  `  select  `Download the current browser graphic in PDF`
  
  ![](episodes/fig/06geneexpression_mm10_Ntrk2.png)
  
::: challenge

## CHALLENGE 5

Which cell type(s) express the long and short transcripts of Ntrk2?

:::

## Linnarsson lab data

Mouse CNS cell type expression data can also be validated using an independent single cell 
dataset of mouse cortex from the [Linnarsson lab](http://linnarssonlab.org/).

The data that is publicly available for viewing in the UCCS genome browser is not housed in the UCSC genome browser. 
You must first access it from the the Linnarsson lab data page.

This RNAseq data is stranded, meaning you can see if the transcript data is from the + or - strand.

### Your task

1. Click [here](http://linnarssonlab.org/cortex/) for the Linnarsson lab public data page for this dataset where you can search for cell expression profiles for individual genes.

2. Click on the `Browse the genome` blue text near the bottom of the page.
  
    This loads 18 different tracks, one for each cell type investigated. The default setting 
    for expression range is quite high and most gene expression is not observed with these settings. 
    Each track must be configured individually rather than as a group, which takes a lot of time. 
  
    We previously created a version of this data where each track is 
    autoscaled which can make it quicker to determine which expression range would be ideal for visualising 
    the expression of an individual gene. The session is illustrated in the screen shot below. 
    Note that the data is also viewed using ‘Multi-Region’ which hides the introns in the gene models. 
  
![Linnarsson lab mouse cortex single cell data as autoscaled datatracks](episodes/fig/06geneexpression_linnarsson_ntrk2.png)

::: challenge

## CHALLENGE 6

Select two or three cell types in your session and adjust the scale to best reflect differences in gene expression of Ntrk2 between these cells. 

Save this session and share it.

:::

<br> 

::::::::::::::::::::::::::::::::::::: keypoints 

- The UCSC genome browser allows you to compare gene expression data from multiple different sources and species

::::::::::::::::::::::::::::::::::::::::::::::::

