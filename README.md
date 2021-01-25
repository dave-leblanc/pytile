# pytile
Dimetric projection tiling engine based on Pygame
pyTile Iso depth sorting
Early prototype of a "perfect" isometric sprite depth sorting thingy


Timothy Baldock
(entropy)
This is going to be a testing demonstration of a sprite depth sorting system I'm working on. Currently it takes a coordinate in 3D space and draws a bounding box around it based on a projection.

The idea is that objects will be represented in 3D based on a coordinate, 3 dimensions, a rotation and a tilt (to allow for tilting up/down for going up/down hills).

The sorting works by finding how close each object is to a plane passing through the 3D space origin, such that a viewing ray from the camera is a normal to that plane. This is used to compare objects and determine if one is in front of another. A simple heap-sort is then used to keep all the sprites in order. Eventually all of this behaviour will be implemented in a sprite group class and used in my game project pyTile.

Controls:
Q/D - position in X
A/E - position in Y
W/S - position in Z
U/L - size in X
O/J - size in Y
I/K - size in Z
Z/X - rotation
UP/DOWN/LEFT/RIGHT - Move origin in 2D
T/Y - toggle origin/coordinate display
