---
layout: post
title:  "MergePDB"
date:   2019-09-01 12:48:04 -0400
categories: projects
---

<li><a href="https://github.com/{{ site.github_username| cgi_escape | escape 
}}/MergePDB"><svg class="svg-icon"><use xlink:href="{{ 
'/assets/minima-social-icons.svg#github' | relative_url }}"></use></svg> <span 
class="username">MergePDB</span></a></li>



While I was at Brookhaven National Laboratory for an internship, I wrote a program to help an xray crystallography researcher better understand the dynamics of a given enzyme. The program 
merges multiple PDB (structure) files based on residue proximity. Specifically, if the deviation of the average position of each main chain and R-chain atom differs by less than a certain 
threshold, that residue is merged. Otherwise, each conformation is kept in a separate chain with split occupancy. A smoothing is also applied so that residues are more likely to be merged if 
they are near other merged residues, and vice versa. This is done to prevent the merging of residues that are coincidentally close, yet are in fact part of a moving structure of the protein. 








