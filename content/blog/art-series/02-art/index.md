---
date: "2022-07-24"
draft: false
excerpt: Chip-firing is a model in dynamical combinatorics in which chips are passed back and forth along the edges of a graph. In this model, one can construct the ''sandpile group'' of a graph; this group's identities have a beautiful fractal-esque structure which can be visualized for certain types of graphs.
subtitle: "Fractal-esque configurations playing the same role as 0"
title: Identities of Sandpile Groups
weight: 3
---

This section contains the code and images I created depicting the Julia set of a holomorphic extension of the Collatz function. Essentially, the way this works is that I took a holomorphic extension of the Collatz function (which is initially defined on any positive integers *n* to divide *n* by 2 if *n* is even and multiply *n* by 3 and add 1 otherwise). This extended function is given by the following formula:

<img src="images/collatz-function.png" alt="Collatz Function Extended" width=600>

Then, this fractal is given by taking a <a href="https://en.wikipedia.org/wiki/Julia_set">Julia set</a> of this function. A link to the code is <a href="collatz_generator.py" target="_blank">here</a>.

<img src="images/collatz1-edited.png" alt="Collatz Fractal 1" width=600>
<p><br></p>
<img src="images/collatz2-edited.png" alt="Collatz Fractal 2" width=600>
<p><br></p>
<img src="images/collatz3-edited.png" alt="Collatz Fractal 3" width=600>
<p><br></p>