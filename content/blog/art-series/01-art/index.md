---
date: "2022-07-25"
draft: false
excerpt: "In this piece, there is a grid of pixels in three colors: one representing rock, one representing paper, and one representing scissors. When pixels are mostly surrounded by pixels which \"beat\" them, they switch (so rock mostly surrounded by paper becomes paper, for example). The system evolves but never settles, as waves of rock, paper, and scissors cross the screen. With the right color choices, the result is striking."
subtitle: "GIFs showing the evolution of a thousand rock-paper-scissors games."
title: Rock-Paper-Scissors Automata
weight: 1
---

In this piece, there is a grid of pixels in three colors: one representing rock, one representing paper, and one representing scissors. When at least 3 of the 8 neighbors of any given pixel are the color which "beats" the pixel's color (that is, when the color which beats it has a plurality among its neighbors), the pixel switches to that color. The system, which is randomly initializes, quickly forms a pattern but never settles into a stable configuration: waves of rock, paper, and scissors cross the screen. Here are three representations of this automaton in the colors of the pansexual flag, the bisexual flag, and the trans flag respectively:  

![Rock-Paper-Scissors Automaton in the Colors of the Pan Flag](images/pan_flag.gif)

![Rock-Paper-Scissors Automaton in the Colors of the Bi Flag](images/bi_flag.gif)

![Rock-Paper-Scissors Automaton in the Colors of the Trans Flag](images/trans_flag.gif)
