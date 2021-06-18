<h1 style="text-align: center;">Games</h1>

<hr>
<div id="ProjectNeon" class="headerAnchor"></div>

# Project Neon (UE4/C++)

<br>

<div class="aspect-ratio" style="float: right; width:50%; margin: 0 15px 15px;">  
    <div style="position: absolute; width: 100%; height: 100%;">

        {% include slideshow.html 
        class="NeonSlides" index="0"
        img1="ProjectNeon/Neon1.PNG" caption1="test caption"
        img2="ProjectNeon/Neon2.PNG" caption2="test caption"
        img3="ProjectNeon/Neon3.PNG" caption3="test caption"
        img4="ProjectNeon/Neon4.PNG" caption4="test caption"
        img5="ProjectNeon/Neon5.PNG" caption5="test caption"
        img6="ProjectNeon/Neon6.PNG" caption6="test caption"
        img7="ProjectNeon/Neon7.PNG" caption7="test caption"
        img8="ProjectNeon/Neon8.PNG" caption8="test caption"
        img9="ProjectNeon/Neon9.PNG" caption9="test caption"
        img10="ProjectNeon/Neon10.PNG" caption10="test caption"
        img11="ProjectNeon/Neon11.PNG" caption11="test caption"
        
        %}

    </div>
</div>

<div style="float: right; clear:right; width: 50%; margin: 0 15px 0">
    <p style="text-align: center; margin: 0 0 10px;">
        Video/Installer Coming Soon
    </p> 
</div>

Junior project at DigiPen, _Project Neon_ is a high mobility first person shooter. Play as a cyber-agent tasked with infiltrating and deactivating the rogue AI, Titan. Dash and wall-run over literal firewalls, "hack" through Titan's security mainframe, and confront the AI face to face. Features a wide array of weapons and enemies, fast paced combat, and striking virtual environments.

Areas of responsibility:

> **Scripting**: Built a highly flexible toolset which made scripting level elements and player movement quick and simple. Used this toolset for several of the campaign's sequences.
 
> **Cinematics**: Repurposed a previously developed dynamic fly-cam system into a robust cinematic creation tool. These cinematics are seen during challenge levels and boss introductions.

<div style ="clear:both; display: block;">
</div>


<hr>
<div id="IslesOfLimbo" class="headerAnchor"></div>

# Isles of Limbo (C++/C#/GLSL)

<br>

Sophmore project at DigiPen, [_Isles of Limbo_](https://store.steampowered.com/app/1389260/Isles_of_Limbo/) is an action packed hack and slash featuring creative enemy designs, scenic ambience, and a wide move set to dispatch foes. Using our team's [custom engine](https://rdavisdev.github.io/projects#Liftoff), we sought to produce a game with eye catching visuals and fast paced gameplay. With hundreds of followers on Steam and dozens of [youtube playthroughs](https://www.youtube.com/results?search_query=isles+of+limbo), the attention this student project got was a gratifying experience.

Areas of responsibility:

> **Graphics**: Team's graphics programmer. Using OpenGL, implimented core functionality like sprite rendering and Spine animation. Developed graphical features including high-capacity particle system, deferred glow effect, and custom stencil culling. Handled mid-project switch from 2D to 3D assets in a low-impact method. Implemented video file streaming for in-game cutscenes.

> **Engine Developement**: Worked closely with development of the engine's foundation. Instanced entities, serialization, entity and component referencing, parenting hierarchies, and modular viewports were my contributions. Near the end of production, added performance diagnostic toolset and entity timewarp system.

<div class="aspect-ratio">

    {% include youtubePlayer.html id="qTxM9mSe6K4" %}

    <div style="position: absolute; width: 49%; left: 50%; height: 98%; margin: 0 5px 0;">
        {% include slideshow.html 
        class="IslesOfLimboSlides" index="1"
        img1="IslesOfLimbo/IslesOfLimbo_Gameplay1.PNG" caption1="test caption"
        img2="IslesOfLimbo/IslesOfLimbo_Gameplay2.PNG" caption2="test caption"
        img3="IslesOfLimbo/IslesOfLimbo_Gameplay3.PNG" caption3="test caption"
        img4="IslesOfLimbo/IslesOfLimbo_Gameplay4.PNG" caption4="test caption"
        %}
    </div>

</div>

<hr>
<div id="ChromaticSplit" class="headerAnchor"></div>

# Chromatic Split (C++)

<br>

Freshmen Summer project at Digipen, [_Chromatic Split_](https://drive.google.com/file/d/1r_M860-sYk4mbykvZJSQm_F5-Ec388Yz/view?usp=sharing) is a multitasking puzzle game where the player navigates multiple characters through color based mazes. With linked movement, conveyor belts, and sliding movement, navigating these mazes are both challenging and satisfying. Completed in 3 months using a school supplied engine framework, the game utilizes a level serialization system that lets developers build mazes using text files.

Areas of responsibility:

> **Gameplay Programmer**: Character collision, character movement, camera dynamics, tile functionality, and menu systems.
  
> **Tools**: Serialization system for building levels through text files. System parses characters, builds tiles, and places player based on these blueprints.

<div class="aspect-ratio">

    {% include youtubePlayer.html id="JcMlbyrXuXQ" %}
 
    <div style="position: absolute; width: 49%; left: 50%; height: 98%; margin: 0 5px 0;">
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
var slideId = ["NeonSlides", "IslesOfLimboSlides", "ChromaticSplitSlides"]
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
    