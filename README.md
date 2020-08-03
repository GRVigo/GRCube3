# GRCube3
C++ classes for 3x3x3 Rubik's cube.

The objective of this code is to search for algorithms that solve the cube, so that it is as fast as possible.

To understand this code you must be familiar with the [notation of the rubik's cube](https://ruwix.com/the-rubiks-cube/notation/).

![headshot](Cube.png)

# How to use these classes (most important features)

## Creating a cube
```
#include "cube.h" // Cube header
#include "algorithm.h" // Algorithm header

Cube C1; // Creates a cube in solve condition

Algorithm A(25); // Creates an algorithm with 25 random movements - movements are optimized and can't be reduced
Cube C2(A); // Creates a cube with the given algorithm applyed
```

## Set a cube to his solve condition (reset)
```
C2.Reset(); // Cube C2 is in his solve condition
```

## Comparing cubes
```
if (C1 == C2) { ... } // Check if two cubes are in the same condition
if (C1 != C2) { ... } // Check if two cubes are in the different condition
```

## Checking the cube status
```
if (C1.IsSolved()) { ... } // Check if the cube is in his solve condition
if (C1.IsSolved(Pieces::UFR) { ... } // Check if the piece UFR (Up, Front, Right) is in his solve position and has his correct direction
if (C1.IsSolved(Layers::F) { ... } // Check if all the pieces in front layer (F) are solved
```

## Making movements to the cubes
```
C.U(); // Move the layer U 90 degrees in clock-wise direction
```

You can use U, U2, Up (as U'), D, D2, ... movements. Also x, x2, xp (as x'), y, y2, yp, z, z2 and zp turns are implemented.


# TODO: This document should be completed!!!
