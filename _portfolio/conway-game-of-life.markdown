---
layout: page
title: Conway Game of Life
description: A Code Generation in Game of Life for JavaFX and Java with Maven
img: /assets/img/gol-screenshot.png
date: September 2, 2019
comments: true
---

I read an interesting article about Conway's Game of Life about unique pattern in zero-player game. To interact with Game of Life by creating initial configuration and observing how the shapes evolves, or creating patterns with particular properties.

The rules is as following: 

1. Any live cell with fewer than two live neighbours dies, as if by underpopulation.
2. Any live cell with two or three live neighbours lives on to the next generation.
3. Any live cell with more than three live neighbours dies, as if by overpopulation.
4. Any dead cell with exactly three live neighbours becomes a live cell, as if by reproduction.

The initial pattern constitute the seed of the system. It is possible the generation is short-lived or the evolution could last as long as infinity.

Check out the videos below for building project and running the program!

### Maven Clean Install
<br/>
<video width="100%" controls>
    <source src="{{site.baseurl}}/assets/mp4/mvncleaninstall.mp4" type="video/mp4">
    Your browser does not support the video tag.
</video>
<hr/>
<br/>
### Java Simulator
<br/>
<video width="100%" controls style="border: 1px solid black;">
    <source src="{{site.baseurl}}/assets/mp4/gol-simulator.mp4" type="video/mp4">
    Your browser does not support the video tag.
</video>

Fork and clone my repository at [Conway Game of Life](https://github.com/jmsweb/conway-gol). If there are anything that could be improved, go and create
a pull request for review.