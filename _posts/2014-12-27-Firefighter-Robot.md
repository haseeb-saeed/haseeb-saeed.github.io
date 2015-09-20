---
layout: post
title: Firefighter Robot
cover: firefighter/firefighter_art.jpg
date:	2014-12-27
categories: posts
---

The firefighter robot was a robot designed to navigate a maze in order to find and extinguish a fire within the maze.

## The Maze

The maze consisted of white walls on a black floor. The areas that contained the candles (the fire to extinguish), referred to as rooms, contained a white line at their entrances to signifiy that a room had just been entered. The candle was placed in one corner of the room upon a sheet of white paper.

## The Robot


![_config.yml]({{ site.baseurl }}/images/firefighter/firefighter.jpg)

The robot contained various sensors to detect the walls, candle, white lines, and paper.

There was a front wall sensor and a side wall sensor, both consisting of an infrared receiver and emitter. The walls would reflect the infrared rays so the robot could sense when there was a wall in front or to its left. Using the sensors, the robot could navigate the maze by "hugging" the wall.

To detect the fire, the robot contained a single infrared receiver mounted on the top. By detecting the infrared rays emitted by the candle, the robot could determine the position of the candle within the room.

For detecting the white lines and the paper, the robot had a super-bright LED with a receiver mounted perpendicular to the floor. When the robot crossed a white line, the receiver would detect the reflected super-bright LED beam.

## The Approach

<iframe width="420" height="315" src="//www.youtube.com/embed/qodz7AqiURc" frameborder="0" allowfullscreen></iframe>

In it's navigation mode, the robot would wall hug to find its way around the maze. More specifically, the robot would move in a straight line if there was a wall to the left of it and no wall in front of it. If there was no wall to the left, the robot would turn left. If a wall appeared in front of the robot, the robot would turn right.

When a white line was detected on the floor, the robot knew that it had entered a room so it would switch to its scanning mode.

In the scanning mode, the robot would rotate 90 degrees and check the top infrared receiver for any readings. If the receiver indicated nothing and the robot finished its rotation (meaning there was no candle in the room), it would exit the room and swtich back to its navigation mode.

If the robot detected the candle, it would move towards the candle while checking the ground for the paper the candle was placed upon. Once the robot detected the paper, it knew that it was close enough to the candle to extinguish it. It would then stop moving and activate its fan to put out the fire.

![_config.yml]({{ site.baseurl }}/images/firefighter/firefighter_design.png)
