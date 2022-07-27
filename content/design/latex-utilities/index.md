---
author: Robin Truax
categories:
- Design
date: "2022-07-24"
draft: false
excerpt: "When creating LaTeX documents, there are a few objects which are particularly annoying to code by hand: graphs, commutative diagrams, tables, etc. In these cases, it's useful to know about online tools or applications which can accelerate the process. This is a continually updated list of useful tools that I've run across."
layout: single
subtitle: All of the most useful tools I've found for LaTeX.
tags:
- hugo-site
title: LaTeX Utilies
---

When creating LaTeX documents, there are a few objects which are particularly annoying to code by hand: graphs, commutative diagrams, tables, etc. In these cases, it's useful to know about online tools or applications which can accelerate the process. This is a continually updated list of useful tools that I've run across.

### DeTeXify

[DeTeXify](https://detexify.kirelabs.org/classify.html) is a tool which recognizes symbols from handwriting. If you ever spot a symbol which you don't know how to use in a paper and are able to recreate it in handwriting, chances are that DeTeXify will recognize it. It's much simpler than Googling, and since DeTeXify gives a list of the most similar options, it also often gives a more complete answer.

{{< figure src="detexifyexample.png" alt="An example use of DeTeXify." caption="An example use of DeTeXify." >}}

### Graphs

In my research, I have often needed to create diagrams of graphs, or of sequences of graphs, or posets of graphs, etc. For this, the usual tool is TikZ. However, TikZ is frustrating to use, so for simple applications I recommend [TikZiT](https://tikzit.github.io/), a GUI interface for generating TikZ code. TikZiT is profoundly easy to use: download and open the app, create a style file with the node and edge styles which you're going to use, and then it's just a matter of clicking. The only pieces of advice that I have are the following answers to questions I'm frequently asked:  
 - Everything about nodes and edges (size, color, shape, etc.) can be changed as a "property" in the style file, so if you think there isn't an option for the modification that you want, look up if there's a keyword for it in TikZ.
 - Everything is tied to nodes, including labels, so if you want a label to be placed a little bit displaced from a node (instead of inside it), create a new invisible node and write your label on that.

{{< figure src="tikzitexample.png" alt="An example use of TikZiT." caption="An example use of TikZiT." >}}

### Commutative Diagrams

There is virtually never a reason to make commutative diagrams by hand. There are two great online tools for making commutative diagrams. The first is [tikzcd-editor](https://tikzcd.yichuanshen.de/), which is barebones but has a great UX experience. If you use it, make sure to import `tikz-cd`. [Quiver](https://q.uiver.app/) has many more features and customization options, but there are two big problems with it which sometimes arise: 
 - As of July 2022, you still cannot make loops.
 - The UX experience is worse in the sense that it takes a few more clicks to do things.
 
For these two reasons, and because I'm usually doing something simple, I tend to prefer tikzcd-editor, but it's a good idea to be aware of both options. 

{{< figure src="tikzcdexample.png" alt="An example use of tikzcd-editor." caption="An example use of tikzcd-editor." >}}

### Tables

Tables are far more customizable than they appear at first, and there are a plethora of options and packages which provide more options. Instead of digging through them, I recommend using an online generator to produce code and then copy/pasting it into your TeX document. I tend to use [tablesgenerator.com](https://www.tablesgenerator.com/) but [latex-tables.com](https://www.latex-tables.com/) is preferred by some.

{{< figure src="tablesgeneratorexample.png" alt="An example use of tablesgenerator.com." caption="An example use of tablesgenerator.com." >}}