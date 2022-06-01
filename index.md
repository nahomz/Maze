<html>
 <body>
  <h1>Maze</h1>
  <header>
   <ul>
    <li><a href="#intro"/>Introduction</a></li>
    <li><a href="#feature"/>Feature</a></li>
    <li><a href="#about"/>About</a></li>
    
   <button type="submit"><a href="https://github.com/nahomz/Maze">Project</a></button>
  </ul>
  
  </header>
 <img src="https://i.ytimg.com/vi/STNqcqLRBgk/maxresdefault.jpg", alt="maze" />
  <br/>
<h2 class="intro">Introduction</h2>
<p>The main goal for this project is  to make a fully functioning game using a third party SDL library in 3D using raycasting that would challenge the player to think outside of the box and move in a different direction.</p>
<p>Another goal included adding enemies(e.g. obstacle ) to make the game interesting and using weapons . Finally, the constraint for time was an issue because the project took a lot of time..</p>


  <h2>Directory layout</h2>
  <h3>Typical layout:</h3>

Maze/            project folder
  <br/>
|--headers/     headers folder
    <br/>
|-- src/         src folder
    <br/>
|-- image/       image folder
    <br/>
| --Makefile     makefile
    <br/>
  <h2 class="feature">Feature</h2> 
  <img src="flowchart2.PNG", alt="maze" />
  <h3>DEFINING PROJECTION ATTRIBUTES</h3>
<p>we need to define some attributes before we can project and render the world. Specifically, we need to know these attributes:</p>
<ol>
 <li> Player/viewer’s height, player’s field of view (FOV), and player’s position.</li>
<li>  Projection plane’s dimension.</li>
<li>  Relationship between player and projection plane.</li>
 </ol>
 <ul>
<li>the player is 32 unit  half of the wall unit</li>
<li> The FOV determines how wide the player sees the world in front of him/her</li>
<li>To put the player inside the world, 
we need to define the player’s X coordinate, the player’s Y coordinate, and the angle that the player is facing to. 
These three attributes forms the “point of view”:</li>
 <img src="dimension.PNG", alt="maze" />
 <h3>So now we know:</h3>
 <ul>
<li>Dimension of the Projection Plane = 320 x 200 units</li>
<li>Center of the Projection Plane = (160,100)</li>
<li>Distance to the Projection Plane = 277 units</li>
<li>Angle between subsequent rays = 60/320 degrees</li>
  </ul>
 <h3>FINDING WALLS</h3>
<p>the wall can be viewed as collection of 320 vertical lines (or 320 wall slices).
Instead of tracing a ray for every pixel on the screen, we can trace for only every vertical column of screen. The ray on the extreme left of the FOV will be projected onto column 0 of the projection plane, and the right  most ray will be projected onto column 319 of the projection plane.</p>
 <ul>
<li>Based on the viewing angle, subtract 30 degrees (half of the FOV).</li>
<li>Starting from column 0:</li>
<li>Cast a ray. Trace the ray until it hits a wall.</li>
<li>Record the distance to the wall (the distance is equal to the length of the ray).</li>
<li>Add the angle increment so that the ray moves to the right</li>
 </ul>
To find walls, we need to check any grid intersection points that are encountered by the ray
<p>The best way is to check for horizontal and vertical intersections separately.
When there is a wall on either a vertical or a horizontal intersection, the checking stops. The distance to both intersection points is then compared, and the closer distance is chosen.</p>
 <h3>DRAWING WALLS</h3>
<img src="drawing walls.PNG", alt="maze" />
  <h2 class="about">About</h2> 
So why did I choose such a project? The purpose of this project for me is firstly,
  <ul>
<li> to learn the mathematics and physics behind developing the game and learn computer graphics concepts like how to render</li>
<li> to learn how to develop a game without a game engine, without using the best free game engine like Unity or Unreal.</li>
<li>finally, it is Alx portfolio project.</li>
  </ul>
  <h3>Nahom Zelalem</h3>
  <br>
github:-https://github.com/nahomz/
  <br/>
github project:- https://github.com/nahomz/Maze
  <br/>
linkedin:- https://www.linkedin.com/in/nahom-zelalem-1158a3225
  <br/>
  <body/>
</html>
