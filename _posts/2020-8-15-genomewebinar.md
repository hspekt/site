---
layout: post
title: 50+ questions about SCoPE2 answered! 
categories: Research
---

I endeavored to answer all the questions asked during [this GenomeWeb seminar I gave](https://www.genomeweb.com/resources/webinars/affordable-quantitative-single-cell-proteomics-scope2). Thanks to all who attended and to all who asked questions. 

***

## Here we go! 


***

**How do you avoid sample loss in protein level during your sample processing since the carrier is added after sample processing?**

SCoPE2 samples are prepared in 1µL of water to minimize surface adsorption, and future improvements of the approach will certainly involve minimizing the the volume of sample preparation further. Additionally, before adding the cells, the wells are passivated with a mixture of seven purified peptides extremely unlikely to be observed in our sample. This helps mitigates the adsorption of proteins and peptides for all steps in the process.   

**For carrier channel cells, are they an equal aliquot mixture of all other single cell samples?**

Yes. We used 100 cell-equivalents of two cell types (macrophage and monocyte) for a total of 200 cell-equivalents. However, the carrier serves no quantitative purpose, so as long as the proteins of interest are abundant in a subset of cell types, all the cell types need not be included.  


**For TMT reagent, how much do you use for carrier, reference and sample channels?**

When preparing the carrier and reference in bulk before diluting to 200 cell-equivalents, we follow the manufacturer's recommendation. When preparing the sample channels, we add 0.5µL of quarter-strength TMT reagent (diluted 1:4 from the manufacturers recommendation) to 1µL of digested sample.  

**How many proteins can be reliably quantified in a single run?**

The number of quantified proteins depends on your priorities reflected in the method parameters. We identify ~800 proteins per run with 60min active gradient and relatively long (300ms) ion accumulation times. Increasing the gradient length or increasing the isobaric carrier and decreasing ion accumulation times can increase the number of proteins / run.

Reliability of the protein quantitation is best determined by comparing the quantitation of their consitutive peptides. However, not every protein we identify has multiple peptides observed and quantified. We observe 10\% missing data in a given run. 

**Regarding isobaric carryover, can you correct the carryover between single cells? Take the case of one cell that expresses a gene orders of magnitude higher than another cell.**

Theoretically, the expectation is that isotopic impurities in the isobaric tags can be corrected with similar efficacy in SCoPE2 sets and bulk samples, and this expectation is supported by our benchmark experiments. 

**How many runs can be reliably combined? What's the maximum number of cells that can be quantified?**

If all SCoPE sets contain the same reference channel, any number of runs, and thus single cells, can be combined. The reliability of combining samples then becomes a question of not inducing batch effects, which we discussed a bit at [SCP2019](https://www.youtube.com/watch?v=mz6Yq2XSu-8&feature=youtu.be).  

**Have you ever tried label-free MS measurement for single cells since it will rule out potential TMT issues?**

We have not. Our interest lies in analyzing 1000s of single cells, which requires the throughput afforded by mutliplexing. We are interested in improving multiplexing reagents to enable more single cells analyzed per run. 

**Do you do MS3?**

No, though I think thereis no reason the claimed benefits of MS3 would not apply.  We use other approaches for decreasing coisolation, such as optmizing duty cycles to target the apex of the peptide elution, since they do not decrease sensitivity. MS3 result in ions loss and thus decreased ion sampling for quantification. 

**Do you work also with fixed cells? Or just fresh samples?**

In our published work, we have used fresh samples. I briefly tried fixing cells with ethanol, but some part of that process increased peptide loss for me. If anyone has observed differently, please contact me! 

**For a beginner single cell proteomics lab, do you suggest we use 384 well plate? Any advice on how to start this?**

We have had success with 96-well and 384-well plates for sample preparation. We have found the 384-well plates to have significantly less sample loss. 

To start, we suggest preparing a sample with SCoPE-like sample with 100-fold more material in each and every channel. So instead of sorting or placing 1 cell, sort or place 100 cells; instead of sorting or placing 100-200 cells for the carrier, sort or place 10,000-20,000 cells. This can be done in your well-plates of choice just as you would prepare a real single cell set. You can then analyze 1/100th of this sample on your mass spec to see what type of data quality you can expect and if there are areas in your preparation that can be improved (digestion efficiency, labeling efficiency, et cetera). 

**Transcriptomics correlates well with proteomics data are weird, right?**

The degree of correspondence between RNA and protein levels that we measured is a bit lower with that observed with in [some bulk studies](Jovanovich_2015) and comparable to that observed in [other studies](Franks_2017). We found some types of proteins positively correlate with their transcript across cell types, other types show an inverse relationship! [See Supplemental Figures 5 and 6](https://www.biorxiv.org/content/10.1101/665307v3). 

**Do you seal the 384 well plate?**

Yes, see [this video](https://www.youtube.com/watch?v=Eq_s6Jlzfnk) for Ed Emmott's complete walk-through of sample preparation. 

**Does rapidly heating to 90C cause complete evaporation since you are working with 1ul?**

I've only observed loss of volume for some wells around the edge of the 384-well plate, where the foil seal may not be so effective. Heating the lid to 110C may help reduce evaporation. 

**What about reduction/alkylation?**

We do not add reducing or alkylating reagents because they may require removal before LC-MS/MS. Thus, we do not typically observe cysteine-containing peptides. Typically, cysteine containing peptides only make up 10\% of the peptides we observe in typical bulk proteomic samples. 

**In slide#34, did you use TMT 16plex?**

We used both TMT11 and TMT16, as the the TMT16 reagent became available part of the way through this study. We hope to see even higher plex reagents soon! 

**You treat reagents volume less than 1ul and incubated. Didn't they evaporize during incubation time?? I think it will be all dry.**

I thought so too! But we have observed no significant evaporation. The small headspace of the 384-well plates is likely the reason, as well as always heating the lid of the plate to a higher temperature than the incubation temperature.  

**What is your LC-MS/MS length and have you found orbi eclipse helps on single cell proteomics?**

We use a 20cm analytical column (the Aurora / Odyssey series from IonOpticks). We have not used an Orbitrap Eclipse. Robust quantitation requires delivering the maximum number of ions from the single cells. If there are improvements in ion delivery in these new instruments, I expect single cell proteomics quantitation will benefit. 

**Could you comment a bit more on those emerging solutions for manual single cell isolating systems and placing them into 96-well/384-well plates?**

We have experience using the Scienion CellenOne to isolate single cells into 96-well and 384-well plates. I am intrigued by the Namocell Hana, but I have no experience using it.  

**How to get clean trypsin? From Promega?**

Yes! Promega Trypsin Gold produced the fewest auto-digest fragments in our hands. While these fragments are abundant, having only a few of them means only a few short periods of our chromatography will have sample peptides coeluting with them. 

**Have you tried using TMT Pro?**

Yes! We plan to use it exclusively until a higher plex reagent is available (fingers crossed for soon!)

**What trypsin brand do you consider "clean"?**

We found Promega Trypsin Gold produced the fewest auto-digest fragments. However, we have not revisited this question for a few years, so there may be cleaner options available. 

**Have you experience contamination of the chromatograohy tip turning yellow?** 

Never yellow! Cool! We have seen quenched TMT form a lovely blue crystal though. To avoid contaminating the instrument with quenched label, we turn off voltage while it elutes.  

**Can you extract the membranes of single cells?**

I have not tried! We have observed and quantified some membrane proteins in single cells. 

**How much protein do you get at the end of the technique? i.e. how much are you injecting into the MS?**

I think this is a very difficult estimate. We can estimate the number of ions delivered to the orbitrap in a single scan, but this represents a small portion of the ions injected into the MS because the MS only samples a small portion of each individual peptide elution. See Figure 5a in the SCoPE2 manuscript. Additionally, quantifying surface-related losses is difficult (I can't think of a good way to do it). 

**What’s the maximal time delay from flow cytometry to protein digestion is optimal?**

We sort and freeze the cells as quickly as possible given the flow cytometer. This is the first step in the lysis process (which we called mPOP) and is also a good pause point. 

**How do you pool the labeled peptides prior to LC-MS? I mean, do you use an automated system? special syringe? Thanks!**

I use a multichannel pipetman. For a video of this process, see Ed Emmott's talk at SCP2019 [(YouTube link)](https://www.youtube.com/watch?v=Eq_s6Jlzfnk) and join us for another similar talk at SCP2021! 

**How many MS runs is normally needed for one single-cell proteomics experiment when using 16-plex TMT?**

We have plexed 12 single cells into one SCoPE set using 16-plex TMT. The optimal total number of single cells will be a function of the sample you wish to analyze: the cell heterogeneity within and variability of proteins of interest being two major considerations.  

**How to remove the liquid when doing the cell sorting?**

The cell is sorted in minimal volume, ~3nL. 

**Which buffer is used to sort cells? What is the volume added in each single-cell well ?**

The flow cytometry buffer we used was 1x PBS. We sort the single cells into 1uL of liquid in each well. The cell is sorted in a ~3nL droplet. 
**For the PCA analysis of monocytes and macrophages, were the carrier cells mixed cell populations?**

An equal number of monocytes and macrophages were used as an isobaric carrier.  

**Each PSM is based on the b- and y-ions, but each single cell peptide ID is based on only the reporter ions, so are you working on a single cell peptide identification FDR?**

The single cell peptide ID is based on the b- and y-ions. However, most of these b- and y-ions are derived from the isobaric carrier sample. However, the peptide, whether from the isobaric carrier sample or the single cell samples, is the same! The single cell quantitation is based on the reporter ions. 

**Do you add any protease inhibitor in the solution before sorting in the sorting buffer?**

No. 

**I would like to ask how did you handle the missing values?**

We imputed missing values only when the data analysis techniques we wanted to employ (like PCA) required complete data. When this was not required, we ignored the missing values when computing statistics. 

**What will be the protocol with cellulose acetate ?**

I don't remember cellulose acetate coming up, contact me to elaborate! 

**Why not 1536-well format vs 384-well?**

1536 would be preferable due to the smaller well volumes and robotic throughput, but we used 384 due to the limited sorting accuracy (placing the cell in the well) of our sorter. 

**If combining multiple runs, typically what percentage of proteins are identified across all/most of these runs? Or are there only a few reproducibly quantified proteins?**

Across the 1,018 cell data set, we quantified over 2,700 proteins and the average protein, the average protein is identified in at least 213 individual cells. To compute missing values for your protein of interest, check out the peptide or protein level data that we've uploaded in an easy-to-understand format, [here](https://scope2.slavovlab.net/docs/data). 

**I have gotten the ion tansfer tube and column tip dirty with yellowish content after the single TMT samples?**

We too observed the quenched TMT in our samples dirtying the ion transfer tube. We get around this by turning off the spray while the quench TMT eluted and using the sheath gas to blow the droplet that subsequently collected off the tip of the column. 

**Are there specific protein properties that would prevent detection of, or bias towards detection of that particular type?**

Yes, and these are the same properties at play in bulk MS analysis. Data dependent acquisition (DDA) mass spectrometry methods prioritize peptides for analysis by their abundance of their ions in the mass spectrometer. This correlates with being biased towards analyzing more abundant proteins. However, targeted approaches (where the peptide m/z and retention time on the analytical column are known) allow us to pick and choose peptides in a less biased manner.   

**Is it possible to analyze the proteomic pattern of single cells fixed in PFA or other fixatives?**

Any fixative that is compatible with bulk proteomic analysis and flow cytometry should be compatible with the SCoPE2 approach. 

**Compared with single cell RNAseq, are SCOPES2 data variabilities larger?**

Within group variability (ie comparing monocytes to monocytes, macrophages to macrophages) is smaller for SCoPE2 as compared to scRNAseq, as demonstrated by [stronger correlations within a cell type in Figure S3](https://www.biorxiv.org/content/10.1101/665307v3). 

**Can you detect phosphorylation?**

Yes, our preliminary data suggest the isobaric carrier can enable quantifying phosphorylated peptides from single cells, but we have not completely optimized and benchmarked this type of analysis However, most phosphorylation is lowly abundant and will require improving the delivery of ions from single cells to the MS. 

**Do you use a particular buffer?**

We use 1x PBS as the sheath fluid for cell sorting, and triethylammonium bicarbonate pH 8.5 for digestion and labelling. 

**Can phosphorylation or other post-translational modifications be detected?**

Abundant phosphorylation and other post-translational modifications can be detected. We have detected proteins in the top 1/3 of the proteome. However, most phosphorylation is lowly abundant and will require improving the delivery of ions from single cells to the MS. 

**What is the well to use for avoiding evaporation?**

We found that the small headspace in the 384-well plates we use limited evaporation during incubation. 

**Can you repeat how do you pool the samples together after labeling?**

I use a multichannel pipetman. For a video of this process, see Ed Emmott's talk at SCP2019 [(YouTube link)](https://www.youtube.com/watch?v=Eq_s6Jlzfnk) and join us for another similar talk at SCP2021! 

**Is it possible to process single cell recovered in a 96 well plate?**

Yes, however we found that loss of peptides to surface adsorption was greater. 

**The peptides from Waters MassPrep you added will be also labled with TMT. How did you avoid the quantitation interference from these protein mixture?**

The Waters MassPrep peptides tend not to ionize well.  Even so, they were a purified peptide mixture of only a few peptides. This meant that we would (at worst) not be able to analyze other peptides while these eluted. Since our peptides typically eluted in ~10-15s, this meant that less than 2 minutes of our 60 minute active gradient would be spend analyzing those peptides. We considered the benefit of passivating the plastic surfaces worth this cost. We have only ever detected one of the MassPrep peptides using the LC-MS parameters we use for SCoPE2 data acquisition. 

**How many cells do you need to robustly define a cluster?**

This is very dependant on the desired definition of a cluster. 

**Are transcription factors better measureable compared to scRNA-seq? **

We profile a limited number of transcription factors, but we have not yet compared the quality of their quantitation with scRNA-seq data. This is doable with our data, please feel free to reanalyze!

**What's your overlap you observe from cell type to cell type for proteins and how does this compare to RNA overlap of the same cell types?**

Most proteins quantified in monocytes were also quantified in macrophages. I have not done the same analysis yet for the RNA overlap, stay tuned! We observed greater in-group (in-celltype) agreement in the protein data. Please feel free to analyze our data! 

**Are different categories of proteins (membrane, nuclear, receptors, ligands) showing different patterns compared to single cell RNA-seq?**

We observe some gene ontologies correlate positively between the protein and RNA data, while others anticorrelate! 

**Why do you combine sonication and benzonase?**

This approaches are used to degrade nucleic acids and enhance cell disruption and release of molecules. However, we do not combine sonication and benzonase for processing single cells. 

**Are membrane protein degraded by your process?**

We identify and quantify membrane proteins. 

**Are you basing cell type identification on FACS or proteomics data?**

Cluster was done without knowledge of cell type. However, the monocyte and macrophage samples were sorted separately, so we were able to trace back the identity of every single cell. 

**What about extra volume from cell sorting?**

Sorting adds ~3nL of sheath fluid. This is <0.3% of the lysis and digestion volume. 

**Can you foresee possible droplet-based adaptations emerge? What might be the biggest bottleneck for that?**

I would love to have droplet-based approaches! A big hurdle I see is the incompadibility of PDMS with organic solvent (used in TMT labelling). It dissolves! 