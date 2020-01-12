# Field-toy

This is a toy repo where you need to define vector field and subdivision of cube surface by giving number of subsegments.
Cube is rendered with respect to the perspective and you can morph its shape by applying vector field you defined (each point of subsegment will move in direction of its vector).

## How to mess around with it

1. Launch vfield.html

2. Enter the number of subsegments (15 is good enough)

3. Use mouse to rotate object. Y axis placed vertically, X horizontally, Z is perpendicular to the screen.

4. Press "Enter" to define a new vector field, where each vector for a given point of cube will be equal to ( Fx(x,y,z,t), Fy(x,y,z,t), Fz(x,y,z,t) ), so you'll have to define Fx, Fy, Fz. 'x','y','z' are coordinates of space and 't' is time

5. When defining a function F, you'll need to write expression in Javascript language with use of variables "x" "y" "z" "t" (constant vector field will be boring)
For example, your inputs might be: 
"Math.sin(y*y+z*z)", "Math.sin(x*x+z*z)", "Math.sin(x*x+y*y)"
or say
"z*y","y*t","-x*y"
these are cool fields

6. Press "t" to start timer and morphing, press again to turn it off.
Also right arrow will move points in positive direction, and left arrow will move them in negative direction and will ignore time
Scrolling will move camera

At start cube is 2x2x2 size, its center placed at (0,0,0) if you want to move cube at some point (a,b,c) of vector field before you apply it then just add it to point(x,y,z) like so:
"Math.sin((y+b)*(y+b)+(z+c)*(z+c))", "Math.sin((x+a)*(x+a)+(z+c)*(z+c))", "Math.sin((x+a)*(x+a)+(y+b)*(y+b))"
or say
"(z+c)*(y+b)","(y+b)*t","-(x+a)*(y+b)"

Also if you want to scale your field, then just multiply these numbers
