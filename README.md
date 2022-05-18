# Exploring the controls on long-term landscape evolution 

Teaching workbook created as part of a group project at the CSDMS Spring School 2022.

Team members: 
* Alex Lipp, Imperial College London
* Boontigan Kuhasubpasin, UCLA
* Jedidiah Dale, Washington University 
* Marina Ruiz Sanchez-Oro, University of Edinburgh 

## Learning Goals 

This is a modular course which allow students to explore the *long-term* evolution of landscapes using the Stream Power Law and Hillslope Diffusion models. During the course students will 

- Understand how to implement a long-term landscape evolution model in `LandLab`.
- Demonstrate the effects of changing the diffusivity and erodibility parameters on landscape evolution
- Explore the impact of different spatial patterns of uplift 
- Investigate the impact of orographic rainfall on landscape evolution
- Become familiar with the role of different lithological rock strength

## Theory

Sediment diffusion and river incision process are essential tools that control landscape evolution.

Focusing on Sediment diffusion, the landscape evolves according to the equation:

![lagrida_latex_editor(1)](https://user-images.githubusercontent.com/22777013/169076010-1aced4a9-5268-4b05-8131-d3ba6ef3c3c6.png)


where D is a hillslope diffusivity or transport-rate coefficient with dimensions of length squared per time and $z$ is elevation.

For a better understanding of the Sediment diffusion equation, see: 

- [Culling, W. (1963)](https://dx.doi.org/10.1086/626891). _Soil Creep and the Development of Hillside Slopes_. The Journal of Geology 71(2), 127-161.

Focusing on the fluvial erosion process, the landscape evolves according to the equation:

![lagrida_latex_editor(2)](https://user-images.githubusercontent.com/22777013/169076527-8aa9486f-fce4-4697-b837-0af115002c81.png)


where *K_sp* is the erodibility coefficient related with climate and lithology. *m_sp* and *n_sp* are positive exponents. These are usually thought to have the ratio:

![lagrida_latex_editor(4)](https://user-images.githubusercontent.com/22777013/169078313-a9334b1d-3548-4ff2-a5d5-789efeb1442b.png)


*A* is drainage area and *S* is the slope of steepest descent. In *-dz/dx*, *x* is horizontal distance and *z* is elevation. *U* is an externally-applied rock uplift field.

For a great overview of the stream power equation, see: 

- [Whipple and Tucker, 1999](https://agupubs.onlinelibrary.wiley.com/doi/10.1029/1999JB900120) _Dynamics of the stream-power river incision model: Implications for height limits of mountain ranges, landscape response timescales, and research needs_, Journal of Geophysical Research. 

According to the equations, there are several factors controlling surface evolution. In this notebook, we will explore the surface and river evolution as a result of diffusion erosion coefficient, lithology, uplift, and precipitation by using landlab, a Python-based modeling environment.


## Method

In this repository, we use `LandLab`, a Python-based modeling environment, to allow students to understand how the diffusivity and erodibility coefficient, lithology, rock uplift rates, and precipitation all control the surface and river network evolution. 

The major Landlab components that we will use in this notebook include `FlowAccumulator`, `FastscapeEroder`, `LinearDiffuser`, `Lithology`, `LithoLayers`, and `SinkFillerBarnes`.

Click the link below to explore the effect of each factor on long-term landscape evoluion.

**We will explore...**
1. [Changing erosional parameters](https://github.com/csdms-spring-school-2022/rock-water-uplift/blob/main/erosion.ipynb)
![erosion](https://user-images.githubusercontent.com/10188895/168962893-03150963-1759-4601-bba7-574ec03e5426.png)
3. [Uplift pattern](https://github.com/csdms-spring-school-2022/rock-water-uplift/blob/main/uplift.ipynb)
![Uplift](https://user-images.githubusercontent.com/10188895/168959615-c564009d-fa1b-4322-acc9-a19198c83070.png)
3. [Orographic precipitation](https://github.com/csdms-spring-school-2022/rock-water-uplift/blob/main/precipitation.ipynb)
![precipitation](https://user-images.githubusercontent.com/10188895/168962321-9f5f2707-e00d-4117-89d2-4c7ad59ad9dd.png)
4. [Lithology & Sediment Provenance](https://github.com/csdms-spring-school-2022/rock-water-uplift/blob/main/lithology.ipynb)

![provenance](https://user-images.githubusercontent.com/10188895/168963151-605ba3a3-6918-4540-8455-ffe421f8e5d5.png)

5. [Synthesis - All variables at once](https://github.com/csdms-spring-school-2022/rock-water-uplift/blob/main/synthesis.ipynb)

![image](https://user-images.githubusercontent.com/10188895/168928493-5319e647-3668-4463-be5d-b59788fa22fb.png)


This lesson was part of the [Community Surface Dynamics Modeling System ](https://csdms.colorado.edu)(CSDMS) spring school 2022

