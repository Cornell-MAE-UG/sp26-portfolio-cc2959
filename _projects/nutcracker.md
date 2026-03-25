---
layout: project
title: Nutcracker
description: Description of a nut cracker
technologies: [statics]
image: /assets/images/nutcracker-fbd.jpg
---

**Problem statement and objective:** To design a nutcracker with the dimensions and geometry to be able to crack a macadamia nut with the average adult max. grip strength. 

**Constraints and input parameters** (based on online sources)
<li> Average maximum grip strength: less than 17 kgf </li>
<li> Strength to crack macadamia nut: around 200-250 kgf </li>
<li> Average hand measurement: 7-8 cm depending on sex </li>
<li> Average macadamia size: around 17 mm(small) to 28 mm(larger) </li>

**Approach to problem:** 
<li>We will take the upper end of the strength needed to crack the macadamia nut(250kgf) and estimate a lower grip strength on average(15kgf). So, we need a force amplification of 250/15, which is 16.7. </li>

<li>Using the average hand measurement, we will estimate a max between handle distance of around 80 mm, which is 3.149 inches. </li>

<li>The handle length will be around 150 mm, which is 5.9 inches. This seems consistent with most handheld tools of the type, with most being around 6 inches, but varying based on use and design.</li>

Material properties have not been considered.

{:style="text-align:center;"}
![Nutcracker FBD]({{"assets/images/nutcracker-fbd.jpg"|relative_url}}){:style="width:90%"}

After making this full FBD, I made an exploded FBD of the top section labeled ABD, where the exploded forces of the nutcracker were shown.

![Nutcracker exploded FBD]({{"assets/images/nutcracker-exploded-fbd.jpg"|relative_url}}){:style="width:90%"}

With this exploded diagram of the nutcracker, I listed out the summation of moment equation: 
$$\sum M_A=(9)(F_{out})-150(F_{in})=0$$

As a result, with the F_{in} being 15kgf, we find that the $$F_{out}$$ is equal to 250kgf, which is consistent with what we want our nutcracker to be able to do.

**Usability:** Currently, the design is not super usable because I failed to take into account what a physical nutcracker might actually look like. The front bit and its measurements are too small to actually fit a macadamia nut comfortably. Since I did not consider that my FBDs were not drawn to scale, I did not realize that the macadamia nut was too close to the point of rotation(only 9mm, less than a centimeter away) and was not physically realistic.

Design needs further improvements to be considered usable.