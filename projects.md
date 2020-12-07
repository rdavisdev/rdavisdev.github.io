
<h1 style="text-align: center;">Projects</h1>

<hr>
<div id="Clouds" class="headerAnchor"></div>

# Volumetric Clouds (HSLS)

<br>

<div class="aspect-ratio" style="float: right; width:50%; margin: 0px 15px 15px;">  
    <div style="position: absolute; width: 100%; height: 100%;">

        {% include slideshow.html 
        class="CloudSimSlides" index="0"
        img1="CloudSim/CloudSim1.PNG" caption1="test caption"
        img2="CloudSim/CloudSim2.PNG" caption2="test caption"
        img3="CloudSim/CloudSim3.PNG" caption3="test caption"
        img4="CloudSim/CloudSim4.PNG" caption4="test caption"
        %}

    </div>
</div>

Over the Summer of 2020, I had a short period of free time during which I began this project. Following my passion for natural environment rendering, I set out to create a real-time volumetric cloud-scape. Taking inspiration from the [cloud showcase](https://youtu.be/5tHzP00qZMQ?t=69) of a game called UHawk VR, I've been learning from the  creator through his [development blog](https://blog.uhawkvr.com/). Credit to Felix Westin. Thank you!

My current implementation follows this abstract process:
- Generate a modified repeating Voronoi noise volumetric texture
- For each pixel, ray-march while sampling from texture to build cloud color
- For each sample inside cloud, ray-march toward sun to build shadow color
- Combine generated colors with scene texture for transparency

Though method this is still missing several important features from Felix's approach, particularly a signed-distance field for improved performance, I'll be continuing to develop it as time allows. Coincidentally, the [game](https://rdavisdev.github.io/games#Behemyth) I'm working on for school this year ended up having an aerial setting, giving me a practical oportunity to implement what I've learned from this. Stay tuned for updates!

<div style ="clear:both; display: block;">
</div>

<hr>
<div id="Liftoff" class="headerAnchor"></div>

# Liftoff Engine (C++/GLSL)

<br>

<div class="aspect-ratio" style="width:100%;">  
    <div style="position: absolute; width: 100%; height: 100%;">

        {% include slideshow.html 
        class="LiftoffSlides" index="1"
        img1="Liftoff/Liftoff1.JPG" caption1="test caption"
        img2="Liftoff/Liftoff2.JPG" caption2="test caption"
        img3="Liftoff/Liftoff3.JPG" caption3="test caption"
        img4="Liftoff/Liftoff4.JPG" caption4="test caption"
        %}

    </div>
</div>

<br>

Built with a team of 5 programmers to support production of [_Isles of Limbo_](https://rdavisdev.github.io/games#IslesOfLimbo). We aimed to mimic the layout and functionality of Unity closely to allow ease of use. Used [ImGui](https://github.com/ocornut/imgui) for UI, a C# [Mono VM](https://www.mono-project.com/docs/advanced/runtime/) for scripting, and [Spine](http://esotericsoftware.com/)'s C++ Runtime for skeletal animation. My specific contributions are list below.

**Basic Functionality**
- Asset archetypes and instanced spawning
- Level and prefab json serialization
- Transform oriented game objects
- Fontsheet sourced sprite text
- Modifiable tint and opacity for renderables

**Graphics**
- Concurrent viewports for fixed cam gameplay and free cam editing
- Determinate particle system allowing >500,000 particles to update and draw at once
- Channel oriented visual effect linking, allowing multiple objects or particles to share deferred shader passes
- Sprite sourced stencil culling, allowing sprites or particles to act as "viewports" to other sprites or particles.
- SFML driven video file streaming

**UI**
- Details widgets for particle systems, sprites, sprite text, and Spine models
- Sprite source importing tool for aligning frames for sprite text or animations
- Performance diagnostics showing hierarchic breakdown of engine or script performance

**Gameplay**
- Hierachic object transformation
- Per object delta time modifiers

<div style ="clear:both; display: block;">
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
var slideIndex = [4, 4];
var slideId = ["CloudSimSlides", "LiftoffSlides"]
var advanceLock = [false, false];
showSlides(1, 0);
showSlides(1, 1);

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
    