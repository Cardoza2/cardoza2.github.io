---
title: "WATT.jl: Wind Aeroelastic Turbine Toolkit"
excerpt: "A toolkit for nonlinear unsteady aeroelastic modeling of wind turbine blades, specifically designed for derivative computation."
collection: portfolio
order: 10
---

<!-- TODO: This is a TEMPLATE. Copy it, rename the file, and write one per project.
     Delete this example once you have real ones. -->

A toolkit for nonlinear unsteady aeroelastic modeling of wind turbine blades, specifically designed for derivative computation. Our model couples blade element momentum theory ([CCBlade](https://github.com/byuflowlab/CCBlade.jl.git)), a dynamic stall model ([DynamicStallModels](https://github.com/byuflowlab/DynamicStallModels.jl.git)), and geometrically exact beam theory ([GXBeam](https://github.com/byuflowlab/GXBeam.jl.git)). Because it is written in the Julia coding language, it gradient computation is as simple as relying on ForwardDiff.jl or ReverseDiff.jl. 

### Capabilities
- Nonlinear unsteady aerostructural analysis
- AD compatibility
- Nonlinear steady aerostructural analysis


### Overview
The model is based on [OpenFAST](https://github.com/OpenFAST/openfast) from the National Renewable Energy Laboratory. This implementation is not intended to replace OpenFAST, but rather serves as a research platform for rapidly prototyping and evaluating differentiation techniques.

Key differences:
- WATT.jl is compatible with mature algorithmic differentiation packages including ForwardDiff, ReverseDiff, and ImplicitAD. 
- CCBlade uses a slightly different implementation of Brent's method which makes small differences which accumulate overtime. The implementation that CCBlade uses converges to tighter tolerances. 
- GXBeam uses constant property linear elements with extended Milenković parameters. This formulation produces an exceptionally robust solver that avoids excessive quadrature, enabling tight convergence of structural states at each time step.


- **Code:** [github.com/byuflowlab/WATT.jl](https://github.com/byuflowlab/WATT.jl)

