# CS-330-Portfolio
# CS-330 Computational Graphics and Visualization Portfolio

**Author:** Dury Ayers
**Course:** CS-330, Southern New Hampshire University

## About This Project

For my final project I built a 3D version of a desk workspace in C++ and OpenGL, based on a reference photo by Andrew Neel. The scene includes a wood desk, an open laptop, a coffee mug, a smartphone, and a notepad with a pen. The mug is built from a cylinder, a torus for the handle, and a disc for the coffee surface. The desk blends a coffee ring stain texture over the wood grain in a single shader, and the phone screen shows a map texture as a nod to the real-time navigation app idea I used as my running example all term.

The scene is lit with four light sources (a warm key light, a cool fill light, a spotlight, and a back light), and you can move through it with keyboard and mouse camera controls.

## What's in This Repository

* **Source code** for the 3D desk scene (C++ / OpenGL, Visual Studio 2022)
* **Design Decisions document** explaining how I built the scene, the navigation controls, and the custom functions I wrote

## Reflection

### How do I approach designing software?

This project taught me to break something complicated down into simple pieces before I write any code. A coffee mug looks like one object, but in OpenGL it's a cylinder, a torus, and a disc that all have to line up. Once I started seeing every object as a set of basic shapes, planning the scene got a lot easier.

My process was pretty straightforward. I picked a reference photo, sketched out which shapes made up each object, figured out where everything sat on the desk, and then built it one object at a time. Instructor feedback also changed how I design. Early on I had everything crammed into one long render function. After moving each object into its own C++ class with a shared placement system, adding new objects took a fraction of the time.

That habit of planning the structure first, and setting it up so new parts plug in cleanly, is something I'll carry into any future project, whether it's a graphics app or one of the financial planning tools I'm building.

### How do I approach developing programs?

The biggest strategy I picked up was building and testing in small steps. I'd add one shape, run it, check the position and texture, and only then move on. When something broke, I knew exactly where to look. I also started using named constants instead of hard-coded numbers and printing the camera controls and camera changes to the console, which made debugging much faster.

Iteration was a big part of this. The lighting is a good example. My laptop lid kept rendering almost black, so I added a back light. Then I noticed rotated shapes were lit wrong, which turned out to be a bug in how the shader handled normals. Each pass through the scene showed me something new to fix.

Looking back across the milestones, my code went from "make it work" to "make it clean." Milestone One was about getting shapes on the screen. By the final project I was thinking about structure, readability, and how easy it would be for someone else to pick up my code.

### How can computer science help me in reaching my goals?

Graphics gave me a much better understanding of what's happening under the hood when something shows up on a screen: transformations, matrices, lighting models, textures, and the rendering pipeline. That foundation will help in the rest of my degree, especially anywhere math and programming meet.

Professionally, I'm building financial planning tools and I've always been interested in navigation apps like the one I used as my example this term. Both depend on visualizing data clearly. Knowing how tools like Mapbox and WebGL draw things in real time, and how lighting and layout affect what people actually notice, helps me design dashboards and apps that are easier to read and more useful. More than anything, this course showed me I can take something that looks complicated, break it down, and build it.
