# Influence of ocean acidification on Eastern oyster (*Crassostrea virginica*) reproductive tissue

This is a collaboration between the Roberts Lab and Dr. Kathleen Lotterhos's lab at Northeastern University. Her team exposed twelve Eastern oysters, *Crassostrea virginica*, to two different pCO<sub>2</sub> for four weeks at 15ºC during the summer of 2017. Half of the oysters were exposed to 400 µatm (control), and the other half to 2800 µatm. The Lotterhos lab sent gonad samples for MBDSeq to identify if different pCO<sub>2</sub> conditions drive differential methylation patterns. I then prepared samples for bisulfite sequencing. Information about sample preparation and tangential analyses can be found in [the broader project repository](https://github.com/RobertsLab/project-virginica-oa).

**My goal is to identify differentially methylated regions and differentially methylated loci between oysters exposed to ambient and elevated pCO<sub>2</sub> conditions**.

## Objectives

1. Identify differentially methylated regions and loci between samples
2. Characterize gene ontology information associated with differential methylation
3. Create reproducible protocols for anlaysis
4. Produce a written report of findings

## Method Overview

1. Receive sequencing data and trim files as appropriate
2. Align trimmed files to a reference bisulfite genome in `bismark`
3. Isolate differentially methylated loci (DML) and regions (DMR) from alignments in `methylKit`
4. Characterize DML and DMR with `bedtools`
5. Perform a gene enrichment

## Project Timeline

**Week 4**: 
- Start `bismark` alignment on Mox: Protocol can be found [here](https://yaaminiv.github.io/DML-Analysis-Part12/)
- Use different samples to create working `methylKit` protocol. This work was done in a [different Github repository](https://github.com/RobertsLab/project-virginica-oa).
  - Validate analysis parameters in `methylKit` with other samples: Results can be found [here](https://yaaminiv.github.io/DML-Analysis-Part13/)
  - Create protocol for tiling analysis in `methylKit`: Results can be found [here](https://yaaminiv.github.io/DML-Analysis-Part14/)

**Week 5**:

- Added [R Markdown file for `methylKit` analysis](https://github.com/fish546-2018/yaamini-virginica/blob/master/notebooks/2018-11-01-DML-and-DMR-Analysis.ipynb)
- Added [Jupyter notebook for DML and DMR characterization](https://github.com/fish546-2018/yaamini-virginica/blob/master/notebooks/2018-11-01-DML-and-DMR-Analysis.ipynb) 

**Week 6**: 
- Run `methylKit` to identify DML and DMR on samples from Mox with [this R Markdown script](https://github.com/fish546-2018/yaamini-virginica/blob/master/notebooks/2018-11-01-DML-and-DMR-Analysis.ipynb)
- Characterize locations of DML and DMR in [this Jupyter notebook](https://github.com/fish546-2018/yaamini-virginica/blob/master/notebooks/2018-11-01-DML-and-DMR-Analysis.ipynb)

**Week 6**:
- Transposable elements analysis
- Conduct flanking analysis with `bedtools closest`

**Week 7**:
- Perform a gene enrichment
- Plot observed vs. expected CpG coverage and methylation

**Week 8-10**:
- Ensure all analyses are easily reproducible
- Draft a manuscript with findings

## Repository Structure

### [analyses](https://github.com/fish546-2018/yaamini-virginica/tree/master/analyses)

R code and output from multiple analyses. Each analysis will be in its own subdirectory.

- [2018-10-25-MethylKit](https://github.com/fish546-2018/yaamini-virginica/blob/master/analyses/2018-10-25-MethylKit): [R Markdown file](https://github.com/fish546-2018/yaamini-virginica/blob/master/analyses/2018-10-25-MethylKit/2018-10-25-MethylKit.Rmd) and output from `methylKit` identification of DML and DMR.

### [data](https://github.com/fish546-2018/yaamini-virginica/tree/master/data)

Raw data used for project analyses, as well as links to data files.

- [Original sample list from Lotterhos lab](https://github.com/RobertsLab/yaamini-virginica/blob/master/data/OysterTissueInfoSheet_GonadTestRoberts_20171002.xlsx)

### [notebooks](https://github.com/fish546-2018/yaamini-virginica/tree/master/notebooks)

Jupyter notebooks that detail reproducible methods for data analysis.

- [2018-11-01-DML-and-DMR-Analysis.ipynb](https://github.com/fish546-2018/yaamini-virginica/blob/master/notebooks/2018-11-01-DML-and-DMR-Analysis.ipynb): Pipeline for `bedtools` analysis of DML and DMR locations in various genome feature tracks. Includes option to specify variable path names for easy reproducibility.

### [scripts](https://github.com/fish546-2018/yaamini-virginica/tree/master/scripts)

Scripts used for Mox.

- [2018-10-31-Revised-Bismark-Parameters-Samtools](https://github.com/fish546-2018/yaamini-virginica/blob/master/scripts/2018-10-31-Bismark-Revised-Parameters-Samtools.sh): Used to run `bismark` alignment on [MBD-Seq data](http://owl.fish.washington.edu/Athaliana/20180411_trimgalore_10bp_Cvirginica_MBD/). This is an edited version of [2018-10-12-Revised-Bismark-Parameters](https://github.com/fish546-2018/yaamini-virginica/blob/master/scripts/2018-10-12-Bismark-Revised-Parameters.sh) that does not redirect standard error to a new file and includes an explicit path to `bowtie2` and `samtools` in the alignment step.

### [tutorials](https://github.com/fish546-2018/yaamini-virginica/tree/master/tutorials)

Data, notebooks, and analyses from class tutorials.

- [BASH Tutorial in Jupyter Notebook](https://github.com/fish546-2018/yaamini-virginica/tree/master/tutorials/2018-10-09-BLAST-Tutorial)
- [BASH Tutorial in R Markdown](https://github.com/fish546-2018/yaamini-virginica/tree/master/tutorials/2018-10-11-BLAST-Tutorial-in-RMarkdown)
