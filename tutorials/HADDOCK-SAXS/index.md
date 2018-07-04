---
layout: page
tags: [WeNRM, NRM, SAXS, e-Infrastructure, Structure, Biology, West-Life, EU, EGI, 7framework, Grid]
comments: false
title: How to use SAXS data in scoring HADDOCK decoys 
image:
  feature: banner.png
---

In this tutorial, we will introduce SAXS data and their use in HADDOCKing. This is a scoring exercise, therefore you won’t need to set a new docking run to go over it, rather you will analyze a provided pre-docked run.

#### Table of contents
{:.no_toc}
* table of contents
{:toc}

<br>
<hr>

## 1. Introduction to SAXS data

Small Angle X-Ray Scattering (SAXS) allows the characterization of biomolecular complexes under native conditions. It measures the intensity scattered by a protein sample at low scattering angles. From the scattering profile, size- and shape-related information, such as molecular weight, radius of gyration, maximum molecular dimension and a low-resolution 3D molecular envelope, can be extracted. (For more information on the SAXS data and the tools to interpret it, you can visit the related WeNMR services page.)

To this end, the SAXS information is typically translated into:  

   (i) a molecular envelope, which can guide the construction of ab initio bead models or the docking of individual 3D structures,      

   (ii) a restraining energy term, which can be used to refine structure directly against the SAXS curve (often in combination with orientational NMR restraints)    

   (iii) a scoring term that calculates the discrepancy (Chi-or-χ) between the experimental scattering curve and the back-calculated one from the model. 

In this tutorial we focus on point (iii), we will investigate the information-content of SAXS data and its usefulness in filtering docking decoys.