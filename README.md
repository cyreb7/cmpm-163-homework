# CMPM 163 Homework
Homework repository for [Winter 2018 CMPM 163](https://creativecoding.soe.ucsc.edu/courses/cmpm163/).

## Homework Packet 2
### Outdoor 3D scene
![alt text](https://cyreb7.github.io/cmpm-163-homework/hw2/textures/OutdoorScene.jpg "Outdoor scene")
In addition to the required elements of the scene, I went a step further and improved the reflection map with waves. I used the noise function example from class in the vertex shader to vary the height. To make the height displacement more believable, I perturbed the normal used to calculate the reflection proportionally to the height displacement, making the reflections vary with the height and producing a more believable effect.

### Abstract scene using particles and noise 
![alt text](https://cyreb7.github.io/cmpm-163-homework/hw2/textures/ParticleAndNoise.jpg "Particle system")
My particle system mimics a fountain spraying water into the air. I spent a lot of time reverse engineering GPUParticleSystem.js so I could modify their shaders. I got it working eventually and added gravity to the vertex shader and customized the alpha value in the fragment shader to make it look more like water. A slider to vary the turbulence of the particles based on a noise function is provided.

## Homework Packet 1
* [Image Processing](https://cyreb7.github.io/cmpm-163-homework/hw1/imageProcessing.html)
* [3D Scene](https://cyreb7.github.io/cmpm-163-homework/hw1/3dscene.html)
* [Game of Life](https://cyreb7.github.io/cmpm-163-homework/hw1/gameOfLife.html)
* [Visual Effect](https://cyreb7.github.io/cmpm-163-homework/hw1/Homework1D.pdf)

## Setup
Running web pages from your local machine requires a local server. Running a Python server is usually easiest:
```python -m http.server```
