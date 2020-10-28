<html>
    <hr>
</html>

# Isles of Limbo (C++/C#)

Created in my 2019-2020 semester at DigiPen, Isles of Limbo is an action packed hack and slash featuring creative enemy designs, scenic ambience, and a wide move set to dispatch foes with. Using our team's custom built engine, we sought to produce a game with eye catching visuals and fast paced gameplay. Resulting in over 400 followers on Steam and dozens of youtube playthroughs, the success of this student project was a gratifying experience for me. You can download and play through Steam here.

Originally planned to be a 2D top down game, midway through production we re-tooled the engine to support an orthoganol perspective. To accomplish this in a timely manner, we utilized tricks like ordered drawing, drop shadows, and 3D assets and animations rendered to 2D sprite animations. Through this, we were able to achieve an asthetic similar to games like Don't Starve or Diablo 2. Avoiding more work than necessary, the internal logic of the game still operated on a 2D level, only utilizing a height displacement when rendering in order to simulate standing or flying figure.

Areas of responsibility:

> Graphics: With Argonautic's amazing art team, I was lucky to be the engine's graphics programmer. Using OpenGL, I implimented core functionality like sprite rendering and Spine animations. I also developed tools such as the determinate particle system, deferred glow shaders, and the stencil culling system. I also handled the mid-project switch from 2D to psuedo-3D in a seamless method. Video file streaming was another graphical feature of the engine.

> Engine Developement: I worked closely with the early development of the engine's foundation. Functionality I worked on includes instanced entities, serialization of scenes and assets, entity and component referencing, entity parenting hierarchies, and modular viewports. Later in the project's lifecycle, I added the performance diagnostics toolset and a per-entity timewarp system.
