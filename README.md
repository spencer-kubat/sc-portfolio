# Spencer Kubat — Software Portfolio

## Overview

This repository serves as a portfolio of selected projects from my coursework at the University of St. Thomas. Each project represents a different area of computer science that I found compelling enough to keep building on beyond the minimum requirements — whether that meant implementing real AI search algorithms in a game, wiring up webcam-based hand tracking to a 3D engine, or learning how to generate natural-looking shapes with Perlin noise. Together, they reflect the range of skills I've developed as a student: building interactive applications from scratch, working with game engines and web technologies, and applying the problem-solving mindset that a computer science education is really about.

The three projects I chose to highlight are **Swim Sim**, **Wheel of Sustainability**, and **Asteroids**. They span different tools (Three.js, Godot, p5.js), different languages (JavaScript, GDScript), and different domains (3D graphics, artificial intelligence, 2D game development), but they share a common thread: each one started as a class assignment and turned into something I was genuinely proud to ship. All three are deployed and playable in the browser.

---

## Swim Sim

**Repository:** [github.com/spencer-kubat/cc-final](https://github.com/spencer-kubat/cc-final)
**Live Demo:** [spencer-kubat.github.io/cc-final](https://spencer-kubat.github.io/cc-final/)

Swim Sim is a first-person underwater swimming simulator built with Three.js and ml5.js for my Creative Coding final project (with Dakota Snyder). The player explores a procedurally tiled ocean floor populated with animated seaweed, schools of fish, and rising bubbles. What makes it unique is the control scheme: by default, the game reads the player's hand gestures and head orientation through their webcam using ml5's HandPose and FaceMesh machine learning models. A breaststroke motion with your hands propels you forward, and turning your head steers the camera. Keyboard and mouse controls are available as a fallback.

I chose to highlight this project because it pushed me furthest outside my comfort zone. I had never worked with WebGL, 3D scene graphs, or machine learning APIs before this course, and this project required all three at once. The gesture recognition system alone involved building a full state machine (idle → primed → swim stroke) on top of raw hand keypoint data, plus a separate head-tracking pipeline that converts facial landmark positions into camera pitch and yaw. Getting the infinite-scrolling chunk system to tile seamlessly was another challenge I'm proud of solving.

---

## Wheel of Sustainability

**Repository:** [github.com/spencer-kubat/ai-final](https://github.com/spencer-kubat/ai-final)
**Live Demo:** [spencer-kubat.github.io/ai-final](https://spencer-kubat.github.io/ai-final/)

Wheel of Sustainability is a Wheel of Fortune-style word game built in Godot 4.4 for my AI course final project. Every puzzle is a sustainability-related term or concept drawn from a curated list of 100 phrases. The game supports 1–3 players in any mix of human and AI, with three difficulty levels that change both the puzzle length and the AI's decision-making strategy. The AI opponents use a pipeline of real search algorithms: CSP (constraint satisfaction problem) filtering to narrow down candidate phrases, Uniform Cost Search on easier difficulties to pick the most cost-effective consonant, and Greedy Search on hard to converge on a solve as fast as possible.

This is the project I chose to highlight from my AI coursework because it's where the theory from class clicked into something tangible. Reading about CSP filtering and search algorithms in a textbook is one thing; wiring them into a game where they have to make real decisions against a human player is another. Seeing the AI narrow 100 phrases down to one through constraint propagation and then guess the answer outright was a satisfying moment.

---

## Asteroids

**Repository:** [github.com/spencer-kubat/cc-asteroids](https://github.com/spencer-kubat/cc-asteroids)
**Live Demo:** [spencer-kubat.github.io/cc-asteroids](https://spencer-kubat.github.io/cc-asteroids/)

Asteroids is a clone of the classic 1979 Atari arcade game, built from scratch with p5.js for my Creative Coding course. The player pilots a triangular starship through a field of 15 procedurally generated asteroids, rotating, thrusting, and firing missiles to destroy them. Large asteroids split into two smaller, faster fragments on impact. The game features Perlin noise-based asteroid shape generation (producing unique, irregular polygons rather than simple circles), a point-in-polygon collision detection algorithm, particle explosion effects, and spatial audio where the thruster sound pans stereo based on the ship's screen position. A Tweakpane GUI panel lets players adjust stroke color, background color, asteroid speed, and noise intensity in real time.

I chose this project because it was my first real experience building a game loop from scratch — handling input, physics, rendering, and collision detection all in one cohesive system. The Perlin noise generation was a highlight: learning how to map 2D noise into polar coordinates to produce organic, natural-looking asteroid silhouettes was a technique I hadn't encountered before and it made the game feel much more polished than simple circles would have. The Tweakpane integration was also valuable as a lesson in making creative tools adjustable and explorable.
