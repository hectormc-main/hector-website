---
layout: page
title: Interactive Music Systems
description: >
    "Interactive Music Systems is a hands on programming and design course that explores audio synthesis, musical structure, HCI (human computer interaction), and visual presentation as the ingredients for the creation of engaging real-time interactive musical experiences."
hide_description: false
sitemap: false
---

0. unordered list to be replaced by Hydejack Table Of Contents 
{:toc}
** Check out PSet 4 if nothing else. It's my favorite. PSet 6 close second.
{:.note}

## Overview

How do people interact with music creation/editing software/hardware? That is the class's purpose.

The class provides a technical foundation in: audio scheduling, Numpy, filtering, and Kivy graphics.
Afterwards, design takes center stage as we become intentional towards our target audience and actions we want to facilitate.

This class is famous for having beet taught by [Eran Egozy](https://mta.mit.edu/person/eran-egozy), co-founder of Harmonix (creator of Guitar Hero).
These days it is taught by [Ryaan Ahmed](https://mta.mit.edu/person/ryaan-ahmed) and I am so grateful for that.
I'm sure Egozy is great, but Ryaan is so personable and made the class so engaging.
I'm very grateful I took this class when I did.


## Coursework

All of my coursework is viewable on YouTube and you can see a definite uptick in quality as the year progresses.

### PSet 1 - Audio Mixing and Scheduling

This one doesn't have a video but it was basically create a sine-wave for each note, combine them with mixers, and filter them.
All of this controllable by the user.

### [PSet 2 - Clip Mixer](https://www.youtube.com/watch?v=vl0WqEdLx6c)
Click title for video link
{:.note}

Create a clip mixer with looping, speed, and audio controls.

There are two stretch goals I didn't get to meet:
1. Add a "estimated tempo" field so that the user has a better sense of how to line up the tracks.
2. Mark beats and have an option such that, when enabled and the user clicks play, the clip starts playing at the next beat. (This is quite a bit of work though).

### [PSet 3 - MIDI Player](https://www.youtube.com/watch?v=HKZkQJkTNMo)

Free-form MIDI player.
Simply click circles to have the note playback to you.
You may record your playing and that can be played back to you.

The graphics are ok.
I could not get the circle-sine wave to close properly and that will forever stain this PSet : (

### [PSet 4 - MIDI Player and the Axe](https://www.youtube.com/watch?v=APhUTjueD68)

[The Axe](https://www.youtube.com/watch?v=XzttQw6xbEE) is Harmonix's first piece of commercial software.
The central gimmick is this field tha plays music based on where your mouse is.
{:.note}

The PSet I am most proud of. We abandon keyboard controls in favor of pure mouse.
I think the board looks clean and it feels very responsive.
I really like the simple pulsating of the buttons.

I have two regrets:
1. Not showing which articulation/rhythm is currently active for each MIDI track.
2. Not having the pulsating of the buttons react to articulation and gain.

I remember I got feedback that they wished the pitch of the MIDI instruments modulated based on where the mouse was.
But I'm a big of atonal, achordal, chaotic music; I wouldn't have it any other way.

### [PSet 5 - Leap Harp](https://www.youtube.com/watch?v=sQjRgqUgcqY)

A virtual harp!

There is no keyboard/mouse interaction in this PSet.
This is controlled purely by [Leap Motion Controllers](https://www.ultraleap.com/product/leap-motion-controller/).
It's a camera that tracks where your hand is in space.
Two in fact. This was a partnered PSet.
To take advantage of that, this is a two-player harp; the left harp is an octave down.



### [PSet 6 - Guitar Hero](https://www.youtube.com/watch?v=FMjF2ziGmhc)

Recreated Guitar Hero! Song of choice: Killer Queen.

This took a lot of work.
1. First I annotated Killer Queen in Audacity to have fingerings at the perfect time.
2. Then translating this .txt file into gems (the notes you play in Guitar Hero).
3. Actual game logic
4. Responsive (this was done in Python so can't be wasteful).
5. Graphics

This song shows up in Guitar Hero 1, but I wanted to author my own gems (the notes you play in the game).
I'm very proud of the gems for I find them very natural but challenging.
For this reason, it is my second favorite PSet.

## Final Project
Video coming soon.
{:.note}

I recently played [Before Your Eyes](https://store.steampowered.com/app/1082430/Before_Your_Eyes/).
A game in which time moves forward when you blinking.

As this was a class interactivity with music, I decided to make blinking the central focus.
I had ambitions of purely eye-based interaction, but that proved difficult so this is controlled with the [Leap](https://www.ultraleap.com/product/leap-motion-controller/).

The project consisted of scenes.
Each scene had object that changes the music is interesting ways.
Blinking on the sky could cause rain to fall.
Clicking on trees could add a soft muffle/rustle to the tracks.
We even had bioluminescent plants that would light-up to the beat of the music.
Note that we did not label the music, peak-detection algorithm was responsible for beat-detection.

When you satisfy certain criteria, an object would spawn that would take you to the next scene when interacted with.

At the moment, there is no video as this PSet was actually showcased to the entire school and anyone could come up to try it.
A video will be up shortly.
