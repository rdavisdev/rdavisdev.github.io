<html>
    <hr>
</html>

# Isles of Limbo (C++/C#)

Created in our 2019-2020 semester at DigiPen, Isles of Limbo is an action packed hack and slash featuring creative enemy designs, scenic ambience, and a wide move set to dispatch foes with. Using our custom built Liftoff Engine, team Argonautics sought to produce a game with eye catching visuals, along with fast paced gameplay and lots of effects. Resulting in over 400 followers and dozens of youtube playthroughs, the success of this student project on Steam was incredibly gratifying for the team. With one of the main complaints being that players wanted more, our team is very proud of the game we were able to produce. You can download and play through Steam here.

Originally planned to be a 2D top down game, midway through production we re-tooled the engine to support an orthoganol perspective. To accomplish this in a timely manner, we utilized tricks like ordered drawing, drop shadows, and 3D assets and animations rendered to 2D sprite animations. Through this, we were able to achieve an asthetic similar to games like Don't Starve or Diablo 2. Avoiding more work than necessary, the internal logic of the game still operated on a 2D level, only utilizing a height displacement when rendering in order to simulate standing or flying figure.

Aspects of the game I worked on include:

> Graphics: With Argonautic's amazing art team, I was lucky enough to enable their work as the sole graphics programmer. I tackled implementing the visuals of the Liftoff Engine using OpenGL. The core graphic functionality includes static sprite rendering and sprite sheet animation, along with driving and rendering a rigged animation system through Spine. Graphical effects include an incredibly powerful determinate particle engine, a flexible deferred glow effect, and the stencil culling system. I also handled the switch from 2D to psuedo-3D, implementing it in a method that would not effect other aspects of the engine like collision or physics. After bringing on more artists late in the game's development, video file streaming for cutscenes was also added.

> Engine Developer: In the early stages of the Liftoff Engine, I worked closely with the development of the engine's foundation. Both in rendering as well as the core architecture of the engine's functionality. Features I helped implement were instanced entities, serialization of scenes and assets, entity and component referencing, entity parenting hierarchies, along with modular viewport manipulation and debug info rendering. Later in the engine's developement, I also worked on the diagnostics toolset which helped us remove performance bottlenecks of the engine, along with a timewarp system that allowed slomo to be applied to any set of entities in the game at runtime. With help from the rest of the skilled tech team, we were able to create a robust and flexible game engine to drive Isles of Limbo's development.
