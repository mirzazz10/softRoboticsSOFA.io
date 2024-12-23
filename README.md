  # Soft Robot Grasping Dataset using SOFA framework

## Introduction
Soft robots are flexible robotic systems that can bend and deform. They are advantageous for:
- Increased dexterity
- Better grasping capabilities
- Medical applications

### Types and Modeling of Continuum Robots
- **Intrinsic and Extrinsic** modeling
- **Cosserat Rod**: Continuous structures
- **PCC** and rigid link combinations for beam-like structures
- **FEM Mesh**: General or complex simulations
- **Lumped Mass Structures**
- **Surrogate Models**: Neural networks for approximations

For detailed references, explore:
- [Soft Robotics Review](https://onlinelibrary.wiley.com/doi/full/10.1002/aisy.202200367)
- [HAL Archive](https://hal.science/hal-04334544v1/file/2112.03645.pdf)
- [IEEE Article](https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=10136424)

---

## Tools for Simulation

### Overview of Soft Robotics Tools
- **SOFA**: FEM Mesh simulations
- **SoMo**: Lumped Mass modeling
- **Sorotoki**: FEM Mesh toolkit

### The SOFA Framework
SOFA (Simulation Open Framework Architecture) is an open-source, modular framework specifically designed for physics-based simulations. Initially introduced in 2012 by HAL (French National Archive), SOFA provides a versatile environment for research and development in robotics, biomechanics, and more.

#### Key Features:
- **Root Node and Scene Graph**:
- SOFA organizes simulations into a hierarchical scene graph with a root node, enabling modularity and ease of configuration.
- **Mathematical Modeling and Solvers**:
- Supports advanced solvers for Finite Element Method (FEM), mass-spring systems, and rigid body dynamics to ensure accurate physical simulations.
- **Object Properties and Interactions**:
- Offers tools to define material properties, constraints, and interactions between objects.
- **Plugin Architecture**:
- Extensible with plugins for specialized functionalities like soft robotics, surgical simulation, and real-time interaction.

#### Controlling Interfaces:
- SOFA supports external control through Python scripts and C++ APIs, making it easy to integrate with custom algorithms and controllers.
- Provides prebuilt modules for tasks such as kinematic control, force feedback, and dynamic manipulation, essential for simulating soft robots.

Explore tools:
- [SOFA Framework GitHub](https://github.com/sofa-framework)
- [Sorotoki Code](https://bjcaasenbrood.github.io/SorotokiCode/)
- [SOFA Overview Paper](https://www.lirmm.fr/~gilles/papers/faure_springer12.pdf)

---

## Project Workflow and Dataset

### General Environment Setup
- Simulation of a three-finger cable gripper interacting with objects on a floor
- Tasks: Picking and orienting objects to specific goal positions
- Rotational control embedded in the gripper

### Dataset Design
- **Action Space**: Gripper actions
- **Gripper Configuration**: Positional data
- **Object Types and Positions**: Various geometries

### Logger Details
- Logs actions taken
- Captures scene frames using SOFA

### Docker Image
Quickly explore the project with the pre-built Docker image:
```bash
docker pull mirzarbaig/sofa-application_v3
docker run -it \
  -e DISPLAY=$DISPLAY \
  -v /tmp/.X11-unix:/tmp/.X11-unix \
  --device /dev/dri:/dev/dri \
  mirzarbaig/sofa-application_v3
```

## steps to run inside docker container for adding paths
```bash
cd /home/rahman/sofa/build/bin
./runSofa
```

## Steps to run the Cable gripper module and control the cable gripper 
Click on open file and open the following python script for running the cable gripper module.
```basb
"/home/rahman/ext_plugin_repo/SoftRobots/examples/tutorials/CableGripper/details/step6.py"
0) Run Animate
1) Cntl + arrow direction ----> to translate the gripper
2) Cntl + "+" ----> to close the gripper and "-" to release the gripper
3) Cntl + "C", "A", "5", "6", "7", "8" to rotate the gripper in different directions.
```

### Dataset Link
Access the dataset [here](https://drive.google.com/file/d/1c2X_SopB0AovaBwLmH0h0JhwIudQu1AH/view?usp=drive_link).

---

## Dataset Summary
| Object Type | Count of Trajectories |
|-------------|-----------------------|
| Cube        | 100                   |
| Sphere      | 100                   |

---

## Challenges and Future Work

### Challenges
- Installation and usage of SOFA can be challenging.
- Issues encountered with pneumatic gripper simulations.
- Potential for improvement by adding more objects and enhancing the dataset.

### Future Work
- Utilize the dataset for training policies on grasping and picking objects.
- Extend usage to dexterous in-hand manipulation.
- Explore reinforcement learning support in SOFA ([SofaGym](https://github.com/SofaDefrost/SofaGym)).

### SofaFramework Author Citation
## Citation

The **SOFA Framework** is an open-source simulation framework for multi-physics, used in various fields such as robotics, biomechanics, and computer graphics. For more information, please visit the official website: [SOFA Framework](https://www.sofa-framework.org/).

If you use the SOFA framework in your research or project, please cite the following:

- **SOFA Framework**: [SOFA Framework - Official Website](https://www.sofa-framework.org/)

Additionally, if you're looking for academic papers or more formal citations related to SOFA, you can refer to the following publication:

- **SOFA Framework Paper**: B. Allard, A. Beaucamp, M. Dap, et al., *SOFA: A Multi-Physics Framework for the Simulation of Soft Robots*, International Journal of Robotics Research, 2018.


### Request for the dataset please reach out to 
```bash
Rahman Baig Mirza( rmirza2@asu.edu), Nakul Gopalan( ngopala6@asu.edu), Arizona State University.
```
