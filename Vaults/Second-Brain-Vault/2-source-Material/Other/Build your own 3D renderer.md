2026-08-30 12:12

Status: #baby

Tags: [[programming]] [[JS]] [[graphics]] 

# Build your own 3D renderer

## Background

ray tracing(which simulates how light work by sending rays from the camera), shadows, reflections are know as global illumination.

rasterization is faster approach than global illumination.

## Casting rays from the camera to the image plane

In backward tracing(the more efficient) we trace the rays that end at the light source(the camera) by starting in the camera. while forward tracing we consider all reflected rays.

linear interpolation(lerp) is used to determine the image positions to cast rays onto, by having the point P some percent n along x_1 x_2. 
![[Pasted image 20260830124438.png]]

$$t =(1-\alpha)x_1+\alpha x_2$$
$$b =(1-\alpha)x_3+\alpha x_4$$
$$p=(1-\beta)t+\beta b$$

Isn't this just equivalent to $x_1+\alpha$ ? 


## the visibility problem with intersection tests

the camera sees the geometry that intersects with one of the casted rays.
![[Pasted image 20260901135836.png]]
![[Pasted image 20260901140025.png]]

## Simulating illumination using Phong shading 

local illumination 
Phong reflectance model consists of:
The scene containing some ambient light with intensity $i_a$.
For each light in the scene, the object reflects some portion $k_d$ This is the diffuse component taht scatters light in all directions

The contribution depends on the angle between the light vector and the surface normal, $L$ 
![[Pasted image 20260903163523.png]]

spectacular highliht depends on the viewing angle, and is given by $R = 2(N \cdot L)N-L$

# References
https://avikdas.com/build-your-own-raytracer/00-background/