---
layout: page
title: Execution
lc_title: execution
---

Matlab scripts are separated into two folders: `Example`, designed for simple user experience, and `Core/`, which contains the scripts need to run PH.

`Example` includes two scripts needed for to perform the demo:

`Defaults.m`, a script that be can shared by multiple driver scripts. 
`CostaRica.m`, used to generate the example analysis.

# How to run PH example

It is assumed that all users have access to the example Supercatchment: `PHdata/CostaRica/Supercatchments/CostaRicaSupercatchment9.tif`

`Defaults` sets the path for PHtools, Topotoolbox, and all input (PHdata) and output (PHanalysis) data.

`CostaRica.m` runs the complete PH algorithm. It calls the script `RunPH.m`, which performs the following three steps:

## Step 1: Hypsometry of progressive (nested) subcatchments

Traverse upstream along chains (flowpaths) in supplied DEM and record the modal elevation of the catchment draining to (progressively higher) position on stream network.

## Step 2: Progressive Hypomsetric Bench (PHB) Identification

Identify groups of nested subcatchments with similar modal elevation, PHBs.

## Step 3: Generate PHB plot

For this example, users can specify file type for a final figure (`outputFigType`) and axes scale (`peakElevationForOutputFig`). 

# Output

PHtools writes to the data repository, PHanalysis.

## Step 1: 
Folder containing a txt file for each flow path: PHanalysis/ROI/Subcatchments/25mStep 
## Step 2: 
Folder containing a txt file for each PHB: PHanalysis/ROI/PHBs/AllSupercatchments
