# Behemyth (UE4, C++) [In Progress]
 

2019-2020 project at DigiPen, [_Isles of Limbo_](https://store.steampowered.com/app/1389260/Isles_of_Limbo/) is an action packed hack and slash featuring creative enemy designs, scenic ambience, and a wide move set to dispatch foes. Using our team's [custom engine](), we sought to produce a game with eye catching visuals and fast paced gameplay. With hundreds of followers on Steam and dozens of [youtube playthroughs](https://www.youtube.com/results?search_query=isles+of+limbo), the attention this student project got was a gratifying experience.

<div style="display: inline-block; width=100%;">
    <div class="aspect-ratio" style="width:50%; float: right; ">  
        <div style="position: absolute; width: 100%; height: 100%;">

            {% include slideshow.html 
            class="BehemythSlides" index="0"
            img1="Behemyth/ConceptArt1.jpg" caption1="test caption"
            img2="Behemyth/ConceptArt2.jpg" caption2="test caption"
            img3="Behemyth/ConceptArt3.jpg" caption3="test caption"
            img4="Behemyth/ConceptArt4.jpg" caption4="test caption"
            %}

        </div>
    </div>
</div>


<p></p> 
<hr> 
 
# Isles of Limbo (C++/C#)

2019-2020 project at DigiPen, [_Isles of Limbo_](https://store.steampowered.com/app/1389260/Isles_of_Limbo/) is an action packed hack and slash featuring creative enemy designs, scenic ambience, and a wide move set to dispatch foes. Using our team's [custom engine](), we sought to produce a game with eye catching visuals and fast paced gameplay. With hundreds of followers on Steam and dozens of [youtube playthroughs](https://www.youtube.com/results?search_query=isles+of+limbo), the attention this student project got was a gratifying experience.

Areas of responsibility:

> Graphics: Was the team's graphics programmer. Using OpenGL, I implimented core functionality like sprite rendering and Spine animation. Developed tools such as determinate particle system, deferred glow shaders, and stencil culling system. Handled mid-project switch from 2D to 3D assets in a low-impact method. Implemented video streaming for cutscenes.

> Engine Developement: Worked closely with development of the engine's foundation. Worked on instanced entities, serialization, entity and component referencing, parenting hierarchies, and modular viewports. Near end of production, added performance diagnostic toolset and a per-entity timewarp system.

<div class="aspect-ratio">

    {% include youtubePlayer.html id="qTxM9mSe6K4" %}

    <div style="position: absolute; width: 49%; left: 50%; height: 98%;">
        {% include slideshow.html 
        class="IslesOfLimboSlides" index="1"
        img1="IslesOfLimbo/IslesOfLimbo_Gameplay1.PNG" caption1="test caption"
        img2="IslesOfLimbo/IslesOfLimbo_Gameplay2.PNG" caption2="test caption"
        img3="IslesOfLimbo/IslesOfLimbo_Gameplay3.PNG" caption3="test caption"
        img4="IslesOfLimbo/IslesOfLimbo_Gameplay4.PNG" caption4="test caption"
        %}
    </div>

</div>

<p></p>
<hr> 

# Chromatic Split (C++)

Summer of 2019 project at Digipen, [_Chromatic Split_](https://drive.google.com/file/d/1r_M860-sYk4mbykvZJSQm_F5-Ec388Yz/view?usp=sharing) is a multitasking puzzle game where the player navigates multiple characters through color based mazes. With linked movement, conveyor belts, and sliding movement, navigating these mazes are both challenging and satisfying. Completed in 3 months using a school supplied engine framework, the game utilizes a level serialization system that lets developers build mazes using text files.

Areas of responsibility:

> Gameplay Programmer: Developed character collision, character movement, camera dynamics, tile functionality, and menu systems.
 
> Tools: Programmed serialization system for building levels through text files. Engine parses characters, builds tiles, and places player based on these blueprints.

<div class="aspect-ratio">

    {% include youtubePlayer.html id="JcMlbyrXuXQ" %}

    <div style="position: absolute; width: 49%; left: 50%; height: 98%;">
        {% include slideshow.html 
        class="ChromaticSplitSlides" index="2"
        img1="ChromaticSplit/ChromaticSplit_Gameplay1.PNG" caption1="test caption"
        img2="ChromaticSplit/ChromaticSplit_Gameplay2.PNG" caption2="test caption"
        img3="ChromaticSplit/ChromaticSplit_Gameplay3.PNG" caption3="test caption"
        img4="ChromaticSplit/ChromaticSplit_Gameplay4.PNG" caption4="test caption"
        %}
    </div>

</div>

<div id="Modal" class="modal">
    <img id="Modal_img" class="modal-content">
    <div id="modal_caption" class="modal-caption"></div>
</div>

<p></p>

<script>

var images = document.getElementsByClassName("slideshow-image");
for(var i = 0; i < images.length; i++)
{  
    images[i].onclick = function(){
        document.getElementById("Modal").style.display = "block";
        document.getElementById("Modal_img").src = this.src;
        document.getElementById("Modal_caption").innerHTML = this.alt;
    }
}

document.getElementById("Modal").onclick = function(){
    document.getElementById("Modal").style.display = "none";
}

</script>

<script>
var slideIndex = [4,4,4];
var slideId = ["BehemythSlides", "IslesOfLimboSlides", "ChromaticSplitSlides"]
var advanceLock = [false, false, false];
showSlides(1, 0);
showSlides(1, 1);
showSlides(1, 2);

advanceSlides();
function advanceSlides()
{
    for(var i = 0; i < slideId.length; i++)
    {
        if(!advanceLock[i])
            plusSlides(1, i);
        advanceLock[i] = false;
    }
    setTimeout(advanceSlides, 6000);
}

function plusSlides(n, no) {
    showSlides(slideIndex[no] += n, no);
    advanceLock[no] = true;
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
    