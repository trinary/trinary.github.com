---
layout: post
title: "Dials and Blogging"
date: 2012-07-14 18:38
comments: true
categories: [ meta, visualization ]
---
#### Hello there!
Once again I'm trying to get in the habit of writing.  I think the only way I'm going to be able to do it is to just start and not worry too much if what I'm writing is particularly groundbreaking.

Information Display
-------------------

I'd like to start with one of my favorite subjects: information visualization and clarity of display.

I was recently asked to implement a dial-style representation of a single data point for a dashboard system I'm working on.  I think I managed to create something that looks ok, but I don't think it's a good way to display a single piece of information.  Let's discuss why.

### What's a Dial?

By dial, I mean a speedometer-type representation of a value, gauge is another accurate name.  You have a circular layout, typically with an indicator pointing from the center to a particular spot on the circle.  By rotating, the indicator points at a different place along the circle and indicates a change in magnitude.

### Why don't I like them?

Dials, because of their round nature, take up a ton of space.  For that budget of display area the viewer gets only a single point of information.  It's difficult to represent any context without making things cluttered.  You can add a reference point (e.g. a historical average), but doing so with another indicator will make it look like a clock and require a legend, using a simple dot on the outside of the dial increases the radius of the whole visualization, and so on.

Furthermore, they are difficult to compare to one another when several are used together.  The indicators for totally different values can be at the same plane, think 9 o'clock vs 3 o'clock on a line of clocks next to each other.

Perhaps most importantly, they don't use any of the typical visual indicators that our brains have been trained to associate with magnitude for a zillion years.  Bar charts are instantly parseable, because we implicitly understand that increased area = increased value.  Distance from a baseline in the case of line or area charts are similarly simple to interpret as enclosing greater area as magnitude increases.  Angular distance from an arbitrary point is a recently invented way to communicate magnitude, and one that is difficult to interpret by comparison.

### What should you use instead?

[Stephen Few's Bullet graphs](https://en.wikipedia.org/wiki/Bullet_graph) are an ideal alternative to the dial if representing a single value (with context) is what you want.  Here's what you get by using them:

  * A magnitude representation that makes instant sense (length)

  * Ranges for status context (good and bad values) that cost very little ink and space

  * An additional indicator for historical context that can be easily understood and compared

  * Easily scannable and comparable sets of charts

  * A layout that makes labels and current value displays easy to add in a pleasing way.  
    For example, if you have long labels you can stack multiple bullets vertically and not force your label text to wrap awkwardly or have to space them too far apart.  You can scan multiple charts and easily understand their ranges relative to one another.

### What's next?

I'm continuing to work on data visualization, I think it's the most fun I've had coding in a long time.  I'm working (quite infrequently) on a system that uses websockets to let browsers subscribe to data from various sources, and when I can I'll add some quality displays of data.  Outside of getting to play with websockets, it's basically an excuse to start using [d3](http://d3js.org/) with websocket data at high frequency and see how it works.

On friday I get to go see [Edward Tufte](https://en.wikipedia.org/wiki/Edward_Tufte) give one of his all-day seminars on data visualization!  I cannot wait, I've been wanting to attend one for years and years.  I'll definitely be writing about the class.
