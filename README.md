# Influence of ocean acidification on Eastern oyster (*Crassostrea virginica*) reproductive tissue

This is a collaboration between the Roberts Lab and Dr. Kathleen Lotterhos's lab at Northeastern University. Her team exposed twelve Eastern oysters, *Crassostrea virginica*, to two different pCO<sub>2</sub> for four weeks at 15ºC during the summer of 2017. Half of the oysters were exposed to 400 µatm (control), and the other half to 2800 µatm. The Lotterhos lab sent gonad samples for MBDSeq to identify if different pCO<sub>2</sub> conditions drive differential methylation patterns. I then prepared samples for bisulfite sequencing.

**My goal is to identify differentially methylated regions and differentially methylated loci between oysters exposed to ambient and elevated pCO<sub>2</sub> conditions**.

## Objectives

1. Identify differentially methylated regions and loci between samples
2. Characterize gene ontology information associated with differential methylation
3. Create reproducible protocols for anlaysis
4. Produce a written report of findings

## Method Overview

1. Extract DNA and prepare samples for MBD-BSseq
2. Send samples to ZymoResearch for sequencing
3. Receive sequencing data and trim files as appropriate
4. Align trimmed files to a reference bisulfite genome in `bismark`
5. Isolate differentially methylated loci (DMLs) and regions (DMRs) from alignments in `methylKit`
6. Perform a gene enrichment

## Project Timeline

**Week 4**: 
- Start `bismark` alignment on Mox: Protocol can be found [here](https://yaaminiv.github.io/DML-Analysis-Part12/)
- Use different samples to create working `methylKit` protocol. This work was done in a [different Github repository](https://github.com/RobertsLab/project-virginica-oa).
  - Validate analysis parameters in `methylKit` with other samples: Results can be found [here](https://yaaminiv.github.io/DML-Analysis-Part13/)
  - Create protocol for tiling analysis in `methylKit`: Results can be found [here](https://yaaminiv.github.io/DML-Analysis-Part14/)

**Week 5**: 
- Run `methylKit` to identify DMLs and DMRs on samples from Mox

**Week 6**:
- Perform a gene enrichment

## Repository Structure

### [analyses](https://github.com/fish546-2018/yaamini-virginica/tree/master/analyses)

R code and output from multiple analyses. Each analysis will be in its own subdirectory. Empty as of 2018-10-16.

### [data](https://github.com/fish546-2018/yaamini-virginica/tree/master/data)

Raw data used for project analyses, as well as links to data files.

### [notebooks](https://github.com/fish546-2018/yaamini-virginica/tree/master/notebooks)

Jupyter notebooks that detail reproducible methods for data analysis. Empty as of 2018-10-16.

### [scripts](https://github.com/fish546-2018/yaamini-virginica/tree/master/scripts)

Scripts used for Mox.

[2018-10-12-Revised-Bismark-Parameters](https://github.com/fish546-2018/yaamini-virginica/blob/master/scripts/2018-10-12-Bismark-Revised-Parameters.sh): Used to run `bismark` alignment on [MBD-Seq data](http://owl.fish.washington.edu/Athaliana/20180411_trimgalore_10bp_Cvirginica_MBD/).

### [tutorials](https://github.com/fish546-2018/yaamini-virginica/tree/master/tutorials)

Data, notebooks, and analyses from class tutorials.

- [BASH Tutorial in Jupyter Notebook](https://github.com/fish546-2018/yaamini-virginica/tree/master/tutorials/2018-10-09-BLAST-Tutorial)
- [BASH Tutorial in R Markdown](https://github.com/fish546-2018/yaamini-virginica/tree/master/tutorials/2018-10-11-BLAST-Tutorial-in-RMarkdown)
