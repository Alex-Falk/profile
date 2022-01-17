# PORTFOLIO: ALEXANDER FALK

~
6  ]rt451 

_Programmer with 3 years experience in the games industry
MSc. Computer Games Engineering
Mphys. Astrophysics_

I am a Programmer with 3 years professional experience in programming gameplay features in C++ and C#.  I have worked on The Lego Movie 2 Videogame (2019), Lego Star Wars: The Skywalker saga (announced 2021) and Iron Harvest (2020).

I am always eager to learn more and improve my abilities as a programmer through experience as well as learning resources such as GDC talks. I am always motivated to apply my critical thinking and problem-solving abilities in a team environment in order to bring a project to a joint success.

I have grown up in an international environment, having lived, studied and worked in a total of 6 different countries. I am always eager to learn more about other cultures and work with people from all around the globe.

I am passionate about gaming, programming, music, travel, cultures and science.

**Key skills**: C++, C#, Python, Perforce, Git, SVN, OpenGL (GLSL), Physics, Maths (Linear Algebra), Critical Thinking, Problem Solving, Teamwork

You can find Code samples from my university projects on my [GitHub](https://github.com/Alex-Falk).

My [CV]()

--- 

# Games I Worked On

## IRON HARVEST
While working on Iron Harvest I was part of a small team focused on improving units and implementing new abilities for them. To achieve this we disected the units in meetings and discussed how they can be improved by code, design, animation, vfx and sfx. This allowed me to then implement new features and units in close collaboration with the other teams. We also created abilities for units from the ground up for the upcoming expansion for Iron Harvest, as well as overhauling systems such as how infantry aim. We continued with these improvements for the live patches after the official release date of 1st September 2020. During this project I gained experience working with Unity3D and C#.

## LEGO STAR WAR: THE SKYWALKER SAGA
As a Junior Game Mechanics Programmer at Tt Games I mostly worked on "Lego Star Wars: The Skywalker Saga" for which I took responsibility of implementing the physics based "The Force" game mechanic as well as some smaller features like an edge highlighting system to manage which objects are highlighted by which colour. My work at Tt Games involved using C++ and an in house game engine.
Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

## THE LEGO MOVIE 2 VIDEOGAME
During my initial months at Tt Games I was bug fixing in various systems of the game Lego Worlds. These bug fixes were not integrated into the live version of the game, but the systems were used in "The Lego Movie 2 Videogame", gaining me a credit in that title.

---

# University Projects

## "El Bloob" - Team Project
<iframe width="100%" height="315" src="https://www.youtube.com/embed/IgmXKeS9seU" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

This was my Team project in my MSc Computer Games Engineering degree. We were tasked with making a multiplayer game in which players paint the enviroment with the examples of De Blob or Splatoon.

My Roles in the team project were:

- Framework: We chose to base this project on the framework we were provided for the "Game Tech" course. Specifically we chose my version of it which I had expanded with my own code during that course.
- Git Admin: Handled all merges/merge conflicts to the develop branch and fixed resulting bugs.
- Networking: Implement the server-client system, Dead Reckoning and generally everything that needs to be sent over the network (using the ENet UDP library). This included working with other team members to make their implementation of features network compatible.
- Particle Effect: I created the particle effect seen in the videos by using an openGL compute shader
- The "paint pool" effect: There a pools of each colour of paint, the transparent part of that pool that represents the liquid is done with a tessellated quad and a sine wave applied to it
- QA, bug finding and fixing: To discover bugs to later be fixed either by myself or other team members.
- Sobel Shader: I wrote the shader for the 'cartoony' black outline effect and used my teammate's post processing system to add it to the game.

The github repo for this project can be found here where the nclgl and ncltech libraries are based on my previous courseworks, the networking folder contains my networking code and the PC folder contains the code for the actual game, which I also contributed to.

## Fast Protoyping using UE4
<iframe width="100%" height="315" src="https://www.youtube.com/embed/wzvcy0FLRkM" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

This prototype is a 2 player split-screen game in which the goal is to paint a certain amount of the environment before the opposing player does. It includes the following features:
- ainting on contact (using decals attached to box colliders to prevent large overlaps)
- An "Ammo" Paint level that decreases when the player paints the environment. This decreases the size of the ball and therefore the area it paints
- Paint 'pool' (the square areas) which allows the player to recharge their paint level up to 150%. If the player goes onto a pool of the other player's colour they loose all their paint instead
- 4 different kinds of pickups:
  - Double Size: Increases the "ammo" level to double (or the max value of 200%)
  - Double Speed: Speeds up the player by doubling the torque applied to it on key presses for 10 seconds
  - Infinite Paint: Lets the player paint without decreasing the ammo level and size for 10 seconds
  - Paint bomb: Allows the player to shoot a 'bomb' of paint that paints a large area on impact
- There is simple rubber-banding for the pickups that if a player is 10% of the max score ahead of the other, then the player who is ahead only gets the pickup for 5 seconds while the one behind gets them for 15 seconds
- When a player reaches the maximum score the game will end and allow the player to either choose restart or quit

## GPU Modelled Softbody
<iframe width="100%" height="315" src="https://www.youtube.com/embed/Mjj8oiJLEJU" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

In my "Advanced Game Tech" module one of the advanced tasks was to create a GPU accelerated soft-body. I created this using a set of points connected to each other by springs. Both the spring interactions and the other physics acting on the particles (collisions with other objects and gravity) are calculated on the GPU using CUDA (see code here). For this project I used C++ and the NCLGL framework from my graphics course.

Each update the soft body is calculated in the following way:
- Calculate the collisions of each node with other objects in parallel
- Calculate the spring constraints in 8 separate parallelisable sets. For a set to be parallel each node can only be affected by one spring
- Repeat this for 5 passes to achieve a better result
The rendering of the soft-body is done using openGL and each of the physical node positions is used as a vertex for the mesh. These mesh vertices are then updated every frame.

## Graphics for Games
<iframe width="100%" height="315" src="https://www.youtube.com/embed/ri7PLdAxPmw" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

The goal of this project was in implement a rendering pipeline and show off an Array of different graphical effects and techniques. The video shows three separate scenes with the following effects:

**Scene 1: **
- Rain particle effects
- Advanced lighting using a spotlight
- Real time shadows of the hellknight on the floor and himself
- Particle effects

**Scene 2:**
- Height-map generation using a given texture
- Basic Lighting with ambient, diffuse and specular lighting as well as reflection of the skybox in the water
- Texture blending
- Periodically changing textures
- Post processing effects applying a sobel filter and a contrast calculation (these work in all scenes but are shown off here)

**Scene 3:**
- Tessellation of a plane of 16x16 quads ("patches"). Each quad gets tessellated to 64x64 quads. A height-map is read in and applied to this using a scaling factor which allows the terrain to grow.
- Tessellation of the water. It takes 32x32 quads ("patches") and applies two sine waves to the height in order to simulate the wave effect
- Particle effects: Lava particles emitted from the volcano
- Deffered rendering

## GameTech: Networking/AI
<iframe width="100%" height="315" src="https://www.youtube.com/embed/rlYH0_0A-tM" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

This is part of my coursework for the Advanced Game Tech module. The video here shows a server running with 3 clients connecting to it. The server does the calculations such as pathfinding, maze creation and AI and sends it to the clients for them to render. The client has a point and click interface to choose starting and end positions for its avatar (green cube).  The hazards (red cubes) are controlled by a Finite State Machine. Collisions can be detected between avatars and hazards. Below is an overview of some of the main features:

**Server Features:**
- Generation of a random maze with a given size and complexity (parameters received by user)
- Control of Avatar (green cube) movement and pathfinding (using A*)
- Control of the 'Hazards' (red cubes) using a FSM with the states 'Patrol','Chase' and 'Search'. The switching of states is based online of sight checks in the horizontal and vertical directions. The find state is activated if the hazard has been chasing an avatar and has lost sight. It will move to the last known position of the avatar and check if it can see it again.
- Collision response for avatar-avatar collisions and hazard-avatar collisions. Avatar-avatar collisions are simply done by moving the avatars back to the previous tile-center they passed and then stop. In order to start moving again the client can choose a new end position. Hazard-avatar collisions 'kill' the client's avatar and the hazard will switch back to the 'patrol' state
- Sending maze information as well as avatar/hazard positions and client specific paths for rendering client side

**Client Features:**
- Rendering of the maze in 3D as well as rendering of avatars and hazard positions
- Possibility of rendering the path of the given client
- The client can point and click tiles in the maze to select start (right click) and end (left click) positions. This information is then sent to the server for pathfinding calculations.

## Gametech: Physics
<iframe width="auto" height="315" src="https://www.youtube.com/embed/f_6jUrX0kq8" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

The goal of this project was to create a physics engine that could handle a certain amount of collision checks. The initial clip shows different physics integration methods at different framerates.

 I implemented an octree for the physics engine to manage the collision checks in a more efficient manner. The red squares in the video show is adapting octree in action.

 Later on in the video you can also see a ballpool filled with small blue balls, this is run on the GPU using cuda. The ball pool implementation was partially provided by the lecturer but I extended it such that elements from my physics system enact forces on the GPU modelled balls. The cloth shown in this video is the same as from the above video about the GPU modelled soft body.
