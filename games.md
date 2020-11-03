# Isles of Limbo (C++/C#)

2019-2020 project at DigiPen, [_Isles of Limbo_](https://store.steampowered.com/app/1389260/Isles_of_Limbo/) is an action packed hack and slash featuring creative enemy designs, scenic ambience, and a wide move set to dispatch foes with. Using our team's [custom engine](), we sought to produce a game with eye catching visuals and fast paced gameplay. With hundreds of followers on Steam and dozens of [youtube playthroughs](https://www.youtube.com/results?search_query=isles+of+limbo), the attention this student project got was a gratifying experience.

Areas of responsibility:

> Graphics: With Argonautic's amazing art team, I was lucky to be the engine's graphics programmer. Using OpenGL, I implimented core functionality like sprite rendering and Spine animations. I also developed tools such as the determinate particle system, deferred glow shaders, and the stencil culling system. I also handled a mid-project switch from 2D to psuedo-3D in a seamless method. Video file streaming was another graphical feature of the engine.

> Engine Developement: Worked closely with the early development of the engine's foundation. Functionality I worked on includes instanced entities, serialization of scenes and assets, entity and component referencing, entity parenting hierarchies, and modular viewports. Later in the project's lifecycle, I added the performance diagnostics toolset and a per-entity timewarp system.

<div class="aspect-ratio">

    {% include youtubePlayer.html id="qTxM9mSe6K4" %}

    {% include slideshow.html 
    class="IslesOfLimboSlides"
    img1="IslesOfLimbo_Gameplay1.jpg" caption1="test caption"
    img2="IslesOfLimbo_Gameplay2.jpg" caption2="test caption"
    img3="IslesOfLimbo_Gameplay1.jpg" caption3="test caption"
    img4="IslesOfLimbo_Gameplay2.jpg" caption4="test caption"
    %}

</div>

<p></p>
<hr>

# Chromatic Split (C++)

Summer of 2019 project at Digipen, [_Chromatic Split_]() is a multitasking puzzle game where the player navigates multiple characters through color based mazes. With linked movement, conveyor belts, and sliding movement, navigating these mazes are both challenging and satisfying. Completed in 3 months using a premade engine framework, the game utilizes a level serialization system that lets developers build mazes using text files.

Areas of responsibility:

> Gameplay Programmer: Developed collision and movement of characters, along with tile functionality and menu systems.

> Tools: Programmed level serialization system for building mazes with text files.

<div class="aspect-ratio">

    {% include youtubePlayer.html id="qTxM9mSe6K4" %}


    {% include slideshow.html
    class="ChromaticSplitSlides"
    img1="IslesOfLimbo_Gameplay1.jpg" caption1="test caption"
    img2="IslesOfLimbo_Gameplay2.jpg" caption2="test caption"
    img3="IslesOfLimbo_Gameplay1.jpg" caption3="test caption"
    img4="IslesOfLimbo_Gameplay2.jpg" caption4="test caption"
    %}

</div>
<p></p>

{% include modal.html ID="IslesOfLimbo_Gameplay1" %}
{% include modal.html ID="IslesOfLimbo_Gameplay2" %}
{% include modal.html ID="IslesOfLimbo_Gameplay3" %}
{% include modal.html ID="IslesOfLimbo_Gameplay4" %}
{% include modal.html ID="IslesOfLimbo_Gameplay5" %}
{% include modal.html ID="IslesOfLimbo_Gameplay6" %}
{% include modal.html ID="IslesOfLimbo_Gameplay7" %}
{% include modal.html ID="IslesOfLimbo_Gameplay8" %}

<script>
    var slideIndex = [1,1];
    var slideId = ["IslesOfLimboSlides", "ChromaticSplitSlides"]
    showSlides(1, 0);
    showSlides(1, 1);
    
    function plusSlides(n, no) {
      showSlides(slideIndex[no] += n, no);
    }
    
    function showSlides(n, no) {
      var i;
      var x = document.getElementsByClassName(slideId[no]);
      if (n > x.length) {slideIndex[no] = 1}    
      if (n < 1) {slideIndex[no] = x.length}
      for (i = 0; i < x.length; i++) {
         x[i].style.display = "none";  
      }
      x[slideIndex[no]-1].style.display = "block";  
    }
</script>
    