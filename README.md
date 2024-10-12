# SBW_DeepLearning
An exploration into the usage of Deep Learning and Machine Learning Algorithms to solve the statically indeterminate structure of a Strut Braced Wing.

**Author**: Devraj Katkoria

**Aeronautical Engineering**

**Imperial College London**


## Usage 

## Problem Definition
The problem aiming to be solved through this study into Strut Braced Wings is solving for the tension force $T$ in the strut, alongside the tip deflection of the wing $\delta_{tip}$ . This problem has been attempted to be solved through various theoretical based methods, inclusive of **force balance** (equilibrium) and the **priniciple of virtual work**. When considering the problem, it can be considered from a 1D or 3D approach with the only key difference being the interaction between the strut and the wing itself as they are indeed two separate bodies being joined together. 

The one solution that does work at the moment is dependent of the usage of Finite Element tools such as ***Abaqus***. Although Finite Element is majorly used in the Aerospace industry due to its ability to handle insanely complex structures, e.g. a wing which would be composed of various rib, stringer, spar and skin structures all interacting with one another, there does not appear to be any currently available tools to assist with the design of an aircraft with a strut braced wing configuration during the conceptual design phase of aircraft design. I personally ran into this struggle when attempting to design a Strut Braced Wing structure for a group design project at university. This tool is primarily useful for this purpose as by evaluating the Tension force, secondary computations can be made, i.e. Shear Force, Bending Moment and Torque Distributions alongside aeroelastic effects analysis by evaluating the expected tip deflection. 

This tool also makes it easier to work in a multi-disciplinary project, for example, for working with the aerodynamics team as any adjustment that would need to be made to the strut, e.g. for drag reduction can be easily planned in the conceptual design phase or alternatively, have a tool available for a quick feasibility study, enhancing communication between the two teams. 

