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

Example: Uniform mesh on a triangle
```matlab
pv  [0  0;  1  0;  0.2  1];  %Polygon Vertices
Re = 1;  %Reynolds Number
[xp, v] = findMigrationPolyChannel(pv,Re);
```

<p align="center">
  <img align="center" src='/images/schematic_diagram_size_stability_proj2.png' width="50%">
</p>

Example: Take advantage of symmetry by specifying points and using reflections
```matlab
pv = [-0.5  -0.5; -0.5  0.5; 0.5  0.5;  0.5  -0.5;  -0.5  -0.5];
Re = 1;
fh=@(p) min(0.02+max(0,0.5*drectangle(p, -2, 0, -0.5, 0).^3),0.1);  % custom mesh distance that puts more points in one quadrant
[X,Y] =    meshgrid(-0.5:0.05:0,-0.5:0.05:0);
X = reshape(X,numel(X),1);
Y = reshape(Y,numel(Y),1);
xp = [X,Y]';  %particle testing locations
settings = {'reflectx','reflecty'};  %commands to take advantage of symmetry
[xp,v] = findMigrationPolyChannel(pv, Re, fh, xp, settings)
```


% Example (Define a channel with curved edges)



% Example ()

more complicated stuff 

Work in progress...
