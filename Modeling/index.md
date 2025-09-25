---
layout: default
title: Modeling
permalink: /modeling/
nav_order: 2
---

# Modeling 

<div style="display: flex; align-items: flex-start; gap: 20px; flex-wrap: wrap;">

  <div style="flex: 1; min-width: 250px;">
    <p>
    This page looks at some of the modeling projects I have done. These projects were motivated by wanting to learn new mathematical techniques, interest in capturing physical phenomena, and learning how to implement numerical techniques. 
    </p>
    <p>
    The pojects found below are:
    </p>
     <ul>
        <li><a href="#CFD">CFD project</a>: A description of the project and the end objective</li>
        <li><a href="#kalmanFilter">Kalman filter</a>: A description of the project and the end objective</li>
     </ul>
    <p>
    Click on a specific project to learn more. Each project has a brief description on what you can find in each one. 
    </p>
  </div>
</div>

---

<!-- # [CFD Project](cfd.html) -->

<div id='CFD' style="display: flex; align-items: center; gap: 20px; flex-wrap: wrap;">

  <!-- Text content -->
  <div style="flex: 1; min-width: 250px;">
    <h1><a href="cfd.html">CFD Project</a></h1>
    <p>
      CFD has always interested me with its combination of physical modeling and numerical integration. With this project, I wanted to see if I could build my own CFD model to test my understanding. Currently, the model is only a 1D model where the user can specify inlet and outlet conditions and enter simple geometries (converging, diverging, converging-diverging). The area is symmetrical along the axial direction. Currently, the model uses ideal gas equations, so it is only valid for fluids that can be modeled as ideal gas.
    </p>
    <p>
      The goal is to eventually expand to 2D, where I can look at more complicated geometries and find the full flow field for the simple geometries used in the 1D model. The current model is written in Python, but C++ will be evaluated for writing the 2D model.
    </p>
  </div>

  <!-- Figure -->
  <figure style="flex: 0 0 50%; min-width: 200px;">
    <img src="/assets/cfd/IntroGeometryAndMach.png" alt="CFD Results" style="width:100%; border-radius:5px;">
    <figcaption style="text-align:center;"><em>Converging-diverging geometry (top) and Mach number results (bottom).</em></figcaption>
  </figure>

</div>

---

<!-- # [Kalman Filter Project](kalmanfilter.html) -->

<div id='kalmanFilter' style="display: flex; align-items: center; gap: 20px; flex-wrap: wrap;">

  <!-- Text content -->
  <div style="flex: 1; min-width: 250px;">
    <h1><a href="kalmanfilter.html">Kalman Filter</a></h1>
    <p>
      This project was motivated by a conversation with a work colleague where we were discussing how a measurement used in engine control was noisy and the control would end up using the model value instead of the measurement. I came across the Kalman filter on a previous project and this seemed like another application where it could be implemented. 
    </p>
    <p>
      Here, I revisit the Kalman filter and build it out to test my understanding of the filter, its derivation, and any practical challenges in practically implementing the filter.
    </p>
    <p>
      I learned a few things about how to better organize this project so hopefully this is a little more clear than the CFD project. Overall, it was cool to experiment with the Kalman filter. It’s clearly a very ingenious idea but it can be challenging to tune (which I get into but don’t explore too too much)
    </p>
  </div>

  <!-- Figure -->
  <figure style="flex: 0 0 50%; min-width: 200px; align-items: center">
    <img src="/assets/kalmanFilter/KalmanFilterBlockDiagram.png" alt="Kalman Filter Block Diagram" style="width:100%; border-radius:5px;">
    <figcaption style="text-align:center;"><em>Kalman Filter Block Diagram.</em></figcaption>
    <img src="/assets/kalmanFilter/FUDS_0degC_80SOC.png" alt="CFD Results" style="width:100%; border-radius:5px;">
    <figcaption style="text-align:center;"><em>Kalman Filter SOC esimation vs Coulomb Counting compared to actual SOC.</em></figcaption>
  </figure>

</div>