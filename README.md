# Terrain-Visualization

Get the height field from a file called or.hgt. It has 105 rows, with 201 points per row. Ignore the exact formatting -- just read them freeform. (See below.)
Get the texture map from a file called Oregon2048.bmp. Use the BmpToTexture routine to read it. (See below.)
This image is 2048x2048. If that is too big for the system you are on, try Oregon1024.bmp or Oregon0512.bmp instead. All three files will be in the grading folder. You don't need to turn them in with your executable.

Draw the triangles of the terrain in shades of white. Compute s and t texture coordinates at each vertex. Do OpenGL lighting or pseudo-lighting for each triangle. (See below)
Using texture mapping, display the texture on top of the terrain.
Using the GLUI interface, allow the user to switch between (1) no texturing, (2) GL_REPLACE texturing, and (3) GL_MODULATE texturing.
Use GL_LINEAR as the minification and magnification filters.
The cloud can be drawn any way you want, but it must use OpenGL blending to make it look translucent.
The cloud can move any periodic way you want it to move. (It just has to move -- it doesn't have to dance like Joe Graphic's sample.) 
Make the period 10 seconds.
Hitting the 'p' key should pause or resume the animation. You can implement this by having a bool variable called Paused, initialized to false, and then in your Keyboard( ) function do something like this:
case 'p':
        Paused = ! Paused;
        if( Paused )
                GLUI_Master.set_glutIdleFunc( NULL );
        else
                GLUI_Master.set_glutIdleFunc( Animate );
        break;
BTW, this is always a good animation debugging feature.

Using the GLUI interface, allow the user to exaggerate the height of the terrain. I.e., scale it in the vertical direction, starting at 1.0 and going to whatever maximum value you think is good.
Using the GLUI interface, allow the user to turn the cloud off and on.
Using the GLUI interface, allow the user to toggle between orthographic and perspective projections.
