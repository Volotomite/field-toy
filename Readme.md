# Field-toy

This is a toy-project where you define vector field and subdivision of cube surface by giving number of subsegments.
Cube is rendered with respect to the perspective and you can morph its shape by applying vector field you defined (each point of subsegment will move in direction of its vector).

## How to mess around with it

1. Launch vfield.html

2. Enter the number of subsegments (15 is good enough)

3. Use mouse to rotate object. Y axis placed vertically, X horizontally, Z is perpendicular to the screen.

4. Press "Enter" to define a new vector field, where each vector for a given point of cube will be equal to ( Fx(x,y,z), Fy(x,y,z), Fz(x,y,z) ), so you'll have to define Fx, Fy, Fz.

5. When defining a function F, you'll need to write expression in Javascript language with use of variables "x" "y" "z" (otherwise vector field will be constant which is boring)
For example, your inputs might be: "Math.sin(y*y+z*z)", "Math.sin(x*x+z*z)", "Math.sin(x*x+y*y)"

6. Hold left or right arrow to apply vector field (each point will move a little in direction of its vector each step of iteration).
Right arrow will move points in positive direction, and left arrow will move them in negative direction
