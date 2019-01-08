---
layout: page
title: Code
lc_title: Code
---

## Matlab code

The progressive hypsometry algorithm is implemented in `Matlab` and requires `TopoToolbox`
to run. 

The `Matlab` code is archive as a `GitHub` repository at [PHtools](PHtools). 
This repo is very simple: it consists of a [Core/](PHtools/tree/master/Core) folder 
containing the set of scripts needed to peform progressive hypsometry, 
and an [Example/](PHtools/tree/master/Example) folder containing a demo driver script
[CostaRica.m](PHtools/tree/master/Example/CostaRica.m) and a 
[Defaults.m](PHtools/tree/master/Example/Defaults.m) script that can be shared by 
multiple drivers.