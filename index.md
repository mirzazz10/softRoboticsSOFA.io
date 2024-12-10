# Soft Robotics - Applied Project

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
- Introduced in 2012 by HAL
- Features root nodes, scenes, object properties, and advanced mathematical simulations
- Includes controlling interfaces for soft robot simulations

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
docker pull mirzarbaig/sofa_application_v2
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

### Citation
```bash
Rahman Baig Mirza( rmirza2@asu.edu) and Nakul Gopalan( ngopala6@asu.edu), Arizona State University.
```

