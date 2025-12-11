---
layout: project
title: Torque Wrench Optimization
description: Cad/ANSYS project
technologies: [Autodesk Fusion],[ANSYS], [MATLAB]
---

For my Mechanics of Engineering Materials class, we were asked to use ANSYS to analyze a given torque wrench, then write a MATLAB script to optimize the design. We would then run a series of hand calculations and use ANSYS to confirm the newly optimized design. We were looking at specs including stress, strain, deformation, and factor of safety againt brittle failure, crack growth failure, and fatigue faliure.

After running through the given base case, we wrote a script that would determine the best possible material and dimensions of a new design, based off the specs we analyzed in the base case. For the material, we landed on Ti-6Al-4V -- a titanium alloy. This was found to be the most suitable material for this wrench because it has a high ratio of strength relative to its weight. This is a tool at the end of the day, so it is important that it has the strength it needs to complete its tasks without being too heavy for the user to operate throughout a day. It has a high sensitivity due to the balance it has between strength and compliance, so it can be made thinner without compromising on strength compared to materials such as aluminum or steel. So, it is just the best of both worlds and is the ideal material to use for this torque wrench design.

We then determined the best dimensions for this torque, which can be seen below in the CAD rendering. 
<p align="center">
  <img src="assets/images/torque cad w dimensions.jpg" width="300">
</p>

With the CAD model and hand calculations finished, it was then time to put the new design in ANSYS for verification. The loads and boundary conditions can be seen below, and gave the following results:

<p align="center">
  <img src="assets/images/loads and forces for torque wrench.png" width="300"><br>
  <em>Figure 1: Loads and Boundary Conditions used in ANSYS Model</em>
</p>

<p align="center">
  <img src="assets/images/normal elastic strain.png" width="250">
  <img src="assets/images/normal elastic strain closeup.png" width="250"><br>
  <em>Figure 2: Normal Elastic Strain from ANSYS</em>
</p>

<table>
  <tr>
    <td align="center">
      <img src="assets/images/wrench principal stress.png" width="250"><br>
      <em>Figure 3: Principal Stress</em>
    </td>
    <td align="center">
      <img src="assets/images/wrench normal stress.png" width="250"><br>
      <em>Figure 4: Normal Stress</em>
    </td>
  </tr>
</table>

<table>
  <tr>
    <td align="center">
      <img src="assets/images/wrench deflection.png" width="250"><br>
      <em>Figure 5: Deflection</em>
    </td>
    <td align="center">
      <img src="assets/images/wrench strain at strain gauge.png" width="250"><br>
      <em>Figure 6: Strain at strain gauge locations</em>
    </td>
  </tr>
</table>

On the wrench, at a location an inch away from the drive, there was a strain gauge. Due to the nature of the wrench, it was a half-bridge in order to allow for it to fit on the device, but it allowed us to measure the strain in the tool. For the strain gauge itself, we used a small uniaxial foil strain gauge that fits cleanly on the flat side surface of the handle near the high-strain region. A gauge with a 3–5 mm grid length (roughly 6–7 mm long and 2–3 mm wide) works well for this design because it has enough bonded area to capture the strain gradient without being too large for the narrowed geometry. This size also makes it easy to align the grid with the bending direction and leave enough room for good lead attachment. Overall, it gives a reliable reading while fitting into the space allowed by the handle shape. In the end, we recorded a sensitivity of 0.413 mV/V at the location of the strain gauges. 
