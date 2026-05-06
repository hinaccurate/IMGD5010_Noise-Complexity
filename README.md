# IMGD5010_Noise-Complexity
An assignment to create and control at least 100 "agents", use randomness or noise to influence agent properties, and add some type of mouse-based interaction that influences the agents.

## Find the Queen
### link to work

[https://editor.p5js.org/hinaccurate/full/_X77EhJDR](https://editor.p5js.org/hinaccurate/full/_X77EhJDR)

### what I tried to create 

A busy hive is being built by at least 200 bees. When the beekeeper (you) want to find the queen, clicking on the hive with the mouse creates another, slightly different-looking bee in a random location: the queen bee. The goal is to find her.

### what's actually there

200 yellow ellipses ("bees") appear to randomly move across the canvas to build a hive. When the mouse is pressed, a "queenbee" appears in antique white, but with the same behavior--it moves around and behind the other bees, but leaves white honeycomb instead of yellow. Since it doesn't match where the mouse presses, it's effectively hidden (like real queens are) until you locate it. This is accomplished by 

1. building two constructors, one for the honeybees and one for the queenbee, using instructions from "Make: Getting Started with p5.js",
2. an array for honeybees (and an array for the one queenbee, because removing the array somehow broke the entire thing),
3. a centered area 400x200 within the canvas that allows room for the hive to expand,
4. a push inside of a mousePressed function to create the queenbee.

### what didn't really work...

What I _really_ wanted to do was create a push that would drop a new, unmoving "queen's daughter" cell inside the hive wherever the mouse clicked, which would have a thicker stroke around the outside and that the regular bees would move around instead of over. The remnants of that code are still inside the submitted sketch (in the form of naming conventions and the doubled arrays). However, when I tried to add collision behavior, the whole thing broke, and when I tried to use push to create multiple queenbees, the unmoving cells appeared... but there'd be one weird moving one that just looked like a color-changed honeybee. I couldn't figure out how to stop the weird one, so I decided to make it a feature instead of a bug--I made the queenbees only a pixel big so they were essentially invisible amongst the other bees, and revised the "interaction" to be about finding the weird bee after it's generated.

The additional weird thing that I don't know how to correct is that the queenbee doesn't seem to actually appear in a random location-- it's always at around the same Y coordinate, though the X coordinate is at least marginally more random. As such, the "game" of finding the queen resolves pretty quickly once you see the pattern. I do wonder if adding a specific collision or physics library would help, which might be an avenue for further experimentation.
