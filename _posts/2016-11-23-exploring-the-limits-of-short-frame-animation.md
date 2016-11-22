---
title: Design Patterns for narrow short frame animation
date: '2016-11-23 09:22:38'
layout: post
---
We've had great progress recently technically refining our praxinoscope machinery and now I'm coming back around to animation. Recent exploration has led us to shift from 12 frame animation to 16 frame animation and we have reworked our mirrored carosels to match. Unfortunatley even though we have more frames we don't really have much more time. Our animations are limited by the time it takes for a single frame to cycle around the record player and in the end the maximum speed for the record player is 45 rotations/minute. Changing the number of frames has helped slightly and allowed us to upgrade from 9FPS (with 12 frames) to 12 FPS (now there are 16 frames), but we're at a hard limit.

This limit has proven hard when portraying concepts that need a natural amount of time to breath.

We have around 1.3 seconds and just 16 frames to tell our stories.

## A looping problem

A key issue Im coming up against is looping back, that is to have a smooth animation we need the last frame to seemlessly transition back to the first frame to create the holy grail of short frame animation, **the continious-loop**.

## A review of looping options

There are a number of looping options, and to create variation across our exhibit we've wanted to explore and display a number of them as using just one technique over and over is well, boring. That said some techniques are much harder than others to achieve a satisfying result.

Herein I'll review a few options we've discovered towards helping us and future short frame animators in isolating techniques and considering their pro's and cons.

### 1. Endless Zoom

With Endless Zoom you create a main element with a cavity in it and inside the cavity you copy in smaller copies of itself.

The camera then zooms continously (continous Zoom In or Zoom Out is both fine) and at say the edge of the cavity you loop back on itself.

Pros

*   Has a nice sense of pace, people experience is that the animation is longer than it actually is and they look away after a number of cycles.
*   Easy to tell stories that say 'there are millions of these inside each other' or 'this goes infinitley deep'.

Diffucilties

*   Praxinoscope frames are very very very narrow, the animation pushes up against the side frames and often creates shapes at the seems between frames that can be confusing and attract attention away from the primary animation.
*   Possibly Remedy is to make the background colours fairly flat so they at worst blend into each other at the frame edges.

### 2. 360 Spin

Full 360 Spins go very fast and can't really be slowed down.

Creating an effective spin illusion is hard to do by hand but relativley easy with 3D modelling software.

The Spin occurs very fast and this is a key limitation. Recommendation is to spin only very simple shapes, to spin slower consider Illusionary One Side Spin.

### 3. Illusionary One Side Spin

This technique relies on animating a symetrical shape but only doing the transition from one corner to the next, in essence the eye perceives that 4 cycles will need to go by for a full spin to occur.

Cons This technique only works with symetrical objects where you can find a clearly repeated registration point at which to begin and end the frames on.

You will also need to tell your story on just one of the rotations as the rest of the rotation cycles don't really exist.

### 4. Melt/Fade

Idea here is to start with an empty background and then after the object appears, to then melt or fade it back to the empty state.

Pros This is a fantastic technique as you have the full 16 frames to tell your story and it works as long as your first and last frame are in an empty state.

### 5. Morph/State to State

Ok this technique looks good on paper but beware. I have had much pain working with this technique.

The biggest pro/attraction of this technique is that it is easy to use for storytelling purposes.

But as I mentioned it's a path to despair.

The reason is that there is generally not enough frames to achieve the transition across and then the transition back again.

Given 16 frames (or 1.3 second), you have on .65 of a second to transition from state A to state B and then the same to transition back.

One optimisation is to hold for longer on the 2 primary states and attempt to speed up the transformation across the remaining frames.

My experience has been this doesn't work very easily.

Essentially the eye needs time to recognise and appreciate each state and there is just not enough time to budget this time for two states and also fit in a reasonable transition between the two.

Recommendation: After transitioning from A to B, consider transitioning from B to blank, this can possibly done with less frames.

### 6. Walk cycle

This is a classic technique and can be achived in 16 frames. It's easy to tell a story and the sense of continous walking/running is immediatley understandable and likely satisfying to the viewer.

The main difficulty with this approach is the limits of your skills in character animation/illustration.

It will likely take a lot of trial and error to create a realisitic look but otherwise the animation fits the medium.

(Disclaimer: I haven't achieved a realistic walk cycle yet as I was unsure of my illustration skills).

### 7. Abstact movement

This technique involves animating things that aren't immediatley identifyable as real world objects.

A pro of this technique is the ability to create nice asthetic movement and animation without the constraints of making something that needs to be interpreted as a real world object.

The biggest con of this approach is the likely lack of narrative and story telling capability. Maybe ok for an art piece but not so good to tell more nuianced stories.

Requires clever application to tell a worthwhile story.

### 8. Bouncing/Rolling

These techniques offers similar benefits to the walk cycle but possibly can be achieved with less effort.

## Conclusion

In creating this article I've actually had a few new ideas.

There are possibly more, I'd love to hear if you come up with any others, specifically animation approaches that are well suited to short frame praxionoscope based animation.