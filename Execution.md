---
layout: page
title: Execution
lc_title: execution
---

Matlab scripts are separated into two folders: `Example`, designed for simple user experience, and `Core/`, which contains the scripts need to run PH.

`Example/` includes two scripts needed to perform the demo:

`Defaults.m`, a script that be can shared by multiple driver scripts. 
`CostaRica.m`, used to generate the example analysis.

# How to run PH example

It is assumed that all users have access to the example Supercatchment: `PHdata/CostaRica/Supercatchments/CostaRicaSupercatchment9.tif`

`Defaults` sets the path for PHtools, Topotoolbox, and all input (PHdata) and output (PHanalysis) data.

`CostaRica.m` runs the complete PH algorithm. It calls the script `RunPH.m`, which performs the following three steps:

## Step 1: Hypsometry of progressive (nested) subcatchments

Traverse upstream from base level to main drainage divide along chains (flowpaths) in supplied DEM Record the modal elevation of the catchment draining to the (progressively higher) position on each chain. 

Create and write .txt file for each flow path: `PHanalysis/ROI/Subcatchments/25mStep`

## Step 2: Progressive Hypomsetric Bench (PHB) Identification

Identify groups of nested subcatchments with similar modal elevation, PHBs.

Create and write .txt file for each PHB: `PHanalysis/ROI/PHBs/AllSupercatchments`.


## Step 3: Generate PHB plot

Read in PHB text files and generate plot of outlet vs. modal elevation for all chains in catchment.

For this example, users can specify file type for a final figure (`outputFigType`) and axes scale (`peakElevationForOutputFig`). 

