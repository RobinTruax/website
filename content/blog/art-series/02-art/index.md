---
date: "2022-07-24"
draft: false
excerpt: Chip-firing is a model in dynamical combinatorics in which chips are passed back and forth along the edges of a graph. In this model, one can construct the ''sandpile group'' of a graph; this group's identities have a beautiful fractal-esque structure which can be visualized for certain types of graphs.
subtitle: "Fractal-esque configurations playing the same role as 0"
title: Identities of Sandpile Groups
weight: 3
---

This section displays the identity element of various sandpile groups. Each raster image of size *n* by *n* was considered as a graph by allowing each pixel to be a node and designating one "off-the-image" node. Then, each pixel has four edges to its adjacent pixels -- if a pixel is on the boundary, then it has an edge (or two edges, for corner pixels) to the "off-the-image" node to ensure it genuinely has 4 edges. Due to the computational complexity of this project, it was done in Julia. 


A link to the code is [here](identity_elements.jl).

**Color legend:**
 - Color Scheme 1: Blue (0 grains of sand), Light Blue (1 grain of sand), Yellow (2 grains of sand), Maroon (3 grains of sand).
 - Color Scheme 2: Neon Blue (0 grains of sand), Medium Blue (1 grain of sand), Dark Blue (2 grains of sand), Midnight Blue (3 grains of sand).
 - Color Scheme 3: Neon Pink (0 grains of sand), Light Purple (1 grain of sand), Dark Purple (2 grains of sand), Midnight Blue (3 grains of sand).

<p><b>10x10 Sandpile Identity Elements:</b></p>
<img src="images/id_10_c1.png" alt="Sandpile Identity 10x10 Color Scheme 1" width=180>
<img src="images/id_10_c2.png" alt="Sandpile Identity 10x10 Color Scheme 2" width=180>
<img src="images/id_10_c3.png" alt="Sandpile Identity 10x10 Color Scheme 3" width=180>
<p><br></p>
<p><b>25x25 Sandpile Identity Elements:</b></p>
<img src="images/id_25_c1.png" alt="Sandpile Identity 25x25 Color Scheme 1" width=180>
<img src="images/id_25_c2.png" alt="Sandpile Identity 25x25 Color Scheme 2" width=180>
<img src="images/id_25_c3.png" alt="Sandpile Identity 25x25 Color Scheme 3" width=180>
<p><br></p>
<p><b>50x50 Sandpile Identity Elements:</b></p>
<img src="images/id_50_c1.png" alt="Sandpile Identity 50x50 Color Scheme 1" width=180>
<img src="images/id_50_c2.png" alt="Sandpile Identity 50x50 Color Scheme 2" width=180>
<img src="images/id_50_c3.png" alt="Sandpile Identity 50x50 Color Scheme 3" width=180>
<p><br></p>
<p><b>100x100 Sandpile Identity Elements:</b></p>
<img src="images/id_100_c1.png" alt="Sandpile Identity 100x100 Color Scheme 1" width=500>
<p></p>
<img src="images/id_100_c2.png" alt="Sandpile Identity 100x100 Color Scheme 2" width=500>
<p></p>
<img src="images/id_100_c3.png" alt="Sandpile Identity 100x100 Color Scheme 3" width=500>
<p><br></p>
<p><b>200x200 Sandpile Identity Elements:</b></p>
<img src="images/id_200_c1.png" alt="Sandpile Identity 200x200 Color Scheme 1" width=500>
<p></p>
<img src="images/id_200_c2.png" alt="Sandpile Identity 200x200 Color Scheme 2" width=500>
<p></p>
<img src="images/id_200_c3.png" alt="Sandpile Identity 200x200 Color Scheme 3" width=500>
<p><br></p>
<p><b>500x500 Sandpile Identity Elements:</b></p>
<img src="images/id_500_c1.png" alt="Sandpile Identity 500x500 Color Scheme 1" width=500>
<p></p>
<img src="images/id_500_c2.png" alt="Sandpile Identity 500x500 Color Scheme 2" width=500>
<p></p>
<img src="images/id_500_c3.png" alt="Sandpile Identity 500x500 Color Scheme 3" width=500>
<p><br></p>
<p><b>1000x1000 Sandpile Identity Elements:</b></p>
<img src="images/id_1000_c1.png" alt="Sandpile Identity 1000x1000 Color Scheme 1" width=500>
<p></p>
<img src="images/id_1000_c2.png" alt="Sandpile Identity 1000x1000 Color Scheme 2" width=500>
<p></p>
<img src="images/id_1000_c3.png" alt="Sandpile Identity 1000x1000 Color Scheme 3" width=500>
<p><br></p>
<p><b>2000x2000 Sandpile Identity Elements:</b></p>
<img src="images/id_2000_c1.png" alt="Sandpile Identity 2000x2000 Color Scheme 1" width=500>
<p></p>
<img src="images/id_2000_c2.png" alt="Sandpile Identity 2000x2000 Color Scheme 2" width=500>
<p></p>
<img src="images/id_2000_c3.png" alt="Sandpile Identity 2000x2000 Color Scheme 3" width=500>