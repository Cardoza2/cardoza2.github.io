---
title: "PIV.jl"
excerpt: "A collection of methods for conducting particle image velocimetry using Julia.<br/><video src='/images/imageset_10_dual.mp4' autoplay loop muted playsinline style='max-width:100%;'></video>"
collection: portfolio
order: 30
---

<video src="/images/imageset_10_dual.mp4" autoplay loop muted playsinline style="max-width:100%;"></video>

A simple PIV processing package in Julia that I wrote for my experimental fluids class. 

Note that the package is still under development. Currently there are 3 correlation methods:
1. Direct
2. Minimum Quadratic Difference (MQD)
3. Fast Fourier Transform (FFT)

Additional features include:
- Sub-pixel displacement (a 5 point Gaussian fit)
- A pre-processing contrast filter
- Some vector validation techniques:
  - Mean value test
  - median test using 8 neigbors
  - ratio of correlation peaks. 
- Vector replacement
  - 8 neighbor average
  - Decimation
- Vorticity calculations. Derivatives will be calculated by:
  - Central Difference
  - 8 point circulation using trapezoidal integration. 
  - Richardson Extrapolation
- Image set analysis

Features under development:
- Image set averaging

- **Code:** [github.com/Cardoza2/PIV.jl](https://github.com/Cardoza2/PIV.jl)

The astute experimentalist will note that the animation above has some regions of non-physical flow on the aft side of the airfoil. While the leading edge vortices may contribute some reversal of flow, the main mechanism at play is those vortices had a lower density of hydrogen bubbles so the FFT algorithm predicted lower velocities in the region. The vortices pushed the incoming hydrogen bubbles away and dispersed them quicker than the rest flow. With fewer hydrogen bubbles, it is significantly more difficult to track particles from image to image. A special thanks to the BYU Photography department for helping with the lighting setup and high-speed photography (and epic water tunnel photos). 