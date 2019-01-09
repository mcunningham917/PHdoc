---
layout: page
title: Execution
lc_title: execution
---

Matlab scripts are separated into two folders: [`Example/`](https://github.com/mcunningham917/PHtools/tree/master/Example), designed for simple user experience, and [`Core/`](https://github.com/mcunningham917/PHtools/tree/master/Core), which contains the scripts need to run PH.

[`Example/`](https://github.com/mcunningham917/PHtools/tree/master/Example) includes two scripts needed to perform the demo:

[`Defaults.m`](https://github.com/mcunningham917/PHtools/blob/master/Example/Defaults.m), a script that be can shared by multiple driver scripts. 
[`CostaRica.m`](https://github.com/mcunningham917/PHtools/blob/master/Example/CostaRica.m), used to generate the example analysis.

# How to run PH example

It is assumed that all users have access to the example Supercatchment: [`PHdata/CostaRica/Supercatchments/CostaRicaSupercatchment9.tif`](https://github.com/mcunningham917/PHdata/tree/master/CostaRica/Supercatchments)

`Defaults` sets the path for PHtools, Topotoolbox, and all input (PHdata) and output (PHanalysis) data.

`CostaRica.m` runs the complete PH algorithm. It calls the script 
[`RunPH.m`](https://github.com/mcunningham917/PHtools/blob/master/Core/RunPH.m), which performs the following three steps:

## Step 1: Hypsometry of progressive (nested) subcatchments

Traverse upstream from base level to main drainage divide along chains (flowpaths) in supplied DEM Record the modal elevation of the catchment draining to the (progressively higher) position on each chain. 

Create and write .txt file for each flow path: [`PHanalysis/ROI/Subcatchments/25mStep`](https://github.com/mcunningham917/PHanalysis/tree/master/CostaRica/Subcatchments/25mStep)

## Step 2: Progressive Hypomsetric Bench (PHB) Identification

Identify groups of nested subcatchments with similar modal elevation, PHBs.

Create and write .txt file for each PHB: [`PHanalysis/ROI/PHBs/AllSupercatchments`](https://github.com/mcunningham917/PHanalysis/tree/master/CostaRica/PHBs/Cusum02_BenchLength3Steps/AllSupercatchments).


## Step 3: Generate PHB plot

Read in PHB text files and generate plot of outlet vs. modal elevation for all chains in catchment.

For this example, users can specify file type for a final figure (`outputFigType`) and axes scale (`peakElevationForOutputFig`). 

