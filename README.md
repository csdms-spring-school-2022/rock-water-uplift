# Exploring the controls on long-term landscape evolution 

![image](https://user-images.githubusercontent.com/10188895/168928493-5319e647-3668-4463-be5d-b59788fa22fb.png)

## Introduction

Sediment diffusion and river incision process are essential tools that control landscape evolution.

Focusing on Sediment diffusion, the landscape evolves according to the equation:

$$\frac{\partial z}{\partial t} = D \nabla^2 z$$.

where D is a hillslope diffusivity or transport-rate coefficient with dimensions of length squared per time and $z$ is elevation.

For a better understanding of the Sediment diffusion equation, see: 

- [Culling, W. (1963)](https://dx.doi.org/10.1086/626891). Soil Creep and the Development of Hillside Slopes. The Journal of Geology 71(2), 127-161.

Focusing on the fluvial erosion process, the landscape evolves according to the equation:

$$\frac{d z}{d t} = -K_\text{sp} A^{m_{sp}} S^{n_{sp}} + U$$.

where $K_{sp}$ is the erodibility coefficient related with climate and lithology. $m_{sp}$ and $n_{sp}$ are positive exponents (usually thought to have a ratio, $m_{sp}/n_{sp} \approx 0.5$). $A$ is drainage area and $S$ is the slope of steepest descent. ($-\frac{dz}{dx}$) where $x$ is horizontal distance and $z$ is elevation. $U$ is an externally-applied rock uplift field.

For a great overview of the stream power equation, see: 

- [Whipple and Tucker, 1999](https://agupubs.onlinelibrary.wiley.com/doi/10.1029/1999JB900120) Dynamics of the stream-power river incision model: Implications for height limits of mountain ranges, landscape response timescales, and research needs, Journal of Geophysical Research. 

According to the equations, there are several factors controlling surface evolution. In this notebook, we will explore the surface and river evolution as a result of diffusion erosion coefficient, lithology, uplift, and precipitation by using landlab, a Python-based modeling environment.

## Method

In this repository, we use `LandLab`, a Python-based modeling environment, to allow students to understand how the diffusivity and erodibility coefficient, lithology, rock uplift rates, and precipitation all control the surface and river network evolution. 

The major Landlab components that we will use in this notebook include `FlowAccumulator`, `FastscapeEroder`, `LinearDiffuser`, `Lithology`, `LithoLayers`, and `SinkFillerBarnes`.

Click the link below to explore the effect of each factor on long-term landscape evoluion.

**We will explore...**
1. [K_sp and D](https://github.com/csdms-spring-school-2022/rock-water-uplift/blob/main/erosion.ipynb)
2. [Uplift rate]()
3. [Precipitation]()
4. [Lithology](https://github.com/csdms-spring-school-2022/rock-water-uplift/blob/main/lithology.ipynb)
5. [Synthesis - All variables at once](https://github.com/csdms-spring-school-2022/rock-water-uplift/blob/main/synthesis.ipynb)

This lesson was part of the CSDMS spring school 2022
</br>
[Community Surface Dynamics Modeling System ](https://csdms.colorado.edu)(CSDMS).
