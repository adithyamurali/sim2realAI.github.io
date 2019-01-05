---
layout: post
title: "Welcome!"
date: 2019-01-01 13:32:20 +0300
description: Welcome Post # Add post description (optional)
img:  # Add image post (optional)
---

Welcome to our website! We are indexing the progress on simulations to real world transfer in robot perception and control. Motivated by the recent interest in learning in simulated environments and transferring results to the real world, we believe it is important to consolidate and characterise the progress now in this direction. Physics simulators like [MuJoCo](http://mujoco.org/), [Bullet](https://pybullet.org/wordpress/), [FleX](https://developer.nvidia.com/flex), [PhysX](https://developer.nvidia.com/physx-sdk) and [DART](https://dartsim.github.io/), and 3D rendering engines in [Unity](https://unity3d.com/), [UnrealEngine](https://www.unrealengine.com/en-US/what-is-unreal-engine-4), and Physically Based Rendering [(PBR)](https://www.pbrt.org/) engines have played a substantial role in this progress. Moreover, various well known robotics companies like [Boston Dynamics](https://en.wikipedia.org/wiki/Boston_Dynamics), [Agility Robotics](https://www.therobotreport.com/agility-cassie-bipedal-robot-simulators/), [Kuka Robotics](https://www.kuka.com/en-us/products/robotics-systems/software/simulation-planning-optimization/kuka_sim), [Universal Robotics](https://www.universal-robots.com/plus/software/robodk-simulation-and-offline-programming/) and [SpaceX](https://motherboard.vice.com/en_us/article/ezv79w/spacex-is-using-these-simulations-to-design-the-rocket-thatll-take-us-to-mars) rely heavily on simulations and we believe simulators will continue to be important in helping us design, characterise and develop robots and environments and eventually transferring learned models to the real world.

The real world is often complex and there is a huge cost involved in running experiments. Robots tend to be expensive and break often which can slow down the iteration cycle of research. Furthermore, collecting large scale real world data can be quite labourious as tasks become more and more complex. Simulators on the other hand offer appealing advantages\: 

* **Repeatability** - being able to replay the recorded trajectory with no changes/stochasticity --- resetting the states to exactly the same initial values. This is also very helpful in diagnostics and debugging.
* **Controllability** - being able to control various simulation parameters systematically and understand how they affect the performance of the task. 
* **Scalability** - it is a lot easier to scale a simulation experiment via distributed computing or high performance engineering infrastructure.
* **Efficiency** - simulators can often run much faster than real time. This is an extremely important characteristic and allows for fast iteration cycles in training / learning.
* **Variability** - simulators can allow for collecting large diversity of scenarios.
* **Evaluation** - providing a test bed to benchmark various algorithms and characterise the performance.


However, simulators have their limitations too --- simulating complicated real world phenomenon is still an open research problem. Therefore, it is important to understand various critical aspects of simulations in the context of real world transfer *e.g.* 

* How good are the contact models in a physics engine and what approximations are they making?
* What level of rendering quality do we need to be able to transfer results to real world? 
* What are the strengths and limitations of ensemble methods (*e.g.* domain randomisation)? 
* What can simulators faithfully simulate? What are their limitations?  
* Which simulator, given the parameterisation it uses (*e.g.* [generalised or maximal coordinates](/assets/img/GeneralisedVsMaximal.jpg) [cite](https://www.cc.gatech.edu/classes/AY2014/cs7496_fall/slides/Lagrangian.pdf)), might be more fitting to a given task and which is the fastest?
* How do the simulators implement things behind the scenes? What is the generative model they use? How can that be integrated with model-based methods?   

Keeping this in mind, we thought it might be worth consolidating, characterising, and cataloguing various things related to simulations and offer suggestions and constructive feedback on different simulators, synthetic datasets and the state of the art in simulations to real world transfer. We hope to cover all this via series of summary posts about various datasets and de-facto methods that have shown progress in transfer and occasional tutorials and introductory posts on rendering, physics, robot kinematics and optimisation, and hardware.


## Acknowledgements
We would like to thank Avital Oliver, Balakumar Sundaralingam, David Ha, James Davidson, Jacky Liang, Aravind Rajeswaran, Feryal Behbahani, Lerrel Pinto, Miles Brundage, Pulkit Agrawal, Jan Czarnowski, Karl Van Wyk, Pranav Shyam, Vikash Kumar, Fei Xia, Yevgen Chebotar, Jurgen Leitner and Arsha Nagrani for proofreading and suggestions. We would also like to thank the experts in physics simulations, Emo Todorov, Miles Macklin, Erwin Coumans and Karen Liu --- the developers of MuJoCo, FleX, Bullet and DART respectively --- who have kindly agreed to offer suggestions and directions in future to help us organise the evolving landscape of simulations to real world transfer. 
