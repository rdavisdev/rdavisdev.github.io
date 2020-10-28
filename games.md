# Isles of Limbo (C++/C#)

2019-2020 project at DigiPen, [_Isles of Limbo_](https://store.steampowered.com/app/1389260/Isles_of_Limbo/) is an action packed hack and slash featuring creative enemy designs, scenic ambience, and a wide move set to dispatch foes with. Using our team's custom built engine, we sought to produce a game with eye catching visuals and fast paced gameplay. With hundreds of followers on Steam and dozens of [youtube playthroughs](https://www.youtube.com/results?search_query=isles+of+limbo), the attention this student project got was a gratifying experience.

Areas of responsibility:

> Graphics: With Argonautic's amazing art team, I was lucky to be the engine's graphics programmer. Using OpenGL, I implimented core functionality like sprite rendering and Spine animations. I also developed tools such as the determinate particle system, deferred glow shaders, and the stencil culling system. I also handled the mid-project switch from 2D to psuedo-3D in a seamless method. Video file streaming was another graphical feature of the engine.

> Engine Developement: Worked closely with the early development of the engine's foundation. Functionality I worked on includes instanced entities, serialization of scenes and assets, entity and component referencing, entity parenting hierarchies, and modular viewports. Later in the project's lifecycle, I added the performance diagnostics toolset and a per-entity timewarp system.

<div class="aspect-ratio">
    <iframe src="https://www.youtube.com/embed/qTxM9mSe6K4" 
        frameborder="0" 
        allowfullscreen>
    </iframe>
</div>

<!-- Trigger the Modal -->
<img id="myImg" src="assets/IslesOfLimb_Gameplay1.jpg" alt="Isles Of Limbo Gameplay" style="width:100%;max-width:300px">

<!-- The Modal -->
<div id="myModal" class="modal">

  <!-- The Close Button -->
  <span class="close">&times;</span>

  <!-- Modal Content (The Image) -->
  <img class="modal-content" id="img01">

  <!-- Modal Caption (Image Text) -->
  <div id="caption"></div>
</div>

<script>
    // Get the modal
var modal = document.getElementById("myModal");

// Get the image and insert it inside the modal - use its "alt" text as a caption
var img = document.getElementById("myImg");
var modalImg = document.getElementById("img01");
var captionText = document.getElementById("caption");
img.onclick = function(){
  modal.style.display = "block";
  modalImg.src = this.src;
  captionText.innerHTML = this.alt;
}

// Get the <span> element that closes the modal
var span = document.getElementsByClassName("close")[0];

// When the user clicks on <span> (x), close the modal
span.onclick = function() {
  modal.style.display = "none";
}
</script>

<p></p>
<hr>

# Chromatic Split (C++)

Summer of 2019 project at Digipen, [_Chromatic Split_]() is a multitasking puzzle game where the player navigates multiple characters through color based mazes. With linked movement, conveyor belts, and sliding movement, navigating these mazes are both challenging and satisfying. Completed in 3 months using a premade engine framework, the game utilized a level serialization system that let our team build mazes using text files. 

Areas of responsibility:

> Gameplay Programmer: Developed collision and movement of characters, along with tile functionality and menu systems.

> Tools: Programmed level serialization system for building mazes with text files.

<div class="aspect-ratio">
    <iframe src="https://www.youtube.com/embed/qTxM9mSe6K4" 
        frameborder="0" 
        allowfullscreen>
    </iframe>
</div>
<p></p>