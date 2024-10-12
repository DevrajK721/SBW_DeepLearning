# SBW_DeepLearning
An exploration into the usage of Deep Learning and Machine Learning Algorithms to solve the statically indeterminate structure of a Strut Braced Wing.

**Author**: Devraj Katkoria

**Imperial College London**


**Aeronautical Engineering**

## Usage 

## The Problem
### Introduction
The objective of this study is to determine the tension force ($T$) in the strut and the tip deflection of the wing ($\delta_{tip}$) in **strut-braced wing** configurations. Traditional analytical approaches to this problem, including **force balance** (equilibrium analysis) and the **principle of virtual work**, have been explored but present significant challenges or severe simplifications taking away from the true accuracy of the problem. The complexity arises due to the interaction between the wing and the strut, which are treated as separate bodies connected to form a structural system. This complexity can be approached from both 1D and 3D perspectives, with the key difference being how the strut-wing interaction is modeled.

While various theoretical methods have been attempted, **finite element analysis** (FEA), particularly through tools like Abaqus, remains the most reliable method currently available for solving this problem. FEA is widely used in the aerospace industry due to its capability to handle intricate and complex structures, such as a wing composed of ribs, stringers, spars, and skins. However, one of the key challenges is that FEA tools are often not suited for use during the conceptual design phase. At this stage of aircraft design, there are limited tools available for evaluating the performance of strut-braced wing configurations. This gap became apparent during a recent group design project where designing a strut-braced wing structure was hindered by the absence of efficient conceptual design tools.

This project aims to address that gap by leveraging **machine learning** (ML) and **deep learning** (DL) algorithms to develop a tool that can assist in the early design stages of a strut-braced wing configuration for an aircraft. By predicting the tension force in the strut, it will enable secondary analyses such as shear force, bending moment, and torque distribution, as well as aeroelastic effects through tip deflection predictions. Such a tool could serve as a valuable resource for conducting feasibility studies and preliminary design evaluations, making it easier to explore different design options rapidly.

Moreover, this tool will facilitate multi-disciplinary collaboration in aerospace projects. For example, by integrating structural analysis with aerodynamic considerations, it becomes simpler to optimize the strut design for both structural performance and drag reduction. The ability to quickly assess design changes at an early stage will streamline communication between teams and enhance the overall design process.

By incorporating modern machine learning techniques into structural analysis, this project aims to push the boundaries of traditional finite element methods and offer a faster, more adaptable solution for conceptual aircraft design. This will not only improve the design of strut-braced wing configurations but also offer a more integrated, efficient workflow for multi-disciplinary engineering teams.

### The Model 
[[INSERT IMAGE HERE]]

### Theory
The bare bones idea of a viable solution would be a tool which can allow a user to input various parameters for their particular strut braced wing configuration to explore the structure in a fast way without having to build a Finite Element model (at least while still in the conceptual design phase). The typical solution arm would be:

**Inputs**
- Cross-Section of the Wing Box at the root $(a, b)$
- Taper Ratio of the wing $(\lambda)$
- Inertia of the Strut Cross-Section $(I_{xx})$
- Wing box Material $(E_{box}, \nu_{strut})$
- Strut Material $(E_{strut}, \nu_{strut})$
- Loading Conditions $(n)$ (The Load Factor)
- Spanwise connection point of the strut $(y_{strut})$
- Chordwise connection point of the strut $(x_{strut})$ (Given as percentage of chord)

**Ouputs**
- **Primary**
  - Tension in the Strut $(T)$
  - Tip Deflection $(\delta_{tip})$
- **Secondary**
  - Shear Force, Bending Moment and Torque Distributions 
  - Aeroelastic Analysis 

Some limitations of this approach (which are mostly insignificant during the design phase) include:
- Failure Analysis Neglected
- Most suitable for metallic structures 

### Implementation 
The implementation of this project involves several intricate steps, which are briefly outlined below:

1. **Automating Model Creation and Job Submission:** Develop an Abaqus scripting framework that automates the construction of finite element models and handles the job submission process, allowing for the generation of a large range of test data.

2. **Data Extraction:** Extract key outputs from the Abaqus analysis, specifically the strut tension and tip deflection, from the generated .odb (output database) files.

3. **Data Preparation:** Format the extracted results into a structured dataset, ready for further processing and analysis in machine learning workflows.

4. **Model Training:** Build and train a variety of machine learning and deep learning models, evaluating their performance based on minimizing a specified loss parameter across all test cases.

5. **Model Selection:** Identify the most optimal model based on performance metrics and select it for use in the final solution.

This workflow combines the strengths of finite element analysis with advanced machine learning techniques to develop a predictive tool for structural analysis of strut-braced wing configurations.

## Contact
Please feel free to contact me with any bugs/issues you face with using this tool or any suggestions you have to improve it!
