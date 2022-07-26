---
author: Robin Truax
categories:
- Design
date: "2022-07-26"
draft: false
excerpt: "`exparrows` is a simple LaTeX package that allows one to easily insert customizable arrows pointing to parts of your equations. Adapted from Sibin Mohan's [examples](https://twitter.com/sibinmohan/status/1480583840858996743) on Twitter, `exparrows` can improve the readability of long equations by clarifying the role of each term in the equation with a colorful annotation."
layout: single
links:
- icon: book
  icon_pack: fas
  name: Documentation
  url: https://github.com/RobinTruax/exparrows/blob/main/exparrows-documentation.pdf
- icon: github
  icon_pack: fab
  name: Download
  url: https://github.com/RobinTruax/exparrows/blob/main/exparrows.sty
subtitle: A simple LaTeX package for improving readability and accessibility in complex math equations.
tags:
- hugo-site
title: "exparrows: a LaTeX package"
---

## `exparrows` makes it easier for readers to understand complicated equations.

---

`exparrows` is a simple LaTeX package that allows one to easily insert customizable arrows pointing to parts of your equations. Adapted from Sibin Mohan's [examples](https://twitter.com/sibinmohan/status/1480583840858996743) on Twitter, `exparrows` can improve the readability of long equations by clarifying the role of each term in the equation with a colorful annotation. `exparrows` allows one to create arrows with many customization options: whether or not they point to one or two places in the code, the direction and color of the arrows, etc. 

### An Example

Consider the following equation, which gives a recursive definition for a logical formula that succintly (in the sense that it has polynomial length in *k*) checks whether or not a Turing machine reaches state *d* from state *c* in at most 2<sup>*k*</sup> steps: 

{{< figure src="equation-no-exparrows.png" alt="An equation which does not use expositionary arrows." caption="An equation which does not use expositionary arrows." >}}

This formula is correct, but it's hard to understand why without spending a few minutes puzzling over why. To ease this process, one can add expositionary arrows using the `exparrows` package that explain the role of each term in the formula.

{{< figure src="equation-with-exparrows.png" alt="An equation using expositionary arrows for clarity." caption="An equation using expositionary arrows for clarity." >}}

This second option is far easier to understand, improving readability and accessibility.

### Documentation

The documentation for `exparrows` is available [here](https://github.com/RobinTruax/exparrows/blob/main/exparrows-documentation.pdf) (and the TeX for that documentation is available [here](https://github.com/RobinTruax/exparrows/blob/main/exparrows-documentation.tex)).

### Code

The code for `exparrows` is available [here](https://github.com/RobinTruax/exparrows/blob/main/exparrows.sty).

### Attribution

All credit for the idea goes to Sibin Mohan [here](https://twitter.com/sibinmohan/status/1480583840858996743); all I did was reorganize the code so that those less familiar with TikZ would have an easier time using his examples (and those familiar with TikZ reproduce the results more quickly and efficiently).
