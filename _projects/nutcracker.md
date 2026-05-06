---
layout: project
title: Nutcracker
description: Description of a nut cracker
technologies: [statics]
image: /assets/images/nutcracker-fbd.jpg
---

**Part A**

**Problem statement and objective:** To design a nutcracker with the dimensions and geometry to be able to crack a macadamia nut with the average adult max. grip strength. 

<br/>
**Constraints and input parameters** (based on online sources)
<li> Average maximum grip strength: less than 17 kgf </li>
<li> Strength to crack macadamia nut: around 200-250 kgf </li>
<li> Average hand measurement: 7-8 cm depending on sex </li>
<li> Average macadamia size: around 17 mm(small) to 28 mm(larger) </li>

<br/>

**Approach to problem:** 
<li>We will take the upper end of the strength needed to crack the macadamia nut(250kgf) and estimate a lower grip strength on average(15kgf). So, we need a force amplification of 250/15, which is 16.7. </li>

<li>Using the average hand measurement, we will estimate a max between handle distance of around 80 mm, which is 3.149 inches. </li>

<li>The handle length will be around 150 mm, which is 5.9 inches. This seems consistent with most handheld tools of the type, with most being around 6 inches, but varying based on use and design.</li>

Material properties have not been considered.

{:style="text-align:center;"}
![Nutcracker FBD]({{"assets/images/nutcracker-fbd.jpg"|relative_url}}){:style="width:90%"}

After making this full FBD, I made an exploded FBD of the top section labeled ABD, where the exploded forces of the nutcracker were shown.

![Nutcracker exploded FBD]({{"assets/images/nutcracker-exploded-fbd.jpg"|relative_url}}){:style="width:90%"}

With this exploded diagram of the nutcracker, I listed out the summation of moment equation: The sum of the momentum about A is equal to (9)*(F_out) - (150)*(F_in) = 0

As a result, with the F_in being 15kgf, we find that the F_out is equal to 250kgf, which is consistent with what we want our nutcracker to be able to do.

**Usability:** Currently, the design is not super usable because I failed to take into account what a physical nutcracker might actually look like. The front bit and its measurements are too small to actually fit a macadamia nut comfortably. Since I did not consider that my FBDs were not drawn to scale, I did not realize that the macadamia nut was too close to the point of rotation(only 9mm, less than a centimeter away) and was not physically realistic.

Design needs further improvements to be considered usable.

<br/> **Part B**

**Problem statement and objective:** Find the location of maximum elastic deflection, beam design such that the vertical elastic deflection is below 2% of its length and is the most mass efficient

**Assumptions:**
<li>E and I are constant
<li>Loads are only transverse
<li>free ends

![First FBD]({{"assets/images/InitialFBD.jpeg"|relative_url}}){:style="width:90%"}

From part (a), we know that the beam is 150 mm and the section from A to B is 9mm. In this FBD, we re-labeled to A, B, and C. Using the summation of forces in the y direction, we find that the force Ay = 235 kgf in the downward direction. 

![FBD with forces]({{"assets/images/FBDwForces.jpeg"|relative_url}}){:style="width:90%"}

We can use this information to construct a shear diagram. Just right of A, the shear force is -235 kgf. At point B, it jumps up 250 to 15 kgf. At C, it drops -15 to 0 kgf. So, V is less than 0 from A to B and greater than 0 from B to C. 

We can also analyze the moment behavior. The moment decreases from A to B and then increases from B to C.

Because there is a change in curvature and it is a place where the internal force reverses sign, the maximum deflection should occur at or very close to point B.

<br/>To keep deflection under 2 percent of its length, it must be under 3mm. We want to control its deflection while keeping the mass at a minimum. The deflection is proportional to (FL^3)/EI, and the mass is proportional to roAL. As a result we would want to maximize EI/roA. 

For material choice, carbon fiber would have the greatest E/ro, which is (150 G Pa)/600.

For shape, we want to maximize I/A, meaning a thin hollow circular tube is better. This maximizes moment of inertial while keeping the Area low.
