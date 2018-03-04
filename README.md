# CMPM 163 Homework
Homework repository for [Winter 2018 CMPM 163](https://creativecoding.soe.ucsc.edu/courses/cmpm163/).

## Homework Packet 3

### SDF
![alt text](https://cyreb7.github.io/cmpm-163-homework/hw3/images/sdf.png "SDF")
For my SDF project I tried to write as much of the shader code as possible myself. I made some concessions for functions that are complex or easy to mess up (as I invariably did), but the overall structure of the code is my own. Trying to keep my code clean turned out to be one of the hardest challenges, it seems to be nearly impossible to declare data in a reusable and iterable way in GLSL, but I guess you aren't supposed to anyway.

![alt text](https://cyreb7.github.io/cmpm-163-homework/hw3/images/sdf-bad.png "Errors rendering SDF shadows")
Once I had my shader rendering properly, I realised it should be easy to add simple occlusion checking for lights. It was easy to modify my ray marching function to accept a max distance parameter and return a specific value if it ran into that limit. Using this I was able to march a ray from the point on the object to the light and only render it if the ray doesn't hit anything by the time it reaches the light. My biggest problem was that with this simple implementation there were obvious bands on the objects that were being unlit (pictured above). After much head banging, I realised that because I started the ray marching at the same place as it previously ended, many of the rays were so close to the object that they were immediately stopping. Adding an initial march away from the object fixed the issue. [View project](https://cyreb7.github.io/cmpm-163-homework/hw3/sdf.html)


### Begin Planning Your Final Project

---

## Homework Packet 2
### Outdoor 3D scene
![alt text](https://cyreb7.github.io/cmpm-163-homework/hw2/textures/OutdoorScene.jpg "Outdoor scene")
In addition to the required elements of the scene, I went a step further and improved the reflection map with waves. I used the noise function example from class in the vertex shader to vary the height. To make the height displacement more believable, I perturbed the normal used to calculate the reflection proportionally to the height displacement, making the reflections vary with the height and producing a more believable effect. [View project](https://cyreb7.github.io/cmpm-163-homework/hw2/OutdoorScene.html)

### Abstract scene using particles and noise
![alt text](https://cyreb7.github.io/cmpm-163-homework/hw2/textures/ParticlesAndNoise.jpg "Particle system")
My particle system mimics a fountain spraying water into the air. I spent a lot of time reverse engineering GPUParticleSystem.js so I could modify their shaders. I got it working eventually and added gravity to the vertex shader and customized the alpha value in the fragment shader to make it look more like water. A slider to vary the turbulence of the particles based on a noise function is provided. [View project](https://cyreb7.github.io/cmpm-163-homework/hw2/ParticlesAndNoise.html)

---

## Homework Packet 1
* [Image Processing](https://cyreb7.github.io/cmpm-163-homework/hw1/imageProcessing.html)
* [3D Scene](https://cyreb7.github.io/cmpm-163-homework/hw1/3dscene.html)
* [Game of Life](https://cyreb7.github.io/cmpm-163-homework/hw1/gameOfLife.html)
* [Visual Effect](https://cyreb7.github.io/cmpm-163-homework/hw1/Homework1D.pdf)

## Setup
Running web pages from your local machine requires a local server. Running a Python server is usually easiest:
```python -m http.server```
