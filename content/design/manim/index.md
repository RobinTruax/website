---
author: Robin Truax
categories:
- Design
date: "2022-07-23"
draft: false
excerpt: ManimCE is a Python library that allows for the creation of math animations. Originally developed by Grant Sanderson of [3Blue1Brown](3blue1brown.com) and then transformed by a dedicated community into a more accessible tool, ManimCE can be used to create short animations for use in presentations, full-length explainer videos, and everything in between.
layout: single
links: 
- icon: book
  icon_pack: fas
  name: Documentation
  url: https://docs.manim.community/en/stable/
- icon: download
  icon_pack: fas
  name: Download
  url: https://docs.manim.community/en/stable/installation.html
- icon: download
  icon_pack: fas
  name: Video in Beamer
  url: https://github.com/RobinTruax/embedding-video
subtitle: A programmatic animation tool for visualizing math, and a series of hacky solutions for putting them in math talks.
tags:
- hugo-site
title: "ManimCE + Video in Beamer"
---

### Notes About ManimCE

ManimCE is a Python library that allows for the creation of math animations. Originally developed by Grant Sanderson of [3Blue1Brown](3blue1brown.com) and then transformed by a dedicated community into a more accessible tool, ManimCE can be used to create short animations for use in presentations, full-length explainer videos, and everything in between.

I used Manim to create the animation on my [homepage](/), as well as the video [A Tale of Three Triangles](https://www.youtube.com/watch?v=5nuYD2M2AX8), my entry for the Summer of Math Exposition #1.

<iframe width="560" height="315" src="https://www.youtube.com/embed/5nuYD2M2AX8" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

Following is another animation that I made using Manim for one of my resarch projects. It shows the transformation between a hyperplane arrangement (in this case, a projection of the Shi arrangement for *n* = 3) and a graph encoding the adjacency relations of this arrangement (in this case, it is called the Shi adjacency graph). This is a simple animation, just about 50 lines of code.

<iframe width="560" height="315" src="https://www.youtube.com/embed/NCSb1YVd0ZY" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

Manim has excellent documentation, but my number one piece of advice for using Manim is to join their Discord server (even if you don't usually use the site). It's an incredibly helpful community of the most experienced ManimCE users (including essentially all the developers), and their help channels have come in handy on many occassions. An invite link is given on the documentation site. I am also available to answer most questions (email me, I'll try to respond when I have time), as by now I have tens of thousands of lines of code in experience with the library. 

### Embedding ManimCE Animations in Beamer

I am a strong believer in the idea that now that we have the technology to create animations, they have a place in math exposition, even in formal settings such as conference talks. The above animation in conjunction with the formal definition of the Shi adjacency graph is far more pedagogically effective than the definition alone. Unfortunately, since Beamer is standard for math conference talks, and Beamer produces PDFs, including video requires some special workarounds (which have become harder since the Adobe dropped support for Flash).

There are three options. You can see a demonstration of all of these options [here](https://github.com/RobinTruax/embedding-video).

#### Using a link to a video online (easy).

For this, including the following code: 
```
\begin{figure}
        \centering
        \href{video-link}{\includegraphics[width=\textwidth]{image}}
        \caption{Caption}
        \label{fig:label}
    \end{figure}
```

Here, `video-link` is a link to a video (probably on YouTube), and `image` is an image to be included in the folder as the TeX file when compiling which serves as the thumbnail to click on. This method is not finnicky at all and works everywhere, including in Chrome, as it is simply a hyperlink on an image. However, it breaks immersion, so sometimes another option is better.

#### Using an external video player (medium).

For this, include the following code: 

```
\begin{frame}
    \centering
    \movie[externalviewer]{\includegraphics[width=0.5\textwidth]{image}}{video}
\end{frame}

```

Here, `image` is an image to be included in the folder as the TeX file when compiling, and serves as the thumbnail to click on, and `video` is a video to be included in the same folder as the **finished PDF presentation file when you're presenting**. The only caveat to this method is that it only works in some PDF readers (including Adobe Acrobat but not Chrome). Now, this breaks immersion less, but it still does break it. Furthermore, it can be nice to have the final frame of the video remain on the slide, so that one can keep discussing the result once the animation is done and still seamlessly transition to the next slide. For this, we have the final option.

#### Embedding a video player (hard).

For this, one needs the `embed-video.sty` file available in the demo [here](https://github.com/RobinTruax/embedding-video), which is stolen from the StackExchange answer [here](https://tex.stackexchange.com/questions/516029/media9-is-becoming-obsolete-dec-2020-any-alternatives-for-embedding-video-audio). Include it with `\usepackage{embed-video}`, and then include the following code: 

```
\embedvideo{\includegraphics[page=1, width=\textwidth]{image}}{video}
```

Here, `image` is an image to be included in the folder as the TeX file when compiling, and serves as the thumbnail to click on, and `video` is the video to be included in the same folder as the **TeX file when compiling**. Now, this method does not break immersion, and the final frame of the video remains on the slide, but there are a few caveats to this method.
 - Besides being more annoying to set up, this only works in some PDF viewers, for example Adobe Acrobat. Furthermore, one needs to approve multimedia playback the first time one opens the PDF.
 - Pausing is frustrating. One must double click to make the video fullscreen, and then single click to pause or unpause the video. There are no other controls.
 - To reset the video (so you can play it again), right click the video and select "Disable content" in the pop-up menu which appears. This resets the video to the thumbnail, so you can play it again.