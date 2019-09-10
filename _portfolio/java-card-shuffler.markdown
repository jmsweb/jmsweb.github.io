---
layout: page
title: Javax Swing Card Shuffler
description: A Javax Swing application for Card Shuffler 
img: /assets/img/card-shuffler-screenshot.png
comments: true
date: September 9, 2019
---
One day, my friend and I was playing a random game to guess which order the shuffled card will lay out on the table. After repeatedly shuffling cards numerous time, I thought about designing a simple Java program to shuffle the cards automatically for us. That led me to thinking about using unicode to save time drawing the symbols and position on the deck. By using unicode, I eliminate the designing and focus more on logic.

There are several algorithm to randomly sort the deck and I found Fisher-Yates Algorithm efficiently to randomize the remaining cards in the deck. Due to constraints with action listener and hiding and showing deck, I opted to use `Collections.sort()` to improve code readability. Someday, I'll revisit this code to implement different features to maximize the usefulness of this application. 

The code is developed with Javax Swing components as a standalone application. There are two ways to execute the application; double click on card-deck.jar, or run `java -jar card-deck.jar` command. By doing so, the operating system should detect the JVM to load graphical user interface on computer screen. The application cannot be resized, and exit button would exit the application. This is essentially a basic application with two buttons one to reset the card deck and other to shuffle the deck. This application cannot be resized and exit button on top corner would exit the application.

<img src="{{site.baseurl}}/assets/img/card-shuffler-screenshot.png" style="width: 100%"/>

Fork and clone my repository at [Card Shuffler](https://github.com/jmsweb/card-shuffler). If there are anything that could be improved, go  ahead and create a pull request for review.