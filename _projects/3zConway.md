---
layout: default
title: "ConwayScope - Cellular Automata Matrix (C++)"
---

# ConwayScope

Unused muscles fade, and the exact same applies to the brain. Recently, I felt that my coding abilities were... hmm, slightly deteriorating from a lack of practice. To counter this, I decided to pick up C++,a language I last saw in high school over six years ago, and challenged myself to write a complete project from scratch, without the assistance of AI.

### The Concept
The result is **ConwayScope**. It is a hardware-software integration that runs John Conway's famous [Game of Life](https://en.wikipedia.org/wiki/Conway%27s_Game_of_Life) and visualizes the cellular automata on a physical 16x16 LED matrix display.  The LED matrix is composed of four 8x8 matrices driven by MAX7219 units.

<figure style="text-align:center; margin: 40px 0;">
  <video width="450" controls muted loop style="border: 1px solid #333; border-radius: 4px;">
    <source src="/assets/ConwaySc.mp4" type="video/mp4">
  </video>
  <figcaption style="margin-top: 10px; color: #999;">
    <em>The ConwayScope in action.</em>
  </figcaption>
</figure>

### The "Scope" Feature
I implemented a movable "window" or camera—the *Scope*. The application allows the user to pan a 16x16 viewport across the much larger, simulation plane. This means you can freely move the frame around to explore different evolving clusters and ecosystems of cells in real-time, just like looking through a microscope at a petri dish.

### Technologies & What I Learned
Building this project served as an excellent refresher and a deep dive into several technical domains:
* **C++ Programming:** Re-learning memory management, pointers, and object-oriented design in a modern context to write the core simulation engine.
* **Hardware Interfacing:** Utilizing an **Arduino Uno** to drive the 16x16 LED matrix, which required managing power draw and pushing pixel updates at a high refresh rate.
* **Serial Communication:** Designing a reliable byte-stream protocol to send the calculated grid states from the host computer's backend down to the Arduino via USB/UART.

### GitHub Repository

See the full code <a href="https://github.com/JanskyContinuum/ConwayScope" target="_blank">here</a>.