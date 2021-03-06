SpaceSimulator
==============
*PROJECT LAST MODIFIED: 15th of May 2011, 18:09 PM, +2 GMT*

## Introduction 

The Space Simulator is an application that has been developed using the C++ language using the 
GLUT and OpenGL libraries. The application responds to some user input. The goal of the application 
was to simulate a universe (or a space if you will) and to display this with some simple graphics. 

## Classes 

The classes used in the project are as follows: 
* **Window**
    * The class responsible for creating a window 
* **Draw**
    * The class handling all drawing in the application 
        * Has a window member to draw in 
        * Has a space member to draw 
* **Space**
    * Keeps lists of all objects in space 
        * A list containing all objects 
        * As well as different lists for different types of objects: Suns, Planets and Moons. 
* **SpaceObject**
    * Creates an object in space that can be affected by gravity. 
* **Star**
    * Inherits SpaceObject and is special because it emits light. 
* **Planet**
    * Inherits SpaceObject and is just a planet. 
* **Moon**
    * Inherits SpaceObject and is special because it orbits a planet. 
* **Coordinate**
    * Handles coordinates in the application. 

## User Input 

The application responds to some user input as listed here: 
* The ‘+’ and ‘–‘-buttons zoom in and out, respectively. 
* The ‘n’ button follows the next object in space(default is the sun) 
* The ‘q’ button exits the application 
* The delete button deletes the last object added into space. 
* A left mouse click creates a planet at the pointers position with a speed relative to the press and release position difference. 
 
More objects can be created within the main function. Follow the guidelines given there, first create an object and then add it to the space to be displayed in. Multiple stars can be created (to a maximum of 8) which all will emit light.

## Dependencies 

The program is displaying graphics using GLUT and therefore the GLUT files are needed. These can be 
found in the *dependencies* folder. 

## Compiling
The code was written entirely in the Code::Blocks IDE. To compile the
code glut.h, libglut32.a and glut32.dll has to be added to the IDE and
system folders if these aren't included already. These files can be found
in the *dependencies* folder, together with some simple instructions.

The code has only been tested to compile on the Windows Vista
Operating System. It will most likely also run on all other Windows
Operating systems released after Windows 95. On the earlier versions
support for OpenGL has to be installed manually.

## Notes
At the time of the creation of this program I had no experience
with GLUT before and very little experience with OpenGL. Therefore the
code concerning GLUT and OpenGL will probably not be optimal. It was
simply a means to an end of presenting my results in a more concrete way.

All the lines within the code have been kept at 78 characters long
for the sake of proper printing line length.

The coding standard used in this project is inspired by:
http://www.possibility.com/Cpp/CppCodingStandard.html
