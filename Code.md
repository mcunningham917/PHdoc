---
layout: page
title: Code
lc_title: Code
---

## Matlab code

The progressive hypsometry algorithm is implemented in 
[`Matlab`](https://www.mathworks.com/products/matlab.html) and requires 
[`TopoToolbox`](https://topotoolbox.wordpress.com/) to run. 
Version R2018b of [`Matlab`](https://www.mathworks.com/products/matlab.html) 
is assumed; other versions are likely to be compatible.
Version 2.0 of [`TopoToolbox`](https://topotoolbox.wordpress.com/) is assumed, but later
versions may be compatible.
The [`Matlab`](https://www.mathworks.com/products/matlab.html) code is archived as a 
[`GitHub`](https://github.com) repository at [PHtools](PHtools). 

This code is very simple: it consists of a 
[`Core/`](https://github.com/mcunningham917/PHtools/tree/master/Core) folder 
containing the set of scripts needed to peform progressive hypsometry, 
and an [`Example/`](https://github.com/mcunningham917/PHtools/tree/master/Example) 
folder containing a demo driver script
[`CostaRica.m`](https://github.com/mcunningham917/PHtools/tree/master/Example/CostaRica.m) 
and a 
[`Defaults.m`](https://github.com/mcunningham917/PHtools/tree/master/Example/Defaults.m) 
script that can be shared by multiple driver scripts.

A full application of the code is archived on a separate repository 
at [`PHanalysis`](PHanalysis) (see [Application](/Application) for more details). 
The data used in this application are archived 
separately on the [`PHdata`](/PHdata) repository 
(see [Data](Data) for more details). 