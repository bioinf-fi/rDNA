# RNA Assembly Repository
This repository contains datasets for rDNA assembly and analysis.

## Datasets

### Links
- **Whole-genome sequencing (WGS) Dataset:** [WILL BE AVAILABLE SOON][link-wgs]
- **Adaptive sampling (AS) Dataset:** [WILL BE AVAILABLE SOON][link-as]
- **Whole-genome sequencing using high-throughput flow cells (WGS HTFC) Dataset:** [WILL BE AVAILABLE SOON][link-htfc]

[link-wgs]: https://your-link-here.com/wgs
[link-as]: https://your-link-here.com/as
[link-htfc]: https://your-link-here.com/htfc

### Overview of the available datasets

| Dataset | Number of reads | Coverage | \>Q15 (QV) | \>Q30 (QV) | Sequencing Date |
| :--- |:---------------:|:--------:|:----------:|:----------:|:---------------:|
| **WGS** |     14,922      |   27x    |   92.8%    |    0.8%    |  [06/2025](#)   |
| **AS** |     13,774      |   29x    |   92.4%    |    2.1%    |  [08/2025](#)   |
| **WGS HTFC** |     18,569      |   35x    |  96.3%   |    2.3%    |  [11/2025](#)   |
| **WGS + AS** |     28,696      |   56x    |  92.6%   |    1.4%    |        -        |
| **WGS+AS+HTFC** |     47,265      |   91x    |  94.1%   |    1.8%    |        -        |

### Methodology
These datasets were basecalled using a new experimental ONT model called 
**hyperbasecalling**, which offers higher precision compared to the standard SUP 
(Super Accuracy) model. However, please note that this increased precision comes with a 
computational cost, as hyperbasecalling is approximately **10x slower** than SUP.

To identify reads containing rDNA units, we aligned the sequencing data against an **rDNA array** reference
(10x KY962518-ROT reference) using minimap2 version 2.30-r1287. This method outperformed single-unit 
reference mapping (one KY962518-ROT), yielding significantly higher coverage.

## Current rDNA assemblies
Chromosome 14 maternal (active) and paternal (inactive) rDNA arrays.

| maternal rDNA array | paternal rDNA array | 
|:----------|:----------|
| [chr14 maternal](https://public.gi.ucsc.edu/~mcechova/pedigree/assemblies/rDNA/PAN027.rDNA.chr14.maternal.ref.fa) | [chr14 paternal](https://public.gi.ucsc.edu/~mcechova/pedigree/assemblies/rDNA/PAN027.rDNA.chr14.paternal.ref.fa) | 
