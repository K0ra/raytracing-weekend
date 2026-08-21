# Raytracing Weekend

A simple CPU ray tracer written in C++, built as a hands-on exercise in rendering fundamentals.

## Overview

This project follows *Ray Tracing in One Weekend* and implements a basic ray tracer from scratch, rendering scenes of spheres to a PPM image. The current implementation covers the core ray tracing pipeline through diffuse materials and gamma correction.

## Implemented

- Vector math utilities (`vec3`) for points, directions, and colors
- Ray representation and ray-object intersection logic
- Sphere geometry with hit detection
- A generic `hittable` interface and `hittable_list` for managing multiple scene objects
- Interval utility for managing and clamping ranges (e.g. hit distances)
- A configurable camera responsible for scene rendering and image output
- Color utilities for writing pixel data
- Antialiasing via multi-sample pixel rendering
- Diffuse materials with Lambertian reflection
- Gamma correction (gamma = 2) for proper color display
- Shared math/utility helpers (`rtweekend.h`)

## Project Structure

```
src/
├── camera.h         # Camera setup and rendering loop
├── color.h           # Color representation and output
├── hittable.h         # Base interface for objects that can be hit by rays
├── hittable_list.h    # Container for multiple hittable objects
├── interval.h        # Range/interval utility
├── main.cpp           # Entry point; scene setup and render trigger
├── ray.h             # Ray class and operations
├── rtweekend.h        # Common constants and utility functions
├── sphere.h           # Sphere primitive implementation
└── vec3.h            # 3D vector math
```

The project is built with CMake (`CMakeLists.txt`), and rendered output is written as a `.ppm` image.

## Reference

Based on *Ray Tracing in One Weekend* by Peter Shirley.

## Progress

Current progress: ray tracing fundamentals through diffuse materials.

Future chapters (reflection/refraction, positionable camera, defocus blur, and beyond) will be added incrementally as the project develops.
