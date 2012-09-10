---
layout: post
title: "Raspberry Pi Project Ideas"
date: 2012-09-09 22:07
comments: true
categories: [hacking, raspberrypi]
---

## What to do?

I finally got an RPi last week.  Still haven't gotten all the memory cards and cables and whatnot I'll need to actually use it, but I'm looking forward to getting hold of all that stuff in the next couple days.  I'm wondering what I'm going to do with it.  Here are my current thoughts.

### Something Simple

The first inclination is to use it as just another computer: a web client driving a public screen, or a media center.  This is boring.  The whole point behind the Raspberry Pi is to make something that can interact with the real world.  Normal Computer Stuff is out.  If it would be better done by a Mac Mini it's not on the cards.

What I need to get started is something very, very simple, but something that uses the GPIO pins on the RPi to interact with the real world in some way.  I can write regular code anywhere, let's do something suited to the hardware.  I figure that input using GPIO is easier than output, so I'm going to make a sampler.

### A Sampler

It's pretty simple.  There appear to be 17 GPIO pins on the RPI that can be used for input or output.  That means I can hook up 17 buttons to them.  Here's the idea:

 * Most sampler boards have a 4x4 grid of pads that are used to play back the current bank of sounds.  They tend to have lots of fancy features like velocity sensitivity, LEDs embedded in the buttons to indicate what sounds are playing, and so on.  I will not have any of that.
 * Clearly I can replicate the 4x4 grid, but that doesn't leave me much in the way of control featuers.  Granted, I have no real idea what I'll end up using this thing for, but let's at least try to make it fully featured.
 * I am a vim user, and I love the idea of modality in interfaces.  Vim uses modal editing to allow every easily accessible key to have a purpose outside of typing a letter, and it ends up being enormously efficient.  So, the 17th button will be the command vs input switch.

 That gives me 16 control buttons and one button to switch between control mode and input mode.  That'll let me set loop points, move between 4 different stored loops, switch between sound banks, etc.

A sampler sounds like a fun, simple enough starting project, so that's what I'm going to go with.  If it ends up being fun enough, I might wire up a control box with nice arcade buttons.
