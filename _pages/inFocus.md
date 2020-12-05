---
layout: archive
title: "InFocus"
permalink: /InFocus/
author_profile: false
---

## InFocus: A fast inertial lift calculator in MATLAB

InFocus is an easy-to-use tool that can calculate particle focusing positions in a channel of arbitrary cross section after just a few minutes of computation on a desktop computer.
 The method used draws upon and sharpens asymptotic theory to replace particles by singularities of known sizes.  Read more about the algorithm on The Arxiv.
 
## Download 
 
 [Download Infocus on github](https://github.com/SamuelEChristensen?tab=repositories)

## Examples

% Example (Uniform mesh on a triangle)
pv  [0  0;  1  0;  0.2  1];  %Polygon Vertices
Re = 1;  %Reynolds Number


<p align="center">
  <img align="center" src='/images/schematic_diagram_size_stability_proj2.png' width="50%">
</p>
% Example (Take advantage of symmetry by specifying points and using reflections)
pv = [1  1;  -1  1;  -1  -1;  1  -1];  %Polygon Vertices
Re = 1l  %Reynolds Number



% Example (Define a channel with curved edges)



% Example ()

more complicated stuff 

Work in progress...
