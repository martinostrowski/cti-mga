Martin Ostrowski edited this page on 11 October 2021

# cti-mga
Community trait indices from metagenomes and amplicons

Martin Ostrowski, Mark Brown, Anthony Richardson and Wayne Rochester

The concept and code for deriving community trait-indicies from kernell-weigthed density 
estimations of the realised niches of individual species or strains was devloped in collaboration 
with Mark Brown, Martin Ostrowski, Wayne Rochester and Anthony Richardson. 

## Inputs

1. A sequence, type or species abundance table, samples (rows) by sequences (columns)
2. a corresponding metadata table with samples as rows

## Method overview

resampling of input data to avoid sampling bias

## Outputs 

**Species Temperature Index** is a measure of the peak of the realized niche of an organisms’ (represented by an ASV) for a given environment variable. Calculated as the value corresponding to the peak of the abundance weighted kernel density plot or using the mean of the value of the variable for samples containing the top 4 relative abundances.

**Species thermal range (STR)** is the temperature range for a defined species abundance, here calculated as the difference between the minimum and maximum temperatures where kernel density = ¼ peak height.

**Community temperature/thermal index (CTI)** is the average thermal affinity of the entire assemblage. Calculated as the realised thermal niche of each organism present (STI) weighted by their abundance. 

**Thermal bias (t_bias) CTI - ST** difference between CTI and environmental sea temperature (ST). Thermal bias is positive for assemblages that are composed of taxa displaying temperature affinities higher than the local temperature. Theoretically these assemblages may be preconditioned to higher temperatures and thus display reduced sensitivity to warming. Conversely, thermal bias is negative for assemblages dominated by taxa with a cooler thermal affinity than the local temperature, implying increased sensitivity to warming. 

**Community thermal range (CTR)** is the abundance weighted average width of thermal ranges of all species in the assemblage. This index provides an indication of whether the predominant STRs of the species in the assemblage are broad or narrow.

**Community thermal diversity (CTDiv)**  is the variability of thermal affinities among species in the assemblage, calculated as the abundance weighted standard deviation of  all STIs. Low values of CTDiv correspond to assemblages that are composed of taxa with similar STIs, while higher values of CTDiv reflect an assemblage structure with a wider range of STIs, that is,  composed of both warm and cold-water taxa. 

## References






